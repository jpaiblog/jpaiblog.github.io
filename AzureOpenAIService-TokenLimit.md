---
title: AzureOpenAIServiceのトークン数の上限について
date: 2023-07-19 00:00:00
categories:
- Azure OpenAI
tags:
- Azure OpenAI
---
この記事は、AzureOpenAIServiceのトークン数の上限についてご紹介します。

<!-- more -->
<br>
<!-- TrackingID#2305290060000459 -->
<!-- TrackingID#2306270060001789 -->


***

## トークン数の上限値(最大要求)とは

Azure OpenAI Service では、モデル毎にトークン数の上限値(最大要求)が設定されています。

モデル毎のトークン数の上限値(最大要求)は、下記ドキュメントに記載されています。

- [Model Summary table and region availability : Max Request (tokens)](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/concepts/models#model-summary-table-and-region-availability) 

## トークン数の上限値(最大要求)を超えた場合の挙動

現在の内部実装では、トークン数の上限値(最大要求)を超えるトークン数でも処理できる場合がございます。  
しかし、本内部実装は予告無く変更される可能性があるため、ドキュメントに記載されているトークン数の上限値(最大要求)を超えないよう利用いただくことを強くお勧めします。

下記ドキュメントでも制限内に留まることを推奨しています。

- [GPT-35-Turbo および GPT-4 モデルの操作方法 : 会話の管理](https://learn.microsoft.com/ja-jp/azure/cognitive-services/openai/how-to/chatgpt?pivots=programming-language-chat-completions#managing-conversations)
  > 注意  
  > すべてのモデルに関する文書化された入力トークンの制限を超えることができる場合でも、その制限内に留まることを強くお勧めします。

## トークン数の上限値(最大要求)を超えないようにする方法

Azure OpenAI Service と同じモデルを開発している OpenAI 社が提供しているライブラリ (tiktoken) により、指定された文章からトークン数を計算することが可能です。

下記ドキュメントでは、過去の会話が長くなり、トークンの合計数が上限 (例では 4096 トークン) を超える場合に、一番古い会話を削除しつつ、上限のトークン数以下の会話を実現する方法についてサンプルコードを交えてご紹介しております。  
API 上でご利用する際の会話の管理の一例として、ご参考にして頂けますと幸いに存じます。

- [ChatGPT および GPT-4 モデルの操作方法の説明#会話の管理](https://learn.microsoft.com/ja-jp/azure/cognitive-services/openai/how-to/chatgpt?pivots=programming-language-chat-completions#managing-convesations)
  > 次のコード サンプルは、OpenAI の tiktoken ライブラリを使用して 4096 トークン数を処理する手法を使用した単純なチャット ループの例を示しています。  

なお、tiktoken 自体はマイクロソフトのサービスの一部ではないため、Azure の技術サポートの範囲外となりますこと、予めご了承いただきますようお願いいたします。

- [openai/tiktoken (GitHub)](https://github.com/openai/tiktoken)

***
`変更履歴`  
`2023/07/19 created by Kudou`   

※ 本記事は 「[jpaiblog について](https://jpaiblog.github.io/blog/2020/01/01/about-jpaiblog/)」 の留意事項に準じます。  
※ 併せて 「[ホームページ](https://jpaiblog.github.io/blog/)」 および 「[記事一覧](https://jpaiblog.github.io/blog/archives/)」 もご参照いただければ幸いです。  
