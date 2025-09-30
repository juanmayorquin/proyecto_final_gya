# Proyecto GyA

Este proyecto contiene un flujo de análisis y visualización de datos utilizando **PostgreSQL**, **Python (Jupyter Notebook)** y **Power BI**.

## Estructura del proyecto

* **content/**

  * `filtrado_2022.csv` → Dataset original. (Debe crearse y añadirse el archivo)
* **docker-compose.yml** → Configuración del contenedor con PostgreSQL.
* **ProyectoGyA.ipynb** → Notebook principal de análisis en Python.
* **GyA_Dashboard.pbix** → Dashboard de Power BI.
* **requirements.txt** → Librerías necesarias para ejecutar el notebook.

---

## Requisitos previos

* Tener instalado **Docker** y **Docker Compose**.
* Tener instalado **Python 3.10+** y **Jupyter Notebook**.
* Tener instalado **Power BI Desktop** (para abrir el archivo `.pbix`).

---

## 1. Levantar la base de datos con Docker

En la raíz del proyecto se encuentra el archivo `docker-compose.yml` con la configuración de la base de datos PostgreSQL.

Ejecute el siguiente comando:

```bash
docker-compose up -d
```

Esto levantará un contenedor de PostgreSQL con las siguientes credenciales:

* **Usuario**: `gya`
* **Contraseña**: `password`
* **Base de datos**: `db`
* **Puerto**: `5432`

La carpeta `pgdata/` almacena los datos de manera persistente.

---

## 2. Instalar dependencias de Python

Antes de ejecutar el notebook, instale las librerías necesarias con el comando:

```bash
pip install -r requirements.txt
```

---

## 3. Ejecutar el Notebook

Con la base de datos corriendo, abra Jupyter Notebook y cargue el archivo:

```bash
jupyter notebook ProyectoGyA.ipynb
```

En este notebook se realiza la conexión a la base de datos, la carga de datos y el análisis.

---

## 4. Visualización en Power BI

Para visualizar los resultados en Power BI:

1. Abra el archivo `GyA_Dashboard.pbix`.
2. Configure la conexión a la base de datos PostgreSQL si es necesario.
3. Explore las visualizaciones y reportes.

---

## 5. Detener el contenedor

Cuando finalice el trabajo, puede detener el contenedor con:

```bash
docker-compose down
```
