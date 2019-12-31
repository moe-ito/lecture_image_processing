# 課題レポート8

標準画像「pokemon」を原画像とする。この画像は縦736画像，横1026画素によるディジタルカラー画像である。

ORG=imread('https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai2写真/pokemon.png'); % 原画像の入力

imagesc(ORG); axis image; % 画像の表示

によって，原画像を読み込み，表示した結果を図１に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai8%E5%86%99%E7%9C%9F/0.png)  
図1 原画像

以下のプログラムにより閾値128で二値化したのち、グレースケールの画像を出力する。

IMG = ORG > 128; 

imagesc(IMG); colormap(gray); colorbar; 

閾値を128にした結果を図２に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai8%E5%86%99%E7%9C%9F/1.png)  
図2 閾値が128の時の画像

以下のプログラムにより二値化された画像の連結成分にラベルをつけたのち、カラースケールの画像を出力する。

IMG = bwlabeln(IMG);

imagesc(IMG); colormap(jet); colorbar;

結果を図３に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai8%E5%86%99%E7%9C%9F/2.png)  
図3 二値化された画像の連結成分にラベリングしたの画像

