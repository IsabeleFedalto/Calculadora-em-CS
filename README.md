using System;
class Calculadora
{
    static void Main()
    {
        Console.WriteLine("=========================\n\tCalculadora\n=========================\n");
        int n1, n2, op;
        do
        {
            Console.WriteLine("Escolha uma opção:\n1 - Soma\n2 - Subtração\n3 - Divisão\n4 - Multiplicação\n5 - Sair\n");
            op = int.Parse(Console.ReadLine());
            if (op == 5) break;
            Console.WriteLine("Digite o primeiro número:");
            n1 = int.Parse(Console.ReadLine());
            Console.WriteLine("Digite o segundo número:");
            n2 = int.Parse(Console.ReadLine());
            switch(op)
            {
                case 1:
                    Console.WriteLine("=======Soma=======");
                    Console.WriteLine("Total: " + (n1 + n2));
                    break;
                case 2:
                    Console.WriteLine("=======Subtração=======");
                    Console.WriteLine("Total: " + (n1 - n2));
                    break;
                case 3:
                    Console.WriteLine("=======Divisão=======");
                    if (n2 != 0)
                    {
                        Console.WriteLine("Total: " + (n1 / n2));
                    }
                    else
                    {
                        Console.WriteLine("O segundo número não pode ser 0");
                    }
                    break;
                case 4:
                    Console.WriteLine("=======Multiplicar=======");
                    Console.WriteLine("Total: " + (n1 * n2));
                    break;
                default:
                    Console.WriteLine("Opção inválida...");
                    break;
            }
            Console.WriteLine("\nPressione qualquer tecla para continuar...");
            Console.ReadKey();
            Console.Clear();
        } while (op != 5);
    }
}
