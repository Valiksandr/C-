Console.Clear();

Console.Write("Введите 2 числа и я возведу первое в степень второго.\nПервое число: ");
int n = Convert.ToInt32(Console.ReadLine());
Console.Write("Отлично! \nВ какую степень возводим: ");
int m = Convert.ToInt32(Console.ReadLine());
int result = 1;
for (int i = 0; i < m; i++)
    result = result * n;
Console.Write($"{result}");