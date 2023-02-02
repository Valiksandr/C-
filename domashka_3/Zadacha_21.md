Console.Clear();

Console.Write("Посчитаем длину вектора в 3D пространстве.\nВведите координату X1: ");
double x1 = Convert.ToDouble(Console.ReadLine());
Console.Write("Введите координату Y1: ");
double y1 = Convert.ToDouble(Console.ReadLine());
Console.Write("Введите координату z1: ");
double z1 = Convert.ToDouble(Console.ReadLine());
Console.Write("Введите координату X2: ");
double x2 = Convert.ToDouble(Console.ReadLine());
Console.Write("Введите координату Y2: ");
double y2 = Convert.ToDouble(Console.ReadLine());
Console.Write("Введите координату X2: ");
double z2 = Convert.ToDouble(Console.ReadLine());
double l = Math.Round(Math.Sqrt(Math.Pow(x2 - x1, 2) + Math.Pow(y2 - y1, 2)+Math.Pow(y2 - y1, 2)), 2);
Console.WriteLine($"Расстояние между точками: {l}");
