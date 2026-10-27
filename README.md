# Transcriptor Local

Aplicación web de una sola página para trabajar con documentos y grabaciones **sin subirlos a la nube**: todo el procesamiento ocurre en el navegador de tu equipo.

**👉 Úsala en línea: [adfincarserv-source.github.io/transcripcion](https://adfincarserv-source.github.io/transcripcion/)**

## Funciones

| Pestaña | Qué hace | Salida |
| --- | --- | --- |
| ⚡ Automático | Detecta el tipo de cada archivo y aplica la conversión adecuada | Según el archivo |
| 📝 A Markdown | Convierte PDF, Word, PowerPoint, Excel, CSV, HTML, texto e imágenes (como MarkItDown). Aplica OCR a las páginas escaneadas | `MarkitDown/*.md` |
| 🔍 OCR de PDF | Reconoce el texto de PDF escaneados o imágenes (español, inglés, portugués) | `OCR/*_OCR.pdf` (buscable), `.txt`, `.md` |
| 🎙️ Audio y video | Transcribe m4a, mp3, wav, mp4… con Whisper, sin límite de duración (fragmentos de 30 s) | `Transcripciones/*.md` (con marcas de tiempo), `.txt` |
| ▦ Generador QR | Crea códigos QR a partir de enlaces o texto | PNG o SVG |

- Acepta **archivos sueltos o carpetas completas** (con subcarpetas). En Chrome o Edge los resultados se guardan directamente en una subcarpeta de la carpeta elegida; en otros navegadores se descargan individualmente o en un ZIP.
- Diseño adaptable a celulares, tabletas y portátiles; tema claro, oscuro o automático y tamaño de letra ajustable (se recuerdan entre sesiones).

## Cómo usarla

### En línea (recomendado)

Abre **https://adfincarserv-source.github.io/transcripcion/** en Chrome o Edge (computador) o en el navegador del celular. GitHub solo entrega la página: tus archivos se procesan en tu dispositivo y no se suben a ningún servidor.

### Sin conexión a GitHub

1. Descarga el repositorio (botón **Code → Download ZIP**) y descomprímelo.
2. En Windows, haz doble clic en **`Iniciar.bat`**. Se abre la app en `http://localhost:8765`, un servidor que solo existe en tu equipo.
   - Alternativa: abre `index.html` directamente en Chrome o Edge.

Luego elige una carpeta o archivos, ajusta las opciones y pulsa **Procesar**.

> La primera vez se necesita internet para descargar las librerías y los modelos (datos de OCR y el modelo Whisper elegido, entre 75 MB y 1 GB). Quedan guardados en el navegador. Tus archivos nunca salen de tu equipo.

## Modelos de transcripción

| Modelo | Tamaño | Recomendado para |
| --- | --- | --- |
| Tiny | ~75 MB | Pruebas rápidas |
| Base | ~150 MB | Uso general |
| Small | ~500 MB | Mejor precisión en español |
| Large v3 Turbo | ~1 GB | Equipos con tarjeta gráfica (WebGPU) |

## Tecnologías

[pdf.js](https://mozilla.github.io/pdf.js/) · [Tesseract.js](https://tesseract.projectnaptha.com/) · [Transformers.js](https://huggingface.co/docs/transformers.js) (Whisper) · [mammoth](https://github.com/mwilliamson/mammoth.js) · [Turndown](https://github.com/mixmark-io/turndown) · [SheetJS](https://sheetjs.com/) · [JSZip](https://stuk.github.io/jszip/) · [pdf-lib](https://pdf-lib.js.org/) · [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator)
