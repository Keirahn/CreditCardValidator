**Отчёт о тестировании Credit Card Number Validator**

**Краткое описание**
08.03.2021 было проведено тестирование документации, тестирование установки и функциональное тестирование приложения Credit Card Number Validator.

На тестирование затрачено: 1.5 часа

В результате тестирования выявлено, что валидация проваливается в случае, если введенное значение больше или меньше 16 цифр, в результате чего не проходят валидацию некоторые виды кредитных карт:

1. [Валидный номер кредитной карты Discover не проходит валидацию в приложении Credit Card Number Validator](https://github.com/Keirahn/CreditCardValidator/issues/6)

2. [Валидный номер кредитной карты American Express (AMEX) не проходит валидацию в приложении Credit Card Number Validator](https://github.com/Keirahn/CreditCardValidator/issues/5)

3. [Валидный номер кредитной карты JCB не проходит валидацию в приложении Credit Card Number Validator](https://github.com/Keirahn/CreditCardValidator/issues/4)
4. [Валидный номер кредитной карты Diners Club - Сarte Blanche не проходит валидацию в приложении Credit Card Number Validator](https://github.com/Keirahn/CreditCardValidator/issues/3)
5. [Валидный номер кредитной карты Diners Club - International не проходит валидацию в приложении Credit Card Number Validator](https://github.com/Keirahn/CreditCardValidator/issues/2)
6. [Валидный номер кредитной карты Visa не проходит валидацию в приложении Credit Card Number Validator](https://github.com/Keirahn/CreditCardValidator/issues/1)

**Описание процесса тестирования**

В качестве тестовых данных использовались [Инструкция по установке IntelliJ IDEA](https://github.com/netology-code/javaqa-homeworks/blob/master/intro/idea.md), 
[сгенерированный набор номеров фейковых кредитных карт на Freeformatter.com](https://www.freeformatter.com/credit-card-number-generator-validator.html#fakeNumbers)

Для проведения тестирования был использован следующий набор номеров кредитных карт:

VISA:
```
4893077371512773  - ожидаемый результат "Result is OK" 
4539635479181545791 - ожидаемый результат "Result is OK" 
```
MasterCard:
```
5276603313799071 - ожидаемый результат "Result is OK" 
```
American Express (AMEX):
```
373277979451435 - ожидаемый результат "Result is OK" 
```
Discover:
```
6011170275681026 - ожидаемый результат "Result is OK"  
6011775764201929507 - ожидаемый результат "Result is OK" 
```
JCB:
```
3541208880477657 - ожидаемый результат "Result is OK" 
3534454198901263382 - ожидаемый результат "Result is OK" 
```
Diners Club - North America:
```
5423964567056515 - ожидаемый результат "Result is OK" 
```
Diners Club - Carte Blanche:
```
30143073327613 - ожидаемый результат "Result is OK" 
```
Diners Club - International:
```
36677075388002 - ожидаемый результат "Result is OK" 
```
Maestro:
```
6763311583897314 - ожидаемый результат "Result is OK" 
```
Visa Electron:
```
4175004743501747 - ожидаемый результат "Result is OK" 
```
InstaPayment:
```
6391570876504610 - ожидаемый результат "Result is OK" 
```

**Тестирование производилось в следующем окружении:**

- macOS 11.1 (20C69)
- openjdk version "11.0.10" 2021-01-19
- OpenJDK Runtime Environment AdoptOpenJDK (build 11.0.10+9)
- OpenJDK 64-Bit Server VM AdoptOpenJDK (build 11.0.10+9, mixed mode)
- IntelliJ IDEA 2020.3.2 (Community Edition) Build #IC-203.7148.57, built on January 26, 2021
Runtime version: 11.0.9.1+11-b1145.77 x86_64

