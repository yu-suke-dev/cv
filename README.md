# 基本情報

|key|value|
|----|----|
|名前|藤井 祐輔|
|生息地|東京都 渋谷区|
|Twitter|[@yu_suke_dev](https://twitter.com/yu_suke_dev)|
|Qiita|[@yusuke_dev](https://qiita.com/yusuke_dev)|
|ポートフォリオ|[yu-suke.dev](https://yu-suke.dev)|

# 概要

- 現在、自社開発の企業で正社員としてSREとして働きつつ、業務委託でもいろいろなお仕事をさせてもらっています。
- AWS/GCPのどちらの業務経験も持っています。
- フェーズを問わず、長期的な技術課題に対して広い視点でアプローチを打っていくことをやっているエンジニアです。
- お仕事に関するお問い合わせはTwitterのDM等からお気軽にどうぞ。

# スキル
- 基本的にすべて実業務で使用した技術だけを列挙しています。

## 言語
TypeScript | Java

## フレームワーク等
Express | Spring Framework

## RDB/NoSQL
MySQL / Firestore

## クラウド
### AWS
VPC | S3 | Cloud Front | Lambda | ELB | EC2 | ECS | Route53 | IAM | RDS(MySQL) | Aurora | ElastiCache(Redis) | Kinesis | Athena | QuickSight | SQS | Cloud Watch | KMS

### GCP
VPC | Cloud Functions | GCS | GCE | IAM | Cloud Pub/Sub | Cloud Container Repository | Stackdriver Logging | Cloud Load Balancing | Serverless VPC Access Connector | Cloud Run

## SaaS/PaaS
GitHub | GitHub Actions | BitBucket | CircleCI | Sentry | NewRelic

## その他
Terraform | Docker | Apache | Tomcat | Zabbix | Algolia | LDAP

# 主な業務経歴

## 介護経営支援のSaaSにおけるSREとしての業務(2020)

### 技術要素
AWS, Terraform, MySQL, Firebase

### 担当業務
- Terraformによるインフラ(開発環境)のコード化(VPC, EC2, Aurora, IAM等)
  - 開発環境のTerraform環境にてコード化できていない部分のコード化をした。
- SLIの可視化(Kinesis/Athena/QuickSight/Lambda)
  - 同一ドメインでパスベースでアプリが分かれているが、全アプリでのSLIしか集計されていなかったため、アプリごとにSLIを集計するように実装した。
  - 可視化がされていなかったため、QuickSight SDKを利用し、社内公開した。
- GitHubを利用した、開発環境に必要な公開鍵の自動管理
  - GitHubに公開鍵をpushしS3に保存して、それをEC2のuserdataで取得することによって公開鍵をGitHubで管理するようにした。
- S3を利用したデプロイフローの改善
  - これまではCircleCIからアーティファクトをダウンロードしており、デプロイの作業が煩雑になっていたため、S3にpushするようにした。
- DB負荷改善
  - SlowqueryやNew RelicからDBの負荷を高めているクエリを見つけ、インデックスの追加等クエリ改善を行った。
  - Auroraのマスター(Writer)にSelectクエリがSlowqueryとして多く存在していたため、スレーブ(Reader)に流すように改善した。
- 各種権限の管理方針の決定、管理
  - AWS IAM, Firebase(GCP) IAM, 各種SaaSの権限の管理。

### 発揮したバリュー
- AWSを業務で使用するのが初めてだったため、Terraformのコードを読みながらAWSについて素早くキャッチアップをした。

<hr>

## デザインアセットのバージョン管理アプリのMVP開発(2020)

### 技術要素
GCP, TypeScript, Express, Docker

### 担当業務
- アップロードされたファイル処理をするアプリの設計と実装
- インフラの設計、構築。
- GitHub Actionsを利用したCI/CDの導入。

### 発揮したバリュー
- これまでの案件で培ったAWSやFirebaseの知見を活かし、GCPの知識を短期間でキャッチアップした。
- Cloud Functions,Cloud Pub/Sub, Cloud Runを利用したサーバレスアーキテクチャで構成したが、Cloud Runの用意するサーバのメモリでは足りなかったが、GCEを使った構成に作り直すなどの対応力を発揮した。

<hr>

## スケジュール管理アプリのバックエンド及び管理画面のバックエンドの開発(2019)

### 技術要素
- TypeScript, Node.js, Firebase

### 担当業務
- 100種類のクローリングをするアプリケーションの設計から実装と定期実行のインフラ設計
- Firebase Projectを複数利用した管理画面のアプリケーションの設計から実装。
- GitHub Actionsを利用したCI/CDの導入。
- Linter(eslint, prettier)の導入。
- Firestore、全文検索サービスの導入

### 発揮したバリュー
- Firestoreを使用したプロジェクトは初めてだったが、すばやくキャッチアップをし、機能要件や設計の段階からジョインし貢献した。
- Firebaseのプロジェクトを複数使用した安全な管理画面のバックエンドを構築した。
- TypeScriptは初めてだったが、キャッチアップをし、バッチアプリケーションの設計と共通部分の実装および定期実行のためのインフラ設計を行った。

<hr>

## 税理士法人向け顧客管理システムの開発(2019)

### 技術要素
Java, Spring Framework, MySQL, MyBatis

### プロジェクト概要
- 税理士法人の会社の社内システムにて、APIやバッチアプリの保守、追加機能開発。

### 担当業務
- 言語はJava、フレームワークとライブラリはSpring Frameworkを使用し、主に定期的に実行されるバッチアプリやAPIの開発の一部をコーディング、結合テストまで担当。

### 発揮したバリュー
- エンジニアになって最初の開発案件ながら、増税対応に伴う税率計算部分を実装するとともに、それまで導入されていなかったユニットテストを導入。テストは書いたことがなかったため、素早くキャッチアップして対応した。API開発では、数千件の住所の重複判定をするAPIの実装などを行い、メンバーとしての自走能力を発揮した。
