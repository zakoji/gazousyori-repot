課題8　ラベリング


まず，画像を白黒の画像に変換する．

ORG=imread('dog.png'); % 原画像の入力

ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

表示結果は図1のようになった．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog8-1.jpg)

図1　原画像

次に閾値128で二値化する．

IMG = ORG > 128; % 閾値128で二値化

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

表示結果は図2のようになった．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog8-2.jpg)

図2　閾値128で二値化した画像

これを，colormap(jet)で調べると，図3のようになる.

IMG = bwlabeln(IMG);

imagesc(IMG); colormap(jet); colorbar; % 画像の表示

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog8-3.jpg)

図3　色調を分けた画像
