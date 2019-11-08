# Start-cars
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;

namespace WebApplication2.Models
{
    public class CarInformationApplication
    {
        class Program
        {
            class Car
            {
                public string CarID;
                public string CarName;
                public string CarLogo;
                public string Run;
                enum run { start=1, stop};
                public void Runed()
                {
                    Random r1 = new Random();
                    int a = r1.Next(1, 2);
                    Run = ((run)a).ToString();
                }

                public void PrintOne()
                {
                    Console.WriteLine("{0},{1},{2},{3}", CarID, CarName, CarLogo, Run);
                }
                public Car()
                { }
                public Car(string ID,string carname)
                {
                    CarID = ID;
                    CarName = carname;
                }
                public Car(string ID, String carname, string carlogo)
                {
                    CarID = ID;
                    CarName = carname;
                    CarLogo = carlogo;
                }
                static void Main(string[] args)
                {
                    Car c1 = new Car();
                    c1.CarID = "198701";
                    c1.CarName = "Altima";
                    c1.CarLogo = "Nissan";
                    c1.Runed();
                    c1.PrintOne();
                    Car c2 = new Car("199004", "Sarah", "Toyota");
                    c2.Runed();
                    c2.PrintOne();
                    Car c3 = new Car("201310", "Tyler", "Toyota");
                    c3.Runed();
                    c3.PrintOne();
                    Console.ReadLine();
                }
            }
        }
    }
}
