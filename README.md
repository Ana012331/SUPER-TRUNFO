# SUPER-TRUNFO
SUPER TRUNFO EM C.
#include <stdio.h>
#include <string.h> // para usar strlen()

// Função para limpar o buffer do teclado
void limparBuffer() {
    int c;
    while ((c = getchar()) != '\n' && c != EOF);
}

int main() {
    // === CARTA 1 ===
    char Estado1[3], Cidade1[50], Codigo1[4];
    int Populacao1, PontosTuristicos1;
    float Pib1, Area1, PibPerCapita1, Densidade1;

    // === CARTA 2 ===
    char Estado2[3], Cidade2[50], Codigo2[4];
    int Populacao2, PontosTuristicos2;
    float Pib2, Area2, PibPerCapita2, Densidade2;

    printf("=== Cadastro da CARTA 1 ===\n");
    printf("Digite o estado (ex: SP): ");
    scanf("%2s", Estado1);
    limparBuffer();

    printf("Digite o nome da cidade: ");
    fgets(Cidade1, sizeof(Cidade1), stdin);
    Cidade1[strcspn(Cidade1, "\n")] = '\0'; // remove o ENTER

    printf("Digite o código da carta: ");
    scanf("%3s", Codigo1);

    printf("Digite a população: ");
    scanf("%d", &Populacao1);

    printf("Digite o número de pontos turísticos: ");
    scanf("%d", &PontosTuristicos1);

    printf("Digite o PIB (em bilhões de reais): ");
    scanf("%f", &Pib1);

    printf("Digite a área (em km²): ");
    scanf("%f", &Area1);

    // Calcula valores derivados da carta 1
    PibPerCapita1 = (Pib1 * 1000000000) / Populacao1;
    Densidade1 = Populacao1 / Area1;

    // ==========================================
    printf("\n=== Cadastro da CARTA 2 ===\n");
    printf("Digite o estado (ex: SP): ");
    scanf("%2s", Estado2);
    limparBuffer();

    printf("Digite o nome da cidade: ");
    fgets(Cidade2, sizeof(Cidade2), stdin);
    Cidade2[strcspn(Cidade2, "\n")] = '\0'; // remove o ENTER

    printf("Digite o código da carta: ");
    scanf("%3s", Codigo2);

    printf("Digite a população: ");
    scanf("%d", &Populacao2);

    printf("Digite o número de pontos turísticos: ");
    scanf("%d", &PontosTuristicos2);

    printf("Digite o PIB (em bilhões de reais): ");
    scanf("%f", &Pib2);

    printf("Digite a área (em km²): ");
    scanf("%f", &Area2);

    // Calcula valores derivados da carta 2
    PibPerCapita2 = (Pib2 * 1000000000) / Populacao2;
    Densidade2 = Populacao2 / Area2;

    // ==========================================
    // Comparações
    printf("\n=== RESULTADO DA COMPARAÇÃO ===\n");

    printf("População: ");
    if (Populacao1 > Populacao2)
        printf("%s venceu! (%d x %d)\n", Cidade1, Populacao1, Populacao2);
    else if (Populacao2 > Populacao1)
        printf("%s venceu! (%d x %d)\n", Cidade2, Populacao2, Populacao1);
    else
        printf("Empate (%d x %d)\n", Populacao1, Populacao2);

    printf("PIB: ");
    if (Pib1 > Pib2)
        printf("%s venceu! (%.2f x %.2f bilhões)\n", Cidade1, Pib1, Pib2);
    else if (Pib2 > Pib1)
        printf("%s venceu! (%.2f x %.2f bilhões)\n", Cidade2, Pib2, Pib1);
    else
        printf("Empate (%.2f x %.2f bilhões)\n", Pib1, Pib2);

    printf("PIB per capita: ");
    if (PibPerCapita1 > PibPerCapita2)
        printf("%s venceu! (%.2f x %.2f)\n", Cidade1, PibPerCapita1, PibPerCapita2);
    else if (PibPerCapita2 > PibPerCapita1)
        printf("%s venceu! (%.2f x %.2f)\n", Cidade2, PibPerCapita2, PibPerCapita1);
    else
        printf("Empate (%.2f x %.2f)\n", PibPerCapita1, PibPerCapita2);

    printf("Densidade populacional (menor vence): ");
    if (Densidade1 < Densidade2)
        printf("%s venceu! (%.2f x %.2f hab/km²)\n", Cidade1, Densidade1, Densidade2);
    else if (Densidade2 < Densidade1)
        printf("%s venceu! (%.2f x %.2f hab/km²)\n", Cidade2, Densidade2, Densidade1);
    else
        printf("Empate (%.2f x %.2f hab/km²)\n", Densidade1, Densidade2);

    printf("Pontos turísticos: ");
    if (PontosTuristicos1 > PontosTuristicos2)
        printf("%s venceu! (%d x %d)\n", Cidade1, PontosTuristicos1, PontosTuristicos2);
    else if (PontosTuristicos2 > PontosTuristicos1)
        printf("%s venceu! (%d x %d)\n", Cidade2, PontosTuristicos2, PontosTuristicos1);
    else
        printf("Empate (%d x %d)\n", PontosTuristicos1, PontosTuristicos2);

    printf("\n=== Fim da comparação ===\n");

    return 0;
}