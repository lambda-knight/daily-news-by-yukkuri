---
title: "セキュリティニュース 2026-09-07"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# セキュリティニュース 2026-09-07

**2026-09-07 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-09-07-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-09-07-security)

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年9月7日）</h1>
<p><strong>キーワード:</strong> OpenAI Astra 重大サイバー能力 / Snowflake恐喝有罪答弁 / MikroTik認証なし乗っ取り / MagentoゼロデイStyleSmuggler / ClickFixブロックチェーン配信 / REVSTEALER常駐モジュール / ATM暗号ソフト9件欠陥 / Metabase SQLインジェクション</p>
<h2>オープニング：2026年9月7日 — セキュリティニュース</h2>
<ul>
<li>本日は8本。OpenAIが自社の安全評価で初めて「重大（Critical）」なサイバー能力に達したと認めたモデル「Astra」を近く公開する件、クラウド基盤Snowflakeの利用企業165社超を侵害・恐喝したカナダ人被告Connor Riley Mouckaが米国で有罪答弁した件、MikroTik製ルーターがインターネットに開いたSSH経由で認証なしに乗っ取られている件、通販システムMagento・Adobe Commerceの未修正ゼロデイ「StyleSmuggler」、決済用ブロックチェーン上にマルウェアを隠して5400以上の改ざんサイトから配る「ClickFix」大規模キャンペーン、情報窃取マルウェア「REVSTEALER」が残す4つの常駐モジュール、ATMなどで使われる暗号化ソフトに見つかった9件の欠陥、そして認証なしで管理者権限を奪えるMetabaseのSQLインジェクション欠陥を扱う。</li>
<li>今日の軸は「攻撃を自動化・省力化する道具立て」と「広く共有された部品の弱さ」だ。AIによる脆弱性発見、ブロックチェーンを使った停止しにくい配信基盤、フルディスク暗号化のような共通コンポーネントの欠陥が、いずれも単発の事件を超えて横に広がる構図に注目してほしい。</li>
</ul>
<h2>OpenAI、初の「重大」サイバー能力に達したモデル「Astra」を公開へ</h2>
<ul>
<li>OpenAIは2026年9月1日、開発中のモデル「Astra」が自社の「Preparedness Framework（準備度フレームワーク）」で初めてサイバーセキュリティの脅威度を最上位の「Critical（重大）」に分類したと公表した。内部評価で、人手による段階的な指示なしに未知のソフトウェア脆弱性を自力で発見し、複雑な攻撃を組み立てられることが確認されたためとしている。</li>
<li>ベンチマークでは攻撃用の評価データ「ExploitBench」で満点を記録し、2026年半ばに公表された深刻度の高い脆弱性20件を対象にしたテストでは、うち2件について未修正のゼロデイを見つけて攻撃の連鎖に組み込んだという。OpenAIは能力を検知した時点でいったん開発を止め、被害を十分に下げられると判断できる対策を整えてから再開したと説明している。</li>
<li>OpenAIはAstraを「近く」提供するとしつつ、サイバー攻撃に関わる機能へのアクセスは制限すると述べている。攻撃側と防御側のどちらが先にこの能力を実務で使うかで、脆弱性が公表されてからパッチが当たるまでの猶予が今より短くなる可能性がある。防御側にとっては、AIによる自動的な脆弱性発見を前提にした資産管理とパッチ運用への移行が課題になる。</li>
</ul>
<h2>スノーフレーク恐喝事件、カナダ人被告が米国で有罪答弁</h2>
<ul>
<li>クラウドのデータ基盤Snowflakeを使う企業を狙った大規模な侵害・恐喝事件で、カナダ・オンタリオ州キッチナー在住のConnor Riley Moucka被告（26）が、コンピューター詐欺、電信詐欺、加重個人情報窃盗、共謀の罪について米国で有罪を認めた。攻撃対象はSnowflake利用企業165社以上に及び、Ticketmaster、LendingTree、Advance Auto Parts、Neiman Marcusなどが被害企業として確認されている。</li>
<li>Moucka被告は、通信大手AT&amp;Tの利用者1億人超の通話・SMSの履歴記録を盗んだことも認めた。活動時期は2024年2月から10月で、被害企業から少なくとも合計250万ドルの身代金を得ていたほか、盗んだ政府関係者のデータを使って被害者の一部を再度脅していたという。量刑言い渡しは2026年10月27日の予定で、最低2年、最長で30年の刑に問われ得る。</li>
<li>この事件は、盗んだIDとパスワードを多要素認証のないSnowflakeアカウントに片端から試す、比較的単純な手口で起きた。共犯とされる米陸軍兵Cameron Wageniusは既に有罪を認めており、もう一人の関与者John Erin Binnsはトルコで拘束後に釈放され、トルコ国籍を得て引き渡しが困難な状態にある。クラウド上のデータ保管では、利用側が多要素認証を強制していたかどうかが被害の分かれ目になったことがあらためて示された。</li>
</ul>
<h2>MikroTik製ルーター、公開SSHから認証なしで乗っ取り</h2>
<ul>
<li>ポーランドの国家コンピューター緊急対応チームCERT Polskaは2026年9月5日、MikroTik製ルーターがインターネットに開いたSSH（遠隔操作用の暗号化接続）経由で、認証なしに完全な管理者権限を奪われる攻撃を確認したと警告した。攻撃は少なくとも2026年9月2日から続いており、2つの弱点を組み合わせる手口とされるが、CVE番号や技術的な詳細はまだ公表されていない。</li>
<li>攻撃者は侵入後、ルーターの設定を書き換えたり、権限の高い管理アカウントを勝手に作ったりしていた。ログには身に覚えのない「ops」アカウントの作成記録が残るという。ルーターはインターネットと社内・家庭内ネットワークの境界にあるため、乗っ取られると通信の盗聴や他機器への侵入の足場にされる。</li>
<li>MikroTikは修正版として、RouterOSの6.49.21、7.23.4以降、7.24.2を公開している。CERT Polskaは、管理用サービスを一時的に停止するか信頼できるネットワークからのみ接続できるよう制限し、直ちに更新したうえで、不審な設定変更やアカウント作成の記録がないか点検するよう促している。侵入の痕跡が見つかった機器は初期化が必要になる。</li>
</ul>
<h2>Magento・Adobe Commerceに未修正ゼロデイ「StyleSmuggler」</h2>
<ul>
<li>オランダのEC専門セキュリティ企業Sansecは2026年9月5日、通販サイト構築ソフトMagento Open SourceとAdobe Commerceに未修正の脆弱性「StyleSmuggler」があり、ログインなしでサーバー上の任意コードを実行される攻撃が2026年9月4日から始まっていると発表した。2.4.9を含む現行の全バージョンが影響を受け、2.4.7・2.4.8・2.4.9での悪用が確認されている。</li>
<li>攻撃は2段階で進む。まずMagentoが生成する障害レポートなどのファイルにPHPコードを注入し、その後「支払い失敗のリマインダーメール」機能を使ってコードを実行させる。メールを誰かが開く必要はなく、Magentoがメール本文を組み立てる過程で実行されてしまう。侵入に成功するとサーバー権限でのコード実行が可能になり、5分ごとにcronで再起動される偽装プロセスの裏口が仕込まれる。</li>
<li>現時点でCVE番号は割り当てられておらず、正式なパッチも出ていない。Sansecやホスティング事業者は暫定策として、GraphQLの無効化、有志が公開した非公式パッチの適用、PHPの<code>disable_functions</code>に<code>proc_open</code>を追加する対応を挙げている。決済情報を扱う通販サイトは、パッチを待つ間も自衛策を講じる必要がある。</li>
</ul>
<h2>改ざんサイト5400件超、ブロックチェーン上のコードから「ClickFix」配信</h2>
<ul>
<li>クラウドセキュリティ企業Netskopeは、改ざんされた5400以上の中小企業サイトを使い、偽のCAPTCHA画面で利用者をだましてPowerShellコマンドを実行させる「ClickFix」攻撃が大規模に行われていると報告した。改ざんされているのは主にWordPressとPrestaShopのサイトで、攻撃の中身をBNBスマートチェーンというブロックチェーン上のプログラム（スマートコントラクト）に保存する「EtherHiding」という手口が使われている。</li>
<li>攻撃コードをブロックチェーンに置くと、ホスティング事業者への通報で消せる中央サーバーがないため、配信基盤を止めにくい。キャンペーンは2026年春から続いており、8月には1日あたり最大536件の改ざんサイトがブロックチェーン上の接続先へアクセスしていた。当初のClickFix用プログラムは、後にブラウザーのメモリー内だけで動く通信用の仕掛けに置き換えられ、ディスクに痕跡を残しにくくなっている。</li>
<li>一般の利用者にとっての教訓は変わらない。サイトの指示に従ってWindowsの「ファイル名を指定して実行」やターミナルにコマンドを貼り付けさせる画面が出たら、それは攻撃だと考えてよい。企業側は該当するブロックチェーンの接続先を遮断し、Webページ以外から出るUDP通信を監視する対策が挙げられている。</li>
</ul>
<h2>情報窃取「REVSTEALER」、Windows UpdateとDefenderを止めて裏で採掘</h2>
<ul>
<li>Elastic Security Labsは2026年9月2日、新興のWindows向け情報窃取マルウェア「REVSTEALER」に関連する、これまで未報告の4つの常駐プログラムを公開した。REVSTEALER本体はブラウザーのパスワードやCookie、50種類以上の暗号資産ウォレットのファイルを盗んだ後に自分を消すが、この4つは感染したパソコンに居座り続ける。</li>
<li>4つのうち「LockAppHost」は、Windows UpdateとMicrosoft Defenderを無効化・除外設定したうえで、管理者権限で暗号資産の採掘プログラムを動かす。ほかの3つは、偽のウォレット画面を重ねてパスワードを盗む「ProManager」、クリップボードを監視して送金先アドレスをすり替える「WinUpdate」、感染機を攻撃者の中継地点にする「SoftManager」だ。いずれもレジストリの自動起動やタスクスケジューラーで長期間潜伏する。</li>
<li>Elasticの検知ルールは過去1年で約4700個の検体に一致しており、最も古い検体は2026年2月にさかのぼる。対策として、ソフトは公式サイトからのみ入手すること、LockAppHostが動いた場合はWindows Updateを再有効化しDefenderの除外設定を消すこと、そしてCookieによるセッション乗っ取りを防ぐためパスワード変更だけでなくログイン中のセッションも切ることが挙げられている。</li>
</ul>
<h2>ATM暗号ソフトに9件の欠陥、影響はソフトウェア供給網全体に</h2>
<ul>
<li>セキュリティ研究者Matt Burch氏は、Black HatとDefconのカンファレンスで、CryptWare社のフルディスク暗号化ソフト「CryptoPro Secure Disk」に9件の脆弱性があると発表した。このソフトは企業のパソコンやATMメーカーで広く使われており、起動前の認証と復号を担う。欠陥を悪用すると、ソフトの整合性チェックを回避して暗号化されたディスクへ完全にアクセスできたという。</li>
<li>問題は、特定の失敗状態でボリュームが暗号化されないまま読み込まれることや、鍵の材料や設定値がディスク自体に保存されている点にある。ATMメーカーのDiebold Nixdorfは、9件のうち自社実装に関係するのは2件だけで、現金の窃取に直結するかどうかは研究者と見解が異なると反論している。</li>
<li>Burch氏が強調しているのは、ATMという特定の機器の話にとどまらない点だ。同じフルディスク暗号化ソフトが他の業種の重要システムでも使われており、一つの共通コンポーネントの弱さが、それを組み込んだ多数の製品へ同時に波及する。ソフトウェアの供給網では、どの部品を誰が作り、どこで使い回されているかの把握が防御の前提になる。</li>
</ul>
<h2>Metabaseに緊急のSQLインジェクション欠陥、認証なしで管理者権限</h2>
<ul>
<li>データ可視化ソフトMetabaseは2026年8月6日、パスワード再設定用の入り口を通じて、認証なしの攻撃者がデータベースに任意のSQL文を送り込める脆弱性「CVE-2026-72898」を公表した。悪用されるとMetabaseの管理者権限を奪われる。JPCERTコーディネーションセンターも2026年8月14日に注意喚起を出しており、CVSSスコアは最大の10.0とされている。</li>
<li>影響を受けるのはMetabaseのバージョン0.58系から0.63系（商用版は1.58系から1.63系）で、各系列の修正版が公開されている。この欠陥はパッチ公開前からゼロデイとして悪用されており、クラウド版と自前で運用する複数の利用者が実際に攻撃を受けたと報告されている。</li>
<li>Metabaseは社内の売上や利用状況を集計するダッシュボードとして使われることが多く、接続先の業務データベースの認証情報を保持している。管理者権限を奪われれば、そこにつながる基幹データまで一気に露出する。インターネットに公開しているMetabaseを運用する組織は、対象バージョンかどうかを確認し、修正版へ更新する対応が急がれる。</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>8件を貫くのは「攻撃を省力化する道具立て」と「共有部品の弱さ」だ。AIが自力で未知の脆弱性を見つけるAstra、停止しにくいブロックチェーン配信基盤、盗んだIDを機械的に試すだけで165社を破ったSnowflake事件は、いずれも攻撃側の手間が下がっていることを示す。一方、ATMの暗号化ソフトやMetabaseの欠陥は、広く使われる一つの部品の穴が多数の組織へ同時に及ぶ構図だ。</li>
<li>個人にできることは、サイトの指示でコマンドを貼り付けさせる画面を攻撃と見なすこと、公式サイト以外からソフトを入れないこと、パスワード変更だけでなくログイン中のセッションも切ること。企業・組織は、多要素認証の強制、インターネットに開いた管理サービスの遮断、そして自社が使うソフトが内部で何を組み込んでいるかの棚卸しが、今日の事例に共通する備えになる。</li>
<li>AIによる脆弱性発見が実務に入ってくると、公表からパッチ適用までの猶予は今より短くなる。防御側がその前提で資産管理とパッチ運用を組み替えられるかが、今後の分かれ目になりそうだ。</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://www.wired.com/story/openai-is-about-to-release-its-first-ai-model-with-critical-cyber-abilities/">Wired Security: OpenAI Is About to Release Its First AI Model With 'Critical' Cyber Abilities</a></li>
<li><a href="https://www.cnbc.com/2026/09/01/open-ai-astra-cyber-model.html">CNBC: OpenAI says Astra AI model is its first that crosses 'Critical' cybersecurity capability</a></li>
<li><a href="https://krebsonsecurity.com/2026/08/canadian-man-pleads-guilty-in-snowflake-extortions/">Krebs on Security: Canadian Man Pleads Guilty in Snowflake Extortions</a></li>
<li><a href="https://thehackernews.com/2026/09/attackers-hijack-mikrotik-routers.html">The Hacker News: Attackers Hijack MikroTik Routers Through Internet-Exposed SSH Without Authentication</a></li>
<li><a href="https://thehackernews.com/2026/09/unpatched-magento-and-adobe-commerce.html">The Hacker News: Unpatched Magento and Adobe Commerce Zero-Day Exploited to Backdoor Online Stores</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/over-5-400-hacked-sites-serve-clickfix-payloads-stored-on-the-blockchain/">Bleeping Computer: Over 5,400 hacked sites serve ClickFix payloads stored on the blockchain</a></li>
<li><a href="https://thehackernews.com/2026/09/four-revstealer-linked-modules-disable.html">The Hacker News: Four REVSTEALER-Linked Modules Disable Windows Update and Defender to Run a Crypto Miner</a></li>
<li><a href="https://www.wired.com/story/atm-flaws-reveal-key-weaknesses-in-the-software-supply-chain/">Wired Security: ATM Flaws Reveal Key Weaknesses in the Software Supply Chain</a></li>
<li><a href="https://www.jpcert.or.jp/at/2026/at260023.html">JPCERT/CC: MetabaseのSQLインジェクションの脆弱性（CVE-2026-72898）に関する注意喚起</a></li>
</ul>

</details>

---

[← 2026-09-07 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
