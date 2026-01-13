# Урок 7: Условия if-else

> [!info] 🎯 Цель урока  
> После этого урока ты сможешь писать простые программы с выбором: выполнять разные действия в зависимости от условия с помощью if﻿ и else﻿.[programiz+1](https://www.programiz.com/python-programming/if-elif-else)​

## 📚 Что понадобится

-  Компьютер с Python
    
-  Предыдущий урок: [[06-Работа-со-строками|Урок:6 Работа со строками]] 
    

---

## 🔥 Разминка (3 мин)

> [!question] Вспомни  
> Какие математические операторы сравнения ты знаешь в математике (больше, меньше, равно)?

 Больше, меньше, больше или равно, меньше или равно, равно, не равно. В Python им соответствуют: 
```text
 >, <, >=, <=, ==, !=
```

---

## 📖 Теория (7 мин)

## Что такое условие?

Условие в программе — это вопрос «да/нет», на который компьютер отвечает True﻿ (истина) или False﻿ (ложь).
Оператор if﻿ позволяет выполнить блок кода только если условие истинно, иначе можно выполнить другой блок через else
## Синтаксис

```python
age = 14

if age >= 18:
    print("Тебе уже можно всё по-взрослому!")
else:
    print("Ты ещё подросток.")

print("Эта строка выполняется всегда.")
```
## Как это работает?

1. После if﻿ пишется условие (обычно сравнение), затем двоеточие и блок кода с отступом​
    
2. Если условие истинно, выполняется блок if﻿, а else﻿ пропускается; если ложно — наоборот​
    
3. Операторы сравнения: >﻿, <﻿, >=﻿, <=﻿, ==﻿, !=﻿ возвращают только True﻿ или False﻿.​
    

> [!warning] Частая ошибка  
> Не путай =﻿ (присваивание) и ==﻿ (сравнение), а также не забывай ставить отступ (4 пробела или Tab) внутри блоков if﻿ и else﻿.​

---

## 💻 Практика (15 мин)

## Задание: «Совершеннолетний или нет?»

**Что делаем:** спрашиваем возраст и выводим разное сообщение в зависимости от того, есть ли 18 лет.

## Шаг 1: Создай файл

```text
Создай новый файл: uroк7_if_else.py
```

## Шаг 2: Напиши код

```python
age_text = input("Сколько тебе лет? ")
age = int(age_text)

if age >= 18:
    print("Ты совершеннолетний(ая). Можно многое!")
else:
    print("Ты ещё несовершеннолетний(ая). Главное сейчас — учёба и развитие!")

print("Программа завершена.")
```

## Шаг 3: Запусти программу

Введи разные значения возраста: меньше 18 и больше/равно 18, смотри, как меняется ответ.

## Шаг 4: Добавь ещё одно условие

Добавь проверку, что если возраст меньше 7, выводится сообщение "Ты ещё дошкольник!"﻿ перед основным if﻿. Можно сделать второй if﻿ отдельно.

## Шаг 5: Поменяй текст под себя

Сделай формулировки более «своими» — чтобы программа звучала как сообщение от тебя.

text

`Ожидаемый результат: Программа запрашивает возраст и выводит разные сообщения для несовершеннолетнего и совершеннолетнего пользователя.`

> [!success] Готово!  
> Если программа корректно реагирует на разные введённые возраста, условие работает как надо.

---

## ✅ Проверь себя (5 мин)

## Твой код должен:

-  Использовать if﻿ и else﻿ с отступами
    
-  Проверять возраст с помощью оператора сравнения (например, >=﻿)
    
-  Работать корректно для возрастов меньше и больше/равно 18
    

## Ответь на вопросы:

1. Чем отличаются операторы =﻿ и ==﻿ в Python?
    
2. Что произойдёт, если условие в if﻿ ложно и есть блок else﻿?
    

<details> <summary>Ответы</summary>

1. =﻿ присваивает значение переменной, а ==﻿ сравнивает два значения и возвращает True﻿ или False﻿.[study+1](https://study.com/learn/lesson/python-not-equal-conditional-operators.html)​
    
2. Блок кода под if﻿ пропускается, и выполняется блок под else﻿.[programiz+1](https://www.programiz.com/python-programming/if-elif-else)​
    

</details>

---

## ⭐ Бонус (если осталось время)

> [!tip] Дополнительное задание  
> Сделай «оценщик оценок»: попроси ввести число от 1 до 5 и с помощью нескольких if﻿–else﻿ выводи комментарий, например: 5 — "Отлично!"﻿, 4 — "Хорошо"﻿, 3 — "Нужно подтянуться"﻿ и т.д.

---

## 🔗 Навигация

◀️ Предыдущий: [[06-Работа-со-строками|Урок:6 Работа со строками]]  
▶️ Следующий: [[08-Калькулятор|Урок:8 Калькулятор]]  
🏠 [[00 - Главная|Вернуться к оглавлению]]

---

## 📝 Мои заметки

[Место для заметок ученика]

1. [https://www.programiz.com/python-programming/if-elif-else](https://www.programiz.com/python-programming/if-elif-else)
2. [https://www.w3schools.com/python/python_conditions.asp](https://www.w3schools.com/python/python_conditions.asp)
3. [https://study.com/learn/lesson/python-not-equal-conditional-operators.html](https://study.com/learn/lesson/python-not-equal-conditional-operators.html)
4. [https://pykili.github.io/prog/02-if-and-comparison-ops](https://pykili.github.io/prog/02-if-and-comparison-ops)
5. [https://www.w3schools.com/python/gloss_python_comparison_operators.asp](https://www.w3schools.com/python/gloss_python_comparison_operators.asp)
6. [https://realpython.com/python-conditional-statements/](https://realpython.com/python-conditional-statements/)
7. [https://www.freecodecamp.org/news/python-if-else-statement-conditional-statements-explained/](https://www.freecodecamp.org/news/python-if-else-statement-conditional-statements-explained/)
8. [https://www.simplilearn.com/tutorials/python-tutorial/python-if-else-statement](https://www.simplilearn.com/tutorials/python-tutorial/python-if-else-statement)
9. [https://www.digitalocean.com/community/tutorials/if-else-statements-in-python](https://www.digitalocean.com/community/tutorials/if-else-statements-in-python)
10. [https://www.geeksforgeeks.org/python/python-if-else/](https://www.geeksforgeeks.org/python/python-if-else/)
11. [https://www.ionos.com/digitalguide/websites/web-development/python-if-else/](https://www.ionos.com/digitalguide/websites/web-development/python-if-else/)
12. [https://proglang.su/python/comparison-operators](https://proglang.su/python/comparison-operators)
13. [https://www.freecodecamp.org/news/how-to-use-conditional-statements-if-else-elif-in-python/](https://www.freecodecamp.org/news/how-to-use-conditional-statements-if-else-elif-in-python/)
14. [https://docs.python.org/3/tutorial/controlflow.html](https://docs.python.org/3/tutorial/controlflow.html)
15. [https://www.youtube.com/watch?v=-rZPM-VlKB8](https://www.youtube.com/watch?v=-rZPM-VlKB8)
16. [https://www.youtube.com/watch?v=-BOBedcjySI](https://www.youtube.com/watch?v=-BOBedcjySI)
17. [https://github.com/Pierian-Data/Python-Russian/blob/master/01-%D0%9E%D0%BF%D0%B5%D1%80%D0%B0%D1%82%D0%BE%D1%80%D1%8B%20%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D1%8F%20%D0%B2%20Python%20(Python%20Comparison%20Operators)/01-Comparison%20Operators.ipynb](https://github.com/Pierian-Data/Python-Russian/blob/master/01-%D0%9E%D0%BF%D0%B5%D1%80%D0%B0%D1%82%D0%BE%D1%80%D1%8B%20%D0%A1%D1%80%D0%B0%D0%B2%D0%BD%D0%B5%D0%BD%D0%B8%D1%8F%20%D0%B2%20Python%20\(Python%20Comparison%20Operators\)/01-Comparison%20Operators.ipynb)
18. [https://labex.io/ru/tutorials/python-python-data-types-and-operators-393077](https://labex.io/ru/tutorials/python-python-data-types-and-operators-393077)
19. [https://senjun.ru/courses/python/chapters/python_chapter_0090/](https://senjun.ru/courses/python/chapters/python_chapter_0090/)
20. [https://www.guru99.com/ru/python-operators-complete-tutorial.html](https://www.guru99.com/ru/python-operators-complete-tutorial.html)