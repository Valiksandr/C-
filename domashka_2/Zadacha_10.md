Console.Clear();

Console.Write("Бонжур. Введи трехзначное число и я покажу тебе его вторую цифру: ");
int n = Convert.ToInt32(Console.ReadLine());
int n1 = n / 10;
int n2 = n1 % 10;
Console.WriteLine($"Красава! лови: {n1 % 10}");