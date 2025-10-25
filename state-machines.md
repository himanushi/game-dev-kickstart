# ゲーム開発におけるステートマシン

## ステートマシンとは？

ステートマシン（State Machine、状態機械）は、ゲーム開発において**キャラクターの行動**、**アニメーション**、**ゲームフロー**などを管理する基本的かつ重要な設計パターンです。

JavaScriptの**XState**のように、ゲームエンジンにもステートマシンの仕組みが組み込まれています。

## ステートマシンの種類

### 1. **FSM（Finite State Machine / 有限ステートマシン）**
- 最も基本的なステートマシン
- 状態（State）と遷移（Transition）で構成
- 例: 待機 → 歩行 → ジャンプ → 着地 → 待機

### 2. **HFSM（Hierarchical FSM / 階層型FSM）**
- ステートマシンの中にステートマシンをネスト
- 複雑な挙動を整理できる

### 3. **ビヘイビアツリー（Behavior Tree）**
- FSMの代替/補完として使われる
- AI開発でより柔軟な挙動を実現

## 各ゲームエンジンのステートマシン実装

### Unity

#### 1. **Animation State Machine（アニメーションステートマシン）**
- Unityの**Animator Controller**に組み込み
- アニメーションクリップの遷移を視覚的に管理
- ユーザー入力やゲームイベントでアニメーション切り替え

#### 2. **コードベースのFSM実装**
人気のライブラリ・アセット：
- **ImtStateMachine**: ピュアC#の軽量・高速ライブラリ、サーバーサイドや大規模プロジェクト向け
- **Playmaker**: ビジュアルスクリプティング対応
- **NodeCanvas**: ノードベースでステート遷移を表現
- **Arbor 3**: ビジュアルスクリプティング、ノード接続でステート遷移

#### メリット:
- 仕様の食い違いやバグを減らせる
- ステート遷移図により、仕様変更時の影響範囲が明確

### Godot

#### **AnimationTree + StateMachine**
- **AnimationTree**ノードでステートマシンを構築
- **AnimationNodeStateMachine**でアニメーション管理
- `travel()`メソッドで指定したアニメーションへ遷移
- Unityと似た視覚的なステートマシン

#### コードベースの実装:
- **StateMachine.gd**: スクリプトでステート変更、イベント対応、前の状態への復帰が可能
- シンプルな実装では`if`や`switch`文を使用（状態が少ない場合）

### Unreal Engine
- **Blueprint**や**Animation Blueprint**にステートマシンが組み込まれている
- ビヘイビアツリーと組み合わせてAI構築

### Bevy（Rust）
- **ECSアーキテクチャ**に基づくステート管理
- `iyes_loopless`などのステートマシンクレート（ライブラリ）を使用
- コンポーネントベースでステートを表現

### JavaScript（Web/HTML5ゲーム）

#### **XState + Phaser.js**
- **Phaser.js**: HTML5の2Dゲームフレームワーク（JavaScript/TypeScript）
- **XState**: FSMとステートチャートを使った状態管理ライブラリ
- 組み合わせ事例あり（例: [xstate-game on GitHub](https://github.com/malcolm-kee/xstate-game)）
- 階層的なステートマシン構造が可能
  - トップレベル: メニュー/プレイ状態
  - ネスト: プレイ中の回転/推進/武器などの状態

#### 課題:
- 両方初めての場合は学習曲線が急
- XStateをアプリのどこに配置するか設計が重要

## FSM vs ビヘイビアツリー

### FSM（Finite State Machine）の特徴

#### ✅ 強み:
1. **シンプルで理解しやすい**: 直感的、少数の状態ならベスト
2. **実装が簡単**: ゼロから構築しやすい
3. **明確な遷移**: 特定の状態間で明確な遷移条件

#### ⚠️ 弱み:
1. **スケールしにくい**: 状態が増えると複雑化・脆弱化
2. **実行時の変更に弱い**: 遷移の再編成が必要
3. **メンテナンスが困難**: 大規模になると変更が怖くなる

### ビヘイビアツリー（Behavior Tree）の特徴

#### ✅ 強み:
1. **柔軟性**: ゲーム状態に応じた反応が容易
2. **変更しやすい**: ビジュアルエディタで編集が簡単
3. **複雑な挙動**: 様々な状況に対応しやすい

#### ⚠️ 弱み:
- AI以外の用途では過剰な場合がある

### ハイブリッドアプローチ 🔥

**FSM + ビヘイビアツリーの融合**が最強：
- **ビヘイビアツリー**: AIのフロー（意思決定）を記述
- **FSM**: 機能（アニメーション、状態）を記述
- あるデベロッパーは10状態で苦労していたのが、40状態以上を2週間で管理できるようになった

## ステートマシンの実装例（シンプルな場合）

### パターン1: switch文（シンプル）

```csharp
// Unity C# 例
enum PlayerState { Idle, Walking, Jumping, Falling }
PlayerState currentState = PlayerState.Idle;

void Update() {
    switch (currentState) {
        case PlayerState.Idle:
            // 待機処理
            if (Input.GetKey(KeyCode.Space))
                currentState = PlayerState.Jumping;
            break;
        case PlayerState.Jumping:
            // ジャンプ処理
            if (velocity.y < 0)
                currentState = PlayerState.Falling;
            break;
        // ...
    }
}
```

**問題点**: 状態が増えると冗長で保守が困難に

### パターン2: クラスベース（拡張性高）

```csharp
// Unity C# 例
public interface IState {
    void Enter();
    void Execute();
    void Exit();
}

public class StateMachine {
    private IState currentState;

    public void ChangeState(IState newState) {
        currentState?.Exit();
        currentState = newState;
        currentState?.Enter();
    }

    public void Update() {
        currentState?.Execute();
    }
}

public class IdleState : IState {
    public void Enter() { /* 待機開始 */ }
    public void Execute() { /* 毎フレーム処理 */ }
    public void Exit() { /* 待機終了 */ }
}
```

### パターン3: GodotのGDScript例

```gdscript
# StateMachine.gd
extends Node

var current_state = null

func change_state(new_state):
    if current_state:
        current_state.exit()
    current_state = new_state
    current_state.enter()

func _process(delta):
    if current_state:
        current_state.update(delta)
```

## ステートマシンが使われる場面

### 1. **キャラクターの挙動**
- プレイヤー: 待機/歩行/走行/ジャンプ/攻撃/ダメージ/死亡
- 敵AI: 巡回/追跡/攻撃/逃走/警戒

### 2. **アニメーション管理**
- アニメーションクリップの切り替え
- ブレンド（混合）処理

### 3. **ゲームフロー**
- タイトル → メニュー → ゲームプレイ → ポーズ → ゲームオーバー → リザルト

### 4. **UI状態**
- メニュー階層の管理
- ダイアログの表示/非表示

### 5. **カットシーン/イベント**
- イベントシーケンスの管理

## ステートマシン設計のベストプラクティス

### ✅ DO（推奨）
1. **状態遷移図を描く**: 仕様を可視化して共有
2. **Enter/Update/Exit**を明確に分ける
3. **状態の責務を明確にする**: 1つの状態は1つの役割
4. **階層化を検討**: 複雑になったらHFSMへ
5. **ビヘイビアツリーとの併用**: AIには特に有効

### ❌ DON'T（避けるべき）
1. **全てを1つのステートマシンに詰め込まない**
2. **状態数が多すぎる場合は設計を見直す**（10状態超えたら要注意）
3. **遷移条件が複雑すぎる場合**: ビヘイビアツリーへの移行を検討

## 各エンジンでのステートマシン対応まとめ

| エンジン | ビルトイン | ビジュアルエディタ | コードベース | 推奨ライブラリ |
|---------|----------|-----------------|------------|-------------|
| Unity | Animator | あり | C# | ImtStateMachine, Playmaker |
| Godot | AnimationTree | あり | GDScript | StateMachine.gd |
| Unreal | Animation BP | あり | C++/Blueprint | ビヘイビアツリー |
| Bevy | なし | なし | Rust | iyes_loopless |
| Phaser.js | なし | なし | JS/TS | XState |

## XState風のライブラリを各言語で

- **JavaScript/TypeScript**: XState（最強）
- **C#（Unity）**: Stateless, ImtStateMachine
- **Rust（Bevy）**: state_machine_future, iyes_loopless
- **Python**: python-statemachine, transitions
- **GDScript（Godot）**: 組み込みAnimationTree、カスタムStateMachine.gd

## まとめ

ゲーム開発において、ステートマシンは**基本中の基本**です：

1. **キャラクター挙動、アニメーション、ゲームフロー**すべてに使われる
2. **各エンジンに組み込み**または専用ライブラリがある
3. **XStateのようなもの**は各エンジン/言語に存在する
4. **シンプルな場合はFSM**、**複雑なAIにはビヘイビアツリー**
5. **FSM + ビヘイビアツリーの併用**が最も強力

初心者は**まずシンプルなFSMから始める**のがおすすめです！
