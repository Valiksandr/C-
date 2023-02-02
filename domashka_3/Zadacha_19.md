Console.Clear();

Console.Write("Введите пятизначное число, для проверки на палиндромность: ");
int n = Convert.ToInt32(Console.ReadLine());

while (n < 10000 || n > 99999)
{
    Console.Write("Я же сказал, 'ПЯТИЗНАЧНОЕ'!\nВведите заново: ");
    n = Convert.ToInt32(Console.ReadLine());
}
int n1 = n / 10000;
int n4 = n /10 % 10;
int n3 = n / 100 % 10;
int n2 = n /1000 % 10;
int n5 = n % 10;


if (n5 == n1 && n4 == n2)
{
    Console.WriteLine($"Ваше число: {n} - палиндром.");
}
else 
Console.WriteLine($"Ваше число: {n} - НЕ палиндром.");