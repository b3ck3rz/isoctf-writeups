# Strange audio from Space | Stego

## Описание

> Ученый Максим Кочанов получил странное послание из космоса. Он пытался его расшифровать, но ничего не получилось. Но там определенно что-то есть. Может ты сможешь его расшифровать?

Перед нами аудиофайл. Его стоит открыть в аудиоредакторе, например Audacity.
Смотрим спектрограмму данного файла. В спектрограмме строка в кодировке Base64.

![Спектрограмма](https://user-images.githubusercontent.com/67109334/97040240-561d0a00-1576-11eb-8c7d-a1a28b1f05a5.png)

Осталось лишь декодировать эту строку в привычный нам UTF-8.

#### Bash

 `echo 'aXNvezFzXzF0X3NwNGMzX3N0M2cwP30=' | base64 --decode`

Получаем наш флаг **iso{1s_1t_sp4c3_st3g0?}**
