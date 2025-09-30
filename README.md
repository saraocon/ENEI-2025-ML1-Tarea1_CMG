Integrantes:

Ginno Jacinto Castro

Marco Quispe Estrada

Sara Ocon Tovar

Se debe instalar todas las dependencias:

pip install (library)
California dataset
Differences observed between OLS, Ridge, and Lasso,
Tabla comparativa de resultados:

Modelo	MSE (test)	R² (test)	α óptimo
OLS	0.5250	0.6100	–
Ridge	0.5294	0.62	2.5
Lasso	0.5175	0.65	0.0020
El modelo OLS alcanzó un R² de aproximadamente 0.61 y un MSE de 0.52. Ridge, con un valor de 
α
 aproximado de 2.5, redujo ligeramente el MSE a 0.53 y mejoró la generalización mediante la regularización L2, que atenúa la magnitud de los coeficientes sin eliminarlos. Lasso, con 
α
 = 0.0020, obtuvo el menor MSE (0.5294) y aplicó regularización L1, lo que permitió que algunos coeficientes se aproximaran a cero. Se concluye que Lasso tiene un mejor desempeño predictivo.


Los resultados muestran que la tasa de aprendizaje influye principalmente en la velocidad de convergencia. Con lr=0.1, el algoritmo necesitó 319 iteraciones para alcanzar un MSE de 0.2613 en entrenamiento (0.27297 en prueba). Con lr=0.5, la convergencia se logró en 127 iteraciones, con un MSE de 0.2604 en entrenamiento (0.27092 en prueba). El incremento de la tasa de aprendizaje permitió entrenar más rápido sin comprometer la precisión final. Los coeficientes obtenidos fueron similares en ambos casos, indicando estabilidad en la solución.

How k-fold cross-validation influenced the choice of regularization strength.
La validación cruzada k-fold permitió seleccionar de manera óptima los parámetros de regularización (
α
) para Ridge y Lasso, evaluando su desempeño promedio en múltiples particiones del conjunto de entrenamiento. Los valores elegidos, (
α
 
≈
 2.5) para Ridge y 
α
=
0.0020
 para Lasso, lograron un MSE en los datos de prueba de 0.5175 y 0.5294, respectivamente. Este procedimiento garantiza que la elección de la fuerza de regularización no dependa de una única división de los datos, mejorando la generalización del modelo y asegurando un balance adecuado entre sesgo y varianza.
