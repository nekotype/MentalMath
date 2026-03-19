# MentalMath

ブラウザで遊べるフラッシュ暗算ゲームです。実体は単一ファイルの [`index.html`](/home/ryu/projects/MentalMath/index.html) です。

## Project Structure

- [`index.html`](/home/ryu/projects/MentalMath/index.html): アプリ本体
- [`test-results/browser-evidence`](/home/ryu/projects/MentalMath/test-results/browser-evidence): ブラウザ検証の証跡

## Browser Test Evidence

`test-results/browser-evidence` には以下を保存しています。

- `01-initial.png`: 初期表示
- `02-answer-ready.png`: ゲーム開始後、回答待ち状態
- `03-game-over.png`: 3回ミス後の終了状態
- `mentalmath-run.webm`: 自動ブラウザ検証の録画

## Test Conditions

- 対象: [`index.html`](/home/ryu/projects/MentalMath/index.html)
- 実行方式: `python3 -m http.server` でローカル配信し、Playwright でヘッドレス実行
- 確認内容:
  - 初期表示
  - 桁数と速度の変更
  - 空入力と非整数入力のバリデーション
  - 正答後のラウンド進行
  - ゲーム終了後の Best Score / 履歴更新

## Notes

- 証跡は 2026-03-19 に取得しました。
- 実行時は Linux 側 Chromium の不足ライブラリを一時的に補って検証しています。
