# 課題５　判別分析法

今までの課題と同じく標準画像「sushi.png」を元画像とする。

判別分析法を用いて画像を二値化する。


ORG=imread('sushi.png'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
![img](http://i.imgur.com/IgTCPDX.png)  
図1 白黒原画像

H = imhist(ORG); %ヒストグラムのデータを列ベクトルEに格納  
myu_T = mean(H);  
max_val = 0;  
max_thres = 1;  
for i=1:255  
C1 = H(1:i); %ヒストグラムを2つのクラスに分ける  
C2 = H(i+1:256);  
n1 = sum(C1); %画素数の算出  
n2 = sum(C2);  
myu1 = mean(C1); %平均値の算出  
myu2 = mean(C2);  
sigma1 = var(C1); %分散の算出  
sigma2 = var(C2);  
sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); %クラス内分散の算出  
sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2); %クラス間分散の算出  
if max_val<sigma_B/sigma_w  
max_val = sigma_B/sigma_w;  
max_thres =i;  
end;  
end;  

IMG = ORG > max_thres;  
imagesc(IMG); colormap(gray); colorbar;  
![img](http://i.imgur.com/7GTa5S3.png)  
図2 判別分析法の結果

まとめ

判別分析法の結果を画像で見てみると、白身である「いか」は真っ白である一方で海老等白一色でない他の寿司は黒く塗り潰されている。
判別分析法により背景と対象物を明確に判別できていることが確認できる。