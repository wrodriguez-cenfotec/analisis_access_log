# Práctica: Análisis de access.log y detección de anomalías

Libreta de práctica para los estudiantes del curso CIB-209 Tópicos Especiales de Seguridad de los Datos y Sistemas

## Cómo ejecutar en Binder

1. Abrir el repositorio en Binder con el botón de abajo (reemplazar USUARIO/REPO por la ruta real del repositorio).

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/USUARIO/REPO/HEAD)

2. La primera carga tarda unos minutos mientras se construye el entorno. Tener paciencia.
3. Adjuntar el archivo access.log en el mismo directorio de la libreta. El código asume ese nombre exacto.
4. Ejecutar las celdas en orden, de arriba hacia abajo.
5. La sesión de Binder es temporal. Antes de cerrar, descargar la libreta o guardar capturas de los resultados.


## Qué hace la libreta

- Parsea el access.log en formato NGINX combined a una tabla ordenada por tiempo.
- Grafica las solicitudes por minuto para ver la forma global del tráfico.
- Detecta los picos de forma automática con un detector tipo PersistAD de la librería ADTK, con un respaldo equivalente por si el entorno trae una versión de pandas incompatible. Ambos usan los mismos parámetros window y c.
- Separa la señal por código de estado, por dirección IP y por volumen de bytes para caracterizar cada pico.

## Recursos

- ADTK, documentación. https://adtk.readthedocs.io/
- mybinder. https://mybinder.org/
