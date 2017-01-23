# 課題8　ラベリング

今までの課題と同じく標準画像「sushi.png」を元画像とする。

二値化された画像の連結成分にラベルを付ける。


原画像を白黒の画像に変換する．


ORG=imread('sushi.png'); % 原画像の入力

ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

![img](http://i.imgur.com/HcmEjtv.png)

図1　白黒原画像


閾値128で二値化する．


IMG = ORG > 128; % 閾値128で二値化

imagesc(IMG); colormap(gray); colorbar; % 画像の表示


![img](http://i.imgur.com/uUP5HOs.png)

図2　閾値128で二値化した画像

ラベリングを行う

IMG = bwlabeln(IMG);

imagesc(IMG); colormap(jet); colorbar; % 画像の表示

![img](http://i.imgur.com/pbuxDIo.png)

図3　ラベリング結果


まとめ

課題4のヒストグラムでsushi.pngが全体的に白目の画像であることは既に確認できている。

それゆえ、二値化で画像のほとんどが白化してしまうため、ラベリングを行うと二値化で白くなっている部分以外は青くなってしまう。

かろうじて海老の目やまぐろの身の中の濃赤色部分の輪郭が確認できる程度である。