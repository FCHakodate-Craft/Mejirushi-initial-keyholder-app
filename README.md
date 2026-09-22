# Mejirushi initial keyholder app

iPadで枠・イニシャル・チャーム色を選び、レーザー加工用SVGとカラー確認用JSONを生成する静的Webアプリです。

## 素材の配置

- 枠：`assets/frames/frame-01.svg` ～ `frame-15.svg`
- イニシャル：`assets/initials/style-1/A.svg` ～ `Z.svg`

IllustratorからSVGを書き出す際は、文字や図形をすべてパス化し、塗りなし、線色をCMYKのM100/Y100にしてください。SVG上では `#FF0000` として正規化します。枠SVGとイニシャルSVGは同じ `viewBox`（推奨 `0 0 40 40`）で書き出してください。枠ごとにイニシャル位置を調整するときは、イニシャルデータ側を40mmのアートボード上の完成位置へ配置して書き出します。

## URL

端末ごとに `?device=A`、`?device=B` のように指定すると受付番号を分けられます。

## 保存データ

- 加工用：枠＋イニシャルを統合した赤線のみのSVG
- 確認用：受付番号、枠、イニシャル、チャーム色を記録したJSON

Google Drive送信は既存のGoogle Apps Script URLを使用しています。GAS側が追加の `proof` 項目を無視する構成でもSVG保存は従来どおり動作します。
