---
title: "セキュリティニュース｜さくらインターネット不正アクセス・136万件流出か【2026/08/20】"
layout: default
---

<script>
MathJax = { tex: { inlineMath: [['$','$'],['\\(','\\)']], displayMath: [['$$','$$'],['\\[','\\]']], processEscapes: true } };
</script>
<script src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-chtml.js" async></script>

# セキュリティニュース｜さくらインターネット不正アクセス・136万件流出か【2026/08/20】

**2026-08-20 / セキュリティニュース**

<audio controls src="https://archive.org/download/news-pickup-2026-08-20-security/security_yukkuri.m4a" style="width:100%;margin-top:4px"></audio>

- [Internet Archive](https://archive.org/details/news-pickup-2026-08-20-security)

---

## 概要

2026年8月20日のセキュリティニュース。固有名詞、数字、当事者の声を軸に、ずんだもんと四国めたんが解説します。

▼ 今日のトピック
・さくらインターネット、営業管理システムに不正アクセス 最大136万件の顧客情報流出の可能性
・米ヘルステック企業CareCloud、患者370万人分のデータ漏洩が判明
・監視カメラメーカーDahua製、1万4500台超が35日間で乗っ取られる「CameraSwarm」攻撃
・パスワードスプレー攻撃が155倍に急増、多要素認証の抜け穴を突く
・米、知的財産窃盗34億ドル相当でイラン人ハッカー17人を起訴
・Citrix NetScaler ADC/Gatewayに未認証リモートコード実行の脆弱性、JPCERT/CCが注意喚起

#ニュース #ゆっくり解説 #ずんだもん #四国めたん

---

<details>
<summary>スライド（クリックで展開）</summary>

<h1>セキュリティニュース（2026年8月20日）</h1>
<p><strong>キーワード:</strong> さくらインターネット漏洩 / CareCloud患者データ流出 / Dahuaカメラ乗っ取り / パスワードスプレー急増 / イラン人ハッカー起訴 / NetScaler脆弱性</p>
<h2>オープニング：2026年8月20日 — セキュリティニュース</h2>
<ul>
<li>本日は国内クラウド大手さくらインターネットの顧客情報流出、米ヘルステック企業の患者370万人分データ漏洩、監視カメラ1万4500台の乗っ取り、パスワードスプレー攻撃の155倍急増、知的財産窃盗でのイラン人17人起訴まで7本を取り上げる</li>
</ul>
<h2>さくらインターネット、営業管理システムに不正アクセス 最大136万件の顧客情報流出の可能性</h2>
<ul>
<li>国内クラウド・データセンター大手のさくらインターネットは、顧客の契約情報や会員情報を保管する営業管理システムに外部から不正アクセスがあったと発表した</li>
<li>影響を受けた可能性があるのは最大136万件のアカウント情報。氏名、連絡先、契約内容などが対象とみられる</li>
<li>国内利用者が多いクラウドサービス事業者での大規模漏洩となり、同社を利用する法人・個人は今後の公式発表を確認し、不審な連絡やなりすましメールに注意する必要がある</li>
</ul>
<h2>米ヘルステック企業CareCloud、患者370万人分のデータ漏洩が判明</h2>
<ul>
<li>米国の医療IT企業CareCloudは、今年前半に発生していたデータ漏洩事件について、影響を受けた患者数が370万人以上に達したと発表した</li>
<li>CareCloudは電子カルテや請求管理などを扱う医療機関向けシステムを提供しており、漏洩したデータには患者の医療・個人情報が含まれるとみられる</li>
<li>「つまりどういうこと？」といえば、自分がかかった病院がCareCloudのシステムを使っていた場合、直接契約していなくても情報が漏れる可能性があるということ。米国の医療機関を利用したことがある人は通知の有無を確認する必要がある</li>
</ul>
<h2>監視カメラメーカーDahua製、1万4500台超が35日間で乗っ取られる「CameraSwarm」攻撃</h2>
<ul>
<li>セキュリティ研究者が「CameraSwarm」と名付けた大規模攻撃で、中国メーカーDahua製のネットワークカメラ1万4500台以上が、35日間にわたる攻撃で乗っ取られたことが判明した</li>
<li>被害はウクライナとロシアに集中しており、認証情報を使い回す攻撃、認証回避、機器間の直接通信（P2P）機能の悪用など複数の手口が組み合わされていた</li>
<li>「監視カメラが乗っ取られるとどうなるのだ？」といえば、映像そのものを盗み見られるだけでなく、乗っ取った大量のカメラを別の攻撃の踏み台（ボット）として悪用される危険がある。家庭・企業でネットワークカメラを使う場合はパスワードの使い回しを避け、初期設定のまま使わないことが対策になる</li>
</ul>
<h2>パスワードスプレー攻撃が155倍に急増、多要素認証の抜け穴を突く</h2>
<ul>
<li>セキュリティ企業Huntressの調査によると、2026年上半期にパスワードスプレー攻撃（少数のよくあるパスワードを多数のアカウントに順番に試す手口）が前年比155倍に急増した</li>
<li>ある攻撃キャンペーンでは、わずか2週間で8100万回超のログイン試行が観測された</li>
<li>攻撃者は古い認証方式や、多要素認証（MFA）が設定されていないログイン経路の抜け穴を突いていた。「パスワードを強くするだけでは足りないのだ？」という点が今回の核心で、組織側は古い認証プロトコルを無効化し、すべてのログイン経路にMFAを適用することが対策になる</li>
</ul>
<h2>米、知的財産窃盗34億ドル相当でイラン人ハッカー17人を起訴</h2>
<ul>
<li>米司法省は、ハッキング請負業者「Mabna Institute」の関係者とされるイラン人17人を、米国の企業・大学から長年にわたりデータを盗んだ罪などで起訴した</li>
<li>被害総額は知的財産だけで34億ドル（約5000億円）相当にのぼるとされ、研究データや企業秘密が標的になっていた</li>
<li>「なぜ大学まで狙われるのだ？」といえば、大学は先端研究データを保有しながら企業ほどセキュリティ対策が手厚くない場合が多く、国家の後ろ盾を持つ攻撃者にとって狙いやすい標的になっているため</li>
</ul>
<h2>Citrix NetScaler ADC/Gatewayに未認証リモートコード実行の脆弱性、JPCERT/CCが注意喚起</h2>
<ul>
<li>JPCERT/CCは、Citrix NetScaler ADCおよびNetScaler Gatewayにおけるヒープベースのバッファオーバーフローの脆弱性（CVE-2026-8452）について注意喚起を出した</li>
<li>セキュリティ企業watchTowr Labsが8月14日に詳細分析を公表。この脆弱性は2026年6月30日に公表されたサービス運用妨害（DoS）につながる脆弱性と関連するとみられ、機器がSAML SPまたはIdPとして構成されている場合、認証なしでリモートコード実行につながる可能性がある</li>
<li>NetScaler ADC/Gatewayは企業のリモートアクセスや認証基盤として広く使われており、該当機能を有効にしている組織は修正の適用状況を優先的に確認する必要がある</li>
</ul>
<h2>まとめ</h2>
<ul>
<li>本日は国内外の大規模データ漏洩（さくらインターネット、CareCloud）と、認証の弱点を突く攻撃（パスワードスプレー、NetScaler）が並んだ一日だった</li>
<li>個人でできる備えは、利用サービスからの通知メールの確認、パスワードの使い回しをやめること、ネットワーク機器の初期パスワード変更の3点</li>
</ul>
<h2>参考ソース</h2>
<ul>
<li><a href="https://www.bleepingcomputer.com/news/security/sakura-internet-hack-exposes-data-of-up-to-136-million-accounts/">Sakura Internet hack exposes data of up to 1.36 million accounts - Bleeping Computer</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/healthtech-firm-carecloud-data-breach-impacts-37-million-patients/">Healthtech firm CareCloud data breach impacts 3.7 million patients - Bleeping Computer</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/hackers-compromise-14-500-dahua-web-cameras-in-35-day-campaign/">Hackers compromise 14,500 Dahua web cameras in 35-day campaign - Bleeping Computer</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/password-spraying-attacks-surge-155x-as-hackers-exploit-mfa-gaps/">Password spraying attacks surge 155x as hackers exploit MFA gaps - Bleeping Computer</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/us-charges-iranian-hackers-over-34-billion-intellectual-property-theft/">US charges Iranian hackers over $3.4 billion intellectual property theft - Bleeping Computer</a></li>
<li><a href="https://www.jpcert.or.jp/at/2026/at260024.html">注意喚起: NetScaler ADCおよびNetScaler Gatewayにおけるリモートコード実行につながる脆弱性（CVE-2026-8452）に関する注意喚起 - JPCERT/CC</a></li>
</ul>

</details>

---

[← 2026-08-20 の一覧に戻る](../)

---

*音声合成: [VOICEVOX](https://voicevox.hiroshiba.jp/) / キャラクター: [ずんだもん](https://zunko.jp/) ・ [四国めたん](https://zunko.jp/)*
