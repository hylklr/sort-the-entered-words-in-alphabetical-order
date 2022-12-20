# sort-the-entered-words-in-alphabetical-order
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp1
{
    internal class Program
    {
        static void Main(string[] args)
        {
            int adet;
            Console.Write("Girilecek Veri Adeti : ");
            adet = Convert.ToInt16(Console.ReadLine());
            Console.WriteLine("sayı yada isim giriniz: ");
            Console.WriteLine("*---------------------------------------*");
            string[] liste = new string[adet];
            string isim;

            for (int i = 0; i < adet; i++)
            {
                Console.Write(i + 1 + ". İsmi veya sayıyı giriniz: ");
                isim = Console.ReadLine();
                liste[i] = isim;
            }

            Console.WriteLine();
            Console.WriteLine("Sıralamadan önce liste:");
            Console.WriteLine("*---------------------------------------*");


            foreach (string eleman in liste)
            {
                Console.WriteLine(eleman);
            
            
            }
            Array.Sort(liste);
            Console.WriteLine();
            Console.WriteLine("A-Z Sıralama || Sıralamada ilk sayıdan başlayıp sıralama :");
            Console.WriteLine("*---------------------------------------*");

            foreach (string eleman in liste)
            {
                Console.WriteLine(eleman);
            }
            Console.WriteLine();
            Array.Reverse(liste);
            Console.WriteLine("Z-A Sıralama || sıralamada son sayıdan başlayıp sıralama: ");
            Console.WriteLine("*---------------------------------------*");

            foreach (string eleman in liste)
            {
                Console.WriteLine(eleman);
            }

            Console.ReadKey();
        }

    }

}
