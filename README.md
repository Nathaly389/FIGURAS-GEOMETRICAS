# FIGURAS-GEOMETRICAS
TAREA
using System;

namespace FigurasGeometricas
{
    public class Circulo
    {
        private double radio;

        public Circulo(double radio)
        {
            this.radio = radio;
        }

        public double CalcularArea()
        {
            return Math.PI * radio * radio;
        }

        public double CalcularPerimetro()
        {
            return 2 * Math.PI * radio;
        }
    }

    public class Rectangulo
    {
        private double ancho;
        private double alto;

        public Rectangulo(double ancho, double alto)
        {
            this.ancho = ancho;
            this.alto = alto;
        }

        public double CalcularArea()
        {
            return ancho * alto;
        }

        public double CalcularPerimetro()
        {
            return 2 * (ancho + alto);
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("=== Figuras Geométricas ===");

            Console.Write("\nIngrese el radio del círculo: ");
            double radio = double.Parse(Console.ReadLine());
            Circulo c = new Circulo(radio);

            Console.WriteLine($"Área del círculo: {c.CalcularArea():F2}");
            Console.WriteLine($"Perímetro del círculo: {c.CalcularPerimetro():F2}");

            Console.Write("\nIngrese el ancho del rectángulo: ");
            double ancho = double.Parse(Console.ReadLine());

            Console.Write("Ingrese el alto del rectángculo: ");
            double alto = double.Parse(Console.ReadLine());

            Rectangulo r = new Rectangulo(ancho, alto);

            Console.WriteLine($"Área del rectángulo: {r.CalcularArea():F2}");
            Console.WriteLine($"Perímetro del rectángulo: {r.CalcularPerimetro():F2}");

            Console.WriteLine("\nPresione ENTER para salir...");
            Console.ReadLine();
        }
    }
}
