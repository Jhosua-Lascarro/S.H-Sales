# S.H Sales

Pipeline de análisis de datos de ventas con DuckDB y PostgreSQL.

## Descripción

Este proyecto procesa datos de ventas, los transforma en un modelo dimensional y los carga en PostgreSQL para análisis.

## Estructura

```
data/raw/          → Datos originales (Sales.csv)
data/staging/      → Datos limpios (Parquet)
data/curated/      → Modelo dimensional (Parquet)
PostgreSQL         → Base de datos final
```

## Tecnologías

- Python 3.12
- DuckDB
- PostgreSQL 17
- Pandas
- ipykernel
- Docker

## Modelo de Datos

**Dimensiones:**

- cities
- customer_types
- product_types
- sale_types
- customers
- products

**Hechos:**

- sales

## Instalación

### Requisitos

- Docker y Docker Compose
- Git

### Pasos

1. Clonar el repositorio

```bash
git clone https://github.com/Jhosua-Lascarro/S.H-Sales.git
cd S.H-Sales
```

2. Levantar servicios

```bash
docker-compose up -d
```

PostgreSQL: `localhost:5432`

3. Ejecutar notebooks en orden

- `01_data_understanding.ipynb` - Exploración de datos
- `02_cleaning.ipynb` - Limpieza de datos
- `03_data_modeling.ipynb` - Creación de modelo dimensional
- `04_etl_to_database.ipynb` - Carga a PostgreSQL

4. Detener servicios

```bash
docker-compose down
```

## Configuración PostgreSQL

- Base de datos: `analytics`
- Usuario: `user`
- Contraseña: `pass`
- Puerto: `5432`
