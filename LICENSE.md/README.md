/*
* Porgrama: Menu de repaso de estructuras 1
* Fecha: 21 de agosto del 2017
* Elaborado por: Andres Felipe Farfan Hernandez
*/

#include <stdio.h>
#include <conio.h>
#include <stdlib.h>
#include <time.h>

// Funcion principal del programa
int main() 
{ 
	int n;
	
	do
	{
		// Opciones del menu
		printf("************MENU************\n");
		printf("1.Ciclo While\n");
		printf("2.Ciclo For\n");
		printf("3.Arreglos\n");
		printf("4.Switch\n");
		printf("5.Matrices\n");
		printf("6.Estructuras o Registros\n");
		printf("7.Punteros\n");
		printf("0.Salir\n");
		printf("*****************************\n");
		printf("Ingrese una opcion: ");
		scanf("%d",&n);
		
		switch(n)
		{
			char p;
		case 1:
		{
			
			do
			{
				// Opciones del Ciclo While
				fflush(stdin);  
				printf("************Ciclo While************\n");
				printf("a.Sumar los numeros del 1 al 100\n");
				printf("b.Sumar los números pares del 1 al 50\n");
				printf("c.Sumar los números impares del 1 al 50\n");
				printf("s.SALIR\n");
				printf("*************************************\n");
				printf("Ingrese una opcion: ");
				scanf("%c",&p);
				
				
				switch(p)
				{
				case 'a':
				{
					int cont=1; 
					int sumatoria = 0; 
					
					while(cont<=100) 
					{ 
						sumatoria = sumatoria + cont;
						cont++;
					} 
					printf("La sumatoria de los numeros del 1 al 100 es igual a: %d\n", sumatoria);
					break;
					
				}
				
				case 'b':
				{
					int cont = 1; 
					int sumatoria = 0; 
					//int n= 2;
					
					while(cont <= 50) 
					{
						if(cont % 2 == 0)
						{
							sumatoria = sumatoria + cont;
						}
						
						cont++;
					} 
					
					printf("La sumatoria de los numeros pares del 1 al 50 es igual a: %d\n", sumatoria); 
					break;
					
				}
				
				case 'c':
				{
					int cont = 1; 
					int sumatoria = 0; 
					//int n= 2;
					
					while(cont <= 50) 
					{
						if(cont % 2 == 1)
						{
							sumatoria = sumatoria + cont;
						}
						
						cont++;
					} 
					
					printf("La sumatoria de los numeros impares del 1 al 50 es igual a: %d\n", sumatoria); 
					break;
					
				}
				case 's':
				{
					break;  
				}
				
				
				default:
				{
					printf("Error al digitar\n");
				}
				
				}
			}while(p != 's'); 
			break;
		}
		case 2:
		{
			
			do
			{
				// Opciones del Ciclo For
				fflush(stdin);
				printf("************Ciclo For************\n");
				printf("a.Imprimir las tablas de multiplicar de un número, del 1 al 20\n");
				printf("b.Solucionar el factorial de un número\n");
				printf("c.Solucionar el número de Fibonacci\n");
				printf("s.SALIR\n");
				printf("*************************************\n");
				printf("Ingrese una opcion: ");
				scanf("%c",&p);
				
				
				switch(p)
				{
				case 'a':
				{
					int i,num,total;
					printf("tabla del numero: ");
					scanf("%d",&num);
					
					for(i=1;i<=20;i++)
					{
						total = num * i;
						printf("%d x %d = %d\n",num,i,total);
						
					}
					break;
					
				}
				
				case 'b':
				{
					int i,num,temp;
					printf("ingrese el numero factorial: ");
					scanf("%d",&num);
					
					temp = num-1;
					for(i=temp;i>=1;i--)
					{
						num = num * i;
					}
					printf("El Factorial es: %d\n",num);
					break;
					
				}
				
				case 'c':
				{
					int a,i,fin,ant=0,des=1;
					
					printf("cuantas veces desea el Fibonacci:");
					scanf("%d",&a);
					
					for(i=0;i<=a;i++)
					{
						fin = ant + des;
						ant = des;
						des = fin;
						printf("%d\n",fin);
					}
					break;
				}
				case 's':
				{
					break;  
				}
				
				default:
				{
					printf("Error al digitar\n");
				}
				
				}
			}while(p != 's'); 
			break;
		}
		case 3:
		{
			
			do
			{
				// Opciones de arreglos
				fflush(stdin);
				printf("************Arreglos************\n");
				printf("a.Declara un array de numéricos decimales e introduce...\n");
				printf("b.Pedirle al usuario que ingrese dos valores, y de acuerdo a los valores...\n");
				printf("c.Crear un arreglo de dimensión 4x4, y pedirle al usuario que ingrese 4 números...\n");
				printf("s.SALIR\n");
				printf("*************************************\n");
				printf("Ingrese una opcion: ");
				scanf("%c",&p);
				
				
				switch(p)
				{
				case 'a':
				{
					float a[3]={32.583,11.239,22.237};
					int i;
					
					for(i=0;i<3;i++)
					{
						
						printf("el valor del arreglo a es: %.3f",a[i] );
						printf("\n");
						
					}
					break;
					
				}
				
				case 'b':
				{
					int i,n,m,fin,j,band=0,band1=0;
					printf("ingrese el primer valor: ");
					scanf("%d",&n);
					printf("ingrese el segundo valor: ");
					scanf("%d",&m);
					fin=n * m;
					int x[fin];
					
					for(i=0;i<=fin;i++)
					{
						if(band==0&&band1==0)
						{
							x[i]=0;
							band=1;
							band1=1;
							
						}
						
						else
						{
							x[i]=1;
							band=0;
							band1=0;
						}
						
						
					}
					
					
					for(j=0;j<fin;j++)
					{
						printf("%d ",x[j]);
						
					}
					break;	
					
				}
				
				case 'c':
				{
					int a[4][4];
					int m,j,k;
					
					for(k=0;k<=3;k++)
					{
						
						printf("ingresar los numeros: ");
						scanf("%d",&a[k][0]);
						
					}
					for(j=0;j<=3;j++)
					{
						
						a[j][1] = a[j][0]*a[j][0];
						a[j][2] = a[j][0]*a[j][0]*a[j][0];
						a[j][3] = a[j][0]*a[j][0]*a[j][0]*a[j][0];
						
					}
					
					for(m=0;m<=3;m++)
					{
						
						printf("mostrar datos ingresados %d",a[m][0] );
						printf("\n");
						printf("mostrar datos ingresados al cuadrado %d",a[m][1] );
						printf("\n");
						printf("mostrar datos ingresados al cubo %d",a[m][2] );
						printf("\n");
						printf("mostrar datos ingresados elevado a la cuarta %d",a[m][3] );
						printf("\n");
					}
					break;	
				}
				case 's':
				{
					break;  
				}
				
				default:
				{
					printf("Error al digitar\n");
				}
				
				}
			}while(p != 's'); 
			break;
		}
		case 4:
		{
			do
			{   
				// Opciones de Switch
				fflush(stdin);
				printf("************Switch************\n");
				printf("a.Consultar el mes del sistema e imprimir el mes en español\n");
				printf("b.Crear un programa que devuelva el código ascii de una vocal ingresada\n");
				printf("c.Crear un programa que devuelva el código ascii de un número ingresado del 0 al 9\n");
				printf("s.SALIR\n");
				printf("*************************************\n");
				printf("Ingrese una opcion: ");
				scanf("%c",&p);
				
				
				switch(p)
				{
				case 'a':
				{
					struct tm *tiempo;
					int mes;
					
					
					time_t fecha_sistema;
					time(&fecha_sistema);
					tiempo=localtime(&fecha_sistema);
					
					mes=tiempo->tm_mon +1;
					
					switch(mes)
					{
					case 1:
					{       
						printf("El mes es Enero\n");
						break;
					}
					case 2:
					{       
						printf("El mes es Febrero\n");
						break;
					}
					case 3:
					{
						printf("El mes es Marzo\n");
						break;
					}
					case 4:
					{
						printf("El mes es Abril\n");
						break;
					}
					case 5:
					{
						printf("El mes es Mayo\n");
						break;
					}
					case 6:
					{
						printf("El mes es Junio\n");
						break;
					}
					case 7:
					{
						printf("El mes es Julio\n");
						break;
					}
					case 8:
					{
						printf("El mes es Agosto\n");
						break;
					}
					case 9:
					{
						printf("El mes es Septiembre\n");
						break;
					}
					case 10:
					{
						printf("El mes es Octubre\n");
						break;
					}
					case 11:
					{
						printf("El mes es Noviembre\n");
						break;
					}
					case 12:
					{
						printf("El mes es Diciembre\n");
						break;
					}
					default:
					{
						printf("Error\n");
						break;
					}
					
					
					}
					break;
				}
				case 'b':
				{
					char opcion;
					int codigo;
					
					printf("ingresar una vocal: ");
					scanf("%s", &opcion);
					
					switch(opcion)
					{
					case 'a':
					{       
						codigo = 97;
						printf("el codigo ascii de la vocal a es: %d" , codigo);
						break;
					}
					case 'e':
					{
						codigo = 101;
						printf("el codigo ascii de la vocal e es: %d" , codigo);
						break;
					}
					case 'i':
					{
						codigo = 105;
						printf("el codigo ascii de la vocal i es: %d" , codigo);
						break;
					}
					case 'o':
					{
						codigo = 111;
						printf("el codigo ascii de la vocal o es: %d" , codigo);
						break;
					}
					case 'u':
					{
						codigo = 117;
						printf("el codigo ascii de la vocal u es: %d" , codigo);
						break;
					}
					}
					break;
				}
				
				case 'c':
				{
					int opcion;
					int codigo;
					
					printf("ingresar una vocal: ");
					scanf("%d", &opcion);
					
					switch(opcion)
					{
					case 0:
					{       
						codigo = 48;
						printf("el codigo ascii del numero 0 es: %d" , codigo);
						break;
					}
					case 1:
					{       
						codigo = 49;
						printf("el codigo ascii del numero 1 es: %d" , codigo);
						break;
					}
					case 2:
					{
						codigo = 50;
						printf("el codigo ascii del numero 2 es: %d" , codigo);
						break;
					}
					case 3:
					{
						codigo = 51;
						printf("el codigo ascii del numero 3 es: %d" , codigo);
						break;
					}
					case 4:
					{
						codigo = 52;
						printf("el codigo ascii del numero 4 es: %d" , codigo);
						break;
					}
					case 5:
					{
						codigo = 53;
						printf("el codigo ascii del numero 5 es: %d" , codigo);
						break;
					}
					case 6:
					{
						codigo = 54;
						printf("el codigo ascii del numero 6 es: %d" , codigo);
						break;
					}
					case 7:
					{
						codigo = 55;
						printf("el codigo ascii del numero 7 es: %d" , codigo);
						break;
					}
					case 8:
					{
						codigo = 56;
						printf("el codigo ascii del numero 8 es: %d" , codigo);
						break;
					}
					case 9:
					{
						codigo = 57;
						printf("el codigo ascii del numero 9 es: %d" , codigo);
						break;
					}
					}
				}
				case 's':
				{
					break;  
				}
				
				default:
				{
					printf("Error al digitar\n");
					break;
				}
				break;
				}
			}while(p != 's'); 
			break;
		}
		
		case 5:
		{
			
			do
			{
				// Opciones de matrices
				fflush(stdin);
				printf("************Matrices************\n");
				printf("a.Crear una matriz de 3x3 donde el usuario completa sus valores desde el teclado...\n");
				printf("b.Crear una matriz de 3x3 y llenarla de manera automática por el sistema\n");
				printf("c.Crear una matriz de 3x3 y llenarla de manera automática por el sistema con números primos.\n");
				printf("s.SALIR\n");
				printf("*************************************\n");
				printf("Ingrese una opcion: ");
				scanf("%c",&p);
				
				
				switch(p)
				{
				case 'a':
				{
					int a[3][3];
					int i,m,j,k,cont=0;
					
					for(j=0;j<=2;j++)
					{ 
						for(k=0;k<=2;k++)
						{
							
							printf("ingresar los numeros: ");
							scanf("%d",&a[j][k]);
							
						}
					}
					
					for(i=0;i<=2;i++)
					{ 
						for(m=0;m<=2;m++)
						{
							cont = a[i][m]+cont;
							printf("conteo de posiciones: %d\n",cont);
							
						}
					}
					
				}
				
				case 'b':
				{
					int a[3][3];
					int i,m,j,k;
					
					srand(time(NULL));
					
					for(j=0;j<=2;j++)
					{ 
						for(k=0;k<=2;k++)
						{
							a[j][k] = 1+rand()%100;
							
						}
					}
					
					for(i=0;i<=2;i++)
					{ 
						for(m=0;m<=2;m++)
						{
							printf("%d\n",a[i][m]);
						}
					}
					break;
				}
				
				case 'c':
				{
					int pri[8],i,a,j,p,k,m,h;
					int matriz[3][3];
					
					srand(time(NULL));
					
					a=0;
					
					for(j=0;j<=8;j++)
					{
						a=0;
						
						pri[j]=1+rand()%50;
						
						
						for(i=1;i<=pri[j];i++)
						{
							if(pri[j]%i==0)
							{
								a++;
							}
							
							
						}
						
						
						if(a==2)
						{
							printf("El número %d es primo\n",pri[j]);
							
							
						}
						else
						{
							j--;
						}
						
					}
					
					j=0;
					for(p=0;p<=2;p++)
					{ 
						for(k=0;k<=2;k++)
						{
							matriz[p][k] = pri[j];
							j++;
						}
					}	
					
					j=0;
					for(h=0;h<=2;h++)
					{ 
						for(m=0;m<=2;m++)
						{
							printf("Posicion %d = %d\n",j,matriz[h][m]);
							j++;
						}
					}
				}
				case 's':
				{
					break;  
				}
				
				default:
				{
					printf("Error al digitar\n");
					break;
				}
				
				}
			}while(p != 's'); 
			break;
			
		}
		case 6:
		{
			
		}
		
		case 0:
		{
			break;
		}
		default:
		{
			printf("Error al digitar\n");
			break;
		}
		}
		
		
	} while(n != 0);
	
	return 0;
}



