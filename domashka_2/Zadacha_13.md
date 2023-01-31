Console.Clear();

Console.Write("Бонжур. Введи число и я покажу тебе его третью цифру: ");
int n = Convert.ToInt32(Console.ReadLine());
    if (n >= 100)
    {
    while (n > 1000) n /= 10;
    int k = n % 10;
    Console.Write(k);
    }
else
    Console.Write("Хватит баловаться!!! Тут нет третьей цифры!");