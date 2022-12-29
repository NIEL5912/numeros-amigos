# numeros-amigos

#include <stdio.h>
#include <stdlib.h

int soma_divisores( int n);
int sao_amigos (int s1, int s2);

int main (void){
   int a,b;
   printf ("Entre com dois inteiros positivos:\n");
   scanf ("%d%d", &a, &b);
   if ( sao_amigos(a, b)==1) { printf ("Os numeros %d e %d sao amigos.\n", a, b);} 
   if ( sao_amigos(a, b)==0) { printf ("Os numeros %d e %d nao sao amigos.\n", a, b);}
   
   
   return 0;
}
int soma_divisores( int n){int i; int soma=0;
 for ( i=1; i<n; i++){
      if ( n%i==0) soma=soma+i;
   }
   return soma;
} 
int sao_amigos (int s1, int s2){ 
if (soma_divisores(s1)==s2 && soma_divisores(s2)==s1) {
   return 1; } else {return 0;}
}


