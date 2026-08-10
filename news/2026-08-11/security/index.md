---
title: "パスキーも狙われる？Steam配送漏洩と新型ランサムウェア【2026/08/11】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# パスキーも狙われる？Steam配送漏洩と新型ランサムウェア【2026/08/11】

**2026-08-11 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-11-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-11-security)

---

## 概要

新型ランサムウェアStormEncryptor、北朝鮮系KimsukyのオフラインAI、パスキーを巡る3研究を解説。偽VS Code拡張機能、SonicWall悪用、Steam配送委託先の情報漏洩について、利用者と管理者が取るべき対策を整理します。

▼ 今日のトピック
・StormEncryptorと遠隔管理製品N-central
・KimsukyがオフラインAIで攻撃準備を効率化
・パスキーの暗号ではなく同期と端末を狙う研究
・偽Solidity Pro拡張機能がウォレットとAPI鍵を窃取
・SonicWall SMA1000の修正済み脆弱性を悪用
・Steam配送委託先CEVAから連絡先流出の恐れ

▼ 参考記事・ソース
・The Hacker News「China-Linked Hackers Deploy New StormEncryptor Ransomware」 https://thehackernews.com/2026/08/china-linked-hackers-deploy-new.html
・The Hacker News「Kimsuky Builds Offline AI Stack」 https://thehackernews.com/2026/08/kimsuky-builds-offline-ai-stack-that.html
・The Hacker News「New Passkey Attacks」 https://thehackernews.com/2026/08/new-passkey-attacks-can-recover-synced.html
・The Hacker News「Solidity Pro VS Code Extensions Steal Crypto Wallets」 https://thehackernews.com/2026/08/solidity-pro-vs-code-extensions-steal.html
・BleepingComputer「CISA: SonicWall SMA1000 flaws now exploited」 https://www.bleepingcomputer.com/news/security/cisa-sonicwall-sma1000-flaws-now-exploited-by-ransomware-gangs/
・BleepingComputer「Valve notifies Steam hardware customers of a data breach」 https://www.bleepingcomputer.com/news/security/valve-notifies-steam-hardware-customers-of-a-data-breach/

#サイバーセキュリティ #ランサムウェア #パスキー #Steam #情報漏洩 #フィッシング #ゆっくり解説 #ずんだもん #四国めたん #セキュリティニュース

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>信頼の内側を突く攻撃——パスキー、開発環境、配送委託先（2026年8月11日）</h1>
<p><strong>キーワード:</strong> StormEncryptor / Kimsuky / パスキー / VS Code / SonicWall / Steam / サプライチェーン</p>
<h2>オープニング：2026年8月11日 — セキュリティニュース</h2>
<ul>
<li>2026年8月11日、火曜日のセキュリティニュース。新型ランサムウェア、北朝鮮系攻撃者のオフラインAI、パスキー研究、開発拡張機能、VPN機器、Steam配送委託先の漏洩を扱う</li>
<li>共通点は、正規の管理ツール、端末内の認証情報、公式らしい拡張機能、取引先という「すでに信頼された場所」を攻撃者が足場にしていること</li>
</ul>
<h2>StormEncryptor、N-central経由で管理者の入口から侵入</h2>
<ul>
<li>Microsoftは8月、金銭目的の攻撃者Storm-1175が新しい身代金要求型ウイルス「StormEncryptor」を展開したと公表した。過去にMedusaランサムウェアを使っていた勢力とされる</li>
<li>初期侵入には、IT事業者が多数の顧客端末を遠隔管理するN-centralの脆弱性が使われた可能性が高い。管理ツールを奪われると、一つの侵入口から複数組織へ操作を広げられる</li>
<li>StormEncryptorはC++で書かれ、暗号化したファイルへ「.encrypted」を付加する。新名称でも、侵入後に管理権限を広げ、データを読めなくして金銭を要求する構造は従来型</li>
<li>管理者はN-centralの修正版適用だけでなく、外部公開の有無、管理者ログイン、遠隔実行履歴、バックアップへの到達を確認する必要がある。バックアップは同じ管理系統から切り離す</li>
<li>次に確認すべきは、悪用された正確な脆弱性、侵入期間、影響版、データ持ち出しの有無</li>
</ul>
<h2>Kimsuky、外部チャットを使わずオフラインAIでフィッシングを強化</h2>
<ul>
<li>韓国のセキュリティ企業Geniansは、北朝鮮系の攻撃集団Kimsukyが、自らのサーバー上でAIをオフライン運用している証拠を確認したと報告した</li>
<li>攻撃者は保有文書を検索する仕組みとAIを接続し、標的に合わせたフィッシング文面やマルウェア開発を効率化しようとしている。公開チャットへ機密情報を送らず、利用停止や監視を避けられる点が防御側には厄介</li>
<li>AIが自動で侵入を完成させたと断定する材料ではない。現時点で重要なのは、既存の諜報活動に文書検索、翻訳、コード補助を組み込み、準備時間を短縮していること</li>
<li>組織は不自然な日本語だけを手掛かりにせず、差出人ドメイン、返信先、添付ファイル、ログイン先を照合する。標的型メールでは内容が自然でも、別経路で送信者へ確認する</li>
<li>次に見るべきは、生成文面の識別より、侵入に使われたアカウント、配布基盤、マルウェア部品という観測可能な痕跡</li>
</ul>
<h2>パスキーを破る3研究、暗号ではなく同期と端末を狙う</h2>
<ul>
<li>8月上旬に公表された3件の研究は、パスキーの暗号そのものを解読せず、Windowsが露出した署名済み認証情報の再利用、端末内マルウェアによる同期済み秘密鍵への接近、認証フローの中継で防御を回避できる条件を示した</li>
<li>パスキーは、サービス側に公開鍵、利用者の端末や認証情報管理サービスに秘密鍵を置く。偽サイトへ秘密を入力させる従来型フィッシングには強いが、すでに端末が侵害されている場合まで万能ではない</li>
<li>同期型は機種変更と紛失復旧に便利だが、クラウド同期アカウントと端末の保護が新しい要所になる。端末固定型や物理セキュリティキーは持ち運びにくい代わりに、秘密鍵の移動範囲を狭められる</li>
<li>利用者はパスキーを捨ててパスワードへ戻す必要はない。OSとブラウザーを更新し、同期アカウント自体へ強い多要素認証を設定し、見覚えのない端末と登録済み認証器を削除する</li>
<li>企業はアカウント復旧と新規パスキー登録を監査し、重要管理者には端末準拠性や物理キーを組み合わせる</li>
</ul>
<h2>偽Solidity Pro拡張機能、開発者のウォレットとAPI鍵を窃取</h2>
<ul>
<li>研究者は、Visual Studio Code互換の拡張機能「Solidity Pro」を装う二つの悪性パッケージを確認した。Open VSXからは削除されたが、関連するGitHubリポジトリも攻撃経路に使われた</li>
<li>対象は暗号資産アプリを開発する人で、ブラウザーウォレット、API鍵、各種認証情報を盗む機能を配布した。コード補完を入れるつもりが、資産移動やクラウド操作に使える秘密を渡す結果になる</li>
<li>拡張機能は開いているファイル、ターミナル、認証情報へ広い権限を持ち得る。名前やアイコンが本物らしいこと、公開リポジトリがあることだけでは安全を証明できない</li>
<li>インストール済みなら削除だけで終えず、ウォレット資産の安全な移動、API鍵とアクセストークンの失効・再発行、端末のマルウェア検査、操作ログ確認が必要</li>
<li>チームは許可済み拡張機能の一覧、発行者確認、バージョン固定、秘密鍵を開発端末へ常置しない運用を組み合わせる</li>
</ul>
<h2>SonicWall SMA1000、修正後もランサムウェアが悪用</h2>
<ul>
<li>米CISAは、SonicWallのリモートアクセス製品SMA1000にある二つの修正済み脆弱性が、ランサムウェア攻撃で悪用されていると確認した</li>
<li>一つは深刻度が最大級のサーバー側リクエスト偽造。攻撃者が装置から内部向け通信を出させ、本来は外部から届かない管理機能やサービスへ近づく恐れがある</li>
<li>VPN装置は社外から社内へ入る正規の玄関であり、侵害されるとパスワード変更だけでは足りない。設定改ざん、追加アカウント、証明書、接続ログまで調べる必要がある</li>
<li>管理者は対象版と修正状況を確認し、管理画面をインターネットへ直接公開しない。侵害の兆候があれば、装置を隔離して認証情報と証明書を更新する</li>
<li>利用者は通常、個人端末で直接修正できないため、勤務先の案内に従い、不審な再認証要求をIT部門へ報告する</li>
</ul>
<h2>Steamハードウェア購入者、配送委託先CEVAから連絡先流出の恐れ</h2>
<ul>
<li>Valveは欧州のSteamハードウェア購入者へ、配送を担当するCEVA Logisticsへのサイバー攻撃で顧客情報が盗まれた可能性を通知した</li>
<li>攻撃は7月29日から8月1日の間に発生し、Valveは8月7日に把握したとされる。氏名、住所、電話番号、メールアドレス、配送情報が対象になり得る一方、決済カード情報とSteamのパスワードは含まれないと説明された</li>
<li>パスワードが漏れていなくても、商品名、住所、配送時期を知る攻撃者は「配送再手続き」や「購入確認」を装った精巧なメールやSMSを送れる</li>
<li>対象者は通知内のリンクからログインせず、Steamの公式アプリや自分で入力した公式URLから注文状況を確認する。住所や注文番号を知っていることを、正規業者の証明にしてはいけない</li>
<li>企業側には、委託先へ渡す項目と保存期間を最小化し、事故時にどの顧客へ何が渡っていたかを即座に追跡できる台帳が必要</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>今日の6件は、遠隔管理、AIの社内運用、認証情報同期、開発拡張機能、VPN、物流委託先という信頼済みの経路が攻撃面になることを示した</li>
<li>一つの万能対策はない。管理ツールの更新と監査、メールの別経路確認、端末保護、秘密鍵の分離、VPN侵害調査、委託データの最小化を役割ごとに実施する</li>
<li>利用者が今日できるのは、OSとブラウザーの更新、登録端末の確認、不審な拡張機能の削除、配送通知を公式アプリから確かめること</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li>The Hacker News「China-Linked Hackers Deploy New StormEncryptor Ransomware, Likely via N-central Flaw」 https://thehackernews.com/2026/08/china-linked-hackers-deploy-new.html</li>
<li>The Hacker News「Kimsuky Builds Offline AI Stack to Boost Phishing and Automate Malware Development」 https://thehackernews.com/2026/08/kimsuky-builds-offline-ai-stack-that.html</li>
<li>The Hacker News「New Passkey Attacks Can Recover Synced Private Keys or Bypass Phishing-Resistant MFA」 https://thehackernews.com/2026/08/new-passkey-attacks-can-recover-synced.html</li>
<li>The Hacker News「Solidity Pro VS Code Extensions Steal Crypto Wallets, API Keys, and Credentials」 https://thehackernews.com/2026/08/solidity-pro-vs-code-extensions-steal.html</li>
<li>BleepingComputer「CISA: SonicWall SMA1000 flaws now exploited by ransomware gangs」 https://www.bleepingcomputer.com/news/security/cisa-sonicwall-sma1000-flaws-now-exploited-by-ransomware-gangs/</li>
<li>BleepingComputer「Valve notifies Steam hardware customers of a data breach」 https://www.bleepingcomputer.com/news/security/valve-notifies-steam-hardware-customers-of-a-data-breach/</li>
</ul>

</details>

---

[← 2026-08-11 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
