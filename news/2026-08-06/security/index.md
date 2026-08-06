---
title: "格安Claudeの罠、入力内容が丸見えに？ 2026/08/06"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# 格安Claudeの罠、入力内容が丸見えに？ 2026/08/06

**2026-08-06 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-06-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-06-security)

---

## 概要

安さや便利さの裏側を確認するため、AI転売、Mac向けClickFix、クラウド管理製品の脆弱性を解説します。

▼ 今日のトピック
・ゼロデイ買取業者の運営者問題
・格安Claude利用権とプロンプト窃取
・悪用中3脆弱性に3日以内の対処命令

▼ 参考記事・ソース
本文末尾の参考ソースをご覧ください。

#サイバーセキュリティ #情報漏洩 #フィッシング #Claude #Mac #ずんだもん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース 2026年8月6日</h1>
<p>キーワード: 犯罪歴持ちのゼロデイ買取業者, 闇市場のAI乗っ取りサービス, ClickFixマルウェア進化, Veeam/Terraform/DjangoのCVSS満点脆弱性, CISA緊急是正命令, Blogger誤検知, AIフィッシングと防御の転換</p>
<h2>オープニング：2026年8月6日 — セキュリティニュース</h2>
<p>今日は、脆弱性を買い取る企業の裏にいた「前科持ちの経営者」から、闇市場で他人の名義のAIチャットを盗み見販売する新手口、そして企業のクラウド管理ツールに見つかった最高深刻度の脆弱性まで、お金と信頼が絡むセキュリティの話題を集めました。</p>
<h2>ゼロデイ買取企業の裏に「前科持ちの陰謀論者」、Krebsが実態を暴露</h2>
<ul>
<li>セキュリティ研究者Brian Krebsが調査したところ、ソフトウェアの未公開の脆弱性(ゼロデイ)を数百万ドルで買い取ると宣伝している新興セキュリティ企業の経営陣が、極右の陰謀論者かつ前科持ちの2人組だったことが判明した。</li>
<li>この2人は過去に、実在しない「情報機関」を名乗る偽会社や、偽名で運営していたAIロビイング(政治工作)プラットフォームなど、複数の疑わしい事業を手がけていた。</li>
<li>ゼロデイ買取業は本来、発見された脆弱性を製品ベンダーの修正につなげる健全な仕組みとして期待されるが、運営者の身元があいまいなまま多額の資金が動く業界では、買い取られた脆弱性が誰の手に渡るのか分からないリスクがある。セキュリティ製品や取引先を選ぶ際は、運営元の実態を確認する姿勢が欠かせない。</li>
</ul>
<h2>闇市場で「格安Claude利用権」を販売、実は運営者が全プロンプトを盗み見</h2>
<ul>
<li>セキュリティ研究者が、サイバー犯罪フォーラムやメッセージアプリで「Poison Claude」と名乗るサービスが、AnthropicのAIモデル「Claude」(Opus 4.8やSonnet 4.6など)への割引アクセスを違法に販売しているのを発見した。</li>
<li>同種のAI不正転売サービスは他にも半ダース以上確認されており、利用者は正規料金より安くAIを使えると誘われるが、実際には運営者が利用者の入力内容(プロンプト)をすべて閲覧できる仕組みになっている。</li>
<li>会社の機密情報や個人情報を「格安AI」に入力してしまうと、それがそのまま第三者に筒抜けになる恐れがある。仕事や個人情報の入力には、公式サイトや正規の契約経由のAIサービスのみを使うことが基本になる。</li>
</ul>
<h2>偽の「壊れたページ修復」ボタンでMacに感染させる手口、250以上のサイトで指紋認証回避を追加</h2>
<ul>
<li>「ClickFix」と呼ばれる、偽のエラー画面から「これをコピーして実行してください」と操作を誘導し悪意あるコードを実行させる詐欺手口で、macOSを狙う攻撃キャンペーンが250以上のドメインに拡大していることが確認された。</li>
<li>攻撃者はブラウザの指紋情報(画面サイズやフォントなど利用者ごとの特徴)を事前に調べ、セキュリティ企業の調査ツールや自動巡回ロボットには偽のページを見せず、標的にしたMacユーザーにだけ悪意あるダウンロード画面を表示するよう作り込んでいる。</li>
<li>「このサイトは壊れています、修復のため次の手順をコピーして実行してください」という表示は典型的な詐欺の入口。ブラウザやOSが求めていないのに、コマンドの実行やコードの貼り付けを指示された場合は、まず疑うことが自衛の基本になる。</li>
</ul>
<h2>クラウド管理ツール3製品にCVSS満点級の脆弱性、テナントをまたいで乗っ取りも</h2>
<ul>
<li>HashiCorp・Veeam・DjangoソフトウェアファウンデーションがそれぞれTerraform MCPサーバー、Veeam Service Provider Console、Djangoに見つかった合計11件の脆弱性を修正した。</li>
<li>最も深刻なのはVeeamコンソールの認証不要で管理対象エージェントの認証情報を奪える欠陥(深刻度9.5)と、HashiCorpのMCPサーバーで、ある利用者のTerraformトークンが別の利用者に使い回されてしまうテナントをまたいだ欠陥。</li>
<li>クラウドの管理業務を代行するサービスプロバイダーがこれらのツールを使っている場合、自社だけでなく契約先の顧客企業にも影響が及ぶ。管理ツールを使う企業は、ベンダーからの更新通知を放置せず速やかに適用することが重要になる。</li>
</ul>
<h2>CISA、実際に悪用中の3脆弱性を3日以内に対処するよう米政府機関に命令</h2>
<ul>
<li>米サイバーセキュリティ・インフラセキュリティ庁(CISA)は、AI開発ツール「IBM Langflow」、リモート監視ソフト「N-central」、Webサーバー「Apache Tomcat」の脆弱性が実際に攻撃で悪用されていると警告し、連邦政府機関に3日以内の対処を義務付けた。</li>
<li>CISAがこうした緊急是正命令を出すのは、攻撃者がすでにこれらの欠陥を使って侵入を試みている、つまり「理論上の危険」ではなく「現在進行形の被害」であることを意味する。</li>
<li>政府機関以外でもこれら3製品を使っている企業や組織は多い。CISAの警告リストは無料で公開されており、自社が使っているソフトが載っていないか定期的に確認する習慣が実務的な防御につながる。</li>
</ul>
<h2>Googleのブログサービス「Blogger」、誤検知で数百のブログを凍結・一部削除</h2>
<ul>
<li>Googleが、ブログサービス「Blogger」において「マルウェアおよび類似の悪質なコンテンツ」ポリシー違反と誤って判定するシステム不具合により、数百のブログを凍結し、一部は削除してしまったことが分かった。</li>
<li>該当したブログの運営者からは、何年もかけて書きためた記事や画像が突然アクセスできなくなったという報告が相次いでいる。</li>
<li>自動検知システムは悪意あるサイトを素早く止められる利点がある一方、誤検知が起きると無関係な利用者が一方的に被害を受ける。クラウドサービスに大切なデータを預ける場合は、独自のバックアップを別途取っておくことが結局のところ一番の保険になる。</li>
</ul>
<h2>「AIフィッシングがブロックリストを終わらせた」——防御側も検知方式の転換を迫られる</h2>
<ul>
<li>セキュリティ企業Push Securityの分析によると、攻撃者がAIを使って使い捨てのフィッシングサイトや手口を次々と生成するようになった結果、既知の悪質なドメインや署名を集めた「ブロックリスト」方式の防御が実質的に機能しなくなってきているという。</li>
<li>同社は、ドメインや既知の指標を追いかける従来型の防御ではなく、ブラウザ上での操作パターンそのもの(ログイン画面を模倣する挙動など)を検知する「技術ベースの検知」への転換が必要だと指摘する。</li>
<li>個人でできる対策として、URLやアイコンの見た目だけで正規サイトと判断せず、パスワードマネージャーが自動入力しない(=登録済みの正規URLと一致しない)ページでは特に警戒するという習慣が、ブロックリストに頼らない自衛策になる。</li>
</ul>
<h2>まとめ</h2>
<p>今日は、ゼロデイ買取業者の身元、闇市場のAI転売サービス、Macを狙う指紋認証回避型の詐欺サイト、そしてクラウド管理ツールの深刻な脆弱性まで、「信頼して使っていたはずの仕組みが裏切られる」話題が目立ちました。運営元の実態、更新通知の中身、表示された指示の妥当性を一呼吸おいて確かめる習慣が、今日共通する教訓です。</p>
<h2>参考ソース</h2>
<ul>
<li>Krebs on Security「Felons, Fraudsters Flog Offensive Cybersecurity Startup」 https://krebsonsecurity.com/2026/07/felons-fraudsters-flog-offensive-cybersecurity-startup/</li>
<li>The Hacker News「Poison Claude Sells Discounted Claude Access While Its Operator Sees Every Customer Prompt」 https://thehackernews.com/2026/08/poison-claude-sells-discounted-claude.html</li>
<li>The Hacker News「Over 250 ClickFix Domains Use Browser Fingerprinting to Hide macOS Malware Lures」 https://thehackernews.com/2026/08/over-250-clickfix-domains-use-browser.html</li>
<li>The Hacker News「Veeam, Terraform MCP, Django Patch Critical Flaws, Led by CVSS 10.0 Cross-Tenant Bug」 https://thehackernews.com/2026/08/veeam-terraform-mcp-django-patch.html</li>
<li>Bleeping Computer「CISA warns of hackers exploiting Langflow, N-central, Apache Tomcat flaws」 https://www.bleepingcomputer.com/news/security/cisa-warns-of-hackers-exploiting-langflow-n-central-apache-tomcat-flaws/</li>
<li>Bleeping Computer「Google Blogger locks hundreds of blogs in malware false positive」 https://www.bleepingcomputer.com/news/google/google-blogger-locks-hundreds-of-blogs-in-malware-false-positive/</li>
<li>Bleeping Computer「How AI-powered phishing killed blocklists for good」 https://www.bleepingcomputer.com/news/security/how-ai-powered-phishing-killed-blocklists-for-good/</li>
</ul>

</details>

---

[← 2026-08-06 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
