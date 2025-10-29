# 2ntvf
using System;

namespace Practice
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Сумма чисел: " + Sum(5, 3));

            int number = 10;
            CheckNumber(number);
            User user1 = new User();
            user1.Id = 1;
            user1.Name = "Иван";
            user1.Email = "ivan@mail.ru";
            user1.Age = 25;

            user1.PrintInfo();

            User user2 = new User
            {
                Id = 2,
                Name = "Мария",
                Email = "maria@yandex.ru",
                Age = 22
            };

            Console.WriteLine(user2.GetUserData());
        }

        public static int Sum(int a, int b)
        {
            return a + b;
        }
        private static void CheckNumber(int num)
        {
            if (num > 0)
                Console.WriteLine("Число положительное");
            else if (num < 0)
                Console.WriteLine("Число отрицательное");
            else
                Console.WriteLine("Число равно нулю");
        }
    }

    public class User
    {
        public int Id { get; set; }
        public string Name { get; set; }
        public string Email { get; set; }
        public int Age { get; set; }

        public void PrintInfo()
        {
            Console.WriteLine($"ID: {Id}, Имя: {Name}, Email: {Email}, Возраст: {Age}");
        }

        public string GetUserData()
        {
            return $"ID: {Id}, Имя: {Name}, Email: {Email}, Возраст: {Age}";
        }
    }
}
