# セキュリティポリシー / Security Policy

[English version below](#english)

---

## サポート対象バージョン

最新の `main` ブランチおよび最新の release タグのみをサポート対象とします。古いバージョンへのバックポートは原則行いません。

| バージョン | サポート |
|---|---|
| 1.x.x  | ✅ |
| < 1.0  | ❌ |

## 脆弱性の報告

本リポジトリに脆弱性を見つけた場合、**公開 Issue ではなく**以下の方法で非公開に報告してください：

- **メール**: system@oceans-creative.com
- 件名は `[SECURITY] claude-code-agents-jisaa: <概要>` を推奨

報告に含めていただきたい情報：

1. 脆弱性の概要
2. 再現手順
3. 影響範囲（情報漏洩・権限昇格・コード実行 等）
4. 可能であれば緩和策の提案

### 想定される脆弱性の種類

本リポジトリは Markdown / 設定ファイル中心のため、典型的なコード実行系の脆弱性は限定的ですが、以下のようなケースを報告対象とします：

- `examples/` 内のテンプレートに、実在の個人情報や機密情報が誤って含まれている場合
- エージェント定義に、プロンプトインジェクションの抜け穴や深刻な業際違反を引き起こす指示がある場合
- リポジトリで参照している外部リンク・依存関係が侵害されている場合

### 対応の目安

- **24 時間以内**：受領確認の返信
- **7 日以内**：影響評価と対応方針の連絡
- **30 日以内**：修正版のリリース（重大度に応じて短縮）

## 開示ポリシー

修正版リリース後、報告者の同意を得たうえで脆弱性の概要を CHANGELOG / Release Notes に記載します。報告者の名前を含めるかは報告者の希望に従います。

---

<a id="english"></a>

# Security Policy (English)

## Supported Versions

Only the latest `main` branch and the latest release tag are supported. Backports to older versions are not provided.

| Version | Supported |
|---|---|
| 1.x.x  | ✅ |
| < 1.0  | ❌ |

## Reporting a Vulnerability

If you find a vulnerability, **do not file a public issue**. Report it privately:

- **Email**: system@oceans-creative.com
- Suggested subject line: `[SECURITY] claude-code-agents-jisaa: <summary>`

Please include:

1. Summary of the issue
2. Steps to reproduce
3. Scope of impact (data exposure, privilege escalation, code execution, etc.)
4. Suggested mitigation, if any

### Typical In-Scope Issues

Since this repository is primarily Markdown and configuration, classical RCE-style vulnerabilities are limited. In-scope examples:

- Templates in `examples/` accidentally containing real personal or confidential information
- Agent definitions that enable prompt injection or instructions leading to serious regulatory violations
- Compromised external links or dependencies referenced by the repository

### Response Targets

- **Within 24 hours**: acknowledgment of receipt
- **Within 7 days**: impact assessment and remediation plan
- **Within 30 days**: fix release (faster for high-severity issues)

## Disclosure Policy

After the fix is released, we will document the issue in CHANGELOG / Release Notes with the reporter's consent. Reporter attribution is included at the reporter's discretion.
