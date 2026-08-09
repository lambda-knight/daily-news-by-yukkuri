---
title: "医療委託先380万人流出、ビデオ会議ソフトに裏口【2026/08/10】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# 医療委託先380万人流出、ビデオ会議ソフトに裏口【2026/08/10】

**2026-08-10 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-10-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-10-security)

---

## 概要

医療ソフト委託先Unlimited Technology Systemsから380万人分の情報が流出した話、ビデオ会議ソフト「TrueConf」のインストーラーが改ざんされバックドアが仕込まれた話、CISAが実際の悪用を確認したKemp LoadMasterの脆弱性、Outlook・Gmailなど6大ウェブメールを横断するCSS攻撃、LGがスマートテレビの不正転用を禁止した動き、米国土安全保障省とデモ参加者のSignalチャットを巡る訴訟、AIハッキングの実態研究まで7件を解説します。

▼ 今日のトピック
・医療ソフト委託先「Unlimited Technology Systems」から380万人分流出
・ビデオ会議ソフト「TrueConf」のインストーラーが改ざんされバックドア配布
・CISA、Kemp LoadMasterの脆弱性を悪用確認済みリストに追加(792件の攻撃試行)
・Outlook・Gmailなど6大ウェブメールを横断するCSS攻撃
・LG、スマートテレビアプリの住宅プロキシ転用を禁止へ
・米国土安全保障省、デモ参加者のSignalチャットログ提出を要求
・「AIハッキングの最も危険な手口」も結局は人間の判断が要る

▼ 参考記事・ソース
・Bleeping Computer「Unlimited Technology Systems breach impacts 3.8 million people」 https://www.bleepingcomputer.com/news/security/unlimited-technology-systems-breach-impacts-38-million-people/
・Bleeping Computer「Hackers breach TrueConf to trojanize client installers with backdoors」 https://www.bleepingcomputer.com/news/security/hackers-breach-trueconf-to-trojanize-client-installers-with-backdoors/
・The Hacker News「Progress Kemp LoadMaster Flaw Hits CISA KEV After 792 Reported Exploit Attempts」 https://thehackernews.com/
・The Hacker News「New CSS Attacks Can Break Webmail Defenses to Steal Passwords and Tokens」 https://thehackernews.com/2026/08/new-css-attacks-can-break-webmail.html
・Krebs on Security「LG to Ban Residential Proxies from Smart TV Apps」 https://krebsonsecurity.com/2026/07/lg-to-ban-residential-proxies-from-smart-tv-apps/
・Wired Security「DHS Wants Protesters' Signal Group Chats」 https://www.wired.com/story/dhs-wants-protesters-signal-group-chats/
・Wired Security「The Most Dangerous AI Hacking Techniques Still Have Humans in the Loop」 https://www.wired.com/story/the-most-dangerous-ai-hacking-techniques-still-have-human-input/

#セキュリティ #サイバー攻撃 #データ漏洩 #脆弱性 #ゆっくり解説 #ずんだもん #四国めたん #ハッキング #CISA

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年8月10日）</h1>
<p><strong>キーワード:</strong> 医療データ漏洩 / ビデオ会議バックドア / CISA KEV / ウェブメールCSS攻撃 / 住宅プロキシ / AIハッキング</p>
<h2>オープニング：2026年8月10日 — セキュリティニュース</h2>
<ul>
<li>本日は、医療分野の委託先企業から380万人分のデータが流出した事案、ビデオ会議ソフト「TrueConf」のインストーラーが改ざんされた事案、CISAが実際の悪用を確認して緊急是正を命じた脆弱性、Outlook・Gmailなど主要ウェブメール6サービスを横断する新しい攻撃手法、LGがスマートテレビの不正転用を禁止した動き、そして米国土安全保障省とデモ参加者の暗号化チャットを巡る訴訟の7本を扱う。</li>
<li>共通する論点は「本人が気づかないところでデータや端末が第三者に使われている」こと。医療委託先、ビデオ会議の配布経路、メール受信箱、テレビの通信経路、暗号化チャットのログという異なる場所で、同じ構造の問題が起きている。</li>
</ul>
<h2>医療ソフト委託先「Unlimited Technology Systems」、380万人分の情報が流出</h2>
<ul>
<li>米国の医療関連ソフトウェア企業Unlimited Technology Systemsが、2025年10月に発生したデータ侵害で約380万人が影響を受けたと発表した。同社は病院・診療所向けに患者情報を扱うシステムを提供する立場にあり、直接の患者ではなく委託先経由での被害という点が特徴。</li>
<li>発生から公表まで約10か月かかっている。米国の医療データ漏洩は被害調査・通知義務の手続きに時間がかかることが多く、今回もその典型例にあたる。</li>
<li>論点: 自分がその病院にかかった記憶がなくても、検査機関や請求代行など「裏側の委託先」経由で情報が流出することがある。通知が来た場合は発生時期（2025年10月）との関連を確認する必要がある。</li>
</ul>
<h2>ビデオ会議ソフト「TrueConf」、侵入者がインストーラーを改ざんしてバックドアを配布</h2>
<ul>
<li>ハクティビスト集団「Head Mare」が、パッチを当てていないTrueConfのビデオ会議サーバーの脆弱性を悪用してサーバーに侵入し、配布用のクライアントインストーラーを不正なバージョンに差し替え、バックドアを仕込んでいたことが確認された。</li>
<li>通常のソフトウェア更新の仕組みを乗っ取り、正規の配布元から悪意あるファイルを配る「サプライチェーン型」の手口。利用者は正規サイトからダウンロードしたつもりでも被害に遭う。</li>
<li>論点: 自社でTrueConfサーバーを運用している組織は、サーバーのパッチ適用状況と、配布済みインストーラーのハッシュ値の確認が急務。個人利用者側でも、心当たりのない再インストール要求には注意が必要。</li>
</ul>
<h2>CISA、Kemp LoadMasterの脆弱性を「悪用確認済み」リストに追加——792件の攻撃試行</h2>
<ul>
<li>米CISA（サイバーセキュリティ・インフラセキュリティ庁）が、Progress社のロードバランサー製品「Kemp LoadMaster」の脆弱性（CVE-2026-8037、深刻度スコア9.6）を、実際に悪用が確認された脆弱性の一覧「KEVカタログ」に追加した。任意のコマンドを実行される「コマンドインジェクション」型の欠陥で、これまでに792件の攻撃試行が報告されている。</li>
<li>KEVカタログ登録は、米連邦政府機関に対して期限付きでの是正を義務付ける効果を持つ。民間企業への強制力はないが、実際の攻撃が進行中であることを示す強いシグナルとして業界で参照される。</li>
<li>論点: LoadMasterはネットワークの入口に置かれる機器のため、乗っ取られると内部への足がかりを与えてしまう。管理者は792件という攻撃件数の多さを踏まえ、パッチ適用を後回しにしない判断が必要。</li>
</ul>
<h2>Outlook・Gmailなど6大ウェブメールを横断する新攻撃、CSSだけでパスワードを盗む</h2>
<ul>
<li>セキュリティ研究者（PortSwigger社のGareth氏）が、メール本文に埋め込んだCSS（見た目を整える技術）だけでウェブメールの表示領域から「はみ出し」、Outlook・Gmail・Fastmail・Proton Mail・Yahoo Mail・AOL Mailの防御を破る一連の攻撃手法を発表した。パスワードや認証トークンの窃取、他サービスへのなりすましログイン、AIがメールを読み取る機能の誤動作まで引き起こせるという。</li>
<li>通常「メールを開いただけでは安全」とされてきた前提を、添付ファイルもリンククリックも使わずに崩す点が新しい。CSSは本来デザイン用の技術であり、多くのメールサービスがセキュリティ検査の対象外にしてきた領域。</li>
<li>論点: 対策は基本的にサービス提供者側のパッチ待ちになる。利用者側で今すぐできることは、パスワード使い回しをやめ、二段階認証を有効にしておくこと。各社の修正状況は今後の続報で確認する必要がある。</li>
</ul>
<h2>LG、スマートテレビアプリの「住宅プロキシ」転用を禁止へ</h2>
<ul>
<li>LGエレクトロニクスが、自社スマートテレビ向けアプリがユーザーのテレビを「常時稼働の住宅プロキシ（他人の通信を経由させる中継点）」に変えてしまう仕組みを禁止し、該当アプリを停止すると発表した。背景には、LGのアプリストア「webOS」で配信されているゲームなどのアプリのうち42%超が、本人の知らないところで第三者の通信をテレビ経由で流していたという研究者の指摘がある。</li>
<li>前日までに報じたFBIによる住宅プロキシサービス「NetNut」摘発（2026年8月9日既報）と地続きの問題で、今回はサービス提供側ではなく「機器メーカー側の対策」という別の角度になる。悪意ある通信を隠す側と、それを許してしまう機器の双方から対策が進んでいる形。</li>
<li>論点: 自宅のスマートテレビが意図せず他人の通信の踏み台にされていた可能性がある。LGはアプリの停止を進めるとしているが、他メーカーの対応は明らかになっていない。</li>
</ul>
<h2>米国土安全保障省、デモ参加者の暗号化チャット「Signal」のログ提出を要求</h2>
<ul>
<li>デモ参加者らが「表現の自由を侵害された」として米国土安全保障省（DHS）を訴えている訴訟の中で、DHS側が原告らの暗号化メッセージアプリ「Signal」のグループチャットの内容提出を求めていることが分かった。訴訟自体はDHSの行為を問うものだが、DHSはその手続きを利用して原告側の非公開の通信内容にアクセスしようとしている。</li>
<li>Signalはメッセージが送信者と受信者以外に読めない「エンドツーエンド暗号化」を採用しており、本来は法的手続きを経ても第三者が内容を見ることは想定されていない。訴訟の証拠開示手続きという別の経路から中身に迫ろうとする点が論点になっている。</li>
<li>論点: 暗号化アプリを使っていても、訴訟の証拠開示や捜査令状など別の法的手段で内容提出を求められる可能性がある。技術的な暗号化と、法的な開示義務は別の問題として捉える必要がある。</li>
</ul>
<h2>「AIハッキングの最も危険な手口」も、結局は人間の判断が要る——研究者の実験</h2>
<ul>
<li>セキュリティ研究者ジェームズ・ケトル氏が、AIにどこまでハッキング作業を任せられるかを検証した結果、最も効果的だったのは「AI単独」ではなく「AIと人間の専門知識を組み合わせた」手法だったと報告した。AIは大量の候補を高速に試す作業に強い一方、どこに本当の弱点があるかを見極める判断は依然として人間の経験に依存するという。</li>
<li>AIによる攻撃の脅威が語られる際、しばしば「AIが自動で何でもやってしまう」という極端な想定が先行しがちだが、今回の実験結果はその想定に対する具体的な反証データになる。</li>
<li>論点: 防御側にとっても同じ構図が当てはまる可能性がある。AIによる検知・対応の自動化を進める場合も、人間の専門知識をどこに残すかが引き続き重要な設計判断になる。</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>本日取り上げた7件は、いずれも「本人の目が届かない場所」で情報や端末が使われていた事例。医療委託先、ソフト配布経路、ネットワーク機器、メール受信箱、家庭のテレビ、暗号化チャットの証拠開示、AIハッキングの実態と、対象は多岐にわたるが、共通するのは「見えていない経路をどう可視化し、管理するか」という課題。</li>
<li>今後の確認点: Unlimited Technology Systemsの詳細な被害範囲、TrueConf利用組織のパッチ適用状況、Kemp LoadMasterの是正期限、CSS攻撃への各ウェブメール事業者の対応、LG以外のテレビメーカーの動き、DHSと原告側の訴訟の行方。</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/unlimited-technology-systems-breach-impacts-38-million-people/">Unlimited Technology Systems breach impacts 3.8 million people</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-breach-trueconf-to-trojanize-client-installers-with-backdoors/">Hackers breach TrueConf to trojanize client installers with backdoors</a></li>
<li><a href="https://thehackernews.com/">Progress Kemp LoadMaster Flaw Hits CISA KEV After 792 Reported Exploit Attempts</a></li>
<li><a href="https://thehackernews.com/2026/08/new-css-attacks-can-break-webmail.html">New CSS Attacks Can Break Webmail Defenses to Steal Passwords and Tokens</a></li>
<li><a href="https://krebsonsecurity.com/2026/07/lg-to-ban-residential-proxies-from-smart-tv-apps/">LG to Ban Residential Proxies from Smart TV Apps</a></li>
<li><a href="https://www.wired.com/story/dhs-wants-protesters-signal-group-chats/">DHS Wants Protesters' Signal Group Chats</a></li>
<li><a href="https://www.wired.com/story/the-most-dangerous-ai-hacking-techniques-still-have-human-input/">The Most Dangerous AI Hacking Techniques Still Have Humans in the Loop</a></li>
</ul>

</details>

---

[← 2026-08-10 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
