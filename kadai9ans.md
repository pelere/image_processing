#課題9　メディアンフィルタと先鋭化

今までの課題と同じく標準画像「sushi.png」を元画像とする。

メディアンフィルターを適用し，ノイズ除去を体験する。


画像を白黒の画像に変換する。

ORG=imread('sushi.png'); % 原画像の入力

ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

![img](http://i.imgur.com/SGnHxmR.png)

図1　白黒原画像

この画像にノイズを添付する。

ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

![img](http://i.imgur.com/HiJC31m.png)

図2　ノイズを添付した画像

平滑化フィルタで雑音除去を行う。

IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

![img](http://i.imgur.com/2GVuc52.png)

図3　平滑化フィルタで雑音除去を行った画像

メディアンフィルタで雑音除去を行う。

IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

![img](http://i.imgur.com/iFb9wbU.png)

図4　メディアンフィルタで雑音除去を行った画像


こちらでフィルタを設計し、それを適用する

f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計

IMG = filter2(f,IMG,'same'); % フィルタの適用

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

![img](http://i.imgur.com/qs3FeS3.png)

図5　フィルタを適用した画像


まとめ

平滑化フィルタとメディアンフィルタによるノイズの除去を体験した。

平滑化フィルタは多少ノイズが混じってはいるが色彩は原画像に最も近い。

反対に、メディアンフィルタは色彩は原画像よりも明るいが、ノイズはほとんど見受けられない。

自分の求める画像加工に応じてフィルタを使い分けることが大事であると言える。