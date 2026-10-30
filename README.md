Lector de extintores

Aplicación web para escanear el código QR de las estampillas de matafuegos y guardar sus datos de forma ordenada. Funciona desde el celular, sin instalar nada.
Link que te lleva a la página en cuestión: https://ncomaa.github.io/Matafuegos-qr/
Qué hace
Escanea el QR con la cámara en vivo, con una foto del código o pegando el enlace a mano.
Trae los datos solos desde la página oficial de la AGC (si está configurado el Google Apps Script). Si no se pueden traer, se completan a mano.
Calcula las fechas clave: último mantenimiento, prueba hidráulica, fabricación y vida útil, con cuánto falta o cuánto pasó desde cada vencimiento.
Marca el estado de cada extintor según lo primero que vence:
🟢 Vigente
🟡 Por vencer (menos de 30 días)
🔴 Vencido
Guarda una foto de la etiqueta como respaldo.
Registra varias estampillas por extintor, para ver el historial de mantenimientos.
Cómo se usa
Tocá Escanear con cámara y apuntá al QR del matafuego. Si la cámara en vivo no está disponible, usá Foto del QR o pegá el enlace.
Revisá los datos cargados y completá lo que falte. Las fechas van como MM/AAAA, por ejemplo 08/2027.
Opcional: sacá una foto de la etiqueta.
Tocá Guardar. El extintor aparece en la lista, con su estado y el detalle al desplegarlo.

Para guardar, alcanza con completar Nro. de extintor y Empresa fabricante.

Dónde se guardan los datos

Los datos quedan en el navegador del dispositivo (localStorage), así que no se pierden al cerrar la página, pero tampoco se comparten entre dispositivos. Si se configura SCRIPT_URL en script.js, cada registro también se envía a una hoja de Google a través de Apps Script.

Archivos
Archivo	Función
index.html	Estructura de la página
style.css	Estilos y tema
script.js	Escaneo, cálculo de fechas y almacenamiento
Requisitos
Un navegador moderno, preferentemente Chrome en el celular.
La página tiene que abrirse por HTTPS (por ejemplo, con GitHub Pages) para que funcione la cámara.
La lectura de QR usa el detector nativo del navegador y jsQR como alternativa.
