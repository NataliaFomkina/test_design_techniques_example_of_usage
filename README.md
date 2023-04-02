Сначала узнаем есть ли документация, или руководство пользователя

# Форма регистрации
## 1) https://vk.com/
<img width="257" alt="image" src="https://user-images.githubusercontent.com/44865195/229306029-128ac76d-8a38-433a-81a6-be20ce74c929.png">

### Эквивалентное разбиение

**Замечания**
Посмотреть телефонный план нумерации (в википедии)

Смотрим в DevTools в консоли обработку ошибок 

Смотрим cookies (номер телефона может браться из cookies) - в DevTools в Application - > Cookies / или C:\Users\Пользователь\AppData\Local\Google\Chrome\User Data\Default\

Смотрим в Local storage, что не сохраняется пароль и номер телефона

Должна ли работать регистрация с отключенными cookies?

**Валидные:**

-валидные российские мобильные номера (начинаются с +7, далее 10 цифр)

-валидные зарубежные мобильные номера (количество цифр может быть разным, нужно узнавать)

-стационарный номер (возможно ли?)

-регистрация через фейсбук например( вроде был такой способ)

-нажатие Enter

-вставить скопированный корректный номер

-очистить куки, отправить номер с галочкой Сохранить вход, вернуться на форму (или открыть другую вкладку) и проверить, что номер сохранился и его можно выбрать

-очистить куки, отправить номер без галочки Сохранить вход, вернуться на форму (или открыть другую вкладку) и проверить, что номер не сохранился 

**Невалидные:**

-невалидные по длине символов (меньше, больше допустимого, пустое поле)

-недопустимые символы

-уже зарегистрированный телефон

-вставить скопиррованный некорректный номер
