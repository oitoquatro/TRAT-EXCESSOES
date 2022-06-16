import java.util.InputMismatchException;
import java.util.Scanner;

public class ExercicioTratamentoExcecoes_Divisao {

	public static void main(String[] args) throws Exception {
		Scanner ler = new Scanner(System.in);

		int res = 0;
		int num1 = 0;
		int num2 = 0;
		
		System.out.println("Insira um número e em seguida um outro para fazer sua divisão.");
		System.out.println();

		try {
			System.out.print("1º número: ");
			num1 = ler.nextInt();
			System.out.print("12º número: ");
			num2 = ler.nextInt();

			res = num1 / num2;
		} catch (ArithmeticException e) {
			System.out.println("");
			System.out.println("Erro: "+ num1 + " não é divisível por " + num2 + " ! ");
		} catch (InputMismatchException e) {
			System.out.println("Erro: Valor inserido 'INVÁLIDO'!");
		}

		System.out.println("");
		System.out.println("Resultado de " + num1 + " dividido por " + num2 + " é igual à " + res);

	}

}
