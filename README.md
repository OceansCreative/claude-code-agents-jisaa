# Claude Code Agents for Jisaa (士業)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Release](https://img.shields.io/github/v/release/OceansCreative/claude-code-agents-jisaa)](https://github.com/OceansCreative/claude-code-agents-jisaa/releases)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](./CONTRIBUTING.md)
[![Code of Conduct](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](./CODE_OF_CONDUCT.md)

> 行政書士・税理士・社労士・司法書士・弁理士など、士業の一人事務所向け Claude Code サブエージェント集。
> 業際遵守・期限管理・顧客コミュニケーションを AI で加速する。

[English version below](#english)

---

## 🎯 これは何か

[Claude Code](https://docs.claude.com/en/docs/claude-code/overview) で士業事務所の業務判断・書類作成・顧客対応を補助する 7 つの専門エージェント定義集です。

業際違反・倫理規程違反は懲戒事由に直結します。本パックは「グレーゾーンには踏み込まない」を基本方針とし、各エージェントに業界特有のリスクチェックを組み込んでいます。

```
あなた: @compliance-officer
        建設業の顧客から、新たに発生した工事代金未払いトラブルの
        相談を受けた。行政書士として対応できる範囲は？

compliance-officer:
        紛争性ある事案の代理交渉は弁護士法 72 条により弁護士の独占業務です。
        御所が対応可能なのは…
        （業際の境界と現実的な対応案を整理）
```

## 👥 含まれる 7 エージェント

| エージェント | 主な相談内容 |
|---|---|
| **compliance-officer** | 業際確認・倫理規程・利益相反・守秘義務違反リスク判断 |
| **case-intake** | 新規案件の受任可否判断・ヒアリング設計・見積もり |
| **document-drafter** | 申請書・添付書類・職務上請求理由書・上申書のドラフト |
| **deadline-tracker** | 申請期限・更新期限・時効・案件スケジュール管理 |
| **client-communicator** | 顧客への進捗報告・追加書類依頼・遅延説明・苦情対応 |
| **referral-coordinator** | 他士業への紹介・連携・共同受任・紹介料の取扱い |
| **jisaa-marketer** | 事務所マーケ・SEO・ブログ・地域営業・セミナー集客 |

## 🚀 クイックスタート

### 前提：ベースの C-Suite エージェント集を導入

このパックは以下と組み合わせて使うことを推奨します：

- [claude-code-c-suite-agents](https://github.com/OceansCreative/claude-code-c-suite-agents)（CFO・CMO・CRO 等の汎用 13 エージェント）

### このパックの追加

```bash
git clone https://github.com/OceansCreative/claude-code-agents-jisaa.git
cd /path/to/your/project

# 7 つの士業特化エージェントを追加
cp claude-code-agents-jisaa/.claude/agents/*.md .claude/agents/

# 士業特化の CLAUDE.md テンプレートを使う場合（推奨）
cp claude-code-agents-jisaa/CLAUDE.md.template ./CLAUDE.md
```

### CLAUDE.md を埋める

業種別の記入例を [`examples/`](./examples/) に用意しています：

- [行政書士事務所](./examples/gyosei-shoshi/CLAUDE.md)
- [税理士事務所](./examples/zeirishi/CLAUDE.md)
- [社会保険労務士事務所](./examples/sharoshi/CLAUDE.md)

## 💡 設計思想

このパックは「**一人事務所**」を主な想定読者として作っています。

- **業際遵守を最優先**：他士業の独占業務には踏み込まない判断ルールを各エージェントに組み込み
- **守秘義務の徹底**：顧客情報の取り扱いに最高レベルの注意を促す
- **「やらない」判断の重視**：受任すべきでない案件は明確に紹介・辞退を促す
- **専門家への委ねを明記**：法的紛争・税務調査など、専門外領域への適切な引き渡しを推奨
- **広告規制への配慮**：マーケティング提案は士業特有の規制を踏まえた範囲で行う

## ⚠️ 重要な注意

このエージェント集は**意思決定の補助**であり、**判断の代替**ではありません。

- 業際違反・倫理規程違反は懲戒処分・刑事罰・民事責任のリスクがあります
- 最終的な判断は、所属する単位会・連合会の規程に基づき自身で行う必要があります
- 法改正・通達変更により、エージェントの提案が古くなる可能性があります
- 利益相反・受任可否の最終確認は必ず人間（自分）が行ってください

## 🤝 コントリビュート

改善案・プルリクエスト歓迎です。出す前に [CONTRIBUTING.md](./CONTRIBUTING.md) と [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md) をご確認ください。新業種の example 追加（司法書士・弁理士・海事代理士など）は特に歓迎です。

- 🐛 バグ報告: [Issues](https://github.com/OceansCreative/claude-code-agents-jisaa/issues/new/choose)
- 🔒 脆弱性報告: [SECURITY.md](./SECURITY.md)
- 📜 変更履歴: [CHANGELOG.md](./CHANGELOG.md)

## 📜 ライセンス

MIT License - [LICENSE](./LICENSE) を参照。

自由に fork ・改変・商用利用してください。

## 🙋 つくったひと

開発・メンテナンス：**池田和司（[OceansBase](https://oceans-base.com)）**

[OceansBase](https://oceans-base.com) は島根県を拠点とする個人事業屋号で、受託開発・IT コンサル・コンテンツ制作を行っています。
本パックは、士業向け SaaS の開発過程で得られた業界知見をベースに設計しています。

---

<a id="english"></a>

# Claude Code Agents for Jisaa (English)

> A specialized agent pack for solo practitioners of Japanese licensed professional services — gyosei-shoshi (administrative scriveners), zeirishi (tax accountants), sharoshi (labor & social security consultants), shiho-shoshi (judicial scriveners), benrishi (patent attorneys).

## Seven Specialized Agents

- **compliance-officer** – Cross-license boundaries, ethics, conflicts of interest
- **case-intake** – New case assessment, hearing design, fee estimation
- **document-drafter** – Permit applications, attachments, formal letters
- **deadline-tracker** – Filing deadlines, statute of limitations, scheduling
- **client-communicator** – Progress reports, additional document requests, complaint handling
- **referral-coordinator** – Referrals across professional licenses
- **jisaa-marketer** – Practice marketing under regulatory advertising rules

## License

MIT - free to fork, modify, and use commercially.

## Author

Maintained by **Kazushi Ikeda** ([OceansBase](https://oceans-base.com)) — solo IT consulting practice in Shimane, Japan. This pack is informed by experience developing SaaS products for Japanese licensed professionals.
