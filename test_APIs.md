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
- [v3.0 (Preview)](https://westus2.dev.cognitive.microsoft.com/docs/services/5d98695995feb7853f67d6a6/operations/5d9869604be85dee480c8750)  
- [v2.1](https://westus.dev.cognitive.microsoft.com/docs/services/5cd27ec07268f6c679a3e641/operations/56f91f2e778daf14a499f21b)  

***
#### [Custom Vision Service](https://docs.microsoft.com/ja-jp/azure/cognitive-services/Custom-Vision-Service/)
- [v3.2 Training](https://southcentralus.dev.cognitive.microsoft.com/docs/services/Custom_Vision_Training_3.2/operations/5dddfe4dc8d30b100855c608)  
- [v3.0 Prediction](https://southcentralus.dev.cognitive.microsoft.com/docs/services/Custom_Vision_Prediction_3.0/operations/5c82db60bf6a2b11a8247c15)  

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
Speech Service はさらに複数のサービス、機能に分かれます。利用可能な REST API の参考サイトを以下に列挙します。サービス、機能の一覧は [こちら](https://docs.microsoft.com/ja-jp/azure/cognitive-services/speech-service/overview) をご確認ください。  
- [Speech to Text - 音声テキスト変換](https://docs.microsoft.com/ja-jp/azure/cognitive-services/speech-service/rest-speech-to-text)  
- [Text to Speech - テキスト読み上げ](https://docs.microsoft.com/ja-jp/azure/cognitive-services/speech-service/rest-text-to-speech)  
- [Conversation transcription - 会話の文字おこし (Preview)](https://signature.centralus.cts.speech.microsoft.com/UI/index.html)


***
#### [Speaker Recognition (Preview)](https://docs.microsoft.com/ja-jp/azure/cognitive-services/speaker-recognition/home)
- [v1.0 (Preview)](https://westus.dev.cognitive.microsoft.com/docs/services/563309b6778daf02acc0a508/operations/5645c3271984551c84ec6797)  

***
#### [Language Understanding - LUIS](https://docs.microsoft.com/ja-jp/azure/cognitive-services/luis/)
利用可能な REST API の仕様について [こちら](https://docs.microsoft.com/ja-jp/azure/cognitive-services/luis/developer-reference-resource#rest-specifications) を参照ください。  
- [v3.0 オーサリング (preview)](https://westeurope.dev.cognitive.microsoft.com/docs/services/luis-programmatic-apis-v3-0-preview/operations/5890b47c39e2bb052c5b9c2f)  
- [v3.0 予測](https://westus.dev.cognitive.microsoft.com/docs/services/luis-endpoint-api-v3-0/operations/5cb0a91e54c9db63d589f433)  
- [v2.0 オーサリング](https://westus.dev.cognitive.microsoft.com/docs/services/5890b47c39e2bb17b84a55ff/operations/5890b47c39e2bb052c5b9c2f)  
- [v2.0 予測](https://westus.dev.cognitive.microsoft.com/docs/services/5819c76f40a6350ce09de1ac/operations/5819c77140a63516d81aee78)  

***
#### [QnA Maker](https://docs.microsoft.com/ja-jp/azure/cognitive-services/qnamaker/)
- [v4.0 Alterations](https://docs.microsoft.com/ja-jp/rest/api/cognitiveservices/qnamaker/alterations)  
- [v4.0 Endpoint Keys](https://docs.microsoft.com/ja-jp/rest/api/cognitiveservices/qnamaker/endpointkeys)  
- [v4.0 Endpoint Settings](https://docs.microsoft.com/ja-jp/rest/api/cognitiveservices/qnamaker/endpointsettings)  
- [v4.0 Knowledgebase](https://docs.microsoft.com/ja-jp/rest/api/cognitiveservices/qnamaker/knowledgebase)  
- [v4.0 Operations](https://docs.microsoft.com/ja-jp/rest/api/cognitiveservices/qnamaker/operations)  
- [v4.0 Runtime](https://docs.microsoft.com/ja-jp/rest/api/cognitiveservices/qnamakerruntime/runtime)  

***
#### [Text Analytics](https://docs.microsoft.com/ja-jp/azure/cognitive-services/text-analytics/)
- [v3.0 (Preview)](https://westus.dev.cognitive.microsoft.com/docs/services/TextAnalytics-v3-0-Preview-1/operations/Languages)  
- [v2.1](https://westcentralus.dev.cognitive.microsoft.com/docs/services/TextAnalytics-v2-1/operations/56f30ceeeda5650db055a3c7)  

***
#### [Anomaly Detector (Preview)](https://docs.microsoft.com/ja-jp/azure/cognitive-services/anomaly-detector/)
- [v1.0 (Preview)](https://westus2.dev.cognitive.microsoft.com/docs/services/AnomalyDetector/operations/post-timeseries-entire-detect)  

***
#### [Content Moderator](https://docs.microsoft.com/ja-jp/azure/cognitive-services/content-moderator/)
- [v1.0 Moderate](https://westus.dev.cognitive.microsoft.com/docs/services/57cf753a3f9b070c105bd2c1/operations/57cf753a3f9b070868a1f66c)  
- [v1.0 Review](https://westus.dev.cognitive.microsoft.com/docs/services/580519463f9b070e5c591178/operations/580519483f9b0709fc47f9c5)  

***
#### [Personalizer](https://docs.microsoft.com/ja-jp/azure/cognitive-services/personalizer/)
- [v1.0](https://westus2.dev.cognitive.microsoft.com/docs/services/personalizer-api/operations/Rank)  

***
<br>
※ このページは 2020 年 5 月 1 日に更新しました。