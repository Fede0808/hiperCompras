# HiperCompras

Este proyecto busca recomendar la mejor opción de compra de una canasta de productos, considerando la ubicación del usuario, precios de distintos proveedores y las promociones disponibles.

## 🚀 Objetivo MVP
- Definir un modelo de datos para productos, proveedores y promociones.
- Implementar algoritmo de optimización que seleccione el proveedor óptimo.
- Analizar impacto de promociones en el costo total.
- Generar reportes comparativos.

Épica 1 – Configuración e Infraestructura
  Historia 1.1: Configurar entorno de desarrollo (requirements.txt/poetry, Docker opcional).
  Historia 1.2: Definir modelo de datos para productos, precios, ubicaciones y promociones.
  Historia 1.3: Scripting para cargar dataset inicial de proveedores y productos consumiendo los CSV de SEPA.
  
Épica 2 – Búsqueda y Optimización
  Historia 2.1: Implementar algoritmo para obtener precios de un producto por proveedor.
  Historia 2.2: Implementar cálculo de costo total de una canasta en cada proveedor.
  Historia 2.3: Implementar selección de proveedor óptimo en función de la ubicación (ejemplo: menor distancia + costo total).

Épica 3 – Análisis de Promociones
  Historia 3.1: Modelar diferentes tipos de promociones (2x1, descuentos por volumen, % off).
  Historia 3.2: Crear Script que recorra y consolide las promociones de bancos, tarjetas y billeteras virtuales.
  Historia 3.3: Incluir promociones en el cálculo de costo de la canasta.
  Historia 3.4: Comparar ahorro con y sin promociones.

Épica 4 – Visualizaciones (A analizar)
  Historia 4.1: Generar reporte de proveedor óptimo con desglose de costos.
  Historia 4.2: Gráfico comparativo de precios de la canasta entre proveedores.
  Historia 4.3: Mostrar impacto de promociones en costo total.

---

## Tecnologías Utilizadas  

- **Lenguaje:** Python.
- **Fuente de Datos:** PRECIOS CLAROS SEPA
- **Framework de API:** FastAPI.  
- **Base de Datos:** PostgreSQL

