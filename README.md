# ADA2-Arreglos
import numpy as np
import time

# Crear una matriz de calificaciones aleatorias para 100 alumnos en 6 materias
np.random.seed(0)
calificaciones = np.random.randint(0, 101, size=(100, 6))

# Función para buscar la calificación de un alumno en una materia específica
def buscar_calificacion(alumno, materia):
    return calificaciones[alumno - 1, materia - 1]

# Función para buscar todas las calificaciones de un alumno
def buscar_calificaciones_alumno(alumno):
    return calificaciones[alumno - 1, :]

# Función para buscar todas las materias de una materia específica
def buscar_materias(materia):
    return calificaciones[:, materia - 1]

# Buscar calificación del alumno 95 en la materia 5
calificacion_95_materia_5 = buscar_calificacion(95, 5)
print("Calificación del alumno 95 en la materia 5:", calificacion_95_materia_5)

# Buscar todas las calificaciones del alumno 95
calificaciones_alumno_95 = buscar_calificaciones_alumno(95)
print("Todas las calificaciones del alumno 95:", calificaciones_alumno_95)

# Buscar todas las materias de la materia 5
materias_materia_5 = buscar_materias(5)
print("Todas las materias de la materia 5:", materias_materia_5)

# Medir el tiempo de ejecución para poner las 6 materias en fila y los 100 alumnos en columnas
start_time = time.time()
calificaciones_alumnos_en_fila = np.random.randint(0, 101, size=(6, 100))
print("Tiempo de ejecución (materias en fila, alumnos en columnas):", time.time() - start_time)

# Medir el tiempo de ejecución para poner los 100 alumnos en fila y las 6 materias en columnas
start_time = time.time()
calificaciones_materias_en_fila = np.random.randint(0, 101, size=(100, 6))
print("Tiempo de ejecución (alumnos en fila, materias en columnas):", time.time() - start_time)


Coclusión: Este programa utiliza la biblioteca NumPy para trabajar con matrices de manera eficiente. Realiza las búsquedas requeridas y también mide el tiempo de ejecución para ambas disposiciones de la matriz, donde las filas representan a los alumnos y las columnas representan a las materias, y viceversa. Puedes ejecutar este programa y comparar los tiempos de ejecución para ver cuál disposición es más rápida en tu entorno de ejecución específico. En general, el rendimiento puede variar según la implementación de Python y la biblioteca utilizada para matrices. Puedes ejecutar el código en tu entorno para obtener resultados específicos. para mi se me facilito mas el poner los 100 alumnos en filas y las materias en columnas.
