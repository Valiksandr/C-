Console.Clear();

Console.Write("Введите число и я напишу таблицу кубов чисел от 1 до вашего значения: ");
int n = Convert.ToInt32(Console.ReadLine()), i = 1;
while (i <= n)
{
    Console.Write($"{i * i * i} ");
    i++;