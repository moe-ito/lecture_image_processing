# 課題レポート9

標準画像「pokemon」を原画像とする。この画像は縦736画像，横1026画素によるディジタルカラー画像である。

ORG=imread('https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai2写真/pokemon.png'); % 原画像の入力  

imagesc(ORG); axis image; % 画像の表示

によって，原画像を読み込み，表示した結果を図１に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai9%E5%86%99%E7%9C%9F/0.png)  
図1 原画像

以下のプログラムにより原画像にノイズを添加したのち、グレースケールの画像を出力する。

ORG = imnoise(ORG,'salt & pepper',0.02); 

imagesc(ORG); colormap(gray); colorbar; 

原画像にノイズを添加した結果を図2に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai9%E5%86%99%E7%9C%9F/1.png)  
図2 原画像にノイズを添加した画像

以下のプログラムにより平滑化フィルタで雑音除去したのち、グレースケールの画像を出力する。

IMG = filter2(fspecial('average',3),ORG);

imagesc(IMG); colormap(gray); colorbar; 

平滑化フィルタで雑音除去した結果を図3に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai9%E5%86%99%E7%9C%9F/2.png)  
図3 平滑化フィルタで雑音除去した時の画像

以下のプログラムによりメディアンフィルタで雑音除去したのち、グレースケールの画像を出力する。

IMG = medfilt2(ORG,[3 3]);

imagesc(IMG); colormap(gray); colorbar; 

メディアンフィルタで雑音除去した結果を図4に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai9%E5%86%99%E7%9C%9F/3.png)  
図4 メディアンフィルタで雑音除去した時の画像

以下のプログラムによりフィルタを設計し適用したのち、グレースケールの画像を出力する。

f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計

IMG = filter2(f,IMG,'same'); % フィルタの適用

imagesc(IMG); colormap(gray); colorbar; % 画像の表示

設計したフィルタで雑音除去した結果を図5に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai9%E5%86%99%E7%9C%9F/4.png)  
図5 設計したフィルタで雑音除去した時の画像
