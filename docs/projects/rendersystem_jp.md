---
layout: default
title: About Render System Lib
---

## レンダリングシステムライブラリーについて

>異なるスタイルのレンダリングをサポートできる柔軟性を持って、Windowsプラットフォームでのリアルタイムレンダリングライブラリー

このライブラリーは、レンダリングパイプラインを容易に構築できるため開発したものであります。

コンテンツは主に以下の通り分けられています :

- パイプラインシステム
  - パイプライン Pipeline（複数のトピックより組み立てる）
  - トピック Topic（複数のパスより組み立てる）
  - パス Pass（特定のDraw・Dispatchを行うオブジェクト）
- ほかのサブシステム
  - DirectXデバイス管理
  - カメラ作成・管理
  - 光源作成・管理
  - パーティクル作成・管理
  - Mesh作成・読み込み・管理
  - DrawCall管理
  - リソース管理
  - 静的リソース参照

レンダリングシステムライブラリーは、サブシステムにサポートされて、**異なるトピックより柔軟なレンダリングパイプラインを構築**、その中に必要なパイプラインで描画するという仕組みです。

例えば、[HycFrame3D](hycframe3d_jp.md)より作ったゲーム[JADEITE](jadeite_jp.md)の描画パイプラインは以下の順で、複数のトピックより構築されています :

`Diffuse+Normal+Position+Material+Depth Topic` → `SSAO Topic` → `Shadow Map Topic` → `Deferred Rendering Topic` → `Skybox Topic` → `Bloom Topic` → `Particle Topic` → `UI Topic`

## パイプラインシステム

## ほかのサブシステム

## 自分なりに頑張ったところ

## 改善すべきなところ