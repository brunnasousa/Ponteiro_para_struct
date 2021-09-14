# Ponteiro_para_struct
//Ponteiro para Struct - https://www.youtube.com/watch?v=MciBI4xxhEw



#include <stdio.h>
#include <stdlib.h>

//usando typedef na struct para encurtar o comando na declarção

typedef struct {
    int matricula;
    float nota;
}tAluno;

int main(void){

    //a1 é uma struct do tipo tAluno
    tAluno a1; //pq usou o typedef pode escrever essa forma
    //nao precisa escrever "struct tAluno a1"


    //*ptrAluno é um ponteiro do tipo tAluno que
    //recebe o endereco a1
    //ponteiro - tem que ser do tipo da variavel q vai apontar
    tAluno *ptrAluno = &a1; //nome da variavel e com tipo tAluno = (apontando) a a1 

    //atribuindo valores para os membros da struct a1
    a1.matricula = 55555;
    a1.nota = 8.0;

    //exibindo dados usando a struct diretamente usando
    printf("matricula: %d nota: %.2f\n", a1.matricula, a1.nota);



    //acessando usando um ponteiro

    //podemos atribuir ou acessar um valor usando ponteiro (*ptrAluno)
    (*ptrAluno).nota = 8.5;

    //exibindo dados usando um ponteiro para struct 
    printf("\nMatricula %d nota:%.2f\n", (*ptrAluno).matricula, (*ptrAluno).nota);



    //"modo mais facil"

    //ptrAluno -> substitui a notação (*ptrAluno). 
    //atribuindo um novo valor a nota usando ptrAluno ->
    ptrAluno -> nota = 9.0;

    printf("\nMatricula %d nota:%.2f\n", ptrAluno->matricula, ptrAluno->nota);

    system("pause");
    return 0;
}



