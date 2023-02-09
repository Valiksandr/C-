Console.Clear();

Console.Write("Мой господин, с удовольствием создам массив и посчитаю колличество четных чисел среди всех значений массива. \nВведите колличество значений вашего массива: ");
int n = Convert.ToInt32(Console.ReadLine());
int countchet = 0;
int[] array = new int[n];
for (int i = 0; i < array.Length; i++)
    array[i] = new Random().Next(100, 1000);
Console.WriteLine($"Результат: [{string.Join(", ", array)}]");
foreach (int element in array)
{
    if (element % 2 == 0)
        countchet = countchet + 1;
   
}
 Console.WriteLine($"Четных: {countchet}");
 