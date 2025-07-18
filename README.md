# 📄 Generación de PDF con Dompdf en Proyecto ASODAT

Este repositorio forma parte del sistema desarrollado para ASODAT, e incluye la funcionalidad de generar documentos PDF usando la biblioteca **Dompdf**. A continuación se detallan **dos métodos de instalación** según las necesidades del entorno.

---

## ✅ Requisitos

- PHP >= 7.1
- Extensiones habilitadas: `mbstring`, `dom`, `gd`
- Servidor local como XAMPP, WAMP o PHP CLI

---

## 🛠️ Opción 1: Instalación con Composer (recomendado)

```bash
composer require dompdf/dompdf
```
Luego en tu archivo PHP:
```bash
require 'vendor/autoload.php';
```
```bash
use Dompdf\Dompdf;

$dompdf = new Dompdf();
$dompdf->loadHtml('<h1>Hola mundo</h1>');
$dompdf->setPaper('A4', 'portrait');
$dompdf->render();
$dompdf->stream('documento.pdf', ["Attachment" => false]);
```

Opción 2: Instalación manual (ZIP)
Si Composer no está disponible, puedes usar Dompdf manualmente así:
