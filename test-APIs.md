---
title: Cognitive Serivces で使用する API テスト ページについて
date: 2020-04-30 12:00:00
categories:
- Cognitive Services
tags:
- API
---
Cognitive Serivces の API について、テスト実行用の参考サイトを紹介します。
<!-- more -->
<br>

***
#### はじめに
- Cognitive Serivces の API は複数あります。どのような API があるかは以下サイトを参照ください。  
[Azure Cognitive Services とは](https://docs.microsoft.com/ja-jp/azure/cognitive-services/welcome)  

- Azure REST API のリファレンス サイトより、Cognitive Services の REST API を確認できます。いくつかのサービスは、こちらのサイトから REST API の実行が可能です。  
[Azure REST API Reference](https://docs.microsoft.com/en-us/rest/api/azure/)  
[Azure Cognitive Services REST API reference](https://docs.microsoft.com/en-us/rest/api/cognitiveservices/)  
[Azure Cognitive Services - Bing Search REST API reference](https://docs.microsoft.com/en-us/rest/api/cognitiveservices-bingsearch/)  

- Cognitive Services 関連の API をまとめたサイトにも REST API を実行可能なページが用意されています。https:// に続くリージョンの指定によっては API が用意されていない場合があるため、代表的な 4 リージョンを紹介します。  
[Cognitive Services APIs (westus)](https://westus.dev.cognitive.microsoft.com/docs/services)  
[Cognitive Services APIs (westus2)](https://westus2.dev.cognitive.microsoft.com/docs/services)  
[Cognitive Services APIs (southcentralus)](https://southcentralus.dev.cognitive.microsoft.com/docs/services)  
[Cognitive Services APIs (westeurope)](https://westeurope.dev.cognitive.microsoft.com/docs/services)  

- REST API の実行には API キーが必要になります。以下のサイトから API キーを取得できます。こちらにないサービスについては、各サービスのクイック スタート ページ等から利用方法を参照ください。  
[Cognitive Services を試す](https://azure.microsoft.com/ja-jp/try/cognitive-services/)  

<br>API のテスト実行可能な直リンクを紹介します。Video Indexer, Bing Speech (廃止), Translator Speech (廃止), Translator Text, Bing Search 系 API は含まれません。

***
#### [Computer Vision](https://docs.microsoft.com/ja-jp/azure/cognitive-services/computer-vision/)
- [v3.2-preview.1](https://westus2.dev.cognitive.microsoft.com/docs/services/computer-vision-v3-2-preview-1/operations/5d9869604be85dee480c8750)  
- [v3.1](https://westus2.dev.cognitive.microsoft.com/docs/services/computer-vision-v3-1-ga/operations/56f91f2e778daf14a499f21b)  

***
#### [Custom Vision Service](https://docs.microsoft.com/ja-jp/azure/cognitive-services/Custom-Vision-Service/)
- [Training v3.4-Preview](https://southcentralus.dev.cognitive.microsoft.com/docs/services/Custom_Vision_Training_3.4-preview/operations/5f760168a787531990ba30b2)  
- [Training v3.3](https://southcentralus.dev.cognitive.microsoft.com/docs/services/Custom_Vision_Training_3.3/operations/5eb0bcc6548b571998fddebd)  
- [Prediction v3.1](https://southcentralus.dev.cognitive.microsoft.com/docs/services/Custom_Vision_Prediction_3.1/operations/5eb37d24548b571998fde5f3)  

***
#### [Face](https://docs.microsoft.com/ja-jp/azure/cognitive-services/face/)
- [v1.0](https://westus.dev.cognitive.microsoft.com/docs/services/563879b61984550e40cbbe8d/operations/563879b61984550f30395236)  

***
#### [Form Recognizer (Preview)](https://docs.microsoft.com/ja-jp/azure/cognitive-services/form-recognizer/)
- [v2.0 (Preview)](https://westus2.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-v2-preview/operations/AnalyzeWithCustomForm)  

***
#### [Ink Recognizer (Preview)](https://docs.microsoft.com/ja-jp/azure/cognitive-services/ink-recognizer/)
- [v1.0 (Preview)](https://docs.microsoft.com/en-us/rest/api/cognitiveservices/inkrecognizer/inkrecognizer)  

***
#### [Speech Service](https://docs.microsoft.com/ja-jp/azure/cognitive-services/speech-service/)  
Speech Service はさらに複数のサービス・機能に分かれます。利用可能な REST API の直リンクを以下に列挙します。サービス、機能の一覧は [こちら](https://docs.microsoft.com/ja-jp/azure/cognitive-services/speech-service/overview) をご確認ください。  
- [Speech to Text REST API](https://docs.microsoft.com/ja-jp/azure/cognitive-services/speech-service/rest-speech-to-text)  
  - [v2.0](https://japaneast.dev.cognitive.microsoft.com/docs/services/speech-to-text-api-v2-0/operations/GetTranscription/console)  
  - [v3.0](https://centralus.dev.cognitive.microsoft.com/docs/services/speech-to-text-api-v3-0/operations/CopyModelToSubscription)  
- [Conversation transcription (Preview)](https://signature.centralus.cts.speech.microsoft.com/UI/index.html)
- [Speaker Recognition](https://docs.microsoft.com/ja-jp/rest/api/speakerrecognition/)
***
#### [Speaker Recognition (Preview)](https://docs.microsoft.com/ja-jp/azure/cognitive-services/speaker-recognition/home)
- [v1.0 (Preview)](https://westus.dev.cognitive.microsoft.com/docs/services/563309b6778daf02acc0a508/operations/5645c3271984551c84ec6797)  

***
#### [Language Understanding - LUIS](https://docs.microsoft.com/ja-jp/azure/cognitive-services/luis/)
利用可能な REST API の仕様について [こちら](https://docs.microsoft.com/ja-jp/azure/cognitive-services/luis/developer-reference-resource#rest-specifications) をご確認ください。  
- [v3.0 オーサリング (preview)](https://westeurope.dev.cognitive.microsoft.com/docs/services/luis-programmatic-apis-v3-0-preview/operations/5890b47c39e2bb052c5b9c2f)  
- [v3.0 予測](https://westus.dev.cognitive.microsoft.com/docs/services/luis-endpoint-api-v3-0/operations/5cb0a91e54c9db63d589f433)  
- [v2.0 オーサリング](https://westus.dev.cognitive.microsoft.com/docs/services/5890b47c39e2bb17b84a55ff/operations/5890b47c39e2bb052c5b9c2f)  
- [v2.0 予測](https://westus.dev.cognitive.microsoft.com/docs/services/5819c76f40a6350ce09de1ac/operations/5819c77140a63516d81aee78)  

***
#### [QnA Maker](https://docs.microsoft.com/ja-jp/azure/cognitive-services/qnamaker/)
- [v4.0 Alterations (Get, Replace)](https://docs.microsoft.com/ja-jp/rest/api/cognitiveservices/qnamaker4.0/alterations)  
- [v4.0 Endpoint Keys (Get Keys, Reflesh Keys)](https://docs.microsoft.com/ja-jp/rest/api/cognitiveservices/qnamaker4.0/endpointkeys)  
- [v4.0 Endpoint Settings (Get Settings, Update Settings)](https://docs.microsoft.com/ja-jp/rest/api/cognitiveservices/qnamaker4.0/endpointsettings)  
- [v4.0 Knowledgebase (Create, Delete, Download, Publish, Replace, Update, etc.)](https://docs.microsoft.com/ja-jp/rest/api/cognitiveservices/qnamaker4.0/knowledgebase)  
- [v4.0 Operations (Get Details)](https://docs.microsoft.com/ja-jp/rest/api/cognitiveservices/qnamaker4.0/operations)  
- [v4.0 Runtime (GenerateAnswer, Train)](https://docs.microsoft.com/ja-jp/rest/api/cognitiveservices/qnamaker4.0/runtime)  

***
#### [Text Analytics](https://docs.microsoft.com/ja-jp/azure/cognitive-services/text-analytics/)
- [v3.1-preview.2](https://centralus.dev.cognitive.microsoft.com/docs/services/TextAnalytics-v3-1-Preview-2/operations/Languages)  
- [v3.1-preview.1](https://centralus.dev.cognitive.microsoft.com/docs/services/TextAnalytics-v3-1-Preview-1/operations/Languages)  
- [v3.0](https://centralus.dev.cognitive.microsoft.com/docs/services/TextAnalytics-v3-0/operations/Languages)  
- [v2.1](https://centralus.dev.cognitive.microsoft.com/docs/services/TextAnalytics-v2-1/operations/56f30ceeeda5650db055a3c7)  

***
#### [Anomaly Detector (Preview)](https://docs.microsoft.com/ja-jp/azure/cognitive-services/anomaly-detector/)
- [v1.0 (Preview)](https://westus2.dev.cognitive.microsoft.com/docs/services/AnomalyDetector/operations/post-timeseries-last-detect)  

***
#### [Content Moderator](https://docs.microsoft.com/ja-jp/azure/cognitive-services/content-moderator/)
- [Content Moderator API リファレンス](https://docs.microsoft.com/ja-jp/azure/cognitive-services/content-moderator/api-reference)
  - [Content Moderator (Image, Text)](https://westus.dev.cognitive.microsoft.com/docs/services/57cf753a3f9b070c105bd2c1/operations/57cf753a3f9b070868a1f66c)  
  - [List Management](https://westus.dev.cognitive.microsoft.com/docs/services/57cf755e3f9b070c105bd2c2/operations/57cf755e3f9b070868a1f675)  
  - [Review (Job, Review, Workflow)](https://westus.dev.cognitive.microsoft.com/docs/services/580519463f9b070e5c591178/operations/5813b4103f9b0711b43c5c67)

***
#### [Metrics Advisor (Preview)](https://docs.microsoft.com/ja-jp/azure/cognitive-services/metrics-advisor/)
- [v1.0 (Preview)](https://westus2.dev.cognitive.microsoft.com/docs/services/MetricsAdvisor/operations/createDataFeed)

***
#### [Personalizer](https://docs.microsoft.com/ja-jp/azure/cognitive-services/personalizer/)
- [v1.0](https://westus2.dev.cognitive.microsoft.com/docs/services/personalizer-api/operations/Rank)  

***
`変更履歴`  
`2020/04/30 created by Mochizuki`  
`2020/05/01 modified by Mochizuki`  
`2020/10/19 modified by Mochizuki`  
`2020/11/02 modified by Mochizuki`  