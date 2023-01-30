Console.Clear();

Console.Write("Бонжур. Введи число и я определю, четное оно или нет: ");
int n = Convert.ToInt32(Console.ReadLine());
if (n % 2 == 0)
    Console.Write("Четное!");
else Console.WriteLine("Нечетное!");