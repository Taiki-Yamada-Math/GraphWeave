# GraphWeave

**Draw a network by hand, and measure its geometry and structure on the spot.**
自分で描いたネットワークの幾何学的・構造的な指標を、その場で計算して色で可視化する iOS アプリです。

This repository hosts the **support** and **privacy policy** pages for the app.
このリポジトリは、アプリの **サポート** および **プライバシーポリシー** ページを公開するためのものです。

- Support / サポート: `https://Taiki-Yamada-Math.github.io/GraphWeave/support.html`
- Privacy Policy / プライバシーポリシー: `https://Taiki-Yamada-Math.github.io/GraphWeave/privacy.html`


---

## 日本語

### 概要
GraphWeave は、指でノードとリンクを置くだけでグラフを作り、離散曲率や各種中心性を瞬時に計算して色分け表示するツールです。グラフ理論・ネットワーク科学の学習や、小さなネットワークの構造確認に向いています。

### 主な機能
- ノードとリンクを直感的に描画（ドラッグで配置調整）
- 離散リッチ曲率（Ollivier–Ricci）をリンクごとに計算
- 6種類のノード指標：次数 / 近接 / 媒介 / 固有ベクトル中心性、クラスタ係数、PageRank
- 指標に応じてリンクまたはノードを coolwarm（青→赤）で自動色分け＋数値表示
- 作ったグラフを端末内に保存し、いつでも読み込んで再分析
- 完全オフライン動作。アカウント登録・通信は不要

### プライバシー
データを一切収集しません。作成したグラフは端末内にのみ保存され、外部に送信されることはありません。広告もありません。詳細は [privacy.html](privacy.html) を参照。

### サポート
ご質問・ご要望・不具合報告はお気軽にどうぞ。
連絡先: `taiki_yamada@riko.shimane-u.ac.jp`

---

## English

### Overview
GraphWeave lets you sketch a graph with your finger and instantly compute discrete curvature and centrality measures, shown in color. It is made for learning graph theory and network science, and for quickly inspecting the structure of small networks.

### Features
- Sketch nodes and links directly; drag to arrange them freely
- Discrete Ollivier–Ricci curvature for every link
- Six node measures: degree, closeness, betweenness and eigenvector centrality, clustering coefficient, and PageRank
- Links or nodes are colored on a coolwarm (blue→red) scale, with numeric labels
- Save graphs on your device and reopen them anytime to re-analyze
- Fully offline — no account, no network connection

### Privacy
GraphWeave collects no data. Your graphs are stored only on your device and are never sent anywhere. No ads. See [privacy.html](privacy.html).

### Support
Questions, requests, and bug reports are welcome.
Contact: `taiki_yamada@riko.shimane-u.ac.jp`

---

## Notes / 技術メモ
- Metric definitions follow the open-source **networkx** implementations.
  指標の定義はオープンソースの networkx の実装に準拠しています。
- The curvature uses the Ollivier–Ricci definition with idleness ε = 0.5; the Wasserstein-1 transport is solved exactly.
  曲率は idleness ε = 0.5 の Ollivier–Ricci 定義で、Wasserstein-1（最適輸送）を厳密に解いています。
- Built with SwiftUI. Requires iOS 16 or later.
  SwiftUI 製。iOS 16 以降が必要です。

© 2026 GraphWeave. All rights reserved.
