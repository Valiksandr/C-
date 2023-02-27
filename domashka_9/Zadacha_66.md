int CalcSumm(int m, int n)
		{
			int start = m;
			int end = n;
			if(m > n)
			{
				start = n;
				end = m;
			}
			return (end + start)*(end - start + 1)/2; 
		}
		
		
Console.Clear();
Console.Write("Задайте значения M и N и я найду сумму натуральных элементов в промежутке от M до N. \nВведите 1-ое число: : ");
int m = Convert.ToInt32(Console.ReadLine());
Console.Write("Введите 2-ое число: ");
int n = Convert.ToInt32(Console.ReadLine());
Console.WriteLine(CalcSumm(m, n));
