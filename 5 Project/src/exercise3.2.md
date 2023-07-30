#  Выбор полиса

## 1. Кнопки `button`:

(//button[@name='type'])[1] - "Квартира"

(//button[@name='type'])[2] - "Дом"

//button[contains(@class,'mat-focus-indicator mat-icon-button')] - кнопка для отрытия датапикера "Срок действия страхования"

- Если кнопка "Квартира" активна:

(//button[@type='button'])[4] - "Да" (Сдается в аренду)

(//button[@type='button'])[5] - "Нет" (Сдается в аренду)

(//button[@type='button'])[6] - "Да" (Расположена на первом или последнем этаже)

(//button[@type='button'])[7] - "Нет" (Расположена на первом или последнем этаже)

(//button[@type='button'])[8] - "Да" (Установлена охранная сигнализация)

(//button[@type='button'])[9] - "Нет" (Установлена охранная сигнализация)

- Если кнопка "Дом" активна:

(//button[@type='button'])[4] - "Да" (Сдается в аренду)

(//button[@type='button'])[5] - "Нет" (Сдается в аренду)

(//button[@type='button'])[6] - "Да" (Установлена охранная сигнализация)

(//button[@type='button'])[7] - "Нет" (Установлена охранная сигнализация)

(//button[@type='button'])[8] - "Да" (Материал несущих стен)

(//button[@type='button'])[9] - "Нет" (Материал несущих стен)

//div[@class='reg-button']//button[1] - "Применить"

//button[contains(@class,'mat-focus-indicator mat-stroked-button')] - "Оформить"

## 2. Поля ввода текста:

(//input[contains(@class,'mat-input-element mat-form-field-autofill-control')])[1] - "Регион проживания"

(//input[contains(@class,'mat-input-element mat-form-field-autofill-control')])[3] - "Сумма"

(//input[contains(@class,'mat-input-element mat-form-field-autofill-control')])[4] - "Промокод"

(//input[contains(@class,'mat-input-element mat-form-field-autofill-control')])[2] -  поле ввода "Дата начала"

## 3. Datepicker:

//mat-calendar[@id="mat-datepicker-0"] - "Срок действия страхования" (календарь)

(//div[@class='mat-form-field-wrapper ng-tns-c61-1']//div)[1] - датапикер целиком (инпут + кнопка)

## 4. Логотип "СБЕР СТРАХОВАНИЕ":

//div[@class="sber-logo"] - Логотип "СБЕР СТРАХОВАНИЕ"

## 5. Слайдер выбор суммы:

//mat-slider[@role="slider"] - слайдер

## 6. Заголовок "Что будет застраховано?":

//h4[@class='block-header'][1]

## 7. Текстовые блоки:

//div[text()=' Мебель, техника и ваши вещи '] -  "Мебель, техника и ваши вещи"

//div[text()='Падение летательных аппаратов и их частей'] - "Падение летательных аппаратов и их частей"

## 8. Колонки под заголовком "Страховая защита включенная в программу":

(//div[@class='sbi-form__col-2'])[2] - Первая колонка

(//div[@class='sbi-form__col-2'])[3] - Вторая колонка

***

# Оформление

## 1. Кнопки `button`:

(//button[@type='button'])[1] - "Заполнить по Сбер ID "

(//button[@type='button'])[2] - "Дата рождения"

(//button[@name='mat-button-toggle-group-84'])[1] - "Мужской"

(//button[@name='mat-button-toggle-group-84'])[2] - "Женский"

(//button[@type='button'])[5] - кнопка для открытия датапикера "Дата выдачи"

//div[@class='form-actions']//button[1] - "Вернуться"

//button[@color='accent'] - "Оформить"

## 2. Поля ввода текста:

(//input[contains(@class,'mat-input-element mat-form-field-autofill-control')])[1] - "Фамилия"

(//input[contains(@class,'mat-input-element mat-form-field-autofill-control')])[2] - "Имя"

(//input[contains(@class,'mat-input-element mat-form-field-autofill-control')])[3] - "Отчество"

(//input[contains(@class,'mat-input-element mat-form-field-autofill-control')])[4] - "Дата рождения"

//input[@data-placeholder='Серия'] - "Серия"

//input[@data-placeholder='Номер'] - "Номер"

//input[@data-mat-calendar='mat-datepicker-2'] - "Дата выдачи"

//textarea[@id="mat-input-11"] - "Кем выдан"

//input[@id="mat-input-12"] - "Код подразделения"

(//input[@role='combobox'])[1] - "Регион

(//input[@role='combobox'])[2] - "Город или населённый пункт"

(//input[@role='combobox'])[3] - "Улица"

((//span[text()=' '])[2]/following::input)[1] - "Дом, литера, корпус, строение"

//input[@id="mat-input-17"] - "Квартира"

//input[@type='phone'] - "Телефон"

(//input[@type='email'])[1] - "Электронная почта"

(//input[@type='email'])[2] - "Повтор электронной почты"

## 3. Чекбоксы:

//mat-checkbox[@id="mat-checkbox-1"] - "Отчество отсутствует"

//mat-checkbox[@id="mat-checkbox-2"] - "Улица отсутствует"

## 4. Datepicker:

//*[@id="mat-datepicker-1"] - "Дата рождения" (календарь)

(//div[@class='mat-form-field-wrapper ng-tns-c61-7']//div)[1] - "Дата рождения" (датапикер целиком)

//*[@id="mat-datepicker-2"] - "Дата выдачи" (календарь)

(//div[@class='mat-form-field-wrapper ng-tns-c61-10']//div)[1] - "Дата выдачи" (датапикер целиком)
