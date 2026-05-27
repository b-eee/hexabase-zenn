---
title: "CNCF Graduated プロジェクト一覧 2025: 本番環境で信頼できる OSS"
emoji: "📝"
type: "tech"
topics: ["kubernetes", "cncf", "k3s", "cloudnative", "oss"]
published: false
---

クラウドネイティブ技術を導入する際、「どのオープンソースプロジェクトが本番環境で信頼できるのか」は最も重要な判断基準の一つです。[CNCF（Cloud Native Computing Foundation）](https://www.cncf.io/) の **Graduated** ステータスは、そのプロジェクトが成熟し、広範な本番環境での採用実績があることを証明する最高レベルの認定です。[Kubo](https://kubo.hexabase.io/) は K3s ベースの Kubernetes プラットフォームとして、これら CNCF Graduated プロジェクトとの高い親和性を持っています。本記事では、2025 年時点の全 Graduated プロジェクトをカテゴリ別に解説します。

<!-- 画像: CNCF プロジェクトの成熟度レベル図（Sandbox → Incubating → Graduated の段階と各段階の要件） -->

## CNCF Graduated とは：信頼性の証

[CNCF](https://www.cncf.io/projects/) の Graduated ステータスを取得するには、プロジェクトが以下の厳格な基準を満たす必要があります：

- **広範な本番採用**: 複数の企業・組織での本番環境での使用実績
- **健全なコミュニティ**: 多様なコントリビュータと活発な開発活動
- **セキュリティ監査**: 第三者によるセキュリティ監査の完了
- **ガバナンス**: 明確なプロジェクトガバナンスと意思決定プロセス
- **成熟したドキュメント**: 包括的なドキュメントとユーザーガイド

[CNCF Annual Report 2025](https://www.cncf.io/reports/cncf-annual-report-2025/) によると、CNCF は 230 以上のプロジェクトをホストし、30 万人以上のコントリビュータを擁しています。Graduated プロジェクトはその頂点に位置するエリートです。

[Captain.AI](https://www.hexabase.com/product/captain-ai/) は、これらの CNCF Graduated プロジェクトを活用した Kubernetes 環境の構築と運用を AI で支援します。

<!-- 画像: CNCF Landscape の Graduated プロジェクト一覧を示すマップ -->

## オーケストレーションとランタイム

### Kubernetes -- コンテナオーケストレーションの標準

[Kubernetes](https://kubernetes.io/) は CNCF の最初の Graduated プロジェクトであり、コンテナオーケストレーションのデファクトスタンダードです。コンテナ化されたアプリケーションのデプロイ、スケーリング、管理を自動化します。

### containerd / CRI-O -- コンテナランタイム

[containerd](https://containerd.io/) と [CRI-O](https://cri-o.io/) は、Kubernetes 向けの軽量コンテナランタイムです。Docker デーモンに依存しない CRI（Container Runtime Interface）準拠のランタイムとして、本番環境で広く採用されています。

### Crossplane -- インフラストラクチャのオーケストレーション

[Crossplane](https://www.crossplane.io/) は 2025 年に Graduated を達成したプロジェクトで、Kubernetes API を使ってクラウドインフラストラクチャを宣言的に管理します。AWS、GCP、Azure のリソースを Kubernetes マニフェストとして統一的に管理できます。

### Knative -- サーバーレス

[Knative](https://knative.dev/) は 2025 年 10 月に Graduated を達成した、Kubernetes 上のサーバーレスプラットフォームです。[CNCF の発表](https://www.cncf.io/announcements/2025/10/08/cloud-native-computing-foundation-announces-knatives-graduation/)によると、イベント駆動のアプリケーション層を提供し、オートスケーリングとゼロスケールをネイティブにサポートします。

### KEDA -- イベント駆動オートスケーリング

[KEDA](https://keda.sh/) は、Kafka、RabbitMQ、Azure Queue などの外部イベントソースに基づいて Kubernetes ワークロードをスケールするイベント駆動オートスケーラーです。

### KubeEdge -- エッジコンピューティング

[KubeEdge](https://kubeedge.io/) は、Kubernetes をエッジデバイスまで拡張するプロジェクトです。クラウドとエッジの統合管理を実現します。

[Kubo](https://kubo.hexabase.io/) はこれらのオーケストレーション技術の恩恵を受け、K3s ベースの軽量な Kubernetes プラットフォームとしてエッジからクラウドまで対応しています。

<!-- 画像: オーケストレーション＆ランタイムカテゴリの CNCF プロジェクト関係図 -->

## オブザーバビリティ

### Prometheus -- メトリクス収集の標準

[Prometheus](https://prometheus.io/) は、プルベースのメトリクス収集と PromQL クエリ言語で、Kubernetes 環境のモニタリングを支える基盤です。詳細は本ブログの [Prometheus 監視ガイド](https://kubo.hexabase.io/) をご覧ください。

### OpenTelemetry -- 統合オブザーバビリティ

[OpenTelemetry](https://opentelemetry.io/) は、トレース、メトリクス、ログを統合的に扱うベンダーニュートラルなフレームワークです。90 以上のオブザーバビリティベンダーがサポートしており、業界標準としての地位を確立しています。

### Jaeger -- 分散トレーシング

[Jaeger](https://www.jaegertracing.io/) は、マイクロサービス環境における分散トレーシングバックエンドです。リクエストの全体像を可視化し、パフォーマンスボトルネックの特定を支援します。

### Fluentd -- ログ収集

[Fluentd](https://www.fluentd.org/) は、統一ログ収集レイヤーを提供するオープンソースのデータコレクターです。500 以上のプラグインで多様なデータソースと出力先に対応しています。

[Captain.AI](https://www.hexabase.com/product/captain-ai/) は、これらのオブザーバビリティツールから得られるデータを AI で統合分析し、インシデントの早期検知と対応を自動化します。

## ネットワーキングとサービスメッシュ

### Cilium -- eBPF ベースネットワーキング

[Cilium](https://cilium.io/) は、eBPF 技術を活用して L3-L7 のネットワーキング、セキュリティ、オブザーバビリティを提供する CNCF Graduated プロジェクトです。iptables を超えるパフォーマンスと、アイデンティティベースのセキュリティモデルが特徴です。

### Envoy -- サービスプロキシ

[Envoy](https://www.envoyproxy.io/) は、Lyft が開発した高性能なサービスプロキシです。Istio や多くのサービスメッシュの基盤として使用されており、L7 トラフィック管理、ロードバランシング、可視性を提供します。

### CoreDNS -- サービスディスカバリ

[CoreDNS](https://coredns.io/) は、Kubernetes のデフォルト DNS サーバーです。プラグインベースのアーキテクチャにより、DNS ベースのサービスディスカバリを柔軟にカスタマイズできます。

### Istio -- サービスメッシュ

[Istio](https://istio.io/) は、マイクロサービス間の通信を管理するサービスメッシュです。トラフィック管理、セキュリティ（mTLS）、可観測性を透過的に提供します。

### Linkerd -- 軽量サービスメッシュ

[Linkerd](https://linkerd.io/) は、Kubernetes 向けの軽量・シンプルなサービスメッシュです。最小限の設定で mTLS、メトリクス、リトライを実現します。

<!-- 画像: ネットワーキング＆サービスメッシュの CNCF プロジェクト構成図（Cilium、Envoy、CoreDNS、Istio、Linkerd の関係） -->

## セキュリティとコンプライアンス

### cert-manager -- TLS 証明書自動管理

[cert-manager](https://cert-manager.io/) は、Kubernetes 上の TLS 証明書の発行・更新を自動化します。Let's Encrypt、HashiCorp Vault 等、複数の認証局に対応しています。

### Falco -- ランタイムセキュリティ

[Falco](https://falco.org/) は、Linux カーネルのシステムコールを監視し、コンテナやホストレベルの異常な動作をリアルタイムで検出するクラウドネイティブランタイムセキュリティエンジンです。

### OPA（Open Policy Agent） -- ポリシーエンジン

[Open Policy Agent](https://www.openpolicyagent.org/) は、クラウドネイティブ環境における汎用ポリシーエンジンです。Kubernetes のアドミッションコントロール、API 認可、データフィルタリングなどに使用されます。

### Kyverno -- Kubernetes ネイティブポリシー

[Kyverno](https://kyverno.io/) は、Kubernetes ネイティブのポリシーエンジンです。YAML でポリシーを記述でき、Rego 言語を必要としない直感的な使い勝手が特徴です。

### SPIFFE / SPIRE -- ワークロードアイデンティティ

[SPIFFE](https://spiffe.io/) はワークロードのアイデンティティ標準、[SPIRE](https://spiffe.io/spire/) はその実装です。サービス間の認証を自動化し、ゼロトラストセキュリティの基盤を提供します。

### in-toto / TUF -- ソフトウェアサプライチェーン

[in-toto](https://in-toto.io/) と [TUF（The Update Framework）](https://theupdateframework.io/) は、ソフトウェアサプライチェーンの完全性を保証するフレームワークです。ビルドからデプロイまでの各段階を暗号的に検証します。

## ストレージ、レジストリ、CI/CD

### Rook / CubeFS -- クラウドネイティブストレージ

[Rook](https://rook.io/) は Kubernetes 上で Ceph を自動管理するストレージオーケストレーター、[CubeFS](https://cubefs.io/) は大規模分散ファイルシステムです。

### Harbor / Dragonfly -- コンテナレジストリ

[Harbor](https://goharbor.io/) はエンタープライズ向けコンテナレジストリ、[Dragonfly](https://d7y.io/) は P2P ベースのコンテナイメージ配信システムです。

### Argo -- CI/CD と GitOps

[Argo](https://argoproj.github.io/) は、Kubernetes ネイティブの CI/CD ツールセットです。Argo CD（GitOps）、Argo Workflows（ワークフロー）、Argo Rollouts（プログレッシブデリバリー）を含みます。

### Flux -- GitOps

[Flux](https://fluxcd.io/) は、Git リポジトリの状態をクラスタに自動同期する GitOps ツールです。Argo CD と並ぶ GitOps の二大プロジェクトの一つです。

### Helm -- パッケージマネージャ

[Helm](https://helm.sh/) は、Kubernetes アプリケーションのパッケージマネージャです。Chart と呼ばれるテンプレートで、複雑なアプリケーションの配布とデプロイを簡素化します。

### その他

- [Dapr](https://dapr.io/) -- 分散アプリケーションランタイム
- [CloudEvents](https://cloudevents.io/) -- イベントデータの標準仕様
- [etcd](https://etcd.io/) -- 分散キーバリューストア（Kubernetes の基盤）
- [TiKV](https://tikv.org/) -- 分散トランザクショナル KV ストア
- [Vitess](https://vitess.io/) -- MySQL のスケーリングソリューション

<!-- 画像: 全 CNCF Graduated プロジェクトのカテゴリ別マップ -->

## Kubo と CNCF エコシステム

[Kubo](https://kubo.hexabase.io/) は K3s ベースの軽量 Kubernetes プラットフォームとして、CNCF Graduated プロジェクトとの高い親和性を持っています：

| カテゴリ | Kubo での活用例 |
|---|---|
| **オーケストレーション** | K3s (Kubernetes 準拠) がベース |
| **モニタリング** | Prometheus + Grafana による標準監視 |
| **ネットワーキング** | Cilium / CoreDNS による高性能ネットワーク |
| **セキュリティ** | cert-manager による TLS 自動管理 |
| **CI/CD** | Argo CD / Flux による GitOps デプロイ |
| **ストレージ** | Rook/Ceph による永続ストレージ |
| **レジストリ** | Harbor によるプライベートレジストリ |

[CNCF のプロジェクト速度レポート](https://www.cncf.io/blog/2026/02/09/what-cncf-project-velocity-in-2025-reveals-about-cloud-natives-future/)が示すように、クラウドネイティブエコシステムは加速度的に成長しています。Kubo はこのエコシステムの恩恵を最大限に活用できるプラットフォームです。

[Captain.AI](https://www.hexabase.com/product/captain-ai/) と Kubo を組み合わせることで、CNCF Graduated プロジェクトを活用した本番環境の構築・運用を AI が支援するインテリジェントなプラットフォームが実現します。

## まとめ

2025 年時点で CNCF Graduated プロジェクトは 36 件を数え、クラウドネイティブ技術のあらゆる領域をカバーしています：

1. **Graduated ステータス**は広範な本番採用、セキュリティ監査、成熟したガバナンスの証
2. **Kubernetes を中心に**、オーケストレーション、オブザーバビリティ、ネットワーキング、セキュリティの全領域をカバー
3. **2025 年の新規 Graduated** として Crossplane、Knative が加わり、IaC とサーバーレスが強化
4. **Cilium、OpenTelemetry** など eBPF やオブザーバビリティの革新的プロジェクトが成熟
5. **エコシステム全体**が有機的に連携し、包括的なクラウドネイティブ基盤を形成

[Kubo](https://kubo.hexabase.io/) は K3s ベースでこれらの CNCF Graduated プロジェクトとシームレスに連携し、エンタープライズグレードのクラウドネイティブ環境を提供します。CNCF エコシステムの活用にご興味がある方は、ぜひ [Kubo](https://kubo.hexabase.io/) をご検討ください。

AI によるクラウドネイティブ運用の自動化については、[Captain.AI](https://www.hexabase.com/product/captain-ai/) をご確認ください。導入のご相談は[お問い合わせ](https://www.hexabase.com/contact-us/)からお気軽にどうぞ。

---

この記事は [株式会社Hexabase](https://www.hexabase.com/) のテックブログから転載しています。

**関連リンク:**
- [Kubo - マネージド K3s サービス](https://kubo.hexabase.io/)
- [Captain.AI - AIエージェント実行基盤](https://www.hexabase.com/product/captain-ai/)
- [お問い合わせ](https://www.hexabase.com/contact-us/)
