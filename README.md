# 本郷キャンパス Minecraft ワールド / Hongo Campus in Minecraft

東京大学 本郷地区（本郷・弥生・浅野）と周辺の通りを、Minecraft のワールドにしたものです。Java 版と統合版（Bedrock 版）があります。
航空レーザ測量の点群と PLATEAU の建物データから、手を加えずに自動で作っています。1 ブロック = 1 m です。

The Hongo campus of the University of Tokyo and the streets around it, as a Minecraft world, for Java Edition and Bedrock Edition.
Generated automatically from aerial laser scanning and PLATEAU building data, with no hand-placed parts. 1 block = 1 m.

![安田講堂の前から / Yasuda Auditorium and its square](images/yasuda.jpg)

![全体を真上から（上が北） / The whole area from above (north up)](images/overview.jpg)

画像は [BlueMap](https://bluemap.bluecolored.de/)（ワールドをブラウザで見る 3D 地図）で描いたものです。
Rendered with BlueMap, a 3D web map of the world.

## ダウンロード / Download

[Releases](https://github.com/nakamura196/hongo-campus-minecraft-world/releases/latest) から取得してください。

- Java 版 26.3 以降: `hongo-campus.zip` / Java Edition 26.3 or later
- 統合版（iPhone・iPad・Android・Windows など）1.21.130 以降: `hongo-campus.mcworld` / Bedrock Edition 1.21.130 or later
- 範囲: 約 1.1 × 1.65 km（ワールドの x 3072..4171, z 0..1649）
- 出発地点: 安田講堂前 / Spawn: in front of Yasuda Auditorium

## 開き方 / How to open

### Java 版 / Java Edition

1. zip を Minecraft の `saves` フォルダに展開します
   （Windows: `%APPDATA%\.minecraft\saves`、Mac: `~/Library/Application Support/minecraft/saves`）
2. シングルプレイで「hongo-campus」を開きます
3. リソースパックを使うか聞かれたら「はい」を選びます。坂の草を描くためのもので、無いと青緑の板に見えます

Unzip into the `saves` folder, open "hongo-campus" in Singleplayer, and accept the bundled resource pack
(it draws the grass slopes; without it they look like blue-green planks).

### 統合版 / Bedrock Edition

`hongo-campus.mcworld` を開くと、Minecraft にワールドが取り込まれます。
iPhone・iPad では、AirDrop で受け取るか、ファイルアプリでファイルを開き、Minecraft を選びます。
Windows では、ファイルをダブルクリックします。取り込んだあと「プレイ」のワールド一覧から「hongo-campus」を開きます。
リソースパックやビヘイビアパックは使っていません。

統合版のワールドは、Java 版のワールドを [Chunker](https://github.com/HiveGamesOSS/Chunker)（Hive Games、MIT）で変換したものです。
草の坂のリソースパックは Java 版用のため、統合版では坂の草が普通の草ブロックになります。

Open `hongo-campus.mcworld` and Minecraft imports it (on iPhone/iPad, via AirDrop or the Files app; on Windows, double-click).
It is the Java world converted with [Chunker](https://github.com/HiveGamesOSS/Chunker) (Hive Games, MIT).
No resource or behavior packs are used; the grass slopes appear as plain grass blocks.

## 作り方 / How it was made

1. 点群を 1 m の格子に分け、各マスを「地面・建物・木・水・その他」に分類します。
   PLATEAU の建物の輪郭の内側を建物、緑色の点やレーザーが突き抜けた点を木としています
2. 建物は輪郭に沿って屋根の高さまで積み、屋根は平面に当てはめて凸凹を均します。
   ブロックの色は、点群に付いた航空写真の色から近いものを 1 棟 1 色で選びます
3. 木は樹冠を 1 本ずつに分け、幹と葉にします。三四郎池は、点が返ってこない所を水にしています
4. 地面と屋根の傾きは、ハーフブロックと階段で表します

The point cloud is split into a 1 m grid and each cell is classified as ground, building, tree, water or other
(inside a PLATEAU footprint = building; green points or points the laser passed through = tree).
Buildings are filled to roof height along their footprints, with roofs fitted to planes; each building gets one block
chosen from the aerial-photo colours of its points. Tree crowns are split into individual trees with trunks.
Sanshiro Pond is where the laser returned nothing. Slopes on the ground and roofs use slabs and stairs.

## 出典 / Sources

- 東京都デジタルツイン実現プロジェクト 区部点群データ（東京都デジタルサービス局）、
  [G空間情報センター](https://www.geospatial.jp/ckan/dataset/tokyopc-23ku-2024)、CC BY 4.0
- 3D 都市モデル（Project PLATEAU）文京区（国土交通省）を加工して作成（建物の輪郭と高さをブロックに変換）。
  このワールドは国土交通省が作成したものではありません

## ライセンス / License

ワールド（`hongo-campus.zip` と `hongo-campus.mcworld` の中身）は [CC BY 4.0](LICENSE) です。表示の例:
「本郷キャンパス Minecraft ワールド（中村 覚、CC BY 4.0）。東京都 区部点群データ（CC BY 4.0）・国土交通省 PLATEAU を加工して作成」

The world is licensed under [CC BY 4.0](LICENSE). Credit both this work and the sources above.

リソースパックの画像は自作で、ゲーム本体の素材は含みません。
The resource pack texture is original; no game assets are included.

Minecraft の公式製品ではありません。Mojang および Microsoft の承認を受けたものでも、関係するものでもありません。
NOT AN OFFICIAL MINECRAFT PRODUCT. NOT APPROVED BY OR ASSOCIATED WITH MOJANG OR MICROSOFT.

## 作成者 / Author

中村 覚（東京大学） / Satoru Nakamura (The University of Tokyo)
