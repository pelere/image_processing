# 課題２　階調数と疑似輪郭
２階調，４階調，８階調の画像を生成せよ．

課題1と同じく標準画像「sushi.png」を元画像とする。

まず、画像から白黒画像を生成する。

clear; % 変数のオールクリア  
ORG=imread('view.png'); % 原画像の入力  
ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % 画像の表示  

![img](http://i.imgur.com/S9n36Rv.png)  
図1 白黒画像


2階調画像の生成を行う。
% ２階調画像の生成  
IMG = ORG>128;  
imagesc(IMG); colormap(gray); colorbar;  axis image;

![img](http://i.imgur.com/ueC87F2.png)  
図2 2階調

4階調画像の生成を行う。
% ４階調画像の生成  
IMG0 = ORG>64;  
IMG1 = ORG>128;  
IMG2 = ORG>192;  
IMG = IMG0 + IMG1 + IMG2;  
![img](http://i.imgur.com/0lhmmxz.png)  
図3 4階調

8階調画像の生成を行う。
8階調画像を生成するプログラムは、2階調、4階調画像生成のサンプルプログラムから以下のプログラムであると考えた。
% ８階調画像の生成  
IMG0 = ORG>32;  
IMG1 = ORG>64;  
IMG2 = ORG>96;  
IMG3 = ORG>128;  
IMG4 = ORG>160;  
IMG5 = ORG>192;  
IMG6 = ORG>224;  
IMG = IMG0 + IMG1 + IMG2 + IMG3 + OMG4 + IMG5 + IMG6;  
![img](http://i.imgur.com/SRrvm3Q.png)  
図4 8階調

まとめ
２階調，４階調，８階調の画像を生成した。
階調数に応じて8階調、4階調、2階調の順に画像が鮮明になっていることが確認できる。  
