# Converter PDF Word Images

Herramienta desarrollada en Python para convertir automáticamente documentos PDF en archivos Word (.docx), preservando la apariencia visual original de cada página.

El programa detecta automáticamente un archivo PDF en la misma carpeta donde se encuentra el script, convierte cada página en una imagen de alta resolución y genera un documento Word donde cada imagen ocupa una página completa.

---

## Características

* Detección automática de archivos PDF en el directorio de trabajo.
* Conversión de cada página del PDF a imágenes PNG de alta resolución.
* Generación automática de documentos Word (.docx).
* Inserción de una página del PDF por cada página del documento Word.
* Conservación de la apariencia visual original del documento.
* Ajuste automático de las imágenes al tamaño de la hoja.
* Uso del mismo nombre del PDF para generar el archivo Word resultante.
* No requiere configuración manual de rutas.

---

## Estructura del Proyecto

```text
converter-pdf-word-images/
│
├── converter.py
├── documento.pdf
├── documento.docx
│
├── assets/
│   └── workflow.png
│
└── imagenes_temporales/
    ├── pagina_001.png
    ├── pagina_002.png
    └── ...
```

---

## Flujo de Trabajo

![Flujo de trabajo](assets/workflow.png)

---

## Requisitos

* Python 3.9 o superior
* PyMuPDF
* python-docx
* Pillow

---

## Instalación

Instalar las dependencias necesarias:

```bash
pip install pymupdf python-docx pillow
```

O utilizando el archivo de requisitos:

```bash
pip install -r requirements.txt
```

---

## Uso

Coloca el archivo PDF en la misma carpeta donde se encuentra el script:

```text
converter.py
mi_documento.pdf
```

Ejecuta el programa:

```bash
python converter.py
```

Al finalizar, se generará automáticamente un documento Word en la misma carpeta:

```text
mi_documento.docx
```

---

## Funcionamiento

El proceso realizado por el programa es el siguiente:

1. Buscar automáticamente el primer archivo PDF disponible en el directorio actual.
2. Convertir cada página del PDF en una imagen PNG.
3. Crear un nuevo documento Word.
4. Insertar las imágenes generadas en el documento, una por página.
5. Guardar el archivo Word utilizando el mismo nombre que el PDF original.

---

## Resumen del Proceso

```text
Archivo PDF
      │
      ▼
Conversión a imágenes PNG
      │
      ▼
Creación del documento Word
      │
      ▼
Inserción de imágenes
      │
      ▼
Generación del archivo DOCX
```

---

## Tecnologías Utilizadas

* Python
* PyMuPDF
* python-docx
* Pillow

---

## Casos de Uso

Este proyecto puede resultar útil para:

* Convertir PDFs escaneados a documentos Word conservando su formato visual.
* Generar versiones DOCX de documentos académicos.
* Automatizar procesos de digitalización documental.
* Preparar documentos para edición o distribución en formato Word.

---

## Licencia

Este proyecto se distribuye con fines educativos, de aprendizaje y automatización de tareas.
