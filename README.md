# Сегментация изображений на основе архитектуры UNet++. 
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
![IoU](https://quicklatex.com/cache3/e0/ql_2e94206e0c3ecb2dd8c141394cb728e0_l3.png)
<div style="background-color: white; display: inline-block;">
    <img src="https://quicklatex.com/cache3/e0/ql_2e94206e0c3ecb2dd8c141394cb728e0_l3.png" alt="Описание изображения">
</div>
В качестве функции потерь:
![Focal Dice loss](https://quicklatex.com/cache3/3e/ql_b481f5109391080e547650620dc1dc3e_l3.png)

## Итоговые метрики: 
![Metrics](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/graphics/unet%2B%2B%20250.png)
![Map of errors](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/graphics/map_of_errors.png)
### Источник:
[Исходное изображение](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/check/big_tlt_test.png)
[Истинная маска](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/check/big_tlt_test_mask.png)
[Предсказанная маска](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/check/big_tlt_check_250.png)
![test](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/graphics/Performance%20Metrics%20for%20Models.png)
