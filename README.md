# auth-system-jwt
A scalable and well-structured application built with modern technologies. This project focuses on performance, security, and clean architecture, making it suitable for real-world use.


#  Simple Scraper

Extrae datos de sitios web y los exporta a CSV o JSON con un solo comando.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-4.12-orange)
![License](https://img.shields.io/badge/License-MIT-green)
![Status](https://img.shields.io/badge/Status-Active-brightgreen)

---

##  Características

- Scraping multipágina con navegación automática
- Exporta resultados a **CSV** o **JSON** según configuración
- Configurable sin tocar el código (`config.json`)
- Guarda archivos con timestamp para no sobrescribir resultados
- Manejo de errores de red con mensajes claros

---

## Estructura del proyecto

```
simple-scraper/
├── scraper.py       # Script principal
├── config.json      # URL, formato de salida y número de páginas
├── requirements.txt
├── output/          # Resultados generados (ignorados por Git)
│   └── .gitkeep
└── README.md
```

---

## Instalación y uso

### 1. Clona el repositorio

```bash
git clone https://github.com/tu-usuario/simple-scraper.git
cd simple-scraper
```

### 2. Instala las dependencias

```bash
pip install -r requirements.txt
```

### 3. Configura el scraper

Edita `config.json`:

```json
{
  "url": "https://books.toscrape.com",
  "output_format": "csv",
  "max_pages": 3
}
```

### 4. Ejecuta

```bash
python scraper.py
```

### Ejemplo de salida

```
Scrapeando página 1...
Scrapeando página 2...
Scrapeando página 3...

Total de libros encontrados: 60
Guardado en: output/books_20240315_143022.csv
```

---

## Configuración

| Campo | Descripción | Valores posibles |
|---|---|---|
| `url` | Sitio web a scrapear | Cualquier URL válida |
| `output_format` | Formato de exportación | `csv` o `json` |
| `max_pages` | Número máximo de páginas | Cualquier número entero |

---

## Dependencias

```
requests==2.31.0
beautifulsoup4==4.12.2
```

Instálalas con:

```bash
pip install -r requirements.txt
```

---

## Ejemplo de datos extraídos

| title | price | rating | availability |
|---|---|---|---|
| A Light in the Attic | £51.77 | Three | In stock |
| Tipping the Velvet | £53.74 | One | In stock |
| Soumission | £50.10 | One | In stock |

> Este proyecto usa [books.toscrape.com](https://books.toscrape.com), un sitio creado específicamente para practicar scraping de forma legal y sin restricciones.

---

## Uso responsable

- Revisa siempre el archivo `robots.txt` del sitio antes de scrapearlo
- No hagas demasiadas solicitudes en poco tiempo (respeta los servidores)
- Este proyecto es solo con fines educativos

---

## Roadmap

- [ ] Argumentos por línea de comandos con `argparse`
- [ ] Exportación a Excel con `openpyxl`
- [ ] Reintentos automáticos ante fallos de red
- [ ] Soporte para sitios con JavaScript (Selenium / Playwright)

---

## Contribuciones

¡Las contribuciones son bienvenidas! Si tienes ideas o encuentras un bug:

1. Haz fork del repositorio
2. Crea una rama: `git checkout -b feature/nueva-funcionalidad`
3. Haz commit: `git commit -m "feat: descripción"`
4. Abre un Pull Request

---

## Licencia

Distribuido bajo la licencia MIT. Consulta el archivo `LICENSE` para más detalles.
