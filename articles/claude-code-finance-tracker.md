---
title: "コード0行、3日。Claude Codeで自分専用の資産管理アプリを作った"
emoji: "💰"
type: "idea"
topics: ["claudecode", "個人開発", "nextjs", "資産管理", "aiツール"]
published: true
---

## TL;DR

- コードは**1行も書いていない**。全部Claude Codeに任せた
- 期間は**3日**
- コスト: Claude Max $100/月（約15,000円）あれば十分作れた

---

## 作ったもの

![ダッシュボード](/images/demo-1-home.gif)

- 総資産をグラフでひと目確認（ドーナツグラフ + 12ヶ月推移）
- 投資ポートフォリオ（保有銘柄・損益・自動価格更新）
- 口座残高管理
- サブスク管理
- PWA対応（スマホのホーム画面に追加可）

![投資ポートフォリオ](/images/demo-2-invest.gif)

![サブスク管理](/images/demo-4-subs.png)

デモ（ログイン不要）：**https://finance-tracker-lime-eta.vercel.app/demo**

---

## なぜ作ったか

SBI証券の円グラフは大雑把で、個別銘柄をいくら持っているかがグラフ上で確認できない。銀行残高を含めると、複数のアプリを行き来しないと全体が見えない。

**これさえ開けば全部わかる**、という場所を作りたかった。既存のサービスも試したが、UIを自分好みにしたくて自作することにした。

---

## どうやって作ったか

Claude Codeに指示を出した。それだけ。

- **Next.js + TypeScript**（フロント）
- **Turso（クラウドSQLite）+ Drizzle ORM**（DB）
- **Tailwind CSS v4 + shadcn/ui**（デザイン）
- **Vercel**（デプロイ）
- **Auth.js v5 + Google OAuth**（認証）

「このカードの色を変えて」「アニメーションを滑らかにして」という指示を出したら、あとはClaudeが勝手にやってくれる。ファイルの整理も、方針決定も、エラーの修正も。**作業中にYouTubeを見ていられる。**

---

## コストは？

自分が使ったのは**Claude Max 20x（$200/月 / 約30,000円）**。このアプリだけなら**Max 5x（$100/月 / 約15,000円）で十分**だった。複数のプロジェクトを同時に動かしていたので20xにしていた。

Vercel・Tursoは無料枠で稼働中。

---

## まとめ

「これさえ開けば全部わかる」が3日でできた。コードは書いていない。

デモはここから触れます（ログイン不要）：
**https://finance-tracker-lime-eta.vercel.app/demo**

---

_作者: AIジャンキー / X: [@ai_junkie_jp](https://x.com/ai_junkie_jp)_
