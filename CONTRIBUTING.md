# コントリビューションガイド / Contributing Guide

このリポジトリへのコントリビューションを歓迎します。本ドキュメントは、Issue / Pull Request を出す際の指針です。

[English version below](#english)

---

## 🗣 まずは Issue で相談を

大きな変更（エージェントの追加・既存エージェントの方針変更・examples の追加）を計画している場合は、PR を出す前に **Issue で相談**してください。本パックは「業際遵守」「守秘義務」を最優先する設計方針があり、PR 前に方向性を揃えておくと手戻りが減ります。

軽微な修正（誤字・リンク切れ・記述の明確化）は Issue 不要、直接 PR で OK です。

## 🛠 開発フロー

1. リポジトリを fork する
2. ブランチを切る（例：`feat/add-shiho-shoshi-example`）
3. 変更をコミット（[Conventional Commits](https://www.conventionalcommits.org/) 推奨：`feat:` / `fix:` / `docs:` / `chore:` 等）
4. PR を main に向けて作成

## ✍️ エージェント定義を追加・変更するときの指針

このパックの 7 エージェントは、以下の共通設計に沿っています。新規エージェント追加や既存エージェント変更の際は、これらを踏襲してください。

- **業際は踏み越えない**：他士業の独占業務に踏み込む提案は出さない。グレーゾーンは「専門家確認」を促す
- **「やらない」判断を重視**：受任すべきでない案件は明確に紹介・辞退を促す
- **守秘義務を徹底**：顧客情報の取り扱いには最高レベルの注意を促す
- **広告規制への配慮**：マーケティング系の提案は士業特有の規制（不当誘致・誇大広告等）を踏まえる
- **法改正への注意喚起**：判断には常に「最新の法令・通達を確認」のリマインダーを入れる

## 📋 業種別 examples の追加について

`examples/` への新業種追加（司法書士、弁理士、海事代理士など）は特に歓迎します。追加時は：

1. `examples/<業種ローマ字>/CLAUDE.md` を作成
2. 既存の `gyosei-shoshi` / `zeirishi` / `sharoshi` を雛形として、業種特有の業際境界・特有の期限・特有の規制を反映
3. 実在の事務所名・顧客名・案件名は**絶対に使わない**（架空のサンプルに置き換える）
4. ルートの `README.md` の examples 一覧と `examples/README.md` にリンクを追加

## 🚫 機微情報・個人情報の扱い

- 実在の事務所名・顧客名・案件名・事件番号・実在の住所などは **絶対にコミットに含めない**
- スクリーンショットや会話例を載せる場合は、すべて架空のサンプルに置き換える
- API キー・認証情報は `.env` 等に分離し、`.gitignore` で確実に除外

## 📜 ライセンス

PR を出した時点で、変更内容が本リポジトリと同じ MIT License の下で公開されることに同意したものとみなします。

---

<a id="english"></a>

# Contributing Guide (English)

Contributions are welcome. This document outlines how to file issues and pull requests.

## File an Issue First for Large Changes

For substantial changes (adding agents, changing existing agent behavior, adding examples), please **open an issue first** to align on direction. This pack prioritizes regulatory compliance (業際遵守) and confidentiality (守秘義務), and aligning on these up front avoids rework.

For small fixes (typos, broken links, clarifications), feel free to open a PR directly.

## Development Flow

1. Fork the repository
2. Create a branch (e.g., `feat/add-shiho-shoshi-example`)
3. Commit your changes ([Conventional Commits](https://www.conventionalcommits.org/) recommended)
4. Open a PR against `main`

## Design Principles for Agent Definitions

The 7 agents in this pack follow a shared design philosophy. New or modified agents should respect:

- **Stay within license boundaries** — never recommend actions that overstep into another profession's exclusive scope
- **Prioritize "don't take this case"** — push for referral or decline when appropriate
- **Confidentiality first** — handle client data with maximum caution
- **Respect advertising regulations** — marketing suggestions must comply with profession-specific rules
- **Reminder of legal updates** — always remind users to verify current statutes

## Adding Industry Examples

New profession examples in `examples/` (shiho-shoshi, benrishi, etc.) are especially welcome. When adding:

1. Create `examples/<profession-romaji>/CLAUDE.md`
2. Use existing examples as templates; reflect profession-specific boundaries, deadlines, and regulations
3. **Never** use real firm/client/case names — always use fictional samples
4. Link the new example from root `README.md` and `examples/README.md`

## Sensitive Information

- Never commit real firm names, client names, case numbers, real addresses, etc.
- Replace screenshots and dialog examples with fictional samples
- Keep API keys and credentials in `.env` (gitignored)

## License

By submitting a PR, you agree that your contribution will be licensed under the same MIT License as this repository.
