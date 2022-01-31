---
layout: default
title: About HycFrame3D
---

## HycFrame2Dについて

>HycFrame2DはWindowsをプラットフォームにして、汎用性が持っている通用2Dゲーム開発できるのフレームワークを目指して作った物であります。

[ソースコード](https://github.com/HIBICUS-CAI/HycFrame2D)

フレームワークの特徴 :

- Entity+Componentの組み方
- シーンの内容物をJSON化してデータとして保存
- スクリプトに似てる特定コードの実行方

## フレームがサポートしている内容

主に四つの部分に分けられています :

- 特定の処理をレジスター・実行するできるInteractionとInput仕組み
- Interaction・Input以外用意している多様なコンポーネント
- SceneNodeに関する管理・操作機能
- 音声・JSON解析等のサブシステム

コンポーネントについての情報 :

|Component種類|提供している機能|
|:----:|:----:|
|(Actor&UI)<br>[A/U]TransformComponent|Objectの位置、角度と大きさ調整|
|(Actor&UI)<br>[A/U]InputComponent|レジスターされていた入力関数を入力処理段階で自動的に呼び出す<br>Unity C# Scriptのようなカスタマイズできる処理仕組み|
|(Actor&UI)<br>[A/U]InteractComponent|レジスターされていた初期化関数を初期化段階で自動的に呼び出す<br>レジスターされていた更新用関数を更新段階で自動的に呼び出す<br>レジスターされていたリリース関数を削除する時自動的に呼び出す<br>Unity C# Scriptのようなカスタマイズできる処理仕組み|
|(Actor&UI)<br>[A/U]SpriteComponent|テクスチャの描画処理<br>Offset色処理|
|(Actor)<br>[A]CollisionComponent|二つのものは当たっているかどうかを判断<br>円と四角形処理のサポート|
|(Actor)<br>[A]AnimateComponent|複数のスプライトアニメーションを読み込み<br>特定のアニメーションに変わる<br>再生速度調整|
|(Actor)<br>[A]TimerComponent|複数のタイマーを作る<br>特定タイマーの開始、一時停止、リセット処理<br>ある時間に越えたどうかの判断|
|(UI)<br>[U]BtnMapComponent|隣のボタンを選択する機能<br>このボタンは選択されているかどうかの判断|
|(UI)<br>[U]TextComponent|キャラクタ配列より自動的に文字を描画する仕組み<br>標準フォマードサポート（\n・\t等）|

## コードの組み方

## 特に頑張ったところ

## フレームを実行するため必要なもの（整合済）

## 改善点

## これで作っていた作品