## Создание вероятностной модели покупки товара используя SQL-код

Цель: увеличить доход магазина за счет дополнительной продажи горных велосипедов существующим и новым клиентам. 
Определить целевую аудиторию которая с максимальной вероятностью положительно отреагирует на предложение о покупке горного велосипеда.
Используя концепцию Байесовской условной вероятности определить клиентов магазина, которые не покупали в нашем магазине горные велосипеды, но на 80-100% по своим характеристикам (пол, возраст, доход и прочие исследованные данные) соответствуют покупателям ранее купившим горный велосипед.
Для достижения поставленной цели: информировать предложением о покупке следующие группы клиентов с идентичными характеристиками:
* существующих клиентов магазина не купивших ранее горный велосипед;
* вновь регистрируемых клиентов в базе данных магазина;
* потенциальных покупателей, не являющихся клиентами магазина, но по имеющимся данным соответствующих нашей выборке.

В базе данных магазина накоплен большой объем поведения 18’484 покупателей (массивы DimCustomer, DimGeography учебной базы MS AdventureWorksDW2014) и их покупках (массивы FactInternetSales, DimProduct). 

Предполагая стабильность прошлых факторов в будущем можно экстраполировать поведение текущих покупателей на будущих: надо взять большой массив в прошлых данных на основе них построить вероятностную модель с выявленными условиями.
Через эту модель проанализировать: текущих клиентов (которые еще не купили исследуемый товар) + всех вновь регистрируемых у нас клиентов + потенциальных  клиентов.

Используя SQL – обработка данных быстрее за счет произведения расчетов в месте хранения данных.
