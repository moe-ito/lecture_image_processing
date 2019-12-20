# 課題２レポート

標準画像「pokemon」を原画像とする。この画像は縦736画像，横1026画素によるディジタルカラー画像である。

ORG=imread('https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai2写真/pokemon.png'); % 原画像の入力  
imagesc(ORG); axis image; % 画像の表示

によって，原画像を読み込み，表示した結果を図１に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai2写真/0.png)  
図1 原画像

以下のプログラムにより2諧調画像にしたのち、グレースケールの画像を出力する。
IMG = ORG>128;
imagesc(IMG); colormap(gray); colorbar;  axis image;

2諧調画像にした結果を図２に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai2写真/2.png)  
図2 2諧調画像

以下のプログラムにより4諧調画像にしたのち、グレースケールの画像を出力する。

IMG0 = ORG>64;
IMG1 = ORG>128;
IMG2 = ORG>192;
IMG = IMG0 + IMG1 + IMG2;
imagesc(IMG); colormap(gray); colorbar;  axis image;

とする．4諧調画像にした結果を図３に示す。

![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai2写真/3.png)  
図3 4諧調画像

2諧調ではIMGに1つの値が、4階調ではIMGに3つの値が足されていたことから、8諧調は7つの値を足すことによって生成できると考えた。
また、1つの時は128のみだったが、3つの時は128を半分にした64、128とその半分にした値を足した192になっていたので、会長を足すと元の値をどんどん割って、その割った値をまた足していくと予想した。以下がプログラムである。

IMG0 = ORG>16;
IMG1 = ORG>32;
IMG2 = ORG>64;
IMG3 = ORG>128;
IMG4 = ORG>192;
IMG5 = ORG>224;
IMG6 = ORG>240;
IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6;
imagesc(IMG); colormap(gray); colorbar;  axis image;

8諧調画像にした結果を図３に示す。
![原画像](https://github.com/moe-ito/lecture_image_processing/blob/master/image/kadai2写真/4.png)  
図6 8諧調画像
