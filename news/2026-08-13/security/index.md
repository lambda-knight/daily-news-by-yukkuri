---
title: "Windowsゼロデイ悪用中、今すぐ確認する6対策【2026/08/13】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# Windowsゼロデイ悪用中、今すぐ確認する6対策【2026/08/13】

**2026-08-13 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-13-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-13-security)

---

## 概要

LazarusのWindowsゼロデイ、vCenter攻撃、悪性LiteLLM、Androidカード中継、偽VPN拡張737本、不正USBを技術条件と具体対策まで解説します。

▼ 参考ソース
https://www.bleepingcomputer.com/news/security/lazarus-hackers-exploited-windows-zero-day-to-target-defense-firms/
https://thehackernews.com/2026/08/attackers-exploit-vmware-vcenter.html
https://thehackernews.com/2026/08/malicious-litellm-releases-tied-to.html
https://www.bleepingcomputer.com/news/security/android-malware-combo-takes-out-loans-and-relays-victims-credit-cards/
https://www.bleepingcomputer.com/news/security/hundreds-of-fake-chrome-vpn-extensions-route-traffic-through-a-proxy/
https://www.bleepingcomputer.com/news/security/plug-and-pwn-attack-uses-fake-usb-devices-for-windows-system-access/

#サイバーセキュリティ #脆弱性 #Windows #マルウェア #情報セキュリティ #ずんだもん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年8月13日）</h1>
<p><strong>キーワード:</strong> Windowsゼロデイ / vCenter / LiteLLM / Android不正送金 / Chrome拡張 / 不正USB</p>
<h2>オープニング：2026年8月13日 — セキュリティニュース</h2>
<p>本日は、攻撃確認済みのWindowsとVMware vCenter、LiteLLM供給網攻撃、Androidのカード中継、偽VPN拡張、不正USB機器の6件を扱う。直近回の月例更新全体ではなく、侵入条件と優先対策へ焦点を移した。</p>
<h2>LazarusがWindowsゼロデイでSYSTEM権限を取得</h2>
<ul>
<li>北朝鮮系LazarusがCVE-2026-68820を悪用し、フランス、ドイツ、ブラジル、インドの防衛・航空宇宙企業を標的にした。</li>
<li>Operation Dream Job系列で、Windowsの最高権限SYSTEMを得て新型バックドアを展開する。</li>
<li>Windows更新を適用し、採用連絡の文書・リンクを隔離環境で開く。管理者は不審なプロセス生成と永続化を調査する。</li>
</ul>
<h2>VMware vCenterのCVE-2026-59310が実際に悪用</h2>
<ul>
<li>CVSS 9.8のディレクトリトラバーサル脆弱性が攻撃され、ネットワーク到達可能な攻撃者が任意コード実行と永続アクセスを得る恐れがある。</li>
<li>vCenterは仮想基盤全体を管理するため、侵害時の影響は単一サーバーにとどまらない。</li>
<li>修正版を適用し、管理画面を直接公開しない。管理経路をVPN・許可リスト・多要素認証で限定し、侵害痕跡も確認する。</li>
</ul>
<h2>悪性LiteLLMパッケージ、2,100超組織に潜在影響</h2>
<ul>
<li>3月にPyPIへ公開された2つの悪性LiteLLM版は約40分間、クラウド鍵、SSH鍵、Kubernetesトークン、DBパスワードを窃取するコードを含んだ。</li>
<li>約43万4,000ファイルの窃取データから、2,100超の組織に潜在的な露出があると分析された。</li>
<li>導入履歴をロックファイルとCIログで調べ、秘密情報を失効・再発行する。パッケージ名だけでなくハッシュを固定する。</li>
</ul>
<h2>AndroidのWindRelay、カード情報をリアルタイム中継</h2>
<ul>
<li>NFC中継マルウェアWindRelayとSpyNoteを組み合わせ、被害者のカード情報をリアルタイム転送し、融資まで受ける攻撃が報告された。</li>
<li>NFC中継は番号保存だけでなく、正規端末と決済端末の通信を遠隔で橋渡しする。</li>
<li>不明APKを入れず、アクセシビリティと端末管理者権限を確認する。金融通知と利用上限を有効にし、不審時はカード停止を優先する。</li>
</ul>
<h2>偽Chrome VPN拡張737本、通信を単一プロキシへ転送</h2>
<ul>
<li>少なくとも40の開発者アカウントから737本が公開され、7万5,486件の導入を確認。274本は66ブランドを偽装した。</li>
<li>無料VPNでも、通信が運営者のSOCKS5プロキシへ送られれば閲覧やセッションの監視・改変リスクがある。</li>
<li>拡張の提供元と権限を確認し不要品を削除する。削除後も重要サービスのセッション失効とパスワード変更を行う。</li>
</ul>
<h2>Plug and Pwn、不正USBで脆弱ドライバーを導入</h2>
<ul>
<li>偽USB機器でWindowsのプラグ・アンド・プレイを起動し、脆弱なベンダーソフトを自動導入させSYSTEM権限を得る手法が公開された。</li>
<li>物理接触が必要だが、会議室、受付、共有端末、出張先では短時間の接続でも成立しうる。</li>
<li>デバイスインストール制限とドライバー許可リストを使い、未承認USBを遮断する。拾得物や出所不明USBを挿さない。</li>
</ul>
<h2>まとめ</h2>
<p>OS、仮想基盤、依存パッケージ、スマホ、拡張、USBという異なる入口から高権限や秘密情報が狙われた。更新に加え、管理面の非公開化、秘密の失効、権限棚卸し、部品固定、物理ポート制御を組み合わせる。</p>
<h2>参考ソース</h2>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/lazarus-hackers-exploited-windows-zero-day-to-target-defense-firms/">BleepingComputer: Lazarus</a></li>
<li><a href="https://thehackernews.com/2026/08/attackers-exploit-vmware-vcenter.html">The Hacker News: vCenter</a></li>
<li><a href="https://thehackernews.com/2026/08/malicious-litellm-releases-tied-to.html">The Hacker News: LiteLLM</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/android-malware-combo-takes-out-loans-and-relays-victims-credit-cards/">BleepingComputer: WindRelay</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hundreds-of-fake-chrome-vpn-extensions-route-traffic-through-a-proxy/">BleepingComputer: Chrome VPN</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/plug-and-pwn-attack-uses-fake-usb-devices-for-windows-system-access/">BleepingComputer: Plug and Pwn</a></li>
</ul>

</details>

---

[← 2026-08-13 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
