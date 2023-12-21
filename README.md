## Комп'ютерні системи імітаційного моделювання
## СПм-22-5, **Ні Олег В'ячеславович**
### Лабораторна робота №**1**. Опис імітаційних моделей та проведення обчислювальних експериментів

<br>

### Варіант 6, модель у середовищі NetLogo:
[Rabbits Grass Weeds](https://www.netlogoweb.org/launch#http://www.netlogoweb.org/assets/modelslib/Sample%20Models/Biology/Rabbits%20Grass%20Weeds.nlogo)

<br>

### Вербальний опис моделі:
Модель передбачає наявність трьох ключових складових у природній спільноті: трава – слугує джерелом харчування для кроликів; кролики – споживають траву як свою основну їжу; бур'ян – рослини, що можуть конкурувати з травою за ресурси, але не є основною їжею для кроликів. Ця екосистемна модель дозволяє вивчати взаємодію цих компонентів та застосовувати її для розуміння екологічних концепцій, таких як динаміка популяцій, взаємодія хижак-жертва та вплив конкуренції між рослинними видами.

### Керуючі параметри:
- **number-of-rabbits** - кількість кроликів в початковому стані середовища моделювання;
- **birth-threshold** - кількість енергії, необхідна кожному кролику для того, щоб мати можливість розмножуватися;
- **grass-grow-rate** - темп, з яким трава зростає в середовищі протягом кожного ігрового циклу;
- **grass-energ**y - кількість енергії, яку кролик отримує, споживаючи траву;
- **weeds-grow-rate** - швидкість зростання бур'яну в кожному ігровому циклі;
- **weeds-energy** - кількість енергії, яку кролик отримує, споживаючи бур'ян.

### Показники роботи моделі:
- **поточна кількість трави** - це кількість трав'янистої рослини, доступної у даний момент часу для харчування для кроликів;
- **поточна кількість бур'яну** - кількість рослин, що можуть конкурувати з травою за ресурси, яка присутня в даний момент у середовищі;
- **поточна популяція кроликів** - це кількість кроликів, які проживають в даному середовищі в даний момент.

### Примітки:
При використанні налаштувань керуючих параметрів за замовчуванням спостерігається стрімке зменшення популяції кроликів, за яким слідує помітний стрибок у популяції, після чого вона повертається до нормальних значень.

### Недоліки моделі:
Кролик рухається випадковим чином по "полю", не спрямовуючись на пошук їжі, але рухаючись випадковим чином по клітинках. Початкове значення енергії кролика є випадковим, що може вплинути на результат експерименту (наприклад, через низькі початкові значення енергії у деяких випадках популяція кроликів може досягти нуля).

<br>

## Обчислювальні експерименти

### 1. Вплив почтакової кількості кроликів на їхню подальшу популяцію

Вивчається вплив початкової кількості кроликів на середнє значення популяції кроликів протягом 500 тактів в ході симуляції. Експерименти проводяться для діапазону значень від 150 до 500 з кроком 50, загалом виконується 8 симуляцій. Інші контрольні параметри залишаються на своїх значеннях за замовчуванням:

- birth-threshold: 15
- grass-grow-rate: 15
- grass-energy: 5
- weeds-grow-rate: 0
- weeds-energy: 0

| Кролики | Середня популяція |
| :---: | :---: |
| 150	| 220 |
| 200 |	220 |
| 250 |	230 |
| 300 |	230 |
| 350 |	230 |
| 400 |	230 |
| 450 |	230 |
| 500 |	230 |

Графік нижче візуалізує останню симуляцюю, де кількість кроликів (number-of-rabbits) складає 500. З графіка видно, що початкова кількість кроликів не впливає на середню популяцію, а контрольні параметри за замовчуванням забезпечують майже сталий рівень популяції кроликів. Також для експерименту було перевірено значення number-of-rabbits = 20 і результат був ідентичний.

<img width="539" alt="image" src="https://github.com/olehni1/ksim_lab_1/assets/150624205/552944fb-8150-418c-8ad3-044d32f2a688">

<br>

