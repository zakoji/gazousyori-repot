
課題1 標本化間隔と空間解像度


ORG=imread('dog.png'); % 原画像の入力

imagesc(ORG); axis image; % 画像の表示

によって表示された原画像は図1のようになった．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog.jpg)

図1　原画像

原画像を1/2にサンプリングするには，画像を1/2に縮小した後，2倍に拡大する．拡大する際には，単純補間するためにboxオプションを利用する．

IMG = imresize(ORG,0.5); % 画像の縮小

IMG2 = imresize(IMG,2,'box'); % 画像の拡大

imagesc(IMG2); axis image; % 画像の表示

1/2サンプリングの結果を図２に示す．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog1-1.png)

図2 1/2サンプリング

同様に，1/4サンプリングをするには，1/2サンプリングした画像を1/2に縮小した後，2倍に拡大することで可能である．

IMG = imresize(IMG,0.5); % 画像の縮小

IMG2 = imresize(IMG,4,'box'); % 画像の拡大

imagesc(IMG2); axis image; % 画像の表示

1/4サンプリングの結果を図２に示す．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog1-2.png)

図3 1/4サンプリング

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog1-3.png)

図4 1/8サンプリング

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog1-4.png)

図5 1/16サンプリング

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog1-5.png)

図6 1/32サンプリング
