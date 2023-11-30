## LOGIC TASKS
1) Имеется 9 монеток, 8 весят одинакого, а одна или больше или меньше, чем остальные. Необходимо за минимальное количество взвешиваний на весах с двумя чашами определить эту монетку.
2) Имеется 2 комнаты, в одной выключатели в другой лампочки накаливания. В комнату с лампочками можно войти лишь раз. Как определить какой выключатель за какую лампочку отвечает?
3) 1,5 белки за 1,5 минуты поедают 1,5 жёлудя. Сколько желудей за 9 минут съедят 9 белок?



## GO TASKS
>     Сколько занимает такая структура?
> 
>     type s struct {
>         a bool
>         b uint32
>         с bool
>     }

>     А такая?
> 
>     type s struct {
>         a bool
>         b bool
>         с uint32
>     }

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














рв мутекс

две таблицы без констрейнтов 2log(n)

https://code.avito.ru/r/24c0d892-15b0-44cf-b6dc-97f844ff51e9
https://excalidraw.com/#room=90abaf37092df8be6fde,PaZkMlu3lkJEYqgOMLnx0A
