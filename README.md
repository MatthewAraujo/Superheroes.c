# Superheroes.c
#include <stdio.h>

int main(void) {
  
  int voto, cont1=0, cont2=0, cont3=0, cont4=0, idade, somaidade=0, maiorvoto=0, contm=0;
  float media=0;
  char sexo;

  for (int i=1; i<=50; i++){
    printf("Digite seu sexo (m/f):  ");
    scanf(" %c",&sexo);
    printf("Digite sua idade: ");
    scanf("%d", &idade);
    printf("Vote no seu super herói favorito!\n Digite:\n 1- Hulk\n 2- Thor\n 3- Capitã Marvel\n 4- Voto nulo\n ");
    scanf("%d",&voto);
    if(voto==1){
      cont1++;
    }
    if(voto==2){
      cont2++;
    }
    if(voto==3){
      cont3++;
    }
    if(voto==1){
      somaidade+=idade;
    }
    if (sexo=='f' && voto==4){
      contm++;
    }
  }
  
  if (cont1>=1){
   media=somaidade/cont1;
  }

  printf("\nO total de votos para cada herói foi:\n Hulk= %d \n Thor=%d\n Capitã Marvel=%d.", cont1, cont2, cont3);
  if(cont1>cont2 && cont1>cont3){
    printf("\nO maior votado foi o Hulk com %d votos ",cont1);
  }else if(cont2>cont1 && cont2>cont3){
    printf("\nO maior votado foi o Thor com %d votos ",cont2);
  }else if(cont3>cont1 && cont3>cont2){
    printf("\nO maior votado foi o Capitã Marvel com %d votos ",cont3);
  }
  printf("\nA média de idade de quem votou no Hulk foi de: %.2f", media);
  printf("\nO número de mulheres que votaram nulo foi de: %d", contm);

  return 0;
}
