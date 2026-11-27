# Mi Panel Diario

Panel personal para administrar el día a día. Es una sola página web (`index.html`), sin servidor ni instalación: ábrela en el navegador o instálala como app (PWA) desde Chrome/Edge/Android.

## Qué incluye

- **Reloj de 24 horas**: mediodía arriba y medianoche abajo. El arco amarillo es tu jornada (por defecto 6:00–18:00, se cambia en *Ajustes*), la aguja rosa es la hora actual y en el centro se ve cuánto te queda de jornada. Los eventos de hoy aparecen como puntos sobre el reloj.
- **Cuenta regresiva por evento**: cada fecha límite es un anillo.
  - Más de 3 días: azul, lleno.
  - Faltan 3 días: **verde**, empieza lleno y se vacía a lo largo de ese día.
  - Faltan 2 días: **amarillo**, se vacía durante el día.
  - Último día: **rojo**, se vacía hasta la hora límite.
- **Baterías**: la del dispositivo donde abres el panel se lee automáticamente (Battery API: Chrome, Edge, Android; Safari/iPhone no la ofrece). Las demás (p. ej. tu teléfono) se actualizan a mano tocando la tarjeta.
- **Límites de tus IAs**: usado / límite (o porcentaje), cuándo se reinicia y cada cuántas horas; al pasar la hora de reinicio se pone en cero solo. Botones +1 / − para ir contando.
- **Dinero**: cuentas con saldo, total disponible, presupuesto mensual (se reinicia cada mes, con cuánto puedes gastar por día) y registro rápido de gastos e ingresos.
- **Otros medidores**: agua, sueño, pasos o lo que quieras, con meta y botones de incremento.

Toca cualquier elemento para editarlo o eliminarlo.

## Datos

Todo se guarda en el `localStorage` del navegador. Usa **Exportar** para descargar una copia `.json` e **Importar** para cargarla en otro dispositivo.

## Usarlo

Abre `index.html` directamente, o sírvelo para poder instalarlo como app:

```bash
python3 -m http.server 8000
```

Luego visita `http://localhost:8000`.
