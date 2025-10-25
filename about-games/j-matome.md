この動画は、ゲーム開発におけるUI（ユーザーインターフェイス）制作にまつわる様々な話題をまとめたものです。

---

### 1. UIの基本とスタイル性
* UIとはユーザーインターフェイスの略で、メニューや画面上の表示系を指します [[00:15](http://www.youtube.com/watch?v=33njSckMINk&t=15)]。
* **分かりやすいUI**と**スタイル性の高いUI**は相反することがあるとし、『ペルソナ』シリーズのスタイリッシュなUIを例に挙げています [[00:43](http://www.youtube.com/watch?v=33njSckMINk&t=43)]。
* UIは「引き出し」のようなもので、単純に分かりやすければ良い、分かりにくければ悪いとは言い切れず、ゲーム内の目的に合わせることが重要です [[01:19](http://www.youtube.com/watch?v=33njSckMINk&t=79)]。
* 利便性とスタイルのどちらを優先するかはゲームによって異なり、正解はないため、ゲームの内容や世界観に合うようにデザインすることが求められます [[03:02](http://www.youtube.com/watch?v=33njSckMINk&t=182)]。

### 2. 言語による文字の大きさの違い
* 適切な文字の大きさは言語によって変わり、特に漢字を使う日本語や中国語は、アルファベットを使う言語よりも1文字あたりの情報量が多いため、より大きなスペースを使います [[03:32](http://www.youtube.com/watch?v=33njSckMINk&t=212)]。
* 英語のみを前提としたレイアウトを組むと、日本語で文字が小さくなりすぎる問題が発生することがあります [[04:44](http://www.youtube.com/watch?v=33njSckMINk&t=284)]。
* 最近は制作者が気を配るようになったことや、ゲーム機の解像度向上により、フォントの大きさを選べる設定を持つゲームも出てきており、これは非常に丁寧な対応だと評価しています [[04:52](http://www.youtube.com/watch?v=33njSckMINk&t=292)]。
* 携帯ゲーム機を前提とする作品では、フォントは比較的大きく組まれることが多いです [[05:26](http://www.youtube.com/watch?v=33njSckMINk&t=326)]。

### 3. 『The Last of Us Part I』に見るアクセシビリティ
* PS5の『The Last of Us Part I』のオプションは、アクセシビリティ（利用のしやすさ）において特に丁寧な対応をしており、非常に参考になると紹介されています [[06:37](http://www.youtube.com/watch?v=33njSckMINk&t=397)]。
* **アクセシビリティの主な項目例：**
    * HUD（ヘッドアップディスプレイ）の大きさ変更やプレビュー表示 [[07:41](http://www.youtube.com/watch?v=33njSckMINk&t=461)]
    * 色彩調整やハイコントラスト表示（色覚対応） [[08:16](http://www.youtube.com/watch?v=33njSckMINk&t=496)]
    * 画面酔い対策としてのカメラや演出の調整 [[08:44](http://www.youtube.com/watch?v=33njSckMINk&t=524)]
    * ゲーム進行のヒントとなるナビゲーションや移動の音響 [[09:12](http://www.youtube.com/watch?v=33njSckMINk&t=552)]
    * テキスト読み上げ機能 [[09:58](http://www.youtube.com/watch?v=33njSckMINk&t=598)]
    * 戦闘アクセシビリティ（敵が逃げなくなる、スローモーションなど）や、視認不可の切り替え（実質無敵モード）といった、難易度に大きく影響する項目 [[11:15](http://www.youtube.com/watch?v=33njSckMINk&t=675)]
    * 多数の項目をまとめて設定できるプリセットの用意 [[12:14](http://www.youtube.com/watch?v=33njSckMINk&t=734)]
* また、コントローラー操作のカスタマイズ、デュアルセンス専用の設定、字幕の大きさや背景の調整など、多様なユーザーのニーズに対応する詳細なオプションが用意されている点を評価しています [[12:33](http://www.youtube.com/watch?v=33njSckMINk&t=753)]。
* ゲームを遊ぶ人が多様化している今、ユーザー好みに設定を変えられることは必要なことだと述べています [[17:13](http://www.youtube.com/watch?v=33njSckMINk&t=1033)]。

### 4. ローディング表示の考え方
* ロード時間は歓迎されないため、初代『バイオハザード』の扉の演出のように、ローディング時間をゲームの演出で補う手法があります [[18:09](http://www.youtube.com/watch?v=33njSckMINk&t=1089)]。
* 現代のゲームではスピード感が求められ、ハードの読み込み速度も速くなっているため、単なる待ち時間はほとんど許容されません [[18:47](http://www.youtube.com/watch?v=33njSckMINk&t=1127)]。
* ローディングを演出でごまかせない場合は、今ローディングをしていると素直に表示する方がユーザーは納得しやすいです [[19:00](http://www.youtube.com/watch?v=33njSckMINk&t=1140)]。
* 開発時と完成時でロード時間が変わることが多いため、演出に依存せず、どこにでも表示できるシンプルなロードマークを使うのが良いとしています [[19:20](http://www.youtube.com/watch?v=33njSckMINk&t=1160)]。

### 5. テキストの演出制御
* テキストを読み進めるタイプの作品では、文字の大きさや色、アニメーション、フォントを変えるなどの**文字演出**が重要です [[20:11](http://www.youtube.com/watch?v=33njSckMINk&t=1211)]。
* 文字演出はキャラクターの感情を伝えたり、ゲーム展開に彩りを加えます [[20:40](http://www.youtube.com/watch?v=33njSckMINk&t=1240)]。
* 翻訳を行う際、言語によって適切な強調方法が異なるため、翻訳者が演出設定（スクリプト）を直接調整できるようにしておくのが良いと提言しています [[21:11](http://www.youtube.com/watch?v=33njSckMINk&t=1271)]。
* 日本のコミック文化には、書き文字や漫符など豊かな表現方法があり、それをゲームのテキスト表示にも活かす価値があるとしています [[21:23](http://www.youtube.com/watch?v=33njSckMINk&t=1283)]。

### 6. フォントとUIデザインによる世界観の構築
* UIやフォントの使い方一つで、ターゲット層を変えたり、ゲームの世界観を表現したりすることができます（例：クール系、可愛い系、和風など） [[22:47](http://www.youtube.com/watch?v=33njSckMINk&t=1367)]。
* キャラクターや背景をデザインするのに比べ、フォントを変えることで世界観の構成につながるなら比較的楽な方法であり、見やすさを維持しつつ積極的にデザインすべきだと述べています [[23:43](http://www.youtube.com/watch?v=33njSckMINk&t=1423)]。
* フォントだけでなく、色合いや装飾も含めて、UIはゲームの世界をパッケージングするものです [[24:14](http://www.youtube.com/watch?v=33njSckMINk&t=1454)]。

### 7. メニューの色分けとアイコンの大小
* 桜井氏がディレクションする企画では、メニューを色分けすることが多いです（例：『スマブラSP』） [[24:46](http://www.youtube.com/watch?v=33njSckMINk&t=1486)]。
* デザインを損なうため、同じ画面で色を混ぜこぜにしない方が良いと推奨しています [[25:47](http://www.youtube.com/watch?v=33njSckMINk&t=1547)]。
* 文字を読むより絵や色を見る方が直感的に情報処理できるため、メニューにキャラクターなどの絵を入れることは有効です [[26:21](http://www.youtube.com/watch?v=33njSckMINk&t=1581)]。
* 桜井氏のUIの特徴として、**重要度に応じてアイコンの大きさを変える**手法があります（『メテオス』以降） [[27:08](http://www.youtube.com/watch?v=33njSckMINk&t=1628)]。
    * これはよく使われるモードを大きくすることで、ユーザーにアクセスを促すのが目的です [[27:37](http://www.youtube.com/watch?v=33njSckMINk&t=1657)]。
    * ゲームキューブのコントローラーのボタンの大小も、この思想に近いと分析しています [[27:50](http://www.youtube.com/watch?v=33njSckMINk&t=1670)]。



http://googleusercontent.com/youtube_content/0


















はい、YouTube動画「J: UI2 (まとめ動画) #09～#15」の要約は以下の通りです。

この動画は、ゲーム開発者である桜井政博氏が、より良いUI（ユーザーインターフェース）を実現するための様々な提案や工夫について語った、過去の話題のまとめです。

### 1. コントローラーへの「ホイール」の要望 [[00:27](http://www.youtube.com/watch?v=T8AlCmksaGA&t=27)]
* ゲームキューブの開発時や『スマブラデラックス』の企画時から、コントローラーにマウスのような**「ホイール」**（ジョグダイヤル）を搭載してほしいと提案していました。
* ホイールがあれば、メニュー選択などが格段に速くなり、ゲーム内の様々な指定操作が便利になると考えていました [[00:53](http://www.youtube.com/watch?v=T8AlCmksaGA&t=53)]。
* クリック感のあるホイールであれば、操作の実体感も増すとしています [[01:27](http://www.youtube.com/watch?v=T8AlCmksaGA&t=87)]。
* アナログスティックを「コンコンコン」と倒してメニューを選択する現状に満足できていないと述べています [[01:53](http://www.youtube.com/watch?v=T8AlCmksaGA&t=113)]。

### 2. デモ・ムービーは必ずスキップ・ポーズ可能に [[03:00](http://www.youtube.com/watch?v=T8AlCmksaGA&t=180)]
* 会社ロゴ、オープニング、イベントなど、ゲームをプレイしていない瞬間の表示は、**必ずスキップできるようにする**べきです [[03:07](http://www.youtube.com/watch?v=T8AlCmksaGA&t=187)]。
* プレイヤーが初めて見る場合とは限らず、映像作品と同じく、早送りやスキップができないのは不便そのものだと指摘しています [[03:31](http://www.youtube.com/watch?v=T8AlCmksaGA&t=211)]。
* ロゴなどはガイドラインでスキップできない場合もあるが、時代に合わないため、ガイドライン自体もスキップを前提に設定すべきと提案しています [[03:51](http://www.youtube.com/watch?v=T8AlCmksaGA&t=231)]。
* ムービーはスキップだけでなく、**必ずポーズ（停止）できる**ようにすべきです [[04:21](http://www.youtube.com/watch?v=T8AlCmksaGA&t=261)]。電話や来客などで手を止める事情は多いため、途中で止められないのは不便です [[04:33](http://www.youtube.com/watch?v=T8AlCmksaGA&t=273)]。

### 3. ボタン設定（キーコンフィグ）の必要性と工夫 [[05:18](http://www.youtube.com/watch?v=T8AlCmksaGA&t=318)]
* シンプルな作品であっても、必ず**ボタン設定（キーコンフィグ）**をできるようにすべきだと述べています [[05:21](http://www.youtube.com/watch?v=T8AlCmksaGA&t=321)]。
* 制作上の工夫として、以下の点を挙げています。
    * **コントローラーをグラフィカルに表現**し、視覚的に分かりやすくする [[06:05](http://www.youtube.com/watch?v=T8AlCmksaGA&t=365)]。
    * 変更したいボタンをカーソルで指定し、そこに入ってから該当ボタンを押す設定方法を採用 [[06:20](http://www.youtube.com/watch?v=T8AlCmksaGA&t=380)]。
    * 操作の**重複を許容**する（例：『スマブラ』でジャンプボタンを2つ設定可能） [[06:53](http://www.youtube.com/watch?v=T8AlCmksaGA&t=413)]。
    * ボタン設定を**プレイヤーの「お名前」に記録**し、対戦などで簡単に設定を呼び出せるようにする [[07:08](http://www.youtube.com/watch?v=T8AlCmksaGA&t=428)]。
* PS5で決定ボタンが世界標準の「×」に統一されたことで、Switchだけが決定・キャンセルが逆になってしまったという現状についても触れ、ボタン設定画面を作るのは大変だが、必要としているユーザーのために対応していくべきだと述べています [[07:26](http://www.youtube.com/watch?v=T8AlCmksaGA&t=446)]。

### 4. テキストの表示速度と音声の早送り [[08:37](http://www.youtube.com/watch?v=T8AlCmksaGA&t=517)]
* 人はテロップ（字幕）を読む方が早いので、ゲーム内のテキストはポンポンと読めると気持ちが良い [[08:47](http://www.youtube.com/watch?v=T8AlCmksaGA&t=527)]。
* 演技が付いているデモではスピーディに進められないが、プレイヤーとしてはなるべく**早送りできるようにしてほしい** [[09:15](http://www.youtube.com/watch?v=T8AlCmksaGA&t=555)]。
* セリフ単位で飛ばせるようにするのが望ましい [[09:33](http://www.youtube.com/watch?v=T8AlCmksaGA&t=573)]。
* 映像作品では倍速再生が一般化しており、ゲームでも**セリフ飛ばし対応**をすることで、多くの人が幸せになると提案しています [[10:13](http://www.youtube.com/watch?v=T8AlCmksaGA&t=613)]。

### 5. メニューの「ヘルプ」と分かりやすい言葉遣い [[11:31](http://www.youtube.com/watch?v=T8AlCmksaGA&t=691)]
* メニューの機能が単語だけでは分かりにくい場合があるため、その機能説明である**「ヘルプ」を積極的に入れる**べきです [[11:45](http://www.youtube.com/watch?v=T8AlCmksaGA&t=705)]。
* ヘルプを作る際の注意点として、**メニューと同じ言葉で説明しない**ことを強調しています [[12:18](http://www.youtube.com/watch?v=T8AlCmksaGA&t=738)]。
    * 例：「オプション」の説明を「オプションに行く」としない [[12:34](http://www.youtube.com/watch?v=T8AlCmksaGA&t=754)]。
    * ヘルプは「ゲーム内の様々な設定をする」といったように、意味が頭にすっと入るような、**噛み砕いた違う言葉で説明**すべき [[12:53](http://www.youtube.com/watch?v=T8AlCmksaGA&t=773)]。
* 専門用語を避け、「コンフィグ」より「ボタン設定」、「シングルモード」より「1人で遊ぶ」といったように、分かりやすい言葉を選ぶ [[13:31](http://www.youtube.com/watch?v=T8AlCmksaGA&t=811)]。
* 日本語では**ひらがなを開く**（例：「一人用」→「1人 用」）ことで、より理解しやすくなると説明しています [[13:51](http://www.youtube.com/watch?v=T8AlCmksaGA&t=831)]。

### 6. 言葉が分からなくてもゲームができる工夫 [[14:18](http://www.youtube.com/watch?v=T8AlCmksaGA&t=858)]
* 言葉が分からなくてもゲームができるよう、可能であれば**アイコンに絵やキャラクターを入れる**ことを推奨 [[14:23](http://www.youtube.com/watch?v=T8AlCmksaGA&t=863)]。
    * 単純に楽しいだけでなく、絵を見て何ができるか理解できるようにする [[14:40](http://www.youtube.com/watch?v=T8AlCmksaGA&t=880)]。
* トップメニューからボタン連打した際に、**基本的なメインゲームに入れる**ように意図的に作っている [[15:29](http://www.youtube.com/watch?v=T8AlCmksaGA&t=929)]。
    * 例：『スマブラSP』では連打で大乱闘のファイターセレクトまで進む [[15:36](http://www.youtube.com/watch?v=T8AlCmksaGA&t=936)]。
    * 最悪文字が読めなくてもゲームができるのが理想としています [[16:23](http://www.youtube.com/watch?v=T8AlCmksaGA&t=983)]。

### 7. HUD（ヘッドアップディスプレイ）の工夫 [[16:48](http://www.youtube.com/watch?v=T8AlCmksaGA&t=1008)]
* HUDは画面に表示するインフォメーションの総称です [[17:22](http://www.youtube.com/watch?v=T8AlCmksaGA&t=1042)]。
* 日本の作品は情報が多くなりがちで、海外作品は没入感を重視し情報を抑える傾向があると感じている [[17:39](http://www.youtube.com/watch?v=T8AlCmksaGA&t=1059)]。
* 『スマブラ』シリーズでのHUDの工夫として、以下の例を挙げています。
    * ファイターの顔を出すことで、キャラクター性を高める（観戦者にも有効） [[18:24](http://www.youtube.com/watch?v=T8AlCmksaGA&t=1104)]。
    * 背景に模様を入れ、UVスクロールさせることで、戦っている闘志に燃えている雰囲気を出す [[18:37](http://www.youtube.com/watch?v=T8AlCmksaGA&t=1117)]。
    * 画面外にある味方カーソルは、常に表示せず、距離や状況によって見え隠れするようにしている [[18:52](http://www.youtube.com/watch?v=T8AlCmksaGA&t=1132)]。
    * 『カービィのエアライド』では、コピー能力でメーター表示が変わる、マシンが壊れるとメーターも破壊される [[19:04](http://www.youtube.com/watch?v=T8AlCmksaGA&t=1144)]。
* HUDは「ゲームがやりやすくなる、あるいは面白くなる」という前提で設定する必要があると締めくくっています [[19:50](http://www.youtube.com/watch?v=T8AlCmksaGA&t=1190)]。

***

**この動画はこちらです。**
[J: UI2 (まとめ動画) #09～#15](http://www.youtube.com/watch?v=T8AlCmksaGA)


http://googleusercontent.com/youtube_content/0


