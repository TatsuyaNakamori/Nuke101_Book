このセクションの概要
####################


.. contents:: このページの目次:
   :depth: 2
   :local:

このセクションでは2Dトラッキングについて学習します。

トラッキング素材を読み込む
#######################

1. Node Graph上で ``R`` キーを押してファイルブラウザを開き、tracking2D_photoFrame_####.png 1-72を選択しOpenで読み込みます。

2. Read1をダブルクリックしてプロパティを開き、Colorspaceをcolor_picking(Output-Rec.709)に変更します。

.. figure:: ./../../_images/tracking2D/tracking2D_002.png
   :scale: 100%
   :alt: image01
   :target: path



4点トラッキング
####################

1. Node Graph上で ``TAB`` キーを押してTrackerノードを作成します。

2. Read1の後にTrackerノードを接続します。

3. TrackerノードのPropertiesのadd trackを押して４つのtrackを作成します。 

.. figure:: ./../../_images/tracking2D/tracking2D_003.png
   :scale: 100%
   :alt: image01
   :target: path

4. ４つのTrackを写真フレームの枠に配置します。ターゲット領域の枠が小さいと、トラッキングが失敗する可能性があるので、
トラッキングのターゲット領域は少し広めの茶色い枠まで広げます。

.. figure:: ./../../_images/tracking2D/tracking2D_004.png
   :scale: 100%
   :alt: image01
   :target: path

5. 実際にトラッキングをするにtrack1を選択し、はViewerの上部にある再生ボタンを押します。そうすることでトラッキングが開始されます。

.. figure:: ./../../_images/tracking2D/tracking2D_006.png
   :scale: 100%
   :alt: image01
   :target: path
.. figure:: ./../../_images/tracking2D/tracking2D_005.png
   :scale: 100%
   :alt: image01
   :target: path

6. [5]の工程をtrack２-４も行います。４つトラッキングした結果がこちらです。

.. figure:: ./../../_images/tracking2D/tracking2D_007.png
   :scale: 100%
   :alt: image01
   :target: path

7. TrackerノードのPropatiesのExportをCornerPin2D(use transform ref frame)に変更します。

.. figure:: ./../../_images/tracking2D/tracking2D_008.png
   :scale: 100%
   :alt: image01
   :target: path

8. 4つのトラックを選択した状態でExportのcreateを押してトラッキングデータを抽出します。
するとCornerPin2D１というノードが作られます。こちらがトラッキングデータです。
これでトラッキングの作業は終了です。

.. figure:: ./../../_images/tracking2D/tracking2D_009.png
   :scale: 100%
   :alt: image01
   :target: path

.. figure:: ./../../_images/tracking2D/tracking2D_010.png
   :scale: 100%
   :alt: image01
   :target: path

写真フレームに収める素材を作成
##############################
1. Node Graph上で ``TAB`` キーを押してCheckerBoardノードを出します。

2. CheckerBoardのサイズを写真のL判サイズにするためにPropatiesのformatをクリックして、下部にあるnewを選択します。

.. figure:: ./../../_images/tracking2D/tracking2D_011.png
   :scale: 100%
   :alt: image01
   :target: path

3. 選択するとサイズや名前を決めることが出来ます。サイズはfile sizaをw(横)890のh(縦)1270にします。
名前は自分の分かりやすい名前に設定します。今回は[photo_L]とします。
これで写真素材の作成は終了です。

.. figure:: ./../../_images/tracking2D/tracking2D_012.png
   :scale: 100%
   :alt: image01
   :target: path

.. figure:: ./../../_images/tracking2D/tracking2D_013.png
   :scale: 100%
   :alt: image01
   :target: path

最終コンポジット
####################

トラッキングデータを使って背景の写真立てに写真素材をコンポジットします。

1. 