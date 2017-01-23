課題1:標本化間隔と空間解像度


標準画像「sushi.png」を元画像とする．

ORG=imread('sushi.png'); % 原画像の入力

imagesc(ORG); axis image; % 画像の表示

によって表示された原画像は図1のようになった．

![img](http://i.imgur.com/AJkIVUy.png)

図1　原画像

原画像を1/2にサンプリングするには，画像を1/2に縮小した後，2倍に拡大する．拡大する際には，単純補間するためにboxオプションを利用する．

IMG = imresize(ORG,0.5); % 画像の縮小

IMG2 = imresize(IMG,2,'box'); % 画像の拡大

imagesc(IMG2); axis image; % 画像の表示

1/2サンプリングの結果を図2に示す．

![img](http://i.imgur.com/NqoiUzR.png)

図2 1/2サンプリング

同様に，1/4サンプリングをするには，1/2サンプリングした画像を1/2に縮小した後，2倍に拡大することで可能である．

IMG = imresize(IMG,0.5); % 画像の縮小

IMG2 = imresize(IMG,4,'box'); % 画像の拡大

imagesc(IMG2); axis image; % 画像の表示

1/4サンプリングの結果を図3に示す．

![img](http://i.imgur.com/VNb15HU.png)

図3 1/4サンプリング

![img](http://i.imgur.com/Bvetc41.png)

図4 1/8サンプリング

![img](http://i.imgur.com/OaxA1nz.png)

図5 1/16サンプリング


まとめ

このようにサンプリング幅が大きくなると，モザイク状のサンプリング歪みが発生する．