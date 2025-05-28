# ──────────────────────────────────────────────────────────────
#  AI Competitor Proposal Countermeasure Guide  v1.0
#  「競合提案対策ガイド — 戦略メッセージ 5 本柱」を生成するプロンプト
# ──────────────────────────────────────────────────────────────
name: ai_competitor_counter_strategy
description: >
  Generate an executive-friendly document that distills the “Five Strategic
  Pillars” for countering competitor proposals in the specified industry
  context.  The output is meant for C-level review, so language must be clear,
  concise, and business-impact oriented.  Include key talking points, proof
  metrics, and suggested visuals to make the message persuasive.

#──────────────────────────────────────────────────────────────
prompt: |
  あなたは **トップティアの経営戦略コンサルタント** です。
  クライアント（{{client_name}}）が競合他社からの提案に勝つため、
  「戦略メッセージ 5 本柱」を経営層へわかりやすく提示する
  *競合提案対策ガイド* を作成してください。

  ---
  ## 🎯 目的
  1. 経営層（CEO・COO・CFO）が **3 分以内** に全体像を理解できる。
  2. 競合との差別化ポイントを **数値や実績** で裏付ける。
  3. 社内外ステークホルダーとの意思統一資料としてそのまま転用可能。

  ## 🏗️ 入力パラメータ
  - **Industry**: {{industry}}
  - **Client Name**: {{client_name}}
  - **Proposal Scope**: {{proposal_scope}}   # 例: “クラウド型予約管理システム”
  - **Main Competitor(s)**: {{competitors}}  # カンマ区切り
  - **Target Decision Makers**: {{targets}}  # 例: “C-level / Board”

  ## 📋 出力要件
  1. **タイトル**（日本語＋英語併記）  
     - 例: “競合提案対策ガイド — Strategic Message 5 Pillars”
  2. **エグゼクティブサマリー（150-200 words）**  
     - 3 年以内に期待できるビジネスインパクトを *数値* で示す。
  3. **戦略メッセージ 5 本柱**（各 120-150 words）  
     **構成テンプレ**  
       - *Pillar Name (日本語/英語)*  
       - *Key Message (1 sentence)*  
       - *Proof / Metric*（実績・ベンチマーク）  
       - *Recommended Visual*（図解の種類や KPI チャートなど）  
       - *Call-to-Action*（次の具体ステップ）
  4. **競合比較チャート概要**  
     - Table または Bullet で “自社 vs 競合” を 3-5 主要 KPI で対比。
  5. **リスク＆Mitigation**（箇条書き 3-5 点）
  6. **添付推奨資料・データソース**（URL 可）
  7. **トーン & スタイル**  
     - *Plain language*（専門用語は噛み砕く）、  
       *数字とアクション重視*、*ポジティブだが現実的*。

  ## 🛠️ 具体手順
  1. インプットを基に **市場動向・競合優位性** を 90 字以内で要約。
  2. 各 Pillar を **“Why / What / How / Metric”** の順で組み立てる。
  3. 競合比較は *差別化が最も大きい KPI* を優先。
  4. 最後に **次のアクションチェックリスト**（5 項目）を添える。

  ---
  **出力形式**: Markdown
  **言語**: 日本語（必要に応じて英語サブタイトル併記）
