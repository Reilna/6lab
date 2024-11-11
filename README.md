# Лабораторная работа 6

## Задачи

1. Создание и запуск горутин:
   - Напишите программу, которая параллельно выполняет три функции (например, расчёт факториала, генерация случайных чисел и вычисление суммы числового ряда).
   - Каждая функция должна выполняться в своей горутине.
   - Добавьте использование time.Sleep() для имитации задержек и продемонстрируйте параллельное выполнение.
  
2. Использование каналов для передачи данных:
   - Реализуйте приложение, в котором одна горутина генерирует последовательность чисел (например, первые 10 чисел Фибоначчи) и отправляет их в канал.
   - Другая горутина должна считывать данные из канала и выводить их на экран.
   - Добавьте блокировку чтения из канала с помощью close() и объясните её роль.

3. Применение select для управления каналами:
   - Создайте две горутины, одна из которых будет генерировать случайные числа, а другая — отправлять сообщения об их чётности/нечётности.
   - Используйте конструкцию select для приёма данных из обоих каналов и вывода результатов в консоль.
   - Продемонстрируйте, как select управляет многоканальными операциями.

4. Синхронизация с помощью мьютексов:
   - Реализуйте программу, в которой несколько горутин увеличивают общую переменную-счётчик.
   - Используйте мьютексы (sync.Mutex) для предотвращения гонки данных.
   - Включите и выключите мьютексы, чтобы увидеть разницу в работе программы.

5. Разработка многопоточного калькулятора:
   - Напишите многопоточный калькулятор, который одновременно может обрабатывать запросы на выполнение простых операций (+, -, *, /).
   - Используйте каналы для отправки запросов и возврата результатов.
   - Организуйте взаимодействие между клиентскими запросами и серверной частью калькулятора с помощью горутин.

6. Создание пула воркеров:
   - Реализуйте пул воркеров, обрабатывающих задачи (например, чтение строк из файла и их реверсирование).
   - Количество воркеров задаётся пользователем.
   - Распределение задач и сбор результатов осуществляется через каналы.
   - Выведите результаты работы воркеров в итоговый файл или в консоль.
