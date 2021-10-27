はじめてのコンポジット
######################

素材の読み込み方①
**************

1. ToolbarからReadノードを選択するか、NodeGraph上でショートカットキー **R** を押します

.. figure:: ./../../_images/firstComp/firstComp_001.png
   :scale: 10%
   :alt: firstComp_001.png
   :target: path 

2. ダイアログで読み込むファイルを選択します。
3. Openボタンを押して確定します。(Nextボタンを押すと、そのファイルはキープされ次の連番ファイルを選択することが出来ます。)
4. ReadノードがNodeGraph上に作られたことを確認します。

.. figure:: ./../../_images/firstComp/firstComp_002.png
   :scale: 10%
   :alt: firstComp_002.png
   :target: path 
 
   


素材の読み込み方②
**************

1. エクスプローラーのフォルダを選択し、NodeGraphへドラックをします。
2. フォルダ内に連番ファイルがあれば、素材の数だけReadノードが生成されます。



ノードを整理させる
**************** 

1. 整列させたいノードを選択する。
2. **Edit>Node>Autoplace** で整列させるか、NodeGraph上でショートカットキー **L** を押します。


ビューアに表示する①
**************** 

1. Readノードを選択し、キーボードの **1** を押します。
2. ReadノードとViewerノードが点線で接続されます。
3. ビューアに画像が表示されたことを確認します。


.. figure:: ./../../_images/firstComp/firstComp_003.png
   :scale: 10%
   :alt: firstComp_003.png
   :target: path 


ビューアに表示する②
**************** 

1. キーボードの「0~9」の番号で、ビューアの接続を設定することが出来ます。
2. ノードの選択を解除し(何も選択されていない状態)、数字を押すと、その数字に接続されているノードのアウトプットがビューアに表示されます。

.. figure:: ./../../_images/firstComp/firstComp_004.png
   :scale: 10%
   :alt: firstComp_004.png
   :target: path 


ビューアに表示する③
**************** 

Viewerノードの挙動をまとめると

1. ノードが選択状態で番号を押すと選択されているノードに、新しく接続されます。
2. ノードが何も選択されてない状態で番号を押すと、既に接続されているノードのアウトプットがビューアに表示されます。


Backdropを適用する
**************** 

読み込んでいるレイヤーを区別するために、Backdropを使って分かりやすくします。

1. まとめたいReadノードを選択する
2. Toolbarから、Backdropを選択する

.. figure:: ./../../_images/firstComp/firstComp_005.png
   :scale: 10%
   :alt: firstComp_005.png
   :target: path 


.. figure:: ./../../_images/firstComp/firstComp_006.png
   :scale: 10%
   :alt: firstComp_006.png
   :target: path 


プロパティパネル①
***************

Backdropに、ラベルを設定する。

1. 各ノードが持っているプロパティは、Propertiesタブで見ることができます。
2. ノードのプロパティを表示させたいときは該当のノードをダブルクリックする。


.. figure:: ./../../_images/firstComp/firstComp_007.png
   :scale: 10%
   :alt: firstComp_007.png
   :target: path 


プロパティパネル②
***************

Backdropに、ラベルを設定する。

1. **label** にレイヤーを入力する。
2. バックドロップの左上にラベルを表示される。 


.. figure:: ./../../_images/firstComp/firstComp_008.png
   :scale: 10%
   :alt: firstComp_008.png
   :target: path 


.. figure:: ./../../_images/firstComp/firstComp_009.png
   :scale: 10%
   :alt: firstComp_009.png
   :target: path 


bg,fgレイヤーを並べる
***************

fgレイヤーを読み込み、下図のようにバックドロップを使って整理しましょう。

1. レイヤーの読み込み
2. スクリプトを使って整列
3. バックドロップを作成
4. バックドロップのプロパティで、ラベルを入力


BackdropのTipos①
***************

Backdropの色はランダムなので、色を変更したいときは、タイルカラーを設定する。

.. figure:: ./../../_images/firstComp/firstComp_010.png
   :scale: 10%
   :alt: firstComp_010.png
   :target: path 


タイルカラーを押すとカラーピッカーが出てくるので、スライダーを動かし色を調節する

.. figure:: ./../../_images/firstComp/firstComp_011.png
   :scale: 10%
   :alt: firstComp_011.png
   :target: path 


BackdropのTipos②
***************

タイルカラーのボタンをドラックして、他のノードのタイルカラーを同じ色にすることもできます。

.. figure:: ./../../_images/firstComp/firstComp_012.png
   :scale: 10%
   :alt: firstComp_012.png
   :target: path 


PostageStampを使ってReadノードを参照する①
***************

1. Readノードは複製する事ができるので、NodeGraphの至る所で使うことができるが、読み込み素材を管理しきれなくなるデメリットがあります。
2. 特に実際の現場では、アニメーション変更などで素材のバージョンが更新される頻度が高いので、Readノードの管理は必要最低限にしたいです。　
3. PostageStampノードは、「何もしない」ノードなので、これを使ってReadノードを参照するようにします。(Readノード以外の参照にも使える)
4. Nukeには、AEのような読み込みファイルを管理するものはないので、このような対応をします。


PostageStampを使ってReadノードを参照する②
***************

Readノードを複製して作った例です。レイヤーのバージョンが更新されたら、下図の中で選択しているノードをすべて更新しなければいけません。


PostageStampを使ってReadノードを参照する③
*************** 

1. Readノードを選択します。
2. NodeGraphにカーソルを移動し、tab を押します。 
3. ノードの検索ボックスに「Postage...」と打ち、PostageStampの候補が出てきたら選択します。


.. figure:: ./../../_images/firstComp/firstComp_013.png
   :scale: 10%
   :alt: firstComp_013.png
   :target: path 


.. figure:: ./../../_images/firstComp/firstComp_014.png
   :scale: 10%
   :alt: firstComp_014.png
   :target: path 


1. Propertiesパネルで、ノード名やlabelを変更する。(何のノードを参照しているかｗかりやすく)     
2. hide inputのチェックを入れるとinputの矢印を非表示にすることができます。


.. figure:: ./../../_images/firstComp/firstComp_015.png
   :scale: 10%
   :alt: firstComp_015.png
   :target: path 


[Tips]ノード名やノードの色に関する注意① 
*************** 

基本的には、ノード名やノードの色は変更させずにコンポジットしていきます。

1. ノード名を変更してしまうと、何のノードを使っているか分からなくなります。 
2. 色を変更すると、NodeGraphを引いて見た時にどのような処理をしているか(カラコレなのか、フィルタをかけているのか)が分からなくなります。
3. ノード名や色の変更は、PostageStampなどのノードに限定するようにしましょう。
   

[Tips]ノード名やノードの色に関する注意②
*************** 

1. 名前や色を変更すると、何のノードで処理を行っているか分からなくなります。特にgreenはノードは、色を変更しているか、Greenチャンネルを抽出しているか分かりません。(shuffulノードをつかっていると勘違いさせてしまうかも)
2. 説明を残したい場合は、Backdropを使いましょう。

.. figure:: ./../../_images/firstComp/firstComp_016.png
   :scale: 10%
   :alt: firstComp_016.png
   :target: path 


Nukeのディフォルトの色を残しておくことで、大まかに何の処理を行っているかが、把握しやすくなります。


レイヤーを重ねる
*************** 

1. ReadノードからPostageStampを作り、下図のように並べる

.. figure:: ./../../_images/firstComp/firstComp_017.png
   :scale: 10%
   :alt: firstComp_017.png
   :target: path 


2. Mergeノードを作成する(ショートカットキー **M** )
3. Mergeノードの[B]矢印をbgレイヤーに、[A]矢印をfgレイヤーに接続する。

.. figure:: ./../../_images/firstComp/firstComp_018.png
   :scale: 10%
   :alt: firstComp_018.png
   :target: path 

.. figure:: ./../../_images/firstComp/firstComp_019.png
   :scale: 10%
   :alt: firstComp_019.png
   :target: path 

4. Viewerノードに接続し、結果を確認する。

.. figure:: ./../../_images/firstComp/firstComp_020.png
   :scale: 10%
   :alt: firstComp_020.png
   :target: path 


分かりやすいノードの並べ方①
*************** 

1. Nukeは自由にノードを並べられるので、組織でルールを決めておかないと、レイアウトがバラバラで見ずらいものになってしまいます。
2. 基本的な方針を予め決めておきましょう。

.. figure:: ./../../_images/firstComp/firstComp_021.png
   :scale: 10%
   :alt: firstComp_021.png
   :target: path 


分かりやすいノードの並べ方②
*************** 

基本はプログラミングのフローチャートを参考にします。 
1. 上から下へ
2. 分岐するときは右に流れる
3. 合流するときは左へ


ノード間の矢印を直角にする
*************** 

1. Ctrlボタンを押すと矢印の中間に黄色い短形が表示される。
2. 黄色の短形をクリックする。
3. Dotが追加される
4. Dotをドラックし、矢印を直角にする


.. figure:: ./../../_images/firstComp/firstComp_022.png
   :scale: 10%
   :alt: firstComp_022.png
   :target: path 


.. figure:: ./../../_images/firstComp/firstComp_023.png
   :scale: 10%
   :alt: firstComp_023.png
   :target: path 


writeノードを接続する
*************** 

1. Mergeノードを選択し、writeノードを作ります。(ショートカットキー **W** )

.. figure:: ./../../_images/firstComp/firstComp_024.png
   :scale: 10%
   :alt: firstComp_024.png
   :target: path 


2. プロパティの **file** の右側にあるフォルダアイコンをクリックし、ダイアログを開きます。

.. figure:: ./../../_images/firstComp/firstComp_025.png
   :scale: 10%
   :alt: firstComp_025.png
   :target: path 

3. 階層をたどり、出力するファイル名を記述しSaveボタンを押します。

.. figure:: ./../../_images/firstComp/firstComp_026.png
   :scale: 10%
   :alt: firstComp_026.png
   :target: path 


4. ファイル名が設定されると、拡張子を判別し、書き出しのオプションが自動設定されます。

.. figure:: ./../../_images/firstComp/firstComp_027.png
   :scale: 10%
   :alt: firstComp_027.png
   :target: path 

5. writeノードに、書き出させるファイル名が表示されます。

.. figure:: ./../../_images/firstComp/firstComp_028.png
   :scale: 10%
   :alt: firstComp_028.png
   :target: path 


writeノードの連番の桁数指定の仕方
*************** 

・ 静止画連番の場合の、連番の桁数指定

 1. **#** を使う(桁数分、並べる)
 ・[4桁]filename. **####** .png

 2. **%0[桁数]d** という書き方(プログラミングのゼロパティングの書き方)
 ・[4桁]filename. **%04d** .png 
 ・[10桁]filename. **%010d** .png


writeノードのプロパティ(注意点)
*************** 

・チャンネル設定 

1. デフォルトでは、 **rgb** になっておりαチャンネルが出力されないようになっています。

.. figure:: ./../../_images/firstComp/firstComp_029.png
   :scale: 10%
   :alt: firstComp_029.png
   :target: path 


2. コンボボックスの項目を **rgba** に設定するとαチャンネルが出力されるようになります。

.. figure:: ./../../_images/firstComp/firstComp_030.png
   :scale: 10%
   :alt: firstComp_030.png
   :target: path 

.. figure:: ./../../_images/firstComp/firstComp_031.png
   :scale: 10%
   :alt: firstComp_031.png
   :target: path 


書き出し
*******

1. **create directories** にチェックを入れると、フォルダが存在しない時に自動的に作ってくれます。(フォルダが存在しないと、エラーで止まってしまうで止まってしまう)
2. **Render** ボタンを押し、ダイヤログの情報を確認します。
3. OKボタンを押して、レンダリングを開始します。

.. figure:: ./../../_images/firstComp/firstComp_032.png
   :scale: 10%
   :alt: firstComp_032.png
   :target: path 


.. figure:: ./../../_images/firstComp/firstComp_033.png
   :scale: 10%
   :alt: firstComp_033.png
   :target: path 


writeノード2
*******

・今度はmov形式で書き出しをしてみます。

1. writeノードを追加します。
2. 書き出すフォルダ/ファイル名を指定します。(ファイル名の拡張子は **mov** にします。)
3. プロパティの、その他のオプションは必要に応じて変更し、レンダリングを行います。




.. contents:: このページの目次:
   :depth: 2
   :local:


