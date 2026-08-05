---
title: "セキュリティニュース 2026-08-05"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# セキュリティニュース 2026-08-05

**2026-08-05 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-05-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-05-security)

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース 2026年8月5日</h1>
<p>キーワード: 水道インフラ攻撃, ホテルWi-Fi侵入, npmサプライチェーン, MFA回避フィッシング, Rails脆弱性, AIエージェント乗っ取り</p>
<h2>オープニング：2026年8月5日 — セキュリティニュース</h2>
<p>今日は、ホテルのWi-Fi経由で企業アカウントを狙う国家系ハッカー、水道インフラを狙うイラン関連の攻撃、そして20億回もダウンロードされてきたnpmパッケージ群への侵入まで、生活インフラと開発現場の両方に迫る話題を取り上げます。</p>
<h2>ホテルの公衆Wi-Fiから侵入、ロシア系ハッカーがMicrosoft 365を乗っ取る</h2>
<ul>
<li>Microsoftは、宿泊施設のWi-Fiネットワークを狙った世界規模の攻撃キャンペーンを、ロシアの国家系ハッカー集団「Midnight Blizzard」(別名APT29)によるものと断定した。</li>
<li>攻撃者は独自開発のマルウェアを使い、ホテルの公衆Wi-Fiに接続した利用者からMicrosoft 365アカウントの情報を窃取していたとみられる。</li>
<li>出張先でホテルのフリーWi-Fiに接続して会社のメールを開く、という行動は多くの会社員に心当たりがある。海外出張や国際会議に参加する人は、ホテルのWi-Fiではなく会社支給のモバイル回線やVPNを使う習慣が重要になる。</li>
</ul>
<h2>米ミネソタ州の水道施設への攻撃、イランとの関連が内部文書で判明</h2>
<ul>
<li>水道事業者向けの情報共有組織「WaterISAC」が作成した内部文書で、米ミネソタ州の複数の水道施設に対する一連のサイバー攻撃が、イラン(テヘラン)と関連づけられていることが分かった。</li>
<li>同時期には米国内の7つの州で水道システムがイラン関連とみられる攻撃を受けたとする報道もあり、水道という生活インフラへの攻撃が一過性でなく広範囲に及んでいる可能性がある。</li>
<li>水道や電力といった社会インフラは個人が直接守れるものではないが、こうした攻撃が現実に起きていると知っておくことは、断水などの異常時に「まず落ち着いて自治体の発表を確認する」という心構えにつながる。</li>
</ul>
<h2>自己増殖型マルウェア「ChainDrop」、月間20億ダウンロードのnpmパッケージ群に侵入</h2>
<ul>
<li>ソフトウェア部品を配布する「npm」レジストリで、自己増殖(自分で他のパッケージにも感染を広げる)型のマルウェア「ChainDrop」が確認され、合計で月間20億回以上ダウンロードされている1,300以上のパッケージに感染を広げた。</li>
<li>感染したパッケージ自体に気づかず組み込んでいる開発者は多く、被害の全容はまだ確認が進んでいる段階とみられる。</li>
<li>直接npmを使わない人でも、自分が使っているスマホアプリやWebサービスの裏側でこうした部品が使われていることは珍しくない。開発に関わる人は依存パッケージの更新履歴やバージョン固定(意図せぬ自動更新を防ぐ設定)を見直す必要がある。</li>
</ul>
<h2>フィッシングサービス「Greatness」がMFAを回避する新手口を追加</h2>
<ul>
<li>商用のフィッシング代行サービス「Greatness」が、正規のOAuth認証の仕組み(デバイスコード認証)を悪用してMFA(多要素認証)を回避し、Microsoft 365アカウントを乗っ取る新機能を追加した。</li>
<li>ビジネスチャットツール「RingCentral」になりすました偽の通知を送り、被害者を偽ログイン画面に誘導する手口も確認されている。</li>
<li>MFAは有効な対策として広く推奨されているが、今回のように「正規の認証手順そのもの」を悪用されると、指示された通りに操作しただけで乗っ取られてしまう。見慣れないアプリ連携や認証コードの入力を求められたら、送信元が本当に業務上のツールか一呼吸置いて確認することが重要。</li>
</ul>
<h2>偽のAdobe・Zoomアップデート通知で遠隔操作ツールを仕込む攻撃「SMOKE#SCREEN」</h2>
<ul>
<li>Adobeやビデオ会議ツール「Zoom」のアップデート、業務書類の確認、システムメンテナンスを装った偽の通知を使い、遠隔操作用ソフト「ConnectWise ScreenConnect」をひそかにインストールさせる攻撃キャンペーン「SMOKE#SCREEN」が確認された。</li>
<li>複数の手口を組み合わせた多段階のキャンペーンで、正規のソフト更新に見せかけて持続的な遠隔操作の足がかりを作る点が特徴。</li>
<li>「アップデートしてください」というポップアップは日常的に目にするものだからこそ油断しやすい。ソフトの更新は必ず公式アプリ内の通知やメーカー公式サイトから行い、メールやWebサイトの通知ボタンから直接実行しないことが基本になる。</li>
</ul>
<h2>Ruby on Railsの「Active Storage」に緊急の脆弱性、遠隔からのコード実行に注意</h2>
<ul>
<li>JPCERT/CCは、Webアプリ開発フレームワーク「Ruby on Rails」のファイル管理機能「Active Storage」に、遠隔からのコード実行につながる脆弱性(CVE-2026-66066、通称「KindaRails2Shell」)があるとして注意喚起を出した。</li>
<li>悪用されると、遠隔の攻撃者が細工したファイルをアップロードすることで、サーバー上のファイルや認証情報を読み取られたり、遠隔からコードを実行されたりする恐れがある。</li>
<li>Ruby on Railsは日本国内でも多くのWebサービスの土台に使われている。自分が直接開発していなくても、利用しているサービスの運営元が迅速に対応しているかどうかが、自分の個人情報の安全にも直結する。</li>
</ul>
<h2>TP-Linkのネットワーク機器「Omada」に15件の脆弱性、連鎖でRCEの恐れ</h2>
<ul>
<li>TP-Linkは、法人向けネットワーク機器「Omada」シリーズの自動設定機能(ゼロタッチプロビジョニング)に見つかった15件の脆弱性を修正した。</li>
<li>これらは単独では深刻度が低くても、過去に見つかった別の脆弱性と組み合わせる(連鎖させる)ことで、遠隔からのコード実行(RCE)に発展する恐れがあった。</li>
<li>家庭用ルーターと同じメーカーの法人向け機器で見つかった脆弱性であり、小規模オフィスや店舗でOmada製品を使っている場合はファームウェアの更新状況を確認しておきたい。</li>
</ul>
<h2>GoogleのAIエージェント開発キットに脆弱性、GitHubの投稿だけで権限のあるAIを操作可能に</h2>
<ul>
<li>Googleは、AIエージェントを構築するための開発キット「Agent Development Kit(ADK)」のPythonリポジトリから、3つのワークフローを削除した。</li>
<li>セキュリティ企業Pillar Securityは、誰でも書き込める公開のGitHub上の課題(issue)への投稿だけで、権限を持つ「コード修正エージェント」を勝手に起動できてしまう欠陥を実証した。AIが人間の指示と、悪意ある第三者の投稿を区別できなかったことが原因。</li>
<li>AIエージェントに「見るだけ」ではなく「実行する権限」まで持たせる企業が増えているが、今回のように第三者の入力を鵜呑みにして強い権限を発動してしまう設計は今後も繰り返し起こりうる。AIエージェント導入を検討する企業は、権限の範囲を最小限に絞ることが欠かせない。</li>
</ul>
<h2>まとめ</h2>
<p>今日は、ホテルのWi-Fiや水道インフラという「生活の中の当たり前」を狙う国家系の攻撃から、月間20億ダウンロードのnpmパッケージ群を汚染したマルウェア、正規の認証手順そのものを悪用するフィッシングまで見てきました。共通しているのは、攻撃者が「普段は疑わない正規の仕組み」を悪用している点です。アップデート通知や認証手続きは、送信元と経路を一呼吸おいて確認する習慣が今日一番の教訓です。</p>
<h2>参考ソース</h2>
<ul>
<li>Bleeping Computer「Hotel Wi-Fi attacks use custom malware to breach Microsoft 365 accounts」 https://www.bleepingcomputer.com/news/security/hotel-wi-fi-attacks-use-custom-malware-to-breach-microsoft-365-accounts/</li>
<li>Wired Security「A Leaked Memo Ties Cyberattacks on Minnesota Water Utilities to Iran」 https://www.wired.com/story/a-leaked-memo-ties-cyberattacks-on-minnesota-water-utilities-to-iran/</li>
<li>Wired Security「7 States' Water Systems Hit by Cyberattacks Likely Tied to Iran」 https://www.wired.com/story/security-news-this-week-7-states-water-systems-hit-by-cyberattacks-likely-tied-to-iran/</li>
<li>Bleeping Computer「Massive ChainDrop npm supply-chain attack infects hundreds of packages」 https://www.bleepingcomputer.com/news/security/massive-chaindrop-npm-supply-chain-attack-infects-hundreds-of-packages/</li>
<li>The Hacker News「Greatness PhaaS Adds Device Code Phishing to Bypass MFA and Steal Tokens」 https://thehackernews.com/2026/08/greatness-phaas-adds-device-code.html</li>
<li>Bleeping Computer「Phishing service spoofs RingCentral to steal Microsoft 365 accounts」 https://www.bleepingcomputer.com/news/security/phishing-service-spoofs-ringcentral-to-steal-microsoft-365-accounts/</li>
<li>The Hacker News「Fake Adobe and Zoom Updates Install ScreenConnect for Persistent Remote Access」 https://thehackernews.com/2026/08/fake-adobe-and-zoom-updates-install.html</li>
<li>JPCERT/CC「注意喚起: Ruby on RailsのActive Storageにおけるリモートコード実行につながる脆弱性（CVE-2026-66066）に関する注意喚起」 https://www.jpcert.or.jp/at/2026/at260021.html</li>
<li>Bleeping Computer「TP-Link patches Omada ZTP flaws allowing hackers to breach networks」 https://www.bleepingcomputer.com/news/security/tp-link-patches-omada-ztp-flaws-allowing-hackers-to-breach-networks/</li>
<li>The Hacker News「Google Deletes 3 ADK AI Workflows After Malicious GitHub Issue Could Trigger Privileged Agent」 https://thehackernews.com/2026/08/google-deletes-3-adk-ai-workflows-after.html
</content></li>
</ul>

</details>

---

[← 2026-08-05 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
