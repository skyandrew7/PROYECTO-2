# PROYECTO-2

## Descripción General

Esta base de datos contiene información sobre siniestros viales y víctimas en un área geográfica específica. Se incluyen detalles sobre las características de los accidentes, los tipos de víctimas, los tipos de vehículos involucrados, la localización de los siniestros, y otros datos clave. Estos datos son útiles para analizar incidentes viales y calcular indicadores de seguridad vial, como la tasa de homicidios en siniestros, accidentes mortales de motociclistas, y accidentes mortales en avenidas.

## Propósito del Dataset

Este conjunto de datos fue diseñado para:

Analizar siniestros viales en la Ciudad Autónoma de Buenos Aires (o región equivalente).
Calcular KPIs relacionados con las víctimas fatales en accidentes de tránsito.
Permitir la visualización interactiva de tendencias y patrones en Power BI.
Facilitar estudios sobre la seguridad vial, con foco en motociclistas y accidentes en avenidas.
Estructura del Dataset
La base de datos tiene las siguientes columnas que describen las características de los siniestros y las víctimas:

## Columnas Clave:
### N_victimas:

Descripción: Indica el vehiculo que ocupaba la persona accidentada al moemento del suceso (e.g., PEATON, PASAJERO, MOTO).
Tipo de dato: Numérico.
Ejemplo de valores: 1, 2.

### AAAA_y:

Descripción: Año en el que ocurrió el accidente.
Tipo de dato: Numérico.
Ejemplo de valores: 2022, 2023.
### MM_y:

Descripción: Mes en el que ocurrió el accidente.
Tipo de dato: Numérico.
Ejemplo de valores: 01 (enero), 12 (diciembre).

###DD_y:

Descripción: Día en el que ocurrió el accidente.
Tipo de dato: Numérico.
Ejemplo de valores: 01, 15.

### LUGAR_DEL_HECHO:

Descripción: Dirección exacta o nombre del lugar donde ocurrió el incidente.
Tipo de dato: Texto.
Ejemplo de valores: AV. SANTA FE Y CALLAO, GRAL PAZ Y BEIRO.

### TIPO_DE_CALLE:

Descripción: Tipo de vía donde ocurrió el accidente (e.g., si fue en una avenida o calle secundaria).
Tipo de dato: Texto.
Ejemplo de valores: AVENIDA, CALLE, GRAL PAZ.


### COMUNA:

Descripción: Comuna de la Ciudad Autónoma de Buenos Aires en la que ocurrió el siniestro.
Tipo de dato: Numérico.
Ejemplo de valores: 1, 13.


###VICTIMA_y:

Descripción: Tipo de víctima involucrada en el accidente (e.g., si fue motociclista, peatón, conductor).
Tipo de dato: Texto.
Ejemplo de valores: MOTO, AUTO, PEATON.

### FALLECIDOS_EN_EL_ACTO:

Descripción: Indica si hubo fallecidos en el lugar del siniestro.
Tipo de dato: Texto.
Ejemplo de valores: SI, NO.

El dataset es adecuado para varios tipos de análisis relacionados con la seguridad vial, incluyendo:

### KPI: Tasa de homicidios en siniestros viales:

Fórmula: (Número total de víctimas fatales / Población total) * 100,000.
Columna utilizada: N_VICTIMAS.

### KPI: Cantidad de accidentes mortales de motociclistas:

Fórmula: (Número de accidentes mortales con motociclistas en el año anterior - Año actual) / Año anterior * 100.
Columna utilizada: VICTIMA_y (filtrar por "MOTO").

### KPI: Accidentes mortales de motociclistas en avenidas:

Fórmula: (Número de accidentes mortales en avenidas con motociclistas en el año anterior - Año actual) / Año anterior * 100.
Columnas utilizadas: VICTIMA_y (filtrar por "MOTO"), TIPO_DE_CALLE (filtrar por "AVENIDA").

### Recomendaciones de Uso
Interactividad: La base de datos es ideal para usarse en dashboards interactivos como Power BI, permitiendo realizar filtros por comuna, tipo de calle, tipo de víctima, etc.
Análisis temporal: Los datos incluyen detalles anuales y mensuales, lo que facilita el análisis de tendencias a lo largo del tiempo.
Análisis geográfico: Usar la columna COMUNA para hacer análisis geográficos, pudiendo representarse en mapas temáticos.


### Recomendaciones adicionales:
Limpiar los datos: Asegúrate de revisar valores atípicos o inconsistentes, como faltantes de información.
Incorporar datos adicionales: Si es necesario, agregar una tabla con la población de las comunas para calcular con precisión la tasa de homicidios en siniestros viales.
Transformaciones de datos: Puedes crear medidas calculadas adicionales en Power BI para obtener análisis más detallados sobre los siniestros viales.
