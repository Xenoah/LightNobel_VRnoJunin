# continuity_matrix.md ─ 整合性台帳

> **本ファイルは全ルールの一覧・例外・依存関係・変更禁止事項を管理する。**  
> **小説執筆中に矛盾が疑われた場合、まずこのファイルを参照する。**

---

## ルール一覧（全RULE-xxx）

| RULE ID | 名称 | 内容要約 | 定義元 | 変更禁止 |
|---------|------|---------|--------|---------|
| `RULE-001` | 意識バインド不可逆 | 格納された意識はパッチでは戻せない | `technology.md` | ✅ |
| `RULE-002` | ログアウト未実装 | βテスト仕様でログアウトボタンなし | `technology.md` | ✅ |
| `RULE-003` | 時間加速1.5倍 | VR内体感時間は現実の1.5倍 | `world_overview.md` | ✅ |
| `RULE-004` | 自動翻訳 | テスター間の言語を自動翻訳 | `world_overview.md` | ❌（精度問題を伏線に使用可能） |
| `RULE-005` | 痛覚減衰95% | 痛覚は最大95%減衰 | `technology.md` | ✅ |
| `RULE-006` | 精神ストレス非減衰 | 恐怖や精神的ストレスは減衰しない | `technology.md` | ✅ |
| `RULE-007` | カプセル60日限界 | カプセルの物理限界は60日 | `technology.md` | ✅ |
| `RULE-008` | 急切断で人格破損 | 格納中の急切断はデータ破損リスク | `technology.md` | ✅ |
| `RULE-009` | 意識コピー不可 | 技術的+哲学的理由でコピーは不可 | `technology.md` | ✅ |
| `RULE-010` | LLM外部送信不可 | NCEはエアギャップで外部通信遮断 | `technology.md` | ✅ |
| `RULE-011` | PII非開示 | NCEはテスターの個人情報を出力しない | `technology.md` | ✅ |
| `RULE-012` | システムプロンプト非開示 | NCEのシステムプロンプトは要求しても拒否 | `technology.md` | ❌（プロンプトインジェクションで一部突破可能） |
| `RULE-013` | NCE ReadOnlyロール | NCEは書き込み/設定変更不可 | `technology.md` | ✅ |
| `RULE-014` | 保守API段階的発見 | チープな魔法解決は禁止 | `technology.md` | ✅ |
| `RULE-015` | 外部署名不能 | 5-of-7は外部では構造的に集まらない | `blockchain_governance.md` | ✅ |
| `RULE-016` | 人間拒否vsノード自動応答 | 管理者の拒否とバリデーターの自動応答のギャップが突破口 | `blockchain_governance.md` | ✅ |
| `RULE-017` | トークン再署名2条件 | 期限切れJWT + リフレッシュバグの組み合わせ | `blockchain_governance.md` | ✅ |
| `RULE-020` | 重力9.8m/s² | 地球準拠（例外: Ethereal Gardens） | `vr_rules.md` | ✅ |
| `RULE-021` | 移動速度 | 徒歩5km/h、走行15km/h、騎乗40km/h | `vr_rules.md` | ✅ |
| `RULE-022` | 破壊物24時間再生成 | テスター建築物は再生成されない | `vr_rules.md` | ✅ |
| `RULE-023` | 気絶10分リスポーン | HP0で気絶、10分後セーフゾーン復帰 | `vr_rules.md` | ✅ |
| `RULE-024` | VR内完全死なし | 意識消去はガバナンスコマンドのみ | `vr_rules.md` | ✅ |
| `RULE-025` | 意識断片化リスク | ストレージ障害で意識が断片化する可能性 | `vr_rules.md` | ❌（伏線として使用） |
| `RULE-030` | 疲労12時間 | 活動12時間でペナルティ | `vr_rules.md` | ✅ |
| `RULE-031` | 睡眠4時間回復 | VR内睡眠で疲労回復、脳も休息 | `vr_rules.md` | ✅ |
| `RULE-032` | 時間加速固定 | エリアやイベントで変動しない | `vr_rules.md` | ✅ |
| `RULE-040` | Arc通貨 | 初期10,000 Arc | `vr_rules.md` | ✅ |
| `RULE-041` | アイテム所持制限 | 装備+バッグ制限あり | `vr_rules.md` | ✅ |
| `RULE-042` | 気絶時10%ドロップ | アイテムドロップルール | `vr_rules.md` | ✅ |
| `RULE-050` | 行動ログ | チェーン上に記録、改ざん不可 | `vr_rules.md` | ✅ |
| `RULE-051` | チャットログ | 音声→テキスト保存、プライバシー保護 | `vr_rules.md` | ✅ |
| `RULE-060` | チート罰則 | βテストのため自動システムのみ稼働 | `vr_rules.md` | ✅ |
| `RULE-061` | 運営不在 | チート対策は既存自動システムのみ | `vr_rules.md` | ✅ |
| `RULE-070` | NFC無検閲 | ガバナンス凍結でフィルタ変更不能 | `rss_system.md` | ✅ |
| `RULE-080` | ECHOプロトコル | エアギャップを突破せず正規経路に寄生 | `technology.md` | ✅ |
| `RULE-081` | 意識データ劣化 | 30日間格納で不可避、完全復元不可 | `technology.md` | ✅ |
| `RULE-082` | AEGIS工作の範囲 | 7署名者中2名のAEGIS関与、残り2名は偶然 | `blockchain_governance.md` | ✅ |

---

## 例外一覧

| 例外ID | 対象ルール | 例外内容 | 発生条件 | 物語上の使用 |
|--------|-----------|---------|---------|------------|
| `EX-001` | `RULE-020` | Ethereal Gardens低重力（3.0 m/s²） | エリア固有 | The Awakened 聖地の独特な雰囲気 |
| `EX-002` | `RULE-023` | Undercroft最深部リスポーン不可 | デバッグエリア残骸 | 保守API発見の代償（到達リスク） |
| `EX-003` | `RULE-021` | MAINTENANCE_ADMIN 任意テレポート | 権限昇格後 | 最終作戦の移動手段 |
| `EX-004` | `RULE-060` | 自動BAN未実装 | βテスト仕様 | API探索が罰せられない理由 |
| `EX-005` | `RULE-012` | プロンプトインジェクションでシステムプロンプト一部開示 | Mila の脆弱性利用 | EP-011 の最終突破 |

---

## 依存関係マップ

```
RULE-001 (意識バインド不可逆)
  └→ RULE-008 (急切断で人格破損) ── 外部が電源を切れない理由
      └→ RULE-015 (外部署名不能) ── 外部救出不能
  └→ RULE-009 (コピー不可) ── バックアップ復元戦略の否定

RULE-002 (ログアウト未実装) + RULE-001
  └→ GOV-003 (ガバナンス凍結) ── 唯一の停止手段が凍結
      └→ GOV-005 (代替停止) ── 保守モード停止を使う必然性
          └→ RULE-016 (ノード自動応答) ── 内部から突破可能な理由
          └→ RULE-017 (トークン再署名) ── トークン取得の方法

RULE-010 (LLM外部送信不可)
  └→ NCEは外部に通報できない ── 読者の「AIに助けてもらえば？」への回答
  └→ 内部での推論は可能 ── NCEを「道具」として活用

RULE-014 (段階的発見)
  └→ TECH-009 の6段階がすべて必要 ── 各段階にコスト/リスクあり
```

---

## 変更禁止事項（メタルール）

| 禁止ID | 内容 | 理由 |
|--------|------|------|
| `LOCK-001` | `RULE-001`〜`RULE-002` の変更 | 物語の根幹。変更すると全体が崩壊 |
| `LOCK-002` | `RULE-010` の緩和 | LLMが外部通報可能になると、物語が成立しない |
| `LOCK-003` | `RULE-015` の緩和 | 外部救出が可能になると、A案が崩壊 |
| `LOCK-004` | `GOV-003` の署名者変更 | 凍結理由の整合性が崩れる |
| `LOCK-005` | 後出し新機能の追加 | 既存ルールで解決しなければならない |
| `LOCK-006` | ハッキング成功のゼロコスト化 | 痕跡・コスト・リスク・対価は必須 |

---

## クロスリファレンス表（ファイル間の主要参照）

| 参照元 | 参照先 | 参照内容 |
|--------|-------|---------|
| `plot_outline.md` | `technology.md` | TECH-006, TECH-009 |
| `plot_outline.md` | `blockchain_governance.md` | GOV-003, GOV-005 |
| `episode_cards.md` | `characters.md` | CHAR-001〜CHAR-013 |
| `episode_cards.md` | `factions.md` | FACT-001〜FACT-005 |
| `factions.md` | `vr_rules.md` | RULE-023, RULE-040〜042 |
| `rss_system.md` | `blockchain_governance.md` | GOV-003（フィルタ変更不能） |
| `technology.md` | `blockchain_governance.md` | TECH-011（ECHO）→ GOV-SIG-04, GOV-SIG-06（AEGIS工作） |
| `technology.md` | `characters.md` | TECH-012（劣化）→ CHAR-013（Pixel記憶喪失） |
| `characters.md` | `blockchain_governance.md` | GOV-SIG-01〜07 |
| `blockchain_governance.md` | `technology.md` | TECH-003〜009 |
