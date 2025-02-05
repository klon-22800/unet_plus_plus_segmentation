# Сегментация изображений на основе архитектуры UNet++. 
## Стек:
**Tensorflow**, **Keras**, **scikit-learn**, **Numpy**, **SciPy**, **opencv**.

![Tensorflow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=TensorFlow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-FF0000?style=for-the-badge&logo=keras&logoColor=white)
![Sci-kit learn](https://img.shields.io/badge/scikit_learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)

![NumPy](	https://img.shields.io/badge/Numpy-777BB4?style=for-the-badge&logo=numpy&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-654FF0?style=for-the-badge&logo=SciPy&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-27338e?style=for-the-badge&logo=OpenCV&logoColor=white)

## Описание: 
Проект представляет собой реализацию нейронной сети для сегментации зданий и деревьев на геоснимках. Модель основана на архитектуре UNet++, которая является улучшенной версией классической UNet и обеспечивает более точную сегментацию за счёт вложенных и плотных skip-connections.

### Pipeline: 
1) Сбор датасета и их ручная разметка
2) Аугментирование и предобработка
3) Построение и обучение нескольких моделей на разных гиперпараметрах и архитектурах
4) Анализ метрик и выходных данных через статистические тесты ([Критерий Колмогорова-Смирнова](https://ru.wikipedia.org/wiki/%D0%9A%D1%80%D0%B8%D1%82%D0%B5%D1%80%D0%B8%D0%B9_%D1%81%D0%BE%D0%B3%D0%BB%D0%B0%D1%81%D0%B8%D1%8F_%D0%9A%D0%BE%D0%BB%D0%BC%D0%BE%D0%B3%D0%BE%D1%80%D0%BE%D0%B2%D0%B0), [Критерий хи-квадрат](https://ru.wikipedia.org/wiki/%D0%9A%D1%80%D0%B8%D1%82%D0%B5%D1%80%D0%B8%D0%B9_%D1%85%D0%B8-%D0%BA%D0%B2%D0%B0%D0%B4%D1%80%D0%B0%D1%82))
5) Построение графиков и визуализации результатов 

## Датасет
Изображения 256×256 (3 канала) и соответствующие бинарные маски (1 – объект сегментации, 0 – фон). 
![Dataset example](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/graphics/dataset%20example.png)

## Аугментация
Для увеличения выборки: повороты и отражения. Для предобработки: median blur
![Median blur](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/graphics/median%20blur.png)

## Архитектура 
За основу были взяты архитектуры для сегментации UNet и ее модификация UNet++. 

![UNet](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/graphics/Unet%2B%2B.png)

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

## Пример работы: 
![Results](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/graphics/result.png)
[Итоговое изображение](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/check/big_tlt_check_100_t_o.png)

![test](https://github.com/klon-22800/unet_plus_plus_segmentation/blob/main/graphics/Performance%20Metrics%20for%20Models.png)
