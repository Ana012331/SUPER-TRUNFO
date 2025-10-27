#include <stdio.h>

int main() {
    // Carta 1
    char estado1[3];
    char cidade1[50];
    char codigo1[4];
    int populacao1;
    float area1;
    float pib1;
    int pontosTuristicos1;

    // Carta 2
    char estado2[3];
    char cidade2[50];
    char codigo2[4];
    int populacao2;
    float area2;
    float pib2;
    int pontosTuristicos2;

    int opcao;

    printf("===== DESAFIO SUPER TRUNFO =====\n\n");

    // Cadastro da primeira carta
    printf("--- Cadastro da Carta 1 ---\n");
    printf("Digite o estado (ex: SP): ");
    scanf("%2s", estado1);

    printf("Digite a cidade: ");
    scanf("%s", cidade1);

    printf("Digite o código da carta (ex: A01): ");
    scanf("%3s", codigo1);

    printf("Digite a população: ");
    scanf("%d", &populacao1);

    printf("Digite a área (em km²): ");
    scanf("%f", &area1);

    printf("Digite o PIB (em bilhões): ");
    scanf("%f", &pib1);

    printf("Digite o número de pontos turísticos: ");
    scanf("%d", &pontosTuristicos1);

    printf("\n--- Cadastro da Carta 2 ---\n");
    printf("Digite o estado (ex: RJ): ");
    scanf("%2s", estado2);

    printf("Digite a cidade: ");
    scanf("%s", cidade2);

    printf("Digite o código da carta (ex: A02): ");
    scanf("%3s", codigo2);

    printf("Digite a população: ");
    scanf("%d", &populacao2);

    printf("Digite a área (em km²): ");
    scanf("%f", &area2);

    printf("Digite o PIB (em bilhões): ");
    scanf("%f", &pib2);

    printf("Digite o número de pontos turísticos: ");
    scanf("%d", &pontosTuristicos2);

    // Escolha de atributo para comparar
    printf("\n=== Escolha o atributo para comparar ===\n");
    printf("1 - População\n");
    printf("2 - Área\n");
    printf("3 - PIB\n");
    printf("4 - Pontos Turísticos\n");
    printf("Digite sua opção: ");
    scanf("%d", &opcao);

    printf("\n=== Resultado ===\n");

    // Comparação simples
    if (opcao == 1) {
        if (populacao1 > populacao2)
            printf("Carta 1 venceu em População!\n");
        else
            printf("Carta 2 venceu em População!\n");
    } else if (opcao == 2) {
        if (area1 > area2)
            printf("Carta 1 venceu em Área!\n");
        else
            printf("Carta 2 venceu em Área!\n");
    } else if (opcao == 3) {
        if (pib1 > pib2)
            printf("Carta 1 venceu em PIB!\n");
        else
            printf("Carta 2 venceu em PIB!\n");
    } else if (opcao == 4) {
        if (pontosTuristicos1 > pontosTuristicos2)
            printf("Carta 1 venceu em Pontos Turísticos!\n");
        else
            printf("Carta 2 venceu em Pontos Turísticos!\n");
    } else {
        printf("Opção inválida!\n");
    }

    // Exibir dados das cartas
    printf("\n--- Carta 1 ---\n");
    printf("Código: %s | Estado: %s | Cidade: %s\n", codigo1, estado1, cidade1);
    printf("População: %d | Área: %.2f | PIB: %.2f | Pontos: %d\n",
           populacao1, area1, pib1, pontosTuristicos1);

    printf("\n--- Carta 2 ---\n");
    printf("Código: %s | Estado: %s | Cidade: %s\n", codigo2, estado2, cidade2);
    printf("População: %d | Área: %.2f | PIB: %.2f | Pontos: %d\n",
           populacao2, area2, pib2, pontosTuristicos2);

    printf("\n===== FIM DO JOGO =====\n");

    return 0;
}

