# ConnectaTel | Análisis y segmentación de usuarios

**Proyecto académico de Data Analytics (TripleTen)** · Python, pandas, Seaborn y Matplotlib

## Objetivo
Analizar el uso de servicios de una empresa simulada de telecomunicaciones en Latinoamérica, evaluar la calidad de los datos, encontrar valores atípicos y construir perfiles de consumo por usuario, edad y tipo de plan.

## Datos
El notebook utiliza tres archivos:
- `plans.csv`: condiciones de los planes Básico y Premium.
- `users_latam.csv`: perfiles, edades, ciudades, planes y fechas de registro de los usuarios.
- `usage.csv`: registros de llamadas y mensajes.

Los archivos de entrada **no están publicados** aquí y el notebook utiliza rutas `/datasets/` del entorno académico.

## Metodología y herramientas
1. Exploración de estructura, nulos, duplicados y valores inválidos.
2. Tratamiento de edades inválidas y fechas inconsistentes.
3. Creación de indicadores de mensajes, llamadas y minutos por usuario mediante `groupby` y `merge`.
4. Histogramas y diagramas de caja para comparar planes y distribuciones.
5. Detección de outliers con el método IQR y segmentación por edad y nivel de uso.
6. Interpretación ejecutiva y propuestas de segmentación.

## Resultados documentados en el notebook
| Hallazgo | Resultado |
|---|---:|
| Edades con valor inválido -999 | 40 (1.0 % de usuarios) |
| Fechas de registro futuras inconsistentes | 40 (1.0 % de usuarios) |
| Duraciones nulas en eventos | 22,076 (55.2 % de eventos) |
| Longitudes nulas en eventos | 17,896 (44.8 % de eventos) |
| Atípicos en cantidad de mensajes | 46 (1.15 % de usuarios) |
| Atípicos en cantidad de llamadas | 30 (0.75 % de usuarios) |

Las dos últimas categorías de campos nulos se interpretaron según el tipo de evento (llamada o texto), y no se eliminaron indiscriminadamente. Los valores atípicos de actividad se conservaron por resultar plausibles.

En el análisis exploratorio se observa que el plan Básico reúne más usuarios jóvenes y que las distribuciones de uso entre planes no muestran diferencias claras en ciertas métricas. Se propone evaluar campañas dirigidas a usuarios jóvenes para planes Premium; **no se ejecutó ni validó una campaña comercial**.

## Evidencia técnica
**[Abrir notebook de Jupyter con código, gráficos y conclusiones](S7%20Version-Estudiante-Project-ConnectaTel.ipynb)**

[Ver notebook en GitHub](https://github.com/martinatn95-wq/conectatel-analysis/blob/main/S7%20Version-Estudiante-Project-ConnectaTel.ipynb)

## Cómo reproducirlo
1. Abre el notebook en Jupyter o Google Colab.
2. Instala `pandas`, `numpy`, `matplotlib` y `seaborn`.
3. Carga los tres CSV originales y ajusta las rutas de `pd.read_csv`.
4. Ejecuta las celdas en orden.

**Limitaciones:** no se incluyen los CSV y no se ha repetido la ejecución de punta a punta fuera del entorno del curso. Los resultados son de un ejercicio académico con datos de práctica. Las recomendaciones son hipótesis, no mejoras medidas de negocio.

## Autor
Martín Alejandro Toledo Nieto · [GitHub](https://github.com/martinatn95-wq) · [LinkedIn](https://www.linkedin.com/in/martin-toledo-da-cpt/)
