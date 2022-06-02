# STAS Segmentation

肺腺癌病理切片影像之腫瘤氣道擴散[偵測競賽](https://tbrain.trendmicro.com.tw/Competitions/Details/22) II：運用影像分割作法於切割STAS輪廓

----

## How to use
1. 在本地端執行Preprocessing.py將官網下載的ground truth json檔轉成png黑白圖片

2. 在Google雲端以下列格式建立資料夾，並將括號內的資料分別放入資料夾
```
- stas
    -- train
        --- image (training dataset jpg檔)
        --- label (ground truth png檔)
    -- test (Public Test jpg檔)
    -- Private_Image (Private test jpg檔)
    -- answer
    -- model
    -- post_process
```

3. 將segmentation_unet.ipynb上傳至Google Colab執行

4. 所有答案圖片(png黑白圖片檔)將存在answer資料夾，訓練完的模型將放在model資料夾，後處理的圖片將放在post_processy資料夾

## Note
此Repo包含被訓練好的模型檔案(unet_resnet152.pth)，檔案有夠大，建議不要直接git clone