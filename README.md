# dz5-dz6
#dz5

# import random
# from re import L

# def zadacha1():
#     # Задача 1. Задайте список случайных чисел от 1 до 10, выведите все элементы больше 5.
#     #  Используйте для решения лямбда-функцию.
#     # 2, 3, 4, 6, 7, 8 -> 6, 7, 8
#     numbers = [random.randint(1, 10) for i in range(10)]
#     print(numbers)
#     result = lambda x: x > 5
#     numbers = list(filter(result, numbers))
#     print(numbers)


# def zadacga2():
#     # Задача 2. Дан список случайных чисел. Создайте список, в который попадают числа,
#     # описывающие возрастающую последовательность. Порядок элементов менять нельзя.
#     # [1, 5, 2, 3, 4, 6, 1, 7] =>[1, 2, 3] или [1, 7] или [1, 6, 7] и т.д.
#     numbers = [random.randint(1, 10) for i in range (10)]
#     print(numbers)

#     result = [0]
    
#     while len(result) < 2:
#         index = random.randint(0, 9)  # случайный индекс, с которого начнем возрастающую последовательность
#         result = [numbers[index]]
#         for i in numbers[index:]:
#             if i > result[len(result)-1]:
#                 result.append(i)    
        
#     print(result)    


# def zadacha3():
#     # Задача 3. Задайте список случайных чисел от 1 до 10. 
#     # Посчитайте, сколько всего совпадающих элементов есть в списке. Удалите все повторяющиеся элементы.
#     numbers = [random.randint(1, 10) for i in range(10)]
#     print(numbers)
#     print("Количество повторяющихся элементов ", len(list(filter(lambda x: numbers.count(x) > 1, numbers))))
#     result = []
#     for i in numbers:
#         if numbers.count(i) > 1:
#             numbers.remove(i)
#     print("Список уникальных элементов:")
#     print(numbers)


#dz6
# Задача 1. Дано натуральное число N. Найдите значение выражения:N + NN + NNN
# N может быть любой длины.
# N = 132:132 + 132132 + 132132132 = 132264396
# n = int(input("Введите число n: "))
# temp = str(n)
# t1 = temp + temp
# t2 = temp + temp + temp
# comp = n + int(t1) + int(t2)
# print("Результат равен:", comp)
# Задача 2. Задан массив из случайных цифр на 15 элементов. На вход подаётся трёхзначное натуральное число. Напишите программу, которая определяет, есть в массиве последовательность из трёх элементов, совпадающая с введённым числом.
# [0, 5, 6, 2, 7, 7, 8, 1, 1, 9] - 277 -> да
# [4, 4, 3, 6, 7, 0, 8, 5, 1, 2] - 812 -> нет
# from functools import reduce
# print(reduce(lambda acc,x: acc and (100<=abs(x)<1000),map(int,input().split()),True))
# Задача 3. Найдите все простые несократимые дроби, лежащие между 0 и 1, знаменатель которых не превышает 11.
# def farey(n, a, b, c, d):
#     if b+d <= n:
#       farey(n, a, b, a+c, b+d)
#       print(f'{a+c}/{b+d}')
#       farey(n, a+c, b+d, c, d)
 
# farey(int(input()), 0, 1, 1, 1)
