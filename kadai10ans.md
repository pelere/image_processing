# 課題10 画像のエッジ抽出

今までの課題と同じく標準画像「sushi.png」を元画像とする。


エッジ抽出を体験する。


まず，画像を白黒の画像に変換する．

ORG=imread('sushi.png'); % 原画像の入力

ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

![img](http://i.imgur.com/VcS8wWB.png)

図1　白黒原画像


プレウィット法のエッジ抽出を行う。

IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）

imagesc(IMG); colormap('gray'); colorbar;% 画像表示


![img](http://i.imgur.com/23lvsVg.png)

図2　プレウィット法によるエッジ抽出の結果

ソベル法によるエッジ抽出を行う。

IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）

imagesc(IMG); colormap('gray'); colorbar;% 画像表示

![img](http://i.imgur.com/WmDRtoA.png)

図3　ソベル法によるエッジ抽出の結果

キャニー法によるエッジ抽出を行う

IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）

imagesc(IMG); colormap('gray'); colorbar;% 画像表示

![img](http://i.imgur.com/CFVPMPy.png)

図4　キャニー法によるエッジ抽出の結果


まとめ

プレウィット法、ソベル法、キャニー法の3つの方法によるエッジ抽出を体験した。

これらの結果を比較する。

プレウィット法とソベル法の違いは今回の画像からはあまり見受けられない。

一方、プレウィット法とソベル法が主に輪郭だけを抽出しているのに対し、キャニー法は輪郭とその内部に至るまで抽出を行っていると見受けられる。

今回の原画像では寿司下駄の木目を抽出しようとしているために荒く見えているが、他の画像、特に背景の要素の薄い画像ではこの3つの中でキャニー法が最も良く抽出を行える方法であると考えられる。