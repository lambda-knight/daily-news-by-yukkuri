---
title: "ポスター作成AIが自己改善？生成AIのエージェント設計10論文【2026/08/17】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# ポスター作成AIが自己改善？生成AIのエージェント設計10論文【2026/08/17】

**2026-08-17 / arxiv AI論文解説**

<audio controls src="https://archive.org/download/news-pickup-2026-08-17-arxiv-ai/arxiv_ai_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-17-arxiv-ai)

---

## 概要

2026年8月17日の生成AI最新論文10本を解説。論文からポスターを作る作業手順を実行結果から自己改善させるAutoDesign（平均スコア54.99→67.39）、生データを直接知覚する全モーダルAI科学者OmniScientist、小学校教材相当に知識を絞ったLittleLearnerを取り上げます。

中盤はSAE特徴をモデル自身に言語化させるSAEVerbalizer、許諾データのみで学習し性能で競り合う1BモデルDFM Mimir v1、学習データの影響力が序盤と終盤で入れ替わる分析、397Bの科学エージェント基盤モデルIntern-S2-Previewを解説。後半は「知らない」と言えないLLMの知識境界研究、事前学習の最初から人格を組み込むSynthetic Persona Pretraining、重みを変えずに行列積を間引くReduced Matrix Multiplicationを扱います。

▼ 今日の論文ラインナップ
・ポスター作成ハーネスを自己改善させるAutoDesign（arxiv:2608.13560）
・生データを直接読む全モーダルAI科学者OmniScientist（arxiv:2608.13558）
・知識を小学校レベルに制限したLittleLearner（arxiv:2608.13545）
・疎自己符号化器の特徴を言語化するSAEVerbalizer（arxiv:2608.13538）
・許諾データのみで作る1BのフロンティアモデルDFM Mimir v1（arxiv:2608.13517）
・事前学習を通じたデータ影響力の時間変化を測る研究（arxiv:2608.13515）
・397Bの科学エージェント基盤モデルIntern-S2-Preview（arxiv:2608.13505）
・知らないことを認められないLLM——グライスの後退を探る（arxiv:2608.13484）
・事前学習の最初のトークンから人格を作るSynthetic Persona Pretraining（arxiv:2608.13482）
・入力に応じて行列積を間引くReduced Matrix Multiplication（arxiv:2608.13426）

▼ 参考論文（arXiv）
https://arxiv.org/abs/2608.13560 — ポスター作成ハーネスを自己改善させるAutoDesign
https://arxiv.org/abs/2608.13558 — 生データを直接読む全モーダルAI科学者OmniScientist
https://arxiv.org/abs/2608.13545 — 知識を小学校レベルに制限したLittleLearner
https://arxiv.org/abs/2608.13538 — 疎自己符号化器の特徴を言語化するSAEVerbalizer
https://arxiv.org/abs/2608.13517 — 許諾データのみで作る1BのフロンティアモデルDFM Mimir v1
https://arxiv.org/abs/2608.13515 — 事前学習を通じたデータ影響力の時間変化を測る研究
https://arxiv.org/abs/2608.13505 — 397Bの科学エージェント基盤モデルIntern-S2-Preview
https://arxiv.org/abs/2608.13484 — 知らないことを認められないLLM——グライスの後退を探る
https://arxiv.org/abs/2608.13482 — 事前学習の最初のトークンから人格を作るSynthetic Persona Pretraining
https://arxiv.org/abs/2608.13426 — 入力に応じて行列積を間引くReduced Matrix Multiplication

#生成AI #ChatGPT #Claude #LLM #AI #人工知能 #arxiv #論文解説 #ゆっくり解説 #ずんだもん #AIエージェント #機械学習 #ディープラーニング

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>arXiv生成AIニュース（2026年8月17日）</h1>
<p><strong>キーワード:</strong> エージェント設計の自己改善 / 全モーダルAI科学者 / 発達段階制御プレトレーニング / 疎自己符号化器の言語化 / 許諾データのみの軽量モデル / 事前学習からの人格整合</p>
<h2>オープニング：2026年8月17日 — arxiv生成AI論文解説</h2>
<p>今日は、論文をポスターへ自動変換するハーネスが自己改善していく研究から、生データを直接扱う全モーダルAI科学者、小学生レベルに知識を制限した実験用モデル、内部特徴を言語化するインタープリタビリティ手法、そして事前学習の段階から人格を作り込むアラインメント手法まで、生成AIのエージェント設計・科学応用・学習ダイナミクス・安全性にまたがる10本を扱う。</p>
<h2>論文1: ポスター作成ハーネスを自己改善させるAutoDesign</h2>
<p>論文からポスターを作るような、多様なメディアを条件付きで生成する作業は、モデルと作業手順（ハーネス）が一体となった長時間のエージェント作業として捉えられる。理想的にはハーネス自体が人間の設計方針に沿いつつ、実行結果から再利用可能な経験を蓄積して自己改善していくべきだが、既存の枠組みは静的なままでこの能力を欠いている。本研究は、メタハーネス最適化器がコードエージェントを導き、実行結果のフィードバックをもとにハーネスを再帰的に改善していくAutoDesignを提案する。評価には、5分野100本の論文を対象とするPosterBenchメインと、統制評価用の10本サブセットPosterBench-miniを新たに構築している。</p>
<p>PosterBenchメイントラックでAutoDesignは78.32点を記録し、比較対象とした商用の非公開システムClaude Designを7.45点上回った。7種類のコードエージェント・モデルの組み合わせで検証したところ、学習済みのDesignHarnessを組み込むことで平均スコアが54.99点から67.39点へ一貫して向上した（+12.4%）。完全自律の長時間ループでは、40分以内・3ドル未満で253回のツール呼び出しと11回の編集ターンを実行し、人間評価で学会ポスター相当の品質に達している。システムを伏せた人間評価でも、AutoDesignは評価対象の中で最も高い支持を得た。</p>
<p><strong>出典:</strong> AutoDesign: Meta-Harness Optimization for Long-Horizon Agentic Design. <a href="https://arxiv.org/abs/2608.13560">arXiv:2608.13560</a> (2026).</p>
<h2>論文2: 生データを直接読む全モーダルAI科学者OmniScientist</h2>
<p>近年の基盤モデルは、仮説生成からコード実行、論文執筆までを含む研究ワークフローの自動化を進めているが、ワークフローを網羅しているだけでは、科学的発見を支える証拠すべてに触れられるわけではない。既存システムの多くはテキスト・コード・ラベル・事前計算済みの要約を扱うにとどまり、空間・時間・チャネル間・手続き的な関係といった、科学的判断を左右する情報がエージェントから見えない。本研究は、知覚レイヤーと、着想・実験・執筆を担う3つの自律エージェントが決定的なパイプライン内で動作するOmniScientistを提案し、異種の生データから直接、複数分野にまたがる研究を実行する。</p>
<p>画像・信号・音声・映像・立体構造・軌跡・表・数式・グラフを含む4系統の科学的証拠、5分野にまたがる36件の実データ事例で評価したところ、OmniScientistは全36件で生データから完成原稿までの一連の流れを完走し、参照する推論バックボーンを用いた平均論文スコアは6.3点だった。事前計算済みのスカラー特徴量しか受け取らない盲検バリアントとの対比較では、生データへの直接的な知覚が7つの評価軸すべてを改善し、一対比較の85%で勝利した。この結果は、研究の全過程を通じた知覚が、証拠に根ざした科学的発見に不可欠であることを示している。</p>
<p><strong>出典:</strong> OmniScientist: An Omni-Modal Omni-Discipline AI Scientist. <a href="https://arxiv.org/abs/2608.13558">arXiv:2608.13558</a> (2026).</p>
<h2>論文3: 知識を小学校レベルに制限したLittleLearner</h2>
<p>現代の言語モデルは異種混合のウェブ規模コーパスで学習されるため、モデルがどの知識・スキルをどこで獲得したかを特定するのが難しく、獲得過程の研究自体が困難になっている。本研究はこの課題に対応するため、米国小学校教材相当に絞り込み、5学年より上の概念・事実・語彙を明示的に除外した880億トークンのプレトレーニングコーパスLITTLECURRICULUMを構築した。これをゼロから学習させた50億パラメータのLLMがLITTLELEARNERであり、開かれた評価に耐えるだけの言語能力を持ちながら、カリキュラム基準に沿って解釈可能な知識・能力の境界を持つ。</p>
<p>研究チームはLITTLECURRICULUMとLITTLELEARNERを、モデルがどのようにデータの範囲内で知識を獲得・表現・利用するかを調べるための、発達段階を制御したサンドボックスとして公開した。最初の実験群として、事後学習と文脈内学習を通じて新しい知識を注入する手法を試したところ、いずれの手法もモデルが既存知識をより有効に使えるようにはしたが、学習範囲外の能力を引き上げることはなかった。この結果は、知識獲得の境界を明確に管理できる環境が、今後の学習ダイナミクス研究にとって価値を持つことを裏付けている。</p>
<p><strong>出典:</strong> LittleLearner: Language Models Under Pedagogically Controlled Knowledge Exposure. <a href="https://arxiv.org/abs/2608.13545">arXiv:2608.13545</a> (2026).</p>
<h2>論文4: 疎自己符号化器の特徴を言語化するSAEVerbalizer</h2>
<p>疎自己符号化器（SAE）はLLMの内部表現から多数の特徴を取り出す手法として提案されているが、それぞれの特徴が何を表すかの説明は、依然として外部からの観察に頼っている。この方法は、観測されたモデルの振る舞いから推測する表面的な説明に陥りやすく、そうした行動証拠を大規模に集める計算コストも大きい。本研究は、SAEのデコーダー方向をLLMの表現に注入し、注入された特徴の自然言語説明を生成できるようLLMの下流層をファインチューニングするSAEVerbalizerを提案する。学習後は、デコーダー方向から直接SAE特徴を言語化できるため、両方の限界に対応する。</p>
<p>実験では、学習した言語化能力が未見の特徴にも一般化し、別々に学習されたSAE辞書間でも転用でき、軽量なアダプタを追加すれば異なるLLM由来のSAE特徴にも拡張できることが示された。介入実験では、複数のデコーダー方向を同時に注入すると、それぞれの意味を組み合わせた説明が生成され、個々の方向を反転させるとそれに対応する意味の変化が説明に反映されることも確認された。特徴の意味を後付けで観察するのではなく、モデル自身に語らせるという方向性を示した研究である。</p>
<p><strong>出典:</strong> SAEVerbalizer: Generating Explanations for Sparse Autoencoder Features via Representation Verbalization. <a href="https://arxiv.org/abs/2608.13538">arXiv:2608.13538</a> (2026).</p>
<h2>論文5: 許諾データのみで作る1BのフロンティアモデルDFM Mimir v1</h2>
<p>現在の大規模言語モデル開発の多くは、しばしば許諾を得ていない大規模データセットに依存しており、オープンソースかつ倫理的に調達されたデータにこだわる研究者にとって高い障壁となっている。本研究は、階層型推論モデル（HRM）アーキテクチャに基づく10億パラメータの言語モデルMimir v1を、許諾済みの事後学習データ161個のデータセットのみでゼロから学習し、英語で高い競争力を持ちながらデンマーク語で新たな最高性能を達成したと報告する。</p>
<p>英語・数学とコード・デンマーク語にまたがる20のベンチマークで評価した結果、Mimir v1は元となったHRM-Text 1Bを上回り、より大きなフロンティアモデルであるQwen 3.5 4BやGemma 4 E2Bとも競合する性能を示した。モデルはHugging Face Hub上で公開されている。データ調達の倫理性を保ちながら、パラメータ規模で劣るモデルがどこまで大規模モデルに迫れるかを、実データと具体的なベンチマーク数値で示した点が本研究の意義である。</p>
<p><strong>出典:</strong> DFM Mimir v1: An Open HRM Delivering Frontier Performance at 1B Parameters Using Only Permissible Post-Training Data. <a href="https://arxiv.org/abs/2608.13517">arXiv:2608.13517</a> (2026).</p>
<h2>論文6: 事前学習を通じたデータ影響力の時間変化を測る</h2>
<p>言語モデルの事前学習全体を通じて、どの訓練データがモデルに影響を与えているかを一貫した基準で測ることは難しい。モデルの汎用能力を代表する下流タスクや検証セットを選ぶこと自体が難しく、学習途中のチェックポイントでのタスク性能に依存すると、学習過程全体での比較が複雑になる。本研究は、下流タスクや検証セットを attribution の対象として選ばずに済む、訓練データ影響力の測定手法を提案する。具体的には、あるサンプルの勾配更新が、最終的な学習済みパラメータまでの二乗距離をどれだけ縮めたかとして影響力を定義し、この量を再学習なしに中間チェックポイントから推定する。</p>
<p>PythiaとPolyPythiaの学習系列に含まれる18種類の設定にこの手法を適用したところ、影響力の大きいデータが学習の進行とともに体系的に変化することがわかった。学習初期には文献関連のデータが最終パラメータへの軌道により強く整合し、学習が進むにつれてSTEM系のデータの方がより強く整合するようになるという、質的な逆転現象がモデル設定を超えて広く一貫して観察された。特定の下流タスクや検証セットに紐づく従来の影響力分析を補完する、軌道レベルでの新しい視点を提供する結果である。</p>
<p><strong>出典:</strong> Measuring Task-Agnostic Training Data Influence Across Language Model Pretraining. <a href="https://arxiv.org/abs/2608.13515">arXiv:2608.13515</a> (2026).</p>
<h2>論文7: 397Bの科学エージェント基盤モデルIntern-S2-Preview</h2>
<p>科学的発見には、異種のモダリティにまたがる科学的証拠を推論し、科学的なツールや環境と対話し、長期にわたる作業を継続できるAIシステムがますます求められている。本研究は、多モーダルな科学理解・推論・生成・長期タスクを支援する科学エージェント基盤モデル群Intern-S2-Previewを発表する。学習パイプラインは、科学文書のレンダリング画像やテキストが入り交じったデータ、多様な科学コーパスを用いた多モーダル事前学習から始まり、教師あり微調整、大規模なマルチタスク強化学習、ブラックボックス・ホワイトボックス双方のエージェント型強化学習、オンポリシー蒸留からなる統一的な事後学習パイプラインへと続く。部分ロールアウトとオフポリシー補正、適応的な長さ正則化、オンライン投機的デコーディングなど、学習の安定性と効率を高める実装上の工夫も導入されている。</p>
<p>アーキテクチャ面では、397BパラメータのIntern-S2-Preview-397Bが時系列モデリングを効率的な長系列理解から数値予測にまで拡張し、凍結された397Bのバックボーンを変更せずに済む、記憶拡張型の別経路としてMemory Decoderが検討されている。科学・多モーダル・エージェント・汎用の各ベンチマークで、Intern-S2-Preview-397Bは複数の設定で競争力のある、あるいは最上位の結果を達成した。時系列モジュールはSciTSでの科学信号理解と予測を改善し、独立したIntern-MemDec-4B拡張は、凍結された397Bバックボーンを変更しないままBiology-Instructionsの平均スコアを56.92点から60.32点に引き上げた。</p>
<p><strong>出典:</strong> Intern-S2-Preview: Scientific Agentic Foundation Model. <a href="https://arxiv.org/abs/2608.13505">arXiv:2608.13505</a> (2026).</p>
<h2>論文8: 知らないことを認められないLLM——グライスの後退を探る</h2>
<p>LLMは知識境界の外にある対象について尋ねられると、より安全で一般的な主張へ後退するのではなく、もっともらしい詳細をでっち上げてしまうことが多い。本研究はこの失敗を、協調的な話し手が対象について不確かなとき、具体性を犠牲にして真実性を優先し、より抽象的な言い方へ後退するという、グライスの協調の原理の枠組みで捉え直す。LLMがこの「後退」を行うための材料を備えているかを調べるため、対象の既知度と参照の具体性を変化させたT-RExベースのベンチマークを用い、（1）モデルの内部活性化が対象を知識境界の内側と外側のどちらとして符号化しているか、（2）これから生成しようとする参照の具体性をあらかじめ見越しているかという2つの問いを検証している。</p>
<p>分析の結果、両方の問いに対する答えは「はい」であったが、この2つの信号は生成の段階では統合されていないことが分かった。モデルは対象が未知であっても具体的な参照を圧倒的に好み、正しい一般的な代替案を提示された場合でも同様の傾向を示した。つまりグライス的な後退を行うための材料は揃っているのに、それを実行に移す方針がモデルには備わっていない。研究チームはこの結果を、知識境界の認識と生成時の具体性を結びつける学習・誘導目的である「グライス的アラインメント」に向けた第一歩と位置づけている。</p>
<p><strong>出典:</strong> Toward a Gricean Retreat: Probing LLMs for Knowledge Boundaries and Referent Specificity. <a href="https://arxiv.org/abs/2608.13484">arXiv:2608.13484</a> (2026).</p>
<h2>論文9: 事前学習の最初のトークンから人格を作るSynthetic Persona Pretraining</h2>
<p>言語モデルに基づくAIが自律的な場面で使われるようになるにつれ、その目標や価値観を人間のそれと一致させることが重要になっている。現状のアラインメントやアシスタントとしての人格付けは、行動の事前傾向がすでに定まった事前学習の後に導入されるのが一般的であり、その結果、価値観が根付いたものではなく表面的な上塗りにとどまり、後からの誤整合を招きやすい。本研究は、これとは異なる立場から、規範的な価値憲章に基づく一人称の内省文を事前学習文書に付与し、事前学習の最初のトークンから望ましいアシスタント人格を組み込むSynthetic Persona Pretraining（SPP）を提案する。通常のクロスエントロピー損失で元の事前学習文書とその内省文の両方を学習させ、多数の人格の中に望ましい人格を植え付けたうえで、ユーザーとアシスタントの対話データで事後学習し、この人格をアシスタントという同一性に結びつける「人格の結合」という工程を経る。</p>
<p>最大30億パラメータのモデルを5000億トークンで学習させた実験では、SPPが憲章への追従性とジェイルブレイク耐性を高め、分布外の道徳的ジレンマにおける誤整合の割合を下げる一方で、能力自体は損なわないことが示された。事前学習の終盤だけにSPPを導入した比較条件では、憲章への追従性が弱く、価値の優先順位も変化せず、ジレンマにおける選択の整合性も劣っており、この効果には人格の結合という工程が必要で、かつ事前学習に投じる計算量が増えるほど効果が大きくなることも分かった。価値観をいつ・どのように組み込むかというタイミングの設計が、アラインメントの効果を左右することを具体的に示した研究である。</p>
<p><strong>出典:</strong> Synthetic Persona Pretraining: Alignment from Token Zero. <a href="https://arxiv.org/abs/2608.13482">arXiv:2608.13482</a> (2026).</p>
<h2>論文10: 入力に応じて行列積を間引くReduced Matrix Multiplication</h2>
<p>トランスフォーマー型言語モデルは高い性能を持つ一方、繰り返される高次元の行列積のために推論コストが大きい。本研究は、モデルの重みを変更せず、行列積の縮約次元に沿って情報量の多いスライスだけを選択することで計算量を減らす、訓練不要かつ入力適応的な推論手法Reduced Matrix Multiplication（RMM）を提案する。単純な保持率の制御によって、精度と効率のなめらかで予測可能なトレードオフが得られる設計になっている。</p>
<p>10億から700億パラメータの言語モデル群で検証したところ、どれだけ削減に耐えられるかはモデルファミリー・タスク・コンポーネント・保持率によって異なるものの、多くの場合モデル規模が大きいほど削減耐性が高まる傾向が見られた。中程度の削減であれば、識別・自己回帰生成・長文脈という評価設定を通じてRMMは頑健に機能し、この考え方はマルチモーダルな視覚言語推論にも拡張できることが示されている。メカニズム面の分析では、アテンション側の計算はMLP部分よりも大幅に削減しやすいという構造的な非対称性が明らかになった。NVIDIA A100上で専用カーネルを用いた実時間ベンチマークでは、この計算量削減が実際の実行時間短縮につながり、特に長い系列長でその効果が大きいことも確認されている。</p>
<p><strong>出典:</strong> Reduced Matrix Multiplication: Input-Adaptive Matrix-Product Reduction for LLM Inference. <a href="https://arxiv.org/abs/2608.13426">arXiv:2608.13426</a> (2026).</p>
<hr />
<h2>まとめ</h2>
<p>10本を通じ、「モデル単体の性能」ではなく「学習・運用・評価の設計」が成果を左右する構図が繰り返し現れた。AutoDesignとOmniScientistはエージェントの実行フィードバックや生データへの知覚をシステム設計に組み込むことで性能を引き上げ、LittleLearnerとデータ影響力研究は学習データの範囲・時期がモデルの知識形成をどう規定するかを可視化した。SAEVerbalizerは内部特徴の説明生成そのものをモデルに担わせ、Mimir v1とRMMはデータ許諾性・推論コストという制約下での実用的な効率化を示した。Gricean RetreatとSPPは、知識境界の自覚や価値観をいつ・どう学習過程に組み込むかという、安全性設計のタイミングの重要性を提起している。</p>
<h2>参考ソース</h2>
<ul>
<li>論文1 — AutoDesign: Meta-Harness Optimization for Long-Horizon Agentic Design. <a href="https://arxiv.org/abs/2608.13560">arXiv:2608.13560</a></li>
<li>論文2 — OmniScientist: An Omni-Modal Omni-Discipline AI Scientist. <a href="https://arxiv.org/abs/2608.13558">arXiv:2608.13558</a></li>
<li>論文3 — LittleLearner: Language Models Under Pedagogically Controlled Knowledge Exposure. <a href="https://arxiv.org/abs/2608.13545">arXiv:2608.13545</a></li>
<li>論文4 — SAEVerbalizer: Generating Explanations for Sparse Autoencoder Features via Representation Verbalization. <a href="https://arxiv.org/abs/2608.13538">arXiv:2608.13538</a></li>
<li>論文5 — DFM Mimir v1: An Open HRM Delivering Frontier Performance at 1B Parameters Using Only Permissible Post-Training Data. <a href="https://arxiv.org/abs/2608.13517">arXiv:2608.13517</a></li>
<li>論文6 — Measuring Task-Agnostic Training Data Influence Across Language Model Pretraining. <a href="https://arxiv.org/abs/2608.13515">arXiv:2608.13515</a></li>
<li>論文7 — Intern-S2-Preview: Scientific Agentic Foundation Model. <a href="https://arxiv.org/abs/2608.13505">arXiv:2608.13505</a></li>
<li>論文8 — Toward a Gricean Retreat: Probing LLMs for Knowledge Boundaries and Referent Specificity. <a href="https://arxiv.org/abs/2608.13484">arXiv:2608.13484</a></li>
<li>論文9 — Synthetic Persona Pretraining: Alignment from Token Zero. <a href="https://arxiv.org/abs/2608.13482">arXiv:2608.13482</a></li>
<li>論文10 — Reduced Matrix Multiplication: Input-Adaptive Matrix-Product Reduction for LLM Inference. <a href="https://arxiv.org/abs/2608.13426">arXiv:2608.13426</a></li>
</ul>

</details>

---

[← 2026-08-17 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
