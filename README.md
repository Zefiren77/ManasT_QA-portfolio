# Обо мне

Открытый, ориентированный на результат командный игрок с 8-летним опытом работы в ООН и ОБСЕ и страстью к кондитерскому делу. Меня вдохновляет инновационный опыт и сложная работа, включающая непрерывный цикл обучения, поиск ответов и осознание того, что наша совместная деятельность улучшила показатели и позволила достичь поставленных целей.

Здесь собраны материалы и проекты реализованные в рамках обучения на направлении ["Инженер по тестированию"](https://praktikum.yandex.ru/qa-engineer) в SKYpro.


***



# Направления

[**Проектирование тестов**](#test-design)<br>

    * Виды тестирования | Mind-map | Блок-схемы
    * Тест-дизайн | Классы эквивалентности | Граничные значения
    * Тестирование документации | Чек-листы | Тест-кейсы

**Тестирование API**

    * REST API | JSON | Postman

**Тестирование баз данных**

    * Консоль | SQL | PostgreSQL

 
***

  ## <a name="test-design" />Проектирование тестов
  <br>

📄**1. Составь mind-map сервиса по продаже тортиков**

<details>
<summary>Mind map сервиса</summary>

![Mind Map](https://github.com/ToktombaevM/ManasT_QA-portfolio/blob/9e5d1be44f6df16e7393e5b5eda308cdcf9a831e/IMG/Mind%20Map.jpg)

[Mind map в большом разрешении на MIRO](https://miro.com/app/board/uXjVMV_dsEQ=/?share_link_id=605007146557)

</details>
<br>

📄**2. Классы эквивалентности и граничные значения**

<details>
<summary>Задача 1-Протестировать консольное приложение (приложение в вакууме).</summary> <br>

  - Приложение на вход принимает три целых числа, интерпретируемых как длины сторон треугольника.
  - На выходе выводит на экран, является ли этот треугольник равнобедренным или равносторонним.
 
 > Что нужно сделать?
  - Составьте низкоуровневый чек-лист. Обязательно предложите конкретные значения тестовых данных.

**РЕШЕНИЕ**  
![TASK 1](https://github.com/ToktombaevM/ManasT_QA-portfolio/blob/8cc525406212ae02ac2c38242f5e1e98ae7af35a/IMG/TASK%201.png)

</details>

<details>
<summary>Задача 2-Протестировать лифт в девятиэтажном доме.</summary> <br>
   
 > Что нужно сделать?
  - Составить высокоуровневый чек-лист.

**РЕШЕНИЕ**  
![TASK 2](https://github.com/ToktombaevM/ManasT_QA-portfolio/blob/af535ce865670662d29930dfd9e36b7c3a8043b5/IMG/TASK%202.png)
</details>

<details>
<summary>Задача 3-Протестировать работу накопительных скидочных карт.</summary> <br>

Автомат принимает накопительные скидочные карты и при своем расчете учитывает количество баллов, по которому начисляет процент скидки:

от 0 до 100 баллов — скидка 1%;
от 100 до 200 баллов — скидка 3%;
от 200 до 500 баллов — скидка 5%;
от 500 баллов — скидка 10%.

 > Что нужно сделать?
  - Составить такой набор тестовых данных для автомата, при котором мы гарантированно будем знать, что в соответствии со своими накопленными баллами покупатель получит верную скидку.

**РЕШЕНИЕ**  
![TASK 3](https://github.com/ToktombaevM/ManasT_QA-portfolio/blob/a2c8c01ce1f208b768d4ce170594de717757919a/IMG/TASK%203.png)
</details> 
<br>

📄**3. Тестирование документации**

<details>
<summary>ТЗ от заказчика</summary> <br>
   
   - Реализовать форму, которая по введенным данным определяет, является ли человек совершеннолетним. <br>
   - Приложение должно быть с архитектурой «клиент — сервер».
</details> 

    * 💡ОТВЕТЫ НА ВОПРОСЫ

<details>
<summary>Какие могут возникнуть вопросы к требованиям?</summary> <br>

   - Какой **тип данных** должен быть введен в поле определения возраста: текст, дата или число?
   - Если вводимые данные, дата рождения, **в каком формате** поле должно принимать данные: MM.YYYY, YYYY-MM-DD или другой формат?
   - Требуется уточнить **какое значение** считается совершеннолетием? 16 лет, 18 лет, 21 год?
   - Что ответит система, если вводимое значение **не соответствует требованиям** системы?
   - Что произойдет, если клиент несовершеннолетний?
   - Что произойдет, если клиент совершеннолетний?
   </details>
   
<details>
<summary>Какие виды и типы тестирования стоит проводить? Объясните почему.</summary> <br>
   
   - **Smoke тестирование:** Проверить открывается ли поле, принимает ли оно вводимые данные, работает ли кнопка «ОК» или «Далее», чтобы убедиться, в работоспособности поля для продолжения тестирования?
   - **Функциональное тестирование:** требуется проверить, что поле принимает заданные значения, и обрабатывает значения правильно, например определяет, является ли человек совершеннолетним или нет.
   - **Тестирование безопасности:** поле не позволяет ввести невалидные данные, которые могут привести к неправильному определению возраста человека (например, спецсимволы, иероглифы, скобки, кавычки и тд.).
   - **Тестирование производительности:** проверить, как поле работает под нагрузкой. Например, выдержит ли поле, если его будут заполнять и отправлять одновременно с разных клиентских устройств в большом количестве.
 </details>

<details>
<summary>Что больше подойдет для организации тестовой документации по задаче — тест-кейсы или чек-листы? Почему?</summary> <br>
   
   - Так как мы тестируем одно поле ввода, следует использовать чек-лист для охвата большего количества и вариантов проверок.
   - Чит-лист позволит оптимизировать процесс тестирования путем группировки схожих сценариев и инструментов.
   - Тест-кейсы в данном случае будут не эффективны, так как нерационально, тратить много времени на расшифровку одного действия, в то время как можно произвести большее количество проверок по чек-листу за потраченное время.
 </details> 

 <details>
<summary>Какие техники тест-дизайна вы бы использовали? Почему?</summary> <br>

- **Классы эквивалентности** (в зависимости, от того, какое число мы считаем наступлением совершеннолетием. Например, 18 лет). В данном случае классов эквивалентности будет (меньше 0, 0, 1-17, и больше 18)
- **Граничные значения** 16, 17, 19, 20, чтобы проверить правильность обработки вводимой информации.
   </details>

    <details>
<summary>Какие можно выделить негативные и позитивные входные данные?</summary> <br>

| Позитивные проверки | Примеры |
| --- | --- |
| ввод корректных данных в соответствии с документацией (чисел в заданном диапазоне) | 17, 18, 19, 20 |

| Негативные проверки | Примеры |
| --- | ---      |
| пустое поле |   |
| ввод букв | AnГ |
| спецсимволы | ?:%?* |
| ввод отрицательных чисел  | -17 |

   </details>

   <details>
<summary>Какие теоретически могут быть баги? Опишите 4–6 возможных багов.</summary> <br>
      
- Поле ввода данных неактивно, то есть в него нельзя ввести данные.
- При вводе данных не отображаются все данные, либо отображаются некорректно.
- Кнопка «ОК» неактивна, то есть на нее нельзя нажать.
- Кнопка “OK” активна, но ничего не происходит после нажатия на нее.
- Кнопка “OK” активна, но при нажатии обнуляются данные, введенные в поле.
- Кнопка “OK” активна, но при нажатии страница закрывается.
   </details>

<details>
<summary>Есть ли баги любого типа на приведенных скриншотах? Если есть, опишите все.</summary> <br>

![Screenshot dev](https://github.com/ToktombaevM/ManasT_QA-portfolio/blob/59088d98f2217ea753e99f562ead406ae3f9797f/IMG/Screenshot%20dev.png)
      
- Кнопки “ОК” разного размера и цвета
- Грамматически некорректно написано “Вы совершен**ноле**тний” (пишется слитно); Не совершеннолетний (пишется слитно).
- Неверная формулировка. Оба поля должны быть сформулированы в одном стиле, либо обращение, либо вопрос.
- Нет кнопки закрыть всплывающее окно, либо вернуться назад.
   </details><br>

📄**4. СОСТАВЛЕНИЕ SMOKE-ТЕСТОВ**

<details>
<summary>ТЗ от заказчика</summary> <br>
   
   **Выберите тестовую документацию**

- Если ваше полное имя начинается на согласную букву, вам нужно **составить смоук-тест-кейс(ы) - имя: МАНАС.**

**Выберите приложение, по которому будете составлять документацию**

- Главная страница https://www.rosbank.ru/ - **фамилия: Токтомбаев.**
</details> 

    * 💡ТЕСТ КЕЙСЫ

   <details>
<summary>TA-1: Проверить, что главная страница банка загружается и видны пункты меню.</summary> <br>
      
- Поле ввода данных неактивно, то есть в него нельзя ввести данные.
- При вводе данных не отображаются все данные, либо отображаются некорректно.
- Кнопка «ОК» неактивна, то есть на нее нельзя нажать.
- Кнопка “OK” активна, но ничего не происходит после нажатия на нее.
- Кнопка “OK” активна, но при нажатии обнуляются данные, введенные в поле.
- Кнопка “OK” активна, но при нажатии страница закрывается.
   </details>

[Блок-схема в большом разрешении](https://i.ibb.co/BndGfjN/blockscheme.jpg)

<details>
<summary>Требования к сервису Яндекс.Маршруты</summary>
</details>

# Навыки

* [Навыки и знания 1]
* [Навыки и знания 2]
* [Навыки и знания 3]

# Контактная информация

* [Ваш адрес электронной почты]
* [Ваша ссылка в LinkedIn]
* [Ваш GitHub]

# Резюме

* [Ссылка на ваше резюме]

# Картинки

![Картинка 1](images/image1.png)
![Картинка 2](images/image2.png)
