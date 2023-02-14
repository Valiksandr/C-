Console.Clear();

Console.Write("Мой господин, готов посчитать колличество чисел больше нуля в вашем массиве. \nВведите колличество значений вашего массива: ");
int n = Convert.ToInt32(Console.ReadLine());
int[] array = new int[n];
for (int i = 0; i < n; i++)
    array[i] = Convert.ToInt32(Console.ReadLine());

Console.WriteLine($"[{string.Join(", ", array)}]");
int count = 0;
foreach (int element in array)
{
    if (element > 0)
        count = count + 1;

}
Console.WriteLine($"Чисел больше нуля в этом массиве: {count}");