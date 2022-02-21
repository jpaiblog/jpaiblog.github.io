---
title: Custom Vision における、ONNX 形式のモデルの入力・出力の形式について
date: 2022-02-21 10:30:00
categories:
- Cognitive Services
tags:
- Custom Vision
---
Custom Vision Service にて ONNX 形式でエクスポートされたモデルを使用する方法と関連する注意事項をご紹介いたします。
<br>
***

## エクスポートされた ONNX モデルを使用する方法

Custom Vision Service では、エッジ デバイスのリアルタイム推論用に最適化されている、
"コンパクト ドメイン"によって生成されたモデルのみエクスポートが可能です。

- [コンパクト ドメインとは](https://docs.microsoft.com/ja-jp/azure/cognitive-services/custom-vision-service/select-domain#compact-domains)

もしコンパクト ドメイン以外のドメインを設定された学習済みモデルのエクスポートを行いたい場合は、
対象プロジェクトの設定の内、[ドメイン] セクションにてコンパクト ドメインを選択し、
再学習を行ったうえでエクスポートをご実施くださいますようお願い申し上げます。

![Custom Vision Compact Domain](https://jpaiblog.github.io/images/custom-vision-exported-onnx-format/custom-vision-compact-domain.png)

- [コンパクト ドメインへの変換方法](https://docs.microsoft.com/ja-jp/azure/cognitive-services/custom-vision-service/export-your-model#convert-to-a-compact-domain)

学習済みモデルをエクスポートする際は、対象プロジェクトの[Performance]タブを選択し、[Export]をクリックすることで、エクスポートができます。

![How To Export](https://jpaiblog.github.io/images/custom-vision-exported-onnx-format/custom-vision-how-to-export.png)

なお、エクスポートの際に対応するファイル形式を指定できますが、
ONNX モデルをご利用する場合は以下をご選択ください。

![Export ONNX](https://jpaiblog.github.io/images/custom-vision-exported-onnx-format/custom-vision-export-onnx.png)

- [モデルをエクスポートする](https://docs.microsoft.com/ja-jp/azure/cognitive-services/custom-vision-service/export-your-model#export-your-model)

また、ONNX モデルを用いたサンプルコードをご紹介いたしますので、
適宜ご活用いただきますようお願い申し上げます。

- [ONNXファイルを用いた推論サンプルコード](https://github.com/Azure-Samples/cognitive-services-onnx-customvision-sample)
- [Onnx on GitHub](https://github.com/onnx/onnx)

## 注意事項

##### ■ 再学習やエクスポートのタイミングによって、ONNX ファイル内の入力および出力のフォーマットが変更されることはあるか？

いいえ。Custom Vision Service にて再学習の際も、入力や出力のデータサイズやノード名は固定のまま再学習が行われます。また、これらの形式はエクスポートのタイミングによっても変更されることはありませんので、再学習前に利用していた推論コードをそのまま用いて実行が可能です。

***
`変更履歴`  
`2022/02/21 created by kazuyaonuki`  

※ 本記事は 「[jpaiblog について](https://jpaiblog.github.io/blog/2020/01/01/about-jpaiblog/)」 の留意事項に準じます。  
※ 併せて 「[ホームページ](https://jpaiblog.github.io/blog/)」 および 「[記事一覧](https://jpaiblog.github.io/blog/archives/)」 もご参照いただければ幸いです。