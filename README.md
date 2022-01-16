# lesson..2..python

1.
print(15 * 3)
print(15 / 3)
print(15 // 2)
print(15 ** 2)


2.
def get_sign(x):
    if x[0] in '+-':
        return x[0]

arr = ['в', '5', 'часов', '17', 'минут', 'температура', 'воздуха', 'была', '+5', 'градусов']

i = 0
while i < len(arr):
    sign = get_sign(arr[i])
    if arr[i].isdigit() or (sign and arr[i][1:].isdigit()):
        if sign:
            arr[i] = sign + arr[i][1:].zfill(2)
        else:
            arr[i] = arr[i].zfill(2)

        arr.insert(i, '"')
        arr.insert(i + 2, '"')
        i += 2

    i += 1

print(arr)

print("в '05' часов '17' минут температура воздуха была '+05' градусов")


4.
arr = ['инженер-конструктор Игорь', 'главный бухгалтер МАРИНА', 'токарь высшего разряда нИКОЛАй', 'директор аэлита']
for i in range(len(arr)):
    arr[i].islower()
last_len = len(arr)

for i in range(len(arr)):
    temporary_list = arr[i].split(" ")
    hm_indexes = len(temporary_list) -1
    temporary_name = temporary_list[hm_indexes]
    name = temporary_name.lower().title()
    arr.append(name)

print(arr)
for words in arr.copy():
    print(words)
    arr.remove(words)
    
    
5.
one_minute = 100
one_hour = 1000
duration = int (input('Укажите продолжительность в секундах: '))
if duration<one_minute:
    print ('{} k'.format(duration))
elif one_minute <= duration and one_hour > duration:
    my_minute=duration//one_minute
    my_second=duration%one_minute
    print ('{} r {} k'.format(my_minute,my_second));
