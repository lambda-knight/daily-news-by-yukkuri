---
title: "思考の連鎖でも見えない推論？生成AI重要論文10本【2026/07/29】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# 思考の連鎖でも見えない推論？生成AI重要論文10本【2026/07/29】

**2026-07-29 / arxiv AI論文解説**

<audio controls src="https://archive.org/download/news-pickup-2026-07-29-arxiv-ai/arxiv_ai_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-07-29-arxiv-ai)

---

## 概要

LLMは説明に書かない計算をしているのか。見えない推論、適応的な推論予算、医療文書の矛盾検出、教育AI、多言語評価まで、最新10本を数値と限界を含めて解説します。

▼ 今日の論文ラインナップ
・思考の連鎖に現れないLLMの「見えない推論」（arXiv:2607.22925）
・難しい質問だけ深く考えるAutoThinkSQL（arXiv:2607.22622）
・厳格な採点表がLLM査読を悪化させる（arXiv:2607.22553）
・物語を忘れさせても崩壊させないLENS評価（arXiv:2607.22657）
・ベンガル語の複雑な文章題を集めたPatiGonit22K（arXiv:2607.22859）
・電子カルテ3000件から矛盾候補を検出する二段階LLM（arXiv:2607.22954）
・答えを教えず問い返すソクラテス型教育LLM（arXiv:2607.22996）
・翻訳しない多言語推論評価ADAGE（arXiv:2607.23058）
・アテンションで層を選ぶ対照デコーディング（arXiv:2607.23067）
・LoRAと活性化ステアリングで包摂的な文章を作る（arXiv:2607.23083）

▼ 参考論文（arXiv）
https://arxiv.org/abs/2607.22925 — 見えない推論
https://arxiv.org/abs/2607.22622 — AutoThinkSQL
https://arxiv.org/abs/2607.22553 — LLM自動査読
https://arxiv.org/abs/2607.22657 — 物語忘却のLENS評価
https://arxiv.org/abs/2607.22859 — PatiGonit22K
https://arxiv.org/abs/2607.22954 — 電子カルテ矛盾検出
https://arxiv.org/abs/2607.22996 — ソクラテス型教育LLM
https://arxiv.org/abs/2607.23058 — ADAGE
https://arxiv.org/abs/2607.23067 — アテンション誘導型対照デコーディング
https://arxiv.org/abs/2607.23083 — 包摂的生成の活性化ステアリング

#生成AI #ChatGPT #Claude #LLM #AI #人工知能 #arxiv #論文解説 #ゆっくり解説 #ずんだもん #機械学習 #ディープラーニング

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>arXiv生成AIニュース（2026年7月29日）</h1>
<p><strong>キーワード:</strong> 見えない推論 / 適応的思考 / 医療文書検証 / ソクラテス型教育 / 多言語推論 / 活性化ステアリング</p>
<p>今日のハイライトは三つある。第一に、意味のない埋め草トークンでも推論精度が最大13ポイント上がり、思考の連鎖を監視するだけでは内部計算を捉えきれないという安全上の警告。第二に、テキストからSQLを作る際、問題の難しさに応じて深い推論を使い分け、精度を保ちながら出力トークンと遅延を削減する研究。第三に、電子カルテ3000件から3460件の矛盾候補を拾いながら、時間関係や診断の変化が誤検知を生むことまで分析した研究である。今週は、モデルを単に大きくするより、いつ考え、何を監視し、どの条件で判断を信頼するかを問う論文が目立つ。</p>
<h2>論文1: 思考の連鎖に現れないLLMの「見えない推論」</h2>
<p><strong>出典:</strong> Not All LLM Reasoning is Visible in the Chain-of-Thought. <a href="https://arxiv.org/abs/2607.22925">arXiv:2607.22925</a> (2026).</p>
<p>Vatsal Baherwani氏、Tom Goldstein氏、Ashwinee Panda氏は、言語モデルが推論過程をすべて出力トークンへ表すという、思考の連鎖監視の前提を検証した。三つの合成推論タスクと13の最先端モデルを使い、意味的には課題と無関係な埋め草トークンを途中に出させる。すると多くのモデルで正答率が上がり、改善幅は最大13パーセントポイントに達した。効果は埋め草の種類とモデルの組み合わせに依存しており、単なるトークン数の増加だけでは説明できない。</p>
<p>さらにClaude Opus 4.5では、主要タスクの精度を損なわず、出力された思考からは見えない隠れた剰余算術の制約を満たせた。Qwen3-235Bへの強化学習は埋め草の内容に強い選好を作ったが、強化学習でも教師あり学習でも、テスト時まで持続する埋め草の利益は生じなかった。したがって「自然言語の思考を読めば内部目的も監査できる」とまでは言えない一方、合成課題の現象を実環境の欺瞞へ直結させることもできない。重要なのは、観測可能な説明と実際の計算を同一視しない評価設計である。</p>
<h2>論文2: 難しい質問だけ深く考えるAutoThinkSQL</h2>
<p><strong>出典:</strong> Learning When to Reason for Text-to-SQL via SFT and DPO. <a href="https://arxiv.org/abs/2607.22622">arXiv:2607.22622</a> (2026).</p>
<p>Soohyuk Jang氏らは、自然言語の質問をSQLへ変換するテキスト・トゥ・SQLで、すべての質問に思考の連鎖を強制する非効率を扱う。単純な検索や集計にも長い推論を出すと、精度向上に寄与しないトークンと待ち時間が増える。提案するAutoThinkSQLは、教師ありファインチューニングと直接選好最適化の双方へ「自動思考」機構を組み込み、簡単な質問では推論を省略し、複雑な質問だけ深い思考を呼び出す。</p>
<p>Qwen3-Coder-30B-A3Bを用いたSpiderとBIRDで、最良の比較手法より一貫して性能を改善したうえ、常に思考の連鎖を使う生成と比べ、平均出力トークンをそれぞれ24.6%と18.3%、平均遅延を17.1%と11.5%減らした。追加分析では、思考するか否かの選択が質問難度と整合した。ただし要旨からは、未知のデータベース構造や実運用の分布変化でも選択が安定するかは確認できない。成果の核心は「推論を長くする」のでなく、推論予算を入力ごとに配分した点にある。</p>
<h2>論文3: 厳格な採点表がLLM査読を悪化させる</h2>
<p><strong>出典:</strong> Evaluating the Impact of Reviewer Guideline Design on LLM-Based Automated Peer Review. <a href="https://arxiv.org/abs/2607.22553">arXiv:2607.22553</a> (2026).</p>
<p>Haowen Li氏、Yoichi Ishibashi氏、Masafumi Oyamada氏は、LLMによる査読で、モデルそのものではなく査読ガイドラインの設計が人間との一致にどう影響するかを調べた。比較したのは、学会が蓄積してきた公式ガイドラインと、高品質な人間査読からLLMに模倣生成させたガイドラインである。査読自動化では評価項目を細かく固定すれば安定しそうに見えるが、研究の価値判断は単純なチェックリストへ還元しにくい。</p>
<p>実験では、公式の学会ガイドラインを使った査読が人間の判断と最も整合し、査読者を模倣した生成ガイドラインは概して劣った。さらに厳格なルーブリック式採点を強制すると、一貫して性能が悪化した。これは自由な採点が常に優れるという証明ではなく、要旨には対象分野や絶対的な一致率も示されていない。それでも、査読実務で洗練された基準と、過去の文章表面を模倣することは別物であり、主観的・全体的な判断余地を残す必要性を示す結果である。</p>
<h2>論文4: 物語を忘れさせても崩壊させないLENS評価</h2>
<p><strong>出典:</strong> Between Suppression and Collapse: Evaluating Narrative Unlearning with LENS. <a href="https://arxiv.org/abs/2607.22657">arXiv:2607.22657</a> (2026).</p>
<p>Viktoriia Makovska氏とGeorge Fletcher氏は、LLMが偽情報に沿った物語の枠組みをもっともらしい説明として再生する問題に対し、機械的忘却が本当に深い表現まで抑えたかを測るLENSを提案した。直接尋ねる、出典付きで尋ねる、対比させる、抽象化した抵抗テストを行う、という複数レベルで対象物語の再現を調べる。対象は、ロシアのウクライナ侵攻をNATO拡大で正当化する枠組みと、米国が台湾を利用または放棄するという枠組みである。</p>
<p>約120億パラメータの多言語指示モデル4種を評価し、対象物語の抑制と出力品質の崩壊を同時に扱う抑制・崩壊効率スコアでチェックポイントを選ぶと、再現を減らし、直接の忘却指示を越えて抑制が転移する場合があった。一方、抽象的な選択式プロンプトから対象物語の実在主体を回復する「エンティティ回復」も観測された。二つの物語と4モデルでの診断であり一般化には追加検証が要るが、忘却の成功を拒否率だけで測らず、意味の回り道と能力崩壊の双方を見る設計が重要である。</p>
<h2>論文5: ベンガル語の複雑な文章題を集めたPatiGonit22K</h2>
<p><strong>出典:</strong> PatiGonit22K: A Comprehensive Dataset for Solving Complex Bengali MWPs. <a href="https://arxiv.org/abs/2607.22859">arXiv:2607.22859</a> (2026).</p>
<p>Swastika Kundu氏、Azizul Hakim Fayaz氏、Tashreef Muhammad氏は、英語など高資源言語に偏った数学的文章題評価をベンガル語へ広げるPatiGonit22Kを公開した。元のPatiGonitを拡張し、単一演算だけでなく複数演算を要する問題を含む2万2441問を収録する。数学的推論の評価では、英文問題を翻訳しただけでは言語表現や生活文化の違いが人工的な癖になり、能力差と翻訳差を分離しにくい。</p>
<p>各問題は翻訳、注釈、文化的適応、検証を経て、言語的一貫性と数学的正しさを確保したと報告される。規模と難度を同時に増やした点は、低資源言語の教育自然言語処理と推論研究に共通の基盤を与える。ただし要旨では、モデル別の基準性能、注釈者間一致、難度ごとの分布は示されていないため、データセットの大きさだけを推論品質の保証とはみなせない。公開後には、文化適応が解法構造を保っているかを含む詳細な監査が次の課題になる。</p>
<h2>論文6: 電子カルテ3000件から矛盾候補を検出する二段階LLM</h2>
<p><strong>出典:</strong> Toward Automated Detection of Documentation Inconsistencies in Electronic Health Records. <a href="https://arxiv.org/abs/2607.22954">arXiv:2607.22954</a> (2026).</p>
<p>Jian Lu氏らは、実際の退院時サマリーにある内部矛盾を汎用LLMがどこまで発見でき、どこで誤るかを調べた。MIMIC-IV-Noteから無作為抽出した3000件に、Gemini 2.5 Proで候補を広く抽出し、Gemini 2.5 Flashで文脈に基づき検証する二段階パイプラインを適用した。その一部を臨床専門家が手作業で確認している。</p>
<p>システムは3460件の矛盾候補を抽出し、入院の69.7%に少なくとも一件の候補があった。人口統計、アレルギー、処置、診断、検査、薬剤、ケア計画まで範囲は広い。しかし専門家レビューでは、時系列推論、診断が時間とともに変わる文脈、外来処方の慣行を必要とする場合に反復的な失敗が確認された。したがって69.7%は真の誤記率ではなく候補が付いた割合である。著者らは厳密な矛盾から曖昧さまでを段階化し、分類、文書節、臨床領域、矛盾軸で記述する枠組みを提案しており、大規模運用前の方法論的基礎という位置づけである。</p>
<h2>論文7: 答えを教えず問い返すソクラテス型教育LLM</h2>
<p><strong>出典:</strong> Beyond Direct Answering: Aligning Educational LLMs as Socratic Guides via Heuristic Reinforcement Learning. <a href="https://arxiv.org/abs/2607.22996">arXiv:2607.22996</a> (2026).</p>
<p>Xiaokun Wang氏らは、教育用LLMが最初の応答で答えを開示しがちな問題を、段階的な問いで学習者を導くソクラテス型へ調整した。HeuristicEduは、教師ありの準備学習とグループ相対方策最適化を組み合わせる。訓練には実サービスから再構成した中国語の子ども向け科学対話797件を使い、認知的深さ、好奇心の喚起、直接性を評価するヒューリスティック報酬と、生徒が先に用語を出した場合の補正を設けた。</p>
<p>保持した30問では、最良構成が足場かけ有効性を30.0%から63.3%へ上げ、答えのキーワード漏洩を30.0%から13.3%へ下げた。興味深いのは、最良構成が直接性への罰則を最適化から外していた点で、露骨な漏洩防止項が勾配による行動調整と衝突し得る。未調整のQwen-72Bは有効性0%、漏洩96.7%で、規模だけでは教師役にならなかった。ただし評価は30問と小さく、中国語児童科学対話に限られるため、長期的な学習成果や他年齢への一般化は未確認である。</p>
<h2>論文8: 翻訳しない多言語推論評価ADAGE</h2>
<p><strong>出典:</strong> ADAGE: A Language-Agnostic Pipeline for Analogical Reasoning Evaluation. <a href="https://arxiv.org/abs/2607.23058">arXiv:2607.23058</a> (2026).</p>
<p>Ahmed Haj Ahmed氏とAlvin Grissom II氏は、英語ベンチマークの翻訳に依存する多言語推論評価を見直した。翻訳問題には原文由来の構造や不自然な表現が残り、各言語の文化に根差した類推を測りにくい。ADAGEは母語話者による選別とLLM支援生成を組み合わせ、翻訳を介さず、難度を設計した抽象類推ベンチマークを作る言語非依存パイプラインである。</p>
<p>アラビア語、アムハラ語、日本語でベンチマークを構築し、14のオープンウェイトモデルを評価した。英語のことわざ類推で高性能なモデルでも、三言語の母語ベンチマークでは英語比で正答率が12から52パーセントポイント低下する、一貫した文化的推論ギャップが見つかった。パイプライン、三つのベンチマーク、評価一式は公開される。ただし差のすべてを文化理解不足へ帰属するには、言語ごとの難度同等性や訓練データ量をさらに切り分ける必要がある。翻訳精度でなく、各言語内部で成立する推論を測る方向転換が主な貢献である。</p>
<h2>論文9: アテンションで層を選ぶ対照デコーディング</h2>
<p><strong>出典:</strong> Attention-Guided Layer Selection for Contrastive Decoding in Large Language Models. <a href="https://arxiv.org/abs/2607.23067">arXiv:2607.23067</a> (2026).</p>
<p>Yusuke Sakai氏、Natthawut Kertkeidkachorn氏、Kiyoaki Shirai氏は、LLMの成熟した層と未成熟な層の出力分布を対比して事実性を改善するDoLaの層選択を改良した。従来の動的選択は出力語彙分布の差だけを使うため、モデル内部でどの入力へ注目しているかという構造情報を捨てている。提案手法は自己アテンションを信号にし、ジェンセン・シャノン距離、最大エントロピー、最小エントロピーに基づく三つの選択戦略を導入する。</p>
<p>TruthfulQAで、特にAttention-JSDとAttention-Entropy-Minが元のDoLaを一貫して上回り、複数回答を評価するMC2とMC3で顕著な改善を示した。これは語彙出力の差よりも、アテンション分布が事実知識を解く層の感度の高い手掛かりになり得ることを示唆する。一方、要旨には絶対スコアや計算コスト、他ベンチマークでの結果がない。TruthfulQAでの優位を一般的な幻覚抑制へ拡張せず、内部信号を層選択へ使う有望な証拠として読むべきである。</p>
<h2>論文10: LoRAと活性化ステアリングで包摂的な文章を作る</h2>
<p><strong>出典:</strong> LoRA for Gender-Inclusive Rewriting and Activation Steering for Counter-Narrative Generation. <a href="https://arxiv.org/abs/2607.23083">arXiv:2607.23083</a> (2026).</p>
<p>Akhil Rajeev P氏とManoj Balaji J氏は、LT-EDI 2026共有タスクで、偏りのある文章を意味と文脈を保ちながらジェンダー包摂的に書き換える課題と、偏見へ反論するカウンターナラティブ生成を扱った。書き換えには低ランク適応による効率的ファインチューニングを使う。一方、反論生成では対照的な隠れ活性から主成分分析でステアリング方向を抽出し、Gemma-3-4B-itの中間表現へ推論時に注入する。</p>
<p>重みを更新しない活性化ステアリングと制約付きプロンプトの組み合わせにより、書き換えは公式80.00%、反論生成は78.12%を得た。軽量に挙動を制御できる反面、手作業分析では意味のずれ、偏りの残存、注入層への感度、過剰な誘導、文章崩壊が失敗モードとして確認された。二つの点数は異なる課題の公式指標であり、直接比較はできない。実用上の価値は、パラメータ更新を伴うLoRAと推論時制御を同じシステムで比較し、軽量制御の限界まで報告した点にある。</p>
<hr />
<h2>参考ソース</h2>
<ul>
<li>論文1: Vatsal Baherwani, Tom Goldstein, Ashwinee Panda. Not All LLM Reasoning is Visible in the Chain-of-Thought. <a href="https://arxiv.org/abs/2607.22925">arXiv:2607.22925</a> (2026).</li>
<li>論文2: Soohyuk Jang et al. Learning When to Reason for Text-to-SQL via SFT and DPO. <a href="https://arxiv.org/abs/2607.22622">arXiv:2607.22622</a> (2026).</li>
<li>論文3: Haowen Li, Yoichi Ishibashi, Masafumi Oyamada. Evaluating the Impact of Reviewer Guideline Design on LLM-Based Automated Peer Review. <a href="https://arxiv.org/abs/2607.22553">arXiv:2607.22553</a> (2026).</li>
<li>論文4: Viktoriia Makovska, George Fletcher. Between Suppression and Collapse: Evaluating Narrative Unlearning with LENS. <a href="https://arxiv.org/abs/2607.22657">arXiv:2607.22657</a> (2026).</li>
<li>論文5: Swastika Kundu, Azizul Hakim Fayaz, Tashreef Muhammad. PatiGonit22K: A Comprehensive Dataset for Solving Complex Bengali MWPs. <a href="https://arxiv.org/abs/2607.22859">arXiv:2607.22859</a> (2026).</li>
<li>論文6: Jian Lu et al. Toward Automated Detection of Documentation Inconsistencies in Electronic Health Records. <a href="https://arxiv.org/abs/2607.22954">arXiv:2607.22954</a> (2026).</li>
<li>論文7: Xiaokun Wang et al. Beyond Direct Answering: Aligning Educational LLMs as Socratic Guides via Heuristic Reinforcement Learning. <a href="https://arxiv.org/abs/2607.22996">arXiv:2607.22996</a> (2026).</li>
<li>論文8: Ahmed Haj Ahmed, Alvin Grissom II. ADAGE: A Language-Agnostic Pipeline for Analogical Reasoning Evaluation. <a href="https://arxiv.org/abs/2607.23058">arXiv:2607.23058</a> (2026).</li>
<li>論文9: Yusuke Sakai, Natthawut Kertkeidkachorn, Kiyoaki Shirai. Attention-Guided Layer Selection for Contrastive Decoding in Large Language Models. <a href="https://arxiv.org/abs/2607.23067">arXiv:2607.23067</a> (2026).</li>
<li>論文10: Akhil Rajeev P, Manoj Balaji J. LoRA for Gender-Inclusive Rewriting and Activation Steering for Counter-Narrative Generation. <a href="https://arxiv.org/abs/2607.23083">arXiv:2607.23083</a> (2026).</li>
</ul>

</details>

---

[← 2026-07-29 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
