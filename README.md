//Напишите программу, которая отображает имя в прямоугольнике из символов, выбранных пользователем.
//Программа должна запрашивать у пользователя символ для создания прямоугольника и само имя, которое нужно отобразить внутри этого прямоугольника. Затем выводите имя в прямоугольнике из указанного символа.
//Длина всех строк в прямоугольнике должна быть одинаковой. Чтобы определить эту длину, можно использовать длину строки, содержащей имя, плюс две дополнительные позиции для символов по краям. Например, если пользователь вводит символ % и имя Alexey, то получится //прямоугольник, в котором каждая строка содержит 8 символов (включая символы по краям):

%%%%%%%
%Airat%
%%%%%%%


using System;

namespace ConsoleApp4_2_6
{
    class Program
    {
        static void Main(string[] args)
        {
            string frameWidht = "";
            Console.WriteLine("Вывести имя в прямоугольник из символа, который введет сам пользователь.");

            Console.Write("Введите имя: ");
            string name = Console.ReadLine();
            Console.WriteLine($"Имя:  {name},длина имени: {name.Length}");

            Console.Write("Введите символ: ");
            string simbol = Console.ReadLine();
            int additionToLength = 4;
            string emptySpaceForSecondLine = " ";
            Console.WriteLine($"Cимвол:  {simbol}");

            Console.WriteLine("Решение задачи: ");

            for (int i = 1; i <= (name.Length + additionToLength); i += 1)
            {
                frameWidht += simbol;
            }

            Console.WriteLine(frameWidht);
            Console.WriteLine(frameWidht[0] + emptySpaceForSecondLine + name + emptySpaceForSecondLine + frameWidht[frameWidht.Length - 1]);
            Console.WriteLine(frameWidht);
        }
    }
}
