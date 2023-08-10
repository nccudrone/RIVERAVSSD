# RIVERAVSSD：河流俯視角空拍影像語意切割資料集 (River Aerial View Semantic Segmentation Dataset)

## Overview
此資料集為台灣河流(二仁溪、曾文溪與景美溪)俯視角空拍語意切割資料集。  

## Part 1
由上暘飛行股份有限公司與政大無人機團隊合作 使用 符合資安之改裝DJI無人機 進行錄製收集，並由政大無人機團隊進行資料採樣與標註。  
收集範圍經緯度為  
* 二仁溪：22.907159 ~ 22.894351, 120.242812 ~ 120.304009
* 曾文溪：23.096211 ~ 23.133573, 120.200212 ~ 120.241245

錄製角度可以分為俯視(攝影機向下90度)與前視(攝影機向下45度)  

## Part 2
由政大無人機團隊 使用 Parrot Bebop2、Anafi以及 符合資安之改裝DJI無人機 進行錄製收集，並進行資料採樣與標註。  
收集範圍經緯度為  
* 景美溪：24.978948 ~ 24.987675, 121.561576 ~ 121.572851

錄製角度為俯視(攝影機向下90度)

## Description
img/ 為原始圖像，檔案類型為.jpg。  
label/ 為遮罩圖與標註檔案，檔案類型為.png與.json。  
* 遮罩圖僅標註河流部分。  
* 遮罩圖為二進位png檔案，像素值0表示非河流，像素值1表示河流。
* 標註檔案使用labelme進行河流標註，以描邊方式將河流部分框住。
* 標註檔案內記載資訊如下：  
  * shapes：描邊資料結構  
  * shapes/label：描邊標註類別，此處統一為 "river"
  * shapes/points：描邊多邊形座標
  * shapes/shape_type：描邊種類，統一為 "polygon"
  * imagePath：原始圖像檔名
  * imageHeight：原始圖像高
  * imageWidth：原始圖像寬

下面為部分預覽影像，左邊為原始圖像，右邊為遮罩圖(像素值0以紫色表示，像素值1以黃色表示)：  
<img src="https://github.com/nccudrone/RIVERAVSSD/blob/main/image/riverlabel1.png" width="856" height="240"/>  
<img src="https://github.com/nccudrone/RIVERAVSSD/blob/main/image/riverlabel2.png" width="856" height="240"/><br/>  
## Notes  
* 此資料集為河流俯視角空拍語意切割資料集的一部分，做為免費開放使用
* 此資料集用於學術研究
* 此資料集可以應用如[albumentations](https://github.com/albumentations-team/albumentations "link")進行影像擴增來加強訓練
* 此資料集包含原始圖像、遮罩與標註檔案，原始影像檔案請參考：[repo](https://github.com/nccudrone/RIVERAVVD "link")
## Download Link
Part 1：[img/](http://140.119.164.183:5000/sharing/MjdclAULq)、[label/](http://140.119.164.183:5000/sharing/qepH2xqH1)  
Part 2：[img/](http://140.119.164.183:5000/sharing/RufWX9drA)、[label/](http://140.119.164.183:5000/sharing/MLv49w54t)  
## Licence
請參考 [LICENSE](https://github.com/nccudrone/RIVERAVSSD/blob/main/LICENSE "link")
