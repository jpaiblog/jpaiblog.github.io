---
title: お問い合わせ時の留意事項
date: 2025-05-20 00:00:00
categories:
- Cognitive Services
tags:
- はじめに
---
テクニカルサポートチームでは、お客様のお役に立てるよう日々努めていますが、お客様の協力があって初めてご支援が可能となることも多くあります。調査を迅速に開始し、コミュニケーションを円滑に進めるため、以下の点にご協力ください。

<!-- more -->
<br>

### お問い合わせは、事象の発生後できるだけ早くご起票ください
Azure 基盤ログの保存期間には期限があります。 
事象の発生から時間が経つとログが残っておらず、調査ができない場合がありますので、お問い合わせはできるだけ早めにご起票ください。
<br>

### 有償 Azure テクニカル サポートの対応範囲について
有償 Azure テクニカル サポートの対応範囲は原則として、トラブルシューティング (Break fix) です。
個別のお客様に合わせた以下のような詳細サポートの提供はありません。<br>
例）
- お客様の個別的な要件を満たす Azure 製品構成やコードの提案。 
- 設計、アーキテクチャ、コードの レビュー。 
- アプリケーション、パフォーマンス、構成のチューニング。 
- (コーディングの言語やスクリプトの種類に関わらず）カスタム コードのサンプル提供。 

上記のようなご要望については、別途のサポートメニューの利用をご提案させていただく場合があります。
<br>

### お問い合わせの分割起票について
テクニカルサポートでは、各製品の専任エンジニアが担当となり支援を差し上げています。
そのため、以下のようなご質問は可能な限り、内容 (問題や製品) ごとに分割したお問い合わせ起票をお願いします。 

- 特定のサービスが公開している機能の範囲にはない、複数の製品やサービスがかかわる問い合わせ 
  - 対応範囲内の例: Azure OpenAI On Your Data を使用した際の連携先サービスのロール割り当てについて 
  - 製品ごとの問い合わせが必要な例: Azure AI Vision の画像解析と Azure OpenAI Service の Vision 対応モデルの比較 

- 同 API に対する、性質の異なる質問や問い合わせ 
  - 問い合わせ 1: Azure OpenAI Service の Chat Completion API を使用したときに発生したエラーの解消 
  - 問い合わせ 2: Azure OpenAI Service の Chat Completion API で使用する要求パラメーターの詳細に関する確認 

- 同じ種類の問題でも、発生日時など背景状況が異なる問い合わせ 
  - 例: 2025/05/01 に発生した 5xx エラーが、2025/05/02 時点で解消したが、2025/05/04 からまた発生した 

<br>

### お問い合わせの連絡先メールアドレスについて
誤送信防止の観点から、エンジニアが手動でお客様のメールアドレスを追加することをお承りできません。 
もし、お問い合わせにお客様側の案件関係者様などのメールアドレスを追加する必要が生じた場合には、以下のようにご対応ください。 

- Azure ポータルからの起票時、「連絡先情報」-「通知用のその他の電子メール」項目に追加する。<br>※ 複数のメールアドレスがある場合はセミコロン (;) 等で区切って入力可能。

- テクニカルサポート窓口から届いたメールにご返信いただく際に、必要なメールアドレスを追加する。

<br>

### お客様側での情報採取や確認にお時間がかかる場合について
お客様側での情報採取や案内内容の確認などにお時間がかかる場合には、10日程度を目安に、それ以上のお時間が必要な場合には、お問い合わせのクローズにご理解ください。 
テクニカルサポートは、原則として短期的な課題に対して集中した支援を差し上げるサービスとして、数営業日ごとにお客様の状況の確認を実施しています。
<br>

### 長期にわたる修正について
調査の結果、サービス側の改修が必要となることがありますが、修正が長期にわたることが想定される場合は、原則として、お問い合わせをクローズとさせていただきます。 
定期的な修正状況の確認や進捗報告をご希望の場合は、ご確認が必要なタイミングでその都度お問い合わせを起票いただくようお願いします。
<br>

### クローズ後の再開方法について
クローズ後にご質問が発生した場合には、以前のお問い合わせ番号を記載してお問い合わせいただければ、情報を引き継いで支援を再開することが可能です。 
これにより、過去のやり取りを踏まえた上でスムーズにサポートを提供することができます。
<br>

### リリース時期や今後の予定に関するご質問について
新機能のリリース時期や修正の展開時期など、今後の予定に関するご質問には基本的にはお答えできません。 
状況に応じてベストエフォートで開発部門への確認を行い、目安として案内を差し上げることがありますが、案内する時期についてはあくまでもその時点での予定であり、変更となる可能性が多分にあることをご承知おきください。
<br>

### 公開情報の修正依頼・追加依頼について
サポートチームは責任をもってお客様に回答を差し上げていますため、障害発生時や製品に不具合が発生している場合、サポートからの回答をもってマイクロソフトからの正式な案内とさせていただく場合があります。 
公開情報に情報の記載がない場合、サポートチームよりフィードバックすることは可能ですが、情報の記載をお約束することはできかねますのでご了承ください。
<br>

### プレビュー機能について
プレビュー版製品や機能のサポートの前提については、以下の Azure サポート一般の FAQ 内容をご参照ください。 
プレビュー版の公開状況や機能内容は予告なく変更される場合があり、原則として現状有姿 (AS-IS) でのご提供となることをご承知おきください（そのためベストエフォートでのご対応となり、例えばプレビュー版機能への修正ご要望などについては、弊社開発部門へのフィードバックに留まる場合もあります）。<br>
- [Azure サポート プランに関する FAQ](https://azure.microsoft.com/ja-jp/support/faq/)
  >Q. プレビューのサービスや機能とは何ですか? 
  >
  >A. （前略） 
  >Azure のプレビューのサービスや機能には、お客様のサービス契約で規定されているものとは異なる縮小版のサービス条件と、プレビューの追加使用条件が適用されます。 
  >プレビューは、現状のまま、すべての欠点を含み、提供可能な場合に提供され、サービス レベル アグリーメント (SLA) や、Microsoft が一般提供を開始している Azure サービスに対して提供する限定的な保証からは除外されています。

<br>

***
`変更履歴`  
`2025/05/21 created by Uehara`  

※ 本記事は 「[jpaiblog について](https://jpaiblog.github.io/blog/2020/01/01/about-jpaiblog/)」 の留意事項に準じます。  
※ 併せて 「[ホームページ](https://jpaiblog.github.io/blog/)」 および 「[記事一覧](https://jpaiblog.github.io/blog/archives/)」 もご参照いただければ幸いです。  
