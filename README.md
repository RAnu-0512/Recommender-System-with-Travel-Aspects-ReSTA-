# システム概要
システム上で「旅行スタイル」「観点」「行ってみたいスポット」「行って良かったスポット」を選択でき、それに基づいてスポットが推薦されます。
推薦は4つの選択条件の内1つ以上選択することによって行われます。

以下はシステムの動作画面の一連です。

![観点](https://github.com/user-attachments/assets/1917a073-c45b-44d7-9cd4-ff0a22a11432)
![スタイル](https://github.com/user-attachments/assets/fd2d2d6d-5fb1-4196-a5da-8e9fd2ed028c)
![行ってみたい](https://github.com/user-attachments/assets/99a852d7-871e-422e-adb6-2ceb197ae47b)
![行って良かった](https://github.com/user-attachments/assets/3b108827-14c4-459c-a390-d0580372510b)
![スポット詳細](https://github.com/user-attachments/assets/da358a7f-1b6f-490a-8b9b-c92895a8df2d)



# システムの具体的な説明
## システムの全体像
![image](https://github.com/user-attachments/assets/c0cda982-47ee-4d9b-a23e-f7f795d803cf)

上記から推薦の都道府県を選択すると以下の画面に遷移します。

![image](https://github.com/user-attachments/assets/68435b39-55f0-48a6-ae50-52128a40d277)

- 左上で観点を検索し選択できます
- 左側の「旅行スタイルを選択」ボタンから旅行スタイルを選択できます。
- 左側の「行ってみたいスポット」欄の「スポットを選択」ボタンから行ってみたいスポットを選択できます。
- 左側の「行って良かったスポット」欄の「スポットを検索」ボタンから行って良かったスポットを検索できます。
- 画面全体にわたってマップが広がっています。ここに推薦スポットがピンで表示されます。
- 画面右側に推薦されたスポットの一覧が表示されます。

## 観点の検索 & 選択欄
![image](https://github.com/user-attachments/assets/30c14e4d-a543-43f3-9cdc-349748ad87d3)

上記の検索欄で自由に検索できます。検索を行うと関連する観点が最大15個表示されます。
以下の画像は岡山県で「自然を楽しみたい」を検索した結果です

![image](https://github.com/user-attachments/assets/e8388b54-38c2-4a9a-9e66-d6c0ed6450b6)

チェックボックスをチェックすると以下のように「選択した観点」ボックスに観点が追加されます

![image](https://github.com/user-attachments/assets/eb28ade2-b2f2-4386-a1cf-ef1de3b2a7c4)

また観点の優先度を以下の5つから選択できます。

![image](https://github.com/user-attachments/assets/192537a8-5432-41d7-97b7-eae3e7b19db6)

- その他のボタン
  - よく見る観点 : 選択地域内で多くのスポットに見られる観点が表示されます  
  - ランダム観点 : 選択地域内の全スポットの観点からランダムで表示されます
  - 再推薦 : 推薦条件を一部だけ変更したい場合、変更した推薦条件で再推薦を行います。例えば推薦範囲を100km->10kmにして再推薦する等。
  

## 推薦条件の変更欄

![image](https://github.com/user-attachments/assets/6334c9f3-ac62-43c3-b91b-88a11b9154e5)

上記の画像では「旅行スタイル」「行ってみたいスポット」「行って良かったスポット」を選択できます。

### 旅行スタイルの選択

![image](https://github.com/user-attachments/assets/27520f06-d0fb-4e9b-b9c6-ecb868bad4e5)

ボタンを押すと以下のようにモーダルが開きます。

![image](https://github.com/user-attachments/assets/1b9f1e21-00e9-4fec-87a8-843aace7d797)

旅行スタイルから一つ以上選択すると以下のように画面が変わります。

![image](https://github.com/user-attachments/assets/707db500-fb05-43ac-b1a4-6129c6948f88)

### 行ってみたいスポットの選択

![image](https://github.com/user-attachments/assets/600ee288-32d1-4ab6-aabb-777ac5e2561f)

ボタンをクリックすると以下のようなモーダルが開きます。

![image](https://github.com/user-attachments/assets/36d1737e-f19e-4889-bcb8-6026c359c23b)

モーダルには全国の有名スポットがランダムに表示されます。

右下の「違うスポットを見る」を押すと別のスポットの切り替わります。

スポットを選択して完了すると以下のようになります。

![image](https://github.com/user-attachments/assets/60295e5a-76e9-40c1-83f8-0cacf7f2c62b)

### 行って良かったスポットの検索 & 選択

![image](https://github.com/user-attachments/assets/4193d5ce-d4ec-4a24-a3ee-f9596ff1e20b)

ボタン押すと以下のモーダルが開きます。

![image](https://github.com/user-attachments/assets/006e17f4-7c14-4691-953c-ec3264c81d10)

モーダル上部で検索ができます。以下は「岡山後楽園」を検索した結果です。

![image](https://github.com/user-attachments/assets/d3d231d3-9ae7-4746-9e1a-6663c4dccf75)

スポットを選択すると以下のようになります。

![image](https://github.com/user-attachments/assets/dc99e2b9-4af1-4d6a-9b85-101653dead41)

### 推薦するスポットの人気度の調整

![image](https://github.com/user-attachments/assets/9b72a033-6e97-42ac-ad24-f6303e1b585f)

上記の画像から推薦するスポットの人気度を調整できます。
「人気」に近いほど人気スポットのみが推薦され、「穴場」に近いほど穴場のスポットが推薦されます。


## 推薦された画面

![image](https://github.com/user-attachments/assets/6e2bb988-1c51-4cfc-a68f-9f51dc9b4756)


上記は推薦された画面となります。選択した推薦条件は観点として「自然」、旅行スタイルとして「歴史を感じる」を選択してます。

以下はマップ上のピンをクリックした際の画面です。

![image](https://github.com/user-attachments/assets/a16c9a65-5626-40c5-b9fa-1a572a8f4b0d)

## スポットの詳細を見る

推薦されたスポットのピンを押した際に出るスポット名を押す、右側の一覧から「詳細を見る」ボタンをクリックするとスポットの詳細を確認できます。以下は詳細ボタンをクリックした時の画面です。

![image](https://github.com/user-attachments/assets/d38fef05-e2c2-43db-99ae-bd25fca76b4b)

詳細ボタンからはじゃらんnetへのurl、画像の出典、拡大画像、すべての観点を見れます。

![image](https://github.com/user-attachments/assets/c78646cb-6cb4-4cf5-893b-a6a167322f29)

上記の画像は観点の一部となります。

赤色の観点は関連性が高い観点で、「関連」の部分には、どの設定条件に関連しているのかが分かります。

また観点の横の「レビューアイコン」からはレビューを確認できます。


# プログラム実行方法
python server.pyでプログラムが実行されます。

python server.py --port ____　でポート番号を指定することができます。

例えば python server.py --port 8000 な形です。

但し、"../word2vec/"のパスに事前に用意したword2vecのベクトルモデルが必要です。

以下のURLで事前に学習済みの単語ベクトルを取得できます。

https://fasttext.cc/docs/en/crawl-vectors.html

word2vecモデルを用意できない方は"server.py"と"return_aspect.py"の"<注意>"のコメントを読み、適宜コメントアウトしてください。

なお、"./data/pre_processed_review_txt/<各都道府県>/"のフォルダ上には、ダミーのレビューデータを用意しているため、実際のレビューはシステム上で確認できません。こちらにレビューテキストを改行で保存することでシステム上でも観点に関連するレビューを確認することができます。

フロントエンドはJavaScript、バックエンドはPythonで、Flaskを利用して構築しています。



