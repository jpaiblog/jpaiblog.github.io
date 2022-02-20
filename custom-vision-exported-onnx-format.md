---
title: Custom Vision における、ONNX 形式のモデルの入力・出力の形式について
date: 2022-02-20 00:00:00
categories:
- Cognitive Services
tags:
- Custom Vision
---
Custom Vision Service にて ONNX 形式でエクスポートされたモデルを使用する方法と関連する注意事項をご紹介いたします。
<br>
***

## エクスポートされたONNX形式モデルを使用する方法

Custom Vision Service では、エッジ デバイスのリアルタイム推論用に最適化されている、"コンパクト ドメイン"によって生成されたモデルのみエクスポートが可能です。

- [コンパクト ドメインとは](https://docs.microsoft.com/ja-jp/azure/cognitive-services/custom-vision-service/select-domain#compact-domains)

もしコンパクト ドメイン以外のドメインを設定されている学習済みモデルのエクスポートを行いたい場合は、
対象プロジェクトの [ドメイン] セクションにて、コンパクト ドメインを選択し、再学習をしたうえでエクスポートを行ってください。

- [コンパクト ドメインへの変換方法](https://docs.microsoft.com/ja-jp/azure/cognitive-services/custom-vision-service/export-your-model#convert-to-a-compact-domain)

![Custom Vision Compact Domain](https://jpaiblog.github.io/images/custom-vision-exported-onnx-format/custom-vision-compact-domain.png)

Custom Vision Serviceは、様々なエクスポート形式に対応しています。
以下では、Windows ML、Android、iOS に対応した ONNX 形式のモデルを使用する方法をご紹介しておりますので適宜ご活用ください。

- [ONNXファイルを用いた推論サンプルコード](https://github.com/Azure-Samples/cognitive-services-onnx-customvision-sample)
- [Onnx on GitHub](https://github.com/onnx/onnx)

## エクスポートに関する注意事項


##### ■ 再学習やエクスポートのタイミングによって、ONNX ファイル内の入力および出力のフォーマットが変更されることはあるか？

いいえ。Custom Vision Service にて再学習の際も、入力や出力のデータサイズやノード名は固定のまま再学習が行われます。また、これらの形式はエクスポートのタイミングによっても変更されることはありませんので、再学習前に利用していた推論コードをそのまま用いて実行が可能です。

***
`変更履歴`  
`2022/02/20 created by kazuyaonuki`  

※ 本記事は 「[jpaiblog について](https://jpaiblog.github.io/blog/2020/01/01/about-jpaiblog/)」 の留意事項に準じます。  
※ 併せて 「[ホームページ](https://jpaiblog.github.io/blog/)」 および 「[記事一覧](https://jpaiblog.github.io/blog/archives/)」 もご参照いただければ幸いです。