# Mejirushi initial keyholder app

iPadで枠・イニシャル・チャーム色を選び、レーザー加工用SVGとカラー確認用JSONを生成する静的Webアプリです。

## 素材の配置

- 枠：`assets/frames/frame-01.svg` ～ `frame-15.svg`
- イニシャル：`assets/initials/style-1/A.svg` ～ `Z.svg`

IllustratorからSVGを書き出す際は、文字や図形をすべてパス化し、塗りなしにしてください。加工用SVGの線色はアプリ側で純赤の `#FF0000`（RGB 255, 0, 0）へ統一します。枠SVGとイニシャルSVGは同じ `viewBox` に揃えてください。現在の正式素材はすべて `0 0 113.39 113.39` です。

## URL

端末ごとに `?device=A`、`?device=B` のように指定すると受付番号を分けられます。

## 保存データ

- 加工用：枠＋イニシャルを統合した赤線のみのSVG
- 確認用：受付番号、枠、イニシャル、チャーム色を記録したJSON

## 枠ごとのイニシャル位置補正

- 05 ほし：1.5mm下
- 07 おはな：1.5mm下
- 13 うさぎ：6mm下
- 14 くま：1.5mm下
- 15 ねこ：2.5mm下

Google Drive送信は既存のGoogle Apps Script URLを使用しています。GAS側が追加の `proof` 項目を無視する構成でもSVG保存は従来どおり動作します。
