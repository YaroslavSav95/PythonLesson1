# PythonLesson1
print('Введите число от 1 до 7');
a = int (input())
if a<6:
   print('Будни')
else:
   print('Выходной')

# Напишите программу для проверки истинности утверждения ¬(X ⋁ Y ⋁ Z) = ¬X ⋀ ¬Y ⋀ ¬Z для всех значений предикат.

for x in [True,False]:
    for y in [True,False]:
        for z in [True,False]:
            print(not (x or y or z) == (not x and not y and not z))
            print (x,y,z)

# Напишите программу, которая принимает на вход координаты точки (X и Y), причём X ≠ 0 и Y ≠ 0 и выдаёт номер четверти плоскости, в которой находится

print('Введите число X');
x = int (input())
print('Введите число Y');
y = int (input())
if (x>0) and (y>0):
    print('Первая')
elif (x<0) and (y>0):
    print('вторая')
elif (x<0) and (y<0):
    print('третья')
elif (x>0) and (y<0):
    print('четвёртая')

# Напишите программу, которая по заданному номеру четверти, показывает диапазон возможных координат точек в этой четверти (x и y).

print('Введите число');
a = int (input())
if a==1:
    print('X = 0 -> 1, Y = 0 -> 1 ')
elif a==2:
    print('X = 0 -> -1, Y = 0 -> 1 ')
elif a==3:
    print('X = 0 -> -1, Y = 0 -> -1 ')
elif a==4:
    print('X = 0 -> 1, Y = 0 -> -1 ')

# Напишите программу, которая принимает на вход координаты двух точек и находит расстояние между ними в 2D пространстве.

print('Введите координаты X');
x1, x2 = float(input()), float(input())
print('Введите координаты Y');
y1, y2 = float(input()), float(input())
c=(((x2-x1)**2)+((y2-y1)**2))**0.5
print(c)