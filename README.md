using System;

class Program
{
    static void Main()
    {
        bool continueCalculating = true;

        while (continueCalculating)
        {
            Console.Clear();
            Console.WriteLine("Calculadora en C#\n");

            // Solicitar el primer numero
            Console.Write("Ingrese el primer numero: ");
            double num1 = Convert.ToDouble(Console.ReadLine());

            // Solicitar el segundo numero
            Console.Write("Ingrese el segundo numero: ");
            double num2 = Convert.ToDouble(Console.ReadLine());

            // Solicitar la operación
            Console.WriteLine("\nSeleccione una operacion:");
            Console.WriteLine("1 - Suma");
            Console.WriteLine("2 - Resta");
            Console.WriteLine("3 - Multiplicación");
            Console.WriteLine("4 - División");
            Console.Write("Opción: ");
            int opcion = Convert.ToInt32(Console.ReadLine());

            double resultado = 0;

            switch (opcion)
            {
                case 1:
                    resultado = num1 + num2;
                    Console.WriteLine($"\nEl resultado de {num1} + {num2} es: {resultado}");
                    break;
                case 2:
                    resultado = num1 - num2;
                    Console.WriteLine($"\nEl resultado de {num1} - {num2} es: {resultado}");
                    break;
                case 3:
                    resultado = num1 * num2;
                    Console.WriteLine($"\nEl resultado de {num1} * {num2} es: {resultado}");
                    break;
                case 4:
                    if (num2 != 0)
                    {
                        resultado = num1 / num2;
                        Console.WriteLine($"\nEl resultado de {num1} / {num2} es: {resultado}");
                    }
                    else
                    {
                        Console.WriteLine("\nError: División por cero no es permitida.");
                    }
                    break;
                default:
                    Console.WriteLine("\nOpcion no valida.");
                    break;
            }
