# PythonLes2
# PythonLes2
# Напишите программу, которая принимает на вход вещественное число и показывает сумму его цифр.
# Пример:
# 0,56 -> 11

n=float(input('Введите число '))
n=n*1000
s=0
while n>0:
    last=n%10
    s=s+last
    n=n//10
    print(n, last, s)

# Напишите программу, которая принимает на вход число N и выдает набор произведений чисел от 1 до N.
# Пример:
# пусть N = 4, тогда [ 1, 2, 6, 24 ] (1, 1*2, 1*2*3, 1*2*3*4)

print('Введите число');
n = int (input())
pr=1
for el in range(1,n+1):
    pr=pr*el
    print(pr)

# Задайте список из n чисел последовательности (1 + 1/n)^n и выведите на экран их сумму.
# Пример:
# Для n=4 {1: 2, 2: 2.25, 3: 2.37, 4: 2.44} Сумма 9.06

print('Введите число');
n = int (input())
pr=1
for el in range(1,n+1):
    pr=((1+1/el)**el)
    print(pr)

# Задайте список из N элементов, заполненных числами из промежутка [-N, N].
# Найдите произведение элементов на указанных индексах. Индексы вводятся одной строкой, через пробел.
# n = 3
# [-3, -2, -1, 0, 1, 2, 3]
# --> 0 2 3
# -3 * -1 * 0 = 0
# Вывод: 0

lt=[]
lt1=[]
a=int(input('Введите число '))
for i in range(0,a):
    lt.append(i-a)
for i in range(0,a+1):
    lt1.append(i)
lts=lt+lt1
print('Список ', lts)
q, w, e=map(int,input('Введите три индекса через пробел ').split())
sum=lts[q]*lts[w]*lts[e]
print('Произведение элементов ', sum)

# Реализуйте алгоритм перемешивания списка

import random


lt=[]
lt1=[]
a=int(input('Введите число '))
for i in range(0,a):
    lt.append(i-a)
for i in range(0,a+1):
    lt1.append(i)
lts=lt+lt1
print('Список ', lts)
lt=lts
ltLength=len(lt)
for i in range(ltLength):
    iRan = random.randint(0, ltLength-1)
    count=lt[i]
    lt[i]=lt[iRan]
    lt[iRan]=count
print(lt)
