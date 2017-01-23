# 課題3　閾値処理


今までの課題と同じく標準画像「sushi.png」を元画像とする。

閾値を4パターン設定し、閾値処理した画像を示す。

まず、画像を白黒の画像に変換する。


ORG=imread('sushi.png'); % 原画像の入力

ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar; % 画像の表示



![img](http://i.imgur.com/PTeOGya.png)

図1　白黒原画像

輝度値が64以上の画素を1、その他を0に変換する。


IMG = ORG > 64; 

imagesc(IMG); colormap(gray); colorbar;


結果は図2のようになった。

![img](http://i.imgur.com/p4ZrN1A.png)

図2　輝度値を64に設定した画像

輝度値が96以上の画素を1、その他を0に変換する。


IMG = ORG > 96;

imagesc(IMG); colormap(gray); colorbar;


結果は図3のようになった。

![img](http://i.imgur.com/GW5u1YV.png)

図3　輝度値を96に設定した画像


輝度値が128以上の画素を1、その他を0に変換する。



IMG = ORG > 128;

imagesc(IMG); colormap(gray); colorbar;


結果は図4のようになった。

![img](http://i.imgur.com/aZmSBWw.png)

図4　輝度値を128に設定した画像

輝度値が192以上の画素を1、その他を0に変換する。


IMG = ORG > 192;

imagesc(IMG); colormap(gray); colorbar;


結果は図5のようになった。

![Imgur](http://i.imgur.com/sdYJ69b.png)

図5　輝度値を192に設定した画像

まとめ

境界値以下の輝度は0となるため、輝度の境界値を上げていくと輝度0の画素が増え、徐々に画像全体が黒く変化していくことが確認できる。