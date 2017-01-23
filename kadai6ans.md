# 課題６　画像の二値化

今までの課題と同じく標準画像「sushi.png」を元画像とする。

画像の二値化を行う。


元の白黒画像  
ORG=imread('sushi.png'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  

![img](http://i.imgur.com/eyaPHOH.png)  

図1 白黒原画像

輝度128を境に二値化  
IMG = ORG>128; % 128による二値化

![img](http://i.imgur.com/oZrYj4E.png)  

図2 輝度128による二値化画像

ディザ法  
IMG = dither(ORG); % ディザ法による二値化

![img](http://i.imgur.com/Vhd47kc.png)  

図3 ディザ法による二値化画像


まとめ

輝度128による画像の二値化とディザ法による画像の二値化を行った。

ディザ法による二値化の方が鮮明に処理できていることが確認できる。