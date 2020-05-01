---
title: Cognitive Serivces で使用する API テスト ページについて
date: 2020-04-30 12:00:00
categories:
- Cognitive Services
tags:
- API
---
Cognitive Serivces の API について、テスト実行用のサイトを紹介します。
<!-- more -->
<br>

***
#### はじめに
- Cognitive Serivces の API は複数あります。どのような API があるかは以下サイトを参照ください。  
[Azure Cognitive Services とは](https://docs.microsoft.com/ja-jp/azure/cognitive-services/welcome)  

- Azure REST API のリファレンス サイトからも確認いただけます。    
[Azure REST API Reference](https://docs.microsoft.com/en-us/rest/api/azure/)  
[Azure Cognitive Services REST API reference](https://docs.microsoft.com/en-us/rest/api/cognitiveservices/)  
[Azure Cognitive Services - Bing Search REST API reference](https://docs.microsoft.com/en-us/rest/api/cognitiveservices-bingsearch/)  

- Cognitive Services 関連の API をまとめたサイトもあります。https:// に続くリージョンの指定によっては API が用意されていない場合があります。代表的な 4 リージョンを紹介します。  
[Cognitive Services APIs (westus)](https://westus.dev.cognitive.microsoft.com/docs/services)  
[Cognitive Services APIs (westus2)](https://westus2.dev.cognitive.microsoft.com/docs/services)  
[Cognitive Services APIs (southcentralus)](https://southcentralus.dev.cognitive.microsoft.com/docs/services)  
[Cognitive Services APIs (westeurope)](https://westeurope.dev.cognitive.microsoft.com/docs/services)  

<br>
各 API の直リンクを紹介します。  
Video Indexer, Speech Service, Bing Speech (廃止), Translator Speech (廃止), Translator Text, Bing Search 系 API はここに含まれておりません。

***
#### Computer Vision
- [v3.0 (Preview)](https://westus2.dev.cognitive.microsoft.com/docs/services/5d98695995feb7853f67d6a6/operations/5d9869604be85dee480c8750)  
- [v2.1](https://westus.dev.cognitive.microsoft.com/docs/services/5cd27ec07268f6c679a3e641/operations/56f91f2e778daf14a499f21b)  
<details><summary style="font-size: 10pt">使用方法</summary>

</details>

***
#### Custom Vision Service
- [v3.2 Training](https://southcentralus.dev.cognitive.microsoft.com/docs/services/Custom_Vision_Training_3.2/operations/5dddfe4dc8d30b100855c608)  
- [v3.0 Prediction](https://southcentralus.dev.cognitive.microsoft.com/docs/services/Custom_Vision_Prediction_3.0/operations/5c82db60bf6a2b11a8247c15)  
<details><summary style="font-size: 10pt">使用方法</summary>

</details>

***
#### Face
- [v1.0](https://westus.dev.cognitive.microsoft.com/docs/services/563879b61984550e40cbbe8d/operations/563879b61984550f30395236)  
<details><summary style="font-size: 10pt">使用方法</summary>

</details>

***
#### Form Recognizer (Preview)
- [v2.0 (Preview)](https://westus2.dev.cognitive.microsoft.com/docs/services/form-recognizer-api-v2-preview/operations/AnalyzeWithCustomForm)  
<details><summary style="font-size: 10pt">使用方法</summary>

</details>

***
#### Ink Recognizer (Preview)
- [v1.0 (Preview)](https://docs.microsoft.com/en-us/rest/api/cognitiveservices/inkrecognizer/inkrecognizer)  
<details><summary style="font-size: 10pt">使用方法</summary>

</details>

***
#### Speaker Recognition (Preview)
- [v1.0 (Preview)](https://westus.dev.cognitive.microsoft.com/docs/services/563309b6778daf02acc0a508/operations/5645c3271984551c84ec6797)  
<details><summary style="font-size: 10pt">使用方法</summary>

</details>

***
#### Language Understanding - LUIS
- [v3.0 オーサリング (preview)](https://westeurope.dev.cognitive.microsoft.com/docs/services/luis-programmatic-apis-v3-0-preview/operations/5890b47c39e2bb052c5b9c2f)  
- [v3.0 予測](https://westus.dev.cognitive.microsoft.com/docs/services/luis-endpoint-api-v3-0/operations/5cb0a91e54c9db63d589f433)  
- [v2.0 オーサリング](https://westus.dev.cognitive.microsoft.com/docs/services/5890b47c39e2bb17b84a55ff/operations/5890b47c39e2bb052c5b9c2f)  
- [v2.0 予測](https://westus.dev.cognitive.microsoft.com/docs/services/5819c76f40a6350ce09de1ac/operations/5819c77140a63516d81aee78)  
<details><summary style="font-size: 10pt">使用方法</summary>

</details>

***
#### QnA Maker
- [v4.0 Alterations](https://docs.microsoft.com/ja-jp/rest/api/cognitiveservices/qnamaker/alterations)  
- [v4.0 Endpoint Keys](https://docs.microsoft.com/ja-jp/rest/api/cognitiveservices/qnamaker/endpointkeys)  
- [v4.0 Endpoint Settings](https://docs.microsoft.com/ja-jp/rest/api/cognitiveservices/qnamaker/endpointsettings)  
- [v4.0 Knowledgebase](https://docs.microsoft.com/ja-jp/rest/api/cognitiveservices/qnamaker/knowledgebase)  
- [v4.0 Operations](https://docs.microsoft.com/ja-jp/rest/api/cognitiveservices/qnamaker/operations)  
- [v4.0 Runtime](https://docs.microsoft.com/ja-jp/rest/api/cognitiveservices/qnamakerruntime/runtime)  
<details><summary style="font-size: 10pt">使用方法</summary>

</details>

***
#### Text Analytics
- [v3.0 (Preview)](https://westus.dev.cognitive.microsoft.com/docs/services/TextAnalytics-v3-0-Preview-1/operations/Languages)  
- [v2.1](https://westcentralus.dev.cognitive.microsoft.com/docs/services/TextAnalytics-v2-1/operations/56f30ceeeda5650db055a3c7)  
<details><summary style="font-size: 10pt">使用方法</summary>

</details>

***
#### Anomaly Detector (Preview)
- [v1.0 (Preview)](https://westus2.dev.cognitive.microsoft.com/docs/services/AnomalyDetector/operations/post-timeseries-entire-detect)  
<details><summary style="font-size: 10pt">使用方法</summary>

</details>

***
#### Content Moderator
- [v1.0 Moderate](https://westus.dev.cognitive.microsoft.com/docs/services/57cf753a3f9b070c105bd2c1/operations/57cf753a3f9b070868a1f66c)  
- [v1.0 Review](https://westus.dev.cognitive.microsoft.com/docs/services/580519463f9b070e5c591178/operations/580519483f9b0709fc47f9c5)  
<details><summary style="font-size: 10pt">使用方法</summary>

</details>

***
#### Personalizer
- [v1.0](https://westus2.dev.cognitive.microsoft.com/docs/services/personalizer-api/operations/Rank)  
<details><summary style="font-size: 10pt">使用方法</summary>

</details>

***
