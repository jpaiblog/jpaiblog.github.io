---
title: Webポータル画面が期待通りに表示されない場合の確認方法
date: 2020-11-11 00:00:00
categories:
- Cognitive Services
tags:
- Cognitive Services
---

 
Coginitive Services の一部には、特有のWebポータル画面を持つサービスがあります。  
Azureポータル画面や、それらサービス特有のWebポータル画面で 『プルダウンに選択肢が表示されるはずなのに、表示されない』 など、期待通りの画面表示とならない場合の確認方法をご紹介します。  
（以下の画像は、Metrics Advisor サービスのポータル画面における例です）

![browser01](https://jpaiblog.github.io/images/not-expected-display-on-the-webbrowser/browser01.jpg "browser01") 

1. [Webブラウザの言語翻訳機能の状態を確認する](#Webブラウザの言語翻訳機能の状態を確認する)
1. [Webブラウザから最新のデータにアクセスして確認する](#Webブラウザから最新のデータにアクセスして確認する)
1. [現在利用しているブラウザ以外のブラウザを使用して確認する](#現在利用しているブラウザ以外のブラウザを使用して確認する) 
<!-- more -->
<br>

***

# Webブラウザの言語翻訳機能の状態を確認する
ブラウザ上で言語翻訳ツールなどをお使いでしたら、その機能が事象に影響している可能性があります。  
翻訳機能を使用しない状態で画面表示をご確認ください。

***
# Webブラウザから最新のデータにアクセスして確認する
Webブラウザがローカルに保存したキャッシュデータ等を使用しているために、古い状態のデータが画面表示されている可能性があります。  

![browser02](https://jpaiblog.github.io/images/not-expected-display-on-the-webbrowser/browser02.jpg "browser02")

インターネット上の最新のデータにアクセスして画面表示が行えるよう、以下をご確認ください。

(1) Webブラウザのプライベート ブラウジングを用いて確認する  

プライベート ブラウジングでは、閲覧履歴、ダウンロード履歴、キャッシュ、Cookie などを保存せずにWebサイトを閲覧可能となります。 

Microsoft Edge をご利用の場合、以下のドキュメントの手順に添って、InPrivate ブラウズを利用してください。  

- [Microsoft Edge で InPrivate ブラウズを使う](https://support.microsoft.com/ja-jp/help/4026200/microsoft-edge-browse-inprivate)
  
Google Chrome をご利用の場合、以下のGoogle社のヘルプドキュメントの手順に添って、シークレットブラウジングを利用してください。  

- [(Google Chrome ヘルプ) シークレット ブラウジング](https://support.google.com/chrome/answer/95464?hl=ja)

(2) ブラウザのキャッシュを削除してから確認する 

Microsoft Edge をご利用の場合、以下のドキュメント以下のドキュメントの [キャッシュされたデータとファイル] にて削除してください。  

- [Microsoft Edge の閲覧履歴を表示または削除する](https://support.microsoft.com/ja-jp/help/10607/microsoft-edge-view-delete-browser-history)
  
Google Chrome をご利用の場合、以下のGoogle社のヘルプドキュメントの手順に添って削除してください。  

- [(Google Chrome ヘルプ) キャッシュと Cookie の消去](https://support.google.com/accounts/answer/32050)

***
# 現在利用しているブラウザ以外のブラウザを使用して確認する
現在利用している Webブラウザ以外のブラウザを使用した場合に、画面表示が変わるかどうかご確認ください。



***
`変更履歴`  
`2020/11/11 created by Uehara`  