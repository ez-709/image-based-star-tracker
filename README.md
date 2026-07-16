# roll-angle-estimation - Project Description

An algorithm has been developed to estimate the roll angle of a spacecraft using nadir-pointing images of the Earth. The method involves:

1. Threshold-based binarization of the image.
2. Detection of the Earth's limb as the sequence of highest white pixels in each column.
3. Least-squares fitting of a circular arc to the limb.
4. Computation of the roll angle from the orientation of the fitted circle's center.

The algorithm has been validated on daylight Earth images.

Current limitations:
- Failure on night-side imagery.
- Sensitivity to bright artifacts such as the Sun or Moon.
- Extension to pitch estimation requires prior knowledge of camera intrinsic parameters.

<img width="1880" height="676" alt="изображение" src="https://github.com/user-attachments/assets/8ba9093b-c18e-45a3-88ba-db2e628e90a2" />

## Installation & Launch

The algorithm is started by running `main.py`:

```bash
python main.py
```

All input images used by the algorithm are stored in the `data` folder.

---

# roll-angle-estimation - Описание проекта

Разработан алгоритм оценки угла крена космического аппарата по надирным изображениям Земли. Метод включает следующие этапы:

1. Пороговая бинаризация изображения.
2. Обнаружение лимба Земли как последовательности самых верхних белых пикселей в каждом столбце.
3. Аппроксимация дуги окружности методом наименьших квадратов по точкам лимба.
4. Вычисление угла крена по ориентации центра аппроксимированной окружности.

Алгоритм проверен на дневных изображениях Земли.

Текущие ограничения:
- Не работает на ночных изображениях.
- Чувствителен к ярким артефактам, таким как Солнце или Луна.
- Расширение до оценки угла тангажа требует знания внутренних параметров камеры.

<img width="1880" height="676" alt="изображение" src="https://github.com/user-attachments/assets/8ba9093b-c18e-45a3-88ba-db2e628e90a2" />

## Установка и запуск

Запуск алгоритма производится из файла `main.py`:

```bash
python main.py
```

Все входные изображения, используемые алгоритмом, хранятся в папке `data`.
