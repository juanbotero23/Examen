# Examen
#include<iostream>
#include<math.h>
#define pi 3.141516

int main(){
	int MRF;
	
	printf("Elija entre las opciones lo que desee realizar: \n 1.Calcular raices de polinomio de 2do grado\n 2.Calculo del area de un circulo y el volumen de una esfera\n 3.Calcular desplazamiento de un movimiento rectilineo uniformemente variado\n ");
	scanf("%d", &MRF);
	
	switch(MRF)
	{
		case 1: printf("Calculadora de raices de polinomios de 2do grado"); 
		
		float a,b,c,x,x1,x2,discriminante,i;
  
  printf("\t\t\nIntroduce los valores de tu ecuacion:");
  printf("\t\t\n A: ");
  scanf("%f",&a);
  printf("\t\t\n B: ");
  scanf("%f",&b);
  printf("\t\t\n C: ");
  scanf("%f",&c); 
  
  discriminante=(pow(b,2)-(4*a*c));
  
  
  if(discriminante>0){
  printf("\t\t Esta ecuacion tiene dos valores reales\n"); 
  x1=(-b+sqrt(discriminante))/(2*a);
  x1=(-b-sqrt(discriminante))/(2*a);
  printf("\t\t El valor de x1 es %.2f \n: ",x1);
  printf("\t\t El valor de x2 es %.2f \n: ",x2);
  
  }
  else
  {
  if(discriminante<0){
  printf("\t\t Esta ecuacion tiene dos valores imaginarios\n");
  discriminante=sqrt(discriminante*(-1));
  discriminante=discriminante/(2*a);
  x=(-b)/(2*a);
  printf("\t\t El x1 es: %.2f+%.2fi",x,discriminante);
  printf("\t\t El x2 es: %.2f-%.2fi",x,discriminante);
  //printf("\t\t El discriminante es: %.2fi",discriminante);
  
  }
  else
  {
  if(discriminante==0){
  printf("\t\t Esta ecuacion tiene un solo valor\n"); 
  
  if(a==0)
  {
  printf("\t\t El sistema esta indeterminado\n");
  }
  else
  {
  x1=(-b)/(2*a);
  printf("\t\t El valor de x1 es %.2f \n: ",x1);
  }
  }
  }
  }
  
	 break;
	
	case 2: printf("Calculo del area de un circulo y el volumen de una esfera en cms...");
	
		float volumen, area, radio;
	
	printf("\nDame la medida del radio: ");
	scanf("%f", &radio);
	
	area = pi * radio * radio;
	printf("El area de el circulo es: %.2f cms\n",area);
	
	volumen = (4.0/3.0) * pi * (radio * radio * radio);
	printf("El volumen de la esfera es %.2f cm cubicos\n",volumen);
	
	break;
	
	case 3: printf("Desplazamiento de un movimiento rectilineo uniformemente variado");
	
		float xo, vo, t, ace;
	
	printf("\nIntroduzca la posicion inicial: "); scanf("%f", &xo);
	printf("\nIntroduzca la velocidad inicial: "); scanf("%f", &vo);
	printf("\nIntroduzca el tiempo: "); scanf("%f", &t);
	printf("\nIntroduzca la aceleracion: "); scanf("%f", &ace);
	
	printf("\nLa posicion lineal es %f", xo + vo * t +((0.5)* ace * t *t));

	break;
	
	default: printf("Opcion no valida");
	}
	return 0;
}
