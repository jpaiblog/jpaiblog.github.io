---
title: 管理サービスのリージョンについて
date: 2020-03-03 00:00:00
categories:
- QNA Maker
tags:
- QNA Maker 管理サービス
---

QNA Maker の管理サービスについてご説明いたします。
<!-- more -->
<br>

***
QnA Maker サービスの全体構成につきましては下記ドキュメントの図をご参照ください。  
 
- [QnA Maker のリソースを管理する](https://docs.microsoft.com/ja-jp/azure/cognitive-services/qnamaker/how-to/set-up-qnamaker-service-azure)  

   ![QNA Maker](https://jpaiblog.github.io/images/key-management.png)  

この図の中で、Cognitive Services としてのリソースは、QnA Maker Subscription に相当いたします。「5. Manage KB in portal or via APIs」においてポータルを操作して KB を編集した場合には、米国西部リージョンにおいてホストされている API 群が呼び出されます。  

KB を編集する際に、米国西部リージョンにある API のバックエンドから、Web Apps 上でホストされた QnA Maker ランタイムに対してアクセスすることで、Q&A の追加や削除といった操作が実現されております。  

なお、実際の KB のコンテンツ (Q&A、メタデータ等) は Azure Search に保存されており、ユーザーのチャットログは Application Insights に保存されておりますので、顧客データは米国西部リージョンには保存されておりません。  

※ 管理サービスで使用する API の詳細は以下サイトをご参照ください。  
 
- [QnA Maker V4.0](https://westus.dev.cognitive.microsoft.com/docs/services/5a93fcf85b4ccd136866eb37/operations/5ac266295b4ccd1554da75ff)  

KB を公開した後の、ボット等のアプリケーションからの問い合わせ (4. User QnA endpoint in Bot) は GenerateAnswer API が使用されます。これは QnA Maker ランタイム (Web Apps) に対して実行されます。そのため、ユーザーからの問い合わせに応答する場合には、米国西部リージョンを経由することはございません。

※ GenerateAnswer API の詳細は以下サイトをご参照ください。  
 
- [GenerateAnswer API およびメタデータを使って回答を取得する](https://westus.dev.cognitive.microsoft.com/docs/services/5a93fcf85b4ccd136866eb37/operations/5ac266295b4ccd1554da75ff)  


***