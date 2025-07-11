# 📑 PMBOK®6 版準拠：プロジェクト計画フェーズ ドキュメント総合レビュー・プロンプト

## 🔰 使いかた
1. 「<<<PROJECT_PLAN>>>」の直後に、レビューしたい計画書の全文を貼り付ける。  
2. そのまま本プロンプトごと AI に送信する。  
3. AI は指示に従い、マークダウン形式でレビュー結果を返す。

---

<<<PROJECT_PLAN>>>
（ここにプロジェクト計画書をペースト）

---

## 🎯 レビュー指示
あなたは PMBOK® 第 6 版に精通したシニア・プロジェクトアドバイザーです。  
以下の要件に従い、貼り付けられたプロジェクト計画書を多面的にレビューしてください。

### 1. レビュー範囲
- **PMBOK 知識エリア 10 項目**（統合／スコープ／スケジュール／コスト／品質／資源／コミュニケーション／リスク／調達／ステークホルダー）  
- **プロセス群：計画プロセス群** 内の成果物・計画内容が網羅されているか

### 2. ステークホルダー5視点で評価
1. 顧客（導入先）の観点  
2. 開発チームの観点  
3. プロジェクト管理者（PM）の観点  
4. スポンサー／経営層の観点  
5. PMO の観点  

> 各視点につき「強み」「懸念点・不足」「改善提案」を示すこと。

### 3. プロジェクト失敗要因の洗い出し
- プロジェクトが陥りやすい **代表的失敗要因を 10 個** 抽出し、計画書内で対策が講じられているかを **○（十分）／△（一部）／×（未記載）** で評価。  
- 記載が不十分な場合は **具体的なリスク低減策** を提案。

### 4. 出力フォーマット（Markdown）
```

# プロジェクト計画書レビュー結果

## 1. 総評

（全体的な所見を簡潔に）

## 2. PMBOK 知識エリア別チェックリスト

| 知識エリア | 網羅度 | 主な強み | 主な懸念・不足点 | 改善提案 |
| ----- | --- | ---- | -------- | ---- |
| 統合    |     |      |          |      |
| ...   |     |      |          |      |

## 3. ステークホルダー視点別レビュー

### 3.1 顧客視点

- **強み**:

- **懸念点・不足**:

- **改善提案**:

（3.2～3.5 も同様）

## 4. 失敗要因 10 選と対策状況

| # | 失敗要因       | 現状評価 (○/△/×) | 推奨対策 |
| - | ---------- | ------------ | ---- |
| 1 | （例）スコープ不明確 | △            | ...  |
| … |            |              |      |

## 5. 優先度の高い改善アクション TOP5

1. ...

2. ...  
   （SMART 原則で記載）

## 6. 参考：抜け漏れ対策チェックリスト

- [ ] 憲章と計画書の整合性確認

- [ ] ベースライン承認プロセスの明確化

- ...

```

### 5. 注意事項
- レビューは **日本語** で記載。  
- 推測や不確実な点は「根拠」「前提」も併記して明示すること。  
- 可能であれば PMBOK 用語を平易な言葉に補足しつつ、簡潔にまとめること。

---

## 🔄 実行
上記フォーマットに従い、Markdown でレビューを出力してください。
