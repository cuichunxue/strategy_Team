# SKILLS

`02_SOLUTIONS/<部門>` での実証を経て定量インパクトが確認された高度な改革フレームワーク・解析手法を、汎用モジュールとして蓄積するディレクトリ。RULES.md 1.4（成功パターンの標準化・横展開）に基づき、1部門の成果を属人化させず、他部門へ横展開できる状態にすることを目的とする。

## 構造

改革フレームワークはどの部門でも再利用されうる汎用資産であるため、部門別ではなく**フレームワーク（手法）単位**でディレクトリを分ける。

```
SKILLS/
  SKILL_TEMPLATE.md                  … スキルモジュールREADMEの共通テンプレート
  qc_story_audit/                    … 統計的品質管理・QCストーリー監査
  weibull_reliability_analysis/      … Weibull分布による設備寿命・予兆検知解析
  design_knowledge_structuring/      … 技術設計ナレッジの構造化
  spec_quote_automation/             … 営業〜技術の仕様選定・見積自動化（部門横断）
  bpr_spec_framework/                … BPR仕様フレームワーク（業務プロセス再設計の共通フォーマット）
```

上記は現時点で登録済みのスキル一覧であり、非網羅的リストである。`02_SOLUTIONS` での実証を経て、統計解析・機械学習モデル・業務プロセス設計等、新たな高度手法が実証され次第、随時追加する。

## スキル一覧・ステータス

| フレームワーク名 | 発祥部門 | 対象業務 | ステータス |
|---|---|---|---|
| `qc_story_audit` | manufacturing | 統計的品質管理・QCストーリー監査 | 提案 |
| `weibull_reliability_analysis` | production_engineering | 設備寿命・予兆検知解析 | 提案 |
| `design_knowledge_structuring` | engineering | 設計ナレッジの構造化 | 提案 |
| `spec_quote_automation` | sales × engineering | 仕様選定・見積自動化 | 提案 |
| `bpr_spec_framework` | sales | BPR仕様フレームワーク | 提案 |

- 各スキルモジュール（`SKILLS/<フレームワーク名>/`）には、`SKILL_TEMPLATE.md` に準拠した `README.md` と、実装（コード／プロンプト／テンプレート等）を格納する。
- フレームワークが最初に実証された部門は README 内「発祥部門」に記録するが、ディレクトリは部門で分けない。他部門への適用実績は「横展開履歴」に記録する。

## 新規スキル登録の手順

1. `02_SOLUTIONS/<部門>` での実証が定量インパクト（RULES.md 1.2）を確認できたら、`SKILLS/<フレームワーク名>/` を作成する。
2. `SKILL_TEMPLATE.md` をコピーし、`README.md` を作成する。**Human-in-the-Loopチェックポイント**（RULES.md 1.3）と**定量インパクト実績**は必須記入項目。
3. マッケンジーは登録時に、他部門への横展開可能性を必ず検討し、改革オーナーに提案する（RULES.md 1.4）。
4. 他部門での適用が決まった場合、当該スキルの README「横展開履歴」に適用部門・適用日・調整点・実績値を追記する（コピーして新ディレクトリを作らない。実体は1本化する）。
5. 上記の一覧表を更新する。

## 命名規則

- ディレクトリ名: 英語小文字スネークケース（例: `qc_story_audit`）
