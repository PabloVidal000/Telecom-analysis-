# Telecom-analysis-
Análisis de Comportamiento de Clientes - ConnectaTel
#  Análisis de una empresa de telecomunicaciones (ConnectaTel)

¡Hola! En este proyecto nos pusimos en los zapatos de un equipo de analistas de datos en **ConnectaTel** (una empresa ficticia que opera en Latinoamérica). Nuestra misión fue entender qué pasa realmente con el uso que los clientes le dan a sus servicios móviles (llamadas y mensajes), detectando patrones de consumo, comportamientos extraños y diferencias clave entre sus planes.

---

##  ¿Qué datos usamos?
Trabajamos combinando tres fuentes de información principales:
1. **`plans.csv`**: El catálogo con los planes disponibles (precios, minutos y gigas incluidos, además de tarifas por consumo extra).
2. **`users_latam.csv`**: Los datos demográficos y contractuales de los clientes (edad, ciudad, fecha de registro y tipo de plan).
3. **`usage.csv`**: El registro transaccional de la actividad de cada usuario (si fue llamada o texto, fechas, duración y longitud).

---

## ¿Cómo abordamos el análisis?
El proyecto siguió un flujo paso a paso muy ordenado:
1. **Exploración inicial**: Cargamos las librerías (`pandas`, `numpy`, `matplotlib`, `seaborn`) y revisamos las tablas para entender con qué nos íbamos a enfrentar.
2. **Revisión de calidad**: Buscamos valores nulos, revisamos proporciones y detectamos posibles inconsistencias.
3. **Limpieza de datos**: Ajustamos tipos de fecha, tratamos los nulos (como los de clientes activos o los estructurales de uso) y corregimos valores fuera de lugar.
4. **Resumen por usuario**: Agrupamos la actividad transaccional por cada `user_id` para tener un perfil consolidado por cliente.
5. **Visualización y Outliers**: Armamos histogramas y gráficos de caja (*boxplots*) por plan para entender las distribuciones de edad y consumo, evaluando límites con el método IQR.
6. **Segmentación**: Clasificamos a los usuarios por **nivel de uso** (Bajo, Medio, Alto) y por **edad** (Joven, Adulto, Adulto Mayor).
7. **Insights y Conclusiones**: Tradujimos los gráficos y números en recomendaciones reales para el negocio.

---

##  Principales descubrimientos
- **El plan Smart manda**: Arrasa con el **70.2%** de la base de usuarios, mientras que el plan **Ultra** se queda con el **29.8%**, manteniendo una distribución de edades bastante equilibrada en ambos.
- **Canales tradicionales en baja**: Gran parte de la base se concentra en la categoría de "Bajo uso" debido a la inactividad en llamadas y mensajes de texto tradicionales, lo que demuestra que los usuarios hoy prefieren volcarse al internet y datos móviles.
- **¿Qué recomendamos?** 
  - Ajustar la oferta comercial orientándola mucho más hacia el consumo de datos.
  - Lanzar campañas para incentivar de forma atractiva la migración de usuarios hacia el plan Ultra.

---

##  ¿Cómo ejecutar este proyecto?
Puedes revisar el código directamente o correrlo en tu entorno favorito:

1. Clona este repositorio o descarga los archivos.
2. Asegúrate de tener Python y las librerías necesarias instaladas:
   ```bash
   pip install pandas numpy matplotlib seaborn
