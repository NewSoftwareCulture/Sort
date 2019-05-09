using System;

namespace Quick_sort
{
   
    class Program
    {
        static void swap(ref int a, ref int b)
        {
            int x = a;
            a = b;
            b = x;
        }
        public static void qsort(int[] items)
        {
            qs(items, 0, items.Length - 1);
        }
        static void qs(int[] items, int left, int right)
        {
            int i, j;
            int x;
            i = left; j = right;
            x = items[(left + right) / 2];
            do
            {
                while ((items[i] < x) && (i < right)) i++;
                while ((x < items[j]) && (j > left)) j--;
                if (i <= j)
                {
                    swap(ref items[i], ref items[j]);
                    i++; j--;
                }
            }
            while (i <= j);
            if (left < j) qs(items, left, j);
            if (i < right) qs(items, i, right);
        }
        static void Main(string[] args)
        {
            int[] test = { 9, 6, 7, 3, 2, 8, 6, 0, 9, 1, 4, 2, 3, };
            for (int i = 0; i < test.Length; i++)
                Console.Write(test[i] + " ");
            Console.WriteLine();
            qsort(test);
            for (int i = 0; i < test.Length; i++)
                Console.Write(test[i] + " ");
            Console.WriteLine();


        }
    }
}
