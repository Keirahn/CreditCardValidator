**Отчёт о тестировании Credit Card Number Validator**

**Краткое описание**
08.03.2021 было проведено тестирование документации, тестирование установки и функциональное тестирование приложения Credit Card Number Validator.

На тестирование затрачено: 1.5 часа

В результате тестирования выявлено, что валидация проваливается в случае, если введенное значение __больше или меньше 16 цифр__, в результате чего не проходят валидацию некоторые виды кредитных карт. Исходя из принципа эквивалентных значений, БР были заведены на один из трёх эквивалентных случаев провала теста для каждой платёжной системы:

1. [Валидный номер кредитной карты Discover не проходит валидацию в приложении Credit Card Number Validator](https://github.com/Keirahn/CreditCardValidator/issues/6)

2. [Валидный номер кредитной карты American Express (AMEX) не проходит валидацию в приложении Credit Card Number Validator](https://github.com/Keirahn/CreditCardValidator/issues/5)

3. [Валидный номер кредитной карты JCB не проходит валидацию в приложении Credit Card Number Validator](https://github.com/Keirahn/CreditCardValidator/issues/4)
4. [Валидный номер кредитной карты Diners Club - Сarte Blanche не проходит валидацию в приложении Credit Card Number Validator](https://github.com/Keirahn/CreditCardValidator/issues/3)
5. [Валидный номер кредитной карты Diners Club - International не проходит валидацию в приложении Credit Card Number Validator](https://github.com/Keirahn/CreditCardValidator/issues/2)
6. [Валидный номер кредитной карты Visa не проходит валидацию в приложении Credit Card Number Validator](https://github.com/Keirahn/CreditCardValidator/issues/1)

**Описание процесса тестирования**

В качестве тестовых данных использовались [Инструкция по установке IntelliJ IDEA](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/idea.md), 
[сгенерированный набор номеров фейковых кредитных карт на Freeformatter.com](https://www.freeformatter.com/credit-card-number-generator-validator.html#fakeNumbers)

Для проведения тестирования был использован следующий набор номеров кредитных карт (ОР - ожидаемый результат, ФР - фактический результат):

VISA:
```
4893077371512773  - ОР: "Result is OK", ФР: "Result is OK"
4716570210702634 - ОР: "Result is OK" 
4539635479181545791 - ОР: "Result is OK", ФР: "Result is FAIL" 
```
MasterCard:
```
5276603313799071 - ОР: "Result is OK", ФР: "Result is OK"
2720991388550118 - ОР: "Result is OK", ФР: "Result is OK"
5591140051571147 - ОР: "Result is OK", ФР: "Result is OK"
```
American Express (AMEX):
```
371572581962858 - ОР: Result is OK", ФР: "Result is FAIL" 
341375842170825 - ОР: Result is OK", ФР: "Result is FAIL" 
373277979451435 - ОР: Result is OK", ФР: "Result is FAIL" 
```
Discover:
```
6011170275681026 - ОР: "Result is OK", ФР: "Result is OK"
6011316377481357 - ОР: "Result is OK", ФР: "Result is OK"
6011775764201929507 - ОР: Result is OK", ФР: "Result is FAIL" 
```
JCB:
```
3541208880477657 - ОР: "Result is OK", ФР: "Result is OK"
3533963049115776 - ОР: "Result is OK", ФР: "Result is OK"
3534454198901263382 - ОР: Result is OK", ФР: "Result is FAIL" 
```
Diners Club - North America:
```
5423964567056515 - ОР: "Result is OK", ФР: "Result is OK"
5540000758154294 - ОР: "Result is OK", ФР: "Result is OK"
5475788735354768 - ОР: "Result is OK", ФР: "Result is OK"
```
Diners Club - Carte Blanche:
```
30143073327613 - ОР: Result is OK", ФР: "Result is FAIL" 
30383581645318 - ОР: Result is OK", ФР: "Result is FAIL" 
30390405132845 - ОР: Result is OK", ФР: "Result is FAIL" 
```
Diners Club - International:
```
36677075388002 - ОР: Result is OK", ФР: "Result is FAIL" 
36212573714317 - ОР: Result is OK", ФР: "Result is FAIL" 
36772575923315 - ОР: Result is OK", ФР: "Result is FAIL" 
```
Maestro:
```
5893827191796650 - ОР: "Result is OK", ФР: "Result is OK"
6759820381193094 - ОР: "Result is OK", ФР: "Result is OK"
6763311583897314 - ОР: "Result is OK", ФР: "Result is OK"
```
Visa Electron:
```
4175004743501747 - ОР: "Result is OK", ФР: "Result is OK"
4026900153920379 - ОР: "Result is OK", ФР: "Result is OK"
4175002048841982 - ОР: "Result is OK", ФР: "Result is OK"
```
InstaPayment:
```
6391570876504610 - ОР: "Result is OK", ФР: "Result is OK" 
6375383847148388 - ОР: "Result is OK", ФР: "Result is OK"
6394029225667161 - ОР: "Result is OK", ФР: "Result is OK"
```

**Тестирование производилось в следующем окружении:**

- macOS 11.1 (20C69)
- openjdk version "11.0.10" 2021-01-19
- OpenJDK Runtime Environment AdoptOpenJDK (build 11.0.10+9)
- OpenJDK 64-Bit Server VM AdoptOpenJDK (build 11.0.10+9, mixed mode)
- IntelliJ IDEA 2020.3.2 (Community Edition) Build #IC-203.7148.57, built on January 26, 2021
Runtime version: 11.0.9.1+11-b1145.77 x86_64

