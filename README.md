# Proyecto de Scraping y Limpieza de Datos de Booking.com

Este proyecto contiene un Jupyter Notebook (`transform.ipynb`) diseñado para realizar dos tareas principales:

1.  **Limpieza de Datos**: Procesa y limpia datos de archivos locales (`.csv` y `.xlsx`) relacionados con ingresos y reservas de un hostal.
2.  **Web Scraping**: Extrae todas las reseñas de un hotel específico en Booking.com utilizando Selenium y las guarda en formato JSON.

---

## Características

- **Limpieza de Datos de Ingresos**: Lee un archivo `reporte de ingreso año 2024 a la fecha.csv`, limpia la columna de valores monetarios y la convierte a formato numérico.
- **Limpieza de Datos de Reservas**: Lee un archivo `Book2.xlsx`, procesa y estandariza los nombres de las habitaciones.
- **Scraping de Reseñas**: Navega a la página de reseñas de "Absolute & Hostel Boutique" en Booking.com, maneja pop-ups y paginación, y extrae detalles de cada reseña (nombre, país, puntuación, título, comentarios, etc.).
- **Exportación de Datos**: Guarda las reseñas extraídas en archivos JSON (uno por página y uno con el total) y finalmente las convierte a un archivo Excel (`Book3.xlsx`).

---

## Requisitos

Para ejecutar este notebook, necesitas tener Python y las siguientes librerías instaladas:

```bash
pip install pandas selenium webdriver-manager openpyxl
```

También necesitas tener Google Chrome instalado, ya que `webdriver-manager` lo descargará y gestionará automáticamente.

---

## Uso

1.  **Asegúrate de tener los archivos de entrada**:
    *   `reporte de ingreso año 2024 a la fecha.csv`
    *   `Book2.xlsx`
    en el mismo directorio que el notebook.

2.  **Abre y ejecuta el Jupyter Notebook**:
    *   Abre `transform.ipynb` en un entorno de Jupyter (como Jupyter Lab o VS Code).
    *   Ejecuta las celdas en orden.

3.  **Resultados**:
    *   El script creará un directorio llamado `booking_scraper_output` donde guardará las reseñas en formato JSON.
    *   El archivo final con todas las reseñas procesadas se guardará como `Book3.xlsx`.
