Console.Clear();

Console.Write("Мой господин, с удовольствием создам массив и посчитаю сумму чисел, стоящих на нечётных позициях. \nВведите колличество значений вашего массива: ");
int n = Convert.ToInt32(Console.ReadLine());
int sumnechet = 0;
int[] array = new int[n];
for (int i = 0; i < array.Length; i++)
    array[i] = new Random().Next(-50, 51);
Console.WriteLine($"Результат: [{string.Join(", ", array)}]");
for (int i = 1; i <= n; i += 2) 
    sumnechet = sumnechet + array[i];

Console.WriteLine($"Сумма чисел, стоящих на нечетных позициях: {sumnechet}");