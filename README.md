📌 Selenium Automation フレームワーク

Java を使った Selenium 自動テスト フレームワーク
このリポジトリは Selenium を用いて Web UI 自動テストを実装するためのベースフレームワークです。

📚 目次（Contents）

🔍 プロジェクト概要

🚀 セットアップ方法

🧪 テスト実行方法

📁 フォルダ構成

🛠 技術スタック

🖼 アーキテクチャ図

📄 ライセンス

🔍 プロジェクト概要

このプロジェクトは以下を目的としています：

Java + Selenium WebDriver を使ったテスト自動化

Page Object Model をベースにした保守性の高い構造

GitHub Actions（CI）での自動テスト実行にも対応可能

拡張しやすいテストフレームワークのテンプレート

🚀 セットアップ方法
必要条件

JDK 11 以上

Maven

Chrome / GeckoDriver

インストール
git clone https://github.com/beniguha/SeleniumAutomation.git
cd SeleniumAutomation
mvn clean install
🧪 テスト実行
ローカル実行
mvn test
指定テストのみ実行
mvn test -Dtest=LoginTest
📁 ディレクトリ構成
SeleniumAutomation/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── framework/
│   │   │       ├── driver/           # WebDriver 設定
│   │   │       ├── pages/            # Page Classes
│   │   │       └── utils/            # ユーティリティ
│   └── test/
│       └── java/
│           └── tests/                # テストクラス
├── pom.xml                            # Maven 設定
└── README.md                          # このファイル
🛠 技術スタック
技術	役割
Java	プログラミング言語
Selenium WebDriver	ブラウザ自動化
Maven	ビルド・依存管理
TestNG / JUnit	テストランナー
GitHub Actions (任意)	CI/CD 実行
🖼 アーキテクチャ図

以下は基本的なフレームワーク構造の概念図です：

┌───────────────────────────────────────┐
│              テストケース             │
│ (tests/*.java — 例: LoginTest.java)   │
└───────────────────────────────────────┘
                     ↓
┌───────────────────────────────────────┐
│             ページオブジェクト         │
│  (pages/*.java — 例: LoginPage.java)    │
└───────────────────────────────────────┘
                     ↓
┌───────────────────────────────────────┐
│       WebDriver & 共通ユーティリティ   │
│ (driver/ + utils/ + config)            │
└───────────────────────────────────────┘
                     ↓
┌───────────────────────────────────────┐
│               ブラウザ起動             │
│         (Chrome, Firefox など)         │
└───────────────────────────────────────┘
