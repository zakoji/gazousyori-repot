課題10　



まず，画像を白黒の画像に変換する．

ORG=imread('dog.png'); % 原画像の入力

ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換

imagesc(ORG); colormap(gray); colorbar; % 画像の表示

表示結果は図1のようになった．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog10-1.jpg)

図1　原画像

次にプレウィット法エッジ抽出を行う．

IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）

imagesc(IMG); colormap('gray'); colorbar;% 画像表示

表示結果は図2のようになった．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog10-2.jpg)

図2　プレウィット法によるエッジ抽出の結果

次にソベル法によるエッジ抽出を行う

IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）

imagesc(IMG); colormap('gray'); colorbar;% 画像表示

表示結果は図3のようになった．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog10-3.jpg)

図3　ソベル法によるエッジ抽出の結果

次にキャニー法によるエッジ抽出を行う

IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）

imagesc(IMG); colormap('gray'); colorbar;% 画像表示

表示結果は図4のようになった．

![](https://github.com/zakoji/gazousyori-repot/blob/master/image/dog10-4.jpg)

図4　キャニー法によるエッジ抽出の結果
