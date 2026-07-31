---
title: "ハーネスごと鍛えるAIエージェント研究ほか生成AI論文10本解説【2026/07/27】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# ハーネスごと鍛えるAIエージェント研究ほか生成AI論文10本解説【2026/07/27】

**2026-07-27 / arxiv AI論文解説**

<audio controls src="https://archive.org/download/news-pickup-2026-07-27-arxiv-ai/arxiv_ai_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-07-27-arxiv-ai)

---

## 概要

今日は、Claude CodeやCodexのような推論ハーネスそのものを強化学習で鍛える基盤、自然言語だけで物理的にもっともらしい4Dワールドを作るマルチエージェント手法、百万トークン級の長文脈で投機的デコーディングを高速化する仕組みから、LLMがなぜ「言い直し」を多用してしまうのかという言語スタイルの分析、心理言語学の定説「サプライザル理論」への根本的批判まで、生成AI論文10本をずんだもんと四国めたんが解説します。

▼ 今日のトピック
・ハーネス常駐型AIエージェントをあらゆる環境で訓練する『OpenForgeRL』
・生成シミュレーションで4D物理世界を作る『GS-Agent』
・LLMが臨床症例をゲーム化する医学教育フレームワーク『MedGame』
・クラウドを使わないエージェント型コーディング：縦断データ整形をオープンウェイトLLMで評価する
・百万トークン文脈での投機的デコーディングを高速化する『Windowed-MTP』
・ランダム化設計でKVキャッシュ破棄の誤差を証明可能にする
・思考トークン予算の飽和と、推論が収束しない兆候の機構的早期検出
・What・Where・Howで解剖する、コード生成モデルの内部表現
・人工的なエパノルソシス：LLMはなぜ「言い直し」を多用するのか
・サプライザル理論はトートロジーである、合理的根拠なしには

▼ 参考論文（arXiv）
https://arxiv.org/abs/2607.21557 — OpenForgeRL: Train Harness-native Agents in Any Environment
https://arxiv.org/abs/2607.21522 — GS-Agent: Creating 4D Physical Worlds With Generative Simulation
https://arxiv.org/abs/2607.21570 — MedGame: Storytelling Gamification Empowered by Large Language Models for Medical Education
https://arxiv.org/abs/2607.21482 — Agentic coding without the cloud: evaluating open-weight large language models on longitudinal data preparation tasks
https://arxiv.org/abs/2607.21535 — Windowed-MTP: Removing the Full-Context Draft-KV Tax at Million-Token Context
https://arxiv.org/abs/2607.21475 — Error Certificates for KV-Cache Eviction via Randomized Design
https://arxiv.org/abs/2607.21433 — Token Budget Saturation and Mechanistic Early Detection of Reasoning Non-Convergence in Chain-of-Thought Models
https://arxiv.org/abs/2607.21491 — What, Where, and How: Disentangling the Roles of Task, Language, and Model in Code Model Representations
https://arxiv.org/abs/2607.21498 — Artificial Epanorthosis: Why large language models overuse a classical rhetorical figure, and how to mitigate it
https://arxiv.org/abs/2607.21574 — Surprisal Theory is Tautological (without Rational Grounding)

#生成AI #ChatGPT #Claude #LLM #AI #人工知能 #arxiv #論文解説 #ゆっくり解説 #ずんだもん #OpenAI #Anthropic #機械学習 #ディープラーニング

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>arXiv生成AIニュース（2026年7月27日）</h1>
<p><strong>キーワード:</strong> ハーネス型エージェント訓練 / 4Dワールド生成 / 投機的デコーディング / KVキャッシュ管理 / 医療教育AI / 言語モデルの解釈可能性</p>
<h2>オープニング：2026年7月27日 — arXiv生成AI論文解説</h2>
<p>今回は、Claude CodeやCodexのような推論ハーネスそのものを強化学習で鍛える研究から、自然言語だけで物理的にもっともらしい4次元世界を作るマルチエージェント手法、百万トークン級の長文脈で投機的デコーディングを高速化する仕組み、そしてLLMがなぜ「言い直し」を多用してしまうのかという言語スタイルの分析まで、生成AI分野の最新10本を取り上げる。</p>
<h2>論文1: ハーネス常駐型AIエージェントをあらゆる環境で訓練する『OpenForgeRL』</h2>
<p><strong>出典:</strong> OpenForgeRL: Train Harness-native Agents in Any Environment. <a href="https://arxiv.org/abs/2607.21557">arXiv:2607.21557</a> (2026).</p>
<p>Columbia University、Dartmouth College、Microsoft Researchの研究チームは、Claude CodeやCodex、OpenClawのような「推論ハーネス」――マルチターンの推論・ツール呼び出し・外部システム連携を取り仕切るオーケストレーション層――を、既存の公開強化学習基盤で端から端まで訓練できない問題を指摘する。現在のオープンなRLスタック（veRLなど）は、ネストしたツール呼び出しやサブエージェント、長時間の文脈といったハーネスのステートフルで多プロセスな挙動をそのまま表現できず、研究の多くは訓練用に簡略化した偽ハーネスを再実装せざるを得ない。その結果、訓練時のハーネスと実際にデプロイされる本物のハーネスとの間に「訓練と運用のズレ」が生じてきた。</p>
<p>提案されたOpenForgeRLは、ハーネスのモデル呼び出しを仲介する軽量プロキシで通信内容を記録して標準的なRLコードベースの訓練データに変換し、Kubernetes上のコンテナでロールアウトごとに独立した環境を走らせることで、任意のハーネスを任意の環境で大規模に訓練できるようにする。ツール利用型エージェントとマルチモーダルなGUI操作エージェントの両方で検証したところ、数百から数千タスクという小規模なデータでも、OpenForge-ClawはClawEvalでpass^3が31.7、pass@3が55.9、QwenClawBenchで33.7を、OpenForge-GUIはOSWorld-Verifiedで37.7、Online-Mind2Webで63.0、WebVoyagerで72.3を達成し、同規模のオープンベースラインをほぼ全ての指標で上回った。一方で、RLはツール網羅性や自己検証などエージェントの信頼性を底上げする反面、エラーからの回復のような能力は依然として弱く、ハーネスの選び方自体が学習の難度を大きく左右することも報告されている。</p>
<h2>論文2: 生成シミュレーションで4D物理世界を作る『GS-Agent』</h2>
<p><strong>出典:</strong> GS-Agent: Creating 4D Physical Worlds With Generative Simulation. <a href="https://arxiv.org/abs/2607.21522">arXiv:2607.21522</a> (2026).</p>
<p>University of Massachusetts AmherstとGenesis AIの研究チームは、自然言語の説明から動的で物理的に妥当な4次元（4D）世界を作る作業が、従来は素材調整・配置・モーション設計・カメラや照明の演出まで多大な人手を要してきたと整理する。生成基盤モデルによる学習だけに頼る近年の手法は、物理的な妥当性と制御性を両立させるのが依然として難しいと著者らは指摘し、人間が世界を作る手順そのものをエージェントに模倣させる方向を選んだ。</p>
<p>提案手法GS-Agentは、3D素材の選定・材質調整・配置・モーション制御を担う「エンティティ管理」と、カメラ・照明を扱う「レンダリング設定」に作業を分解するマルチエージェント枠組みである。専門の異なる複数のエージェントが物理エンジンをコードで操作しながらマルチモーダルなフィードバックを参照し、与えられた説明に沿う4D世界を協調的に構築する。実験では、液体・変形物体・剛体が絡み合う物理的な相互作用と、映画的なカメラワーク・照明制御を両立した4D世界を自然言語から生成できることが示された。定量的な指標は限定的で評価は主に定性的な事例に基づいており、著者らはクリエイティブなコンテンツ制作やフィジカルAIの基盤としての今後の発展を見込んでいる。</p>
<h2>論文3: LLMが臨床症例をゲーム化する医学教育フレームワーク『MedGame』</h2>
<p><strong>出典:</strong> MedGame: Storytelling Gamification Empowered by Large Language Models for Medical Education. <a href="https://arxiv.org/abs/2607.21570">arXiv:2607.21570</a> (2026).</p>
<p>CUHK（香港中文大学）、Southern Medical University（南方医科大学）、Peking University（北京大学）、Tencentの共同チームは、LLMを用いた医学教育システムの多くが一問一答や単発フィードバックにとどまり、症例全体を決定中心の学習軌跡として組み立てられていない点に着目した。臨床症例の要約は豊富な診断・治療知識を含む一方で静的なテキストとして消費され、部分的な情報から次に何を調べるか判断し証拠が増えるたびに理解を更新するという、実際の臨床推論のダイナミズムを再現できていなかった。</p>
<p>提案されたMedGameは、臨床ナラティブを状態と分岐点を持つストーリーとして設計する「Medical Narrative Designer」と、それを依存関係を保ったマルチモーダルな実行計画へ変換する「Story Director」からなる二段構成のフレームワークで、専用のインタラクティブなプラットフォーム上に症例をゲームとして提示する。5,000症例規模のベンチマーク「MedGame Bench」で評価したところ、タスク特化のファインチューニングによってオープンソースLLMの性能が大きく向上し商用モデルとの差が縮まったほか、学習者を対象とした予備調査でもテキストのみの教材よりゲーム版の方が有用で興味を引くと評価された。ただし著者ら自身が「Work in progress」と位置づけており、規模の大きい正式な学習効果検証は今後の課題として残る。</p>
<h2>論文4: クラウドを使わないエージェント型コーディング：縦断データ整形をオープンウェイトLLMで評価する</h2>
<p><strong>出典:</strong> Agentic coding without the cloud: evaluating open-weight large language models on longitudinal data preparation tasks. <a href="https://arxiv.org/abs/2607.21482">arXiv:2607.21482</a> (2026).</p>
<p>University College London（UCL）とUniversity of Bristolの研究チームは、コーディングエージェントの多くがデータをクラウド上の商用モデルへ送信する前提で使われている一方、個人情報保護のガバナンス要件が厳しい縦断的な人口コホート研究では外部へのデータ送信自体が制約になる、という現場の課題を出発点にした。そこで、データが手元の環境から一歩も出ないローカルデプロイ可能なオープンウェイトLLMで、同分野で最も持続的なボトルネックの一つであるデータ前処理を任せられるかを検証する評価基盤を構築した。</p>
<p>評価基盤は、英国の出生コホート研究6波分のデータを整形する正解付きクリーニングスクリプト、カテゴリ統合や複数波のマージといったタスク定義、LLMが生成したR言語コードと出力データを自動採点する仕組みからなり、20種のデータ前処理タスク・102変数の作成についてコンシューマー向けハードウェアで動く複数規模のモデルを比較した。結果、31から35ビリオンパラメータ級の最新オープンウェイトモデルはベンチマークをほぼ飽和させ、平均タスク達成率は87.9パーセントに達した。著者らはこれをガバナンス制約の強い研究現場でもAI支援のデータ前処理が実用段階に近づいている証拠と位置づけつつ、評価対象がR言語の特定タスク群に限られる点には注意が必要だとしている。</p>
<h2>論文5: 百万トークン文脈での投機的デコーディングを高速化する『Windowed-MTP』</h2>
<p><strong>出典:</strong> Windowed-MTP: Removing the Full-Context Draft-KV Tax at Million-Token Context. <a href="https://arxiv.org/abs/2607.21535">arXiv:2607.21535</a> (2026).</p>
<p>投機的デコーディングは、安価な「ドラフト」モデルが候補トークンを提案し、本体の「ターゲット」モデルがそれをまとめて検証することで生成を高速化する手法で、近年のフロンティアモデルは複数トークン予測（MTP）によるドラフトヘッドを内蔵し、ドラフトのコストは無視できるという前提で設計されてきた。NVIDIAの研究者は、文脈長が百万トークン規模になるとこの前提が崩れると指摘する。MTPドラフトヘッドは毎ステップKVキャッシュ全体に全アテンションを行うため、その読み出しコストが文脈長に比例して増大し、投機が最も効くはずの長文脈でむしろドラフト側がボトルネックになる。ドラフト長が深いほど悪化し、ハイブリッド／線形アテンション系のターゲットではさらに問題が顕在化するという。</p>
<p>提案手法Windowed-MTPは、ターゲット側の検証用アテンションはそのまま残し、ドラフト側のアテンションだけにStreamingLLM流のスライディングウィンドウとアテンションシンクを適用する。ターゲットが最終的に全トークンを検証する構造は変えないため、訓練不要かつ理論上ロスレスに、提案されるトークン候補だけが変わる。Qwen系のGDN-MoEやMamba2ハイブリッド構成など3系統のアーキテクチャで百万トークン文脈を単一GPU上で検証したところ、KVエントリを百万トークン時点で約99パーセント削減しつつ、1ステップあたりのデコードコストを既存のネイティブMTPドラフト比で28から44パーセント削減できた。ターゲットの検証出力分布は変えないため精度劣化のない設計だが、効果は文脈長が伸びるほど大きくなる。</p>
<h2>論文6: ランダム化設計でKVキャッシュ破棄の誤差を証明可能にする</h2>
<p><strong>出典:</strong> Error Certificates for KV-Cache Eviction via Randomized Design. <a href="https://arxiv.org/abs/2607.21475">arXiv:2607.21475</a> (2026).</p>
<p>Technical University of Munichの研究者は、KVキャッシュの決定論的な破棄、すなわち重要度スコア上位k件だけを残して残りを消す方式が「何を破棄したか」を原理的に把握できない設計であることを示した。破棄された値を細工すれば、サービング側に残る情報を一切変えずにアテンション出力の真の誤差を任意に大きくできてしまうため、サービング時にその誤差を推定しようとしても一貫した推定量は存在しないと数学的に証明している。</p>
<p>この問題に対し、破棄をランダム化し、既知の採択確率でポアソン抽出した「テール」部分にロジットのオフセットを一回加えてハーイェック補正をソフトマックス内で行う設計を提案する。これにより、残ったトークン集合に対するサーベイサンプリングの分散推定量が、そのままステップごとの誤差証明書として機能し、実測で0.97というカバレッジ率を精度低下なしに達成した。実運用ワークロードでは事前登録した7つの仮説のうち3つが外れ、質問に応じた25から50パーセント予算での破棄はほぼ無償である一方、出力のログ確率の方が誤差証明書より障害予測に優れ、証明書に基づく予算のエスカレーションも効果がなかった。生き残ったのは「帰属」の力で、キャッシュ由来の失敗と本質的な失敗を区別する精度は0.73から0.75（AUC）で出力信頼度の0.47から0.54を上回り、再計算のスケジューリングにも活用できることが示された。</p>
<p>核心アイデアを簡略化すると、次の重み付け推定量になる。</p>
<p>$$ \hat{S} = \sum_{i \in \text{採択集合}} \frac{v_i}{\pi_i} $$</p>
<p>ここで $\pi_i$ はトークン $i$ が生き残る既知の包含確率、$v_i$ はその値。ホーヴィッツ・トンプソン型の重み付け（ハーイェック補正）により、ランダムに落とした分の期待値のズレを打ち消す。</p>
<h2>論文7: 思考トークン予算の飽和と、推論が収束しない兆候の機構的早期検出</h2>
<p><strong>出典:</strong> Token Budget Saturation and Mechanistic Early Detection of Reasoning Non-Convergence in Chain-of-Thought Models. <a href="https://arxiv.org/abs/2607.21433">arXiv:2607.21433</a> (2026).</p>
<p>University of MarylandとSAP Labsの研究チームは、DeepSeek-R1-Distill-Qwen-7Bのような思考の連鎖（CoT）を行う推論モデルが、割り当てたトークン予算内で答えにたどり着く「収束」と、予算を使い切っても結論に至らない「非収束」の二極化したパターンを示すことに着目した。GSM8K・MATH-500・AIME 1983-2024という難度の異なる3つの数学ベンチマークで、Muennighoffらの予算強制手法を用いてトークン予算を256から4,096まで振りながら精度を測定したところ、GSM8KとMATH-500は256トークンという早い段階で無制限時の95パーセントの精度に達する一方、AIMEでは56.5パーセントが平均96.5パーセントの精度で自然に収束するのに対し、43.5パーセントは1万トークンの上限に達しても収束せず精度はわずか11.5パーセントにとどまった。</p>
<p>このバイモーダルな結果は問題の難易度だけではあまり説明できず（決定係数はおよそ0.186）、著者らは収束するかどうかが生成途中の内部表現に現れていないかを調べた。全28層と複数のトークン位置を走査した結果、トークン150付近では層20の活性化から線形プローブを訓練するとAUC 0.608（標準偏差0.080）で偶然を上回る予測ができ、トークンエントロピーや繰り返し統計などの振る舞いベースの指標より一貫して高い性能を示した。学習データに含まれないAIME2025の問題でも収束と正答率の関係が保たれており（収束時100パーセント、非収束時0パーセント）、単純な記憶ではないことも確認された。ただしサンプル数200では個々のチェックポイントでの統計的有意性の確認力が不足しており、著者らはこれを早期終了による推論コスト削減の足がかりと位置づけつつ、統計的な確証には追試が必要だとしている。</p>
<h2>論文8: What・Where・Howで解剖する、コード生成モデルの内部表現</h2>
<p><strong>出典:</strong> What, Where, and How: Disentangling the Roles of Task, Language, and Model in Code Model Representations. <a href="https://arxiv.org/abs/2607.21491">arXiv:2607.21491</a> (2026).</p>
<p>University College Londonの研究者は、「別々に訓練された言語モデルは、同じ概念を同じように表現するのか」という解釈可能性研究の根本的な問いに、コード生成モデルを題材に取り組んだ。PythonとRustという2つのプログラミング言語と、Qwen2.5-Coder-7BとDeepSeek-Coder-V1-6.7Bという2つのモデルを掛け合わせた2×2の実験設計で、文法的な概念（Pythonで58種、Rustで57種）すべてを同一の手法で測定し、タスク・言語・モデルそれぞれの寄与を分離できる最小構成を作った。</p>
<p>結果は3つに分かれた。「何が」専用回路を持つかはタスクによって決まり、2つのモデルはどの概念に回路を割り当てるかでよく一致した（スピアマン相関はPythonで0.638、Rustで0.673、いずれもp値は10のマイナス7乗未満）。しかし「どこに」その回路があるかはモデル依存で、Qwenは層17-19という遅い段階、DeepSeekは層6-7という早い段階で概念を処理しており、この12-13層の差は両言語で共通していた。「どのように」層をまたいで回路が成長するかもモデル依存で、Qwenは概念処理の初期に急峻な立ち上がりを見せるがDeepSeekには見られない。さらにRustの構文はPythonの2-3倍多くの専用回路を持ち、DeepSeekはQwenよりニューロンの言語間共有が1.94倍多いなど、事前には予測できない非対称性も見つかった。著者らはこの結果を2×2の設計に限定されるものと位置づけ、3つ目のモデルへの一般化は今後の検証課題としている。</p>
<h2>論文9: 人工的なエパノルソシス：LLMはなぜ「言い直し」を多用するのか</h2>
<p><strong>出典:</strong> Artificial Epanorthosis: Why large language models overuse a classical rhetorical figure, and how to mitigate it. <a href="https://arxiv.org/abs/2607.21498">arXiv:2607.21498</a> (2026).</p>
<p>所属機関の記載のない単著の論考として発表された本論文は、キケロやクインティリアヌスが二千年前に分類した修辞技法「エパノルソシス」――「これは講座ではありません。変革の旅なのです」のような自己訂正的な言い直し――が、大規模言語モデルの文章に体系的に現れることを指摘する。著者は、この多用が単なる生成方式（左から右への逐次生成）の副産物ではなく、宣伝文的な文章が多い訓練データと、自信ありげで力強い言い回しに報酬を与える選好調整（RLHF）によって身についた「訓練された傾向」だと論じる。</p>
<p>検証のため、あるジャンルにおける人間の使用率を基準にエパノルソシスの密度を測る「Epanorthosis Index」を提案し、ある指示追従モデルファミリーの3つのサイズで測定したところ、演説調の文章では人間の約2倍（イタリア語ではほぼ3倍、大きいモデルほど顕著）過剰使用する一方、くだけた質疑応答形式の文章では逆に少なすぎるという、ジャンルによって逆方向にずれる較正の乱れが見つかった。論文はさらに、軽量なLoRAアダプタを中心とした緩和策を整理し、イタリア語では一行の指示だけでこの修辞の使用を半分から4分の3近くまで減らせること、教師ありファインチューニングのアダプタを使えばほぼ完全に取り除けること、さらにスケーリング係数で人間並みの水準に調整し戻せることを示した。著者は目標をこの技法の根絶ではなく「人間のジャンル別使用率への較正」に置くべきだと結び、人間がAIのような話し方をし始めることこそが本当のリスクだと警鐘を鳴らしている。</p>
<h2>論文10: サプライザル理論はトートロジーである、合理的根拠なしには</h2>
<p><strong>出典:</strong> Surprisal Theory is Tautological (without Rational Grounding). <a href="https://arxiv.org/abs/2607.21574">arXiv:2607.21574</a> (2026).</p>
<p>ETH Zürichのライアン・コッターレル（Ryan Cotterell）氏は、心理言語学で20年近く支持されてきた「サプライザル理論」――文脈中の言語単位を処理する人間の難しさは、何らかの言語モデルによるサプライザル（驚き度、生起確率の対数を反転した量）のアフィン関数で表せるという仮説――に、根本的な批判を投げかける。</p>
<p>論文の主張は、追加の制約なしにはこの理論はトートロジー（自明な同語反復）に過ぎないというものだ。任意の非負の難易度指標に対して、緩やかな技術的条件のもとでそのサプライザルがアフィン関数になるような言語モデルが必ず存在してしまうため、言語モデルに何の制約も課さなければどんな難易度パターンでも「説明できてしまい」、理論として反証可能な予測を一切生まない。この自明さは、訓練コーパスを生成した分布こそが妥当な言語モデルだという心理言語学の暗黙の前提によって20年間見えにくくなっていたが、コーパスへの適合度を上げるほど人間の処理困難度の予測が悪化するという近年の実証研究がこの前提を崩したと指摘する。著者は、トートロジーを破るには経験的なコーパス適合とは独立に、記憶制約や処理目標など理解者側の合理的なモデルから言語モデルを導出する「合理主義的な介入」が必要だと結論づけている。</p>
<p>理論の核心はこの定義式に集約される。</p>
<p>$$ \text{Difficulty}(w_t \mid w_{<t}) = \alpha \cdot \big(-\log p_M(w_t \mid w_{<t})\big) + \beta $$</p>
<p>$p_M$ に何の制約も置かない限り、右辺は左辺のどんな難易度パターンにも合わせられてしまう、というのが本論文の批判の核心である。</p>
<h2>今日のまとめ</h2>
<p>ハーネスごと強化学習するエージェント基盤から、自然言語だけで作る4D物理世界、百万トークン文脈での投機的デコーディング高速化、そしてLLMが「言い直し」を多用する理由やサプライザル理論への根本的批判まで、生成AI研究の広がりを示す10本だった。</p>
<h2>参考ソース</h2>
<ul>
<li>論文1: OpenForgeRL: Train Harness-native Agents in Any Environment — <a href="https://arxiv.org/abs/2607.21557">arXiv:2607.21557</a></li>
<li>論文2: GS-Agent: Creating 4D Physical Worlds With Generative Simulation — <a href="https://arxiv.org/abs/2607.21522">arXiv:2607.21522</a></li>
<li>論文3: MedGame: Storytelling Gamification Empowered by Large Language Models for Medical Education — <a href="https://arxiv.org/abs/2607.21570">arXiv:2607.21570</a></li>
<li>論文4: Agentic coding without the cloud: evaluating open-weight large language models on longitudinal data preparation tasks — <a href="https://arxiv.org/abs/2607.21482">arXiv:2607.21482</a></li>
<li>論文5: Windowed-MTP: Removing the Full-Context Draft-KV Tax at Million-Token Context — <a href="https://arxiv.org/abs/2607.21535">arXiv:2607.21535</a></li>
<li>論文6: Error Certificates for KV-Cache Eviction via Randomized Design — <a href="https://arxiv.org/abs/2607.21475">arXiv:2607.21475</a></li>
<li>論文7: Token Budget Saturation and Mechanistic Early Detection of Reasoning Non-Convergence in Chain-of-Thought Models — <a href="https://arxiv.org/abs/2607.21433">arXiv:2607.21433</a></li>
<li>論文8: What, Where, and How: Disentangling the Roles of Task, Language, and Model in Code Model Representations — <a href="https://arxiv.org/abs/2607.21491">arXiv:2607.21491</a></li>
<li>論文9: Artificial Epanorthosis: Why large language models overuse a classical rhetorical figure, and how to mitigate it — <a href="https://arxiv.org/abs/2607.21498">arXiv:2607.21498</a></li>
<li>論文10: Surprisal Theory is Tautological (without Rational Grounding) — <a href="https://arxiv.org/abs/2607.21574">arXiv:2607.21574</a></li>
</ul>

</details>

---

[← 2026-07-27 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
