# 10zadach
using System;

// Вариант 1: Класс «Точка»
class Point
{
    private double x, y, z;

    public Point(double x, double y, double z)
    {
        this.x = x;
        this.y = y;
        this.z = z;
    }

    public void MoveBy(double dx, double dy, double dz)
    {
        x += dx;
        y += dy;
        z += dz;
    }

    public void Display()
    {
        Console.WriteLine($"Точка: ({x}, {y}, {z})");
    }
}

// Вариант 2: Класс «Пользователь»
class User
{
    private string lastName, firstName, patronymic;
    private int age;

    public User(string lastName, string firstName, string patronymic, int age)
    {
        this.lastName = lastName;
        this.firstName = firstName;
        this.patronymic = patronymic;
        this.age = age;
    }

    public string GetFullName()
    {
        return $"{lastName} {firstName} {patronymic}";
    }

    public void Display()
    {
        Console.WriteLine($"Пользователь: {GetFullName()}, возраст: {age}");
    }
}

// Вариант 3: Класс «Персональный компьютер»
class PersonalComputer
{
    private string model;
    private double cpuFrequency;
    private int ram;
    private int storage;

    public PersonalComputer(string model, double cpuFrequency, int ram, int storage)
    {
        this.model = model;
        this.cpuFrequency = cpuFrequency;
        this.ram = ram;
        this.storage = storage;
    }

    public string Info()
    {
        return $"ПК: {model}, CPU: {cpuFrequency} ГГц, RAM: {ram} ГБ, HDD: {storage} ГБ";
    }
}

// Вариант 4: Класс «Ноутбук»
class Laptop
{
    private string model;
    private double cpuFrequency;
    private int ram;
    private int storage;
    private double weight;

    public Laptop(string model, double cpuFrequency, int ram, int storage, double weight)
    {
        this.model = model;
        this.cpuFrequency = cpuFrequency;
        this.ram = ram;
        this.storage = storage;
        this.weight = weight;
    }

    public string Info()
    {
        return $"Ноутбук: {model}, CPU: {cpuFrequency} ГГц, RAM: {ram} ГБ, HDD: {storage} ГБ, масса: {weight} кг";
    }
}

// Вариант 5: Класс «Смартфон»
class Smartphone
{
    private string model;
    private double cpuFrequency;
    private int ram;
    private int storage;
    private string os;
    private double weight;

    public Smartphone(string model, double cpuFrequency, int ram, int storage, string os, double weight)
    {
        this.model = model;
        this.cpuFrequency = cpuFrequency;
        this.ram = ram;
        this.storage = storage;
        this.os = os;
        this.weight = weight;
    }

    public string Info
    {
        get { return $"Смартфон: {model}, CPU: {cpuFrequency} ГГц, RAM: {ram} ГБ, Память: {storage} ГБ, ОС: {os}, масса: {weight} г"; }
    }
}

// Вариант 6: Класс «Прямоугольник»
class Rectangle
{
    private double x1, y1; // Левый верхний угол
    private double x2, y2; // Правый нижний угол

    public Rectangle(double x1, double y1, double x2, double y2)
    {
        this.x1 = x1;
        this.y1 = y1;
        this.x2 = x2;
        this.y2 = y2;
    }

    public double CalculatePerimeter()
    {
        double width = Math.Abs(x2 - x1);
        double height = Math.Abs(y2 - y1);
        return 2 * (width + height);
    }

    public double CalculateArea()
    {
        double width = Math.Abs(x2 - x1);
        double height = Math.Abs(y2 - y1);
        return width * height;
    }

    public void Display()
    {
        Console.WriteLine($"Прямоугольник: Периметр = {CalculatePerimeter()}, Площадь = {CalculateArea()}");
    }
}

// Вариант 7: Класс «Треугольник»
class Triangle
{
    private double a, b, c;

    public Triangle(double a, double b, double c)
    {
        this.a = a;
        this.b = b;
        this.c = c;
    }

    public double CalculatePerimeter()
    {
        return a + b + c;
    }

    public void Display()
    {
        Console.WriteLine($"Треугольник: Стороны = {a}, {b}, {c}, Периметр = {CalculatePerimeter()}");
    }
}

// Вариант 8: Класс «Почтовое отправление»
class Mail
{
    private string postalCode, city, street, house, building, apartment, message;

    public Mail(string postalCode, string city, string street, string house, string building, string apartment, string message)
    {
        this.postalCode = postalCode;
        this.city = city;
        this.street = street;
        this.house = house;
        this.building = building;
        this.apartment = apartment;
        this.message = message;
    }

    public string GetAddress()
    {
        return $"{postalCode}, {city}, ул. {street}, д. {house}, корп. {building}, кв. {apartment}";
    }

    public void Display()
    {
        Console.WriteLine($"Почтовое отправление: Адрес: {GetAddress()}, Сообщение: {message}");
    }
}

// Вариант 9: Класс «Окружность»
class Circle
{
    private double centerX, centerY, radius;

    public Circle(double centerX, double centerY, double radius)
    {
        this.centerX = centerX;
        this.centerY = centerY;
        this.radius = radius > 0 ? radius : 1;
    }

    public double CalculateCircumference()
    {
        return 2 * Math.PI * radius;
    }

    public double CalculateArea()
    {
        return Math.PI * radius * radius;
    }

    public void Display()
    {
        Console.WriteLine($"Окружность: Центр = ({centerX}, {centerY}), Радиус = {radius}, Длина = {CalculateCircumference():F2}, Площадь = {CalculateArea():F2}");
    }
}

// Вариант 10: Класс «Квадрат»
class Square
{
    private double x, y;
    private double sideLength;

    public Square(double x, double y, double sideLength)
    {
        this.x = x;
        this.y = y;
        this.sideLength = sideLength > 0 ? sideLength : 1;
    }

    public double CalculateArea()
    {
        return sideLength * sideLength;
    }

    public double CalculatePerimeter()
    {
        return 4 * sideLength;
    }

    public void Display()
    {
        Console.WriteLine($"Квадрат: Координаты = ({x}, {y}), Сторона = {sideLength}, Площадь = {CalculateArea()}, Периметр = {CalculatePerimeter()}");
    }
}

class Program
{
    static void Main(string[] args)
    {
        // Вариант 1
        Console.WriteLine("Вариант 1: Точка");
        Point point = new Point(1, 2, 3);
        point.Display();
        point.MoveBy(2, -1, 0);
        point.Display();

        // Вариант 2
        Console.WriteLine("\nВариант 2: Пользователь");
        User user = new User("Иванов", "Иван", "Иванович", 25);
        user.Display();

        // Вариант 3
        Console.WriteLine("\nВариант 3: Персональный компьютер");
        PersonalComputer pc = new PersonalComputer("Dell", 3.2, 16, 512);
        Console.WriteLine(pc.Info());

        // Вариант 4
        Console.WriteLine("\nВариант 4: Ноутбук");
        Laptop laptop = new Laptop("HP", 2.8, 8, 256, 1.5);
        Console.WriteLine(laptop.Info());

        // Вариант 5
        Console.WriteLine("\nВариант 5: Смартфон");
        Smartphone smartphone = new Smartphone("Samsung", 2.4, 4, 128, "Android", 180);
        Console.WriteLine(smartphone.Info);

        // Вариант 6
        Console.WriteLine("\nВариант 6: Прямоугольник");
        Rectangle rectangle = new Rectangle(0, 0, 4, 3);
        rectangle.Display();

        // Вариант 7
        Console.WriteLine("\nВариант 7: Треугольник");
        Triangle triangle = new Triangle(3, 4, 5);
        triangle.Display();

        // Вариант 8
        Console.WriteLine("\nВариант 8: Почтовое отправление");
        Mail mail = new Mail("123456", "Москва", "Ленина", "10", "2", "15", "Привет!");
        mail.Display();

        // Вариант 9
        Console.WriteLine("\nВариант 9: Окружность");
        Circle circle = new Circle(1, 1, 5);
        circle.Display();

        // Вариант 10
        Console.WriteLine("\nВариант 10: Квадрат");
        Square square = new Square(2, 3, 4);
        square.Display();
    }
}
