# Procesamiento y análisis de señales fisiológicas y cinemáticas

## Descripción

Este repositorio contiene el componente computacional desarrollado en el marco de una **tesis de maestría**, orientado al procesamiento, análisis y visualización de datos experimentales relacionados con señales fisiológicas y variables cinemáticas.

El proyecto implementa un flujo de trabajo sistemático para la organización, validación, procesamiento y análisis de diferentes tipos de señales, incluyendo **electrocardiografía (ECG), frecuencia cardíaca (HR), intervalos RR, saturación de oxígeno (SpO₂), electromiografía de superficie (EMG) y variables cinemáticas**.

Los procedimientos desarrollados permiten estructurar los registros de acuerdo con los sujetos, pruebas experimentales y fases de adquisición, manteniendo la trazabilidad de los datos a lo largo de las diferentes etapas del análisis.

El código fue desarrollado principalmente en **Python**, utilizando herramientas del ecosistema científico para procesamiento numérico, análisis de señales, análisis estadístico y visualización. Entre las principales bibliotecas utilizadas se encuentran `NumPy`, `Pandas`, `SciPy`, `Matplotlib`, `Seaborn`, `Statsmodels` y `Scikit-learn`.

---

## Objetivo

El objetivo de este repositorio es documentar el componente computacional empleado durante el desarrollo de la investigación y facilitar la **reproducibilidad, trazabilidad y transparencia del procesamiento y análisis de los datos experimentales**.

El repositorio reúne las rutinas utilizadas para transformar los registros originales en datos procesados, características, análisis estadísticos y representaciones gráficas empleadas en el desarrollo de la tesis.

---

## Notebook principal

El procesamiento se encuentra integrado principalmente en:

```text
TESIS_DATA.ipynb
```

El notebook contiene las diferentes etapas de preparación, procesamiento, análisis y visualización de los datos.

---

## Estructura del procesamiento

El flujo de trabajo implementado en el notebook se organiza en las siguientes etapas:

1. **Configuración del entorno y bibliotecas**
2. **Configuración de rutas de datos**
3. **Inventario y organización de archivos**
4. **Verificación de nombres y estructura de archivos**
5. **Carga y preparación de los datos**
6. **Procesamiento y análisis cinemático**
7. **Procesamiento y análisis de señales sEMG**
8. **Procesamiento y análisis de señales ECG, HR, RR y SpO₂**

## Esta organización corresponde directamente a la estructura de procesamiento implementada en `TESIS_DATA.ipynb`.

## 1. Configuración y preparación de los datos

En las primeras etapas del notebook se configuran las bibliotecas utilizadas, las rutas de acceso a los datos y los directorios destinados al almacenamiento de resultados.

También se realiza un inventario de los archivos disponibles y se construye una estructura de metadatos que permite asociar cada archivo con variables como:

```text
test_id
subject_id
test_type
phase
signal
file_name
path
```

Esta estructura facilita la identificación y trazabilidad de los registros experimentales.

---

## 2. Verificación de archivos

Antes de iniciar el procesamiento, el notebook verifica la estructura y nomenclatura de los archivos correspondientes a las diferentes bases de datos.

Se validan específicamente los conjuntos:

```text
ECG_SPO2_DATA
EMG_DATA
KINEMATICS_DATA
```

La verificación permite detectar archivos que no cumplen con las convenciones de nomenclatura definidas para el proyecto.

---

## 3. Carga de archivos

Una vez validada la estructura, se realiza la carga de los registros experimentales para su posterior procesamiento y análisis.

Esta etapa corresponde a la sección:

```text
5. Cargar archivos
```

del notebook.

---

# Procesamiento de datos cinemáticos

## 4. Datos cinemáticos

El bloque de análisis cinemático se encuentra organizado bajo la sección:

```text
6. DATOS KINEMATIC
```

e incluye diferentes etapas para el procesamiento, representación y análisis de las señales cinemáticas.

### Principales etapas

El procesamiento cinemático incluye:

* utilidades de procesamiento;
* procesamiento de señales cinemáticas;
* visualización de señales;
* resumen de pruebas;
* generación de resultados;
* normalización;
* cálculo de perfiles promedio;
* cálculo de límites promedio de fases normalizadas;
* incorporación de fases promedio;
* análisis bilateral;
* extracción de métricas ROM.

Entre las secciones principales del notebook se encuentran:

```text
6.1. Utilidades de procesamiento cinemático
6.2. Procesamiento de señales cinemáticas
6.3. Visualización de señales cinemáticas
6.4. Visualización de señales cinemáticas
6.5. Visualización de señales cinemáticas
6.6. Resumen de pruebas cinemáticas
6.7. Graficar resultados Kinematics
6.8. Almacenar resultados Kinematics
6.9. Normalización
6.10. Calcular perfil promedio
6.11. Calcular límites promedio de fases normalizada
6.12. Añadir fases promedio a perfiles normalizados
6.13. Graficar perfil promedio de una señal
6.14. Graficar perfil promedio bilateral
6.15. Graficar análisis cinemático promedio
6.16. Resultados graficar análisis cinemático promedio
6.17. Guardar resultados graficar análisis cinemático promedio
6.18. Extraer métricas ROM
6.19. Calcular fase ROM
```

Estas etapas permiten pasar desde los registros cinemáticos individuales hasta perfiles normalizados, representaciones promedio y métricas derivadas del rango de movimiento.

---

# Procesamiento de señales sEMG

## 5. Datos sEMG

El procesamiento electromiográfico se encuentra organizado en la sección:

```text
7. DATOS sEMG
```

El bloque incluye etapas específicas de preparación, preprocesamiento, análisis espectral, extracción de métricas y generación de resultados.

### Principales etapas

El procesamiento sEMG contempla:

```text
7.1. Preparación de señales EMG
7.2. Preprocesamiento de señales EMG
7.3. Visualización de señales EMG
7.4. Visualización de señales EMG
7.5. Visualización de señales EMG
7.6. Análisis espectral de señales EMG
7.7. Extracción de métricas EMG
7.8. Visualización comparativa de métricas EMG
7.9. Tabla resumen de métricas EMG
7.10. Procesamiento de pruebas EMG
7.11. Resumen de pruebas EMG
7.12. Gráficas en el dominio del tiempo
7.13. Almacenar datos sEMG
7.14. Gráficas en el dominio de la frecuencia
7.15. Guardar gráficas en el dominio de la frecuencia
7.16. Gráficas métricas
7.17. Guardar gráficas métricas
7.18. Tabla métricas
7.19. Métricas por fase
```

Este conjunto de procedimientos permite procesar las señales EMG, realizar análisis en los dominios temporal y frecuencial, extraer métricas y organizar los resultados para su comparación entre pruebas y fases experimentales.

---

# Procesamiento de ECG, HR, RR y SpO₂

## 6. Datos ECG y SpO₂

El procesamiento de las señales cardiovasculares y de oximetría se encuentra organizado en:

```text
8. ECG & SPO2 DATA
```

Este bloque contiene las rutinas destinadas a la limpieza, procesamiento temporal, procesamiento de señales ECG, intervalos RR, frecuencia cardíaca y oximetría.

### Principales etapas

```text
8.1. Utilidades de limpieza de datos
8.2. Utilidades temporales
8.3. Procesamiento de señales ECG
8.4. Procesamiento de intervalos RR
8.5. Procesamiento de frecuencia cardíaca
8.6. Procesamiento de oximetría
8.7. Procesamiento de señales
8.8. Verificación de pruebas
8.9. Utilidades de visualización
8.10. Porcentajes temporales de fases
8.11. Visualización de señales fisiológicas
8.12. Resultados ECG & SPO2
8.13. Almacenar resultados ECG & SPO2
8.13. Cálculo de coeficiente de variación
8.14. Extraer segmento por intervalo temporal
8.15. Calcular métricas ECG
8.16. Calcular métricas HR
8.17. Calcular métricas RR
8.18. Calcular métricas SPO2
```

Este bloque permite procesar y caracterizar las diferentes señales fisiológicas, así como generar resultados y métricas asociadas a las condiciones experimentales.

---

# Base de datos

La base de datos utilizada en el desarrollo de la investigación se encuentra disponible en Google Drive:

**[Acceder a la base de datos](https://drive.google.com/drive/folders/1QgDf9aekUkd7llKwzqFCagFk-OI2ngmd?usp=sharing)**

La base de datos contiene los registros experimentales utilizados para el procesamiento de las señales fisiológicas, electromiográficas y cinemáticas.

Se recomienda conservar la estructura original de carpetas y los nombres de los archivos, ya que estos elementos son utilizados por las rutinas de identificación, carga y procesamiento implementadas en el notebook.

---

# Configuración de rutas

## ⚠️ Importante

El notebook fue desarrollado originalmente en **Google Colaboratory (Google Colab)** utilizando archivos almacenados en Google Drive.

Por esta razón, las rutas definidas en `TESIS_DATA.ipynb` corresponden al entorno original de desarrollo y **deben modificarse antes de ejecutar el código en un computador local**.

La ruta principal se define mediante:

```python
BASE_PATH = "/content/drive/Shareddrives/APISI/Database signals/Convocatoria aseo"
```

A partir de esta ruta se construyen las ubicaciones correspondientes a cada conjunto de datos:

```python
ECG_PATH = f"{BASE_PATH}/ECG_SPO2_DATA"
EMG_PATH = f"{BASE_PATH}/EMG_DATA"
KIN_PATH = f"{BASE_PATH}/KINEMATICS_DATA"
```

Estas rutas deben reemplazarse por las ubicaciones correspondientes en el entorno donde se ejecute el proyecto.

```python
BASE_PATH = r"C:\Users\Usuario\Documents\Tesis\Database signals\Convocatoria aseo"

ECG_PATH = f"{BASE_PATH}/ECG_SPO2_DATA"
EMG_PATH = f"{BASE_PATH}/EMG_DATA"
KIN_PATH = f"{BASE_PATH}/KINEMATICS_DATA"
```

## Ejemplo en Windows

```python
BASE_PATH = r"C:\Users\Usuario\Documents\Tesis\Database signals\Convocatoria aseo"

ECG_PATH = f"{BASE_PATH}/ECG_SPO2_DATA"
EMG_PATH = f"{BASE_PATH}/EMG_DATA"
KIN_PATH = f"{BASE_PATH}/KINEMATICS_DATA"

```

## Ejemplo en Linux o macOS

```python
BASE_PATH = "/home/usuario/Documents/Tesis/Database signals/Convocatoria aseo"

ECG_PATH = f"{BASE_PATH}/ECG_SPO2_DATA"
EMG_PATH = f"{BASE_PATH}/EMG_DATA"
KIN_PATH = f"{BASE_PATH}/KINEMATICS_DATA"
```

También deben configurarse las rutas destinadas al almacenamiento de los resultados:

```python
KIN_RESULTS_PATH = f"{BASE_PATH}/Resultados_Kinematics"
EMG_RESULTS_PATH = f"{BASE_PATH}/Resultados_EMG"
ECG_RESULTS_PATH = f"{BASE_PATH}/Resultados_ECG_SPO2"
```

Nota: las rutas que comienzan con /content/drive/ corresponden al entorno de Google Colab y no funcionarán directamente en un entorno local.

# Estructura de directorios

La organización general de los datos utilizada por el proyecto es:

```text
.
├── TESIS_DATA.ipynb
├── README.md
│
├── ECG_SPO2_DATA/
├── EMG_DATA/
├── KINEMATICS_DATA/
│
├── Resultados_ECG_SPO2/
├── Resultados_EMG/
└── Resultados_Kinematics/
```

Los directorios de entrada contienen los registros originales, mientras que los directorios de resultados almacenan los productos derivados del procesamiento y análisis.

# Reproducibilidad

La organización del proyecto está orientada a facilitar la reproducibilidad del análisis computacional desarrollado durante la investigación.

Para obtener resultados consistentes, se recomienda conservar:

- La estructura de las carpetas.
- Los nombres originales de los archivos.
- Los identificadores de sujetos y pruebas.
- Las rutas de entrada y salida.
- Las dependencias utilizadas.
- El orden de ejecución del notebook.

Cualquier modificación en los datos, parámetros de procesamiento o estructura de archivos debe quedar documentada para facilitar la trazabilidad de los resultados.

---

# Consideraciones sobre los datos

La base de datos corresponde a registros experimentales utilizados en una investigación desarrollada en el marco de una tesis de maestría.

El código y la base de datos constituyen recursos relacionados, pero independientes.

> **Importante:** la publicación del código en este repositorio no implica necesariamente autorización para redistribuir, modificar o reutilizar los datos experimentales.

El acceso y utilización de los datos deberá realizarse de acuerdo con las condiciones establecidas para la investigación y con las disposiciones académicas, institucionales y éticas aplicables.

---

# Propósito académico

Este repositorio contiene el componente computacional desarrollado para una **tesis de maestría**.

Su finalidad es documentar los procedimientos empleados para la organización, procesamiento, análisis y visualización de los datos experimentales, proporcionando una referencia para la reproducibilidad y trazabilidad del análisis.

El código debe interpretarse dentro del contexto metodológico de la investigación para la cual fue desarrollado.

---

# Autor

**Stirley Madrid Vélez**

Código desarrollado en el marco de una **tesis de maestría**.

---

# Referencia académica

Cuando este repositorio o sus procedimientos sean utilizados en trabajos académicos, se recomienda citar la tesis asociada y, cuando corresponda, referenciar también este repositorio.

---

# Licencia

La licencia del código deberá establecerse de acuerdo con las condiciones académicas e institucionales aplicables a la tesis y al proyecto de investigación.

> **Nota:** la licencia del código no implica automáticamente una licencia para el uso o redistribución de la base de datos experimental.

