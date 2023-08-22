# LightsUp!

# 始めるための前提条件

1. フラッターをインストールする - [https://docs.flutter.dev/get-started/install](https://docs.flutter.dev/get-started/install)
2. IDE をセットアップしてください - [https://docs.flutter.dev/get-started/editor?tab=vscode](https://docs.flutter.dev/get-started/editor?tab=vscode)
3. テストドライブ - [https://docs.flutter.dev/get-started/test-drive?tab=vscode](https://docs.flutter.dev/get-started/test-drive?tab=vscode)
4. 最初のアプリを書く - [https://codelabs.developers.google.com/codelabs/flutter-codelab-first#0](https://codelabs.developers.google.com/codelabs/flutter-codelab-first#0)

# 続けるためのリソース

1. ダートプログラミング言語-[https://dart.dev/language](https://dart.dev/language)
2. ダートチートシートコーディングラボ-[https://dart.dev/codelabs/dart-cheatsheet](https://dart.dev/codelabs/dart-cheatsheet)
3. リバーポッド - [https://codewithandrea.com/articles/flutter-state-management-riverpod/](https://codewithandrea.com/articles/flutter-state-management-riverpod/)

# 目的

Android および iOS 上で実行されるモバイル アプリを作成して、前の章で学んださまざまな MQTT の概念を導入し、他の MQTT 機能をさらに拡張します。

このアプリには次の機能が導入されています。

- 認証された MQTT クライアント接続を動的に作成してセキュリティを強化
- ESP8266 NodeMCU の内蔵 LED ライトをオン/オフして制御する機能
- 1 つのクライアントはライトを制御でき、別のクライアントはライトがオンであるかどうかに関係なくリアルタイムでリッスンできます。
- モバイルアプリと ESP8266 LED の両方に表示される MQTT メッセージのリアルタイム処理

# どこから始めればよいでしょうか?

GitHub リポジトリは、フロントエンドの構築に必要なすべてのコードを備えた簡単な開始点としてセットアップされます。 MQTT 通信に焦点を当てていますので、一緒に見ていきます。

この git リポジトリのクローンを作成し、`start/lights-up` ブランチをチェックアウトまたはダウンロードします。

[https://github.com/ahdzlee/iPBL2023-PreTraining/tree/start/lights-up/mobile/lights_up](https://github.com/ahdzlee/iPBL2023-PreTraining/tree/start/lights-up/mobile/lights_up)

# ビデオレッスン

アプリを実行して目標を達成するために、実践的なビデオ セッションが作成されています。以下のリンクを推奨される順序で参照してください。

1. [概要とプロジェクトの構造](https://youtu.be/FbndnKULc8E)
   - ここでは、注意が必要な関連プロジェクト ファイルと、Visual Studio Code でプロジェクトを実行する方法を示します。
1. [MQTT クライアント マネージャーを作成する](https://youtu.be/Xg-AAr1IL2E)
   - MQTT メッセージの接続、切断、サブスクライブ、パブリッシュを処理するクラスを実装します。マネージャーは、サブスクリプションの更新をリッスンするストリームも公開します。
1. [MQTT クライアント接続を作成する](https://youtu.be/2Yv1fI4ulR8)
   - MQTT クライアント マネージャーを使用してブローカーへのクライアント接続を作成する方法を示します。
1. [Riverpod を使用してアプリの接続状態の変化を追跡する](https://youtu.be/mP_LQKsqJj0)
   - Riverpod を使用してアプリの状態変更を管理する方法を示します。アプリの接続ライフサイクルの変更と、状態が変化したときにユーザー インターフェイスを更新する方法を示します。
1. [認証されたクライアント接続を作成する](https://youtu.be/eVuhqOFzBeU)
   - ブローカーで資格情報を受け入れることによって認証をアクティブ化する方法を示します。また、アプリは未承認の例外を処理し、クライアント接続の確立を防ぎます。
1. [ライトをオン/オフするイベントを発行する](https://youtu.be/3-4AGUBcNqU)
   - ペイロードをブローカーに送信し、MQTTX 経由でテストする
1. [MQTT トピックを購読する](https://youtu.be/mUgx4FV6ovY)
   - MQTT トピックをサブスクライブし、サブスクライブされた受信 MQTT メッセージを継続的にリッスンする方法を示します。
1. [ESP8266 NodeMCU でのパブリッシュ/サブスクライブ実装](https://youtu.be/pBd3tbD6LB8)
   - 内部 LED のオン/オフを処理するために ESP8266 にフラッシュするスケッチを作成します。

ありがとう、そして楽しんでください！
