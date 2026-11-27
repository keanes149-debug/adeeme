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

## Datos

Todo se guarda en el `localStorage` del navegador. Usa **Exportar** para descargar una copia `.json` e **Importar** para cargarla en otro dispositivo.

## Usarlo

Abre `index.html` directamente, o sírvelo para poder instalarlo como app:

```bash
python3 -m http.server 8000
```

Luego visita `http://localhost:8000`.
