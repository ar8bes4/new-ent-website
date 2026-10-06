---
title: "スタッフ写真更新 ROI・KPI記録"
type: roi-kpi-measurement
roi_measurement_version: v1
task_id: TASK-20261006-STAFF-PHOTOS
measured_on: 2026-10-06
measurement_class: reference-only
comparability_key: one-off-staff-photo-update-no-matched-baseline
timezone: Asia/Tokyo
prompt_started_at: 2026-10-06
delivery_completed_at: 2026-10-06
ai_active_minutes: 8
human_active_minutes: 2
waiting_or_external_minutes: 0
baseline_min_minutes: 25
baseline_max_minutes: 45
baseline_type: estimate
baseline_basis: "人手のみで写真2枚の確認・JPEG変換・スタッフカード2件のHTML更新・ローカル表示確認・差分確認・コミットまで行う想定。工程別に写真準備5–10分、HTML編集5–10分、確認5–10分、Git作業5–15分と置いた概算。実測対照ではない。"
confidence: low
quality_status: CONDITIONAL
artifacts: "50_SNS-WebSite/new-ent-website/staff.html; images/staff/watanabe-naoki.jpg; images/staff/hamano-ichita.jpg; commit fc19c90 (push completed by Antigravity per user)"
---

## Scope and deliverables

渡邉尚喜先生（大学院生）と濵野一太先生（医員）の写真をHEICからJPEGに変換し、スタッフ紹介ページの既存カードに設定しました。`coming-soon.svg` は残しています。コミット `fc19c90` は作成され、pushはAntigravityで実施済みとユーザーから確認しました。

## Measurement evidence and time definitions

- 対象日とタイムゾーンは2026-10-06、Asia/Tokyoです。コミット記録で完了時刻（2026-10-06 12:32:31 JST）は確認できますが、最初の依頼と各工程の開始・終了時刻は記録されていません。このため経過時間は算出しません。
- `ai_active_minutes: 8` は計測値ではなく、会話・実行履歴に残る調査、HEIC変換2件、画像確認、HTML編集、差分確認、コミット準備の作業量から置いた代表推定値です。妥当幅は5–10分程度と見ますが、操作ログに所要時間がないため信頼度は低です。
- `human_active_minutes: 2` は写真提供・確認とページ目視に伴う人手レビューの概算です。ユーザーの実時間は記録されていません。
- 待ち時間は独立して計測されていません。`waiting_or_external_minutes: 0` は未計測の記録上の値で、待ち時間が実際にゼロだったことを示しません。
- 写真の対応、画像参照先、`git diff --check` は確認済みです。ユーザーが `staff.html` の目視確認を行い、問題ないと報告しています。

## Human comparison and ROI assumptions

人手のみの基準時間25–45分は実測値ではなく、写真の確認・変換（5–10分）、HTML編集（5–10分）、表示・差分確認（5–10分）、コミット作業（5–15分）の工程別概算です。AI利用時はAI作業8分（概算代表値）と人手レビュー2分（概算）を合計して約10分と置きます。したがってモデル上の時間差は約15–35分の削減ですが、実測された効果ではありません。単一タスクの低信頼度推定であり、時間単価もないため金銭換算はしません。この記録は `reference-only` であり、比較可能なタスクの集計に含めません。

## Quality gates and limitations

- 画像ファイルの生成と人物への割当、HTMLの画像参照、および差分チェックを確認しました。
- ユーザーがスタッフページを目視し、表示に問題がないと確認しました。
- コミット `fc19c90` は作成済みです。pushは一度ネットワーク失敗後、Antigravityで成功したとユーザーから報告されました（独立確認なし）。
- 人手比較と時間計測はなく、作業時間と基準時間はいずれも推定です。pushもこちらでは再確認していないため、ROI評価の品質状態は `CONDITIONAL` とします。

## Rollup eligibility

`reference-only` の単発記録です。推定レンジは参考情報に限り、時間・金額の比較可能な集計には含めません（not aggregate）。
