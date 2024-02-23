import java.util.Scanner;

public class MediaAluno {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Digite a nota da Prova 1:");
        double prova1 = scanner.nextDouble();

        System.out.println("Digite a nota da Prova 2:");
        double prova2 = scanner.nextDouble();

        System.out.println("Digite a nota da Prova 3:");
        double prova3 = scanner.nextDouble();

        double media = (prova1 + prova2 + prova3) / 3;

        if (media >= 7.0) {
            System.out.println("Média: " + media);
            System.out.println("Aluno aprovado!");
        } else {
            System.out.println("Média: " + media);
            System.out.println("Digite a nota da Rec:");
            double rec = scanner.nextDouble();
            double mediaFinal = (media + recuperacao) / 2;
            if (mediaFinal >= 5.0) {
                System.out.println("Média final: " + mediaFinal);
                System.out.println("Aluno aprovado na rec!");
            } else {
                System.out.println("Média final: " + mediaFinal);
                System.out.println("Aluno reprovado!");
            }
        }

        scanner.close();
    }
}




import java.util.Scanner;

public class PromocaoLivraria {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Digite a quantidade de livros que deseja comprar:");
        int quantidadeLivros = scanner.nextInt();

        double precoTotalA = 0.25 * quantidadeLivros + 7.50;
        double precoTotalB = 0.50 * quantidadeLivros + 2.50;

        if (precoTotalA < precoTotalB) {
            System.out.println("Opção A é a melhor escolha.");
            System.out.println("Preço total: R$" + precoTotalA);
        } else if (precoTotalB < precoTotalA) {
            System.out.println("Opção B é a melhor escolha.");
            System.out.println("Preço total: R$" + precoTotalB);
        } else {
            System.out.println("Ambas as opções têm o mesmo preço.");
            System.out.println("Preço total (opção A): R$" + precoTotalA);
            System.out.println("Preço total (opção B): R$" + precoTotalB);
        }

        scanner.close();
    }
}




import java.util.Scanner;

public class IntervaloTempo {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Entrada dos dados para o primeiro intervalo de tempo
        System.out.println("Digite as horas, minutos e segundos do primeiro intervalo separados por espaços:");
        int horas1 = scanner.nextInt();
        int minutos1 = scanner.nextInt();
        int segundos1 = scanner.nextInt();

        // Entrada dos dados para o segundo intervalo de tempo
        System.out.println("Digite as horas, minutos e segundos do segundo intervalo separados por espaços:");
        int horas2 = scanner.nextInt();
        int minutos2 = scanner.nextInt();
        int segundos2 = scanner.nextInt();

        // Cálculo da soma dos intervalos
        int somaHoras = horas1 + horas2;
        int somaMinutos = minutos1 + minutos2;
        int somaSegundos = segundos1 + segundos2;

        // Ajuste caso os segundos ultrapassem 60
        if (somaSegundos >= 60) {
            somaSegundos -= 60;
            somaMinutos++;
        }

        // Ajuste caso os minutos ultrapassem 60
        if (somaMinutos >= 60) {
            somaMinutos -= 60;
            somaHoras++;
        }

        // Cálculo da diferença entre os intervalos
        int diferencaHoras = Math.abs(horas1 - horas2);
        int diferencaMinutos = Math.abs(minutos1 - minutos2);
        int diferencaSegundos = Math.abs(segundos1 - segundos2);

        // Exibição dos resultados
        System.out.println("Soma dos intervalos:");
        System.out.println("Horas: " + somaHoras);
        System.out.println("Minutos: " + somaMinutos);
        System.out.println("Segundos: " + somaSegundos);

        System.out.println("\nDiferença entre os intervalos:");
        System.out.println("Horas: " + diferencaHoras);
        System.out.println("Minutos: " + diferencaMinutos);
        System.out.println("Segundos: " + diferencaSegundos);

        scanner.close();
    }
}



import java.util.Scanner;

public class NumeroDigitos {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.println("Digite um número inteiro maior ou igual a 0:");
        int numero = scanner.nextInt();

        // Verifica se o número é maior ou igual a 0
        if (numero >= 0) {
            int numeroDigitos = contarDigitos(numero);
            System.out.println("O número de dígitos de " + numero + " é: " + numeroDigitos);
        } else {
            System.out.println("O número digitado não é inválido . Deve ser maior ou igual a 0.");
        }

        scanner.close();
    }

    // Função para contar o número de dígitos de um número inteiro
    public static int contarDigitos(int num) {
        // Converte o número para uma string e retorna o comprimento da string
        return String.valueOf(num).length();
    }
}
