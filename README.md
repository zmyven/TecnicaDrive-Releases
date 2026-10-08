# TécnicaDrive: descargas

APK de la app de TécnicaDrive, el almacenamiento en la nube de la EEST N°2.

- **Descargar la última versión:** el archivo de la carpeta [`apk/`](apk/).
- La app instalada se actualiza sola: al abrirse lee [`ultima.json`](ultima.json) y, si hay una compilación nueva, la ofrece.

El código de la app está en un repositorio privado. Acá solo se publican los APK.

## Cambiar textos de la app sin actualizarla

[`textos.json`](textos.json) reemplaza textos de la app. La app lo lee cada vez que se abre:

```json
{
  "textos": {
    "inicio_titulo": "Portada",
    "drive_buscar_en": "Buscá en %1$s"
  }
}
```

- La clave es el nombre del texto en la app (`res/values/strings.xml` del repositorio de la app).
- Si el original tiene datos variables (`%1$s`, `%1$d`…), el reemplazo tiene que tener los mismos. Si no, la app lo ignora y usa el original.
- Para volver al texto original, borrá esa línea.
- Se puede editar desde el celular: abrí el archivo en GitHub, tocá el lápiz y guardá con "Commit changes". En unos minutos llega a todos los teléfonos, que lo ven la próxima vez que abren la app.
