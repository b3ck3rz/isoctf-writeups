# Space Matryoshka | Stego

## Описание

> Обычная матрешка, но последняя кукла немного поломалась.


Перед нами изображение. Если открыть его через блокнот и найти в файле _Rar!_, то с уверенностью можно открывать изображение как архив, так как это RarJPEG.
Мы получаем 6 файлов, но важны нам лишь 3 из них.

Начнем с файла _«1.png»_.\
Открываем его в программе Stegsolve. В одном из цветовых каналов будет первая часть флага - **«iso{w3_»**.

![1](https://user-images.githubusercontent.com/67109334/97052581-ed3f8d00-1589-11eb-826c-6341f1ee18d3.png)

Далее файл _«2.jpg»_.\
Смотрим метадату файла, в ней будет строка текста - это кодировка ASCII.
`108 48 118 51 95 115 112 52 99 51 95`
Декодировав ее в UTF-8, мы получаем вторую часть флага - **«l0v3_sp4c3_}»**.

Осталась последняя часть флага. Обращаем внимание на файл _«hey_kitten.jpg»_. \
На картинке сказано, что ответ - это название корабля, на котором Гагарин полетел в космос, а также, что ответ в нижнем регистре. _«hey_kitten.jpg»_ тоже является RarJPEG.
Найдя ответ и введя его как пароль, мы получаем еще 3 файла, но из них нам нужен только один. 

![kitten](https://user-images.githubusercontent.com/67109334/97052740-3bed2700-158a-11eb-9cd0-0e09ef5f4d81.png)

Открываем файл _«broken.txt»_. В нем будет программа на экотерическом языке Brainfuck.

`++++++++++[>+>+++>+++++++>++++++++++<<<<-]>>>>+++++++++.<------------------.>+++++++.--.<---.-.>+.-----------.+++.<++++.>++++++++.<<+++.>>++++++++++.`

Ее вывод - последняя часть флага,**«m4tr10shk4s!}»**.

Объединяем все части и получаем цельный флаг: **iso{w3_l0v3_sp4c3_m4tr10shk4s!}**
