# 課題4レポート

標準画像「pokemon」を原画像とする。この画像は縦736画像，横1026画素によるディジタルカラー画像である。

ORG=imread('https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai2写真/pokemon.png'); % 原画像の入力  
imagesc(ORG); axis image; % 画像の表示

によって，原画像を読み込み，表示した結果を図１に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai4%E5%86%99%E7%9C%9F/0.png)  
図1 原画像

以下のプログラムにより原画像の画素の濃度ヒストグラムを出力する。

imhist(ORG); 

濃度ヒストグラムを生成した結果を図２に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai4%E5%86%99%E7%9C%9F/1.png)  
図2 原画像の濃度ヒストグラム

