# Проектная работа "Веб-ларек"

Стек: HTML, SCSS, TS, Webpack

Структура проекта:
- src/ — исходные файлы проекта
- src/components/ — папка с JS компонентами
- src/components/base/ — папка с базовым кодом

Важные файлы:
- src/pages/index.html — HTML-файл главной страницы
- src/types/index.ts — файл с типами
- src/index.ts — точка входа приложения
- src/styles/styles.scss — корневой файл стилей
- src/utils/constants.ts — файл с константами
- src/utils/utils.ts — файл с утилитами

## Установка и запуск
Для установки и запуска проекта необходимо выполнить команды

```
npm install
npm run start
```

или

```
yarn
yarn start
```
## Сборка

```
npm run build
```

или

```
yarn build
```
документация 

Сайт для разработчиков Web-larek.
используемый стек: webpack, TypeScript, HTML, Css.

установка и запуск:
npm install
npm run start

запуск в dev режиме: npm run dev  (добавлено для удобства работы)

сборка: npm run build

Структура проекта:
src/ — исходные файлы проекта
src/common/ — папка с JS компонентами
src/components/base/ — папка с базовым кодом

архитектура:
web-larek создан по принципу ооп с использованием mvp архитектуры (model - view - presenter)

класс api отвечает за создание fetch запросов (методы get и post), handleResponse для бработки ответа сервера

класс Component отвечает за управление компонентами
методы setText, setImage, toggleClass для изменения состояния элементов
render для заполнения свойств элемента

класс EventEmitter Брокер событий
методы jn off emit - подписка отписка уведомление
onAll ofAll - подписка на все события и сброс всех событий
trigger - Сделать коллбек триггер, генерирующий событие при вызове

класс Model - Базовая модель, чтобы можно было отличить ее от простых объектов с данными
метод emitChanges - Сообщить всем что модель поменялась

бизнес логика

класс AppState - Состояние приложения
методы 
addProductInBasket Добавление продукта в корзину
removeProductFromBasket Удаление продукта из корзины
getBasket Получение продуктов в корзине
setPreview Установка превью продукта
setCatalog Установка каталога
getTotalPrice Общая стоимость корзины
clearBasket Очистка корзины
setOrderField Установка поля заказа
validateOrder Валидация заказа
clearOrder Очистка заказа

представление 

класс Basket Класс для управления корзиной, наследует базовый компонент
методы 
items - Установка списка элементов в корзине
total - Установка общей стоимости в корзине

класс Form Класс для работы с формой, наследует базовый компонент
основные методы 
valid - Установка валидности формы
errors - Установка ошибок формы
render - Метод рендеринга состояния формы

класс Modal Класс модального окна, наследуется от базового компонента
основные методы
open - Метод для закрытия модального окна.
close - Метод для закрытия модального окна.
render - од для рендеринга модального окна с данными.

класс Order Класс заказа, наследуется от Form
основные методы
phone - номер телефона заказчика
email - электронная почта заказчика
address - физический адрес заказчика
payment - выбранный способ оплаты заказчиком

класс Page наследуктся от базового компонента
основные методы
counter - Сеттер для счетчика
catalog - Сеттер для каталога
locked - Сеттер для блокировки страницы

класс Product наследуется от базового компонента - шаблон пролукта
основные методы

класс Success наследуется от базового компонента
отоброжение результата заказа

