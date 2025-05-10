// ========================================
// Checkpoint 2 - Algoritmos e Programação
// Nome: Lucas Mendes       - RM: 563667
// Nome: Dante Luiz         - RM: 565419
// ========================================

#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <ctype.h>

// Função 1: Gerar Sequência de Fibonacci  Responsavel Por Lucas
void Fibonacci() {
    int n;
    do {
        printf("Informe quantos termos da sequência de Fibonacci você deseja (entre 1 e 50): ");
        scanf("%d", &n);
        if (n < 1 || n > 50) {
            printf("Número fora do intervalo permitido. Tente novamente.\n");
        }
    } while (n < 1 || n > 50);

    int fib[50];
    fib[0] = 0;
    if (n > 1) fib[1] = 1;

    for (int i = 2; i < n; i++) {
        fib[i] = fib[i - 1] + fib[i - 2];
    }

    printf("Resultado da sequência de Fibonacci:\n");
    for (int i = 0; i < n; i++) {
        printf("%d ", fib[i]);
    }
    printf("\n");
}

// Função 2: Calcular Fatoriais  Responsavel Por Lucas
void Fatoriais() {
    int n;
    do {
        printf("Digite um número entre 1 e 20 para calcular os fatoriais: ");
        scanf("%d", &n);
        if (n < 1 || n > 20) {
            printf("Valor inválido! Tente novamente com um número dentro do intervalo.\n");
        }
    } while (n < 1 || n > 20);

    long long fat[20];

    for (int i = 0; i < n; i++) {
        fat[i] = 1;
        for (int j = 1; j <= i + 1; j++) {
            fat[i] *= j;
        }
    }

    printf("Fatoriais calculados:\n");
    for (int i = 0; i < n; i++) {
        printf("%d! = %lld\n", i + 1, fat[i]);
    }
}

// Função 3: Checar se é Palíndromo (Responsável: Dante Luiz)
void VerificarPalindromo() {
    char palavra[101];
    printf("Digite uma palavra para verificar se é um palíndromo: ");
    scanf(" %100s", palavra);

    int i = 0;
    int j = strlen(palavra) - 1;
    int ehPalindromo = 1;

    while (i < j) {
        if (tolower(palavra[i]) != tolower(palavra[j])) {
            ehPalindromo = 0;
            break;
        }
        i++;
        j--;
    }

    if (ehPalindromo) {
        printf("Sim! Essa palavra é um palíndromo.\n");
    } else {
        printf("Não! Essa palavra não é um palíndromo.\n");
    }
}

// Função 4: Verificar Substring (Responsável: Dante Luiz)
void VerificarSubstring() {
    char textoPrincipal[101], textoPesquisa[101];

    printf("Digite o texto principal: ");
    scanf(" %100[^\n]", textoPrincipal);
    getchar(); // Consome o Enter
    printf("Digite o texto a ser pesquisado: ");
    scanf(" %100[^\n]", textoPesquisa);

    if (strstr(textoPrincipal, textoPesquisa)) {
        printf("Sim! O segundo texto está contido no primeiro.\n");
    } else {
        printf("Não! O segundo texto não foi encontrado dentro do primeiro.\n");
    }
}

// Função principal: Menu de opções
int main() {
    int opcao;

    do {
        printf("\n====== MENU DE OPÇÕES ======\n");
        printf("1 - Gerar sequência de Fibonacci\n");
        printf("2 - Calcular fatoriais\n");
        printf("3 - Verificar se é palíndromo\n");
        printf("4 - Procurar uma substring\n");
        printf("0 - Encerrar o programa\n");
        printf("============================\n");
        printf("Digite sua escolha: ");
        scanf("%d", &opcao);
        getchar(); // Consome o Enter

        switch (opcao) {
            case 1:
                Fibonacci();
                break;
            case 2:
                Fatoriais();
                break;
            case 3:
                VerificarPalindromo();
                break;
            case 4:
                VerificarSubstring();
                break;
            case 0:
                printf("Finalizando o programa... Até logo!\n");
                break;
            default:
                printf("Opção inválida! Por favor, selecione uma das opções disponíveis.\n");
        }

        if (opcao != 0) {
            printf("\nPressione Enter para continuar...");
            getchar();
        }

    } while (opcao != 0);

    return 0;
}
