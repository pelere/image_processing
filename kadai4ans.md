# 課題４　画像のヒストグラム

今までの課題と同じく標準画像「sushi.png」を元画像とする。
画素の濃度ヒストグラムを生成する。


ORG=imread('view.png'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
![img](http://i.imgur.com/x390JSF.png)  
図1 白黒画像

imhist(ORG);   
![img](http://i.imgur.com/3kMhmwG.png)  
図2 ヒストグラム

まとめ

sushi.pngのヒストグラムを生成した。
図2のヒストグラムは右側に偏っているため、元画像が明るい（白めの）画像であることが確認できる。