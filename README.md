# TFM_Cancer_Colorrectal_SEER
Código fuente en R (RMarkdown) para el Trabajo Final de Máster: "Diferencias según el sexo en las características clínico-patológicas y la supervivencia en cáncer colorrectal". UOC-UB, 2026.

# Diferencias según el sexo en las características clínico-patológicas y la supervivencia en cáncer colorrectal: estudio retrospectivo poblacional basado en la base de datos SEER

Este repositorio contiene el código fuente en R utilizado para el Desarrollo del Trabajo Final de Máster (TFM) de **Aaron Pérez Gigante**, correspondiente al Máster Universitario en Bioinformática y Bioestadística (UOC-UB, 2026).

## Contenido del Repositorio
* `Código_TFM_APG.Rmd`: Script principal en RMarkdown con todo el análisis bioestadístico, preprocesado de datos, modelos de Cox y Random Survival Forest.

---

## Instrucciones de Reproducibilidad y Datos

Por motivos de privacidad y debido a las estrictas restricciones del acuerdo de uso de datos (**Data Use Agreement**) de la base de datos SEER, **los datos crudos analizados (`BD_APG.txt`) no están incluidos en este repositorio público**.

Para poder reproducir o auditar este análisis en su equipo local, por favor siga estos pasos:

1. **Solicitar acceso** y descargar la cohorte correspondiente de pacientes con cáncer colorrectal (periodo de diagnóstico 2004-2022) directamente desde el portal oficial de SEER.
2. **Descargar los datos de SEER** Seguir los pasos del punto 3.4 para obtener los mismos datos de SEER. 
3. **Descargar el archivo** `Código_TFM_APG.Rmd` de este repositorio y guardarlo en la carpeta de su elección.
4. **Modificar la ruta de datos (IMPORTANTE):** El script original utiliza una ruta local absoluta para cargar la base de datos. Antes de ejecutar el código en RStudio, localice el bloque de carga de datos en las primeras líneas del archivo `.Rmd` y modifique la ruta por la de su directorio local:

   * **Línea original en el código:**
     ```R
     bd_TFM <- read_tsv("C:/Users/Aaron/Documents/UOC/TFM/BD_APG.txt", ...)
     ```
   * **Debe cambiarla por la ruta donde guardó su archivo .txt:**
     ```R
     bd_TFM <- read_tsv("SU_RUTA_LOCAL/BD_APG.txt", ...)
     ```

5. **Ejecutar el script** de forma secuencial en RStudio. Asegúrese de tener instaladas todas las librerías biomédicas y estadísticas requeridas en el código (como `survival`, `randomForestSRC`, `tableone`, entre otras).
