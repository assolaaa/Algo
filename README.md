#include <stdio.h>
int main(){
printf("Exercice 01:\n   Question 1.1:\n");	
printf("\n");
int A[20][20],i,O[20][20],j,n;	
char R[5][5]={{'1','2','3','4','5'},{'7','a','c','8','d'},{'c','9','4','z','8'},{'5','6','p','n','3'},{'2','9','t','m','k'}};

for(i=0;i<5;i++){
for(j=0;j<5;j++){
printf("\t%c",R[i][j]);}
printf("\n");}

printf("\n pair=\n");
for(i=0;i<5;i+=2){
	for(j=0;j<5;j++){
printf("\t%c",R[i][j]);
}
printf("\n");
}

printf("\n impair=\n");
for(i=1;i<5;i+=2){
	for(j=0;j<5;j++){
printf("\t%c",R[i][j]);
}
printf("\n");
}
printf("\n");  

printf("   Question 1.2:\n"); 
printf("\nla 1e diagonale=\tla 2e diagonale=\n");
for(i=0,j=4;i<5;i++,j--){
printf("%c",R[i][i]);
printf("\t\t\t  %c",R[i][j]);
printf("\n");
}
printf("\n");

printf("Exercice 02:\n");

printf("donne n :\n");
scanf("%d",&n);

printf("\ndonne la matrice :\n");
for(i=0;i<n;i++){
for(j=0;j<n;j++){
printf("A[%d][%d]= ",i,j);	
scanf("\n%d",&A[i][j]);
}
} 

printf("\n");
printf("\tAvant: \n");
for(i=0;i<n;i++){
	for(j=0;j<n;j++){
printf("\t%d",A[i][j]);
}
printf("\n");
}

for( i=0;i<n;i++){
	for( j=0;j<n;j++){
	 if(i!=j){
	 O[i][j]=A[i][j];
	 A[i][j]=A[j][i];
		}
	}
}
for( i=0;i<n;i++){
	for( j=0;j<n;j++){
	 if(i!=j){
	 A[j][i]=O[i][j];	
		}
	}
}

printf("\n");

printf("\tApres: \n");
for( i=0;i<n;i++){
	for( j=0;j<n;j++){
printf("\t%d",A[i][j]);
}
printf("\n");
}
return 0;
}
