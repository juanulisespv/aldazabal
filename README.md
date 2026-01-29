# Catálogo Digital Aldazabal

Este proyecto es el catálogo digital web para la Joyería Aldazabal. Muestra colecciones de Pendientes, Collares, Anillos y Pulseras de forma interactiva.

## 🚀 Características Técnicas

*   **Diseño Responsivo:** Adaptado a móviles, tablets y escritorio.
*   **Carga Híbrida de Datos:**  Prioriza la lectura de archivos **CSV** (más fáciles de editar) y usa `products.json` como respaldo.
*   **Precarga Inteligente:** Descarga las imágenes del catálogo en segundo plano ("loading por atrás") para una navegación instantánea entre categorías.
*   **Enlaces de Contacto:** Botones `mailto:` optimizados.

## 📋 Cómo Actualizar el Catálogo

El catálogo se alimenta automáticamente de archivos CSV (Excel) situados en la carpeta raíz.

### 1. Archivos de Datos
Existen 4 archivos principales. Puedes editarlos con Excel, Numbers o un editor de texto:

*   `pendientes.csv`
*   `collares.csv`
*   `anillos.csv`
*   `pulseras.csv`

**Si uno de estos archivos falta, la web intentará cargar los datos antiguos del archivo `products.json`.**

### 2. Formato del CSV
El formato debe seguir estrictamente estas columnas (separadas por comas). La primera línea es siempre la cabecera:

```csv
Foto,Referencia,Precio
P-658/A.jpg,Pendiente P-658,81€
...
```

*   **Foto:** Nombre del archivo de imagen.
    *   *Nota:* La web convierte automáticamente las barras `/` en dos puntos `:` para buscar el archivo real.
    *   Ejemplo en CSV: `P-658/A.jpg` -> Busca archivo real: `images/pendientes/P-658:A.jpg`
*   **Referencia:** Nombre visible del producto.
*   **Precio:** Precio visible (incluir símbolo €).

### 3. Imágenes
Las imágenes deben guardarse en la carpeta `images/` dentro de su subcarpeta correspondiente:
*   `images/pendientes/`
*   `images/collares/`
*   `images/anillos/`
*   `images/pulseras/`

## 🛠️ Instalación y Despliegue

Este proyecto es **estático** (HTML/CSS/JS puro), por lo que no requiere servidor backend ni Node.js.

1.  **Local:** Simplemente abre el archivo `index.html` en tu navegador.
2.  **Servidor:** Sube todos los archivos (incluyendo carpetas `images` y archivos `.csv`) a cualquier hosting web o GitHub Pages.

## 📧 Contacto
El código incluye scripts para asegurar que los enlaces de correo (`pedidos@aldazabal.es`) funcionen correctamente en distintos dispositivos.
