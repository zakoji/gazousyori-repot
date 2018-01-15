課題4　画像のヒストグラム



まず，画像を白黒の画像に変換する．

ORG=imread('dog.png'); % 原画像の入力

ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar;

表示された画像は図1のようになった．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog4-1.jpg)

図1　原画像

次にヒストグラムを表示する

imhist(ORG);

結果は図2のようになった．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog4-2.jpg)

図2　ヒストグラム
