# Algoritmos-Trimestre1-y-Trimestre2-Matias-Batallas

  Algoritmo Adivina_Numero
  
    	Definir intentos,num_secreto,num_ingresado Como Real; //Define las variables.
    	num_secreto <- azar(100)+1; intentos<-0;					//Número secreto.
    	Escribir "Adivine el número (entero, del 1 al 100):";
	    Leer num_ingresado;										//Pide adivinar el número.
  	  Mientras num_secreto<>num_ingresado Hacer
	    	Si num_secreto>num_ingresado Entonces
	    		Escribir "El número que ingresó es muy bajo";
	      	SiNo 												//Indica si es bajo o alto.
		    	Escribir "El número que ingresó es muy alto";
    		FinSi
    		intentos <- intentos+1;								//Suma intentos.
    		Leer num_ingresado;
    	FinMientras
    	Escribir "Adivinaste el número en ", intentos+1," intentos.";
    FinAlgoritmo


OTRO

Algoritmo CalcularPromedio
  	// Declarar el vector y las variables
  	Definir vector Como Entero
  	Definir suma Como Real
  	Definir promedio Como Real
  	Definir i Como Entero
  	// Inicializar la suma en 0
  	suma <- 0
  	// Solicitar al usuario ingresar 15 números flotantes
  	Para i<-1 Hasta 15 Hacer
  		Escribir 'Ingrese el número ', i, ': '
  		Leer vector
  		// Acumular la suma de los números
  		suma <- suma+vector
  	FinPara
  	// Calcular el promedio
  	promedio <- suma/15
  	// Mostrar el promedio
	  Escribir 'El promedio de los números ingresados es: ', promedio  
  FinAlgoritmo


OTRO

  Algoritmo sin_titulo
	  Definir N,A Como Caracter;
	  Definir T1,T2,T3,PA Como Real;
	  Escribir 'ingresar nombre de estudiantes';
	   Leer N;
  	Escribir 'ingresar nombre de la asignatura';
  	Leer A;
  	Escribir 'Ingresar clalificación quimestral';
  	Leer T1,T2,T3;
  	PA <- (T1+T2+T3)/3;
  	Si P>=7 Entonces
  		Escribir 'El estudiante ',N,'Aprobo la asignatira de',A,'con un promedio de ',PA
  	SiNo
  		Si P>=7 Y P>=4 Entonces
  			Escribir 'El estudiante ',N,'Esta supletorio en la asignatura',A,'con un promedio de ',PA
  		SiNo
  			Escribir 'El estudiante ',N,'Reprobo la asignatura',A,'con un promedio de ',PA
		FinSi
  	FinSi
  FinAlgoritmo

OTRO
  

Algoritmo sin_titulo
	definir num como entero;
	escribir "ingrese su numero ";
	LEER NUM;
	Si num>0 Entonces;
	
		escribir " su numero es positivo";
	SiNo
			Si num<0 Entonces;
				escribir"su numero es negativo" ;
			SiNo
				escribir " el numero es neutro";
			Fin Si
		FinSi
FinAlgoritmo


OTRO
                              Algoritmo sin_titulo
      	Definir ingresado, letras, guion Como Caracter;	//ingresado=letra ingresada  letras=letra por letra.
    	  Definir fallos, a, b, fallosp, aciertos Como entero; Dimension letras(14), guion(14);	//a y b son para los bucles.
      	Definir encontrado Como Logico; aciertos<-0;		//Da un valor de 0 a los aciertos.
      	letras(0)<-"n";	letras(1)<-"i";	letras(2)<-"t";	letras(3)<-"r";	letras(4)<-"o";
      	letras(5)<-"g";	letras(6)<-"l";	letras(7)<-"i";	letras(8)<-"c";	letras(9)<-"e";
      	letras(10)<-"r";	letras(11)<-"i";  letras(12)<-"n";	letras(13)<-"a"; fallos<-0; //Da un valor de 0 a fallos.
      	Escribir "Bienvenido al juego de ahorcado, ingrese la palabra letra por letra, tiene un máximo de 7 errores";
      	Escribir " ";			//Deja un espacio para la pista.
       	Escribir "La palabra secreta es un compuesto utilizado para la fabricación de dinamita y es altamente explosivo";
      	Escribir "Además, este compuesto reacciona con un mínimo golpe";
      	Escribir " ";			//Deja un espacio para los guiones bajos.
      	Esperar 8 Segundos;
      	Para a<-0 hasta 13 Con Paso 1 Hacer
      		guion(a)<-"_ ";						//Asigna "_" a guion.
      	FinPara
      	Repetir
      		Esperar 4 segundos;
      		Borrar Pantalla;
	      	Escribir "Ingrese la letra que usted crea que está en la palabra";
	      	Escribir " "; //Deja un espacio para los guiones y las letras.
  	    	Para a<-0 hasta 12 Con Paso 1 Hacer
  		    	Escribir guion(a) Sin Saltar; 	//Escribe guion (un guion o una letra) 13 veces.
  	  	  FinPara
      		Escribir guion(13);		//Escribe guion(13): si lo pongo en Sin Saltar, lee la letra al lado de los guiones (se ve mal)
    		Leer ingresado;							//Lee la letra ingresada.
      		ingresado<-Minusculas(ingresado);		//transforma la letra en minúscula
      		encontrado<-falso; fallosp<-0;			//Resetea encontrado, y los fallos a una letra (fallosp)
      		Repetir
      			para b<-0 Hasta 13 Con Paso 1 Hacer
	      			Si ingresado=letras(b) Entonces
		      			guion(b)<-letras(b);			//Si está en la palabra, reemplaza un guion por esa letra en su respectivo lugar.
	                SiNo
            fallosp<-fallosp+1;			//Sino, suma un fallo a la letra.
		      
              FinSi
  	     FinPara
	  
        si fallosp=14 Entonces
      				fallos<-fallos+1;				//Si la letra ingresada <> a ninguna letra, entonces suma un fallo.
      				encontrado<-Verdadero;
  	    			Escribir "La letra que ingresaste no pertenece a la palabra";
  	    		SiNo
  	    			encontrado<-Verdadero;			//Sino, sale del bucle y cuenta un acierto.
  	    			aciertos<-aciertos+1;
	  	      	FinSi
    		Hasta Que encontrado=Verdadero
    	Hasta Que fallos>7 o aciertos=10		//Si ha fallado más de 7 veces o ha acertado 10 veces gana o pierde respectivamente.
    	Si aciertos=10 Entonces
    		Borrar Pantalla;
	    	Escribir "Nitroglicerina";			//Muestra la palabra y da a saber que ha ganado.
    		Escribir " ";
    		Escribir "Felicidades, adivinaste la palabra";
        	SiNo
  	  	Escribir "Lo siento, perdiste";	//Informa al usuario que ha perdido.
    	FinSi  
        FinAlgoritmo








        

OTRO
            
                
                              Proceso Rompecabezas_letras
  	Definir letras, ingresado, almacen Como Caracter; //Define las variables de caracteres
  	Definir a, b  Como Entero;			//Define las variables auxiliares (para los bucles)
  	Dimension letras(12);					//Letras es para la palabra, ingresado es la palabra ingresada.
  	letras(0)<-"O"; 	letras(1)<-"r"; 	letras(2)<-"n"; 	letras(3)<-"i";
  	letras(4)<-"t"; 	letras(5)<-"o"; 	letras(6)<-"r"; 	letras(7)<-"r";
  	letras(8)<-"i"; 	letras(9)<-"n"; letras(10)<-"c"; letras(11)<-"o";
  	Para b<-0 hasta 3 Hacer
  		Para a<-0 hasta 10 Hacer
  			Si letras(a)>letras(a+1) Entonces
  				almacen<-letras(a+1);
  				letras(a+1)<-letras(a);				//Se usa el bucle y "almacen" para cambiar el orden de las letras.
  				letras(a)<-almacen;
  			FinSi
  		FinPara
    	FinPara
  	Para a<-11 hasta 1 Con Paso -1 Hacer
  		Escribir letras(a), " " Sin Saltar;		//Escribe las letras.
  	FinPara										//Si pongo todas las letras "Sin saltar" se unirá con el mensaje que pide
  	Escribir letras(0);							//que ingrese la palabra, por eso aquí se ingresa la última letra.
  	Escribir "Ingrese una palabra a partir de las letras mezcladas.";
  	Leer ingresado;									//Pide que ingrese la palabra y la lee.
  	Si ingresado="ornitorrinco" o ingresado="Ornitorrinco" Entonces
  		Escribir "La palabra es correcta: la solución es Ornitorrinco";
  	SiNo											//Verifica que la palabra sea correcta y le informa al usuario si lo es o no.
    		Escribir "Esa no es la solución, esa palabra es incorrecta";
	  FinSi
  FinProceso        
              
    

