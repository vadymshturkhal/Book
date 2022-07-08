## 1.5. Декомпозиция и разделение ответственности

Декомпозиция состоит из разделения задачи на подзадачи.

Рассмотрим алгоритм поиска знака последовательности. Знак последовательности равен -1 в степени количества инверсий последовательности.

Пример на `Python`:

```py
def sign_of_sequence(sequence):
    inversions_quantity = 0
    for i in range(len(sequence)):
        for j in range(i + 1, len(sequence)):
            if sequence[i] > sequence[j]:
                inversions_quantity += 1

    return (-1) ** inversions_quantity
```

Для того, чтобы решить задачу вычисления знака последовательности, необходимо решить задачу вычисления количества инверсий последовательности. Вынесем подсчёт количества инверсий в отдельную функцию:

Пример на `Python`:

```py
def count_inversions(sequence):
    inversions_quantity = 0
    for i in range(len(sequence)):
        for j in range(i + 1, len(sequence)):
            if sequence[i] > sequence[j]:
                inversions_quantity += 1
    return inversions_quantity
```

Теперь функция поиска занака последовательности имеет вид:

Пример на `Python`:

```py
def sign_of_sequence_decomposed(sequence):
    return (-1) ** count_inversions(sequence)
```

Полный алгоритм выглядит следующим образом:

Пример на `Python`:

```py
def sign_of_sequence_decomposed(sequence):
    return (-1) ** count_inversions(sequence)

def count_inversions(sequence):
    inversions_quantity = 0
    for i in range(len(sequence)):
        for j in range(i + 1, len(sequence)):
            if sequence[i] > sequence[j]:
                inversions_quantity += 1
    return inversions_quantity
```
