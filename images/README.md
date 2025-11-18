# Estructura de Imágenes para ALDAZABAL

## 📁 Organización de carpetas

```
images/
├── pendientes/
├── collares/
├── anillos/
└── pulseras/
```

## 📸 Nomenclatura de archivos

### Formato recomendado:
`{categoria}_{nombre-producto}_{id}.jpg`

### Ejemplos:
- `pendientes_lagrima_001.jpg`
- `pendientes_lagrima_002.jpg`
- `collares_perlas_001.jpg`
- `anillos_oro_001.jpg`
- `pulseras_plata_001.jpg`

## ✅ Buenas prácticas

1. **Nombres descriptivos**: Usa nombres que describan el producto
2. **Sin espacios**: Usa guiones (-) o guiones bajos (_)
3. **Minúsculas**: Todos los nombres en minúsculas
4. **Numeración**: Si tienes variantes, usa números consecutivos (001, 002, etc.)
5. **Formato**: Preferiblemente JPG o WebP para web

## 🖼️ Especificaciones técnicas

- **Tamaño recomendado**: 800x800px (cuadrado)
- **Proporción**: 1:1 (aspecto cuadrado)
- **Formato**: JPG, PNG o WebP
- **Peso**: < 200KB por imagen (optimizadas para web)
- **Fondo**: Preferiblemente blanco o neutro

## 📝 Ejemplo de uso en products.json

```json
{
  "id": 1,
  "name": "Pendiente Lágrima",
  "price": "70€",
  "image": "images/pendientes/pendientes_lagrima_001.jpg"
}
```

## 🔄 Múltiples imágenes (futuro)

Si quieres añadir múltiples fotos por producto:

```json
{
  "id": 1,
  "name": "Pendiente Lágrima",
  "price": "70€",
  "image": "images/pendientes/pendientes_lagrima_001.jpg",
  "images": [
    "images/pendientes/pendientes_lagrima_001.jpg",
    "images/pendientes/pendientes_lagrima_002.jpg",
    "images/pendientes/pendientes_lagrima_003.jpg"
  ]
}
```
