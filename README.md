# LB-PR-1-Hurzidze-Anton
## Хурцидзе Антон IПЗ 4.02 Лабораторна-Практична робота № 1

## Тема: Програмні моделі систем координат
## Мета: Спроєктувати та реалізувати імутабельні програмні моделі для представлення точок у 2D та 3D системах координат. Реалізувати механізми перетворення між декартовою, полярною та сферичною системами координат з використанням статичних фабричних методів. Навчитись обчислювати відстані між точками, використовуючи різні математичні підходи. Провести аналіз продуктивності обчислень для різних представлень даних.


## 1. Проєктування та реалізація імутабельних моделей даних

#### 1) Створіємо наступні моделі даних: CartesianPoint2D(x, y), PolarPoint(radius, angle), CartesianPoint3D(x, y, z) та SphericalPoint(radius, azimuth, polarAngle):

![1](https://github.com/GAMECHl/LB-PR-1-/blob/main/1.png)
#### Рис. 1 - Модель CartesianPoint2D

![2](https://github.com/GAMECHl/LB-PR-1-/blob/main/2.png)
#### Рис. 2 - Модель PolarPoint

![3](https://github.com/GAMECHl/LB-PR-1-/blob/main/3.png)
#### Рис. 3 - Модель CartesianPoint3D

![4](https://github.com/GAMECHl/LB-PR-1-/blob/main/4.png)
#### Рис. 4 - Модель SphericalPoint

#### 2) Реалізуємо статичні фабричні методи для перетворень між системами, а саме: CartesianPoint2D fromPolar(PolarPoint p), PolarPoint fromCartesian(CartesianPoint2D p) для 2Д та CartesianPoint3D.fromSpherical(SphericalPoint p), SphericalPoint.fromCartesian(CartesianPoint3D p) для 3Д:
![5](https://github.com/GAMECHl/LB-PR-1-/blob/main/5.png)
#### Рис. 5 - Методи fromCartesian та fromPolar

![6](https://github.com/GAMECHl/LB-PR-1-/blob/main/6.png)
#### Рис. 6 - Методи fromSpherical та fromCartesian(3д)

#### 3) Створюємо кілька тестових точок, та робимо пряме та зворотне перетворення і переконуємось, що початкові координати збігаються з кінцевими:
![7](https://github.com/GAMECHl/LB-PR-1-/blob/main/7.png)
#### Рис. 7 - Перевірка перетворень в коді

![8](https://github.com/GAMECHl/LB-PR-1-/blob/main/8.png)
#### Рис. 8 - Результат перевірки

## 2. Реалізація обчислення відстаней

#### На основі реалізованих моделей даних, створюємо функції для обчислення відстаней, а саме функції distanceCartesian2D, distancePolar для 2Д та distanceCartesian3D, distanceSphericalChord, distanceSphericalArc для 3Д:
![9](https://github.com/GAMECHl/LB-PR-1-/blob/main/9.png)
#### Рис. 9 - Функції distanceCartesian2D та distancePolar

![10](https://github.com/GAMECHl/LB-PR-1-/blob/main/10.png)
![11](https://github.com/GAMECHl/LB-PR-1-/blob/main/11.png)
#### Рис. 10 - Функції distanceCartesian3D, distanceSphericalArc та distanceSphericalChord

![11.1](https://github.com/GAMECHl/LB-PR-1-/blob/main/11.1.png)
#### Рис. 11 - Результати обчислень

## 3. Аналіз продуктивності (Бенчмаркінг)

#### 1) Підготовка даних: згенеруємо один масив з 100,000 пар випадкових точок у полярній системі координат (PolarPoint) та створюємо другий масив, попередньо сконвертувавши кожну точку з першого масиву у декартову систему:

![12](https://github.com/GAMECHl/LB-PR-1-/blob/main/12.png)
#### Рис. 12 - Генерування точок в массив та конвертування в інший

#### 2) Вимірювання чистого часу обчислень: Підхід А (Полярні координати): Замірюємо час обчислення відстаней для всього масиву пар PolarPoint, використовуючи формулу на основі теореми косинусів. Підхід Б (Декартові координати): Замірюємо час обчислення відстаней для всього масиву пар CartesianPoint2D, використовуючи стандартну евклідову формулу:

![14](https://github.com/GAMECHl/LB-PR-1-/blob/main/14.png)
#### Рис. 14 - Використання підхіду А та підхіду Б

## Висновкок: У ході виконання лабораторної роботи я навчився створювати користувацький інтерфейс для взаємодії з реалізованим RESTful API, що надає можливість перегляду, створення, редагування та видалення екземплярів певної сутності. Розробка ведеться на базі React з використанням TanStack Router для реалізації маршрутизації.
