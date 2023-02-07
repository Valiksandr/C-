Console.Clear();

Console.Write("Бонжур. Введи число и я покажу тебе сумму его цифр: ");
int n = Convert.ToInt32(Console.ReadLine());
int sum = 0;
if (n > 10)
{
    while (n > 0)
    {
    sum = sum + n % 10;
    n = n / 10;
    }
    Console.Write($"Сумма цифр числа: {sum}");
}
else
    Console.WriteLine($"Хватит баловаться!!! Сумма цифр числа из одной цифры равна этой цифре!: {n}");