# Программа для вычисления суммы элементов массива
Данная программа на языке C# вычисляет сумму элементов массива, расположенных между минимальным и максимальным элементами.

![scale_1200](https://github.com/JLIM0N4IK/JLIMON4IK/assets/129604382/df60589c-1bf2-4610-adeb-b849a3551ff7)



https://github.com/JLIM0N4IK/JLIMON4IK/blob/main/1663139110_24-mykaleidoscope-ru-p-zloi-shrek-krasivo-28.jpg
## Описание программы
![image](https://github.com/JLIM0N4IK/JLIMON4IK/assets/129604382/dd374bd6-7b3a-4621-824b-65c4c77852c3)

1. Создается массив размером 10 элементов и заполняется случайными числами.
2. Выводится массив на экран.
3. Находятся индексы минимального и максимального элементов в массиве.
4. Вычисляется сумма элементов между минимальным и максимальным элементами, используя найденные индексы.
5. Результат выводится на экран.

## Использование программы


![GX4EyOpyyp4](https://github.com/JLIM0N4IK/JLIMON4IK/assets/129604382/245011e7-ec58-4e5e-8bb9-69d6d143813a)





    using System;
    class Program
    {
    static void Main()
    {
        // Создаем массив и заполняем его случайными числами
        int[] array = new int[10];
        Random random = new Random();
        for (int i = 0; i < array.Length; i++)
        {
            array[i] = random.Next(100);
        }
        // Выводим массив на экран
        Console.WriteLine("Массив:");
        foreach (int element in array)
        {
            Console.Write(element + " ");
        }
        Console.WriteLine();
        // Находим индексы минимального и максимального элементов
        int minIndex = 0;
        int maxIndex = 0;
        for (int i = 1; i < array.Length; i++)
        {
            if (array[i] < array[minIndex])
            {
                minIndex = i;
            }
            if (array[i] > array[maxIndex])
            {
                maxIndex = i;
            }
        }
        // Вычисляем сумму элементов между минимальным и максимальным элементами
        int sum = 0;
        int startIndex = Math.Min(minIndex, maxIndex) + 1;
        int endIndex = Math.Max(minIndex, maxIndex);
        for (int i = startIndex; i < endIndex; i++)
        {
            sum += array[i];
        }
        // Выводим результат на экран
        Console.WriteLine("Сумма элементов между минимальным и максимальным элементами: " + sum);
    }
    }

1. Скомпилируйте программу с использованием компилятора C#.
2. Запустите скомпилированную программу.
3. На экране появится массив случайных чисел и сумма элементов между минимальным и максимальным элементами.

Ссылка на дополнительные ресурсы: https://www.youtube.com/watch?v=widVd98BGrI
