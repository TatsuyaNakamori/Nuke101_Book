このセクションの概要
####################


.. contents:: このページの目次:
   :depth: 2
   :local:

このセクションではバレ消しについて学習します。

トラッキング素材を読み込む
#######################

1. Node Graph上で ``R`` キーを押してファイルブラウザを開き、wireRemoval_magic_####.png 1-72を選択しOpenで読み込みます。

2. Read1をダブルクリックしてプロパティを開き、Colorspaceをcolor_picking(Output-Rec.709)に変更します。

.. figure:: ./../../_images/wireremoval/wireremoval_001.png
   :scale: 100%
   :alt: image01
   :target: path

ワイヤーの除去、クリーンプレートの作成
#######################

1. Read1が選択されている状態で、 ``P`` キーを押してRotoPaintノードを接続します。ビューアにRotoPaintを表示します。

.. figure:: ./../../_images/wireremoval/wireremoval_005.png
   :scale: 100%
   :alt: image01
   :target: path

2. RotoPaintのツールセットから[Clone]ブラシを選択します。


.. figure:: ./../../_images/wireremoval/wireremoval_002.png
   :scale: 100%
   :alt: image01
   :target: path

3. Cloneブラシはイメージ内のピクセルを別の場所にコピーします。ブラシはコピーしたい部分を ``Ctrl`` / ``Cmd`` をクリックし、 クリックしたままコピー先の部分までドラッグすることで設定します。

.. figure:: ./../../_images/wireremoval/wireremoval_003.png
   :scale: 100%
   :alt: image01
   :target: path

4. 背景の服に合うようにコピーしていきます。

.. figure:: ./../../_images/wireremoval/wireremoval_004.png
   :scale: 100%
   :alt: image01
   :target: path

5. クリーンプレートの完成形がこちらです

.. figure:: ./../../_images/wireremoval/wireremoval_006.png
   :scale: 100%
   :alt: image01
   :target: path

クリーンプレートのマスク作成と適応
#######################

1. 先ほど作成したクリーンプレートを適応さるためにマスクを作成します。 ``O`` キーを押してRotoを作成。手の下側に作成します。

.. figure:: ./../../_images/wireremoval/wireremoval_008.png
   :scale: 100%
   :alt: image01
   :target: path

2. 作成したRotoを使ってMerge(mask) でマスクをかけます。

.. figure:: ./../../_images/wireremoval/wireremoval_009.png
   :scale: 100%
   :alt: image01
   :target: path

.. figure:: ./../../_images/wireremoval/wireremoval_010.png
   :scale: 100%
   :alt: image01
   :target: path

3. クリーンプレートで作成した1フレームを48フレーム使用するので、Shuffleノードでalphaを作成してFrameHoldノードでフレームを固定します。

alphaの作成

.. figure:: ./../../_images/wireremoval/wireremoval_012.png
   :scale: 100%
   :alt: image01
   :target: path

.. figure:: ./../../_images/wireremoval/wireremoval_011.png
   :scale: 100%
   :alt: image01
   :target: path

FrameHoldの適応

.. figure:: ./../../_images/wireremoval/wireremoval_013.png
   :scale: 100%
   :alt: image01
   :target: path

これでマスクの作成完了です。

トラッキングと元素材への合成
#######################

1. 服をトラッキングします

.. figure:: ./../../_images/wireremoval/wireremoval_014.png
   :scale: 100%
   :alt: image01
   :target: path

2. 今回はExportを[Transform(match-move)]にしてトラッキングデータをExportします。

.. figure:: ./../../_images/wireremoval/wireremoval_015.png
   :scale: 100%
   :alt: image01
   :target: path

3. 書き出したトラッキングデータをFrameHoldにつなげて、Merge(over)で元素材に合成します。

.. figure:: ./../../_images/wireremoval/wireremoval_017.png
   :scale: 100%
   :alt: image01
   :target: path

.. figure:: ./../../_images/wireremoval/wireremoval_016.png
   :scale: 100%
   :alt: image01
   :target: path

4. こちらが一連の流れです。あとは手の上の部分も同じ工程でクリーンプレートを合成します。

5. 手の上の部分もマスクを作り、トラッキングして合成しました。

.. figure:: ./../../_images/wireremoval/wireremoval_018.png
   :scale: 100%
   :alt: image01
   :target: path

.. figure:: ./../../_images/wireremoval/wireremoval_019.png
   :scale: 100%
   :alt: image01
   :target: path

6. ワイヤーは左右に揺れ、先ほどマスクした部分よりも外に出てしまうので、その分のクリーンプレートも作成します。作成したら先ほどと同様にトラッキングして元素材に合成します。細かいところはRotoPaintoで修正します。

.. figure:: ./../../_images/wireremoval/wireremoval_020.png
   :scale: 100%
   :alt: image01
   :target: path

.. figure:: ./../../_images/wireremoval/wireremoval_022.png
   :scale: 100%
   :alt: image01
   :target: path

7. こちらがワイヤーの揺れの分まで考慮したクリーンプレートを合成したものです。

.. figure:: ./../../_images/wireremoval/wireremoval_021 .png
   :scale: 100%
   :alt: image01
   :target: path

手の復元
#######################

1. 先ほどのクリーンプレートでは手が消されているので、その消された手を復元します。
2. 元素材をマスクで切り取り復元するします。そのマスクを動かす為に指3本をトラッキングします。

.. figure:: ./../../_images/wireremoval/wireremoval_024 .png
   :scale: 100%
   :alt: image01
   :target: path

3. 指のマスクを作成します。

.. figure:: ./../../_images/wireremoval/wireremoval_023 .png
   :scale: 100%
   :alt: image01
   :target: path

4. クリーンプレートの適応と同じ手順で合成します。ですが、指は元素材の1フレームだけでなく全フレーム使用するのでFrameHoldは使用しません。

.. figure:: ./../../_images/wireremoval/wireremoval_025 .png
   :scale: 100%
   :alt: image01
   :target: path

5. 指を復元しました。細かな指の動きはRotoにアニメーションを付けて修正します。

.. figure:: ./../../_images/wireremoval/wireremoval_026 .png
   :scale: 100%
   :alt: image01
   :target: path

.. figure:: ./../../_images/wireremoval/wireremoval_027 .png
   :scale: 100%
   :alt: image01
   :target: path

6. これで完成です。