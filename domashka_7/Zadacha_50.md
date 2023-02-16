Console.Clear();

Console.WriteLine("Задайте количество строк массива:");
int n = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Задайте количество столбцов массива:");
int m = Convert.ToInt32(Console.ReadLine());
int[,] matrix = new int[n, m];

void FillArray(Int32[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(0); j++)
        { matrix[i, j] = Convert.ToInt32(new Random().Next(0, 101)); }
    }
}

void PrintArray(int[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            Console.Write($"{matrix[i, j]} \t");
        Console.WriteLine();
    }
}

FillArray(matrix);
Console.WriteLine();
PrintArray(matrix);

Console.WriteLine("Задайте координат строки:");
int x = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Задайте координат столбца:");
int y = Convert.ToInt32(Console.ReadLine());

if (x > n || y > m)
    Console.WriteLine("Такого значения нет в массиве.");
    
Console.WriteLine($"Ваша цифра:{matrix[x-1, y-1 ]}");