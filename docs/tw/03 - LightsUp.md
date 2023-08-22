# LightsUp!

# 開始的先決條件

1. 安裝顫動 - [https://docs.flutter.dev/get-started/install](https://docs.flutter.dev/get-started/install)
2. 設置您的 IDE - [https://docs.flutter.dev/get-started/editor?tab=vscode](https://docs.flutter.dev/get-started/editor?tab=vscode)
3. 試駕 - [https://docs.flutter.dev/get-started/test-drive?tab=vscode](https://docs.flutter.dev/get-started/test-drive?tab=vscode)
4. 寫你的第一個應用程序 - [https://codelabs.developers.google.com/codelabs/flutter-codelab-first#0](https://codelabs.developers.google.com/codelabs/flutter-codelab-first#0)

# 前進的資源

1. Dart 編程語言 - [https://dart.dev/language](https://dart.dev/language)
2. Dart 備忘單代碼實驗室 - [https://dart.dev/codelabs/dart-cheatsheet](https://dart.dev/codelabs/dart-cheatsheet)
3. Riverpod - [https://codewithandrea.com/articles/flutter-state-management-riverpod/](https://codewithandrea.com/articles/flutter-state-management-riverpod/)

# 目標

我們將創建一個在 Android 和 iOS 中運行的移動應用程序，以演示我們在前面的章節中學到的各種 MQTT 概念，並進一步擴展其他 MQTT 功能。

該應用程序展示了以下功能：

- 動態創建經過身份驗證的 MQTT 客戶端連接以增強安全性
- 能夠通過打開/關閉來控制 ESP8266 NodeMCU 的內置 LED 燈
- 一個客戶端控制燈，另一個客戶端可以實時監控燈是否亮
- 實時處理移動應用程序和 ESP8266 LED 中顯示的 MQTT 消息

# 我從哪裡開始？

GitHub 存儲庫被設置為一個簡單的起點，其中包含構建前端所需的所有代碼。由於我們的重點是 MQTT 通信，因此我們將在本章中一起討論它。

克隆此 git 存儲庫並簽出或下載 `start/lights-up` 分支。

[https://github.com/ahdzlee/iPBL2023-PreTraining/tree/start/lights-up/mobile/lights_up](https://github.com/ahdzlee/iPBL2023-PreTraining/tree/start/lights-up/mobile/lights_up)

# 視頻課程

創建練習視頻課程是為了讓應用程序運行並實現目標。請按照建議的順序查看下面的鏈接。

1. [簡介和項目結構](https://youtu.be/FbndnKULc8E)
   - 顯示您需要了解的有關相關項目文件的信息以及如何在 Visual Studio Code 中運行項目。
1. [創建 MQTT 客戶端管理器](https://youtu.be/Xg-AAr1IL2E)
   - 實現處理客戶端連接、斷開連接、訂閱和發布 MQTT 消息的類。管理器還公開一個流來偵聽訂閱更新。
1. [創建 MQTT 客戶端連接](https://youtu.be/2Yv1fI4ulR8)
   - 演示如何使用 MQTT 客戶端管理器創建與代理的客戶端連接。
1. [使用 Riverpod 跟踪應用程序連接狀態變化](https://youtu.be/mP_LQKsqJj0)
   - 演示如何使用 Riverpod 管理應用程序狀態更改。展示應用程序連接生命週期更改以及如何根據狀態更改更新 UI。
1. [創建經過身份驗證的客戶端連接](https://youtu.be/eVuhqOFzBeU)
   - 演示如何通過接受代理的憑據來激活身份驗證。應用程序還處理未經授權的異常，並不允許它創建客戶端連接。
1. [發布燈開/關事件](https://youtu.be/3-4AGUBcNqU)
   - 將有效負載發送到代理並通過 MQTTX 進行測試
1. [訂閱 MQTT 主題](https://youtu.be/mUgx4FV6ovY)
   - 演示如何訂閱 MQTT 主題並持續偵聽收到的訂閱的 MQTT 消息。
1. [ESP8266 NodeMCU 中的發布-訂閱實現](https://youtu.be/pBd3tbD6LB8)
   - 創建一個草圖，讓 ESP8266 閃爍來處理內置 LED 的打開或關閉。

謝謝，祝你玩得開心！
