Сначала узнаем есть ли документация, или руководство пользователя

# Форма регистрации
## 1) https://vk.com/
<img width="257" alt="image" src="https://user-images.githubusercontent.com/44865195/229306029-128ac76d-8a38-433a-81a6-be20ce74c929.png">

**Замечания**

Посмотреть телефонный план нумерации (например, в википедии)

Смотрим cookies в DevTools в Application - > Cookies 

Смотрим в Local storage, что не сохраняется пароль и номер телефона

Должна ли работать регистрация с отключенными cookies?

**Эквивалентное разбиение и анализ граничных значений**

**Валидные:**

***Поле для ввода номера телефона***

-валидные российские мобильные номера (начинаются с +7, далее 10 цифр)

-валидные зарубежные мобильные номера (количество цифр может быть разным, нужно узнавать)

-стационарный номер (возможно ли?)

***Галочка Сохранить вход***

-выбрана(номер сохраняется). Тест кейс: очистить куки, отправить номер с галочкой Сохранить вход, вернуться на форму (или открыть другую вкладку) и проверить, что номер сохранился и его можно выбрать

-невыбрана(номер не сохраняется). Тест кейс: очистить куки, отправить номер без галочки Сохранить вход, вернуться на форму (или открыть другую вкладку) и проверить, что номер не сохранился 

**Невалидные:**

-невалидные по длине символов (меньше, больше допустимого, пустое поле)

-недопустимые символы

-уже зарегистрированный телефон

-вставить скопиррованный некорректный номер

-регистрация через фейсбук например( вроде был такой способ)

**Действия**

-ввод номера с клавиатуры

-нажать Отправить

-нажать Enter

-вставить скопированный номер

-снять/поставить галочку

-перезагрузить страницу

**Чек-листы**

1) Общий вид формы при загрузке (отображение всех элементов, в поле номера телефона +7, чекбокс выбран, кнопка отправить неактивна)
2) Ввод номера телефона с клавиатуры.
 - В поле ввода номера телефона ввести не цифры. (Если попытаться ввести не цифры, то они игнорируются. Кнопка отправить неактивна.)
 - Ввод валидного номера с клавиатуры: (вводим номера по одному, кнопка Отправить не активна, пока не введем все номера. Далее ввод невозможен.)
 - Первый знак всегда один +.
 - Редактирование номера (Удаление символов (backspace, delete), вставка символов)
 - Появление подсказки Введите номер телефона при удалении всех символов
3) Вставить скопированный номер.
 - Вставить валидный скопированный номер
 - Вставить скопированный номер, содержащий не только цифры
4) Снять/поставить галочку Сохранить вход
5) Нажатие кнопки Отправить (таблица принятия решений?)
 - Сохранение номера при нажатии Отправить с галочкой Сохранить вход
 - Несохранение номера при нажатии Отправить без галочки Сохранить вход
 - Ошибка недопустимый номер при нажатии Отправить (валидация на беке)
 - Переход на страницу Подтвердите вход при успешной валидации номера на беке
 - Отправка смс при успешной валидации номера на беке
6) Нажатие Enter (равносильно нажатию Отправить)
 - когда введен валидный номер телефона (кнопка Отправить активна)
 - когда введен невалидный номер телефона (кнопка Отправить неактивна)
7) Перезагрузить страницу (появляется всплывающее окошко)

**После отправки валдиного номера появляется окошко**

<img width="295" alt="image" src="https://user-images.githubusercontent.com/44865195/229346790-9bc10b0c-ad7f-4edf-9161-3fef8af962f7.png">

