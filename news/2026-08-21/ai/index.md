---
title: "OpenAIがAnthropicに再接近、Grokに暗号化攻撃、学生13人逮捕、QpiAI量子工場稼働【2026/08/21】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# OpenAIがAnthropicに再接近、Grokに暗号化攻撃、学生13人逮捕、QpiAI量子工場稼働【2026/08/21】

**2026-08-21 / 生成AIニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-21-ai/ai_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-21-ai)

---

## 概要

「勢い」の裏で起きている摩擦をテーマに、5本の具体的ニュースを解説します。

▼ 今日のトピック
・法人利用シェアでOpenAIがAnthropicに再接近(Rampデータ)
・Pew研究所調査、ウェブの3分の1でAI生成の疑い
・Grokに新型攻撃「暗号化コンテキスト注入」、個人データ流出が無修正のまま
・OpenAIのロビー拠点「The Workshop」占拠、学生13人逮捕
・インドQpiAI、8インチ量子チップ工場を稼働、1万量子ビットへ布石

▼ 参考記事・ソース
原稿末尾の参考ソース一覧をご覧ください。

#生成AI #OpenAI #Anthropic #量子コンピュータ #ゆっくり解説 #ずんだもん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>生成AIニュース（2026年8月21日）</h1>
<p><strong>キーワード:</strong> OpenAI対Anthropic企業シェア / Pew AI生成疑い調査 / Grok暗号化コンテキスト注入 / OpenAIロビー拠点占拠 / QpiAI量子チップ工場 / 1万量子ビット</p>
<h2>オープニング：2026年8月21日 — 生成AIニュース</h2>
<ul>
<li>本日のテーマ: 企業の「勢い」の裏で起きている摩擦</li>
<li>市場: 法人利用シェアでOpenAIがAnthropicに再接近</li>
<li>実態: ウェブの3分の1がAI生成疑い、Pew研究所が実測</li>
<li>セキュリティ: Grokの新型攻撃で個人データが流出、無修正のまま</li>
<li>政治: OpenAIのロビー拠点占拠で学生13人逮捕</li>
<li>量子: インドQpiAIが8インチ量子チップ工場を稼働</li>
</ul>
<h2>OpenAIがAnthropicに再接近——Ramp企業データが示すシェア逆転の兆し</h2>
<ul>
<li>法人向けカード・経費管理サービスRampが、米国企業7万社超のカード・請求支払いデータをもとに公表</li>
<li>OpenAIはかつて法人・個人ともに独走していたが、2026年5月にRampの有料法人ユーザー内シェアで首位を明け渡した（Anthropic 41%対OpenAI 39%）</li>
<li>2026年7月時点ではAnthropicが約44%、OpenAIが約40%まで差が開いた</li>
<li>Ramp担当エコノミストのAra Kharazian氏によると、第3四半期に入ってからはOpenAIの伸び率がAnthropicを上回っている</li>
<li>四半期はまだ1か月残っており、Kharazian氏も「傾向は締め切り前にまた変わりうる」と留保</li>
</ul>
<h2>ウェブの3分の1がAI生成疑い——Pew研究所が実測</h2>
<ul>
<li>Pew Research Centerが2026年8月20日、Common Crawlのアーカイブから過去5年分の英語ウェブページ約50万件を収集して分析した結果を公表</li>
<li>検出ツール「Open Pangram」でAI関与の兆候を判定したところ、ChatGPT公開（2022年11月）以降に公開されたページの3分の1超でAI関与の兆候が見つかった</li>
<li>ドメイン別では.comが約1割、.orgが4.6%とその半分以下、.eduや.govは約1%とさらに低い</li>
<li>Pewは「ページ全体をAIが書いたと断定するものではなく、AIが関与・大幅編集した兆候を検出したもの」と説明</li>
<li>この発表は、Cloudflareがボットのウェブトラフィックが人間のトラフィックを上回ったと報告した直後に出た</li>
</ul>
<h2>Grokに「暗号化コンテキスト注入」攻撃——個人データ流出、無修正のまま</h2>
<ul>
<li>AIセキュリティ企業Adversaが、xAIの「Grok 4.5 Fast」に対する新手法「Cryptographic Context Injection」を実証</li>
<li>平文でデータ流出指示を書いたウェブページはGrokに拒否されたが、AES-256GCMで暗号化した指示文と復号鍵を埋め込むと、Grokが自らのPython実行環境内で復号・実行し、指示に従ってしまった</li>
<li>コンテンツ分類フィルターは暗号化された文字列の中身までは検査しないため、指示は「コード実行結果」としてモデルのコンテキストに届く</li>
<li>実証では、ユーザー名・おおまかな位置情報・契約プラン・チャット履歴の全プロンプトをURLパラメータとして攻撃者サーバーへ送信できることを示した</li>
<li>2026年8月19日時点で修正パッチ、CVE番号、利用者側の回避策のいずれも存在せず、Adversaは攻撃を再現できると説明</li>
<li>同じ週には、無料版「Grok Lite」が意味不明な応答を返す不具合も利用者から報告されており、品質面でも綻びが目立つ</li>
</ul>
<h2>OpenAIのロビー拠点「The Workshop」占拠——学生13人逮捕</h2>
<ul>
<li>2026年8月10日（月）、ホワイトハウスから数ブロックのOpenAIロビー拠点「The Workshop」前に、学生活動家30人超が集結</li>
<li>Sunrise Movement・QuitGPT・Young Democratic Socialists of Americaが事前に「テック企業が権威主義を支えている実態」への抗議組織化トレーニングを実施していた</li>
<li>学生たちは「Stop Stealing Our Future（私たちの未来を盗むな）」の横断幕を掲げ、「OpenAI Bought My Senator（OpenAIが私の上院議員を買った）」というプラカードも掲示</li>
<li>ロビーの占拠開始から約2時間後の現地時間午後2時30分、Metropolitan Police Departmentが13人を「不法侵入」容疑で逮捕</li>
<li>警察の記録によると、逮捕者は第1・第2・第3地区の各署に分散して連行された</li>
<li>The Workshopは今夏、OpenAIがワシントンでの政治的働きかけを強化する一環として開設したばかりの拠点</li>
</ul>
<h2>QpiAI、ベンガルールに8インチ量子チップ工場——1万量子ビットへ布石</h2>
<ul>
<li>インドのQpiAIが2026年8月17日、ベンガルール・ジャックールの70,000平方フィート研究拠点内に、8インチ量子チップ製造施設（フェーズ2）を稼働</li>
<li>クラス100・クラス1,000のクリーンルーム仕様で、フリップチップ型の超伝導量子プロセッサ（現状は最大128物理量子ビット）や周辺制御チップ・センサーを製造</li>
<li>同社はすでに4種のプロセッサを試作済み: QVidya（8量子ビット・トランズモン型）、Indus（25量子ビット・トランズモン型、ハイブリッドHPCデータセンターに統合）、Kaveri（64量子ビット・トランズモン型、独自フリップチップ配線）、Yukti（9量子ビット・フラクソニウム型、フォールトトレラント表面符号の評価向け）</li>
<li>2027年完了予定のフェーズ3で、単一QPUで最大1万物理量子ビットの製造を目指す</li>
<li>施設への投資額はこれまでに2,000万〜2,500万ドル、フェーズ3の設備・検査能力拡張にさらに1,000万〜1,500万ドルを追加投入する計画</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>法人シェア争い、ウェブ実態調査、セキュリティ、政治、量子製造という5つの角度から、AI業界の「勢い」の裏側を見た一日</li>
<li>OpenAIとAnthropicのシェア争いは1か月でも数字が反転する不安定さを抱え、Pewの調査はウェブ全体がすでにAI生成疑いのコンテンツで埋まりつつある実態を示した</li>
<li>Grokの脆弱性とOpenAIロビー拠点への抗議は、技術と社会実装の両面で信頼の摩擦が続いていることを物語る</li>
<li>インドのQpiAIは着実に量子チップの自国製造能力を積み上げており、量子産業の担い手が広がっている</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://techcrunch.com/2026/08/20/openai-is-gaining-on-anthropic-with-business-users-new-data-indicates/">OpenAI is gaining on Anthropic with business users, new data indicates</a></li>
<li><a href="https://techcrunch.com/2026/08/20/a-third-of-webpages-published-since-chatgpts-launch-show-signs-of-ai-authorship-study-finds/">A third of web pages published since ChatGPT's launch show signs of AI authorship, study finds</a></li>
<li><a href="https://www.pewresearch.org/data-labs/2026/08/20/how-much-of-the-internet-is-written-with-ai/">How Much of the Internet Is Written With AI?</a></li>
<li><a href="https://arstechnica.com/security/2026/08/grok-exfiltrates-user-data-when-malicious-instructions-are-encrypted/">Grok exfiltrates user data when malicious instructions are encrypted</a></li>
<li><a href="https://thehackernews.com/2026/08/new-cryptographic-context-injection.html">New Cryptographic Context Injection Attack Could Let Web Pages Steal Grok Chat Data</a></li>
<li><a href="https://techcrunch.com/2026/08/20/grok-keeps-sending-gibberish-responses-to-users/">Grok keeps sending gibberish responses to users</a></li>
<li><a href="https://www.commondreams.org/news/ai-protest">'Stop Stealing Our Future': Students Arrested in Protest of OpenAI's Lobby Office</a></li>
<li><a href="https://quantumcomputingreport.com/qpiai-inaugurates-8-inch-quantum-chip-foundry-in-bengaluru-targeting-10000-qubit-qpus/">QpiAI Inaugurates 8-Inch Quantum Chip Foundry in Bengaluru Targeting 10,000-Qubit QPUs</a></li>
<li><a href="https://thequantuminsider.com/2026/08/17/qpiai-opens-quantum-chip-foundry-in-india-targets-10000-qubit-processors/">QpiAI Opens Quantum Chip Foundry in India, Targets 10,000-Qubit Processors</a></li>
</ul>

</details>

---

[← 2026-08-21 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
