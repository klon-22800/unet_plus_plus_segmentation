# Сегментация изображений на основе архитектуры UNet++. 
## Стек:
**Tensorflow**, **Keras**, **scikit-learn**, **Numpy**, **SciPy**, **opencv**.

![Tensorflow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=TensorFlow&logoColor=white)
![Keras](![Tensorflow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=TensorFlow&logoColor=white))
![Sci-kit learn](https://img.shields.io/badge/scikit_learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)

![NumPy](	https://img.shields.io/badge/Numpy-777BB4?style=for-the-badge&logo=numpy&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-654FF0?style=for-the-badge&logo=SciPy&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-27338e?style=for-the-badge&logo=OpenCV&logoColor=white)

## Описание: 
Проект представляет собой реализацию нейронной сети для сегментации зданий и деревьев на геоснимках. Модель основана на архитектуре UNet++, которая является улучшенной версией классической UNet и обеспечивает более точную сегментацию за счёт вложенных и плотных skip-connections.
![UNet](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/graphics/Unet%2B%2B.png)

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
