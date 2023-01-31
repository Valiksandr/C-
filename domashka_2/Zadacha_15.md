Console.Clear();

Console.Write("Бонжур. Введи число, обозначающую день недели, и я проверю, является ли этот день выходным: ");
int n = Convert.ToInt32(Console.ReadLine());

while (n < 1 || n > 7)
{
    Console.Write("Нет дня недели для такого числа!\nВведите новое: ");
    n = Convert.ToInt32(Console.ReadLine());
}
if (n <= 5)

    Console.Write("Будний день! Работать, негр!");
else
    Console.Write("Выходной! Может бухнем?");