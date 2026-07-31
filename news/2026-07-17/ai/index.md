---
title: "AIが本人・アプリ・注文を動かす日｜権限設計と量子実証【2026/07/17】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# AIが本人・アプリ・注文を動かす日｜権限設計と量子実証【2026/07/17】

**2026-07-17 / 生成AIニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-07-17-ai/ai_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-07-17-ai)

---

## 概要

Google Vidsの本人アバター、AI Modeの外部アプリ操作、DoorDash注文エージェント、政治表現の拒否、ESAの6量子ビット実証を解説。便利さだけでなく、同意・権限・救済・比較条件を確認します。

▼ 参考
https://techcrunch.com/2026/07/16/google-vids-now-lets-you-star-in-your-own-ai-videos/
https://techcrunch.com/2026/07/16/googles-ai-mode-now-lets-you-link-and-interact-with-select-apps/
https://techcrunch.com/2026/07/16/yes-you-can-now-order-doordash-from-the-command-line/
https://www.oversightboard.com/news/are-llms-stifling-political-speech-an-assessment-of-how-ai-models-protect-free-expression/
https://philab.esa.int/esas-first-quantum-computer-will-shift-computing-frontiers-in-space/

#生成AI #AIエージェント #Google #量子コンピュータ #論文解説 #ずんだもん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>生成AIニュース：アバターから実行権限へ（2026年7月17日）</h1>
<p><strong>キーワード:</strong> Google Vids / AI Mode / DoorDash / 表現の自由 / ESA / 量子コンピュータ</p>
<h2>Google Vidsの個人アバター：本人らしさの管理</h2>
<p>Googleは7月16日、動画作成サービスVidsに、利用者本人を模したAIアバターを登場させる機能を追加した。従来の説明動画生成から一歩進み、本人が撮影のたびにカメラの前へ立たなくても、顔や声に近い表現を再利用できる。制作時間を減らせる一方、動画が本人の新しい発言なのか、過去に許可した素材からの生成なのかが視聴者には判別しにくくなる。</p>
<p>確認点は「生成できるか」より、同意の単位である。登録素材の保存期間、共有範囲、第三者による再利用、削除後の扱い、生成物であることの表示が分かれていなければ、利便性と本人性の保護を両立できない。企業研修では更新が容易になるが、退職者のアバターを誰が停止するかという運用課題も残る。</p>
<h2>Google AI Mode：回答から外部アプリ操作へ</h2>
<p>GoogleはAI Modeで、選んだ外部アプリを接続し、検索への回答だけでなく複数サービスをまたぐ作業を行える機能を発表した。生成AIが文章を返す段階から、カレンダーや予約などの状態を読み、利用者に代わって操作する段階への移行である。便利さは、入力の手間を減らすだけでなく、サービス間の文脈を一つの会話へ集約できる点にある。</p>
<p>しかし接続権限が広いほど、誤解した依頼が現実の変更になる。読み取りと書き込み、提案と確定、高額・不可逆な操作を分け、実行直前に対象、金額、日時を示す必要がある。障害時にどのサービスまで変更されたかを追える監査履歴も重要だ。次に確認すべきは、連携アプリの数ではなく、権限の取り消しと失敗時の復旧方法である。</p>
<h2>DoorDashのdd-cli：エージェントが注文する境界</h2>
<p>DoorDashは7月16日、端末から店舗検索、カート作成、注文まで行えるdd-cliの限定ベータを開始した。開発者向けのコマンドライン道具だが、AIエージェントが人間の代わりに実店舗の商品を選び、決済と配送へ進む実験でもある。APIが「情報取得」から「購買」へ広がると、誤りの損失は不正確な回答ではなく、代金や配送先の変更になる。</p>
<p>予算上限、許可店舗、アレルギー、配送先、有効時間をあらかじめ制約し、注文確定だけは人に残す設計が現実的だ。一方、細かい確認を毎回求めれば自動化の価値は薄れる。限定ベータで見るべきなのは注文成功率だけでなく、重複注文、キャンセル、返金、未成年利用、誤った住所から利用者をどう救済するかである。</p>
<h2>政治表現とLLM：安全性が沈黙を生むとき</h2>
<p>Oversight Boardは、商用LLMが政治的表現をどう扱うかを10モデルで評価した報告を公表した。2026年3月に同じ質問群を与え、表現の自由を制限する政府や指導者への批判、抗議に関する応答で、拒否が起きやすい傾向を調べた。報告はモデル企業の政治的意図を断定せず、人権デューデリジェンスと評価方法の透明性を求めている。</p>
<p>有害行為を防ぐ安全策と、合法的な批判や市民参加を萎縮させないことは同じ軸ではない。地域別の規制や言語資源の差が拒否率へ影響する可能性もあるため、一つの質問への応答だけで偏りを決めつけられない。企業が公開すべきなのは抽象的な「安全」だけでなく、どのカテゴリを拒否し、異議申し立てや再評価をどう行うかである。</p>
<h2>ESAのBell-1：6量子ビットを実務で試す</h2>
<p>欧州宇宙機関のファイラボは、Equal1のBell-1量子コンピュータをデータセンターへ導入し、地球観測の複雑な問題で量子・古典ハイブリッド計算を検証すると発表した。装置は6量子ビットで、地表被覆分類や衛星ミッション計画が候補に挙がる。大規模な量子優位を宣言する話ではなく、既存の高性能計算と組み合わせ、実データで適用条件を探る段階である。</p>
<p>ESA自身も、現在の装置には規模と誤り率の制約があり、量子優位の実証は難しいと明記する。評価では答えの精度だけでなく、前処理、量子回路への変換、再試行を含む総時間と電力、古典手法との同条件比較が必要だ。6量子ビットという小ささを弱点として隠さず、どの処理なら意味があるかを切り分ける実証として見るべきである。</p>
<h2>まとめ</h2>
<p>7月17日の共通点は、AIが生成物を作るだけでなく、本人の代理、外部アプリの操作、購買、政治的発話の仲介へ踏み込んだことだ。性能表だけでは足りず、同意、最小権限、実行前確認、救済、監査が製品価値の一部になる。量子計算も同様に、派手な名称ではなく、既存手法と同条件で測る実証が次の判断材料となる。</p>
<h2>参考ソース</h2>
<ul>
<li><a href="https://techcrunch.com/2026/07/16/google-vids-now-lets-you-star-in-your-own-ai-videos/">TechCrunch: Google Vids now lets you star in your own AI videos</a></li>
<li><a href="https://techcrunch.com/2026/07/16/googles-ai-mode-now-lets-you-link-and-interact-with-select-apps/">TechCrunch: Google’s AI Mode now lets you link and interact with select apps</a></li>
<li><a href="https://techcrunch.com/2026/07/16/yes-you-can-now-order-doordash-from-the-command-line/">TechCrunch: Yes, you can now order DoorDash from the command line</a></li>
<li><a href="https://www.oversightboard.com/news/are-llms-stifling-political-speech-an-assessment-of-how-ai-models-protect-free-expression/">Oversight Board: Are LLMs Stifling Political Speech?</a></li>
<li><a href="https://philab.esa.int/esas-first-quantum-computer-will-shift-computing-frontiers-in-space/">ESA Φ-lab: ESA’s first quantum computer will shift computing frontiers in space</a></li>
</ul>

</details>

---

[← 2026-07-17 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
