Console.Clear();

Console.Write("Напишу все чётные от 1 до: ");
int n = int.Parse(Console.ReadLine());
for (int i = 2; i <= n; i += 2) 
    Console.WriteLine(i);