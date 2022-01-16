# core-code
Martes

Java es compilado o interpretado:

Es ambos a la vez. Con el compilador se convierte el código fuente que reside en archivos cuya extensión es .java, a un conjunto de instrucciones que recibe el nombre de bytecodes que se guardan en un archivo cuya extensión es .class. Estas son independientes del tipo de ordenador. El intérprete las ejecuta en un ordenador específico. Solamente es necesario, compilar una vez el programa, pero se interpreta cada vez que se ejecuta en un ordenador.

Crear un algoritmo:
  Pedir al usuario la cantidad de colones que desea convertir a dolares
  Tomar el valor y multiplicarlo por el tipo de cambio actual 
  Guardar ese valor y mostrarlo al usuario
  
  def cambiodivisaadolar():
      cantidad = input("Digite la cantidad de colones que desea convertir")
      if isinstance(cantidad,int):
          resultado = cantidad * 0.0016
          print("El resultado es: ",resutado)
      else:
          print("Digite un número válido")
          return cambiodivisaadolar()
 
 
 Porque el pseudocodigo es util:
 
 Porque se puede escribir de una forma que se sienta uno más familiarizado, donde uno puede poner las reglas sin tener que usar 
 mucho conocimiento tecnico
 
 Crear un pseudocódigo para calcular la edad aproximada de un usuario
 
    START 
    Y <-- 2022
    YB <-- GET
    QY <-- Y-YB
    PRINT QY
    END
  
  Porque los diagramas de flujo son importantes para nosotros como desarrolladores
  
  Son útiles ya que permiten comunicar de una forma gráfica y más simple un proceso complejo, se puede plasmar el funcionamiento de un software 
  por medio de un diagrama, y con esto lograr entenderlo de una manera más simple.
 
 Miércoles
 
 2 Mi año de nacimiento en binario, decimal y hexadecimal
 
 Decimal 1995
 
 Binario 11111001011
 
 Hexadecimal 7cb
 
 3 Convertir 51966 a hexadecimal y binario
 
 hexadecimal cafe
 binario 1100101011111110
 
 5.1 crear un programa para sumar 2 numeros
 
 .data
	number1: .asciiz "\nIngrese el primer numero: "
	number2: .asciiz "\nIngrese el segundo numero: "
.text
	main:
		li $v0, 4
		la $a0, number1
		syscall

		li $v0, 5
		syscall

		move $t0, $v0

		li $v0, 4
		la $a0, number2
		syscall

		li $v0, 5
		syscall

		move $t1, $v0
		
		add $t2, $t0, $t1

		li $v0, 1
		move $a0, $t2
		syscall
    
 5.2 Crear un programa para desplegar el nombre
 
  .data
    message: .asciiz "\nHi my name is Alex\n"
  .text
    main:
      li $v0, 4
      la $a0, message
      syscall
 
 Aplicaciones reales de Javascript
 
 Se puede hacer casi cualquier cosa en javascript, carruseles, galerias de imágenes, diseños fluctuantes, y respuestas a las pulsaciones de botones. 
 Con más experiencia, se pueden crear juegos, animaciones 2D y gráficos 3D, aplicaciones integradas basadas en bases de datos


 
 
Core Code bootcamp
