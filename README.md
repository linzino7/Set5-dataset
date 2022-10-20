# Set5-dataset
This Rep. privde set5 datasets for super resolution task from [Original Paper](http://people.rennes.inria.fr/Aline.Roumy/results/SR_BMVC12.html).

Image downloaded by [here](https://cv.snu.ac.kr/research/EDSR/benchmark.tar) from [EDSR-PyTorch](https://github.com/sanghyun-son/EDSR-PyTorch).

# Image
## butterfly.png HR
![butterfly HR](https://raw.githubusercontent.com/linzino7/Set5-dataset/main/Set5/HR/butterfly.png)

## butterfly.png LR_bicubic X2
![butterfly LR](https://github.com/linzino7/Set5-dataset/blob/main/Set5/LR_bicubic/X2/butterflyx2.png)


# Super Resolution with different cv resize method
本實驗主要目標為測試不同的 opencv 縮小方法是否會影響深度學習方法在Super Resolution任務上的影響。
圖片使用 [SR論文(2012)](http://people.rennes.inria.fr/Aline.Roumy/results/SR_BMVC12.html) 標準Set5中蝴蝶的圖片。

## PSNR Result 

PSNR 越大越好，通常大於25是人類覺得可以接受的範圍。

| Shrinking Method | EDSR | ESPCN | CUBIC |
|-------|------|-------|-------|
| LINEAR | 30.034 | 29.034 | 26.664 |
| NEAREST| 23.735 | 23.827 | 23.214 |
| CUBIC | 32.330 | 30.049 | 26.984 |

可以看到LINER與CUBIC 還原的效果都不錯。
而NEAREST 效果就很差。

實驗連結: https://colab.research.google.com/drive/1KGAyxSHcN6pIXmaCP_laWoIcE9vM8Cir#scrollTo=e2CS34960WqR

by Zino

2022/10/18 
