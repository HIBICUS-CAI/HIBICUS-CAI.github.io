---
layout: default
title: About JADEITE
---

[【作品集　目次】](../projects_jp.md)

---

![JADEITE_logo](../../assets/jadeite_logo.png)

## JADEITEについて

>JADEITEとは、翡翠のこと。2DインディーズゲームCELESTEを3Dバージョンに拡張したゲームです。

**リンク**

- [ソースコード](https://github.com/HIBICUS-CAI/HycFrame3D/tree/game-backup/JADEITE)
- [バイナリファイル](https://github.com/HIBICUS-CAI/HycFrame3D/releases/tag/JADEITE_v1.0)

![JADEITE_logo](../../assets/jadeite_3.jpg)

## プレイ動画

<iframe width="100%" height="500" src="https://www.youtube.com/embed/-1hSB3A7lp8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## 入力サポートと操作方法

サポートされているデバイスは三つあります：**キーボード＋マウス**、**XBOXコントローラー**、**PS4コントローラー**。ほかのコントローラーはボタンのレイアウトがずれてしまう可能性があるので要注意です。

コントローラーはゲーム開始する前、事前に接続しておいてください。 コントローラーがついている場合でも、キーボード＋マウスで操作することはできます。

操作方法については入力デバイスに分けて説明します（チュートリアルには合わせて説明しています）。

- キーボード＋マウス
  - **ボタン選択**：カーソルを上に移動・上下左右のキー
  - **ボタンクリック**：マウス左クリック・ENTERキー
  - **移動**：WASDキー
  - **カメラ**：マウス
  - **ジャンプ**：SPACEキー
  - **ダッシュ**：左のALTキー
  - **銃を構える**：マウス右クリック（押し続く）
  - **弾を撃つ**：銃を構える上にマウス左クリック
  - **一時停止**：ESCキー
- コントローラー（GamePad）
  - **ボタン選択**：左側の方向ボタン
  - **ボタンクリック**：右側の下のボタン（A・×）
  - **移動**：左スティック
  - **カメラ**：右スティック
  - **ジャンプ**：右側の下のボタン（A・×）・左肩の前のボタン（L1・ LB）
  - **ダッシュ**：右肩の前のボタン（R1・RB）
  - **銃を構える**：左肩の後ろのボタン（L2・LT）
  - **弾を撃つ**：銃を構える上に右肩の後ろのボタン（R2・RT）
  - **一時停止**：右側のメニューボタン（OPTIONS・≡）

## ゲームシステム

ダッシュ操作を中心に、山に登るゲームです。

ダッシュはカメラが向いている方向に高速移動するというスキル、平面だけではなく、どの方向でもダッシュできます。

地面に戻っていない限り、ダッシュは一回しかできません。

ダッシュしている、あるいはダッシュした後、ダッシュパワーを空中でも回復できるため、緑色とピンク色で光っている水晶を作りました。緑の方はそのまま当たるとできますが、ピンクの方はまず弾を撃って、ピンクから青までになったあと当たると回復できます。

プレーヤーには弾丸エネルギー三個分持っています、銃を構えるときは弾丸エネルギーをだんだん消費します。その上、弾丸を撃つとき今未だ完全に消費されていないエネルギーを消費します。（例えば：元々は 3.0、銃を構えるため 2.6 になった、そして撃ったあと 2.0 になる）

銃を構えるとき、プレーヤーの移動速度が遅くなり、移動距離はそのまま減られません。これによって、プレーヤーは精密操作あるいは細かい位置調整ができます。

終点には回っている黄金の火山があり、それと当たると当ステージクリアです。

## OPTIONS調整

毎秒のフレーム数が足りない場合（60以下）、先ずゲームのフレームワークは正しいグラフィックカードを使用しているかどうかをご確認ください。

ゲームは自動的により正しいグラフィックカードを選択していますが、もし万が一違うものに選んだら、ご自分で正しいグラフィックカード番号をコンフィグレーションファイルに記入する必要があります。

記入方は以下の通り：

- ゲームを一度実行して（**実行しないと出てこないです**）`(HycFrame3D/)Assets/Configs/AutoCreated_AdapterInfoInSystem.txt`を開く

    ![Adapter_Info](../../assets/h3d_adapter_config.png)

- `(HycFrame3D/)Assets/Configs/render-deviceconfig.json`を開いて、**使いたいグラフィックカードの番号**を`force-adapter-index`後ろ`null`のところに上書きして保存してください。（nullはフレームワークにより自動的に選択するという意味です）

**もしそうしてもFPSはまだ足りない場合**、`(HycFrame3D/)Assets/Configs/render-effect-config.json`を開いて調整を行ってください。

- `(HycFrame3D/)Assets/Configs/render-effect-config.json`を開く

    ![Adapter_Info](../../assets/jadeite_effect_config.png)

- `ssao-blur-loop-count`の数を`0`から`4`まで調整して保存、数値が小さいと処理量が少ない、大きくと処理量が多い
- `filter-level`後ろの数を`0`から`3`まで調整して保存、数値が小さいと処理量が少ない、大きくと処理量が多い
- まだ足りない場合、`particle-off`後ろの`false`を`true`にしてください（ですが、こうしたらビジュアル的にはちょっと減られるかもしれません）

## アピールしたいところ

- ゲームシステムはCELESTEを参照して、簡単な操作でも色んな組合せができます
     ![CELESTE_Like](../../assets/jadeite_5.jpg)
- [フレームワーク](hycframe3d_jp.md)により綺麗なゲーム画面です

このゲームが使っている描画パイプラインにつきまして説明します。

---

1. 描画パイプライン開始
2. MRTでDiffuseテクスチャカラー、世界空間法線（必要なところにバンプマッピングを利用）、世界空間座標、マテリアルのDiffuse AlbedoとFresnel R0とShininessと奥行きを描画

    |                       シーン1                       |                       シーン2                       |
    | :-------------------------------------------------: | :-------------------------------------------------: |
    | ![Mrt_1_1](../../assets/jadeite_render_mrt_1_1.png) | ![Mrt_1_2](../../assets/jadeite_render_mrt_1_2.png) |
    | ![Mrt_2_1](../../assets/jadeite_render_mrt_2_1.png) | ![Mrt_2_2](../../assets/jadeite_render_mrt_2_2.png) |
    | ![Mrt_3_1](../../assets/jadeite_render_mrt_3_1.png) | ![Mrt_3_2](../../assets/jadeite_render_mrt_3_2.png) |
    | ![Mrt_4_1](../../assets/jadeite_render_mrt_4_1.png) | ![Mrt_4_2](../../assets/jadeite_render_mrt_4_2.png) |
    | ![Mrt_5_1](../../assets/jadeite_render_mrt_5_1.png) | ![Mrt_5_2](../../assets/jadeite_render_mrt_5_2.png) |
    | ![Mrt_6_1](../../assets/jadeite_render_mrt_6_1.png) | ![Mrt_6_2](../../assets/jadeite_render_mrt_6_2.png) |

3. 法線と奥行きによってSSAO（スクリーンスペース・アンビエント・オクルージョン）処理を行う、そして再び法線と奥行きによってEdge-preserving Smoothingを行う（エッジを崩さないブラー）

    |                        シーン1                        |                        シーン2                        |
    | :---------------------------------------------------: | :---------------------------------------------------: |
    | ![Ssao_1_1](../../assets/jadeite_render_ssao_1_1.png) | ![Ssao_1_2](../../assets/jadeite_render_ssao_1_2.png) |
    | ![Ssao_2_1](../../assets/jadeite_render_ssao_2_1.png) | ![Ssao_2_2](../../assets/jadeite_render_ssao_2_2.png) |

4. 影が出る光源から奥行きでシャドウマップを描画

    |                        シーン1                        |                        シーン2                        |
    | :---------------------------------------------------: | :---------------------------------------------------: |
    | ![Shadow_1](../../assets/jadeite_render_sdwmap_1.png) | ![Shadow_2](../../assets/jadeite_render_sdwmap_2.png) |

5. MRTで描画したものとSSAOマップとシャドウマップを合わせて、遅延レンダリングを行う（Deferred Rendering）

    |                          シーン1                           |                          シーン2                           |
    | :--------------------------------------------------------: | :--------------------------------------------------------: |
    | ![Deferred_1](../../assets/jadeite_render_defrender_1.png) | ![Deferred_2](../../assets/jadeite_render_defrender_2.png) |

6. スカイボックス（Skybox）を描画する

    |                     シーン1                     |                     シーン2                     |
    | :---------------------------------------------: | :---------------------------------------------: |
    | ![Sky_1](../../assets/jadeite_render_sky_1.png) | ![Sky_2](../../assets/jadeite_render_sky_2.png) |

7. 光源の描画と結果をブラーして作り出すシンプルなブルーム（Bloom）、そしてメインRTVにブレンド

    |                         シーン1                         |                         シーン2                         |
    | :-----------------------------------------------------: | :-----------------------------------------------------: |
    | ![Bloom_1_1](../../assets/jadeite_render_bloom_1_1.png) | ![Bloom_1_2](../../assets/jadeite_render_bloom_1_2.png) |
    | ![Bloom_2_1](../../assets/jadeite_render_bloom_2_1.png) | ![Bloom_2_2](../../assets/jadeite_render_bloom_2_2.png) |
    | ![Bloom_2_1](../../assets/jadeite_render_bloom_3_1.png) | ![Bloom_2_2](../../assets/jadeite_render_bloom_3_2.png) |

8. Compute Shaderでパーティクル生成、シミュレーション、カーリング、タイルレンダリング（particle emit, simulation, culling, tile rendering）
9.  パーティクルをメインRTVにブレンド

    |                          シーン1                          |                          シーン2                          |
    | :-------------------------------------------------------: | :-------------------------------------------------------: |
    | ![Particle_1](../../assets/jadeite_render_ptcblend_1.png) | ![Particle_2](../../assets/jadeite_render_ptcblend_2.png) |

10. UIなどのSprite描画

    |                    シーン1                    |                    シーン2                    |
    | :-------------------------------------------: | :-------------------------------------------: |
    | ![Ui_1](../../assets/jadeite_render_ui_1.png) | ![Ui_2](../../assets/jadeite_render_ui_2.png) |

11. パイプライン完成

詳しい内容は[レンダリングシステムについてのページ](rendersystem_jp.md)をご覧ください。

## 他の情報

- 開発期間：実装（フレームワーク開発期間抜き）約一週間
- 開発ツール：HycFrame3D、Visual Studio、Visual Studio Code、RenderDoc、Git、自作モデルファイル処理ツール

---

[【作品集　目次】](../projects_jp.md)