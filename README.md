# 📊 Proyecto de Análisis Comparativo - AluraStore LATAM

## 📋 Descripción General

Este proyecto constituye un análisis integral de desempeño operativo y financiero de cuatro unidades de negocio del grupo **AluraStore LATAM**. Mediante técnicas de análisis de datos y visualización, se evalúa el rendimiento de cada tienda en términos de facturación, satisfacción del cliente, eficiencia logística y patrones de demanda de productos.

---

## 🎯 Objetivos del Proyecto

1. **Análisis Financiero**: Calcular y comparar los ingresos totales por tienda.
2. **Evaluación de Satisfacción**: Medir la calificación promedio de clientes en cada unidad.
3. **Optimización Logística**: Analizar costos de envío y su impacto en la estructura de costes.
4. **Inteligencia de Productos**: Identificar los productos más y menos vendidos por tienda.
5. **Segmentación de Mercado**: Estudiar la distribución de ventas por categoría de producto.
6. **Análisis Estratégico**: Proporcionar recomendaciones para decisiones de inversión o desinversión.

---

## 📁 Estructura del Datos

El proyecto utiliza cuatro conjuntos de datos independientes (CSV) alojados en repositorio de GitHub:

| Tienda | URL de Datos | Registros |
| :--- | :--- | :---: |
| Tienda 1 | `tienda_1.csv` | ~26K |
| Tienda 2 | `tienda_2.csv` | ~26K |
| Tienda 3 | `tienda_3.csv` | ~26K |
| Tienda 4 | `tienda_4.csv` | ~26K |

### Columnas Principales de Datos

- **Producto**: Nombre del artículo vendido.
- **Categoría del Producto**: Clasificación temática (ej. Electrónica, Ropa, Hogar, etc.).
- **Precio**: Valor de venta unitario del producto.
- **Calificación**: Puntuación otorgada por el cliente (escala 0-5).
- **Costo de envío**: Gasto logístico asociado a la transacción.

---

## 📊 Análisis Realizados

### 1. Análisis de Facturación

Se calculó la suma total de precios por cada tienda, revelando la siguiente jerarquía de ingresos:

```
Tienda 1: $1,150,880,400  (100%)
Tienda 2: $1,116,343,500  (96.9%)
Tienda 3: $1,098,019,600  (95.4%)
Tienda 4: $1,038,375,700  (90.2%)
```

**Hallazgo**: La Tienda 1 lidera con un 10% más de ingresos que la Tienda 4.

### 2. Ventas por Categoría

Se agruparon las ventas por categoría de producto en cada tienda, identificando patrones de demanda consistentes:

- Las categorías presentan una distribución tipo **Pareto** (80/20).
- Pocas categorías concentran la mayor parte del volumen.
- La estructura es similar entre las cuatro tiendas, sugiriendo un mercado homogéneo.

### 3. Calificación Promedio de Clientes

Se computó la media aritmética de las calificaciones:

```
Tienda 3: 4.05 ⭐ (Mejor satisfacción)
Tienda 2: 4.04 ⭐
Tienda 4: 4.00 ⭐
Tienda 1: 3.98 ⭐ (Menor satisfacción)
```

**Hallazgo**: La Tienda 1 tiene la puntuación más baja, a pesar de ser la más rentable.

### 4. Productos Más y Menos Vendidos

Se identificaron los 5 productos con mayor y menor rotación en cada tienda:

- **Más vendidos**: Son consistentes entre tiendas (liderazgo estable).
- **Menos vendidos**: Varían según la tienda, indicando diferencias en preferencias locales.

### 5. Costo Promedio de Envío

Se calculó el promedio de costos logísticos por transacción:

```
Tienda 1: $26,018.61 (Más caro)
Tienda 2: $25,216.24
Tienda 3: $24,805.68
Tienda 4: $23,459.46 (Más económico)
```

**Hallazgo**: Existe una correlación inversa entre ingresos y costos de envío en el grupo.

### 6. Visualizaciones Generadas

- **Gráficos de Barras**: Ventas por categoría de producto (una por tienda).
- **Gráfico de Pastel**: Proporción de calificaciones promedio entre tiendas.

---

## 🔍 Hallazgos Clave

| Métrica | Ganador | Valor | Observación |
| :--- | :--- | :--- | :--- |
| **Ingresos Totales** | Tienda 1 | $1.15B | Liderazgo claro en facturación |
| **Satisfacción del Cliente** | Tienda 3 | 4.05 | Mejor NPS (Net Promoter Score) |
| **Costo de Envío Mínimo** | Tienda 4 | $23,459 | Ventaja competitiva en logística |
| **Eficiencia General** | Tienda 3 | - | Balance óptimo entre ingresos y costes |

---

## 💼 Análisis Estratégico: Recomendación de Venta

Basado en el análisis integral, se presentan dos escenarios viables:

### ✅ Escenario A: Maximización de Valor (Vender la Tienda 1)

**Recomendación**: Si el objetivo es comercializar el activo más valioso.

**Justificación**:
- Mayor volumen de facturación ($1.15B).
- Base de clientes amplia y productos con demanda comprobada.
- Atractiva para inversores externos por su rendimiento.

**Riesgo**: Puntuación de satisfacción más baja require mejoras en servicio.

---

### ⚠️ Escenario B: Optimización del Portafolio (Vender la Tienda 4)

**Recomendación**: Si el objetivo es eliminar ineficiencias operacionales.

**Justificación**:
- Ingresos más bajos ($1.04B, -10% vs. Tienda 1).
- Calificación cercana a la media sin valor diferencial.
- Costos de envío bajos no compensan el bajo rendimiento.

**Alternativa**: Invertir recursos en reactivar esta tienda bajo nuevo modelo de gestión.

---

## 🛠️ Requisitos Técnicos

### Dependencias

```
pandas >= 1.3.0
matplotlib >= 3.4.0
```

### Instalación

```bash
pip install pandas matplotlib
```

---

## 🚀 Cómo Usar el Proyecto

### 1. Clonar o Descargar el Repositorio

```bash
git clone [URL_DEL_REPOSITORIO]
cd AluraStoreLatam
```

### 2. Actualizar URLs de Datos (si aplica)

Las URLs de los archivos CSV están configuradas en el primer bloque de código. Si deseas usar datos locales, reemplaza:

```python
url = "ruta_local/tienda_1.csv"
tienda = pd.read_csv(url)
```

### 3. Interpretar Resultados

- Los gráficos se mostrarán automáticamente.
- Las tablas de resumen actualizarán según los datos.
- Los prints mostrarán métricas clave en consola.