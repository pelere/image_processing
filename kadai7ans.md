# 課題7　ダイナミックレンジの拡大

今までの課題と同じく標準画像「sushi.png」を元画像とする。

画素のダイナミックレンジを０から２５５にする。


元の白黒画像  
ORG=imread('sushi.png'); % 画像の読み込み 
ORG= rgb2gray(ORG); % 白黒濃淡画像に変換
  
![img](http://i.imgur.com/BfYpzQJ.png)  

図1 白黒原画像

imhist(ORG); % 濃度ヒストグラムを生成、表示

![img](http://i.imgur.com/HW1iJ3F.png)  

図2 原画像のヒストグラム

ORG = double(ORG);  
mn = min(ORG(:)); % 濃度値の最小値を算出
mx = max(ORG(:)); % 濃度値の最大値を算出  
ORG = (ORG-mn)/(mx-mn)*255;
imagesc(ORG); colormap(gray); colorbar; % 画像の表示


![img](http://i.imgur.com/ijBjPhB.png)  

図3 ダイナミックレンジ変更の結果

ORG = uint8(ORG);  
imhist(ORG); % 濃度ヒストグラムを生成、表示

![img](http://i.imgur.com/sPcgXMK.png)  

図4 変更後のヒストグラム


まとめ

uint8は8bit符号なし整数への変換を行う関数である。  

8bitでは値が0～255までの範囲を取るため、必ず正の値を取る。

つまりORGの正負を正の状態にしている。

