---
title: "指紋もPINも不要？パスキー乗っ取りと警察10万人流出【2026/08/04】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# 指紋もPINも不要？パスキー乗っ取りと警察10万人流出【2026/08/04】

**2026-08-04 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-04-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-04-security)

---

## 概要

英国警察関係者10万人超の情報流出、指紋やPINなしでパスキーを乗っ取る新手口、企業向けVPNや遠隔管理ツールの悪用を解説。偽Robloxツール、ブラウザ画像キャッシュ、npmパッケージに潜むマルウェアと、Chromeの週2回パッチも取り上げます。

▼ 今日のトピック
・英国警察の内部データベースから10万人超の情報が流出
・INCランサムウェアがSonicWall SMA 1000の脆弱性を集中攻撃
・遠隔管理ソフトN-centralの認証回避脆弱性が悪用中
・指紋もPINも使わずパスキーを乗っ取る新手口
・偽Roblox改造ツールが情報窃取型マルウェアとRATを配布
・DOUBLECUPがブラウザの画像キャッシュにマルウェアを隠蔽
・Alibaba利用者を狙う18個の悪意あるnpmパッケージ
・AIのバグ発見加速でChromeが週2回パッチを検討

▼ 参考記事・ソース
・Bleeping Computer「ExfilSquad hackers leak info of over 100,000 UK police officers, staff」 https://www.bleepingcomputer.com/news/security/exfilsquad-hackers-leak-info-of-over-100-000-uk-police-officers-staff/
・The Hacker News「PNLD Breach Exposes U.K. Police and Government Contact Details on Dark Web」 https://thehackernews.com/2026/08/pnld-breach-exposes-uk-police-and.html
・The Hacker News「INC Ransomware Emerges as Dominant Actor Exploiting SonicWall SMA 1000 Flaws」 https://thehackernews.com/2026/08/inc-ransomware-emerges-as-dominant.html
・Bleeping Computer「N-able warns of N-central auth bypass flaw exploited in attacks」 https://www.bleepingcomputer.com/news/security/n-able-warns-of-n-central-auth-bypass-flaw-exploited-in-attacks/
・The Hacker News「Google Password Manager Attacks Could Let Malware Hijack Passkey-Protected Accounts」 https://thehackernews.com/2026/08/google-password-manager-attacks-could.html
・Bleeping Computer「Fake Roblox Xeno script launcher pushes infostealer, RAT malware」 https://www.bleepingcomputer.com/news/security/fake-roblox-xeno-script-launcher-pushes-infostealer-rat-malware/
・Bleeping Computer「New DOUBLECUP ClickFix service hides malware in browser cache images」 https://www.bleepingcomputer.com/news/security/new-doublecup-clickfix-service-hides-malware-in-browser-cache-images/
・The Hacker News「18 Malicious npm Packages Deliver Cross-Platform RAT to Alibaba Tool Users」 https://thehackernews.com/2026/08/18-malicious-npm-packages-deliver-cross.html
・Wired Security「Chrome Needs Twice-a-Week Patching Thanks to AI Bug Hunting」 https://www.wired.com/story/chrome-needs-twice-a-week-patching-thanks-to-ai-bug-hunting-for-now/

#セキュリティニュース #サイバー攻撃 #ハッキング #ゆっくり解説 #ずんだもん #四国めたん #脆弱性 #パスキー #ランサムウェア #情報漏洩 #マルウェア #Chrome

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース 2026年8月4日</h1>
<p>キーワード: 個人情報漏えい, ランサムウェア, パスキー乗っ取り, サプライチェーン攻撃, Chrome, VPN機器</p>
<h2>オープニング：2026年8月4日 — セキュリティニュース</h2>
<p>今日は、英国警察の内部情報10万件超の流出、指紋もPINも使わずパスキーを乗っ取る新手口、そしてゲーム機やAI開発ツールにまで忍び寄るマルウェアまで、身近なところから企業の防御網まで幅広く取り上げます。</p>
<h2>英国警察の内部データベースが攻撃され、警察官10万人超の情報が流出</h2>
<ul>
<li>英国の警察・法曹関係者向け内部データベース「PNLD(Police National Legal Database)」が「ExfilSquad」を名乗るハッカー集団の攻撃を受け、10万人を超える警察官・職員・刑事司法関係者の氏名、所属組織、業務用メールアドレスがダークウェブに公開された。</li>
<li>侵害は7月26日に確認されており、対象には警察だけでなく政府の連携機関や取引先の担当者も含まれていた。運営元は被害を確認したと発表している。</li>
<li>業務用の連絡先情報でも、大量に流出すると標的型フィッシング(相手の役職や組織名を知った上で送る詐欺メール)の材料にされやすい。組織に属する人は「知っている相手からのメールでも急かす内容なら疑う」という基本姿勢が重要になる。</li>
</ul>
<h2>ランサムウェア集団「INC」が企業向けVPN機器の脆弱性を集中攻撃</h2>
<ul>
<li>ランサムウェア(身代金要求型ウイルス)集団「INC」が、SonicWall社の企業向けVPN機器「SMA 1000」シリーズで見つかった脆弱性を悪用する攻撃で、8月に入ってから最も活発な攻撃者になったとセキュリティ企業Resecurityが報告した。</li>
<li>INCは被害企業の名前を次々と自らのリークサイト(身代金を払わない企業の情報を晒すサイト)に掲載しており、企業に心理的圧力をかける手口を続けている。</li>
<li>VPN機器は社外から社内ネットワークに安全に接続するための入口だが、その入口自体に穴があると意味がない。該当機器を使う企業はメーカーが出す修正パッチの適用状況を至急確認する必要がある。</li>
</ul>
<h2>リモート監視ツールの認証回避脆弱性が悪用中——IT管理会社が緊急警告</h2>
<ul>
<li>多くの企業のIT部門やIT管理会社が使う遠隔管理ソフト「N-central」に、ログイン認証をすり抜けられる脆弱性(CVE-2026-18577)が見つかり、実際の攻撃で悪用されていることを開発元のN-ableが警告した。</li>
<li>クラウド版・自社設置版の両方が対象で、悪用されるとパソコンやサーバーを遠隔操作する権限そのものを攻撃者に奪われる恐れがある。</li>
<li>「管理する側のツール」が乗っ取られると、そのツールが管理している全ての顧客企業に被害が広がる連鎖リスクがある。IT管理会社を利用している企業は、委託先が緊急パッチを適用済みか確認しておくと安心。</li>
</ul>
<h2>指紋もPINも使わず、パスキーを乗っ取る新手口が判明</h2>
<ul>
<li>Googleのパスワード管理機能(パスキーの保管・同期を担うクラウド認証システム)に対する新しい攻撃手法が、セキュリティ企業Unit42により3種類報告された。最も強力な手法では、パソコンの一般ユーザー権限で動くマルウェアだけで、指紋やPIN、画面上の確認表示なしに、パスキーで守られたアカウントへ勝手にログインできてしまう。</li>
<li>パスキーは「パスワードより安全」とされ普及が進んでいる認証方式だが、今回の手口は端末に侵入したマルウェアが裏で鍵の情報そのものを盗み出す仕組みで、パスキー自体の暗号技術が破られたわけではない。</li>
<li>対策の基本は変わらず、「怪しい添付ファイルやソフトを実行しない」というマルウェア感染の予防が最重要になる。パスキーを使っていても端末がウイルスに感染すれば意味がないことを覚えておきたい。</li>
</ul>
<h2>偽の「Roblox」改造ツールでゲーム好きの子どもが感染被害に</h2>
<ul>
<li>人気ゲーム「Roblox」向けの非公式スクリプト実行ツール「Xeno Executor」を装った偽インストーラーが配布され、実行すると情報窃取型マルウェアと遠隔操作型マルウェア(RAT)に同時感染する被害が確認された。</li>
<li>Xeno Executorはゲームの改造(チート)に使われる非公式ツールで、公式には配布されていない。攻撃者はこの需要を悪用し、検索結果や動画サイトの説明欄などから偽サイトへ誘導しているとみられる。</li>
<li>子どもがゲームの「裏技ツール」を探して検索することは珍しくない。家庭では、公式ストア以外からのソフト導入は基本的に避けること、知らないうちにパソコンの動作が重くなった場合は相談してもらうことを伝えておくとよい。</li>
</ul>
<h2>ブラウザに保存された画像ファイルにマルウェアを隠す新手口「DOUBLECUP」</h2>
<ul>
<li>ロシア語圏で提供されているマルウェア配布サービス「DOUBLECUP」が、ブラウザが自動保存する画像キャッシュ(表示済み画像の一時保存データ)の中に悪意あるコードを隠し、偽の「セキュリティ確認」画面(ClickFix手口)を使って被害者自身にコードを実行させる新手法を使っていることが判明した。</li>
<li>最終的にWindowsとmacOSの両方で動く「CountLoader」というマルウェアや、新型の遠隔操作ツール「DeviceManager」が仕込まれる。</li>
<li>「怪しいポップアップに出てきた手順(コピー&amp;ペーストの指示など)を、言われるがまま実行しない」ことが最大の防御になる。正規のセキュリティ警告が、パソコンの操作をユーザーに指示することは基本的にない。</li>
</ul>
<h2>中国発のAI開発支援ツールを狙う偽パッケージ、遠隔操作マルウェアを仕込む</h2>
<ul>
<li>ソフトウェア部品を配布する場「npm」上で、アリババ(中国大手IT企業)が提供する開発ツール利用者を狙った18個の悪意あるパッケージが発見された。中国語圏の開発環境を主な標的とし、WindowsでもMacでも動く遠隔操作マルウェア(RAT)を配布していた。</li>
<li>偽パッケージの一つ「lib-mtop」は、アリババの非公開パッケージと同じ名前を使い、開発者が誤ってインストールするよう仕向ける「なりすまし」の手口を使っていた。</li>
<li>便利なプログラム部品を無料で組み込めるこうした仕組みは開発の効率化に欠かせない一方、名前だけを信じてインストールすると偽物を掴まされるリスクがある。開発に関わる人は、配布元の公式リポジトリ名かどうかを必ず確認する習慣が求められる。</li>
</ul>
<h2>Chromeがついに週2回パッチへ——AIによるバグ発見が加速</h2>
<ul>
<li>Googleのブラウザ「Chrome」で、6月の2回の更新だけでそれ以前の23回分の更新を上回る数の脆弱性が修正された。背景には、AIを使った自動バグ発見の急速な進歩があり、Googleは今後、通常より頻繁な週2回ペースでの修正配信を検討している。</li>
<li>これまで人間の研究者が時間をかけて見つけていた脆弱性を、AIツールが大量かつ高速に発見できるようになったことで、「直すべき穴」の数自体が急増している状況。</li>
<li>利用者側にできることはシンプルで、Chromeの自動更新をオフにせず、再起動を促す通知が出たら早めに応じることに尽きる。更新頻度が上がるのは面倒に見えて、実際には守りが強化されているサインでもある。</li>
</ul>
<h2>まとめ</h2>
<p>今日は、大規模な個人情報漏えい、企業の入口を狙うVPN機器の脆弱性、そして「安全なはず」のパスキーですらマルウェア感染には無力という現実まで見てきました。共通して言えるのは、どんなに強固な認証技術があっても、端末そのものがマルウェアに感染すれば無意味になるということ。怪しいソフトを実行しない、更新を後回しにしない——この2点が今日一番の教訓です。</p>
<h2>参考ソース</h2>
<ul>
<li>Bleeping Computer「ExfilSquad hackers leak info of over 100,000 UK police officers, staff」 https://www.bleepingcomputer.com/news/security/exfilsquad-hackers-leak-info-of-over-100-000-uk-police-officers-staff/</li>
<li>The Hacker News「PNLD Breach Exposes U.K. Police and Government Contact Details on Dark Web」 https://thehackernews.com/2026/08/pnld-breach-exposes-uk-police-and.html</li>
<li>The Hacker News「INC Ransomware Emerges as Dominant Actor Exploiting SonicWall SMA 1000 Flaws」 https://thehackernews.com/2026/08/inc-ransomware-emerges-as-dominant.html</li>
<li>Bleeping Computer「N-able warns of N-central auth bypass flaw exploited in attacks」 https://www.bleepingcomputer.com/news/security/n-able-warns-of-n-central-auth-bypass-flaw-exploited-in-attacks/</li>
<li>The Hacker News「Google Password Manager Attacks Could Let Malware Hijack Passkey-Protected Accounts」 https://thehackernews.com/2026/08/google-password-manager-attacks-could.html</li>
<li>Bleeping Computer「Fake Roblox Xeno script launcher pushes infostealer, RAT malware」 https://www.bleepingcomputer.com/news/security/fake-roblox-xeno-script-launcher-pushes-infostealer-rat-malware/</li>
<li>Bleeping Computer「New DOUBLECUP ClickFix service hides malware in browser cache images」 https://www.bleepingcomputer.com/news/security/new-doublecup-clickfix-service-hides-malware-in-browser-cache-images/</li>
<li>The Hacker News「18 Malicious npm Packages Deliver Cross-Platform RAT to Alibaba Tool Users」 https://thehackernews.com/2026/08/18-malicious-npm-packages-deliver-cross.html</li>
<li>Wired Security「Chrome Needs Twice-a-Week Patching Thanks to AI Bug Hunting」 https://www.wired.com/story/chrome-needs-twice-a-week-patching-thanks-to-ai-bug-hunting-for-now/</li>
</ul>

</details>

---

[← 2026-08-04 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
