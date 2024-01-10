# Examen 1 de Programación
**Primer examen de programación del curso de DAW Presencial**

## Examen en Pseudocodigo
- Actividad 1
~~~
void decimalBinari(int nombre) {
  while (nombre != 0) {
    print(nombre%2);
    nombre = nombre/2;
  }
}
~~~

- Actividad 2
~~~
void binariDecimal(long binari) {
  double decimal = 0;
  for (int i = 0; decimal != 0; i++) {
    int digit = (int) num%10;
    decimal += digit * 2^i;
    num = num/10;
  }
  print(decimal);
}
~~~

- Actividad 3
~~~
boolean esParell(int n) {
  return (n%2 == 0);
}
~~~

- Actividad 4
~~~
void primersNombresParells(int n) {
  for (int i = 0; i <= n; i++) {
    if (esParell(i)) {
      print(i);
    }
  }
}
~~~

- Actividad 5
~~~
int menu() {
  print(“Tria una de les següents opcions:”);
  print(“1. Decimal a binari”);
  print(“2. Binari a decimal”);
  print(“3. És parell?”);
  print(“4. Calcular parells de 0 fins a n”);
  print(“0. Sortir”);
  return = input();
}
~~~

- Actividad 6
~~~
main() {
  int opcio = menu();
  while (opcio != 0) {
    switch(opcio) {
      case 1:
        print(“Introdueix un nombre decimal:”);
        int nombre = input();
        decimalBinari(nombre);
        break;
      case 2:
        print(“Introdueix un nombre binari:”);
        long nombre = input();
        binariDecimal(nombre);
        break;
      case 3:
        print(“Introdueix un nombre:”);
        int nombre = input();
        print(esParell(nombre));
        break;
      case 4:
        print(“Introdueix un nombre màxim:”);
        int nombre = input();
        primersNombresParells(nombre);
        break;
      default:
        print(“El nombre és incorrecte”);
    }
    opcio = menu();
  }
}
~~~

- Actividad 7
~~~
a)
double volumCilindre(double radi, double longitud) {
  return pi * radi^2 * longitud;
}

b)
double volumPrismaRectangular(double c1, double c2, double c3) {
  return c1 * c2 * c3;
}
~~~

- Actividad 8
~~~
main() {
  println(“Què hem de transportar? 1. Líquids 2. Sòlids”);
  int opcio = input();

  while(opcio != 1 || opcio != 2) {
    println(“No és una opció vàlida”);
    println(“Què hem de transportar? 1. Líquids 2. Sòlids”);
    opcio = input();
  }

  double volum = 0;

  if (opcio == 1) {
    println(“Què medeix el radi de la cisterna”);
    double radi = input();
    println(“Què medeix de llarg la cisterna”);
    double llarg = input();
    volum = volumCilindre(radi, llarg);
  } else if (opcio == 2) {
    println(“Què medeix el costat 1 del camió”);
    double c1 = input();
    println(“Què medeix el costat 2 del camió”);
    double c2 = input();
    println(“Què medeix el costat 3 del camió”);
    double c3 = input();
    volum = volumPrismaRectangular(c1, c2, c3);
  }
  
  println(“Quants metres cúbics hem de transportar?”);
  double m3_a_transportar = input();
  
  println(“El tràiler té “ + volum + “ centímetres cúbics”);
  double capacitat = volum/1000000;
  
  println(“Hi caben “ + capacitat “ metres cúbics”);
  int viatges = (int) m3_a_transportar/capacitat;
  viatges++;
  
  println(“Has de fer “ + viatges + “ viatges.”);
}
~~~

## Examen en Java
- Actividad 1
~~~
import java.util.Scanner;

public class exercici1 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Escriu un numero per saber el seu binari");
        int numero = sc.nextInt();
        decimalBinari(numero);
        sc.close();
    }
    static void decimalBinari(int numero) {
        while (numero != 0) {
            System.out.print(numero%2);
            numero /= 2;
        }
    }
}
~~~

- Actividad 2
~~~
import java.util.Scanner;

public class exercici2 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Escriu un nombre en binari");
        long numero = sc.nextLong();
        binaridecimal(numero);
        sc.close();
    }
    static void binaridecimal(long numero) {
        double decimal = 0;
        for (int i = 0; numero != 0; i++) {
            int digit = (int) numero%10;
            decimal += digit * Math.pow(2,i);
            numero = numero/10;
        }
        System.out.print(decimal);
    }
}
~~~

- Actividad 3
~~~
import java.util.Scanner;

public class exercici3 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Escriu un nombre: ");
        int numero = sc.nextInt();
        System.out.println(esParell(numero));
        sc.close();
    }
    static boolean esParell(int numero) {
        return (numero%2 == 0);
    }
}
~~~

- Actividad 4
~~~
public class exercici4 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Escriu un nombre: ");
        int numero = sc.nextInt();
        System.out.println(esParell(numero));
        primersNombresParells(numero);
        sc.close();
    }
    static boolean esParell(int numero) {
        return (numero%2 == 0);
    }
    static void primersNombresParells(int numero) {
        for (int i = 0; i <= numero; i++) {
            if (esParell(i)) {
                System.out.print(i);
            }
        }
    }
}
~~~

- Actividad 5
~~~
import java.util.Scanner;

public class exercici5 {
    public static void main(String[] args) {
        System.out.println(menu());
    }
    static int menu() {
        Scanner sc = new Scanner(System.in);
        System.out.println("Tria una de les següents opcions");
        System.out.println("1. Decimal a binari");
        System.out.println("2. Binari a decimal");
        System.out.println("3. És parell?");
        System.out.println("4. Calcular parells de 0 fins a n");
        System.out.println("0. Sortir");
        int numero = sc.nextInt();
        sc.close();
        return numero;
    }
}
~~~

- Actividad 6
~~~
import java.util.Scanner;

public class exercici6 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int opcio = menu();
        while (opcio != 0) {
            switch (opcio) {
                case 1:
                    System.out.println("Escriu un numero per saber el seu binari");
                    int numero = sc.nextInt();
                    decimalBinari(numero);
                    break;
                
                case 2:
                    System.out.println("Escriu un nombre en binari");
                    long numero2 = sc.nextLong();
                    binaridecimal(numero2);
                    break;

                case 3:
                    System.out.println("Escriu un nombre: ");
                    int numero3 = sc.nextInt();
                    System.out.println(esParell(numero3));
                    break;

                case 4:
                    System.out.println("Escriu un nombre: ");
                    int numero4 = sc.nextInt();
                    System.out.println(esParell2(numero4));
                    primersNombresParells(numero4);
                    break;

                default:
                    System.out.println("El nombre es incorrecte");
                    break;
            }
            opcio = menu();
        }
        sc.close();
    }
    static int menu() {
        Scanner sc = new Scanner(System.in);
        System.out.println("Tria una de les següents opcions");
        System.out.println("1. Decimal a binari");
        System.out.println("2. Binari a decimal");
        System.out.println("3. És parell?");
        System.out.println("4. Calcular parells de 0 fins a n");
        System.out.println("0. Sortir");
        int numero = sc.nextInt();
        sc.close();
        return numero;
    }
    static void decimalBinari(int numero) {
        while (numero != 0) {
            System.out.print(numero%2);
            numero /= 2;
        }
        System.out.println("");
    }
    static void binaridecimal(long numero2) {
        double decimal = 0;
        for (int i = 0; numero2 != 0; i++) {
            int digit = (int) numero2%10;
            decimal += digit * Math.pow(2,i);
            numero2 = numero2/10;
        }
        System.out.println(decimal);
    }
    static boolean esParell(int numero3) {
        return (numero3%2 == 0);
    }
    static boolean esParell2(int numero4) {
        return (numero4%2 == 0);
    }
    static void primersNombresParells(int numero4) {
        for (int i = 0; i <= numero4; i++) {
            if (esParell(i)) {
                System.out.print(i);
            }
        }
        System.out.println("");
    }
}
~~~

- Actividad 7
~~~
import java.util.Scanner;

public class exercici7 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Escriu una opcio: 1 Volum Cilindre, 2 Volum Prisma Rectanngular");
        int opcio = sc.nextInt();
        if (opcio == 1) {
            System.out.println("Escriu el radi i la longitud del Cilindre: ");
            double radi = sc.nextDouble();
            double longitud = sc.nextDouble();
            System.out.println(volumCilindre(radi, longitud));
        } else if (opcio == 2) {
            System.out.println("Escriu la longitud dels 3 costats: ");
            double c1 = sc.nextDouble();
            double c2 = sc.nextDouble();
            double c3 = sc.nextDouble();
            System.out.println(volumPrismaRectangular(c1, c2, c3));
        }
    }
    static double volumCilindre (double radi, double longitud) {
        return Math.PI * Math.pow(radi, 2) * longitud;
    }
    static double volumPrismaRectangular (double c1, double c2, double c3) {
        return c1 * c2 * c3;
    }
}
~~~

- Actividad 8
~~~
import java.util.Scanner;

public class exercici8 {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Que vols transportar? Escriu 1 per Liquids o 2 per Solids: ");
        int opcio = sc.nextInt();

        while (opcio != 1 || opcio != 2) {
            System.out.println("Escriu una opcio valida");
            System.out.println("Que vols transportar? Escriu 1 per Liquids o 2 per Solids: ");
            opcio = sc.nextInt();
        }

        double volum = 0;

        if (opcio == 1) {
            System.out.println("Escriu el radi de la cisterna: ");
            double radi = sc.nextDouble();
            System.out.println("Escriu la longitud de la cisterna: ");
            double longitud = sc.nextDouble();
            volum = volumCilindre(radi, longitud);
        } else if (opcio == 2) {
            System.out.println("Escriu la mida del Costat 1");
            double c1 = sc.nextDouble();
            System.out.println("Escriu la mida del Costat 2");
            double c2 = sc.nextDouble();
            System.out.println("Escriu la mida del Costat 3");
            double c3 = sc.nextDouble();
            volum = volumPrismaRectangular(c1, c2, c3);
        }

        System.out.println("Quants metres cubics s'han de transportar?");
        double transportar = sc.nextDouble();

        System.out.println("El camio te " + volum + " centimetres cubics");
        double capacitat = volum/1000000;

        System.out.println("Hi caben " + capacitat + " metres cubics");
        double viatges = transportar/capacitat;
        viatges++;
        System.out.println("Has de fer " + viatges + " viatges");
        sc.close();
    }
    static double volumCilindre (double radi, double longitud) {
        return Math.PI * Math.pow(radi, 2) * longitud;
    }
    static double volumPrismaRectangular (double c1, double c2, double c3) {
        return c1 * c2 * c3;
    }
}
~~~
