# 課題レポート10

標準画像「pokemon」を原画像とする。この画像は縦736画像，横1026画素によるディジタルカラー画像である。

ORG=imread('https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai2写真/pokemon.png'); % 原画像の入力 

imagesc(ORG); axis image; % 画像の表示

によって，原画像を読み込み，表示した結果を図１に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai10%E5%86%99%E7%9C%9F/0.png)  
図1 原画像

以下のプログラムによりプレウィット法によるエッジ抽出したのち、グレースケールの画像を出力する。

IMG = edge(ORG,'prewitt'); 

imagesc(IMG); colormap('gray'); colorbar;

プレウィット法によるエッジ抽出した結果を図２に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai10%E5%86%99%E7%9C%9F/1.png)  
図2 プレウィット法によるエッジ抽出の画像

以下のプログラムによりソベル法によるエッジ抽出したのち、グレースケールの画像を出力する。

IMG = edge(ORG,'sobel'); 

imagesc(IMG); colormap('gray'); colorbar;

ソベル法によるエッジ抽出した結果を図３に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai10%E5%86%99%E7%9C%9F/2.png)  
図3 ソベル法によるエッジ抽出の画像

以下のプログラムによりキャニー法によるエッジ抽出したのち、グレースケールの画像を出力する。

IMG = edge(ORG,'canny'); 

imagesc(IMG); colormap('gray'); colorbar;

キャニー法によるエッジ抽出した結果を図4に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai10%E5%86%99%E7%9C%9F/3.png)  
図4 キャニー法によるエッジ抽出の画像
