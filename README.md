using System;

class Vehicle
{
    public string Brand { get; set; }
    public int Year { get; set; }

    public Vehicle(string brand, int year)
    {
        Brand = brand;
        Year = year;
    }

    public void Start()
    {
        Console.WriteLine($"{Year} {Brand} is starting...");
    }
}

class Car : Vehicle
{
    public int NumberOfDoors { get; set; }

    public Car(string brand, int year, int numberOfDoors) : base(brand, year)
    {
        NumberOfDoors = numberOfDoors;
    }
}

class Bus : Vehicle
{
    public int Capacity { get; set; }

    public Bus(string brand, int year, int capacity) : base(brand, year)
    {
        Capacity = capacity;
    }
}

class Motorcycle : Vehicle
{
    public bool HasSidecar { get; set; }

    public Motorcycle(string brand, int year, bool hasSidecar) : base(brand, year)
    {
        HasSidecar = hasSidecar;
    }
}

class Program
{
    static void Main(string[] args)
    {
        Car myCar = new Car("Toyota", 2022, 4);
        Bus myBus = new Bus("Volvo", 2020, 50);
        Motorcycle myBike = new Motorcycle("Harley", 2021, false);

        myCar.Start();
        myBus.Start();
        myBike.Start();

       
    }
}# Vehicle-Hierarchy