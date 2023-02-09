Console.Clear();

Console.Write("Мой господин, с удовольствием создам массив и найдиту разницу между его максимальным и минимальным элементом. \nВведите колличество значений вашего массива: ");
int n = Convert.ToInt32(Console.ReadLine());
int[] array = new int[n];
for (int i = 0; i < array.Length; i++)
    array[i] = new Random().Next(10, 101);
int max = array[0];
int min = array[0];
foreach (int element in array)
{
    if (max < element) max = element;
    if (min > element) min = element;
}
Console.WriteLine($"Максимальный элемент: {max}");
Console.WriteLine($"Минимальный элемент: {min}");
Console.WriteLine($"Разница между максимальным и минимальным: {max - min}");