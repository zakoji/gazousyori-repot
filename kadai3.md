課題3　閾値処理


まず，画像を白黒の画像に変換する．

ORG=imread('dog.png'); % 原画像の入力

ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

表示結果は図1のようになった．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog3-1.jpg)

図1　原画像

次に，輝度値が64以上の画素を1，その他を0に変換する．

IMG = ORG > 64;

imagesc(IMG); colormap(gray); colorbar;

表示結果は図2のようになった．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog3-2.jpg)

図2　輝度値を64に設定した画像

次に，輝度値が96以上の画素を1，その他を0に変換する．

IMG = ORG > 96;

imagesc(IMG); colormap(gray); colorbar;

表示結果は図3のようになった．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog3-3.jpg)

図3　輝度値を96に設定した画像

次に，輝度値が128以上の画素を1，その他を0に変換する．

IMG = ORG > 128;

imagesc(IMG); colormap(gray); colorbar;

表示結果は図4のようになった．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog3-4.jpg)

図4　輝度値を128に設定した画像

次に，輝度値が192以上の画素を1，その他を0に変換する．

IMG = ORG > 192;

imagesc(IMG); colormap(gray); colorbar;

表示結果は図5のようになった．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog3-5.jpg) 

図5　輝度値を192に設定した画像
