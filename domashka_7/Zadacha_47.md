Console.Clear();

Console.WriteLine("Задайте количество строк массива:");
int m = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Задайте количество столбцов массива:");
int n = Convert.ToInt32(Console.ReadLine());
double[,] matrix = new double[m, n];

void FillArray(double[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(0); j++)
        { matrix[i, j] = Convert.ToDouble(new Random().Next(-100, 101) / 10.0); }
    }
}

void PrintArray(double[,] matrix)
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