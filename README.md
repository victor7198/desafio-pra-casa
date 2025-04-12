# desafio-pra-casa

public class ReajusteSalarial {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        System.out.print("Informe o salário atual do colaborador: R$ ");
        double salarioAtual = scanner.nextDouble();

        double percentual = 0;

        if (salarioAtual <= 280) {
            percentual = 20;
        } else if (salarioAtual <= 700) {
            percentual = 15;
        } else if (salarioAtual <= 1500) {
            percentual = 10;
        } else {
            percentual = 5;
        }

        double valorAumento = salarioAtual * (percentual / 100);
        double novoSalario = salarioAtual + valorAumento;
        double inflacao = 3.8;
        double aumentoReal = valorAumento - (salarioAtual * (inflacao / 100));

        System.out.println("\n===== Resultado do Reajuste =====");
        System.out.printf("Salário antes do reajuste: R$ %.2f\n", salarioAtual);
        System.out.printf("Percentual aplicado: %.0f%%\n", percentual);
        System.out.printf("Valor do aumento: R$ %.2f\n", valorAumento);
        System.out.printf("Novo salário: R$ %.2f\n", novoSalario);
        System.out.printf("Aumento real (descontando inflação): R$ %.2f\n", aumentoReal);

        scanner.close();
    }
}
