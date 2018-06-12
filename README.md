/*para obtener el menor numero de billetes y monedas de pesos basta con comenzar por el bilete o moneda de mas alto valor.
para obtener el numero o cantidad que hay que tomar de esa moneda o billete se calcula el cociente de la cantidad dividido por el valor.
el resto de la division entera de la cantidad dividido por el valor.
 si se considera el sistema monetario del peso, 
los billetes y monedas son:
 billetes (quinientos, docientos, cien, cincuenta, veinte,) monedas(diez, cinco, dos, uno, cincuentacentavos)
el programa le la cantidad de pesos en una variable real cantidad original. la transformacion a centavos de pesos y se realizan los calculos.
posteriormente se visualizan los resultados.
*/

#include <iostream>

using namespace std;

int main(){

int mil = 1000, quinientos = 500, docientos = 200, cien = 100, cincuenta =50, veinte = 20, diez = 10, cinco = 5,dos = 2, uno = 1;
int cantidad = 0, peso =0, residuo = 0, moneda = 0, x = 0, residuo_dos = 0, residuo_tres = 0, resultado_de_dos = 0, siguiente = 0;	
int resultado_de_cien = 0, cincuenta_menos=0, cincuenta_resulta = 0, veinte_menos = 0, resulta_veinte = 0;
int diez_menos = 0, resulta_diez =0, cinco_menos = 0, resulta_cinco = 0, dos_menos = 0, resulta_dos = 0; 
int uno_menos = 0, resulta_uno = 0;
    
   mil = 1000;
   quinientos = 500;
   docientos = 200;
   cien = 100;
   cincuenta = 50;
   veinte = 20;
   diez = 10;
   cinco = 5;
   dos = 2;
   uno = 1;
   
  cout<<"digite la cantidad de peso:";cin>>cantidad;
   
   peso = cantidad / mil;               //el peso sera cantidad entre mil
   cout<<"\nmil :"<<peso<<endl;                                       //imprime cuantos billetes de 1000 tiene la cantidad digitada
   
   
   
   residuo = cantidad - peso * mil;  //se hace la operacion del residuo cantidad digitada    ----   menos el el total de la cantidad entre mil
    residuo_dos = residuo / quinientos;    //hace la operacion dividiento el sobrante entre la cantidad siguiente que en este caso es quinientos 
   
   cout<<"\nquinientos :"<<residuo_dos<<endl;                        //imprime cuantos billetes de 500 hay en la cantidad digitada depues de  1000
   
  
  
   residuo_tres = residuo - residuo_dos * quinientos;   //se hace la operacion de residuo tres  que resta el residuo resultado de mil menos el resultado de division entre quinientos
   
   resultado_de_dos = residuo_tres / docientos;         //el resultado de dos se toma el residuo de tres y se divide el numero de quinientos
   
   cout<<"\ndocientos :"<<resultado_de_dos<<endl;     //seimprime el el valor de cuantos billetes de docientos hay en la cantidad digitda
   
   
  
   siguiente = residuo_tres - resultado_de_dos *docientos;    //realiza la operacion de siguiente con la finalidad de sacar el resultado de docientos 
   
   resultado_de_cien = siguiente / cien;              //para sacar el resultado de cien se hace la operacion de siguiente que es un resultado de siguiente  y se divide entre cien que va a ser el numero de billetes que se contara
   
   cout<<"\ncien :"<<resultado_de_cien<<endl;     // se imprime la cantidad de billetes que vamos a diitar el numero
   
   
   
   cincuenta_menos = siguiente - resultado_de_cien * cien;    // hace la operacion de cincuenta tomando en cuenta las operaciones anteriores
   
   cincuenta_resulta = cincuenta_menos / cincuenta;         //hace la operacion tomando en cuenta  el resultado de cincuenta_menos dividiendo entre el cincuenta que sera el numero de billetes
   
  cout<<"\ncincuenta :"<<cincuenta_resulta<<endl;     //imprimira el numero de billetes de cincuenta
  
  
  veinte_menos = cincuenta_menos - cincuenta_resulta * cincuenta;  //operacion de resultado de anterior
  resulta_veinte = veinte_menos / veinte;   //el resultado de cincuenta_resulta es la operacion anterio entre veinte
   cout<<"\nveinte :"<<resulta_veinte<<endl;    //imprime la cantidad de billetes de veinte pesos
  
  
  diez_menos = veinte_menos - resulta_veinte * veinte;
  resulta_diez = diez_menos / diez;
  cout<<"\ndiez :"<<resulta_diez<<endl;
  
  
  cinco_menos = diez_menos - resulta_diez * diez;
  resulta_cinco = cinco_menos / cinco;
  cout<<"\ncinco :"<<resulta_cinco<<endl;
  
  
  dos_menos = cinco_menos - resulta_cinco * cinco;
  resulta_dos = dos_menos / dos;
  cout<<"\ndos :"<<resulta_dos<<endl;
  
  
  uno_menos = dos_menos -resulta_dos * dos;
  resulta_uno = uno_menos / uno;
  cout<<"\nuno :"<<resulta_uno<<endl;
  
  
   	
	return 0;
}
