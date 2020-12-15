### Содержание
  1. [Введение](#1)
  2. [Объект тестирования](#2)
  3. [Атрибуты качества](#3)
  4. [Риски](#4)
  5. [Аспекты тестирования](#5)<br>
    5.1. [Возможность начать новую игру](#001)<br>
    5.2. [Возможность перемещать персонажа](#002)<br>
    5.3. [Изменения значений счета в поле HUD](#003)<br>
    5.4. [Возможность поставить игру на паузу и выход из нее](#004)<br>
    5.5. [Проигрывание музыки](#005)<br>
    5.6. [Возможность выхода в главное меню через меню паузы](#006)<br>
6. [Подходы к тестированию](#6)
7. [Представление результатов](#7)
8. [Выводы](#8)


<a name="1"></a>
### 1. Введение
Данный план предназначен для тестирования игры "ShadowKiller". Цель проведения тестирования - проверка работоспособности и пригодности продукта для практического использования.

<a name="2"></a>
### 2. Объект тестирования
В качестве объектов тестирования можно выделить атрибуты качества платформы по ISO 25010:
1. функциональность
	- функциональная полнота: приложение должно выполнять все заявленные функции
	- функциональная корректность: приложение должно выполнять все заявленные функции корректно
	- функциональная целесообразность: отсутствуют не заявленные функции, которые бы мешали приложению выполнять первоначально поставленные задачи
2. удобство использования
	- эстетика пользовательского интерфейса: элементы управления объектами должны быть всегда доступны пользователю
	
Данные атрибуты были взяты с учётом специфики приложения.

Тестируемое приложение содержит 3 модуля, созданный для выполнения определённого функционала:
 - главное окно (Игровое поле для игры PvP), главное меню и меню паузы.


<a name="3"></a>
### 3. Атрибуты качества
1. Функциональность:
    - функциональная полнота: приложение должно соответствовать всем функциональным требованиям, заявленных в [SRS](https://github.com/vladpochobut/ShadowKiller/blob/main/Documentation/SRS.md);
    - функциональная целесообразность: отсутствуют не заявленные функции, которые бы мешали приложению выполнять поставленные задачи, некоторые функции могут быть видоизменены.
2. Удобство использования:
    - простота пользовательского интерфейса: интерфейс должен быть достаточно простым для интуитивного использования новым пользователем.
3. Платформа:
    - корректная работа приложения на платформе(ах):
      - Windows (поддерживающая версию Unity 2019.4.13f1 и старше)
      

<a name="4"></a>
### 4. Риски
Приложение использует системные средства для воспроизведения звука, из-за чего воспроизведение звука на разных платформах может отличаться. 


<a name="5"></a>
### 5. Аспекты тестирования
Данное тестирование является интеграционным, т. е. программные модули тестируются в группке, также является дымовым, и будет проводиться по типу "Black box", т. е. без доступа к исходному коду.<br>
В ходе тестирования планируется проверить реализацию основных функций, провести позитивные и негативные тесты, а также проверить нефункциональные требования. К основным функциям можно отнести следующие пункты:

    -Возможность начать новую игру
    -Возможность начать новую игру против бота
    -Возможность перемещать "ракетку" в заданных пределах
    -Изменения значений счета в поле HUD
    -Возможность поставить игру на паузу и выход из нее
    -Проигрывание музыки
    -Возможность изменения уровня громкости в главном меню
    -Возможность изменения уровня громкости через меню паузы
    -Возможность выхода в главное меню через меню паузы

#### Функциональные требования:

<a name="001"></a>
##### Возможность начать новую игру
Этот пункт необходимо протестировать на:
1. Реакцию приложения на попытку начать новую игру.
2. Выполнение данной операции.


<a name="002"></a>
##### Возможность перемещать "ракетку" в заданных пределах
Этот пункт необходимо протестировать на:
1. Прыгать, бегать.
2. Врезаться в стены.

<a name="003"></a>
##### Изменения значений счета в поле HUD
Этот пункт необходимо протестировать на:
1. Отображение счета.
2. Обнуление счета после завершения игры
3. Изменения счета при условии, что мяч покинул пределы карты.

<a name="004"></a>
##### Возможность поставить игру на паузу и выход из нее.
Этот пункт необходимо протестировать на:
1. При нажатии на кнопку паузы установка параметра скорости игры на "0". 
2. При выходе из меню паузы установить параметр скорости игры на "1".  

<a name="005"></a>
##### Проигрывание музыки
Этот пункт необходимо протестировать на:
1. Музыка проигрывается при запуске игры.
2. Музыкальный фон не должен дублироваться на двух сценах одновременно.
3. Музыкальный фон должен быть цикличным.

<a name="006"></a>
##### Возможность выхода в главное меню через меню паузы
Этот пункт необходимо протестировать на:
1. Переход на сцену главного меню через меню паузы.
2. Обнуление текущего счета.

#### Нефункциональные требования:
- все элементы пользовательского интерфейса имеют название, описывающее действие которое они выполняют.

<a name="6"></a>
### 6. Подходы к тестированию
Проводимое тестирование можно опередлить как:
  - По степени автоматизации: ручное.
  - По знанию системы: черный ящик.
  - По степени изолированности компонентов: интеграционное.

<a name="7"></a>
### 7. Представление результатов
Результаты тестирования представлены в [таблице](https://github.com/vladpochobut/ShadowKiller/test/TestResults.md).

<a name="8"></a>
### 8. Выводы
Данный тестовый план позволяет протестировать основной функционал продукта. Успешное прохождение всех тестов не гарантирует полной работоспособности на всех платформах и архитектурах, однако позволяет полагать, что данный продукт работает корректно.