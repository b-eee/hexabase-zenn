---
title: "GitHub Star 27万超の『Open Claw』が示す、AIエージェントのセキュリティリスク"
emoji: "🔐"
type: "tech"
topics: ["ai", "security", "llm", "aiagent", "openclaw"]
published: true
---

## GitHub Star 27万超の『Open Claw』が示す、AIエージェントのセキュリティリスク—76%が懸念する脅威と、今すぐできる5つの対策
![](https://api.hexabase.io/api/v0/public/objects/69e0b3494f70eb866be51278)

2026年3月現在、AIエージェントツール『Open Claw（オープンクロー）』がGitHub Star 27万を超え、その成長速度はReactを上回るペースで注目を集めています。開発者のPeter Steinburger氏が2026年2月にOpenAIに移籍したことも大きな話題となりました。

しかし、この爆発的成長の裏で、セキュリティリスクが深刻化しています。Open Clawのスキルマーケットプレイス『Claw Hub』をスキャンしたところ、4,000ファイル中283個（約7%）にAPIキー漏洩等の脆弱性が発見されました。セキュリティ専門家の76%が「AIエージェントのセキュリティリスク」を懸念しており、73%が「検知が困難」と回答しています（2025年調査）。

AIエージェントは、LLMに「計画→実行→反復」の自律性を与えることで強力な生産性向上を実現しますが、その自律性こそが従来のセキュリティ対策では防げない脅威を生み出しています。本記事では、Open Clawが直面したセキュリティリスクを出発点に、AIエージェント全般の脅威と、今すぐ実装すべき5つの対策を解説します。

📌 この記事でわかること

- Open ClawのClaw Hubで発覚した脆弱性の実態（7%に問題）- AIエージェント特有の80種類の攻撃手法とは- 技術リードが今すぐ実装すべき5つのセキュリティ対策- セキュアなAI Co-work環境の構築方法💡 AIエージェント開発で「セキュアな環境をすぐに構築したい」とお考えの方は、エンタープライズグレードのセキュリティを標準搭載した[**Captain.AI**](https://captain-ai.hexabase.com/)もご検討ください。

### 1. Open Clawとは—GitHub Star 27万超のAIエージェントツール
![](https://api.hexabase.io/api/v0/public/objects/69e0b3444f70eb866be51276)

『Open Claw（オープンクロー）』は、2025年にリリースされたオープンソースのAIエージェントツールです。開発者のPeter Steinburger氏（2026年2月にOpenAIに移籍）により、当初「Claudebot」としてスタートし、その後「Maltbot」を経て、現在の「Open Claw」に改名されました。

Open Clawの主な特徴:

- ハートビート機能: バックグラウンドで継続的にタスクを実行- スキルズ対応: 外部ツールとの連携（GitHub, Slack, Notion等）- ローカルLLM対応: Mac miniで動作（プライバシー重視）- メッセージアプリ統合: iMessage等から直接操作- Claw Hub: スキルマーケットプレイス（開発者が機能拡張を共有）GitHub Starは27万を超え、Reactを上回るペースで成長しています。この爆発的人気の背景には、「誰でも簡単にAIエージェントを構築できる」という低い参入障壁があります。

しかし、この「手軽さ」がセキュリティリスクを拡大させています。Claw Hubで公開されているスキルのうち、約7%に脆弱性が発見されました。

### 2. Claw Hubで発覚した脆弱性—7%のスキルに問題
![](https://api.hexabase.io/api/v0/public/objects/69e0b3424f70eb866be5126c)

2026年2月、セキュリティ企業がClaw Hubで公開されている約4,000個のスキルをスキャンした結果、以下の脆弱性が発見されました：

発見された主な脆弱性:

- APIキーのハードコード: スクリプト内にOpenAI APIキー等が平文で記載（283個中最多）- 未検証の外部入力: ユーザー入力をサニタイズせずにシェルコマンドに渡す- 過剰な権限設定: スキルが不要なファイル読み取り権限を持つ- 依存関係の脆弱性: 古いライブラリを使用（既知の脆弱性あり）Peter Steinburger氏は、動画内で以下のようにコメントしています：

「今はセキュリティリスクが注目されているが、1年後には『ハッキングされた時の責任は誰が取るのか』という法的議論が当たり前になるだろう。リモートコード実行脆弱性があった場合、開発者がどこまで責任を負うのか、まだ誰も答えを持っていない。」

この発言は、AIエージェントのセキュリティが「技術課題」から「法的課題」へ移行しつつあることを示唆しています。

### 3. AIエージェントが直面する「産業規模」のセキュリティリスク
![](https://api.hexabase.io/api/v0/public/objects/69e0b34d4f70eb866be5127a)

Open Clawの事例は氷山の一角です。AIエージェント全般で、セキュリティリスクが「産業規模」に拡大しています。

統計データが示すリスクの深刻さ:

- 企業のセキュリティ担当者の76%が「AIエージェントのセキュリティリスク」を懸念（2025年調査）- 73%が「検知が困難」と回答- IPA（情報処理推進機構）の「情報セキュリティ10大脅威2026」で「AIの利用をめぐるサイバーリスク」が初選出なぜAIエージェントのセキュリティリスクは「産業規模」なのでしょうか？理由は以下の3点です：

### Captain.AI
- エージェントが実行できるツールを「承認制」にする- 機密データへのアクセスは「人間の承認」が必要- デプロイ前に、セキュリティレビューを義務化
#### 2. 可観測性: 何が起きているか見える化
- 全てのエージェント動作をダッシュボードで可視化- 異常検知時に自動でエージェントを停止- プロンプトインジェクションの試行をリアルタイム通知
#### 3. 教育: 開発者がリスクを理解する
- OWASP LLM Top 10を社内勉強会で共有- Open Clawのような事例を「失敗から学ぶ」教材として活用- プロンプトインジェクションの実演（Capture The Flag形式）💡 AI Co-work環境を「統合プラットフォーム」として構築したい場合、[Kubo](https://kubo.captainai.app/)は「業務プロセス全体をAIエージェントで自動化」しながら、セキュリティとガバナンスを両立する設計思想を採用しています。

### まとめ
本記事では、GitHub Star 27万超の『Open Claw』で発覚したセキュリティリスクを出発点に、AIエージェント全般の脅威と対策を解説しました。

要点まとめ:

- Open ClawのClaw Hubで7%のスキルに脆弱性が発見された- AIエージェントには80種類以上の攻撃手法が体系化されている- 企業の76%が「データ露出」、73%が「検知困難性」を懸念- 今すぐ実装すべき5つの対策: 入力検証、最小権限、出力フィルタリング、監査ログ、サンドボックス- セキュアなAI Co-work環境の構築にはガバナンス + 可観測性 + 教育が必要AIエージェントは、2026年以降の開発チームにとって「必須のツール」になりつつあります。しかし、セキュリティリスクを無視すれば、企業の信頼を失う可能性があります。Open Clawの事例から学び、今すぐ対策を始めることが、未来のAI Co-work環境を安全に構築する第一歩です。

📢 セキュアなAIエージェント開発を今すぐ始めるなら

- [**Captain.AI**](https://captain-ai.hexabase.com/): エンタープライズグレードのセキュリティを標準搭載したAIエージェントプラットフォーム- [Kubo](https://kubo.captainai.app/): 業務プロセス全体をAIで自動化しながら、ガバナンスを両立する統合環境※ 本記事の情報は2026年3月時点のものです。セキュリティ対策は継続的に更新することを推奨します。

役に立ったら、記事をシェアしてください[コラム一覧](/column)

- カテゴリー[開発事例](/column_cat/開発事例)(5)- [システム開発](/column_cat/システム開発)(55)- [知ったかテックワード](/column_cat/知ったかテックワード)(42)- [ユースケース](/column_cat/ユースケース)(8)- [ソリューション](/column_cat/ソリューション)(12)- [新規事業開発](/column_cat/新規事業開発)(29)- [レポート](/column_cat/レポート)(10)- [製品](/column_cat/製品)(1)- [フロントエンド実績](/column_cat/フロントエンド実績)(2)- [ビジネス](/column_cat/ビジネス)(24)- [サービス](/column_cat/サービス)(28)- [導入事例](/column_cat/導入事例)(5)- [テクノロジー](/column_cat/テクノロジー)(76)- [API連携](/column_cat/API連携)(2)- [事例](/column_cat/事例)(22)- タグ[システム運用 (16)](/column_tag/システム運用)- [TypeScript (1)](/column_tag/TypeScript)- [WebAssembly (2)](/column_tag/WebAssembly)- [ウォーターフォール開発 (2)](/column_tag/ウォーターフォール開発)- [業務システム (28)](/column_tag/業務システム)- [CSS (2)](/column_tag/CSS)- [GraphQL (1)](/column_tag/GraphQL)- [プログラミング (31)](/column_tag/プログラミング)- [スタートアップ (11)](/column_tag/スタートアップ)- [Nexaweb (1)](/column_tag/Nexaweb)- [BaaS (10)](/column_tag/BaaS)- [データベース (5)](/column_tag/データベース)- [SPA (2)](/column_tag/SPA)- [基本用語 (26)](/column_tag/基本用語)- [Case study (5)](/column_tag/Case study)- [Keyword (10)](/column_tag/Keyword)- [FaaS (1)](/column_tag/FaaS)- [システム開発 (69)](/column_tag/システム開発)- [スクラム (1)](/column_tag/スクラム)- [フロントエンド (38)](/column_tag/フロントエンド)- [AI (26)](/column_tag/AI)- [アジャイル開発 (18)](/column_tag/アジャイル開発)- [Supabase (1)](/column_tag/Supabase)- [イノベーション (5)](/column_tag/イノベーション)- [Database (2)](/column_tag/Database)- [月額制 (1)](/column_tag/月額制)- [PaaS (3)](/column_tag/PaaS)- [ACF (1)](/column_tag/ACF)- [BookReview (3)](/column_tag/BookReview)- [サービス開発 (5)](/column_tag/サービス開発)- [React (3)](/column_tag/React)- [Firebase (1)](/column_tag/Firebase)- [クラウドサービス (12)](/column_tag/クラウドサービス)- [low-code (2)](/column_tag/low-code)- [バックエンド (8)](/column_tag/バックエンド)- [ナレッジマネジメント (1)](/column_tag/ナレッジマネジメント)- [ChatGPT (1)](/column_tag/ChatGPT)- [Vue.js (2)](/column_tag/Vue.js)- [Tailwind CSS (1)](/column_tag/Tailwind CSS)- [DBaas (2)](/column_tag/DBaas)- [プロジェクト管理 (13)](/column_tag/プロジェクト管理)- [セミナー (2)](/column_tag/セミナー)- [Web (21)](/column_tag/Web)- [失敗事例 (2)](/column_tag/失敗事例)- [Hexabase_health (1)](/column_tag/Hexabase_health)- [生成AI (7)](/column_tag/生成AI)- [受託開発 (1)](/column_tag/受託開発)- [Kubernetes (3)](/column_tag/Kubernetes)- [WebComponents (1)](/column_tag/WebComponents)- [通知 (1)](/column_tag/通知)- [API (6)](/column_tag/API)- [Next.js (1)](/column_tag/Next.js)- [フレームワーク (3)](/column_tag/フレームワーク)- [ローコード開発 (4)](/column_tag/ローコード開発)- [ノーコード開発 (1)](/column_tag/ノーコード開発)- [JavaScript (2)](/column_tag/JavaScript)- [Hexabase (12)](/column_tag/Hexabase)- [LLM (3)](/column_tag/LLM)- [画像生成 (1)](/column_tag/画像生成)- [DX (34)](/column_tag/DX)[Contact Usお問い合わせはこちら](/contact-us)[![Hexabase](/2022/03/logo2022-2.svg)](/)- [![](/_next/image?url=%2F2022%2F03%2Ficon-sns-fb22.svg&w=48&q=75)](https://www.facebook.com/hexabaseinc)- [![](/_next/image?url=%2F2022%2F03%2Ficon-sns-tw22.svg&w=48&q=75)](https://twitter.com/hexabase_jp)- [![](/_next/image?url=%2F2022%2F03%2Ficon-sns-gh22.svg&w=48&q=75)](https://github.com/b-eee)- [![](/_next/image?url=%2F2022%2F05%2Ficon-sns-dc22.svg&w=48&q=75)](https://discord.gg/nQ6pGkTG2R)- [![](/_next/image?url=%2F2022%2F11%2Ficon-sns-li-wh-3.svg&w=48&q=75)](https://www.linkedin.com/company/hexabase-inc/)
### 製品
- [Captain.AI](/product/captain-ai/)- [Hexavoice](/product/hexavoice/)- [Kubo](/product/kubo/)- [Kubo On-Premise](/product/kubo/on-premise)- [Compass](/product/compass/)- [BaaS (Backend as a Service)](/product/)
### サービス
- [AI駆動開発セミナー](/service/ai-dev)- [AIハンズオンセミナー](https://seminarlp.hexabase.com/)- [安心Techサポート](/service/ai-feature)- [サービスのご紹介](/service/)- [新規事業開発](/service/newbusiness/)
### リソース
- [Captain.AI マニュアル](https://captain-manual.kubo.hexabase.io/)- [開発者向けドキュメント](/documents-top/)- [開発ガイド](https://devdoc.hexabase.com/)- [APIガイド](https://apidoc.hexabase.com/)- [導入事例](/casestudy/)- [コラム](/column/)- [パートナー](/partner/)- [無料テンプレート](/templates/)
### 企業
- [企業情報](/our-company/)- [採用情報](/careers/)- [ニュース一覧](/news/)- [セキュリティへの取り組み](/security/)- [CTOインタビュー](/cto-interview/)- [お問合せ](/contact-us/)© Hexabase

- [利用規約](/terms-of-use/)- [特定商取引法に基づく表記](/legal-notice/)- [プライバシーポリシー](/privacy-policy/)- [情報セキュリティ基本方針](/security-policy/)![](/_next/image?url=%2F2022%2F11%2FSGS_ISO-IEC_27001_with_ISMS-AC_TCL_HR.jpg&w=256&q=75)![](/_next/image?url=%2F2022%2F11%2FSGS_ISO27017_ISMS-AC_TCL_HR.jpg&w=256&q=75)日本語

[English](https://en.hexabase.com/)

---

この記事は [株式会社Hexabase](https://www.hexabase.com/) のテックブログから転載しています。

**関連リンク:**
- [Kubo - マネージド K3s サービス](https://kubo.hexabase.io/)
- [Captain.AI - AIエージェント実行基盤](https://www.hexabase.com/product/captain-ai/)
- [お問い合わせ](https://www.hexabase.com/contact-us/)
