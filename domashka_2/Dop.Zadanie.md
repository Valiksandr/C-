Console.Clear();
int n = Convert.ToInt32(Console.ReadLine());
int max1 = n, max2 = -1000;
while (n != 0)
{
    n = Convert.ToInt32(Console.ReadLine());
    if (n > max1)
    {
        max2 = max1;
        max1 = n;
    }
    else if (n > max2)
    {
        max2 = n;
    }
}
Console.WriteLine(max2);