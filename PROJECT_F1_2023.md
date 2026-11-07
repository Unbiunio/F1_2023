# F1 2023 Analytics — Alonso vs Verstappen

## 1. Descripción del proyecto

Desarrollar un proyecto completo de Data Science utilizando datos reales de la temporada 2023 de Fórmula 1.

Los protagonistas serán:

- Fernando Alonso — Aston Martin.
- Max Verstappen — Red Bull Racing.

El proyecto tendrá dos grandes partes:

**Parte I:** análisis exploratorio, estadístico y de telemetría de toda la temporada 2023.

**Parte II:** desarrollo de una aplicación web interactiva para explorar los resultados y comparar a ambos pilotos.

El objetivo es combinar aprendizaje técnico, análisis deportivo, ingeniería de datos y desarrollo de software.

El proyecto debe tener calidad suficiente para publicarlo en GitHub, compartirlo en LinkedIn y presentarlo durante entrevistas profesionales.

## 2. Fuentes de datos

Investigar y evaluar:

- FastF1.
- OpenF1 API.
- Datos oficiales de Fórmula 1.
- Documentación y resultados oficiales de la FIA.
- Otros datasets públicos fiables.

Priorizar FastF1 como fuente inicial.

Comprobar:

- Disponibilidad de datos de 2023.
- Cobertura de las sesiones.
- Variables disponibles.
- Calidad y frecuencia de muestreo.
- Valores ausentes.
- Limitaciones de precisión.
- Condiciones de uso y publicación.

Utilizar datos reales y documentar claramente las fuentes.

No inventar valores ni presentar estimaciones como mediciones oficiales.

## 3. PARTE I — Análisis de la temporada 2023

### Práctica transversal de Python y SQL

Python y SQL se practicarán desde las primeras fases y con una frecuencia similar; SQL no se pospondrá hasta la fase de almacenamiento. Cuando una pregunta analítica se preste a ello, resolveremos el mismo problema con pandas y SQL, comparando los resultados y razonando qué enfoque resulta más claro.

Utilizaremos DuckDB para consultar DataFrames con SQL cuando sea conveniente, evitando la necesidad de configurar un servidor de base de datos al principio. La práctica SQL crecerá progresivamente e incluirá filtros y agregaciones, JOIN, GROUP BY, HAVING, subconsultas, CTE y funciones de ventana, aplicados a preguntas reales sobre sesiones, pilotos, vueltas y resultados.

Los ejercicios alternarán entre ambas herramientas e incluirán repasos breves. No se mostrarán consultas completas antes de que el usuario lo intente: se ofrecerán pistas y apoyo para corregir errores. El seguimiento registrará por separado los avances y dificultades de Python y SQL.

### Fase 1. Preparación del entorno

Objetivos:

- Configurar Python y el entorno virtual.
- Instalar las bibliotecas necesarias.
- Crear la estructura del repositorio.
- Introducir Git.
- Configurar FastF1.
- Descargar una primera sesión.
- Explorar los datos con pandas.
- Practicar consultas SQL desde el inicio, utilizando DuckDB sobre un DataFrame si resulta conveniente.

Trabajar progresivamente mediante ejercicios alternos de Python y SQL. Cuando sea adecuado, explorar la misma información con pandas y con SQL.

### Fase 2. Caso de estudio: Mónaco 2023

Comenzaremos con la clasificación del Gran Premio de Mónaco 2023.

Resultados de Q3:

- Verstappen: 1:11.365.
- Alonso: 1:11.449.
- Diferencia: 0,084 segundos.

**Pregunta principal: ¿dónde consiguió Verstappen las 84 milésimas que le dieron la pole?**

Análisis previstos:

1. Extraer las vueltas rápidas de ambos pilotos.
2. Comparar los tiempos totales.
3. Analizar los tres sectores.
4. Obtener las telemetrías.
5. Comparar velocidad a lo largo del circuito.
6. Analizar el uso del acelerador.
7. Comparar las zonas de frenada.
8. Analizar las marchas utilizadas.
9. Comparar las RPM.
10. Representar las diferencias sobre el trazado.
11. Estimar la evolución de la diferencia de tiempo.
12. Identificar las curvas y sectores más relevantes.

Intercalar ejercicios SQL sobre las vueltas, pilotos y sectores de la sesión. Por ejemplo, practicar filtros, agregaciones y comparaciones entre pilotos; cuando tenga sentido, formular la pregunta también con pandas y comprobar que ambos resultados coinciden.

Visualizaciones:

- Gráficos de velocidad frente a distancia.
- Acelerador frente a distancia.
- Freno frente a distancia.
- RPM y marchas.
- Diferencias de tiempo acumuladas.
- Mapas del circuito.
- Comparación de sectores.

Explicar las limitaciones del análisis: interpolación, sincronización de telemetrías, resolución de los datos y diferencias entre coches.

Distinguir siempre las vueltas reales de las vueltas ideales calculadas a partir de mejores sectores.

### Fase 3. Análisis completo del campeonato

Ampliar el proyecto a los 22 Grandes Premios de la temporada 2023.

Comparar:

- Resultados de clasificación.
- Posiciones de salida.
- Resultados de carrera.
- Puntos obtenidos.
- Podios.
- Diferencias entre posiciones de salida y llegada.
- Tiempos por vuelta.
- Ritmo de carrera.
- Consistencia.
- Degradación de neumáticos, cuando pueda estimarse razonablemente.
- Estrategias de paradas.
- Evolución del rendimiento.
- Diferencias por tipo de circuito.
- Incidencias y condiciones especiales.

No atribuir automáticamente las diferencias al talento del piloto, ya que competían con vehículos distintos.

Controlar, cuando sea posible, factores como neumáticos, tráfico, meteorología, banderas y condiciones de pista.

### Fase 4. Ingeniería y almacenamiento de datos

Profundizar en SQL de forma práctica, construyendo sobre los ejercicios con DuckDB y DataFrames de las fases anteriores.

Evaluar DuckDB o PostgreSQL.

Diseñar una base de datos que permita almacenar:

- Grandes Premios.
- Circuitos.
- Pilotos.
- Sesiones.
- Resultados.
- Vueltas.
- Sectores.
- Neumáticos.
- Telemetrías seleccionadas.

Aprender:

- Diseño de tablas.
- Relaciones.
- Claves primarias y foráneas.
- JOIN.
- Agregaciones.
- Subconsultas.
- CTE.
- Funciones de ventana.
- Consultas analíticas.
- Calidad de datos.

Avanzar progresivamente por JOIN, GROUP BY, HAVING, subconsultas, CTE y funciones de ventana mediante ejercicios relacionados con preguntas reales del campeonato. Mantener el uso de pandas como punto de comparación cuando aporte valor.

Evitar almacenar datos duplicados o grandes volúmenes de telemetría sin necesidad.

### Fase 5. Estadística y análisis avanzado

Aplicar:

- Estadística descriptiva.
- Distribuciones.
- Medidas de dispersión.
- Correlaciones.
- Comparación de grupos.
- Análisis de tendencias.
- Detección de valores atípicos.
- Visualización de incertidumbre.

Plantear hipótesis y comprobarlas con métodos apropiados.

Explicar las limitaciones derivadas del tamaño de muestra y de las diferencias entre vehículos y circunstancias de carrera.

### Fase 6. Machine Learning e IA

Evaluar si existen aplicaciones justificadas para Machine Learning.

Posibles investigaciones:

- Predicción exploratoria de tiempos por vuelta.
- Agrupación de circuitos según características.
- Identificación de patrones de rendimiento.
- Detección de vueltas atípicas.
- Estimación de tendencias de degradación.

Elegir modelos según los datos disponibles.

Aprender:

- Preparación de variables.
- División entrenamiento/prueba.
- Validación temporal cuando corresponda.
- Prevención de data leakage.
- Selección de modelos.
- Métricas de evaluación.
- Interpretabilidad.
- Limitaciones.

No incorporar modelos únicamente para aparentar complejidad.

Si una técnica estadística sencilla resuelve mejor el problema, priorizarla.

## 4. PARTE II — Aplicación interactiva

### Objetivo

Crear una aplicación denominada provisionalmente:

**F1 2023 — Alonso vs Verstappen Analytics Dashboard**

La aplicación permitirá explorar los resultados del análisis y comparar a ambos pilotos.

### Funcionalidades

El usuario podrá:

- Seleccionar a Alonso o Verstappen.
- Comparar ambos pilotos.
- Seleccionar un Gran Premio.
- Elegir clasificación o carrera.
- Consultar estadísticas de temporada.
- Visualizar posiciones y puntos.
- Comparar vueltas y sectores.
- Explorar gráficos de telemetría.
- Analizar velocidad, acelerador y freno.
- Visualizar mapas de circuitos.
- Consultar resultados estadísticos.
- Explorar modelos predictivos, si se desarrollan.

### Tecnologías propuestas

- Python.
- pandas.
- SQL.
- Streamlit.
- Plotly.
- FastF1.
- Git y GitHub.

Evaluar posteriormente:

- FastAPI.
- Docker.
- Servicios Cloud.
- Automatización de pipelines.
- Herramientas de testing.

Comenzar con una arquitectura sencilla y ampliable.

### Diseño visual

Buscar un aspecto profesional inspirado en herramientas de ingeniería de competición.

Incluir:

- Panel general de temporada.
- Comparador de pilotos.
- Análisis por Gran Premio.
- Comparador de vueltas.
- Visualizaciones interactivas.
- Indicadores clave.
- Explicaciones de resultados.

No sacrificar claridad ni rendimiento por efectos visuales innecesarios.

### Desarrollo progresivo

Construir primero una versión mínima funcional (MVP).

Después incorporar funcionalidades adicionales.

No desarrollar todo el dashboard de una sola vez.

## 5. Calidad y reproducibilidad

El proyecto deberá incluir:

- Código organizado.
- Entorno reproducible.
- Gestión de dependencias.
- Documentación técnica.
- README en inglés.
- Fuentes de datos.
- Metodología.
- Pruebas básicas.
- Resultados reproducibles.
- Limitaciones.
- Gráficos.
- Aplicación funcional.

Evitar subir secretos, credenciales, archivos corporativos o datasets cuya redistribución no esté permitida.

## 6. GitHub y LinkedIn

El proyecto debe servir como demostración profesional de mis habilidades.

Preparar:

- Repositorio público bien documentado.
- README con imágenes y explicación.
- Capturas del dashboard.
- Resultados relevantes del análisis.
- Explicación de tecnologías utilizadas.
- Descripción de problemas resueltos.
- Demostración de la aplicación.

Identificar oportunidades para publicar avances en LinkedIn.

Ejemplos:

- Análisis de las 84 milésimas de Mónaco.
- Comparación de consistencia en carrera.
- Evolución de rendimiento durante 2023.
- Presentación del dashboard.

No publicar conclusiones sin respaldo de datos.

## 7. Metodología de trabajo

Seguir las instrucciones generales de `AGENTS.md`.

Para cada fase:

1. Explicar el objetivo.
2. Presentar los conocimientos necesarios.
3. Proponer un ejercicio práctico.
4. Esperar mi solución.
5. Revisar mi trabajo.
6. Explicar errores y mejoras.
7. Comprobar que he aprendido.
8. Actualizar `PROGRESS.md` cuando corresponda.
9. Pedir confirmación antes de avanzar.

No generar el proyecto completo automáticamente.

Alternar la práctica de Python y SQL durante todas las fases y reflejar por separado ambas habilidades en el seguimiento de aprendizaje.

## 8. Primeros pasos

Antes de escribir código:

1. Confirmar la disponibilidad de telemetrías de Mónaco 2023.
2. Evaluar las bibliotecas y dependencias necesarias.
3. Proponer una estructura inicial sencilla.
4. Diseñar una hoja de ruta por fases.
5. Identificar las habilidades que aprenderé.
6. Preparar el primer ejercicio de Python y FastF1.

**Primer objetivo práctico: descargar, explorar y comprender los datos de la clasificación de Mónaco 2023.**

Después compararemos las vueltas rápidas de Alonso y Verstappen y ampliaremos progresivamente el análisis al campeonato completo.
codex pue