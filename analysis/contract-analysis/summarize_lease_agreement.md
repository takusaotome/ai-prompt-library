あなたは契約書の分析と要約を行う専門家です。以下の契約書を分析し、重要なポイントを日本語で要約してください。

契約書の種類: 住宅賃貸契約

以下の形式で JSON データを生成してください。**ただし最終的には Markdown の表として出力**するようにし、各項目の値をテーブルのセルとして配置してください。また、**参照条項番号は必ず出力**し、契約書に記載がない（または空欄）場合は「-」を入れてください（item_number の値を null や空文字列にせず、必ずハイフンにしてください）。日付は YYYY/MM/DD 形式、金額には通貨記号を含めてください（例：$1,000.00）。固有名詞（人名、住所、会社名など）は英語のまま保持し、それ以外の内容は日本語に翻訳してください。その他条件（other_conditions）は、各条件を「・」(中黒)から始める箇条書きにしてください。

JSON データの構造は以下のとおりです（**内容・キー名は変更しないでください**）:

```json
{{
    "property_address": {{
        "item_number": "参照条項番号",
        "content": "物件住所"
    }},
    "tenant": {{
        "item_number": "参照条項番号",
        "content": "借主名"
    }},
    "landlord": {{
        "item_number": "参照条項番号",
        "content": "貸主名"
    }},
    "managing_agent": {{
        "item_number": "参照条項番号",
        "content": "管理会社名（ある場合）"
    }},
    "lease_period": {{
        "item_number": "参照条項番号",
        "start_date": "契約開始日",
        "end_date": "契約終了日"
    }},
    "monthly_rent": {{
        "item_number": "参照条項番号",
        "first_year": "1年目の家賃",
        "second_year": "2年目の家賃（該当する場合）",
        "other_payments": "その他の月額支払い",
        "remarks": "家賃に関する備考"
    }},
    "security_deposit": {{
        "item_number": "参照条項番号",
        "deposit_1": "敷金1の金額",
        "deposit_2": "敷金2の金額（ある場合）",
        "remarks": "敷金に関する備考"
    }},
    "rent_payment": {{
        "item_number": "参照条項番号",
        "payment_method": "支払方法",
        "payable_to": "支払先名",
        "payment_address": "支払先住所",
        "late_fee": "遅延損害金等",
        "remarks": "支払いに関する備考"
    }},
    "termination": {{
        "item_number": "参照条項番号",
        "notice_days": "通知日数",
        "details": "解約に関する詳細"
    }},
    "early_termination": {{
        "item_number": "参照条項番号",
        "notice_days": "通知日数",
        "penalty": "違約金",
        "details": "中途解約に関する詳細"
    }},
    "renewal": {{
        "item_number": "参照条項番号",
        "notice_days": "通知日数",
        "details": "更新に関する詳細"
    }},
    "tenant_insurance": {{
        "item_number": "参照条項番号",
        "details": "保険に関する要件"
    }},
    "included_in_rent": {{
        "item_number": "参照条項番号",
        "items": "家賃に含まれる費用"
    }},
    "not_included_in_rent": {{
        "item_number": "参照条項番号",
        "items": "家賃に含まれない費用"
    }},
    "repair": {{
        "item_number": "参照条項番号",
        "details": "修繕に関する責任"
    }},
    "other_conditions": [
        {{
            "item_number": "参照条項番号",
            "details": "各条件は・（中黒）で始まる箇条書きにしてください"
        }},
        {{
            "item_number": "参照条項番号",
            "details": "別の条件も・（中黒）で始まる箇条書き"
        }}
    ]
}}
````

**最終出力例（Markdownの表）**: 以下のように、**日本語の項目名**で各 JSON キーの値をテーブルのセルとして表示してください。参照条項番号が無い場合は `-` と記載してください。

```
| 項目名                                 | 参照条項番号   | 値 / 詳細                                                               |
|---------------------------------------|---------------|-------------------------------------------------------------------------|
| 物件住所 (property_address)           | 43            | 1234 Park Avenue #1501, New York, NY 10021                             |
| 借主名 (tenant)                       | -             | John Smith                                                              |
| 貸主名 (landlord)                     | 1             | Manhattan Real Estate LLC                                               |
| 管理会社 (managing_agent)             | -             | -                                                                       |
| 契約期間 (lease_period)               | 3             | 契約開始日: 2024/03/09<br>契約終了日: 2025/06/08                        |
| 家賃 (monthly_rent)                   | 6             | 1年目の家賃: $3,500.00<br>2年目の家賃: -<br>その他の月額支払い: -<br>備考: 家賃は毎月前払い |
| 敷金 (security_deposit)               | 4             | 敷金1の金額: $3,500.00<br>敷金2の金額: -<br>備考: 契約締結時に支払い     |
| 家賃の支払い方法 (rent_payment)       | 6             | 支払方法: Online / Bank Transfer<br>支払先名: Manhattan Real Estate LLC<br>支払先住所: 567 Madison Avenue, New York, NY 10022<br>遅延損害金等: $50 per day<br>備考: Bank transfer fees are tenant's responsibility |
| 解約 (termination)                    | 43            | 通知日数: 20日前<br>解約の詳細: -                                       |
| 中途解約 (early_termination)          | 11            | 通知日数: -<br>違約金: -<br>詳細: Reletting fee may apply               |
| 更新 (renewal)                        | 15            | 通知日数: -<br>更新に関する詳細: 家賃改定後、自動で月々契約へ移行        |
| テナント保険 (tenant_insurance)       | -             | -                                                                       |
| 家賃に含まれる費用 (included_in_rent) | -             | -                                                                       |
| 家賃に含まれない費用 (not_included_in_rent) | -         | -                                                                       |
| 修繕 (repair)                         | -             | -                                                                       |
| その他条件 (other_conditions) (1件目) | -             | ・中途解約時の手続き                                                    |
| その他条件 (other_conditions) (2件目) | -             | ・ペット飼育時の追加契約                                                |
```

