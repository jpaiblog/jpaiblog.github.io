---
title: Azure OpenAI Service の使用中に発生する可能性がある一般的なエラー コードについて
date: 2023-12-29 00:00:00
categories:
- Azure OpenAI
tags:
- Azure OpenAI
---
この記事では、Azure OpenAI Service の使用中に発生する可能性がある一般的なエラー コードの内容や原因、解決策についてご紹介します。 

<!-- more -->
<br>

***

## HTTP 400 エラー / Bad Request

このエラーは、クライアント側から送信したリクエストに問題があることを示します。<br/>
原因として、プロンプトの誤入力、プロンプトがコンテンツフィルターによりブロックされている可能性が挙げられます。

**対処方法：** 
- クライアント側から送信したプロンプトを見直してください（Jsonペイロードの形式や、パラメーターのミススペルなど）
- [コンテンツのフィルター処理](https://learn.microsoft.com/ja-jp/azure/ai-services/openai/concepts/content-filter?tabs=warning%2Cpython) の設定を確認し、必要に応じてレベルを調整してください。


## HTTP 401 エラー / Unauthorized

このエラーは、認証に問題が発生していることを示します。 <br/>
原因として、Azure OpenAI Service へのリクエストに必要な API キーなどの認証情報に誤りがある可能性が挙げられます。  <br/>
 <br/>
 例：リクエスト時にキーが含まれていない、キーに余分なスペースや欠落文字がある、アクセス トークンの有効期限が切れている、必要なロールが割り当てられていない 
 
**対処方法：** 
API キー 認証をご使用の場合は、リクエスト時に必要なENDPOINT, API-KEY, DEPLOYMENT-NAME が正しいかどうかをご確認ください。 
確認方法は、以下の公開情報をご参照ください。 
 
- [キーとエンドポイントを取得する | クイック スタート: Azure OpenAI Service を使用してテキストの生成を開始する](https://learn.microsoft.com/ja-jp/azure/ai-services/openai/quickstart?tabs=command-line%2Cpython&pivots=rest-api#retrieve-key-and-endpoint ) 

Microsoft Entra ID 認証をご使用の場合は、リクエストを行うユーザーに対して、必要なロールが割り当たっているかどうかをご確認ください。 
詳細は、以下の公開情報をご参照ください。 
 
- [Cognitive Services User ロールに自分自身を割り当てる | マネージド ID を使用して Azure OpenAI Service を構成する方法](https://learn.microsoft.com/ja-jp/azure/ai-services/openai/how-to/managed-identity) 

## HTTP 403 エラー / Forbidden

このエラーは、ネットワーク制限により生じている可能性があります。

**対処方法：**

- [Azure OpenAI Service リソースに設定したネットワーク設定](https://learn.microsoft.com/ja-jp/azure/ai-services/cognitive-services-virtual-networks?context=%2Fazure%2Fai-services%2Fopenai%2Fcontext%2Fcontext&tabs=portal#manage-default-network-access-rules) を確認します。

## HTTP 404 エラー / Not Found 

このエラーは、クライアント側の要求で指定されたリソースが、サーバー側で見つけられなかったことを示します。 <br />
原因として、API エンドポイントが正しくないといったことが挙げられます。 
 
**対処方法：**


- [API リファレンス](https://learn.microsoft.com/ja-jp/azure/ai-services/openai/reference) や SDK リファレンスを参照し、API エンドポイントの指定が正しいことを確認します。
- エンドポイント指定時の必須パラメーターを確認します。
（リソース名、デプロイメントID、API バージョン（後述））
- API バージョン（モデルバージョンとは異なります）が正しいかどうかをご確認ください。 (API エンドポイントは、指定された要求が正しく最新であることを確認するために、バージョン管理に api-version クエリ パラメーターを使用しており、サービス API のすべてのバージョンは、YYYY-MM-DD の日付構造になっています。 )
> 例）https:// (中略) /openai/deployments/my-first-deployment/completions?api-version=**2022-12-01** 

## HTTP 408 エラー / Request Timeout 

このエラーは、サーバー側の応答がない、ネットワーク接続が不安定などでリクエストがタイムアウトしたことを示します。<br /> 
原因として、クライアント側のインターネット接続の速度が遅い、大きな要求の送信に時間がかかりすぎている、サーバー側に要求の処理に遅延を引き起こす何らかの問題がある、などが挙げられます。 
 
**対処方法：** 
- ご利用のインターネット環境において、リクエストを送信するのに十分な安定性と速度があることをご確認ください。そのうえで、再度リクエストを送信しエラーが解消するかどうかをご確認ください。 
- 大きなクエリが送信されている場合は、要求を複数の小さなクエリに分割することをご検討ください。これにより、Azure OpenAI は情報をより効率的に処理することができ、タイムアウトの可能性が低減します。
- Chat Completions API を使用している場合は、API リクエストを行う際に stream=true を設定することを検討してください。これにより、サーバー側は、部分的な結果が利用可能になったときに送信できるため、タイムアウトの可能性が低減します。 

## HTTP 429 エラー / Too Many Requests

このエラーは、定義されたレート制限を超過していることや、バックエンドサービスがスケーリング中であることを示します。<br/>
原因として、クライアント側からのリクエストのレート制限超過、クライアント側のワークロードの急激な変化の可能性が挙げられます。

**対処方法：** 
- [レート制限内に収まるようにするための一般的なベスト プラクティス](https://learn.microsoft.com/ja-jp/azure/ai-services/openai/quotas-limits#general-best-practices-to-remain-within-rate-limits) を参照します。

***
`変更履歴`  
`2023-12-29 created by Uehara`   

※ 本記事は 「[jpaiblog について](https://jpaiblog.github.io/blog/2020/01/01/about-jpaiblog/)」 の留意事項に準じます。  
※ 併せて 「[ホームページ](https://jpaiblog.github.io/blog/)」 および 「[記事一覧](https://jpaiblog.github.io/blog/archives/)」 もご参照いただければ幸いです。  
