# 基本情報

| key | value |
| ---- | ---- |
| 名前 | 藤井 祐輔 |
| 生息地 | 東京都 渋谷区 |
| Twitter | [@yu_suke_dev](https://twitter.com/yu_suke_dev) |
| Qiita | [@yusuke_dev](https://qiita.com/yusuke_dev) |
| HP | [yu-suke.dev](https://yu-suke.dev) |

# 概要

- 現在、正社員・業務委託でいろいろなお仕事をしています。
- AWS/GCPのどちらの業務経験も持っています。
- 長期的な技術課題に対して広い視点でアプローチを打つことをやっているエンジニアです。
- お仕事に関するお問い合わせはTwitterのDM等からお気軽にどうぞ。

# 単価
- ¥3,000/h 〜

# スキル
- 基本的にすべて実業務で使用した技術だけを列挙しています。

## 言語
TypeScript | Java | ShellScript

## フレームワーク等
Express | Spring Framework

## RDB/NoSQL
MySQL / Firestore

## クラウド
### AWS
| Type | Service |
| --- | --- |
| Computing | EC2 / ELB / Lightsail / ECS / ECR / Batch / Lambda |
| Storage | S3 |
| Database | RDS(Aurora MySQL / RDS Proxy) / ElastiCache(Redis) / DynamoDB |
| Network | VPC / CloudFront / Route53 / API Gateway |
| Develop | CodeBuild / CodePipeline |
| Management | CloudWatch(Logs) / Systems Manager / Chatbot |
| Analytics | Athena / Kinesis(Streams / Firehose / Analytics) / QuickSight / Glue |
| Security | IAM / Secrets Manager / KMS |
| Integration | Step Functions / SQS |
| Cost | Cost Explorer |
| Other | Corretto |

### GCP

| Type | Service |
| --- | --- |
| Computing | Conpute Engine / Cloud Run / Container Registry / Cloud Functions |
| Storage | Cloud Storage |
| Database | Firestore |
| Network | VPC / Cloud Load Balancing |
| Develop | Cloud Scheduler |
| Management | Cloud Logging |
| Analytics | Cloud Pub/sub |
| Security | IAM |
| Other | Firebase(Hosting, Functions, Storage) |

## SaaS/PaaS
| GitHub | GitHub Actions | BitBucket | CircleCI | Sentry | NewRelic |

## その他
| Terraform | Docker | Apache | Tomcat | Zabbix | Algolia | LDAP |

# 主な業務経歴

## 介護領域の経営支援SaaSにおけるDevOps業務(2019/11~)

### 技術要素
AWS, Terraform, MySQL

### 担当業務
- TerraformによるDev環境のコード化。
  - 開発環境のTerraform環境にてコード化できていない部分をコード化した。
- SLIの可視化
  - サービス内でパスベースで分かれているJavaアプリごとにレスポンスのエラー率を集計できるようにした。
- GitHubを利用した、開発環境に必要な公開鍵の自動管理
  - GitHubに公開鍵を置き、GitHub Actions, S3, EC2のuserdataを利用することでGitHubのイベントドリブンで公開鍵を各ホストに配布する仕組みを構築した。
- S3を利用したデプロイフローの改善
  - アーティファクトの保存先をCircleCIからS3に変更し、運用を楽にした。
- 運用コストの削減
  - S3に静的ファイルをアップロードした後にCFのキャッシュをクリアする運用があったため自動化した。
- DB負荷の改善
  - SlowqueryやNew RelicからDBの負荷を高めているクエリを見つけ、indexの追加などのクエリ改善を行った。
- 各種権限の管理方針の決定、管理
  - AWS IAM, Firebase(GCP) IAM, 各種SaaSの権限の管理。

### 発揮したバリュー
- AWSを業務で使用するのが初めてだったため、Terraformのコードや各種ドキュメント等を読み、素早くキャッチアップをした。

<hr>

## スケジュール管理アプリのBatchアプリ及び管理画面の新規開発(2019/11~)

### 技術要素
- AWS Batch, ECR, Docker, TypeScript, Node.js, Firebase

### 担当業務
- 数百種類のサイトからクローリングをするアプリケーションの共通処理の設計・実装
- Batch実行のインフラ設計、構築、それに伴うBatchアプリの改修、Docker化。
- Firebase Projectを複数利用したアプリケーションの設計・実装。
- GitHub Actionsを利用したCI/CDの導入。
- Linter(ESLint, Prettier)の導入。
- Algoliaの導入

### 発揮したバリュー
- Firebaseを使用したプロジェクトは初めてだったが、すばやくキャッチアップをして機能要件や設計の段階からジョインし貢献した。
- Firebaseのプロジェクトを複数使用した安全な管理画面のバックエンドを構築した。
- TypeScriptは初めてだったが、キャッチアップをし、バッチアプリケーションの設計と共通部分の実装をした。

<hr>

## デザインアセットのバージョン管理アプリのMVP開発(2020)

### 技術要素
GCP, TypeScript, Express, Docker

### 担当業務
- アップロードされたファイル処理をするアプリの設計と実装
- インフラの設計、構築。
- GitHub Actionsを利用したCI/CDの導入。

### 発揮したバリュー
- これまでの案件で培ったAWSの知見を活かし、GCPの知識を短期間でキャッチアップした。
- Cloud Runを用いたサーバレスアーキテクチャで構成したもののアプリケーションの仕様上、メモリが足りずに実現できなかったが、Compute Engineを使った構成に変更する対応力を発揮した。

<hr>

## 税理士法人向け顧客管理システムの開発(2019)

### 技術要素
Java8, Spring Framework, MySQL, MyBatis

### プロジェクト概要
- 税理士法人の会社の社内システムにて、APIやバッチアプリの保守、追加機能開発。

### 担当業務
- Java、Spring Frameworkを用いて、定期的に実行されるバッチアプリやAPIの開発の一部をコーディング、結合テストまで担当。

### 発揮したバリュー
- エンジニアになって最初の開発案件ながら、増税対応に伴う税率計算部分を実装するとともに、それまで導入されていなかったユニットテストを導入。API開発では、数千件の住所の重複判定をするAPIの実装などを行い、メンバーとしての自走能力を発揮した。
