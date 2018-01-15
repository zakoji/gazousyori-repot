課題２ ２階調，４階調，８階調の画像を生成せよ．  

グレースケールで2階調の画像を生成する．MATLABに画像を読み込み，以下の処理を行った．

ORG=imread('dog.png'); % 原画像の入力
ORG = rgb2gray(ORG); colormap(gray); colorbar;

imagesc(ORG); axis image; % 画像の表示   その結果を図１に示す．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog2-1.jpg)  

図１ グレースケール

  続いて，２階調画像を生成する．以下の処理を行った．

IMG = ORG>128;   imagesc(IMG); colormap(gray); colorbar; axis image;

この処理の結果を図２に示す．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog2-2.jpg)

図２  ２階調画像

４階調画像を生成する．以下の処理を行った．

IMG0 = ORG>64;
IMG1 = ORG>128;
IMG2 = ORG>192;
IMG = IMG0 + IMG1 + IMG2;

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog2-3.jpg)

図３  ４階調画像

8階調画像を生成する．以下の処理を行った．   IMG0 = ORG>32;
IMG1 = ORG>64;
IMG2 = ORG>128;
IMG3 = ORG>160;
IMG4 = ORG>192;
IMG5 = ORG>224;
IMG6 = ORG>256;
IMG = IMG0 + IMG1 + IMG2 +IMG3 +IMG4 +IMG5 +IMG6;

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog2-4.jpg)

図４ 8階調画像
