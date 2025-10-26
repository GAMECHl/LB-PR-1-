# LB-PR-1-Hurzidze-Anton
## Хурцидзе Антон IПЗ 4.02 Лабораторна-Практична робота № 1

## Тема: Програмні моделі систем координат
## Мета: Спроєктувати та реалізувати імутабельні програмні моделі для представлення точок у 2D та 3D системах координат. Реалізувати механізми перетворення між декартовою, полярною та сферичною системами координат з використанням статичних фабричних методів. Навчитись обчислювати відстані між точками, використовуючи різні математичні підходи. Провести аналіз продуктивності обчислень для різних представлень даних.


## 1. Проєктування та реалізація імутабельних моделей даних

#### Створіємо наступні моделі даних: CartesianPoint2D(x, y), PolarPoint(radius, angle), CartesianPoint3D(x, y, z) та SphericalPoint(radius, azimuth, polarAngle):

![1](https://github.com/GAMECHl/LB-PR-1-/blob/main/1.png)
#### Рис. 1 - Склонований проект в WebStorm

#### Наступним чином використовуюємо команду npm install а потім npm install --legacy-peer-deps для встановлення всіх залежностей:
![2](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/2.png)
#### Рис. 2 - Встановлення залежностей

#### Запускаємо проект командою npm run dev:
![3](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/3.png)
#### Рис. 3 - Запуск проекту

#### Переходимо на сторінку http://localhost:5173/ та бачимо наступне повідомлення:
![4](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/4.png)
#### Рис. 4 - Запуск проекту

## 1. Сторінка колекції екземплярів сутності (/posts)

#### Перейдемо в дикректорію src/components/ui та створимо там директорії Modal та PostCard. В цих директоріях створюємо файли Modal.tsx, index.ts та PostCard.tsx, index.ts відповідно:
![5](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/5.png)
#### Рис. 5 - Створені директорії та файли

#### Далі вписуємо в ці файли наступні змісти:
![6](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/6.png)
![6.1](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/6.1.png)
#### Рис. 6 - Файл PostCard.tsx
![7](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/7.png)
#### Рис. 7 - Файл index.ts
![8](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/8.png)
#### Рис. 8 - Файл Modal.tsx
![9](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/9.png)
#### Рис. 9 - Файл index.ts

#### Потім створюємо в директорії pages три файли відображення сторінок: Posts.tsx, PostCreate.tsx та PostDetail.tsx:
![10](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/10.png)
![10.1](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/10.1.png)
![10.2](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/10.2.png)
#### Рис. 10 - Файл PostCard.tsx
![11](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/11.png)
![11.1](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/11.1.png)
![11.2](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/11.2.png)
![11.3](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/11.3.png)
#### Рис. 11 - Файл PostCreate.tsx
![12](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/12.png)
#### Рис. 12 - Файл PostDetail.tsx

#### Для завантаження публікацій та обновлення сторінок створюємо директорію src/posts та файл index.ts в ній:
![13](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/13.png)
#### Рис. 13 - Створення директорії та файла
![14](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/14.png)
![14.1](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/14.1.png)
![14.2](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/14.2.png)
#### Рис. 14 - Файл index.ts

#### Для єксортування типів даних створюємо файл Post.ts в директорії src/types:
![15](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/15.png)
#### Рис. 15 - Файл Post.ts

#### Для налаштування маршутів створюємо директорію routes/posts та файл index.ts з наступним змістом:
![16](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/16.png)
#### Рис. 16 - Файл index.ts 

#### Для налаштування маршутів до роутера редактуємо файл routeTree.gen.ts наступним чином:
![17](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/17.png)
![17.1](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/17.1.png)
![17.2](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/17.2.png)
#### Рис. 17 - Файл routeTree.gen.ts

## 2. Сторінка окремого екземпляра сутності (/posts/:id або /posts/new)
#### Для створення окремий сторінок екземплярів сутоностей требя створити в директорії src/routes/posts файли $id.ts та new.ts(всі колишні файли уже налаштовані для працювання окремих сторінок сутностей):
![18](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/19.png)
#### Рис. 18 - Файл $id.ts
![19](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/19.png)
#### Рис. 19 - Файл new.ts

## 3. Запуск сервера
#### Запускаемо сервер командою npm run dev та переходимо на сторінку http://192.168.3.3:5173/posts(чи localhost):
![20](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/20.png)
#### Рис. 20 - Сторінка http://192.168.3.3:5173/posts

#### Переглянемо детальну інформацію про публікацію:
![21](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/21.png)
#### Рис. 21 - Детальна інформація сутності

#### Спробуємо редагувати інформацію публікації:
![22](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/22.png)
![22.1](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/22.1.png)
![22.2](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/22.2.png)
#### Рис. 22 - Редагування сутності

#### Спробуємо додати нову публікацію:
![23](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/23.png)
![23.1](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/23.1.png)
#### Рис. 23 - Додавання сутності

#### Спробуємо видалити публікацію:
![24](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/24.png)
![24.1](https://github.com/GAMECHl/PR-LB-6-Hurzidze-Anton/blob/main/24.1.png)
#### Рис. 24 - Видалення сутності

## Висновкок: У ході виконання лабораторної роботи я навчився створювати користувацький інтерфейс для взаємодії з реалізованим RESTful API, що надає можливість перегляду, створення, редагування та видалення екземплярів певної сутності. Розробка ведеться на базі React з використанням TanStack Router для реалізації маршрутизації.
