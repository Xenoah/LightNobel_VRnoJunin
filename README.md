# VRの囚人 ─ Story Bible

> **ジャンル**: SF / サバイバル・スリラー / サイバーパンク  
> **想定メディア**: Web小説（長編 12話＋）  
> **最終更新**: 2026-02-22  

---

## 概要

次世代フルダイブVRデバイス **HVD（Human Virtualization Device）** のクローズドβテスト中、致命的バグにより約1万人のテスターの意識がブロックチェーン分散サーバーへ格納された。現実世界ではパニックが広がるが、当事者たちはそれに気づかず仮想世界で遊び続ける――やがて真実を知った主人公たちは、内部から脱出する方法を模索する。

---

## ファイル構成

| # | ファイル | 内容 |
|---|---------|------|
| 1 | [premise.md](premise.md) | 企画1ページ要約・テーマ・読者体験 |
| 2 | [world_overview.md](world_overview.md) | 世界の前提・社会状況・マスタータイムライン |
| 3 | [technology.md](technology.md) | HVD / カプセル / 神経I-O / VR基盤 / LLM制約 / ブロックチェーン格納 |
| 4 | [blockchain_governance.md](blockchain_governance.md) | A案核心：停止権限凍結・マルチシグ・署名者・閾値 |
| 5 | [vr_rules.md](vr_rules.md) | VR内物理法則・死・痛覚・疲労・時間加速・通貨・チート罰則 |
| 6 | [characters.md](characters.md) | 主要 / 準主要 / 敵対勢力キャラクター |
| 7 | [factions.md](factions.md) | 住民派閥（帰還派 / 定住派 / 宗教化派 / 暴徒 / 運営擁護派） |
| 8 | [bss_system.md](bss_system.md) | 掲示板BSSの仕様・UI・ニュース流入経路 |
| 9 | [plot_outline.md](plot_outline.md) | Act構成・主要ビート・伏線回収表 |
| 10 | [episode_cards.md](episode_cards.md) | 各話カード（最低12話） |
| 11 | [glossary.md](glossary.md) | 用語辞典 |
| 12 | [continuity_matrix.md](continuity_matrix.md) | 整合性台帳・ルール一覧・例外・変更禁止事項 |
| 13 | [open_questions.md](open_questions.md) | 未決事項・提案解・開示タイミング |
| 14 | [consistency_tests.md](consistency_tests.md) | 整合性テストケース（30項目以上） |

---

## 使い方

1. **本文執筆前**に全ファイルを通読し、矛盾がないか確認。
2. **執筆時**は `RULE-xxx` / `TECH-xxx` / `CHAR-xxx` 等のIDで設定を参照。
3. **執筆後**に `consistency_tests.md` のテストケースを走らせて矛盾を検出。
4. **ASSUMPTION:** / **OPEN_QUESTION:** タグは確定するまで変更禁止。確定したら本文に反映。

---

## ID体系

| 接頭辞 | 対象 | 例 |
|--------|------|----|
| `RULE-` | 世界ルール | `RULE-001` |
| `TECH-` | 技術設定 | `TECH-001` |
| `CHAR-` | キャラクター | `CHAR-001` |
| `FACT-` | 派閥 | `FACT-001` |
| `PLOT-` | プロットビート | `PLOT-001` |
| `EP-` | エピソード | `EP-001` |
| `GLOSS-` | 用語 | `GLOSS-001` |
| `BSS-` | BSS仕様 | `BSS-001` |
| `GOV-` | ガバナンス | `GOV-001` |
| `TEST-` | テストケース | `TEST-001` |

---

## 禁止事項（メタルール）

1. 後出しで都合の良い新機能を生やして解決しない
2. 「外部が実は簡単に救えた」をやらない（A案の凍結ロジック不可侵）
3. LLMが外部へ直接通報しない（制約固定）
4. ハッキング成功には必ず「痕跡・コスト・リスク・対価」を伴う
