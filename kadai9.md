課題9　メディアンフィルタと先鋭化



まず，画像を白黒の画像に変換する．

ORG=imread('dog.png'); % 原画像の入力

ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

表示結果は図1のようになった．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog9-1.png)

図1　原画像

次にこの画像にノイズを乗せる

ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

表示結果は図2のようになった．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog9-2.png)

図2　ノイズを添付した画像

次に平滑化フィルタで雑音除去を使い，ノイズを減らす

IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

表示結果は図3のようになった.

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog9-3.png)

図3　平滑化フィルタで雑音除去を行った画像

また，メディアンフィルタを利用してノイズを減らす

IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

表示結果は図4のようになった.

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog9-4.png)

図4　メディアンフィルタで雑音除去を行った画像

自分でフィルタを設計すると図5のようになった．

f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計

IMG = filter2(f,IMG,'same'); % フィルタの適用

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog9-5.png)

図5　フィルタを設計した画像
