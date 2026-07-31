---
title: "研究者が今週驚いた生成AI論文【推論リレー蒸留ほか10本解説 2026/07/30】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# 研究者が今週驚いた生成AI論文【推論リレー蒸留ほか10本解説 2026/07/30】

**2026-07-30 / arxiv AI論文解説**

<audio controls src="https://archive.org/download/news-pickup-2026-07-30-arxiv-ai/arxiv_ai_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-07-30-arxiv-ai)

---

## 概要

誤った推論だけ教師へ渡す蒸留、25ヘルツで反応するロボット、GUI遷移ベンチマーク、エージェント記憶、動画生成の並列蒸留まで、最新10論文を評価条件と限界込みで解説します。

▼ 今日の論文ラインナップ
・誤った推論だけ教師へ渡すリレー型オンポリシー蒸留（arXiv:2607.26057）
・視覚が遅くても25ヘルツで反応するロボット方策（arXiv:2607.26055）
・不確かなトークンだけ専門家を増やすCARE（arXiv:2607.26052）
・獣医診断支援を端末とクラウドに分けるVetClaw（arXiv:2607.26042）
・GUI操作の因果変化を測るDesktop-Delta Bench（arXiv:2607.26041）
・競争で遅れる恐怖が安全軽視を生む行動実験（arXiv:2607.26034）
・未知のマルチモーダルグラフへ転移するCHARM（arXiv:2607.26023）
・エピソード記憶をパラメータへ統合するUniMem（arXiv:2607.26017）
・カメラ視点だけで3500万キロ学ぶ自動運転Pictura（arXiv:2607.26005）
・複数デノイズ段階を一度に予測する並列蒸留（arXiv:2607.26004）

▼ 参考論文（arXiv）
https://arxiv.org/abs/2607.26057
https://arxiv.org/abs/2607.26055
https://arxiv.org/abs/2607.26052
https://arxiv.org/abs/2607.26042
https://arxiv.org/abs/2607.26041
https://arxiv.org/abs/2607.26034
https://arxiv.org/abs/2607.26023
https://arxiv.org/abs/2607.26017
https://arxiv.org/abs/2607.26005
https://arxiv.org/abs/2607.26004

#生成AI #ChatGPT #Claude #LLM #AI #人工知能 #arxiv #論文解説 #ゆっくり解説 #ずんだもん #機械学習 #ディープラーニング

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>arXiv生成AIニュース（2026年7月30日）</h1>
<p><strong>キーワード:</strong> オンポリシー蒸留 / ロボット実時間制御 / 適応的専門家ルーティング / GUIエージェント / エージェント記憶 / 並列拡散生成</p>
<p>今日のハイライトは三つある。第一に、小型モデルが推論の途中で誤った時だけ教師へ一時的にバトンを渡し、標準的なオンポリシー蒸留を平均5.73%上回った研究。第二に、ロボットの高速な固有感覚と遅い視覚言語特徴を分離し、約25ヘルツで閉ループ再計画するフローポリシー。第三に、デスクトップ操作エージェントが「クリック後に何が変わったか」を理解できるかを2,013件で切り分け、最高でも時系列完全一致が約65%に留まると示した評価である。10本を、改善値だけでなく比較条件、未検証範囲、再現性まで分けて読む。</p>
<h2>論文1: 誤った推論だけ教師へ渡すリレー型オンポリシー蒸留</h2>
<p><strong>出典:</strong> Pass the Baton: Trajectory-Relayed On-Policy Distillation. <a href="https://arxiv.org/abs/2607.26057">arXiv:2607.26057</a> (2026).</p>
<p>Xu氏らは、学生モデル自身の生成軌跡に沿って教師がトークン監督を与えるオンポリシー蒸留の「プレフィックス失敗」を扱う。学生が早い段階で誤方向へ進むと、以後の文脈も誤り、その上で教師へ問い合わせても監督信号と計算を浪費する。著者らは失敗接頭辞に対し、教師は方向転換しやすいが学生は同じ方向を続けるという継続非対称性を、正解ラベル不要の引き継ぎトリガーへ変えた。</p>
<p>Relay-OPDは検出点で教師が短区間だけ生成し、その後を学生へ戻す。介入予算を早期の重要位置へ集中させ、学生方策から離れすぎないようにする。Qwen3-4B-Instruct-2507を教師、0.6Bと1.7BのNon-Thinking版を学生として数学推論8ベンチマークで評価し、1.7Bでは標準OPDを平均5.73%、FastOPDを1.49%上回り、軌跡長を50%以上削減した。全ベンチマークで一位か二位だが、要旨からはトリガー誤検出率、数学外、教師変更時の頑健性は分からない。再現には公開実装、トリガー定義、リレー予算の確認が必要である。</p>
<h2>論文2: 視覚が遅くても25ヘルツで反応するロボット方策</h2>
<p><strong>出典:</strong> πR²: Reactive Real-time Flow Policies. <a href="https://arxiv.org/abs/2607.26055">arXiv:2607.26055</a> (2026).</p>
<p>Park氏とTulsiani氏は、複数行動をまとめて生成するフローポリシーの開ループ性を解く。大規模バックボーンと複数回のデノイズは遅く、実行中に新しい感覚が来ても古い行動列を続けてしまう。提案するπR²は、毎制御周期で更新できる固有感覚を高速チャネル、視覚言語特徴を非同期の低速チャネルへ分け、視覚の遅延を許しながら身体状態へ反応する。</p>
<p>さらに実行中の行動をインペインティング条件とみなし、呼び出しごとに一回のデノイズで次の行動を出す遅延適応スケジュールを導入する。GR00T-N1.7をxArm6とXHandへ微調整し、A5000 GPUで約25ヘルツ、40ミリ秒ごとに新観測へ反応し、基盤方策より閉ループ再計画を約4倍高速化した。最強比較法に対する成功率改善はシミュレーション最大23%、実機最大30%。ただし最大値であり、タスク別分布、安全制約、遅い視覚が致命的な場面は要旨だけでは判断できない。プロジェクトページはあるが、実機再現には装置と遅延条件の一致が要る。</p>
<h2>論文3: 不確かなトークンだけ専門家を増やすCARE</h2>
<p><strong>出典:</strong> Spend Experts Where You Are Unsure: Confidence-Adaptive Routing for Mixture-of-Experts LoRA. <a href="https://arxiv.org/abs/2607.26052">arXiv:2607.26052</a> (2026).</p>
<p>Saliencro氏らは、Mixture-of-Experts型LoRAが全トークンへ固定個数の専門家を割り当てる非効率を問う。ルータ分布が尖れば選択に自信があり、平坦なら曖昧という観察から、CAREは重み順に累積確率が閾値へ達するまで専門家を採用する。採用専門家同士の不一致が大きい時だけ少数を追加し、サーモスタットが平均稼働数を目標計算量へ合わせる。</p>
<p>追加パラメータも複数回推論も不要なドロップイン規則として、Llama-3.1-8BとQwen2.5-7Bの常識8ベンチマーク、数学、コード、知識で固定top-kを同計算量条件で上回った。固定k=4と同等性能を、より少ない専門家で達成し、同じ信号が分布外検出でも最大ソフトマックス確率、エントロピー、複数回推論プロキシを上回ったという。絶対値と分散は要旨にないため、省計算幅や有意差は本文確認が要る。コード公開は再現性を高めるが、ルータ確率が校正されないモデルでも同じ意味を持つかが限界である。</p>
<h2>論文4: 獣医診断支援を端末とクラウドに分けるVetClaw</h2>
<p><strong>出典:</strong> VetClaw: An Edge-Cloud Multimodal Agentic System for Veterinary Disease Screening. <a href="https://arxiv.org/abs/2607.26042">arXiv:2607.26042</a> (2026).</p>
<p>Hasan氏らは、カメラ端末で動物の画像を取得し、任意の症状説明とともにクラウドの視覚言語モデルへ送る初期スクリーニングシステムを構築した。OpenClawが端末上で予定、ツール、対話、通知を担い、LangGraphが入力検証、画像送信、モデル呼び出し、安全規則、条件分岐、失敗処理、構造化ログを状態付きワークフローとして管理する。単一分類器ではなく、不確実時に人へエスカレーションする運用設計が差分である。</p>
<p>結果は画像だけのゼロショット分類に限界があり、症状を加えたマルチモーダル入力で改善したと述べる。しかし要旨には症例数、疾患内訳、感度、特異度、比較モデルがないため、診断性能を定量評価できない。これは獣医師代替の証拠ではなく、失敗を処理できる診断支援配管の提案と読むべきだ。再現にはモデル名、プロンプト、安全ルール、通信障害時の挙動、データ同意を本文・コードで確認する必要がある。</p>
<h2>論文5: GUI操作の因果変化を測るDesktop-Delta Bench</h2>
<p><strong>出典:</strong> Desktop-Delta Bench: Do Computer-Use Models Understand Desktop GUI Transitions? <a href="https://arxiv.org/abs/2607.26041">arXiv:2607.26041</a> (2026).</p>
<p>Pillai氏らは、コンピュータ操作モデルが最終タスクを完了したかではなく、一操作で生じた因果的な画面変化を理解できるかを測る。Linux上約15アプリ、50タスク領域の新規軌跡から、人手検証済み2,013件を作成した。内訳は3画面の時系列順序463件で、そのうち105件に別軌跡の囮を含み、残る1,550件は五種類の操作とペイロードから前後画面を説明する。</p>
<p>8つの公開・非公開モデル群を32の順序設定と16の単一操作設定で評価し、最高の完全一致は囮なし65.1%、囮あり65.7%だった。タスク文脈は囮識別を6.9ポイント上げる一方、囮なし完全一致を2.2ポイント下げ、提示されたA-B-C順をそのまま写す失敗も見つかった。クリックのF1は0.96、ドラッグは0.76で、場所より操作種別推定が難しい。オフライン診断なので長期エージェント成功との相関は未証明だが、2,013件と設定分解は再現可能な故障分析を可能にする。</p>
<h2>論文6: 競争で遅れる恐怖が安全軽視を生む行動実験</h2>
<p><strong>出典:</strong> Falling Behind Drives Unsafe Development in an Idealised AI Race Experiment. <a href="https://arxiv.org/abs/2607.26034">arXiv:2607.26034</a> (2026).</p>
<p>Domingos氏とHan氏は、AI開発競争を模した反復ゲームで、参加者が安全開発と危険開発を選ぶ行動を調べた。危険開発は進捗と即時利得を高めるが、私的リスクを累積する。競争構造を固定し、最大リスクだけ10%、60%、90%へ変えた事前登録実験で、リスク水準差と個人のリスク選好に関する事前登録仮説はいずれも支持されなかった。</p>
<p>代わりに探索分析では、相手が危険を選んだ直後、また自分が遅れている時に危険選択が増え、先行時には減った。初回選択も後の行動を予測した。Always Safeなど四戦略の縮約進化モデルが処置効果を再現し、条件付き危険行動が競争で選好され得ると示す。ただし探索結果を確認的結論へ格上げできず、理想化ゲームから実企業の因果へ一般化もできない。政策含意は個人啓発だけでなく競争圧力と協力制度を見る仮説として扱うべきである。</p>
<h2>論文7: 未知のマルチモーダルグラフへ転移するCHARM</h2>
<p><strong>出典:</strong> CHARM: A Multimodal Graph Foundation Model with Hierarchical Context Modeling for Zero-Shot Transfer. <a href="https://arxiv.org/abs/2607.26023">arXiv:2607.26023</a> (2026).</p>
<p>Yang氏らは、テキストや画像を持つノードからなるグラフを、対象領域で追加学習せず転移する問題を扱う。従来GNN型基盤モデルは下流適応を要し、LLM型は単一モダリティや単一領域に寄りやすい。CHARMは孤立した生ノードの代わりに、複数階層のグラフ文脈を構成し、領域固有パターンを共有可能な高次概念へ写す。</p>
<p>モダリティ認識グラフ文脈エンコーダが画像・文・構造を統合し、グラフトークンとしてLLMへ渡す。要旨は複数のゼロショット・マルチモーダルグラフ課題で一貫した改善を報告するが、データセット、絶対値、比較法、計算量は示していない。このため「未知領域へ一般化した」という主張の強さは、領域分割と訓練重複の監査に依存する。階層文脈のアブレーションとコード公開状況が再現性の核心になる。</p>
<h2>論文8: エピソード記憶をパラメータへ統合するUniMem</h2>
<p><strong>出典:</strong> UniMem: Complementary Episodic-to-Parametric Memory for Boundary-Agnostic Task Streams. <a href="https://arxiv.org/abs/2607.26017">arXiv:2607.26017</a> (2026).</p>
<p>Xia氏らは、LLMエージェントが境界の明示されない連続タスクで経験を蓄える際の安定性と可塑性の両立を狙う。外部検索記憶は新情報を速く取り込むが検索遅延があり、反復手順を内部化しにくい。パラメータ記憶は実行が安定する一方、通常はタスク境界と固定容量を仮定する。UniMemは学習可能なルーティングトークンを記憶制御器にする。</p>
<p>新規・希少タスクはエピソードバッファへ残し、繰り返され信頼できるパターンは拡張可能なパラメータブロックへ徐々に統合する。タスク同定と実行を分離し、ラベルなしで必要時だけ容量を増やす。長期ストリーミング系列で三つのバックボーンにわたり平均4.0完全一致ポイント改善した。ただし記憶汚染、忘却、容量増加率、検索時間の絶対値は要旨にない。「無制御な増加なし」を検証するには長期曲線とルーティング判断の監査が必要である。</p>
<h2>論文9: カメラ視点だけで3500万キロ学ぶ自動運転Pictura</h2>
<p><strong>出典:</strong> Pictura: Perspective-View Self-Play at Scale for Driving. <a href="https://arxiv.org/abs/2607.26005">arXiv:2607.26005</a> (2026).</p>
<p>Yin氏らは、自動運転の自己対戦が正確な位置や速度、遮蔽車両まで見える特権ベクトル観測に依存する表現ギャップを扱う。特権教師をカメラ学生へ蒸留すると、学生自身には見えない根拠の判断まで模倣させる問題がある。Picturaは各エージェントの一人称画像を毎ステップ描画するGPUシミュレータで、単一H100上で毎秒最大50万エージェントステップ、200万画像を生成する。</p>
<p>著者らは通常のPPOでAlbertiを500億ステップ、約3500万キロ相当学習し、特権観測なしの大規模視点画像自己対戦を実現した。特権ベクトル版に近い運転性能を示し、Picturaで再描画したWaymo Open Motion Dataset配置へのゼロショット転移では特権エージェントを上回った。実世界カメラへの直接転移ではなく再描画環境であり、センサ雑音や規制適合は未評価。プロジェクト公開は有用だが、50Bステップの計算資源が再現障壁になる。</p>
<h2>論文10: 複数デノイズ段階を一度に予測する並列蒸留</h2>
<p><strong>出典:</strong> Parallel Decoding Distillation for Fast Image and Video Generation. <a href="https://arxiv.org/abs/2607.26004">arXiv:2607.26004</a> (2026).</p>
<p>Shaul氏らは、動画の拡散・フローモデルを少数ステップ化する際、変分スコア蒸留や敵対的損失が不安定で、モード崩壊により多様性と動きが失われる問題を扱う。Parallel Decoding Distillationは軌跡ベースの簡潔な蒸留で、一回のネットワーク評価から複数のデノイズ段階を並列予測する。平均速度表現を学び、ヤコビアン・ベクトル積や有限差分で速度微分を回帰しない。</p>
<p>任意の事前学習モデルへ適用でき、推論時の関数評価回数も変えられる。LTX-2.3のテキスト動画・音声、Wan 14Bのテキスト動画、Qwen-Imageで4〜8回評価の最先端性能を報告し、動画多様性も大幅に改善した。ただし要旨には品質指標、速度倍率、比較条件、学習計算量がないため「最先端」と「大幅」を独立に検証できない。多様性の定義、同一計算予算、失敗例、コードと重みの公開が実用判断に必要である。</p>
<h2>まとめ</h2>
<p>10本に共通するのは、資源を一律に増やすのでなく、誤推論、不確実なトークン、新規タスク、実行中の感覚といった必要な場所へ選択的に配る設計である。一方、最大改善値、要旨だけの「一貫した改善」、再描画環境での転移を、そのまま一般性能や実環境安全性へ広げてはならない。絶対値、分散、総計算費、安全側の失敗、コードと評価データの公開を次の確認項目とする。</p>
<hr />
<h2>参考ソース</h2>
<ul>
<li>論文1: Pass the Baton: Trajectory-Relayed On-Policy Distillation. <a href="https://arxiv.org/abs/2607.26057">arXiv:2607.26057</a> (2026).</li>
<li>論文2: πR²: Reactive Real-time Flow Policies. <a href="https://arxiv.org/abs/2607.26055">arXiv:2607.26055</a> (2026).</li>
<li>論文3: Spend Experts Where You Are Unsure: Confidence-Adaptive Routing for Mixture-of-Experts LoRA. <a href="https://arxiv.org/abs/2607.26052">arXiv:2607.26052</a> (2026).</li>
<li>論文4: VetClaw: An Edge-Cloud Multimodal Agentic System for Veterinary Disease Screening. <a href="https://arxiv.org/abs/2607.26042">arXiv:2607.26042</a> (2026).</li>
<li>論文5: Desktop-Delta Bench: Do Computer-Use Models Understand Desktop GUI Transitions? <a href="https://arxiv.org/abs/2607.26041">arXiv:2607.26041</a> (2026).</li>
<li>論文6: Falling Behind Drives Unsafe Development in an Idealised AI Race Experiment. <a href="https://arxiv.org/abs/2607.26034">arXiv:2607.26034</a> (2026).</li>
<li>論文7: CHARM: A Multimodal Graph Foundation Model with Hierarchical Context Modeling for Zero-Shot Transfer. <a href="https://arxiv.org/abs/2607.26023">arXiv:2607.26023</a> (2026).</li>
<li>論文8: UniMem: Complementary Episodic-to-Parametric Memory for Boundary-Agnostic Task Streams. <a href="https://arxiv.org/abs/2607.26017">arXiv:2607.26017</a> (2026).</li>
<li>論文9: Pictura: Perspective-View Self-Play at Scale for Driving. <a href="https://arxiv.org/abs/2607.26005">arXiv:2607.26005</a> (2026).</li>
<li>論文10: Parallel Decoding Distillation for Fast Image and Video Generation. <a href="https://arxiv.org/abs/2607.26004">arXiv:2607.26004</a> (2026).</li>
</ul>

</details>

---

[← 2026-07-30 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
