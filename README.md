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

Вивчається вплив початкової кількості кроликів на середнє значення популяції кроликів протягом 500 тактів в ході симуляції. Експерименти проводяться для діапазону значень від 150 до 500 з кроком 50, загалом виконується 8 симуляцій. Інші контрольні параметри залишаються за замовчуванням:

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

### 2. Вплив енергії на популяцію кроликів

Вивчається залежність середнього значення популяції кроликів протягом 500 тактів від енергії, яку отримує кролик від споживання трави. Експерименти проводяться для діапазону значень від 1 до 5 з кроком 0.5, загалом виконується 9 симуляцій. Інші управляючі параметри залишаються за замовчуванням:

- birth-threshold: 15
- grass-grow-rate: 15
- grass-energy: 5
- weeds-grow-rate: 0
- weeds-energy: 0

| Енергія | Середня популяція |
| :---: | :---: |
| 1	| 20(0) |
| 1.5 |	48 |
| 2 |	68 |
| 2.5 |	99 |
| 3 |	130 |
| 3.5 |	148 |
| 4 |	175 |
| 4.5 |	208 |
| 5 |	230 |

**grass-energy = 1**:

<img width="540" alt="image" src="https://github.com/olehni1/ksim_lab_1/assets/150624205/10f79b5f-8419-4b39-b56a-2e6af9ad0f23"><img width="539" alt="image" src="https://github.com/olehni1/ksim_lab_1/assets/150624205/443e1612-dcd6-4de3-9617-ebab59d5fcf4">

<br>

**grass-energy=2**:

<img width="539" alt="image" src="https://github.com/olehni1/ksim_lab_1/assets/150624205/f9336599-d89d-4125-ab04-550e6dc97d0f">

<br>

**grass-energy=5**:

<img width="536" alt="image" src="https://github.com/olehni1/ksim_lab_1/assets/150624205/b14c5574-deb3-456a-845d-17d23bef0fe7">

<br>

Представлені графіки вказують на пряму залежність середньої популяції кроликів від енергії, яку вони отримують від трави. Зв'язок є майже лінійним, за умови врахування лише даних даного експерименту. Також цікавим фактом є те, що при grass-energy = 1 у деяких випадках популяція кроликів припиняла зростання. Це може бути викликане недоліками поточної моделі: кролики не активно "шукають" їжу, а випадково переміщуються по полю.

### 3. Вплив бурʼяну на популяцію

У моделі "Rabbits Grass Weeds" бур'яни зазвичай визначаються як рослини, які здатні конкурувати з травою за ресурси, проте не є основною їжею для кроликів. Ці рослини часто вважаються небажаними в екосистемі і можуть впливати на ріст як трави, так і інших видів рослин. Проте, в реалізації поточної моделі віддається перевага траві. Це означає, що якщо для певної клітини виконуються умови для зростання і трави, і бур'яну, то саме трава буде зростати у цій клітині.

<pre>
to grow-grass-and-weeds
  ask patches [
    if pcolor = black [
      if random-float 1000 < weeds-grow-rate
        [ set pcolor violet ]
      if random-float 1000 < grass-grow-rate
        [ set pcolor green ]
    ]
  ]
end
</pre>

Внесемо зміни в код для зворотнього ефекту, імітуючи негативний вплив бур'яну на зріст трави.

<pre>
to grow-grass-and-weeds
  ask patches [
    if pcolor = black or pcolor = green [
      if random-float 1000 < grass-grow-rate
        [ set pcolor green ]
      if random-float 1000 < weeds-grow-rate
        [ set pcolor violet ]
    ]
  ]
end
</pre>

Вивчається негативний вплив бурʼяну на середню популяцію кроликів протягом 500 тактів. Експерименти проводяться для значень від 0 до 20 з кроком 2, в загальній складності 10 симуляцій. Для кращого зрозуміння скоротимо значення grass-grow-rate до 10. Інші основні параметри залишаються за замовчуванням.

- number-of-rabbits: 150
- birth-threshold: 15
- grass-grow-rate: 10
- grass-energy: 5
- weeds-energy: 0

| Темп росту бурʼяну |	Середня популяція |
| :---: | :---: |
| 0 |	160 |
| 2	|	146 |
| 4	|	136 |
| 6	|	131 |
| 8	|	116 |
| 10 | 106 |
| 12 | 98 |
| 14 | 85 |
| 16 | 72 |
| 18 | 48 |
| 20 | 0 |

