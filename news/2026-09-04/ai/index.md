---
title: "【速報】ChatGPT・Claude・Grok同時障害、Nvidiaが1.3兆円買収 2026/09/04"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# 【速報】ChatGPT・Claude・Grok同時障害、Nvidiaが1.3兆円買収 2026/09/04

**2026-09-04 / 生成AIニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-09-04-ai/ai_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-09-04-ai)

---

## 概要

9月3日に起きたChatGPT・Claude・Grok・Geminiの同時障害、NvidiaによるHugging Face買収、Thinking Machinesの大型調達交渉、MetaのAI利用データ提供割引、AIガードレール除去ビジネス、そしてIonQ・NVIDIA・qBraidの量子誤り訂正の進展を解説します。

▼ 今日のトピック
・ChatGPT・Claude・Grok・Gemini、まれな同時障害
・Nvidia、Hugging Faceを129億ドルで買収
・Thinking Machines、時価総額400億ドルで調達交渉
・Meta、AI利用データ提供に最大95%割引
・Abliteration.ai、AIガードレール除去をビジネス化
・IonQ・NVIDIA・qBraid、量子化学シミュレーションでエラー率54%減

▼ 参考記事・ソース
・Ars Technica「Four major AI models suffer rare overlapping downtime」 https://arstechnica.com/ai/2026/09/four-major-ai-models-suffer-rare-overlapping-downtime/
・TechCrunch「Nvidia confirms it will buy Hugging Face for $12.9 billion」 https://techcrunch.com/2026/09/03/nvidia-confirms-it-will-buy-hugging-face-for-12-9-billion/
・CNBC「Nvidia agrees to buy Hugging Face for $12.9 billion」 https://www.cnbc.com/2026/08/27/nvidia-hugging-face-acquisition.html
・TechCrunch「Accel reportedly in talks to lead $1B round for Thinking Machines at $40B valuation」 https://techcrunch.com/2026/09/03/accel-reportedly-in-talks-to-lead-1b-round-for-thinking-machines-at-40b-valuation/
・TechCrunch「Meta is paying to peek at how you use their latest AI model」 https://techcrunch.com/2026/09/03/meta-is-paying-to-peek-at-how-you-use-their-latest-ai-model/
・TechCrunch「Abliteration.ai is making a business out of removing AI guardrails」 https://techcrunch.com/2026/09/03/abliteration-ai-is-making-a-business-out-of-removing-ai-guardrails/
・Quantum Computing Report「IonQ, NVIDIA, and qBraid Demonstrate 54% Error Reduction in Mid-Circuit Quantum Simulations」 https://quantumcomputingreport.com/ionq-nvidia-and-qbraid-demonstrate-54-error-reduction-in-mid-circuit-quantum-simulations/

#生成AI #ChatGPT #Grok #量子コンピュータ #ゆっくり解説 #AIニュース

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>生成AI・量子コンピュータニュース（2026年9月4日）</h1>
<p><strong>キーワード:</strong> ChatGPT障害 / Grok障害 / Hugging Face買収 / Thinking Machines / AIガードレール解除 / 量子誤り訂正</p>
<h2>オープニング：2026年9月4日 — 生成AIニュース</h2>
<ul>
<li>9月3日、ChatGPT・Claude・Grok・Geminiが立て続けにエラーを起こす珍しい同時障害が発生</li>
<li>Nvidiaが「GitHub of AI」ことHugging Faceを129億ドルで買収へ</li>
<li>Thinking MachinesがAccel主導で時価総額400億ドルの10億ドル調達交渉中</li>
<li>量子コンピュータはIonQ・NVIDIA・qBraidが化学シミュレーションのエラー率を54%削減</li>
</ul>
<h2>ChatGPT・Claude・Grok・Gemini、まれな同時障害</h2>
<ul>
<li>2026年9月3日（米国時間）、OpenAIのChatGPT・Codex、AnthropicのClaude（Opus 4.8・Opus 5系）、xAIのGrok、GoogleのGeminiが立て続けにエラー率上昇・ダウンを起こした</li>
<li>OpenAIの障害は米太平洋時間午前10時58分に発生を認知、午前11時50分に緩和策を適用して「監視」状態へ移行したとステータスページで発表</li>
<li>Anthropicはclaude.ai、Claude API、Claude Code、Claude Cowork全体で複数モデルにわたるエラー増加を確認</li>
<li>xAIもGrokの障害を認め対応中と発表</li>
<li>報道各社はAIモデル自体の不具合ではなく、CloudflareやAzureなど各社が共有するクラウド・CDN基盤側の障害が原因である可能性が高いと指摘</li>
<li>4社の主要チャットボットが同じタイミングで止まった点で、生成AIサービスが少数の基盤インフラに依存しているリスクが改めて浮き彫りになった</li>
</ul>
<h2>Nvidia、Hugging Faceを129億ドルで買収</h2>
<ul>
<li>Nvidiaが「オープンソースAIのGitHub」と呼ばれるHugging Faceの買収に合意したと2026年9月3日に確認</li>
<li>買収額は約129億ドル（一部報道では140億ドル規模との観測もある）で、うち約119億ドルを既存株主へ、最大10億ドルを入社する従業員向けの引き留め株式に充てる</li>
<li>Hugging Faceには300万以上のモデル、50万件のデータセット、100万件のアプリケーションがホストされ、開発者は1800万人以上とされる</li>
<li>買収成立は2027年前半を見込み、規制当局の承認待ち</li>
<li>Nvidiaは昨年、Hugging Faceの株式取得を70億ドル評価で打診し断られた経緯があり、今回は自社スタックに統合せず中立性を保つ方針とCEOジェンスン・フアン氏が説明</li>
<li>半導体を供給してきた相手を買収する形で、Nvidiaがオープンソースの流通経路そのものを握る動きとして注目される</li>
</ul>
<h2>Thinking Machines、Accel主導で時価総額400億ドルの調達交渉</h2>
<ul>
<li>元OpenAI CTOのミラ・ムラティ氏が率いるThinking Machines Labが、既存出資者Accelを主導に少なくとも10億ドルの資金調達を交渉中と2026年9月3日に報道</li>
<li>想定される評価額は約400億ドルで、昨年末に検討していた40億〜50億ドル調達・評価額50億ドル超という水準からは切り下げ</li>
<li>Nvidiaも出資参加を協議しているという</li>
<li>同社は今年7月に最初のAIモデル「Inkling」をリリース済みで、年間経常収益（ARR）は1億ドルを超えると報じられている</li>
</ul>
<h2>Meta、新AIモデルの利用データ提供に最大95%割引</h2>
<ul>
<li>Metaがコーディングなどのエージェント運用向け新モデル「Muse Spark」で、プロンプトと出力を今後のモデル開発向けに提供する利用者に対し平均95%の割引を提示していることが判明</li>
<li>通常価格は入力100万トークンあたり1.25ドル・出力100万トークンあたり4.25ドルだが、データ提供に同意する「貢献者価格」ではそれぞれ10セント・20セントまで下がる</li>
<li>Metaは今年、社員のPC利用状況を追跡する社内施策を試みたが強い反発を受け6月に停止した経緯があり、今回の割引は学習データ確保に向けた新たな手法とみられる</li>
<li>利用料を下げる代わりに利用実態を差し出させる設計は、AI企業がデータ調達で規約上の同意をどこまで実質的な選択にできているかという論点を投げかける</li>
</ul>
<h2>Abliteration.ai、AIガードレール除去をビジネス化</h2>
<ul>
<li>「アブリテーション」と呼ばれる、モデルが有害な要求を拒否する挙動を除去する手法をそのままサービス化したAbliteration.aiが取材で明らかに</li>
<li>Z.aiが公開したばかりの「GLM-5.3」を含むオープンウェイトモデルの改造版をホストし、ブラウザまたはAPI経由で利用可能にしている</li>
<li>昨年末の創業を経て今年3月に法人化、現在はベンチャーキャピタルと資金調達の協議中で、直接の顧客収入で運営</li>
<li>同社はSNS上で「他モデルが拒否する攻撃的サイバー・レッドチーム・エージェントテストの作業を可能にする」ことが目的だと説明</li>
<li>本人確認は主にクレジットカードの記録に依存し、組み込みの制限は最小限。任意でモデレーション層を追加できるオプションは用意している</li>
<li>AI安全非営利団体CivAIの研究責任者アンドリュー・ユン氏は、アブリテーションは「モデルをソシオパスにするようなもの」と批判し、大規模提供が実害につながりかねないと指摘</li>
</ul>
<h2>IonQ・NVIDIA・qBraid、量子化学シミュレーションでエラー率54%減</h2>
<ul>
<li>IonQ、NVIDIA、qBraidの3社が2026年9月上旬、量子化学シミュレーションにおける論理エラー率を54%削減したと発表</li>
<li>IonQのバリウムベース開発システムとNVIDIAのGPUアクセラレーテッド計算を組み合わせ、一般化超高速符号化・クリフォードノイズ低減・アクティブな中間回路測定を組み合わせた「アプリケーション native」な誤り軽減フレームワークを採用</li>
<li>6量子ビットの符号化シミュレーションステップで、従来の物理的トロッター実行と比べて論理エラー率を54%削減</li>
<li>事後選択（良い結果だけを選び出す）ではなく、NVIDIAのGH200システム上で動く機械学習モデルが5万7536サンプルから適切な安定化子をリアルタイムに選ぶ「アクティブ測定」が鍵</li>
<li>量子ビット数を増やす競争から、誤りを抑えて計算品質を上げる競争へと業界の関心が移る中での具体的な成果として位置づけられる</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>9月3日は主要チャットボット4社が同時に不調になり、生成AIサービスが少数の共有クラウド基盤に依存する脆弱性が可視化された</li>
<li>一方でNvidiaのHugging Face買収やThinking Machinesの大型調達交渉など、AI業界の資本・インフラ集約は加速している</li>
<li>Metaのデータ提供割引やAbliteration.aiのガードレール除去ビジネスは、便利さ・収益性と安全性・プライバシーのトレードオフが利用者に転嫁されている実例</li>
<li>量子コンピュータ分野は量から質への転換が進み、IonQ・NVIDIA・qBraidの誤り訂正の実装成果はその流れを裏付けるものになった</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://arstechnica.com/ai/2026/09/four-major-ai-models-suffer-rare-overlapping-downtime/">Four major AI models suffer rare overlapping downtime - Ars Technica</a></li>
<li><a href="https://techcrunch.com/2026/09/03/nvidia-confirms-it-will-buy-hugging-face-for-12-9-billion/">Nvidia confirms it will buy Hugging Face for $12.9 billion - TechCrunch</a></li>
<li><a href="https://www.cnbc.com/2026/08/27/nvidia-hugging-face-acquisition.html">Nvidia agrees to buy Hugging Face for $12.9 billion - CNBC</a></li>
<li><a href="https://techcrunch.com/2026/09/03/accel-reportedly-in-talks-to-lead-1b-round-for-thinking-machines-at-40b-valuation/">Accel reportedly in talks to lead $1B round for Thinking Machines at $40B valuation - TechCrunch</a></li>
<li><a href="https://techcrunch.com/2026/09/03/meta-is-paying-to-peek-at-how-you-use-their-latest-ai-model/">Meta is paying to peek at how you use their latest AI model - TechCrunch</a></li>
<li><a href="https://techcrunch.com/2026/09/03/abliteration-ai-is-making-a-business-out-of-removing-ai-guardrails/">Abliteration.ai is making a business out of removing AI guardrails - TechCrunch</a></li>
<li><a href="https://quantumcomputingreport.com/ionq-nvidia-and-qbraid-demonstrate-54-error-reduction-in-mid-circuit-quantum-simulations/">IonQ, NVIDIA, and qBraid Demonstrate 54% Error Reduction in Mid-Circuit Quantum Simulations - Quantum Computing Report</a></li>
</ul>

</details>

---

[← 2026-09-04 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
