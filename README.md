#include <stdio.h>
#include <stdlib.h>
#include <string.h>

#define TAM 100
int leer();

void main(){

    int numero;

    printf("Tu numero es palindromo?\n");
    printf("Ingrese su numero: ");
    scanf("%d", &numero);
    leer(numero);
    
    if(leer(numero)){
        printf("%d es palindromo", numero);
    }
    else{
                printf("%d no es palindromo", numero);
    }

}

int leer(int numero){

    int original = numero;
    int reverso =0;
    
    while (numero>0)
    {
        int digito =    numero % 10;
        reverso =reverso*10+digito;
        numero =numero/10;
        
    }
    return original==reverso;
}
