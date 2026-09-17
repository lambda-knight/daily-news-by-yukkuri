---
title: "AIが家を操作、Pixelゼロクリック攻撃と量子20億ドル投資 2026/09/17"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# AIが家を操作、Pixelゼロクリック攻撃と量子20億ドル投資 2026/09/17

**2026-09-17 / 生成AIニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-09-17-ai/ai_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-09-17-ai)

---

## 概要

AIエージェントが家庭機器を操作する時代の権限設計、安全評価者の独立性、カメラなし眼鏡、量子ウエハー製造、悪用中のPixel脆弱性を解説します。

▼ 今日のトピック
・Google Homeを操作するAIエージェント
・AnthropicとOpenAIの研究所内安全評価者
・Metaのカメラなしスマート眼鏡
・米政府とIBMの量子ウエハー製造投資
・PixelのCVE-2026-58704
・ScreenConnectのCVE-2026-84869

▼ 参考記事・ソース
・TechCrunch「Your AI agents can now control your Google Home devices」 https://techcrunch.com/2026/09/16/your-ai-agents-can-now-control-your-google-home-devices/
・TechCrunch「Anthropic and OpenAI want to embed safety evaluators」 https://techcrunch.com/2026/09/16/anthropic-and-openai-want-to-embed-safety-evaluators-will-they-really-be-independent/
・TechCrunch「Meta prepares to sell smart glasses without a camera」 https://techcrunch.com/2026/09/16/after-accusations-of-selling-perv-glasses-meta-prepares-to-sell-a-pair-without-a-camera/
・IBM Newsroom「Anderon finalizes $1 billion CHIPS award」 https://newsroom.ibm.com/2026-09-16-anderon,-an-ibm-company,-finalizes-agreement-with-the-u-s-department-of-commerce-for-a-1-billion-chips-award-to-accelerate-r-d-for-u-s-based-pure-play-quantum-foundry
・Google「Pixel Update Bulletin—September 2026」 https://source.android.com/docs/security/bulletin/pixel/2026-09-01
・ConnectWise「ScreenConnect 26.6.5 Security Patch」 https://www.connectwise.com/company/trust/security-bulletins/2026-09-08-screenconnect-bulletin

#生成AI #AI #量子コンピュータ #サイバーセキュリティ #ずんだもん #四国めたん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>生成AI・量子・セキュリティニュース（2026年9月17日）</h1>
<p><strong>キーワード:</strong> AIエージェント / スマートホーム / 独立安全評価 / 量子ウエハー / CVE-2026-58704 / CVE-2026-84869</p>
<h2>オープニング：2026年9月17日 — 生成AI・量子・セキュリティニュース</h2>
<ul>
<li>今日の焦点は、AIに家庭の鍵を渡す設計、安全評価者の独立性、量子チップの製造基盤、スマートフォンと遠隔管理ソフトの緊急更新です。</li>
<li>共通する問いは、強い権限を便利な仕組みに集めたとき、誰が監督し、事故時にどこで止められるかです。</li>
</ul>
<h2>生成AIと家庭：Google Homeを操作するエージェントの権限</h2>
<ul>
<li>Googleは9月16日、AIエージェントがGoogle Home機器を自然言語で操作できるMCPサーバーの早期アクセスを始めました。ClaudeやChatGPTなどから、接続機器の操作、カメラ要約、家庭内活動の参照を行える構想です。</li>
<li>MCPは、モデルと外部サービスを共通の手順で接続する規格です。照明の操作だけでなく、カメラや在宅状況へ接続範囲が広がると、誤指示や乗っ取られたアカウントの影響も物理空間へ及びます。</li>
<li>利便性の核心は、複数のアプリを開かず、目的だけ伝えて一連の操作を任せられることです。一方、エージェントには利用者、部屋、機器、時間帯ごとの最小権限と、実行前の確認、操作履歴が必要になります。</li>
<li>従来のスマートホームは利用者が機器を一つずつ選びました。今回はAIが意図を解釈して操作を組み立てるため、「何を頼んだか」と「実際に何が実行されたか」を分けて記録する設計が争点です。</li>
</ul>
<h2>生成AIの安全監督：研究所内の評価者は独立できるか</h2>
<ul>
<li>TechCrunchは9月16日、AnthropicとOpenAIが外部の安全評価者を研究所内へ受け入れ、開発中モデルへ継続的にアクセスさせる構想を報じました。</li>
<li>外部から完成版だけを試すより、訓練過程、内部評価、未公開能力へ触れられる点は前進です。しかし、研究所が資金、アクセス範囲、公開時期を握れば、不都合な結果を評価者が公表できるかという利益相反が残ります。</li>
<li>独立性を測る具体的な基準は、評価対象を企業だけが選ばないこと、否定的結果の公表権、資金源の開示、経営陣へ直接報告できる経路、規制当局が記録を検査できることです。</li>
<li>前日は大手三社が共通課題を話し合う動きを扱いました。今日は合意の有無ではなく、監督者が開発企業へ深く入るほど得られる情報と、同時に生じる依存を主視点にします。</li>
</ul>
<h2>生成AIとプライバシー：Metaがカメラなし眼鏡を準備</h2>
<ul>
<li>TechCrunchは9月16日、Metaがカメラを搭載しないスマート眼鏡を販売する準備を進めていると報じました。既存のカメラ付き製品には、周囲の人が撮影を認識しにくいとの批判が続いています。</li>
<li>カメラを外せば、無断撮影と顔画像収集の危険は小さくなります。ただし、音声入力、位置、利用履歴、クラウド処理が残るなら、プライバシー問題がすべて消えるわけではありません。</li>
<li>重要なのは、機能を追加してから通知表示で補うのではなく、最初からセンサーを減らす選択肢を商品として用意した点です。利用者は撮影機能を失う代わりに、周囲へ説明しやすい機器を選べます。</li>
<li>社会的受容は装着者だけで決まりません。撮られる側が拒否しにくい公共空間では、表示灯よりも「そもそも撮れない」という構造的な制約の方が強い保証になります。</li>
</ul>
<h2>量子コンピュータ：米政府とIBMが20億ドル規模の製造基盤</h2>
<ul>
<li>IBM子会社Anderonは9月16日、米商務省とCHIPS法に基づく10億ドルの研究開発助成を確定しました。IBMも追加で10億ドルを投じ、ニューヨーク州オールバニーで量子ウエハーの専業ファウンドリーを運営します。</li>
<li>工場は300ミリメートルのウエハーに対応し、超伝導量子ビット配列、量子入出力、読み出し信号系の部品を顧客企業向けに製造します。最初の量子ウエハーはすでに施設内の工程へ入ったと同社は説明しています。</li>
<li>前日の論文賞は量子計算を何に使い、どう評価するかが焦点でした。今回は、研究室ごとの試作から、複数企業が利用できる共通製造設備へ移せるかが主視点です。</li>
<li>助成決定は誤り耐性量子計算の完成を示しません。歩留まり、同一設計の再現性、量子ビットの品質、顧客への納期という半導体製造の指標が、量子ロードマップの実行力を左右します。</li>
</ul>
<h2>セキュリティ：PixelモデムのCVE-2026-58704</h2>
<ul>
<li>Googleは9月15日のPixel更新で、携帯回線用モデムのCVE-2026-58704を修正しました。深刻度はHighで、限定的かつ標的型の実攻撃が確認されています。</li>
<li>この脆弱性はアクセス制御の論理不備による権限昇格です。利用者がリンクを押したりファイルを開いたりしなくても悪用できるゼロクリック型で、モデムの隔離領域から端末の広いデータへ到達する恐れがあります。</li>
<li>Googleは攻撃主体と対象を公表していません。したがって一般利用者への無差別攻撃とまでは言えませんが、標的型攻撃では操作の有無だけで安全を判断できません。</li>
<li>対象のPixel利用者は2026年9月5日以降のセキュリティパッチレベルへ更新します。通信を担う基盤部品の欠陥なので、不審なリンクを避けるだけでは代替策になりません。</li>
</ul>
<h2>セキュリティ：ScreenConnectのCVE-2026-84869</h2>
<ul>
<li>ConnectWiseは9月8日、遠隔管理ソフトScreenConnectのCVE-2026-84869を公開しました。CVSSは9.9で、26.6.5未満のクラウド版とオンプレミス版のクライアントが影響を受けます。</li>
<li>権限の低い攻撃者でも、進行中の遠隔セッションでホスト側の承認なしにファイルを転送・実行できる場合があります。管理ソフトは多数の端末へ正規の操作権限を持つため、一つの弱点が組織内の横展開に結びつきます。</li>
<li>修正版は26.6.5です。クラウド環境は自動更新済みですが、オンプレミス環境は管理者が更新し、ホストクライアントとアクセスエージェントも入れ直します。</li>
<li>すぐ更新できない場合、全役割からTransferFiles権限を外す暫定策があります。ただし更新の代替ではありません。利用者、役割、監査ログを見直し、未知のアカウントがあれば認証情報も変更します。</li>
</ul>
<h2>まとめ：便利な接続ほど停止点を設計する</h2>
<ul>
<li>AIエージェントは家庭機器、評価者は研究所内部、量子ファウンドリーは複数企業、遠隔管理ソフトは多数端末へ接続します。</li>
<li>接続が価値を生む一方、権限の集中は誤操作、利益相反、供給遅延、侵入の影響も広げます。</li>
<li>今日の結論は、接続を増やすだけでなく、最小権限、独立した公表権、製造指標、迅速な更新という停止点を同時に設計する必要があるということです。</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://techcrunch.com/2026/09/16/your-ai-agents-can-now-control-your-google-home-devices/">TechCrunch: Your AI agents can now control your Google Home devices</a></li>
<li><a href="https://techcrunch.com/2026/09/16/anthropic-and-openai-want-to-embed-safety-evaluators-will-they-really-be-independent/">TechCrunch: Anthropic and OpenAI want to embed safety evaluators</a></li>
<li><a href="https://techcrunch.com/2026/09/16/after-accusations-of-selling-perv-glasses-meta-prepares-to-sell-a-pair-without-a-camera/">TechCrunch: Meta prepares to sell smart glasses without a camera</a></li>
<li><a href="https://newsroom.ibm.com/2026-09-16-anderon,-an-ibm-company,-finalizes-agreement-with-the-u-s-department-of-commerce-for-a-1-billion-chips-award-to-accelerate-r-d-for-u-s-based-pure-play-quantum-foundry">IBM Newsroom: Anderon finalizes $1 billion CHIPS award</a></li>
<li><a href="https://source.android.com/docs/security/bulletin/pixel/2026-09-01">Google: Pixel Update Bulletin—September 2026</a></li>
<li><a href="https://techcrunch.com/2026/09/16/google-says-some-pixel-phone-owners-were-hacked-in-zero-day-attacks/">TechCrunch: Google says some Pixel owners were hacked in zero-day attacks</a></li>
<li><a href="https://www.connectwise.com/company/trust/security-bulletins/2026-09-08-screenconnect-bulletin">ConnectWise: ScreenConnect 26.6.5 Security Patch</a></li>
</ul>

</details>

---

[← 2026-09-17 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
