# Primeiros códigos em C

Meu primeiro projeto em C envolvendo:

- Vetores
- Estruturas de repetição
- Controle de estoque
- Busca de produtos

## Código

```c
#include <stdio.h>
int main()
{
    int x[10], y[10];
    int cliente, cod_prod, quant_prod;
    int existe;
    int i;
    
    for(i=0;i<10;i++){
        printf("Digite o codigo do %d° produto:", i + 1);
        scanf("%d", &x[i]);
    }
    printf("\n");
    for(i=0;i<10;i++){
        printf("Quantidade do %d° produto no estoque:", i + 1);
        scanf("%d", &y[i]);
    }
    
    while(1){
        printf("\ndigite o codigo do cliente:");
    scanf("%d", &cliente);
    if(cliente==0){
        break;
    }
    printf("\ncodigo do produto que o cliente quer:");
    scanf("%d", &cod_prod);
    existe=0;
    for(i=0;i<10;i++){
        if(cod_prod==x[i]){
            existe=1;
            break;
        }
    }
    if(existe==0){
        printf("\ncodigo inexistente");
        continue;
    }
    printf("\nquantos produtos ele quer? ");
    scanf("%d", &quant_prod);
    if(quant_prod<=y[i]){
        y[i]-=quant_prod;
        printf("\npedido atendido. Obrigado volte sempre!\n");
    }else{
        printf("\nnão temos estoque o suficiente para esta mercadoria\n");
    }
    
    printf("\nDIGITE 0 PARA ENCERRAR O PROGRAMA!\n");
    }
    printf("\nEstoque final\n");
    for(i=0;i<10;i++){
        printf("codigo: %d estoque:%d\n", x[i], y[i]);
    }
    
    
    
    
    return 0;
}
```
