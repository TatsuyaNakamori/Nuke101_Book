カメラプロジェクション
####################

 **このセクションでは、カメラプロジェクションについて学習します。** 


 1. まず、始めにノードグラフ上でショートカットキー **R** ボタンで素材を読み込みます。
 2. 読み込むファイルを選択し、Openボタンを押します。
 3. Readノードがノードグラフ上に作られたのを確認します。

.. figure:: ./../../_images/cameraProjection/cameraProjection_001.png
   :scale: 10%
   :alt: cameraProjection_001.png


.. figure:: ./../../_images/cameraProjection/cameraProjection_002.png
   :scale: 10%
   :alt: cameraProjection_002.png


カメラの用意
***********

1. NodeGraph上でTabを押してCameraと検索してCameraを作成します。
2. NodeGraph上でCameraをダブルクリックし、Cameraのプロパティを開きます。
3. プロパティの中のNodeのタブを開きlabelにprojectionと打ちます。 

.. figure:: ./../../_images/cameraProjection/cameraProjection_003.png
   :scale: 10%
   :alt: cameraProjection_003.png 

4. NodeGraph上でCameraを選択した状態でTabを押してBackdropと検索し選択します。
5. NodeGraph上のBackdropをダブルクリックしプロパティを開きます。
6. labelにProjectionと打ちます。

.. figure:: ./../../_images/cameraProjection/cameraProjection_011.png
   :scale: 10%
   :alt: cameraProjection_011.png

7. NodeGraphのCameraのBackdropにProjectionと文字が打たれます。

.. figure:: ./../../_images/cameraProjection/cameraProjection_012.png
   :scale: 10%
   :alt: cameraProjection_012.png


8. 撮影時のカメラの情報をもとにカメラの位置を決定します。


.. figure:: ./../../_images/cameraProjection/cameraProjection_005.png
   :scale: 10%
   :alt: cameraProjection_005.png

9. カメラの位置はカメラのプロパティのCameraのタブとProjectionのタブから決定します。

.. figure:: ./../../_images/cameraProjection/cameraProjection_006.png
   :scale: 10%
   :alt: cameraProjection_006.png


.. figure:: ./../../_images/cameraProjection/cameraProjection_007.png
   :scale: 10%
   :alt: cameraProjection_007.png 


10. Tabを押して Project3Dノードと検索し選択します。
11. 下図のようにProject3DノードとCamera、Readノードを接続します。

.. figure:: ./../../_images/cameraProjection/cameraProjection_004.png
   :scale: 10%
   :alt: cameraProjection_004.png


オブジェクトの作成のためのノード作成
****************

1. Tabを押して、Cardと検索し選択します。
2. Tabを押して、Cubeと検索し選択します。
3. Tabを押して、Sceenと検索し選択します。
4. Tabを押して、ScanlineRenderと検索し選択します。

.. figure:: ./../../_images/cameraProjection/cameraProjection_009.png
   :scale: 10%
   :alt: cameraProjection_009.png


5. NodeGraph上のノードを下図のようにDotを使い整理しつなげていきます。

.. figure:: ./../../_images/cameraProjection/cameraProjection_010.png
   :scale: 10%
   :alt: cameraProjection_010.png 




8. 先程作ったCameraProjectionを選択し、ctrl+c & ctrl+vで複製します。
9. 複製したCameraノードをダブルクリックしプロパティを開きNodeタブのlabelにrenderと打ちます。

.. figure:: ./../../_images/cameraProjection/cameraProjection_013.png
   :scale: 10%
   :alt: cameraProjection_013.png

10. RenderCameraを選択した状態でTabでBackdropと検索し選択します。
11. Nodegraph上でBackdropをダブルクリックしプロパティを開きlabelにRenderCamと打ちます。

.. figure:: ./../../_images/cameraProjection/cameraProjection_014.png
   :scale: 10%
   :alt: cameraProjection_014.png

12. ScanlineRenderとRenderCamのノードをつなげます。

.. figure:: ./../../_images/cameraProjection/cameraProjection_015.png
   :scale: 10%
   :alt: cameraProjection_015.png


Cardの作成
****************

1. Cardノードをダブルクリックしてプロパティを開きます。
2. Cardタブのorientationを **ZY** にします


.. figure:: ./../../_images/cameraProjection/cameraProjection_008.png
   :scale: 10%
   :alt: cameraProjection_008.png

3. NodeGraph上でCardノードを選択しているとViewer上でx,y,zのtlanslateの矢印が表示されます。3D上でも同じように表示されます。また2D上で見たい場合はScanlineRenderノードにViewerノードを繋げないと見れません。CameraやSceneノードにViewerノードを繋げた場合3DViewerになってしまいます。

.. figure:: ./../../_images/cameraProjection/cameraProjection_017.png
   :scale: 10%
   :alt: cameraProjection_017.png


.. figure:: ./../../_images/cameraProjection/cameraProjection_018.png
   :scale: 10%
   :alt: cameraProjection_018.png



4. 動かしたい方向の矢印をクリックしながらドラックすれば、Cardの位置を動かすことが出来ます。
5. rotakeを変更したい場合はctrlを押しながらドラックします。
6. scaleを変更したい場合はctrlとshiftを押しながらドラックします
7. Viewer上で、Tabを押して3Dビューと2Dビューを切り替えながら調節します。下図のようにボタンで切り替えも出来ます。



.. figure:: ./../../_images/cameraProjection/cameraProjection_016.png
   :scale: 10%
   :alt: cameraProjection_016.png



8. 細かく微調節するときは、Cardタブのtranslate, rotate,scaleの数値を変えて位置や大きさを調節します。

.. figure:: ./../../_images/cameraProjection/cameraProjection_019.png
   :scale: 10%
   :alt: cameraProjection_019.png


Cubeの作成
****************


1. NodeGraph上でCubeノードをダブルクリックしプロパティを開きuniform scaleを変更し2DViewer上でもCubeが見えるくらいの大きさにします。

.. figure:: ./../../_images/cameraProjection/cameraProjection_020.png
   :scale: 10%
   :alt: cameraProjection_020.png


.. figure:: ./../../_images/cameraProjection/cameraProjection_021.png
   :scale: 10%
   :alt: cameraProjection_021.png


2. translate,rotakeの値を変更して、Cubeを箱の形に合わせていきます。 
3. 微調節する場合は、CubuのプロパティCubuの値を変更するかViewer上でCubuについている点をクリックしながら動かします。選択された点は緑になります。


.. figure:: ./../../_images/cameraProjection/cameraProjection_022.png
   :scale: 10%
   :alt: cameraProjection_022.png


.. figure:: ./../../_images/cameraProjection/cameraProjection_023.png
   :scale: 10%
   :alt: cameraProjection_023.png


4. 3DViewer上で確認する場合は、Viewer上でTabを押します。
5. ViewerのdefaultからCameraを切り替えることが出来ます。

.. figure:: ./../../_images/cameraProjection/cameraProjection_024.png
   :scale: 10%
   :alt: cameraProjection_024.png


Cameraのアニメーション
****************

1. 先程作った、Rendercameraにアニメーションをつけていきます。
2. 今回は、前後にカメラを動かしていきます。
3. タイムラインを1フレームにします。
4. NodeGraph上でCameraRenderをダブルクリックして、プロパティを開きます。
5. translateとrotakeの右側のボタンをクリックし、Setkeyを押してキーフレームを押します。数値の枠を右クリックでも同様の操作が出来ます。

.. figure:: ./../../_images/cameraProjection/cameraProjection_025.png
   :scale: 10%
   :alt: cameraProjection_025.png


.. figure:: ./../../_images/cameraProjection/cameraProjection_026.png
   :scale: 10%
   :alt: cameraProjection_026.png


6. キーフレームが打たれるとプロパティのtranslateとrotakeが青くなります。


.. figure:: ./../../_images/cameraProjection/cameraProjection_027.png
   :scale: 10%
   :alt: cameraProjection_027.png



7. 他にもタイムラインの1フレーム目も青い印が打たれ、NodeGraph上のRenderCameraノードにも赤い丸のA印が付きます。

.. figure:: ./../../_images/cameraProjection/cameraProjection_028.png
   :scale: 10%
   :alt: cameraProjection_028.png


.. figure:: ./../../_images/cameraProjection/cameraProjection_029.png
   :scale: 10%
   :alt: cameraProjection_029.png

8. 一度キーフレームを打てばキーフレームを打った所の数値を変えた場合自動的にキーフレームが打たれます。 
9. RenderCameraノードのプロパティのProjectionタブのFocal lengthを150に変更し同じようにキーフレームを打ちます。


.. figure:: ./../../_images/cameraProjection/cameraProjection_030.png
   :scale: 10%
   :alt: cameraProjection_030.png


10. タイムラインのフレームを100フレームに移動します。タイムラインの下にある下図のボタンで最終フレームまで移動することが出来ます。

.. figure:: ./../../_images/cameraProjection/cameraProjection_031.png
   :scale: 10%
   :alt: cameraProjection_031.png


11. RenderCameraを選択した状態で、Viewerを3DViewerに切り替えz方向にカメラを動かします。そうすると、プロパティのtranslateに自動的にキーフレームが打たれます。

.. figure:: ./../../_images/cameraProjection/cameraProjection_032.png
   :scale: 10%
   :alt: cameraProjection_032.png

12. rotakeも調節していきます。3DViewer上でctrlを押しながら変更もできますが、微調節する場合は、プロパティから直接数値を変更します。
13. 下図のようにキーフレームが打たれなかった場合薄い青色で表示されます。薄い青色なのは、1フレーム目にキーフレームが打たれているからです。

.. figure:: ./../../_images/cameraProjection/cameraProjection_033.png
   :scale: 10%
   :alt: cameraProjection_033.png


14. RenderCameraのプロパティのProjectionタブを開き、focal lengthを50に変更します。
15. Viewerじょうで見た時に破損しているフレームがある場合はそのフレームでtranlateの数値を変更しキーフレームを打てば解決できます。

.. figure:: ./../../_images/cameraProjection/cameraProjection_034.png
   :scale: 10%
   :alt: cameraProjection_034.png

.. figure:: ./../../_images/cameraProjection/cameraProjection_035.png
   :scale: 10%
   :alt: cameraProjection_035.png

16. 再生した際に段ボールのエッジが汚くなる場合はScanlineRenderのプロパティのantialiasingをhighにすると解決できます。

.. figure:: ./../../_images/cameraProjection/cameraProjection_036.png
   :scale: 10%
   :alt: cameraProjection_036.png





.. contents:: このページの目次:
   :depth: 2
   :local:

