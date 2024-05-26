# EVM
EVM - это приложение на C# с использованием WPF, предназначенное для тестирования различных компонентов материнской платы Gigabyte B550M BS3H. Программа содержит в себе тесты напряжения, сопротивления, слотов ОЗУ, слотов PCIe, сокета ЦПУ,  BIOS, батарейки BIOS, линий USB и кварцевых резонаторов.

## Особенности

- **Тестирование напряжения**: Проверка уровней напряжения линий 3.3V, 5V и 12V.
- **Тестирование сопротивления**: Измерение сопротивления различных линий материнской платы.
- **Тестирование BIOS**: Использование осциллографа для проверки BIOS.
- **Тестирование сокета ЦПУ**: Проверка работоспособности сокета ЦПУ.
- **Тестирование линий USB**: Проверка напряжения линий USB.
- **Тестирование слотов ОЗУ**: Проверка состояния слотов ОЗУ.
- **Тестирование слотов PCIe**: Проверка функциональности слотов PCIe.
- **Тестирование кварцевого резонатора**: Проверка кварцевого резонатора с помощью осциллографа.
- **Тестирование батарейки BIOS**: Измерение напряжения батарейки BIOS.

## Пользовательский интерфейс

### Боковая панель инструментов

Верхняя панель инструментов содержит переключатели для выбора метода тестирования:

- **Мультиметр**:
    - Сопротивление
    - Напряжение
    - Сила тока
      
- **Осциллограф**
- **Тестер ОЗУ**
- **Тестер PCIe**
- **Тестер сокета ЦПУ**

### Основная область просмотра

Основная область просмотра отображает изображение материнской платы с кнопками, соответствующими различным компонентам. Эти кнопки запускают определенные тесты в зависимости от выбранного метода тестирования.

### Область вывода результатов

Область вывода результатов показывает результаты тестов, включая любые изображения (например, показания осциллографа), вопросы и кнопки ответов.

## Как использовать

1. **Выберите метод тестирования**:
    - Нажмите одну из кнопок на верхней панели инструментов, чтобы выбрать метод тестирования. Одновременно может быть активен только один метод тестирования.

2. **Выберите компонент для тестирования**:
    - Нажмите соответствующую кнопку на изображении материнской платы, чтобы выбрать компонент для тестирования.

3. **Просмотр результатов**:
    - Результаты теста будут отображены в области вывода результатов. Если применимо, появится вопрос о том, работает ли компонент правильно.
    - Нажмите "Да" или "Нет", чтобы ответить на вопрос на основе отображаемых результатов.

### Пример рабочего процесса

1. **Тестирование напряжения на линии 3.3V**:
    - Выберите кнопку "Проверка напряжения" на верхней панели инструментов.
    - Нажмите кнопку "3.3V" на изображении материнской платы.
    - В области вывода результатов будет показано показание напряжения и вопрос о том, находится ли оно в нормальном диапазоне. Ответьте "Да" или "Нет".

2. **Тестирование сопротивления на линии 5V**:
    - Выберите кнопку "Проверка сопротивления" на верхней панели инструментов.
    - Нажмите кнопку "5V" на изображении материнской платы.
    - В области вывода результатов будет показано показание сопротивления и вопрос о том, находится ли оно в нормальном диапазоне. Ответьте "Да" или "Нет".

## Структура кода

### MainWindow.xaml.cs

Основная логика приложения находится в файле `MainWindow.xaml.cs`. Включает:

- Обработчики событий для нажатия кнопок (`Voltage3_3V_Click`, `Voltage5V_Click` и т.д.).
- Методы для тестирования напряжения и сопротивления (`TestVoltage`, `TestResistance`).
- Методы для случайных тестов (`TestRandom`).
- Методы для тестов с осциллографом (`TestOscilloscope`).
- Вспомогательные методы для обновления интерфейса (`ResetFlagsAndUI`, `ShowQuestionAndAnswers`, `HideQuestionAndAnswers`).

### MainWindow.xaml

Файл `MainWindow.xaml` определяет макет пользовательского интерфейса приложения, включая:

- Боковую панель инструментов с переключателями.
- Основную область просмотра с изображением материнской платы и кнопками.
- Область вывода результатов для отображения результатов тестов, вопросов и ответов.

## Заключение

EVM - это многофункциональный инструмент для имитации тестов компонентов материнской платы. Следуя инструкциям в этом руководстве, вы сможете эффективно использовать приложение для тестирования различных компонентов и проверки их исправности.

