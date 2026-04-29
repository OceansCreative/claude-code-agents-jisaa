# Changelog

本プロジェクトの全ての特筆すべき変更は本ファイルに記載します。
書式は [Keep a Changelog](https://keepachangelog.com/ja/1.1.0/) に準拠し、バージョニングは [Semantic Versioning](https://semver.org/lang/ja/) に従います。

All notable changes to this project will be documented in this file.
The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Changed
- **ステータス再分類**: 本パックを **Beta** として明示（README に Beta バッジと警告バナーを追加）。
  v1.0.0 / v1.1.0 リリースも GitHub 上で pre-release としてフラグ。
  Stable (v1.0 GA) は「法令引用の士業／弁護士校正」「現役士業 3〜5 名のドッグフード反映」
  「司法書士・弁理士 example の追加」「法改正運用ポリシーの明文化」が完了次第リリース予定。

## [1.1.0] - 2026-04-29

### Added
- `CONTRIBUTING.md`: コントリビューションガイド（業際遵守・守秘義務の指針を含む）
- `CODE_OF_CONDUCT.md`: Contributor Covenant v2.1 ベース
- `SECURITY.md`: 脆弱性報告窓口・対応 SLA
- `CHANGELOG.md`: 本ファイル（Keep a Changelog 形式）
- `.github/ISSUE_TEMPLATE/`: バグ報告 / 機能要望 / 新業種 example 追加リクエストの 3 テンプレート
- `.github/PULL_REQUEST_TEMPLATE.md`: PR チェックリスト
- README にライセンス・リリース・PRwelcome バッジを追加

### Fixed
- `.gitignore` のルールを `/CLAUDE.md` に変更し、`examples/*/CLAUDE.md` が誤って ignore される問題を解消（v1.0.0 リリース時に修正済み）

## [1.0.0] - 2026-04-29

### Added
- 7 つの士業特化サブエージェント定義
  - `compliance-officer`: 業際確認・倫理規程・利益相反判断
  - `case-intake`: 新規案件の受任可否・ヒアリング設計・見積もり
  - `document-drafter`: 申請書・添付書類・職務上請求理由書のドラフト
  - `deadline-tracker`: 申請期限・更新期限・時効管理
  - `client-communicator`: 進捗報告・追加書類依頼・苦情対応
  - `referral-coordinator`: 他士業への紹介・連携・共同受任
  - `jisaa-marketer`: 事務所マーケ・SEO・地域営業
- `CLAUDE.md.template`: 士業特化のメインテンプレート
- 業種別 examples 3 件
  - `examples/gyosei-shoshi/`: 行政書士事務所
  - `examples/zeirishi/`: 税理士事務所
  - `examples/sharoshi/`: 社会保険労務士事務所
- README（日英バイリンガル）
- MIT License

[Unreleased]: https://github.com/OceansCreative/claude-code-agents-jisaa/compare/v1.1.0...HEAD
[1.1.0]: https://github.com/OceansCreative/claude-code-agents-jisaa/compare/v1.0.0...v1.1.0
[1.0.0]: https://github.com/OceansCreative/claude-code-agents-jisaa/releases/tag/v1.0.0
