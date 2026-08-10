# SKILLS

`02_PROTOTYPES/<部門>` での検証を経て「効果確認・歯止め」まで到達した成功パターンを、スキルモジュールとして登録するディレクトリ。RULES.md の絶対ルール「1.3 成功パターンの標準化」に基づき、1部門の成果を属人化させず、他部門へ横展開できる状態にすることを目的とする。

## 構造

部門別に標準化可能な業務をスキルモジュールとして登録できるよう、発案部門ごとにディレクトリを分ける。

```
SKILLS/
  SKILL_TEMPLATE.md            … スキルモジュールREADMEの共通テンプレート
  manufacturing/                … 製造発案のスキル
    README.md                   … 製造部門の登録スキル一覧
    qc_story_defect_analysis/   … 例: QCストーリー不良解析
  engineering/                  … 技術発案のスキル
    README.md
    design_knowledge_search/    … 例: 設計ナレッジ検索
  production_engineering/       … 生産技術発案のスキル
    README.md
    predictive_maintenance_fmea_support/  … 例: 予兆検知・設備FMEA支援
  sales/                        … 営業発案のスキル
    README.md
    spec_quote_assist/          … 例: 仕様書/見積補助
```

- 各スキルモジュール（`SKILLS/<発案部門>/<スキル名>/`）には、`SKILL_TEMPLATE.md` に準拠した `README.md` と、実装（コード／プロンプト／テンプレート等）を格納する。
- 発案部門のディレクトリに置くのは「そのスキルが生まれた場所」を表すためであり、利用は部門を限定しない。他部門への適用実績は各スキルの README 内「横展開履歴」に記録する。

## 新規スキル登録の手順

1. `02_PROTOTYPES/<部門>` でのPoCが効果確認・歯止め（または同等の評価）まで到達したら、`SKILLS/<発案部門>/<スキル名>/` を作成する。
2. `SKILL_TEMPLATE.md` をコピーし、`README.md` を作成する。**Human-in-the-Loopチェックポイント**（RULES.md 1.2）は必須記入項目。
3. カイゼンは登録時に、他部門への横展開可能性を必ず検討し、推進リーダーに提案する（RULES.md 1.3）。
4. 他部門での適用が決まった場合、当該スキルの README「横展開履歴」に適用部門・適用日・調整点を追記する（コピーして新ディレクトリを作らない。実体は発案部門のディレクトリに一本化する）。

## 命名規則

- ディレクトリ名: 英語小文字スネークケース（例: `qc_story_defect_analysis`）
- 部門コード: `manufacturing` / `engineering` / `production_engineering` / `sales`
