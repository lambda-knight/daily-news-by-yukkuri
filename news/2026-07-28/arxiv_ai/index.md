---
title: "VLMジェイルブレイクと著作権エージェント検証ほか生成AI論文10本解説【2026/07/28】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# VLMジェイルブレイクと著作権エージェント検証ほか生成AI論文10本解説【2026/07/28】

**2026-07-28 / arxiv AI論文解説**

<audio controls src="https://archive.org/download/news-pickup-2026-07-28-arxiv-ai/arxiv_ai_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-07-28-arxiv-ai)

---

## 概要

今日は、画像の「見せ方」だけでVLMの安全機構を突破するAdversarial Style Optimization、AIエージェントが著作権保護コンテンツを選んでしまうかを検証するCopyright-Bench、文書をLoRAアダプタへ焼き込んでクローズドブックQAの精度を大きく引き上げる研究から、文書からのポッドキャスト生成の忠実性、エージェント記憶の長期評価で起きる順位逆転、MoEモデル向けのMoE型LoRA、言語化せずに考えを引き継ぐJ-CoTまで、生成AI論文10本をずんだもんと四国めたんが解説します。

▼ 今日のトピック
・VLMのジェイルブレイクを画風の最適化で強化するAdversarial Style Optimization
・モデル同士の相互採点でLLMの応答品質を測る合意ベース評価フレームワーク
・執筆過程そのものを証拠化する人間とAIの共同ライティング環境「Humanly」
・LLMエージェントは著作権法を守れるか——Copyright-Benchによる検証
・容量よりデータ品質——文書をLoRAアダプタに焼き込むクローズドブックQA
・検索拡張生成で歴史文書の欠損文字と固有名詞を復元する
・文書からのポッドキャスト生成における忠実性の劣化とその修復
・エージェント記憶の長期評価と「在職期間交差」現象
・MoEモデルにMoE型LoRAを組み合わせるMoE²-LoRA
・言語化しない思考の連鎖——J空間で推論するJ-CoT

▼ 参考論文（arXiv）
https://arxiv.org/abs/2607.21619 — Adversarial Style Optimization: Enhancing VLM Jailbreaks by GRPO-based Stylistic Triggers Optimization
https://arxiv.org/abs/2607.21632 — A Consensus-Based Framework for Relative Preference Evaluation of Large Language Models
https://arxiv.org/abs/2607.21758 — Humanly: A Configurable and Traceable Environment for Human-AI Collaborative Writing
https://arxiv.org/abs/2607.21799 — Copyright-Bench: Agentic Evaluation of Copyright Law Compliance
https://arxiv.org/abs/2607.21861 — Data Quality over Capacity: Internalizing Documents into LoRA Adapters for Closed-Book QA
https://arxiv.org/abs/2607.21936 — Leveraging External Knowledge for Historical Document Restoration via Retrieval-Augmented Large Language Models
https://arxiv.org/abs/2607.21961 — On Improving Faithfulness of Podcasts from Documents
https://arxiv.org/abs/2607.21962 — Ground Truth First: A Longitudinal Evaluation Instrument for Agent Memory, and the Tenure Crossover in Memory-Architecture Rankings
https://arxiv.org/abs/2607.21978 — MoE$^2$-LoRA: When MoE Models Meet MoE-style Low-Rank Adaptation
https://arxiv.org/abs/2607.21981 — J-CoT: Chain-of-Thought in J-Space

#生成AI #ChatGPT #Claude #LLM #AI #人工知能 #arxiv #論文解説 #ゆっくり解説 #ずんだもん #OpenAI #Anthropic #機械学習 #ディープラーニング

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>arXiv生成AIニュース（2026年7月28日）</h1>
<p><strong>キーワード:</strong> ジェイルブレイク耐性 / LLM評価手法 / 著作権コンプライアンス / LoRAファインチューニング / エージェント記憶 / 潜在推論</p>
<p>今日ハイライトする3本は、VLMの安全機構を画風だけで突破する「Adversarial Style Optimization」、コマース系エージェントに著作権遵守を試す「Copyright-Bench」、そして文書をLoRAアダプタへ丸ごと焼き込みクローズドブックQAの精度を大きく引き上げる研究。いずれも「モデルの能力そのもの」ではなく「モデルをどう使い、どう評価し、どう縛るか」という運用面に切り込む論文が今週は目立つ。</p>
<h2>論文1: VLMのジェイルブレイクを画風の最適化で強化するAdversarial Style Optimization</h2>
<p><strong>出典:</strong> Adversarial Style Optimization: Enhancing VLM Jailbreaks by GRPO-based Stylistic Triggers Optimization. <a href="https://arxiv.org/abs/2607.21619">arXiv:2607.21619</a> (2026).</p>
<p>清華大学、ハルビン工程大学、山東大学、西安電子科技大学の共同チームによる研究で、マルチモーダル大規模言語モデル（MLLM）の安全性検証を扱う。従来のジェイルブレイク攻撃研究は、画像に何を写すか（内容ベースの攻撃トリガー）に焦点を当ててきた。この論文は視点を変え、画像がどのように提示されるか、つまり画風や構図といった非内容的な要素そのものが安全機構を回避する脆弱性になり得ることを指摘する。著者らはまず、既存の攻撃画像に「鉛筆スケッチ」のような既製のスタイルフィルタをかけるだけで、攻撃成功率（ASR）が明確に上昇することを予備実験で確認した。</p>
<p>この観察を出発点に、Adversarial Style Optimization（ASO）というプラグイン型の強化モジュールを提案する。ASOは画像編集モデル（FLUX-Kontextを利用）を強化学習でファインチューニングし、任意の既存攻撃画像に最適なスタイル変換を重ねる。学習にはGroup Relative Policy Optimization（GRPO）を用い、報酬はモデルの拒否応答を検知するロジットベースの信号と、判定用の強力な別モデルによる意味的評価を組み合わせた「構造的階層型報酬関数」で与える。これにより、鉛筆スケッチなら線の密度や筆致の強さといった、直感的には選びにくいパラメータまで自動的に最適化できる。実験では既存の最先端攻撃にASOを組み合わせることでASRが一貫して向上したと報告されており、スタイル的なバイアスがMLLMのレッドチーミングにおいてスケール可能な攻撃経路であることを示す。安全機構がテキストの中身だけでなく画像の見た目にも脆弱であるという指摘は、防御側の評価基準の見直しを迫るものだが、論文自体は防御手法の提案までは踏み込んでいない点に留意する必要がある。</p>
<h2>論文2: モデル同士の相互採点でLLMの応答品質を測る合意ベース評価フレームワーク</h2>
<p><strong>出典:</strong> A Consensus-Based Framework for Relative Preference Evaluation of Large Language Models. <a href="https://arxiv.org/abs/2607.21632">arXiv:2607.21632</a> (2026).</p>
<p>単著の研究で、従来のLLMベンチマークが抱える「唯一の正解が決まらない課題にどう点数をつけるか」という問題に取り組む。プログラミングや数学のように客観的に正誤が判定できるタスクと異なり、説明の分かりやすさや構成の良さなど、複数の応答がいずれも妥当な場面では固定の正解データと照合するだけでは品質の差を捉えきれない。そこで著者は、5つの最先端LLMをパネルとして用い、各モデルが生成した匿名化済みの回答を互いにランキングさせる「合意ベース評価」を提案する。モデル間の一致度合いを、盲検条件下での知覚的な応答品質の代理指標として扱う発想である。</p>
<p>具体的には、プログラミング・一般知識・安全性・論理推論・数学という複数領域で、各モデルが応答を生成した後、匿名化された他モデルの応答を構造化された投票プロセスでランク付けし、その結果を集計してRelative Intelligence Index（RII）を算出する。RIIは、あるモデルの応答が他モデルからどれだけ高頻度で選好されたかを表す。分析の結果、領域を横断して一貫した選好パターンが見られ、特定のモデルが恒常的に高く評価される傾向が確認されたと報告されている。ただし著者自身が強調する通り、この指標はモデル間の選好の一致を表すものであり、客観的な正しさや人間の判断そのものと直接一致するとは限らない。先行研究ではモデル集団の選好が人間の評価と部分的に相関するとされており、それが本手法の代理指標としての妥当性を支える根拠に留まる点は、評価設計上の限界として明確にしておくべきだろう。</p>
<h2>論文3: 執筆過程そのものを証拠化する人間とAIの共同ライティング環境「Humanly」</h2>
<p><strong>出典:</strong> Humanly: A Configurable and Traceable Environment for Human-AI Collaborative Writing. <a href="https://arxiv.org/abs/2607.21758">arXiv:2607.21758</a> (2026).</p>
<p>UTオースティン、トロント大学、スタンフォード大学、マサチューセッツ工科大学、南カリフォルニア大学、キング・アブドラ科学技術大学の共同チームによる研究である。教員や学会の査読責任者、一般読者は、完成した文書だけを見て、それが人間の手で書かれたのか、AIが生成したのか、あるいは混在したものかを判断せざるを得ない。既存のAI生成テキスト検出器は完成文のみを分類対象とするため、非母語話者の文章を誤ってAI生成と判定したり、パラフレーズや簡単な文章操作で精度が崩れたりする既知の弱点がある。またウォーターマーキングも、そのウォーターマークが有効化された生成にしか適用できないという制約を持つ。</p>
<p>著者らが提案する「Humanly」は、完成文ではなく執筆プロセスそのものを証拠にする書字環境である。ユーザーは個人利用や課題向けに執筆環境を設定し、ワークスペース内での入力活動とAI支援の利用を記録しながら執筆する。完了したセッションは「封印された執筆証明書」としてパッケージ化され、設定に応じた異常行動レビューが付与される。授業課題や査読、個人の証明といった用途を想定しており、ユーザースタディでは役割を問わず有用性が確認され、レッドチーミング調査ではHumanly Typing Detectorが人間の手入力と自動化されたタイピングを区別できることが示された。既存のGoogle Docsのような文書履歴依存型のツールに比べ、ワークスペース全体の活動やAI支援の詳細まで粒度細かく記録できる点が差分だが、記録自体をユーザーが操作・偽装する余地についての頑健性評価は本文の範囲では確認できない。</p>
<h2>論文4: LLMエージェントは著作権法を守れるか——Copyright-Benchによる検証</h2>
<p><strong>出典:</strong> Copyright-Bench: Agentic Evaluation of Copyright Law Compliance. <a href="https://arxiv.org/abs/2607.21799">arXiv:2607.21799</a> (2026).</p>
<p>Zheng Hui氏らの研究チームによるもので、ICML関連の機械学習分野の枠組みで発表されている。LLMエージェントはウェブサイト制作やマーチャンダイズデザイン、ピッチデック作成といった商用タスクで、外部の画像などのコンテンツを取得し、必要に応じて再利用するようになっている。しかし現状、そうしたエージェントが著作権法を実際に遵守しているかを評価する枠組みが不足していた。既存のエージェント評価はタスク遂行の成否のみを測るため、著作権を侵害しつつタスクを完遂したエージェントが、合法的に遂行した比較対象より高いスコアを得てしまうという「法的な死角」が生じる。</p>
<p>そこで著者らはCopyright-Benchを構築した。パブリックドメインのコンテンツ（利用が合法）と著作権保護されたコンテンツ（この設定では利用が侵害に当たる）のどちらかをエージェントに選ばせる、現実的な商用タスク群である。評価にはユーザーの好みの違いを模したプロンプトのバリエーションや、時間的プレッシャーを課す条件も組み込まれている。最先端のLLMエージェントを人間のベースラインと比較した結果、（1）パブリックドメインの代替物が利用可能であっても、エージェントは著作権保護されたコンテンツを選んでしまうこと、（2）オープンウェイトモデルでは、特定のユーザーの好みや模擬的な時間的プレッシャーに応じて侵害率が上昇すること、が確認された。著作権を意識させる指示を与えると侵害が減り、逆に著作権を軽視するような指示を与えるとプロプライエタリモデルとオープンウェイトモデルの間で挙動が大きく乖離するという知見は、エージェントの商用展開における法的リスク評価に直接関わる。</p>
<h2>論文5: 容量よりデータ品質——文書をLoRAアダプタに焼き込むクローズドブックQA</h2>
<p><strong>出典:</strong> Data Quality over Capacity: Internalizing Documents into LoRA Adapters for Closed-Book QA. <a href="https://arxiv.org/abs/2607.21861">arXiv:2607.21861</a> (2026).</p>
<p>Joan Figuerola Hurtado氏による単著研究で、検索や文脈窓の予算を使わずに文書コーパスに関する質問へ答える「クローズドブックQA」を、4ビット量子化されたGemma系のモデル（4Bクラス）にLoRAで文書を焼き込むことで実現する。単一文書から99文書のコーパスまで、約100回の学習実験を通じて、アダプタの容量が十分である限り、学習データの品質がLoRAのランクや学習率、2種類の代替アーキテクチャを組み合わせた効果よりも支配的な要因になることを示した。一方で容量そのものは、それを下回るとどんなデータ改善も効かない「硬いゲート」として機能するという。</p>
<p>具体的には、正解となる回答を1〜6語程度の正準的な短いスパンに整形し、雑多なトリビア的設問を除去する一度のキュレーション作業だけで、15文書コーパスでのクローズドブック精度が57.7%から85.7%へと、他のどのアーキテクチャ変更よりも大きく向上した。15文書の部分集合ではBM25によるRAGパイプラインとの比較も行われ、内部化したアダプタは84.2%のリコールでBM25-RAG（58.9%）や、正解チャンクを直接与える理想的なオラクル条件（65.6%）さえも、より低いレイテンシで上回った。単一文書ではランク32・3000ステップという控えめなLoRA設定で86〜98%の精度に達する一方、文脈を全く与えないベースモデルはほぼ0%にとどまる。ただし、教師データを人手で作らず自己生成のクレームに切り替えると精度が57.7%へ急落するなど、データ品質への依存度がそのまま脆弱性にもなっている点は運用上の限界として重要である。</p>
<h2>論文6: 検索拡張生成で歴史文書の欠損文字と固有名詞を復元する</h2>
<p><strong>出典:</strong> Leveraging External Knowledge for Historical Document Restoration via Retrieval-Augmented Large Language Models. <a href="https://arxiv.org/abs/2607.21936">arXiv:2607.21936</a> (2026).</p>
<p>Gabeen Kim氏、Kyeongpil Kang氏による研究で、物理的な劣化や損傷で判読不能になった歴史文書の復元を扱う。従来のマスク言語モデリングに基づく復元手法は、周辺の文脈をうまく利用できる一方で、外部の歴史的知識を要する固有名詞の復元には弱いという課題があった。人物名や地名のように、文脈だけからは推測しきれない語を補うには、事前学習済みモデルが暗黙に持つ知識と、外部から明示的に取得した情報の両方が必要になる。</p>
<p>著者らはこの課題に対し、検索拡張生成（RAG）を組み込んだ復元フレームワーク「ARI」を提案する。事前学習済みLLMの暗黙知と、明示的に検索された外部文脈を組み合わせることで、文脈依存的な固有名詞の推定という難所を緩和する狙いである。韓国の歴史文書を対象とした広範な実験により、一般的な文字の復元と固有名詞の復元の両方でベースライン手法を大きく上回る性能が確認された。他分野の先行研究として、古代ギリシャの碑文の欠損文字を予測するタスクで上位20候補内の正解率が73.5%に達した例が引き合いに出されており、本研究も同様に、専門家による評価を含む包括的な評価で実務家にとって実用的なツールになり得ると位置づけられている。ただし対象が韓国語文書に限定されており、他言語・他文字体系への一般化については本文の範囲では確認できない。</p>
<h2>論文7: 文書からのポッドキャスト生成における忠実性の劣化とその修復</h2>
<p><strong>出典:</strong> On Improving Faithfulness of Podcasts from Documents. <a href="https://arxiv.org/abs/2607.21961">arXiv:2607.21961</a> (2026).</p>
<p>Soumya Dutta氏、Tejas Indulal Dhamecha氏、Pannaga Shivaswamy氏による研究で、テキスト資料から長尺の会話形式コンテンツ、すなわちポッドキャストを生成するLLMシステムを扱う。Pew Research Centerの調査によれば、月に一度以上ポッドキャストを聴く12歳以上のアメリカ人の割合は2013年の12%から2023年には42%まで伸びており、この形式でのAI生成コンテンツ需要の高まりが背景にある。こうしたシステムは流暢で魅力的な対話を生成できる一方、原文に根拠のない情報、すなわち「グラウンディングされていない」内容を紛れ込ませやすいという問題が指摘されてきたが、複数話者・長尺の会話形式における忠実性を体系的に調べた研究はこれが最初だという。</p>
<p>著者らは5分野にまたがる1500件超の文書データセットを構築し、複数のLLMでポッドキャストの書き起こしを生成した上で、各発話ターンが原文書によって裏付けられているかを判定する「ターンレベルのLLM-as-a-judge」フレームワークを導入し、人間評価によってその信頼性を検証した。分析の結果、GPT-4oを含む最先端モデルであっても、根拠のない発話を頻繁に生成することが示された。この問題を緩和するため、著者らは不誠実な発話ターンを検出し、会話の流れを保ったまま書き直す「catch-n-repair」というモデル非依存のフレームワークを提案し、ドメイン内・ドメイン外の両条件で忠実性が一貫して改善することを実験で確認している。生成AIによる要約・解説コンテンツ全般に共通する「もっともらしいが原文にない情報」という課題を、会話形式という難条件で定量的に扱った点が本研究の意義である。</p>
<h2>論文8: エージェント記憶の長期評価と「在職期間交差」現象</h2>
<p><strong>出典:</strong> Ground Truth First: A Longitudinal Evaluation Instrument for Agent Memory, and the Tenure Crossover in Memory-Architecture Rankings. <a href="https://arxiv.org/abs/2607.21962">arXiv:2607.21962</a> (2026).</p>
<p>Quentin Spencer氏による単著研究で、LLMエージェントの記憶機構を評価するベンチマークが抱える構造的な問題を指摘する。既存のベンチマークの多くは、まず会話を生成してから後付けで正解データを抽出するパイプラインを取っており、ラベル誤りや事前学習データとの汚染が指摘されている（著者はLoCoMoの正解データの6.4%に監査済みのラベル誤りがあると引用する）。また既存ベンチマークの多くは短い対話履歴しか扱わない点も限界だという。</p>
<p>著者はこのパイプラインを逆転させる。まず妥当性区間・変動クラス・情報源チャネルを持つ事実を「人生脚本サンプラー」が先に生成し、その事実マニフェストに基づいてLLMがチャットやメールの文面をレンダリングし、忠実性検証器がすべての事実が正しく埋め込まれているかを確認し、最後に問いを脚本から機械的に生成する。この設計により正解は構成上「脚本に忠実」であることが保証される。約380問・15種類の問いタイプからなるこの合成ベンチマークで5つの記憶アーキテクチャを無記憶のコントロール条件と比較したところ、履歴の長さによって順位が逆転する「在職期間交差」が観察された。3週間時点の短期履歴で最高精度（94.2%）を出す予算制約付きの要約マップ型記憶は、9週間後には初期に退避された内容の再現率が96.3%から72.2%まで落ち込む一方、来歴情報を型付けして保持するグラフ型記憶は90.4%まで伸び、階層型のハイブリッド方式も93.2%を維持した。短期指標だけでランキングした記憶アーキテクチャの選定が、長期運用では逆効果になりうるという知見は、エージェント記憶の実運用設計にとって重要な警鐘である。</p>
<h2>論文9: MoEモデルにMoE型LoRAを組み合わせるMoE²-LoRA</h2>
<p><strong>出典:</strong> MoE$^2$-LoRA: When MoE Models Meet MoE-style Low-Rank Adaptation. <a href="https://arxiv.org/abs/2607.21978">arXiv:2607.21978</a> (2026).</p>
<p>上海人工知能研究所、スウェーデン王立工科大学（KTH）、中国科学技術大学、復旦大学、香港中文大学の共同研究チームによる。Mixture-of-Experts（MoE、専門家混合）アーキテクチャはDeepSeek-V3やQwen3など大規模言語モデルで広く採用されているが、そのパラメータ効率的ファインチューニング（PEFT）手法は十分に研究されていなかった。既存のMoE向けPEFT手法は、ルーターの事前情報を無視して一様にアダプタを適用するか（効率が落ち忘却リスクが増す）、静的な専門家選択に頼るか（トークンごとの容量や専門家間の学習が制限される）のいずれかの弱点を抱えていた。</p>
<p>著者らが提案するMoE²-LoRAは、事前学習済みの専門家の特化とタスク固有の適応を、デュアルチャネルのRouting-Conditioned Projection（RCP）モジュールを介して深く結合させる。これはベースモデルのルーター活性化を再利用してLoRA側のルーティングに反映させる仕組みである。さらに全レイヤーで共有される単一のグローバルLoRA専門家プールを導入し、レイヤーごとの親和性が自然に立ち現れる形でモデル全体規模の適応とバランスの取れた専門家利用を可能にした。既存手法ESFTやDAS-LoRAはオフラインのルーター統計から重要な専門家の部分集合を選んでLoRAを適用するため、その部分集合から漏れた専門家は推論時に活性化されてもタスク固有の更新を十分受けられないという限界があったが、MoE²-LoRAはこの限界と、専門家間・レイヤー間の協調的なダイナミクスを見落とすという課題の両方に対応する設計である。異なる規模・専門家粒度を持つ複数のMoEバックボーンで評価した結果、下流タスクの精度で一貫して最先端の性能を達成しつつ、汎用能力もより強く保持できたと報告されている。</p>
<h2>論文10: 言語化しない思考の連鎖——J空間で推論するJ-CoT</h2>
<p><strong>出典:</strong> J-CoT: Chain-of-Thought in J-Space. <a href="https://arxiv.org/abs/2607.21981">arXiv:2607.21981</a> (2026).</p>
<p>オックスフォード大学、Imprint Lab、スタンフォード大学の共同研究チームによる。思考の連鎖（Chain-of-Thought、CoT）プロンプティングは、逐次的な計算ステップの間で中間状態を運ぶことで言語モデルの推論性能を高めてきたが、自然言語だけを再帰的なインターフェースとして使うことには制約がある。多くの一時的な計算は完全に言語化する必要がないにもかかわらず、CoTでは毎ステップを文法的に整った文として出力しなければならない。Coconutのような既存の潜在推論手法はこの制約を取り払い、連続的な隠れ状態を再帰的に伝播させるが、次の推論ステップに必要な情報を選択・整理する明示的な仕組みを欠いたまま、密な隠れベクトルを丸ごと渡してしまう。</p>
<p>著者らが提案するJ-CoTは、モデルの隠れ表現内にある「語彙インデックス付き座標系」であるJ空間を基盤にした再帰的推論フレームワークである。各サイクルの内部ではモデルは通常通り全隠れ空間で計算を行うが、サイクルの境界では中間状態をJ空間辞書上の語彙インデックス付き係数として表現し、これを「J思考」として次のサイクルへ引き継ぎ、再びモデルの隠れ表現へマッピングし直す。これにより、流暢な中間説明文を生成する必要も、隠れ状態全体を丸ごと再帰させる必要もなくなる。同一のバックボーンと推論設定で比較した結果、J-CoT-Zero（追加学習なし）は評価した全ベンチマークで最も強い潜在推論ベースラインと同等かそれを上回り、追加学習を行ったJ-CoT-Trainは数学・科学・コーディング・構造化された経路推論タスクの全体で最高スコアを達成したと報告されている。言語化を介さずに推論の「選択と整理」を可能にする中間インターフェースという着想は、CoTの計算コストと表現力のトレードオフに新しい選択肢を示すものだが、より大規模なモデルやより長い推論チェーンでの挙動については本文の範囲では確認できない。</p>
<hr />
<h2>参考ソース</h2>
<ul>
<li>論文1: Bingjun Luo et al. Adversarial Style Optimization: Enhancing VLM Jailbreaks by GRPO-based Stylistic Triggers Optimization. <a href="https://arxiv.org/abs/2607.21619">arXiv:2607.21619</a> (2026).</li>
<li>論文2: Mohtashim Khan. A Consensus-Based Framework for Relative Preference Evaluation of Large Language Models. <a href="https://arxiv.org/abs/2607.21632">arXiv:2607.21632</a> (2026).</li>
<li>論文3: Shenzhe Zhu et al. Humanly: A Configurable and Traceable Environment for Human-AI Collaborative Writing. <a href="https://arxiv.org/abs/2607.21758">arXiv:2607.21758</a> (2026).</li>
<li>論文4: Zheng Hui, Doni Bloomfield, Noam Kolt. Copyright-Bench: Agentic Evaluation of Copyright Law Compliance. <a href="https://arxiv.org/abs/2607.21799">arXiv:2607.21799</a> (2026).</li>
<li>論文5: Joan Figuerola Hurtado. Data Quality over Capacity: Internalizing Documents into LoRA Adapters for Closed-Book QA. <a href="https://arxiv.org/abs/2607.21861">arXiv:2607.21861</a> (2026).</li>
<li>論文6: Gabeen Kim, Kyeongpil Kang. Leveraging External Knowledge for Historical Document Restoration via Retrieval-Augmented Large Language Models. <a href="https://arxiv.org/abs/2607.21936">arXiv:2607.21936</a> (2026).</li>
<li>論文7: Soumya Dutta, Tejas Indulal Dhamecha, Pannaga Shivaswamy. On Improving Faithfulness of Podcasts from Documents. <a href="https://arxiv.org/abs/2607.21961">arXiv:2607.21961</a> (2026).</li>
<li>論文8: Quentin Spencer. Ground Truth First: A Longitudinal Evaluation Instrument for Agent Memory, and the Tenure Crossover in Memory-Architecture Rankings. <a href="https://arxiv.org/abs/2607.21962">arXiv:2607.21962</a> (2026).</li>
<li>論文9: Qingyu Yang et al. MoE$^2$-LoRA: When MoE Models Meet MoE-style Low-Rank Adaptation. <a href="https://arxiv.org/abs/2607.21978">arXiv:2607.21978</a> (2026).</li>
<li>論文10: Junde Wu et al. J-CoT: Chain-of-Thought in J-Space. <a href="https://arxiv.org/abs/2607.21981">arXiv:2607.21981</a> (2026).</li>
</ul>

</details>

---

[← 2026-07-28 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
