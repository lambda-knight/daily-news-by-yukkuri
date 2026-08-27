---
title: "セキュリティニュース 2026-08-27"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# セキュリティニュース 2026-08-27

**2026-08-27 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-27-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-27-security)

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年8月27日）</h1>
<p><strong>キーワード:</strong> ボストン・サイエンティフィック被弾 / QTFY摘発 / SharePoint連鎖攻撃 / Avadaゼロクリック / Ubiquiti最重要脆弱性 / GPUThor</p>
<h2>オープニング：2026年8月27日 — セキュリティニュース</h2>
<ul>
<li>本日は医療機器大手ボストン・サイエンティフィックへのサイバー攻撃、米当局による中国国家系ハッキング基盤「QTFY」の摘発、Microsoft SharePointの連鎖脆弱性が実攻撃入りした件、WordPressの人気テーマAvadaのゼロクリックRCE、Ubiquiti製品の最重要脆弱性3件、NVIDIA GPUへのハードウェア攻撃「GPUThor」、CISAレッドチーム演習が示した防御力の差の7本を扱う。</li>
</ul>
<h2>ボストン・サイエンティフィック、サイバー攻撃で世界規模の業務停止</h2>
<ul>
<li>従業員5万9000人、13の製造施設を127カ国で展開し2025年に年間売上200億ドル超を上げる医療機器大手ボストン・サイエンティフィックが、2026年8月25日にサイバー攻撃を検知し、翌26日に公表した。</li>
<li>同社はネットワーク停止が発生し、一部のオペレーティングシステムやビジネスアプリケーションへのアクセスに支障が出て、顧客注文の処理・出荷能力にも影響したと説明した。患者データの流出やランサムウェア要求の有無は執筆時点で言及がない。</li>
<li>外部サイバーセキュリティ専門家と契約し調査・封じ込めを進めているが、システム復旧の完全なタイムラインは示されていない。ペースメーカーなど生命維持に関わる医療機器メーカーの供給網が止まると、患者の治療スケジュールにも波及しかねない点が焦点になる。</li>
</ul>
<h2>FBI・司法省、中国国家系ハッキング基盤「QTFY」を摘発</h2>
<ul>
<li>米司法省とFBIは2026年8月26日、中国の脅威グループ「QTFY」が運用していた2つのハッキング基盤「QScan」と「QTRouter」の破壊を発表した。QTFYは南京鑫玖维网络科技有限公司に所属し、中国国家安全部（MSS）と人民解放軍（PLA）を顧客に2018年5月から活動していた。</li>
<li>QScanは世界中のIoT機器を自動スキャン・感染させてQTRouterネットワークへ組み込む機能を持ち、QTRouterは侵害済み機器や商用プロキシ、レンタル仮想サーバーを組み合わせて攻撃の発信元を隠すために使われていた。</li>
<li>標的にはNASA、連邦準備制度、エネルギー省、司法省、厚生労働省、国立衛生研究所、米上院など米国の重要機関が含まれ、ゼロデイとNデイの脆弱性で初期侵入したのちQTRouterで持続的アクセスを確保していた。国家が関与する偵察網の摘発でも、代替インフラの再構築には時間がかからない点が今後の課題として残る。</li>
</ul>
<h2>Microsoft SharePointの連鎖脆弱性、公開エクスプロイトで実攻撃入り</h2>
<ul>
<li>SharePointのJWTトークン検証を回避する認証バイパス脆弱性「CVE-2026-55040」と、業務接続サービス（BCS）でのリモートコード実行につながる「CVE-2026-63520」が組み合わされ、8月25日に実際の攻撃で悪用され始めたことが判明した。</li>
<li>CVE-2026-55040のPoCはRapid7の研究者スティーブン・フューワー氏が8月11日に公開し、翌日には脅威インテリジェンス企業Defusedが既に武器化されたことを確認。CVE-2026-63520のPoCはVulnCheckのジョナサン・ピーターソン氏が8月24日に公開した。</li>
<li>Defusedによると、JWT回避の実行後に管理者列挙とBCS探索が確認されているが、コード実行自体はまだ観測されていない。CISAは8月18日に連邦機関へSharePointサーバー保護の緊急命令を出しており、Shadowserverの調査ではインターネットに公開されたSharePointサーバーが8700台以上存在する。</li>
</ul>
<h2>WordPressの人気テーマ「Avada」、未認証でも侵入できるゼロクリックRCE</h2>
<ul>
<li>販売実績100万件超のWordPressテーマ「Avada」と付属プラグイン「Fusion Builder」に、認可・入力検証・信頼境界・ファイル処理の弱点を6段階連鎖させる脆弱性「CVE-2026-18431」が見つかった。深刻度は最高水準の9.8で、認証なしの攻撃者が任意のPHPコードをサーバー上で実行できる。</li>
<li>攻撃は公開リクエストを起点に、匿名ユーザーに制限された機能へ入力を渡し、本来の文脈外で特権コンポーネントを呼び出したうえで、ファイル処理の制限を回避する手順で成立する。両コンポーネントが有効なサイトでのみ悪用が可能となる。</li>
<li>開発元ThemeFusionは既にAvada 7.16.1とFusion Builder 3.16.1で修正版を公開済み。個人ブログから企業サイトまで幅広く使われるテーマだけに、更新の遅れがそのまま被害拡大につながる。</li>
</ul>
<h2>Ubiquiti、UniFi製品の最重要脆弱性3件を修正</h2>
<ul>
<li>ネットワーク機器大手Ubiquitiが、認証なしで悪用できる最大深刻度の脆弱性3件を含む計21件を公表した。監視カメラ管理ソフト「UniFi Protect」の入力検証不備（CVE-2026-77537）は認証なしの攻撃者がデバイスを侵害できる。</li>
<li>UniFi OSデバイス全般に影響するCRLF挿入の脆弱性（CVE-2026-77550）はネットワークにアクセスできる攻撃者が認証をバイパスでき、VoIP電話システム「UniFi Talk」のコマンド注入（CVE-2026-77554）も権限なしで悪用可能だった。</li>
<li>Ubiquitiは「UniFi Protect」を7.2.105以降、「UniFi Talk」を5.3.2以降に更新済みで、影響を受けるのは「UniFi OS Server」5.1.21以前。家庭のWi-Fiルーターから中小企業のネットワークまで広く使われる製品だけに、自動更新設定の確認が実質的な対策になる。</li>
</ul>
<h2>NVIDIA GPUをハードウェアで攻撃する「GPUThor」、ECC保護を突破</h2>
<ul>
<li>トロント大学の研究チームが、メモリセルを繰り返しアクセスしてビット反転を誘発する「Rowhammer」攻撃の新型「GPUThor」を発表した。非均一パターンでGDDR6メモリのTarget Row Refresh防御を回避し、従来の「GPUHammer」より6.6倍多い攻撃行アクティベーションを実現した。</li>
<li>対象はAI・クラウドインフラで広く使われるAmpere世代のワークステーション向けGPU（RTX A4000／A4500／A5000／A6000）。ECC保護なしの環境では1GBあたり7万2000～37万7000件のビット反転を確認し、ECC有効時でも387件の二重ビットエラーと2件の三重ビットエラーが発生した。</li>
<li>悪用可能なビット反転は約1.1分で発見でき、2時間ごとのGPUリセットを強制するDoS攻撃や、GPUページテーブル破損によるroot権限奪取につながる。NVIDIAはSYS-ECC有効化やIOMMU・DMA分離、GPU共有制限、エラー監視を推奨するが、根本対策には将来世代GPUでの多ビットECC強化が必要としている。</li>
</ul>
<h2>CISAレッドチーム演習、同じ手口でも明暗が分かれた2組織</h2>
<ul>
<li>CISAは2026年8月25日、重要インフラの「組織A」（政府サービス・施設）と「組織B」（水道・下水道）に対して同時に実施した侵入テストの結果を公表した。同様の攻撃手口を使ったにもかかわらず、両組織の対応は対照的だった。</li>
<li>組織Aはデフォルト認証情報の残るウェブアプリから侵入され、誤設定されたActive Directory証明書テンプレートで権限昇格、平文保存の認証情報や有効期限なしのAWSアクセスキーで機密システムに到達し、最終的にセキュリティチームのメールまで盗み見された。通常業務由来の偽陽性アラートが数千件あり、実際の攻撃シグナルが埋もれていた。</li>
<li>一方の組織Bは初期フィッシングの実行を検知し、2～20分以内に該当端末を隔離してC2通信を遮断。運用技術（OT）区域のバスティオンホストも外向き通信を遮断していたため侵入拡大を防いだ。CISAは両者の差が技術ツールではなく、それを支える人員・プロセス・手順にあると結論づけている。</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>今日の7本は、医療機器メーカーへの実被害、国家系インフラの摘発、公開エクスプロイトによる実攻撃、広く使われるテーマ・機器の脆弱性、ハードウェアレベルの新型攻撃、そして同じ手口への防御力の差という、攻撃側と防御側双方の動きを並べた。</li>
<li>組織にとってはAvadaやSharePoint、Ubiquitiのようにパッチが出ている脆弱性を放置しないこと、CISAの事例が示すようにアラートの誤検知を減らし権限委譲を整えることが当面の要点になる。</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/boston-scientific-says-cyberattack-disrupted-operations-globally/">BleepingComputer: Boston Scientific says cyberattack disrupted operations globally</a></li>
<li><a href="https://thehackernews.com/2026/08/fbi-disrupts-china-linked-qtfy.html">The Hacker News: FBI Disrupts China-Linked QTFY Infrastructure Used to Steal Data From U.S. Organizations</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-target-microsoft-sharepoint-rce-chain-with-poc-exploit/">BleepingComputer: Hackers target Microsoft SharePoint RCE chain with PoC exploit</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/critical-avada-wordpress-theme-flaw-enables-zero-click-rce/">BleepingComputer: Critical Avada WordPress theme flaw enables zero-click RCE</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/ubiquiti-patches-three-max-severity-security-vulnerabilities/">BleepingComputer: Ubiquiti patches three max severity security vulnerabilities</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/new-gputhor-attack-defeats-nvidia-ecc-protection-for-root-access/">BleepingComputer: New GPUThor attack defeats NVIDIA ECC protection for root access</a></li>
<li><a href="https://thehackernews.com/2026/08/cisa-red-team-compromised-two-critical.html">The Hacker News: CISA Red Team Compromised Two Critical Infrastructure Orgs, One Detected Nothing</a></li>
</ul>

</details>

---

[← 2026-08-27 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
