Console.Clear();
Console.WriteLine("Задайте квадратную матрицу [число строк равно числу столбцов] и я заполню её спирально:");
int n = Convert.ToInt32(Console.ReadLine());

int[,] Hurricane = new int[n, n];

int count = 1;
int i = 0;
int j = 0;

while (count <= Hurricane.GetLength(0) * Hurricane.GetLength(1))
{
  Hurricane[i, j] = count;
  count++;
  if (i <= j + 1 && i + j < Hurricane.GetLength(1) - 1)
    j++;
  else if (i < j && i + j >= Hurricane.GetLength(0) - 1)
    i++;
  else if (i >= j && i + j > Hurricane.GetLength(1) - 1)
    j--;
  else
    i--;
}
void PrintMatrix (int[,] Hurricane)
{
  for (int i = 0; i < Hurricane.GetLength(0); i++)
  {
    for (int j = 0; j < Hurricane.GetLength(1); j++)
    {
      if (Hurricane[i,j] / 10 <= 0)
      Console.Write($" [{Hurricane[i,j]}] ");

      else Console.Write($"[{Hurricane[i,j]}] ");
    }
    Console.WriteLine();
  }
}

PrintMatrix(Hurricane);