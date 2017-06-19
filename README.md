using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Exam_Four
{
    class Program
    {
        static void Main(string[] args)
        {
            int stadiumCapacity = int.Parse(Console.ReadLine());
            double fans = int.Parse(Console.ReadLine());

            double sectorA = 0;
            double sectorG = 0;
            double sectorB = 0;
            double sectorV = 0;

            for (int i = 0; i < fans; i++)
            {
                string sector = Console.ReadLine().ToLower();
                if (sector == "a")
                {
                    sectorA++; 
                }
                else if (sector == "b")
                {
                    sectorB++;
                }
                else if (sector == "v")
                {
                    sectorV++;
                }
                else if (sector == "g")
                {
                    sectorG++;
                }
            }

            double percentageA = (sectorA / fans) * 100;
            double percentageB = (sectorB / fans) * 100;
            double percentageV = (sectorV / fans) * 100;
            double percentageG = (sectorG / fans) * 100;
            double percentageFans = (fans / stadiumCapacity) * 100;

            Console.WriteLine("{0:f2}%", percentageA);
            Console.WriteLine("{0:f2}%", percentageB);
            Console.WriteLine("{0:f2}%", percentageV);
            Console.WriteLine("{0:f2}%", percentageG);
            Console.WriteLine("{0:f2}%", percentageFans);
        }
    }
}
