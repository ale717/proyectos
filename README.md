"# proyectos" 
import java.util.Scanner;

public class Tra03{
    public static void main(String[] args) {
        Scanner ingresar = new Scanner(System.in);
        int contador = 0;
        double suma = 0.0;
        int maximaVecesQueSeRepite = 0;
        int moda = 0;
        double varianza = 0.0;
        System.out.print("Ingrese el numero de numeros:");
      
        
        contador = ingresar.nextInt();
        int[] num = new int[contador];
        for (int i = 0; i < contador; i++) {
            System.out.println("Ingrese num: ");
            num[i] = ingresar.nextInt();
            suma = suma + num[i];
        }

        double media = suma / contador;
        for (int i = 0; i < num.length; i++) {
            int vecesQueSeRepite = 0;
            for (int j = 0; j < num.length; j++) {
                if (num[i] == num[j]) {
                    vecesQueSeRepite++;
                }
            }
            if (vecesQueSeRepite > maximaVecesQueSeRepite) {
                moda = num[i];
            }
        }
        for (int i = 0; i < num.length; i++) {
            double rango;
            rango = Math.pow(num[i] - media, 2f);
            varianza = varianza + rango;
        }
        
        System.out.println("La media es " + media);
        System.out.println("La moda es " + moda);
    }

}

