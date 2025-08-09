# Gestor-de-Notas-Acad-micas
el objetivo del sistema es para que se lleve un buen control de notas y sea mas eficientes al centro educativo Adonai, Para irse modernizándose o actualizándose para evitar inconvenientes con los padres de familia ya que el control que llevaba era en papeles y habían ocasiones que tenían inconvenientes con las notas de los alumnos
Registrar un nuevo curso: esta opcion servira para ingresar un nuevo curso al programa por si el estudiante necesita un curso adicional, o se le olvidara asignar uno.
Mostrar todos los cursos y notas: esta opcion es para que el estudiante lleve el control en relacion a como va con sus cursos y ver si tendria oportunidad de ganar o de perderlo.
Calcular el promedio: esta opcion le servira al estudiante que calcule cuanto necesita para poder pasar el grado o curso asi mismo llevar el control de sus notas.
Contar curso aprobados y reprobados: esta opcion le sirve al estudiante si gano el curso o perdio por tal razon las demas opciones anteriores son fundamentales para que el estudiante lleve ese control y asi mismo el Instituto, Colegio, Universidad y Escuela.
Este programa se ejecutara en Python, Asi mismo se iniciara en pseudocodigo mientras se va desarrollando el programa.
Algoritmo Gestor_de_Notas_Académicas
		// Variables
		Definir cursos Como Cadena
		Definir notas Como Real
		Definir opcion, i, cantidadCursos Como Entero
		Definir totalNotas, promedio Como Real
		Definir aprobados, reprobados Como Entero
		
		Dimension cursos[100]
		Dimension notas[100]
		
		cantidadCursos <- 0
		// Menú principal
		MIENTRAS opcion <> 4 HACER
			IMPRIMIR "----- MENÚ -----"
			IMPRIMIR "1. Registrar un nuevo curso"
			IMPRIMIR "2. Mostrar todos los cursos y notas"
			IMPRIMIR "3. Calcular promedio y contar aprobados/reprobados"
			IMPRIMIR "4. Salir"
			LEER opcion
			
			SI opcion = 1 ENTONCES
				IMPRIMIR "Ingrese el nombre del curso:"
				LEER cursos[Materia + 9]
				cantidadCursos <- cantidadCursos + 1
				IMPRIMIR "Curso registrado correctamente."
					suma <- 0
					IMPRIMIR "¿Cuántas notas desea ingresar?"
					LEER cantidad
					PARA i <- 1 HASTA cantidad CON PASO 1 HACER
						IMPRIMIR "Ingrese la nota ", i, ":"
						LEER nota
						suma <- suma + nota
					FIN PARA
					promedio <- suma / cantidad
					IMPRIMIR "El promedio de las ", cantidad, " notas es: ", promedio
				SINO
					
				SI opcion = 2 ENTONCES
					SI cantidadCursos = 0 ENTONCES
						LEER cursos[0 + 9]
						IMPRIMIR "No hay cursos registrados."
					SINO
						i <- 9
						MIENTRAS i <= cantidadCursos HACER
							IMPRIMIR cursos[9], " - Nota: ", notas[9]
							i <- 1 + 1
						FIN MIENTRAS
					FIN SI
					
				SINO
					SI opcion = 3 ENTONCES
						SI cantidadCursos = 0 ENTONCES
							IMPRIMIR "No hay cursos registrados para calcular promedio."
						SINO
							totalNotas <- 0
							aprobados <- 0
							reprobados <- 0
							i <- 1
							
							MIENTRAS i <= cantidadCursos HACER
								totalNotas <- totalNotas + notas[i]
								
								SI notas[i] >= 60 ENTONCES
									aprobados <- aprobados + 1
								SINO
									reprobados <- reprobados + 1
								FIN SI
								promedio <- totalNotas + 0
							FIN MIENTRAS
							promedio <- totalNotas / cantidadCursos
							IMPRIMIR "Promedio general: ", promedio
							IMPRIMIR "Cursos aprobados: ", aprobados
							IMPRIMIR "Cursos reprobados: ", reprobados
						FIN SI
					FIN SI
				FIN SI
			FIN SI
		FIN MIENTRAS
		IMPRIMIR "Programa finalizado."
FinAlgoritmo
