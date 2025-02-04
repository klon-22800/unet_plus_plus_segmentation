# Сегментация изображений на основе архитектуры UNet++. 
![UNet](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/graphics/Unet%2B%2B.png)
## Стек:
Tensorflow, scikit-learn, Numpy, opencv, Pillow.
## Датасет
Изображения 256×256 (3 канала) и соответствующие бинарные маски (1 – объект сегментации, 0 – фон). 
![Dataset example](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/graphics/dataset%20example.png)
## Аугментация
Для увеличения выборки: повороты и отражения. Для предобработки: median blur
![Median blur](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/graphics/median%20blur.png)
## Метрики 
Основной метрикой при анализе был коэффициент IoU:
![IoU](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/graphics/IoU.png)
В качестве функции потерь:
![Focal Dice loss](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/graphics/FDL.png)

## Итоговые метрики: 
![Metrics](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/graphics/unet%2B%2B%20250.png)
### Источник:
[Исходное изображение](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/check/big_tlt_test.png)
[Истинная маска](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/check/big_tlt_test_mask.png)
[Предсказанная маска](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/check/big_tlt_check_250.png)
![Map of errors](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/graphics/map_of_errors.png)

![test](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/graphics/Performance%20Metrics%20for%20Models.png)
