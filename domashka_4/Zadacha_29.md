Console.Clear();

Console.Write("Я готов посчитать, сколько раз встречается необходимая вам цифра среди всех значений массива. \nВведите колличество значений вашего массива: ");
int n = Convert.ToInt32(Console.ReadLine());
Console.Write("Введите цифру, которую мы будем отслеживать: ");
int x = Convert.ToInt32(Console.ReadLine());
int count = 0;
int[] array = new int[n];
for (int i = 0; i < array.Length; i++)
    array[i] = new Random().Next(0, 11); 

Console.WriteLine($"Результат: [{string.Join(", ", array)}]");
for (int i = 0; i < array.Length; i++)
    if (array[i] == x)
        count = count + 1;

if (count < 2 || count > 4)
    Console.WriteLine($"Цифра {x} встречается {count} раз");
else if (count > 1 & count < 4)
    Console.WriteLine($"Цифра {x} встречается {count} раза");