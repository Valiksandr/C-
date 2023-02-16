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
        for (int j = 0; j < matrix.GetLength(1); j++)
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

void SredneArifStolb(int[,] matrix)
{
    for (int j = 0; j < matrix.GetLength(1); j++)
{
    double sum = 0; 
    double sas = 0;
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        sum = (sum + matrix[i, j]);
    }
    sas = Math.Round(sum / n, 1);
    Console.Write($"[{string.Join(", ", sas)}] \t");
    }
}

FillArray(matrix);
Console.WriteLine();
PrintArray(matrix);
Console.WriteLine();
Console.WriteLine("И вот срежднее арифметическое элементов в каждом столбце.:");
Console.WriteLine();
SredneArifStolb(matrix);