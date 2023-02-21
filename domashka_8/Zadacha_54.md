void Fillmatrix(double[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
        { matrix[i, j] = Convert.ToDouble(new Random().Next(-10, 101)); }
    }
}

void Printmatrix(double[,] matrix)
{
    for (int i = 0; i < matrix.GetLength(0); i++)
    {
        for (int j = 0; j < matrix.GetLength(1); j++)
            Console.Write($"[{matrix[i, j]}] \t");
        Console.WriteLine();
    }
}

void Sortmatrix(double[,] matrix)
{
  for (int i = 0; i < matrix.GetLength(0); i++)
  {
    for (int j = 0; j < matrix.GetLength(1); j++)
    {
      for (int k = 0; k < matrix.GetLength(1) - 1; k++)
      {
        if (matrix[i, k] < matrix[i, k + 1])
        {
          double temp = matrix[i, k + 1];
          matrix[i, k + 1] = matrix[i, k];
          matrix[i, k] = temp;
        }
      }
    }
  }
}

Console.Clear();

Console.WriteLine("Задайте количество строк массива:");
int m = Convert.ToInt32(Console.ReadLine());
Console.WriteLine("Задайте количество столбцов массива:");
int n = Convert.ToInt32(Console.ReadLine());
double[,] matrix = new double[m, n];

Fillmatrix(matrix);
Console.WriteLine();
Printmatrix(matrix);
Sortmatrix(matrix);
Console.WriteLine("Конечный массив:");
Printmatrix(matrix);