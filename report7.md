# 課題レポート7

標準画像「pokemon」を原画像とする。この画像は縦736画像，横1026画素によるディジタルカラー画像である。

ORG=imread('https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai2写真/pokemon.png'); % 原画像の入力  
imagesc(ORG); axis image; % 画像の表示

によって，原画像を読み込み，表示した結果を図１に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai7%E5%86%99%E7%9C%9F/0.png)  
図1 原画像

以下のプログラムにより濃度ヒストグラムを生成し、表示をする。

imhist(ORG);

濃度ヒストグラムを生成した結果を図２に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai7%E5%86%99%E7%9C%9F/1.png)  
図2 濃度ヒストグラムの画像

以下のプログラムにより画素のダイナミックレンジを０から２５５にし、グレースケールの画像を出力する。

ORG = double(ORG);

mn = min(ORG(:)); % 濃度値の最小値を算出

mx = max(ORG(:)); % 濃度値の最大値を算出

ORG = (ORG-mn)/(mx-mn)*255;

imagesc(ORG); colormap(gray); colorbar;

ダイナミックレンジの拡大をした結果を図３に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai7%E5%86%99%E7%9C%9F/2.png)  
図3 ダイナミックレンジの拡大時の画像

以下のプログラムによりダイナミックレンジの拡大をした濃度ヒストグラムの画像を出力する。

ORG = uint8(ORG); 

imhist(ORG);

ダイナミックレンジの拡大時の濃度ヒストグラムの生成した結果を図4に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai7%E5%86%99%E7%9C%9F/3.png)  
図4 ダイナミックレンジの拡大時の濃度ヒストグラムの画像
