課題5　判別分析法



まず，画像を白黒の画像に変換する．

ORG=imread('dog.png'); % 原画像の入力

ORG = rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar;

表示結果は図1のようになる．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog5-1.png)

図1　原画像

次に，判別法を用いて画像を2値化する．

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

sigma_w = (n1 sigma1+n2sigma2)/(n1+n2); %クラス内分散の算出

sigma_B = (n1 (myu1-myu_T)^2+n2(myu2-myu_T)^2)/(n1+n2); %クラス間分散の算出

if max_val<sigma_B/sigma_w

max_val = sigma_B/sigma_w;

max_thres =i;

end;

end;

IMG = ORG > max_thres;

imagesc(IMG); colormap(gray); colorbar;

表示結果は図2のようになる

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog5-2.png)

図2　判別法を用いた2値化
