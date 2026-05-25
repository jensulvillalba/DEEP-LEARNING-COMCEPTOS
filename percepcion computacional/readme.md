# Sistema de Percepción Computacional mediante YOLOv8

Proyecto académico desarrollado para la asignatura de **Percepción Computacional**, enfocado en el reconocimiento y tratamiento de imágenes mediante técnicas de visión por computador e inteligencia artificial.

---

# Descripción del Proyecto

Este proyecto implementa un sistema de detección automática de personas en múltiples imágenes utilizando el modelo **YOLOv8** de Ultralytics y herramientas de procesamiento de imágenes en Python.

El sistema permite:

- Cargar múltiples imágenes.
- Detectar personas automáticamente.
- Contar personas en cada imagen.
- Visualizar resultados en pantalla.
- Exportar resultados a un archivo CSV.
- Ejecutarse en Google Colab o entorno local.

---

# Tecnologías Utilizadas

- Python
- Google Colab
- OpenCV
- Ultralytics YOLOv8
- NumPy
- CSV

---

# Objetivo del Proyecto

Desarrollar un sistema de percepción computacional capaz de identificar y procesar información visual de manera automatizada utilizando técnicas modernas de detección de objetos.

---

# Funcionamiento del Sistema

El flujo del sistema se desarrolla en las siguientes etapas:

1. Instalación automática de dependencias.
2. Carga de imágenes.
3. Validación de archivos.
4. Carga del modelo YOLOv8.
5. Procesamiento de imágenes.
6. Detección de personas.
7. Conteo de objetos detectados.
8. Visualización de resultados.
9. Exportación de resultados en CSV.

---

# Modelo Utilizado

Se utilizó el modelo:

```python
YOLO("yolov8n.pt")
```

La versión **YOLOv8 Nano** fue seleccionada por:

- rapidez de procesamiento,
- bajo consumo de recursos,
- buena precisión en detección de objetos.

---

# Estructura del Proyecto

```bash
/project
│
├── Percepción.ipynb
├── percepción.py
├── resultados_personas.csv
├── evidencias/
└── README.md
```

---

# Instalación

## Clonar el repositorio

```bash
git clone https://github.com/TU-USUARIO/TU-REPOSITORIO.git
```

## Instalar dependencias

```bash
pip install ultralytics opencv-python
```

---

# Ejecución en Google Colab

1. Abrir el notebook `Percepción.ipynb`.
2. Ejecutar todas las celdas.
3. Subir imágenes cuando el sistema lo solicite.
4. Esperar el procesamiento automático.
5. Descargar el archivo CSV generado.

---

# Resultados

El sistema genera:

- detección visual de personas,
- conteo automático,
- imágenes procesadas,
- archivo CSV con resultados.

Ejemplo del CSV generado:

| Imagen | Cantidad_Personas | Fecha_Procesamiento |
|---|---|---|
| imagen1.jpg | 3 | 2026-05-25 |
| imagen2.jpg | 1 | 2026-05-25 |

---

# Evidencias

El proyecto incluye capturas de pantalla del procesamiento y resultados obtenidos durante la ejecución del sistema.

---

# Google Colab

Agregar aquí el enlace de Google Colab:

```text
https://colab.research.google.com/
```

---

# Aplicaciones del Proyecto

Este sistema puede aplicarse en:

- monitoreo de aforos,
- seguridad,
- vigilancia inteligente,
- análisis de espacios públicos,
- automatización visual.

---

# Conclusiones

El proyecto permitió aplicar conceptos de visión por computador y percepción computacional utilizando modelos modernos de inteligencia artificial.

La implementación de YOLOv8 demostró una alta eficiencia para tareas de detección de personas en múltiples escenarios, automatizando el procesamiento y análisis de imágenes.

---

# Referencias

- https://docs.ultralytics.com/
- https://opencv.org/
- https://www.python.org/
- https://colab.research.google.com/

---

# Autores

- Laura Balentina Amado Valencia
- Jensul Villalba Gaitan
- Miguel Angel Cordoba Figueroa
- Harold Daniel Duque Castaneda

---

# Curso

Percepción Computacional

---

# Licencia

Proyecto académico con fines educativos.
