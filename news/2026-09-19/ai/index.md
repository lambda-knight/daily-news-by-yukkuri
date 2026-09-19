---
title: "【速報】AIハルシネーションが米軍作戦を止めかけた ほか今週のAI業界まとめ 2026/09/19"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# 【速報】AIハルシネーションが米軍作戦を止めかけた ほか今週のAI業界まとめ 2026/09/19

**2026-09-19 / 生成AIニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-09-19-ai/ai_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-09-19-ai)

---

## 概要

生成AI・量子コンピュータ・セキュリティの最新動向をまとめてお届けします。AIが捏造した情報が米軍の作戦寸前まで進んだ事例、米連邦官報サイトが中国製Qwenを使っていた矛盾、ClaudeがOpenAIへの侵入に使われた一件、米エネルギー省の量子コンピュータ新競争、そしてAI基盤とネットワーク機器の最高深刻度脆弱性2件を解説します。

▼ 今日のトピック
・生成AIと軍事：ハルシネーションが米国の対中作戦を止めかけた
・生成AIと政治：米連邦官報サイトが中国製Qwenを検索に使っていた
・生成AIとセキュリティ：ClaudeがOpenAIへの侵入に使われ、報奨金を獲得
・量子コンピュータ：米エネルギー省が2億1500万ドルの「量子ジェネシスQ」競争を開始
・セキュリティ：Azure AI Foundryに認証不要のCVSS10.0脆弱性
・セキュリティ：NetScalerのSAML脆弱性、実攻撃で悪用され連邦機関に是正命令

▼ 参考記事・ソース
・TechCrunch「AI hallucination nearly triggers US military operation」 https://techcrunch.com/2026/09/18/ai-hallucination-nearly-triggers-us-military-operation/
・TechCrunch「US government website used AI search tool from China that FBI said copied Anthropic」 https://techcrunch.com/2026/09/18/us-government-website-used-ai-search-tool-from-china-that-fbi-said-copied-anthropic/
・TechCrunch「Researchers used Anthropic's Claude to hack into OpenAI」 https://techcrunch.com/2026/09/18/researchers-used-anthropics-claude-to-hack-into-openai/
・Department of Energy「DOE Launches Competition to Accelerate Development of World's First Fault-Tolerant Quantum Computer」 https://www.energy.gov/science/articles/doe-launches-competition-accelerate-development-worlds-first-fault-tolerant
・The Hacker News「Microsoft Patches CVSS 10.0 Azure AI Foundry Flaw Enabling Unauthorized Privilege Escalation」 https://thehackernews.com/2026/09/microsoft-patches-cvss-100-azure-ai.html
・Bishop Fox「No Crash Required: Verifying the Citrix NetScaler SAML Patch for CVE-2026-8452」 https://bishopfox.com/blog/no-crash-required-verifying-the-citrix-netscaler-saml-patch-for-cve-2026-8452

#生成AI #ChatGPT #Claude #LLM #AI #人工知能 #ゆっくり解説 #ずんだもん #四国めたん #OpenAI #Anthropic #量子コンピュータ #サイバーセキュリティ #AIニュース

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>生成AI・量子・セキュリティニュース（2026年9月19日）</h1>
<p><strong>キーワード:</strong> AIハルシネーション誤爆未遂 / Qwen連邦官報サイト問題 / Claude対OpenAI侵入 / DOE量子ジェネシスQ / Azure AI Foundry認証不備 / NetScaler SAML脆弱性</p>
<h2>オープニング：2026年9月19日 — 生成AI・量子・セキュリティニュース</h2>
<ul>
<li>今日の焦点は、AIが捏造した情報が米軍の作戦寸前まで進んだ事例、米連邦政府サイトが中国製AIを使っていた矛盾、AI同士が攻防を演じたバグ報奨金、量子コンピュータへ2億ドル超を投じる米エネルギー省の新競争、そしてAI基盤とネットワーク機器を狙う最高深刻度の脆弱性2件です。</li>
<li>共通する問いは、AIとその周辺インフラを人間がどこまで信頼し、どこで検証の手を止めないかです。</li>
</ul>
<h2>生成AIと軍事：ハルシネーションが米国の対中作戦を止めかけた</h2>
<ul>
<li>今年春のイラン情勢の緊張下で、米特殊作戦軍の分析官がAIチャットボットに照会した結果、ある船舶の積み荷目録が核兵器計画の部品を含むと誤って報告され、この情報をもとに対中国の作戦が計画されました。軍用機がすでに出撃した段階で、情報の裏付けが取れていないことに分析官本人が気づき、作戦は土壇場で中止されました。</li>
<li>誤情報は、公開情報と機密の信号情報をAIが統合し、公式文書のような体裁で要約を作成したことで生まれ、指揮系統を通じて広まりました。どのAIモデルが使われたかは公表されていません。</li>
<li>GovAIの研究者で元陸軍将校のジェイク・ステックラー氏は「兵士がLLMに内在する不確実性を理解することが重要だ」と指摘し、導入速度を安全対策より優先すれば、現場のAIへの信頼そのものが損なわれかねないと警告しています。</li>
<li>今回は分析官個人の気づきで止まりましたが、機密情報と生成AIの出力が同じ「公式文書」の体裁で流通する仕組み自体に、検証を素通りしやすい構造上の弱点があります。</li>
</ul>
<h2>生成AIと政治：米連邦官報サイトが中国製Qwenを検索に使っていた</h2>
<ul>
<li>米国立公文書館が運営する連邦官報（Federal Register）のウェブサイトで、規則案を検索する機能の一つに中国アリババの「Qwen」モデルが使われていたことが判明しました。このAI検索は水曜日まで他の検索オプションと並んで提供されていましたが、SNSで指摘が広がったのとほぼ同じタイミングで停止されました。</li>
<li>FBIは先週、アリババがアンソロピックのモデルを「産業規模」で不正コピーしていると非難し、米中首脳会談を控えて緊張が高まっていた最中でした。今回の一件は、米政府自身がその翌週に当の中国製モデルを政府サイトで使っていたことになります。</li>
<li>AI専門家は、この利用自体が直接の安全保障上のリスクを生んだとは限らないとしつつ、政府が発する対中警戒のメッセージと現場の調達判断が食い違っていた点を問題視しています。</li>
<li>規制する側と使う側が同じ組織内で分裂している構図は、AIモデルの出自をどう調達基準に反映させるかという、実務レベルの未整備を映し出しています。</li>
</ul>
<h2>生成AIとセキュリティ：ClaudeがOpenAIへの侵入に使われ、報奨金を獲得</h2>
<ul>
<li>セキュリティ企業ハクトロンAIの3人組研究チームが、OpenAIのバグ報奨金プログラムの一環として、アンソロピックのClaudeに攻撃コードを生成させ、2つの重大な脆弱性を連鎖させてOpenAI従業員の複数のChatGPTアカウントへ侵入し、そこから社内のリポジトリにまで到達しました。発見から到達まで72時間以内という短さです。</li>
<li>当初はClaudeに攻撃を試みさせても失敗しましたが、アンソロピックが上位モデル「Opus 5」を投入した翌日に攻撃が成功しました。OpenAIはこの脆弱性を修正済みで、研究チームには6500ドルの報奨金が支払われています。</li>
<li>攻撃に使われたOpus 5自体には輸出規制上の制限がかかっていない一方、さらに新しい「Mythos 5」はハッキング能力への懸念から一時的に利用が制限されていました。同じ企業の中でもモデルごとに扱いが分かれている点が、能力向上のスピードに管理体制が追いついていない現状を示しています。</li>
<li>ライバル企業のAIモデルを攻撃道具として使い、別のライバル企業の防御を突破するという構図は、AI企業同士の競争が同時にセキュリティ検証の役割も担い始めていることを示します。</li>
</ul>
<h2>量子コンピュータ：米エネルギー省が2億1500万ドルの「量子ジェネシスQ」競争を開始</h2>
<ul>
<li>米エネルギー省は9月17日、「フォールトトレラントで科学的に意義のある量子コンピュータ」を2028年までに実現することを目指す競争的資金制度「量子ジェネシスQ・コンピティション」を発表しました。総額は最大2億1500万ドルで、2026会計年度分は250万ドル、残りは議会承認待ちです。</li>
<li>応募条件は、少なくとも100個の論理量子ビットを持ち、数億回規模のフォールトトレラント演算を実行できるシステムであることです。150個・200個の論理量子ビットに到達した場合には、それぞれ5000万ドルずつのボーナス資金枠が別途用意されています。</li>
<li>フェーズ1では採択者ごとに最大150万ドル、フェーズ2では100個以上の論理量子ビット達成に対して1億ドルの共通資金枠が割り当てられます。応募できるのは民間企業に限られ、説明会は9月25日、応募締め切りは10月19日です。</li>
<li>併設策として、国立研究所向けに4500万ドル規模の「量子ハイパフォーマンスコンピューティング検証・実証テストベッド」の公募も同時に始まりました。実機の論理量子ビット数という具体的な数値目標を掲げた点で、これまでの基礎研究支援とは一線を画す取り組みです。</li>
</ul>
<h2>セキュリティ：Azure AI Foundryに認証不要のCVSS10.0脆弱性</h2>
<ul>
<li>マイクロソフトは9月18日、企業向け生成AI開発基盤「Azure AI Foundry」に存在した脆弱性CVE-2026-85889を公表しました。CVSSスコアは最高値の10.0です。重要な機能への認証チェックが欠落しており、攻撃者は有効な認証情報を持たずにネットワーク経由で権限を昇格できる状態でした。</li>
<li>発見者はセキュリティ研究者のレミー・マロ氏です。マイクロソフトは実際の悪用は確認されていないと説明し、クラウド側のサービスであるため既にサーバー側で修正済みで、利用者側の対応は不要としています。</li>
<li>生成AIの開発・運用基盤そのものに認証の抜け穴があったという点で、モデルの安全性以前にインフラの基本的な認証設計が問われた事例です。AI基盤の急速な機能拡張が、こうした基本的な抜け漏れを生みやすい土壌になっていないか、今後の点検対象になります。</li>
</ul>
<h2>セキュリティ：NetScalerのSAML脆弱性、実攻撃で悪用され連邦機関に是正命令</h2>
<ul>
<li>シトリックスのNetScaler ADCおよびNetScaler Gatewayに存在するメモリ破損の脆弱性CVE-2026-8452は、シングルサインオン用のSAMLメッセージを解析する処理にあるヒープオーバーフローです。GatewayまたはAAA仮想サーバーとしてSAML認証を設定した機器に対し、細工した1本のHTTPリクエストを送るだけで、全通信を扱うプロセスのメモリが破壊され、遠隔コード実行につながる恐れがあります。</li>
<li>脆弱性自体は6月30日に公表されていましたが、8月14日にセキュリティ企業ウォッチタワー・ラボが、単なるクラッシュではなく実際にコード実行へつながる仕組みを実証する詳細を公開しました。これを受けて米CISAは8月26日に既知悪用脆弱性カタログへ追加し、拘束力のある命令に基づき連邦機関へ8月29日までの是正を義務付けています。</li>
<li>SSL VPNやICAプロキシなど、外部からアクセスできる形でGatewayを構成している機器が対象です。パッチ公開から実際の悪用実証、連邦命令までの流れは、脆弱性情報が公開された後こそ標的にされやすいという、パッチ適用を先延ばしにする組織へのリスクを改めて示しています。</li>
</ul>
<h2>まとめ：検証の空白を突かれるのはAIもネットワーク機器も同じ</h2>
<ul>
<li>米軍の作戦は分析官個人の気づきで止まり、米政府サイトの矛盾はSNSの指摘で発覚し、AI基盤とネットワーク機器の脆弱性はどちらも「認証されているはず」という前提の穴を突かれました。</li>
<li>どの事例も、仕組みが正式な体裁や既存の信頼を装っていたために、通常の点検をすり抜けていた点が共通しています。</li>
<li>今日の結論は、AIが作る情報にも、AIを支えるインフラにも、体裁の正しさとは別の検証経路を常に残しておく必要があるということです。</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://techcrunch.com/2026/09/18/ai-hallucination-nearly-triggers-us-military-operation/">TechCrunch: AI hallucination nearly triggers US military operation</a></li>
<li><a href="https://techcrunch.com/2026/09/18/us-government-website-used-ai-search-tool-from-china-that-fbi-said-copied-anthropic/">TechCrunch: US government website used AI search tool from China that FBI said copied Anthropic</a></li>
<li><a href="https://techcrunch.com/2026/09/18/researchers-used-anthropics-claude-to-hack-into-openai/">TechCrunch: Researchers used Anthropic's Claude to hack into OpenAI</a></li>
<li><a href="https://www.energy.gov/science/articles/doe-launches-competition-accelerate-development-worlds-first-fault-tolerant">Department of Energy: DOE Launches Competition to Accelerate Development of World's First Fault-Tolerant Quantum Computer</a></li>
<li><a href="https://thehackernews.com/2026/09/microsoft-patches-cvss-100-azure-ai.html">The Hacker News: Microsoft Patches CVSS 10.0 Azure AI Foundry Flaw Enabling Unauthorized Privilege Escalation</a></li>
<li><a href="https://bishopfox.com/blog/no-crash-required-verifying-the-citrix-netscaler-saml-patch-for-cve-2026-8452">The Register: No Crash Required — Verifying the Citrix NetScaler SAML Patch for CVE-2026-8452</a></li>
</ul>

</details>

---

[← 2026-09-19 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
