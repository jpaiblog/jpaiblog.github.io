---
title: QnA Maker リソースに関連付けられている App Service プランについて
date: 2020-10-20 12:00:00
categories:
- QnA Maker
tags:
- リソースの作成
---
QnA Maker を作成する段階で、Free 価格レベルの App Service プランを作成する方法をご紹介します。
<!-- more -->
<br>

***
# テンプレート
## テンプレートファイルについて
QnA Maker を作成する際に、下図のように、QnA Maker リソース自体を含めて、同じリソースグループ内に 5 種類のリソースが自動で作られます。
![qna-maker-related-resources](https://jpaiblog.github.io/images/QnA-Maker-App-Service/qna-maker-related-resources.png)

それぞれのリソースの役割については、下記ドキュメントから確認できます。
- [QnA Maker 用の Azure リソースとその役割](https://docs.microsoft.com/ja-jp/azure/cognitive-services/qnamaker/concepts/azure-resources#resource-purposes)

QnA Maker の利用を検討される段階で、無料での利用が望ましいが、なんと Free 価格レベルの QnA Maker を作成しようとしたら、関連のリソース App Service プランの価格レベルの既定値は、Standard (S1) となっています。
これは、多くの一般的なシナリオで問題なく QnA Maker を利用できるコンピューティング リソースを確保するためです。

もし課金を抑えたい場合は、QnA Maker の作成後、すぐに関連のリソース App Service プランの価格レベルを Free に変更すればいいです。

下図のように、App Service プラン リソースの画面で、スケール アップ (App Service のプラン) ⇒ 開発/テスト ⇒ F1  ⇒ 適用 の順に実施すると、App Service プランの価格レベルを Free に変更できます。
![app-service-plan-scale-down](https://jpaiblog.github.io/images/QnA-Maker-App-Service/app-service-plan-scale-down.png)

Free に変更する前に、Standard 価格レベルの App Service プランに対する課金が秒単位で続けられます。（約 ¥13.216/時間）
各価格レベルの課金情報とそのコンピューティング リソースのスペックについては、下記リンクから確認できます。
- [App Service の価格](https://azure.microsoft.com/ja-jp/pricing/details/app-service/windows/)

なお、App Service プランの価格レベルを Free に変更した場合はリソースの制約（クォータ）により正常に動作しない場合があるので、何らか問題が発生した際は必要に応じて適切な価格レベルへの変更をご検討ください。

ここで、補足として、QnA Maker を作成する段階で、Free 価格レベルの App Service プランのリソースを作る方法を紹介します。

1. QnA Makerの作成画面で基本情報を入力します。
QnA Maker と Azure Search の価格レベルにそれぞれ Freeを指定した上、他の情報の入力後に、「確認および作成」をクリックします。
![step01](https://jpaiblog.github.io/images/QnA-Maker-App-Service/step01.png)

2. 「Automation オプション」をクリックします。
注：この画面で「作成」をクリックしないでください。
![step02](https://jpaiblog.github.io/images/QnA-Maker-App-Service/step02.png)

3. 「ダウンロード」をクリックします。
ダウンロードした zip ファイルを解凍します。 
![step03](https://jpaiblog.github.io/images/QnA-Maker-App-Service/step03.png)

4. 「カスタム テンプレートのデプロイ」を検索します。
Azure ポータルの検索バーに「カスタム テンプレートのデプロイ」を入力し、下に表示される「カスタム テンプレートのデプロイ」をクリックします。
![step04](https://jpaiblog.github.io/images/QnA-Maker-App-Service/step04.png)

5. 「エディターで独自のテンプレートを作成する」をクリックします。
![step05](https://jpaiblog.github.io/images/QnA-Maker-App-Service/step05.png)

6. テンプレートファイルを読み込みます。
「ファイルの読み込み」をクリックして、ステップ 3 でダウンロードした template.json ファイルを選択します。
![step06](https://jpaiblog.github.io/images/QnA-Maker-App-Service/step06.png)

7. テンプレートを編集して保存します。
以下のように、”type:” “Microsoft.Web/serverfarms” の項目で “sku” の ”Standard” と “S1” をそれぞれ “Free” と “F1” に変更してファイルを保存します。
なお、アップロード前の JSON ファイルで編集いただいても構いません。
![step07](https://jpaiblog.github.io/images/QnA-Maker-App-Service/step07.png)

8. 「パラメーターの編集」をクリックします。
注：Web ブラウザーによってはボタンの名前が全て表示されない場合がございますので、マウスカーソルをボタン上に置いて表示されるツールチップでご確認ください。
![step08](https://jpaiblog.github.io/images/QnA-Maker-App-Service/step08.png)

9. パラメーターファイルを読み込みます。
「ファイルの読み込み」をクリックし、ステップ 3 でダウンロードした parameters.json ファイルを選択します。
![step09](https://jpaiblog.github.io/images/QnA-Maker-App-Service/step09.png)

10. パラメーターを保存します。
![step10](https://jpaiblog.github.io/images/QnA-Maker-App-Service/step10.png)

11. テンプレートファイルをデプロイします。
デプロイ先のリソースグループを選択した上、使用条件を確認して同意いただけましたら「購入」をクリックします。
![step11](https://jpaiblog.github.io/images/QnA-Maker-App-Service/step11.png)

ARM テンプレートを利用して、Free の価格レベルの App Service プランを含む QnA Maker を作成する手順は以上となります。

***
`変更履歴`  
`2020/10/20 created by Chao`  