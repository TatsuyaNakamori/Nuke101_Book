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







6. Cardノードをダブルクリックしてプロパティを開きます。
7. Cardタブのorientationを **ZY** にします。

.. figure:: ./../../_images/cameraProjection/cameraProjection_008.png
   :scale: 10%
   :alt: cameraProjection_008.png


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


オブジェクトの作成
****************







.. contents:: このページの目次:
   :depth: 2
   :local:

