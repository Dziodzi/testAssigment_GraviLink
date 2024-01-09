# Тестовое задание для GraviLink

## Система координат
В огромном офисе компании GraviLink кабинет Матвея находится на координатах (13, -1, 42), а кабинет Дениса – на координатах (7, 0, 3). Найдите координаты кабинета Дениса в системе отсчёта кабинета Матвея.

Полученные координаты введите через запятую.

Пример ответа: "1, -2, 4" без кавычек

### Ответ: 
> -6, 1, -39

## Многочлен Талгата
Талгату на день рождения подарили многочлен. Многочлен ему понравился, поэтому он записал его производную и значение в точке 0 на листочек. На следующее утро Талгат забыл свой любимый многочлен, из-за чего очень расстроился. Можно ли по имеющейся информации помочь Талгату восстановить многочлен?

Пусть p(x) — многочлен Талгата.
p'(x) = 12 * x ^ 3 + 18 * x ^ 2 + 4 * x + 4, p(0) = 5

Если многочлен восстановить невозможно, введите в качестве ответа одно слово "Нет" без кавычек.
Если возможно — в качестве ответа введите коэфициенты многочлена через запятую в порядке уменьшения степени.

Например, если вы получили в качестве ответа 5 * x ^ 3 + x ^ 2 + 2 * x + 1, введите "5, 1, 2, 1" без кавычек.

### Ответ: 
> 3, 6, 2, 4, 5

## Две копилки
У Максима дома есть две одинаковые свиньи-копилки. Каждый раз, возвращаясь после магазина, он кладет одну монетку из сдачи в одну из копилок (равновероятно – его младшие сестры постоянно их переставляют местами), а оставшиеся отдает маме. В копилку может поместиться N монет. Изначально копилки пустые. Какова вероятность того, что в момент заполнения одной из копилок, в другой будет ровно K монет? Выведите формулу для произвольных N и K.

В качестве ответа напишите два числа через запятую: сначала ответ при n = 10, k = 5, затем при n = 15, k = 7. Ответы округлите до трёх знаков после запятой.
Например, если вы получили в качестве ответа при n = 10, k = 5 число 0.1278, а при n = 15, k = 7 число 0.78912, то в ответ нужно записать "0.128, 0.789" без кавычек.

### Код решения:
[Moneyboxes.java](https://github.com/Dziodzi/testAssigment_Gravilink/blob/master/src/main/java/org/example/Moneyboxes.java)

### Ответ: 
> 0.022, 0.001

## Лесенки
Дениса попросили написать функцию на языке программирования С#, которая будет считать количество подмассивов вида [1, 2, ..., А] для заданного массива и значения А. Переутомившись к концу рабочего дня, Денис написал следующий код:

    static int Stairs(List<int> nums, int A)
    {
      int answer = 0;
      int n = nums.Count;

      for (int i = 0; i < n; ++i)
      {
          for (int j = i; j < n; ++j)
          {
              if (nums[j] != j - i + 1)
              {
                  if (j - i == A)
                  {
                      answer++;
                  }
                  break;
              }
          }
      }

      return answer;
    }

Определите асимптотическую сложность решения Дениса.

### Ответ: 
> O(n^2)

## Лесенки, тесты
В программе Дениса есть логическая ошибка. Исправьте ее, и запустите на двух предложенных тестах: 
1. 4_1.txt
2. 4_2,txt

### Формат тестов:
В первой строке дается число n — размер массива nums. Во второй строке дано число A. В третьей строке через пробелы перечисленны числа — элементы массива nums.

В качестве ответа введите два числа — ответы на два теста. Ответы следует вводить через запятую. Сначала ответ на тест 4.1, затем на тест 4.2. 
Пример ответа: "100, 10" без кавычек.

### Код решения:
[Ladders.java](https://github.com/Dziodzi/testAssigment_Gravilink/blob/master/src/main/java/org/example/Ladders.java)

### Ответ: 
> 14, 3396

## График
Диме дали следующую задачу. Дана кусочно-линейная функция, заданная целочисленными точками `(x_i, y_i)`. Чтобы получить график функции необходимо соединить соседние по х координате точки. Необходимо определить, можно ли сдвинуть оси параллельным переносом (т.е `x’ = x + C1; y’ = y + C2`) так, чтобы эта заданная ломаная стала четной функцией в новой системе координат.

Для этого требуется реализовать функцию со следующей сигнатурой:
`static bool Solve(List<(int, int)> points)`

На вход подается массив попарно различных точек. Необходимо вернуть ответ на вопрос о существовании описанного преобразования.

Для проверки вашего решения, запустите его на следующих двух тестах:

1. 5_1.txt
2. 5_2.txt

### Формат тестов:
В первой строке дается число n — размер массива points.
В следующих n строках дан массив points. В каждой строке находится два числа через пробел — координаты точки.

В качестве ответа введите две цифры 0 или 1 через запятую, где 0 соответсвует false, 1 соответствует true — результат возращенный функцией на соответствующем тесте.
Например, если на тесте 5.1 вы получили ответ false и на 5.2 тоже false — введите в качестве ответа "0, 0" без кавычек.

### Код решения:
[Coordinates.java](https://github.com/Dziodzi/testAssigment_Gravilink/blob/master/src/main/java/org/example/Coordinates.java)

### Ответ: 
> 0, 1
