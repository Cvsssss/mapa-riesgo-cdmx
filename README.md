# mapa-riesgo-cdmx

Mapa interactivo del índice de riesgo delictivo en la Ciudad de México, del proyecto **riesgo-delictivo-cdmx** del equipo Data Bloom para el cliente simulado SAFEZONE MÉXICO.

**Ver el mapa:** https://TU-USUARIO.github.io/mapa-riesgo-cdmx/

## Qué muestra

- Puntos de color por celda de 1 km: nivel de riesgo **alto**, **medio** o **bajo** según la época del año (mes o semana).
- Las celdas con menos de 10 registros históricos se marcan como "sin información suficiente".
- La tasa ponderada de delitos por 100,000 habitantes de cada alcaldía.

El índice es relativo (percentil frente a las demás celdas del mismo periodo), no una predicción de delitos. Los pesos por tipo de delito son un supuesto del equipo.

## De dónde salen los datos

Los datos salen de las tablas `indice_celda` e `indice_alcaldia` de la **Capa Silver consultable** del proyecto. Se exportaron a CSV y se incrustaron en `index.html`, por lo que el mapa funciona sin servidor ni conexión a AWS. Para actualizarlo hay que volver a generar el archivo desde el repo principal.

Fuentes originales: carpetas de investigación de la FGJ-CDMX (CC BY 4.0) y Censo de Población y Vivienda 2020 del INEGI.

## Repo principal

El pipeline completo (infraestructura, código, ADR y documentación) está en: https://github.com/Cvsssss/CrimenesEnCDMX

## Licencia

GPL-3.0, igual que el repo principal.
