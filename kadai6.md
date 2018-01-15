課題6　画像の2値化


まず，画像を白黒の画像に変換する．

ORG=imread('dog.png'); % 原画像の入力

ORG = rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar;

表示結果は図1のようになる．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog6-1.png)

図1　原画像

次に輝度値を128に設定した場合の2値化を行う

IMG = ORG>128; % 128による二値化

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog6-2.png)

図2　128による二値化の画像

最後にディザ法による2値化を行う

IMG = dither(ORG); % ディザ法による二値化

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog6-3.png)

図3　ディザ法による2値化の画像
