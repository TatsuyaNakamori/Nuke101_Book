このセクションの概要
####################


.. contents:: このページの目次:
   :depth: 2
   :local:

このセクションではエクスプレッションについて学習します。

背景の作成
#######################

1. NodeGraph上で ``TAB`` キーを押して「Constant[Image]」ノードを表示します。

2. Propatiesのformatを[HD_720]にします。

.. figure:: ./../../_images/expression/expression_001 .png
   :scale: 100%
   :alt: image01
   :target: path

エクスプレッション
#######################

1.素材の[gear01-03.png]を読み込みます。

.. figure:: ./../../_images/expression/expression_002 .png
   :scale: 100%
   :alt: image01
   :target: path

2.素材と背景をMergeノードで繋ぎます。

.. figure:: ./../../_images/expression/expression_003 .png
   :scale: 100%
   :alt: image01
   :target: path

3. Transformノードで位置と回転を合わせます。Propatiesの[translate]で位置の調整。[rotate]で回転を調整します。

.. figure:: ./../../_images/expression/expression_005 .png
   :scale: 100%
   :alt: image01
   :target: path

.. figure:: ./../../_images/expression/expression_004 .png
   :scale: 100%
   :alt: image01
   :target: path

4. エクスプレッション用のTransformノードを作成します。

.. figure:: ./../../_images/expression/expression_006 .png
   :scale: 100%
   :alt: image01
   :target: path

5. gear01.pngのエクスプレッション用のTransformノードのrotateを右クリックし、[Add expression]を選択します。

.. figure:: ./../../_images/expression/expression_007 .png
   :scale: 100%
   :alt: image01
   :target: path

6. Expressionに[frame]を入力します。フレーム数に応じてその数がrotateに入力されるようになります。

.. figure:: ./../../_images/expression/expression_008 .png
   :scale: 100%
   :alt: image01
   :target: path

7. gear02とgear03の回転をgear01とエクスプレッションで接続させて回転させます。利点としてはgear01を変更することでgear02とgear03も自動で変更されます。

8. gear01のTransformのrotateを右クリック、Copy Animationをクリックします。

.. figure:: ./../../_images/expression/expression_009 .png
   :scale: 100%
   :alt: image01
   :target: path

9. gear02.03のTransformのrotateを右クリックしPaste Absoluteをクリック。これでエクスプレッションでつながりました。

.. figure:: ./../../_images/expression/expression_010 .png
   :scale: 100%
   :alt: image01
   :target: path

10. gear02の円周はgear01の半分で、gear01が一周するとgear02は二週するためgear02のエクスプレッションを表示して[*-2]と入力します。

.. figure:: ./../../_images/expression/expression_011 .png
   :scale: 100%
   :alt: image01
   :target: path

11. gear03はgear01の1/4なので[*4]を入力します。

.. figure:: ./../../_images/expression/expression_012 .png
   :scale: 100%
   :alt: image01
   :target: path

12. 全体の回転数を変更したい場合はgear01のエクスプレッションを変更します。