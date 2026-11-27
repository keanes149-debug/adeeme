# Mi Panel Diario

Panel personal para administrar el día a día. Es una sola página web (`index.html`), sin servidor ni instalación: ábrela en el navegador o instálala como app (PWA) desde Chrome/Edge/Android.

## Qué incluye

Todo es un anillo, del mismo estilo, y el panel se ajusta solo para caber en una pantalla sin desplazarse (laptop o teléfono).

- **Hoy** (el anillo un poco más grande): mediodía arriba, medianoche abajo. El arco amarillo es tu jornada (6:00–18:00 por defecto, se cambia en *Ajustes*), el punto rosa es la hora actual y los puntos oscuros son tus eventos de hoy.
- **Fechas límite**: más de 3 días azul; faltan 3 días **verde**, 2 días **amarillo**, último día **rojo**. Cada uno empieza lleno y se vacía a lo largo de su día.
- **Baterías**: la del dispositivo donde abres el panel se lee sola (Chrome, Edge, Android); las demás se actualizan tocando el anillo.
- **IAs**: cuánto te queda libre y cuándo se reinicia; al tocarla aparecen botones −1 / +1.
- **Dinero**: total y presupuesto del mes; al tocarlo ves cuentas, movimientos y registras gastos o ingresos.
- **Medidores**: agua, sueño, pasos o lo que quieras, con meta.

Toca cualquier anillo para verlo o editarlo, y el anillo **+** para agregar.

## Registrar hablando

Toca **Hablar**, di todo de corrido (por ejemplo: «gasté 250 en café, el teléfono va en 30 %, presento el proyecto el viernes a las 10 y llevo 5 vasos de agua») y la IA lo convierte en registros. Antes de guardar te muestra la lista para que confirmes o desmarques lo que no quieras.

- **Dentro de Claude** (el enlace del artifact): usa el dictado y la IA de Claude, sin clave. El dictado funciona en Chrome/Edge de escritorio y en la app de escritorio; en el teléfono escribe o usa el micrófono del teclado.
- **Fuera de Claude** (abriendo `index.html` o instalada como app): pon tu clave de OpenAI en *Ajustes*. Se graba el audio, se transcribe con `gpt-4o-mini-transcribe` y se interpreta con `gpt-4o-mini`. La clave se guarda solo en ese navegador (`localStorage`), nunca en el repositorio ni en la copia exportada. Si no hay clave pero el navegador tiene reconocimiento de voz (Chrome), se usa para dictar, pero la interpretación sí necesita la clave.

## Datos

Todo se guarda en el `localStorage` del navegador. Usa **Exportar** para descargar una copia `.json` e **Importar** para cargarla en otro dispositivo.

## Instalarla en el teléfono

Para que sea una app (ícono en la pantalla de inicio, pantalla completa, funciona sin internet) tiene que estar publicada en una dirección `https://`. Con GitHub Pages:

1. En GitHub: *Settings → Pages → Build and deployment → Source: Deploy from a branch*, rama `claude/zealous-hamilton-9f6ehe`, carpeta `/ (root)`, *Save*. (En repositorios privados GitHub Pages requiere un plan de pago; si no lo tienes, haz el repositorio público: no contiene datos ni claves.)
2. Espera uno o dos minutos y abre `https://keanes149-debug.github.io/adeeme/` en el teléfono.
3. **Android (Chrome):** menú ⋮ → *Instalar app* (o *Agregar a pantalla principal*).
   **iPhone (Safari):** botón Compartir → *Agregar a pantalla de inicio*.

## Usarlo

Abre `index.html` directamente, o sírvelo para poder instalarlo como app:

```bash
python3 -m http.server 8000
```

Luego visita `http://localhost:8000`.
