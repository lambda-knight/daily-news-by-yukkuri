---
title: "AI監査法と256量子ビット量産、Microsoft974件修正 2026/09/14"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# AI監査法と256量子ビット量産、Microsoft974件修正 2026/09/14

**2026-09-14 / 生成AIニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-09-14-ai/ai_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-09-14-ai)

---

## 概要

AI安全が米国の選挙争点と州法へ。量子計算機の量産設計、Microsoft史上最大規模の月例修正まで、性能の先にある監査・製造・配備を解説します。

▼ 今日のトピック
・オバマ氏が民主党へAI安全と雇用対策の具体化を要求
・カリフォルニア州が独立AI評価・監査人制度を法制化
・IonQが256量子ビットのSuperion 256を発表
・Microsoftが974件を修正、悪用確認済みCVEを優先

▼ 参考記事・ソース
・AP「Trump downplays the need to check AI development」 https://apnews.com/article/9df0ebb4c1b0619aa0f88057b5a1092d
・California Governor「Independent AI assessment and auditor laws」 https://www.gov.ca.gov/2026/09/09/governor-newsom-signs-first-in-the-nation-ai-safeguards-to-protect-californians-calls-on-the-federal-government-to-do-its-part/
・OpenAI「The AI policy window is open」 https://openai.com/index/ai-policy-window/
・IonQ「IonQ debuts Superion 256」 https://www.ionq.com/news/ionq-launches-superion-product-line-industry-leading-upgradeable-platform-designed-to-scale-manufacturable-fault-tolerant-quantum-computing
・Microsoft「2026年9月のセキュリティ更新プログラム」 https://www.microsoft.com/en-us/msrc/blog/2026/09/202609-security-update
・Krebs on Security「Microsoft Plugs Nearly 1,000 Security Holes」 https://krebsonsecurity.com/2026/09/microsoft-plugs-nearly-1000-security-holes/

#生成AI #AI #量子コンピュータ #サイバーセキュリティ #ずんだもん #四国めたん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>生成AI・量子・セキュリティニュース（2026年9月14日）</h1>
<p><strong>キーワード:</strong> AI安全規制 / カリフォルニア州法 / Superion 256 / 量産型量子計算機 / Patch Tuesday / CVE-2026-85880</p>
<h2>オープニング：2026年9月14日 — 生成AI・量子・セキュリティニュース</h2>
<ul>
<li>2026年9月14日、生成AI、量子コンピュータ、セキュリティの最新動向をまとめる。</li>
<li>AIでは、米国で安全規制が選挙争点になり、カリフォルニア州が独立評価と監査人の制度を先に法制化した。</li>
<li>量子ではIonQが256量子ビット機を「一台ずつ作る装置」から「数百台作る製品」へ変える構想を発表。セキュリティではMicrosoftが過去最大規模の974件を修正した。</li>
</ul>
<h2>生成AIと政治：オバマ氏が民主党に具体策を要求</h2>
<ul>
<li>APは9月13日、バラク・オバマ元大統領が民主党にAIを中心的な政策課題とし、安全、子ども、雇用への具体策を示すよう促したと報じた。</li>
<li>同じ報道でドナルド・トランプ大統領は、開発速度を抑えれば中国へ優位を譲るとして、業界の警告に距離を置いた。争点は「規制か無規制か」より、競争力を損なわず被害へ備える制度の速度である。</li>
<li>オバマ氏は雇用代替がどこへ集中し、政府がどう応じるかを具体的に考えるべきだとした。抽象的な破滅論ではなく、職種・地域・所得層ごとの移行支援が政策の試金石になる。</li>
<li>前日は企業自身による能力開発のペース調整を扱った。本日は、その提案を選挙、公的規制、対中競争へ接続する政治側の応答が新しい主視点である。</li>
</ul>
<h2>生成AI規制：カリフォルニア州が独立評価を制度化</h2>
<ul>
<li>ギャビン・ニューサム知事は9月9日、SB 813とAB 1405に署名した。前者はAIシステムを州法に照らして評価する独立検証組織の枠組み、後者はAI監査人の登録と独立性・透明性・誠実性の基準を設ける。</li>
<li>OpenAIは同日、この2法に加え、未成年向けコンパニオン・チャットボットの年齢確認、リスク評価、独立監査、保護者機能を求めるSB 1119など計4法案への支持を公表した。</li>
<li>SB 1119は9月10日に署名された。企業の自主的な安全評価だけでなく、評価する側の利益相反と資格まで制度の対象にした点が重要である。</li>
<li>一方、州ごとに基準が違えば開発者の負担は増える。OpenAIも連邦レベルの能力基準型規制を優先するとしつつ、連邦議会が動くまで州法を支持する立場を示した。</li>
</ul>
<h2>量子コンピュータ：IonQがSuperion 256を量産設計へ</h2>
<ul>
<li>IonQは9月8日、第6世代のトラップドイオン型量子計算基盤「Superion 256」を発表した。子会社SkyWaterで256量子ビットの統合チップを初めて製造し、試作機でイオンを捕捉した段階である。</li>
<li>受注は開始済みで、顧客への納入目標は2027年。256量子ビット機が完成して性能試験を終えたという発表ではなく、チップ製造と試作の工程が進んだという発表である。</li>
<li>従来のレーザー中心の制御から、チップ上の電子回路でイオンを制御するEQCへ移す。標準的な半導体工程、一般的なサーバーラック、通常のデータセンター冷却へ寄せ、数百台規模での生産を狙う。</li>
<li>前日のスイス拠点は誰が量子装置へアクセスするかが主題だった。本日の焦点は、研究設備を反復製造できる工業製品へ変えられるかである。量子ビット数だけでなく、ゲート忠実度、稼働率、納期、同一品質での製造が成否を決める。</li>
</ul>
<h2>セキュリティ：Microsoftが974件を一括修正</h2>
<ul>
<li>Microsoftは9月8日、Windows 11、Windows Server、Officeなどの月例セキュリティ更新を公開した。Krebs on SecurityはMicrosoft製品の修正が974件に達し、同社史上最大の単月バッチだと報じた。</li>
<li>実際の悪用が確認されたCVE-2026-81963とCVE-2026-85880はいずれもCVSS 7.8。標準利用者として端末へ入った攻撃者がSYSTEM権限へ昇格できるローカル攻撃で、初期侵入後の被害拡大に使われる。</li>
<li>CVE-2026-85880はWindowsのALPCにあるヒープ領域のバッファーオーバーフローで、Windows 10の複数版とWindows Server 2012から2022などが影響を受ける。該当する9月更新を適用すれば修正される。</li>
<li>さらにWindows DHCP ServerのCVE-2026-69845はCVSS 9.8。認証も利用者操作もなくネットワーク越しにコードを実行できる可能性があり、DHCP役割を持つサーバーでは更新の優先度が高い。</li>
<li>974という総数だけで一律に緊急度を決めると運用が詰まる。悪用実績、外部公開の有無、権限、資産の重要度で優先順位を付け、検証後に配備する人手がボトルネックになる。</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>AIでは、企業の警告が選挙論と州法へ移り、評価する組織の独立性まで制度化された。</li>
<li>IonQの発表は、量子計算機の競争軸を最大量子ビット数だけでなく、製造工程、設置条件、納入能力へ広げた。</li>
<li>Microsoftの大型更新は、AIによる発見速度が上がっても、組織の試験と配備は人と資産管理に依存するという非対称を映す。</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://apnews.com/article/9df0ebb4c1b0619aa0f88057b5a1092d">AP: Trump downplays the need to check AI development</a></li>
<li><a href="https://www.gov.ca.gov/2026/09/09/governor-newsom-signs-first-in-the-nation-ai-safeguards-to-protect-californians-calls-on-the-federal-government-to-do-its-part/">California Governor: Independent AI assessment and auditor laws</a></li>
<li><a href="https://www.gov.ca.gov/2026/09/10/governor-newsom-signs-the-strongest-child-safety-chatbot-and-social-media-laws-in-the-nation/">California Governor: Child safety chatbot laws</a></li>
<li><a href="https://openai.com/index/ai-policy-window/">OpenAI: The AI policy window is open</a></li>
<li><a href="https://www.ionq.com/news/ionq-launches-superion-product-line-industry-leading-upgradeable-platform-designed-to-scale-manufacturable-fault-tolerant-quantum-computing">IonQ: IonQ debuts Superion 256</a></li>
<li><a href="https://www.microsoft.com/en-us/msrc/blog/2026/09/202609-security-update">Microsoft: 2026年9月のセキュリティ更新プログラム</a></li>
<li><a href="https://krebsonsecurity.com/2026/09/microsoft-plugs-nearly-1000-security-holes/">Krebs on Security: Microsoft Plugs Nearly 1,000 Security Holes</a></li>
<li><a href="https://nvd.nist.gov/vuln/detail/CVE-2026-85880">NVD: CVE-2026-85880</a></li>
<li><a href="https://nvd.nist.gov/vuln/detail/CVE-2026-69845">NVD: CVE-2026-69845</a></li>
</ul>

</details>

---

[← 2026-09-14 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
