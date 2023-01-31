Console.Clear();

Console.Write("Бонжур. Введи число, обозначающую день недели, и я проверю, является ли этот день выходным: ");
int n = Convert.ToInt32(Console.ReadLine());

while (n < 1 || n > 7)
{
    Console.Write("Вы ошиблись!\nВведите число: ");
    n = Convert.ToInt32(Console.ReadLine());
}
if (n <= 7)

    if (n <= 5)

        Console.Write("Будний день! Работать, негр!");
    else
        Console.Write("Выходной! Может бухнем?");

else
    Console.Write("Хватит баловаться! Дня недели для такой цифры нет!");