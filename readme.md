## LOGIC TASKS
1) Имеется 9 монеток, 8 весят одинакого, а одна или больше или меньше, чем остальные. Необходимо за минимальное количество взвешиваний на весах с двумя чашами определить эту монетку.
    <details>
        <summary>Ответ</summary>
        
        Взвешиваем кучками по 3 и гарантированно за 2 взвешивания определяем монетку.
    </details>

2) Имеется 2 комнаты, в одной выключатели в другой лампочки накаливания. В комнату с лампочками можно войти лишь раз. Как определить какой выключатель за какую лампочку отвечает?
    <details>
        <summary>Ответ</summary>
        
        Включаем один выключатель и ждём минут 5. Выключаем и включаем любой другой выключатель.
        Идём в комнату с лампочками и находим теплую лампочку - это лампочка от первого включённого выключателя.
        Горящая лампочка - это лампочка от текущего включённого выключателя. Оставшуюся пару определяем исключением.
    </details>

3) 1,5 белки за 1,5 минуты поедают 1,5 жёлудя. Сколько желудей за 9 минут съедят 9 белок?
    <details>
        <summary>Ответ</summary>
        
        1 белка за теже 1,5 минуты съест 1 жёлудь.
        1 белка за 9 минут съест 6 желудей.
        9 белок за 9 минут съедят 54 жёлудя.
    </details>

## GO TASKS
    Сколько места занимает каждая из структур и почему?

    type s struct {
        a bool
        b uint32
        с bool
    }

    type s struct {
        a bool
        b bool
        с uint32
    }
>
    Что выведет программа и сколько времени будет работать?
    Как её можно ускорить?

    package main

    import (
        "fmt"
        "time"
    )

    const numRequests = 10000

    var count int

    func networkRequest() {
        time.Sleep(time.Millisecond) // Эмуляция сетевого запроса
        count++
    }

    func main() {
        for i := 0; i < numRequests; i++ {
            networkRequest()
        }
        fmt.Println(count)
    }
>
    Есть функция getWeather, которая через нейронную сеть вычисляет температуру за ~1 секунду
    Есть highload ручка /weather/highload с нагрузкой 3-5k RPS
    Необходимо реализовать код этой ручки

    func getWeather() int {
        time.Sleep(1 * time.Second)
        return rand.Intn(70) - 30
    }

    func main() {
        http.HandleFunc("/weather/highload", func(resp http.ResponseWriter, req *http.Request) {

        })
    }

- рв мутекс
- https://code.avito.ru/r/24c0d892-15b0-44cf-b6dc-97f844ff51e9

## DESIGN TASKS
- https://excalidraw.com/#room=90abaf37092df8be6fde,PaZkMlu3lkJEYqgOMLnx0A

## SQL TASKS
- две таблицы без констрейнтов 2log(n)

