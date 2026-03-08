# Tracker-CampeonatoAAU-2026
🏃 Campeonato 5K 2026 — Tracker Personal

Aplicación web para llevar el registro personal de resultados en el Campeonato 2026 de la Entidad Deportiva Más Accesible del País (carreras de 5km).

## ¿Qué es esto?
Un archivo HTML autónomo que funciona como app móvil. No requiere instalación ni servidor. Los datos se pueden guardar localmente en el dispositivo o sincronizarse en la nube mediante login con Google, permitiendo acceder desde cualquier dispositivo.

## Funcionalidades

### 🔐 Login opcional con Google
- Iniciá sesión con tu cuenta de Google para guardar tus datos en la nube
- Sin cuenta, la app funciona igual y los datos quedan en el dispositivo (localStorage)
- Al loguearte, los datos locales se migran automáticamente a tu cuenta
- Accedé desde cualquier dispositivo con la misma cuenta y tus carreras aparecen solas
- Los datos de cada usuario son privados — nadie puede ver los tuyos

### 📅 Calendario completo
Las 18 fechas del campeonato organizadas por mes, del 1 de marzo al 6 de diciembre de 2026. La fecha de Pérez Scremini (13 de septiembre) está marcada como Fuera del Campeonato. Fechas especiales (sábados) identificadas con su etiqueta correspondiente.

### ✏️ Registro de resultados
Por cada carrera se puede registrar:
- Tiempo total en formato mm:ss (ej: 23:05)
- Ritmo por kilómetro — se calcula automáticamente al ingresar el tiempo total
- Posición — número de posición y total de corredores (ej: 11 / 528)
- Notas libres — sensaciones, clima, terreno, etc.

### ⚡ Autocompletar desde atletas.uy
Ingresá el ID del evento desde la URL de atletas.uy/results y la app busca automáticamente tu tiempo, ritmo y posición usando tu nombre o dorsal configurado en el perfil.

### 🚫 No participé
Si no se corrió una fecha, se puede marcar como "No participé". Esto la distingue visualmente de las fechas pendientes y de las completadas, usando un indicador naranja en el progreso.

### 📊 Panel de estadísticas
- Mejor tiempo registrado
- Mejor ritmo (min/km)
- Mejor posición relativa
- Total de carreras completadas

### 📈 Gráfico de progresión
Visualización cronológica de todos los tiempos registrados para ver la evolución carrera a carrera. Se activa automáticamente al tener 2 o más resultados cargados.

### 🏆 Top 5 mejores tiempos
Tabla con las 5 carreras más rápidas, mostrando tiempo, ritmo y posición.

### 🔵 Barra de progreso
Indicador visual del avance en el campeonato con un punto por fecha:
- Verde → carrera completada
- Naranja → no participé
- Gris → pendiente

### 📥 Exportar CSV
Descarga un archivo .csv con todos los datos registrados, compatible con Excel y Google Sheets. Incluye todas las fechas con su estado (Completada / No participé / Pendiente).

### 📱 PWA — Funciona como app nativa
- Se puede agregar a la pantalla de inicio del celular desde Safari (compartir → Agregar a pantalla de inicio)
- Una vez cargada con internet, funciona completamente sin conexión
- Muestra una barra de aviso cuando no hay conectividad

## Uso en móvil (iOS)
1. Abrí el link en **Safari**
2. Tocá el ícono de compartir ↑
3. Seleccioná "Agregar a pantalla de inicio"
4. La app queda guardada con ícono propio, sin barra de navegación

> El login con Google desde Safari/iOS usa redirect automáticamente para mayor compatibilidad.

## Datos y sincronización

### Sin cuenta (localStorage)
Los datos se guardan en el localStorage del navegador de cada dispositivo. Persisten entre sesiones mientras no se limpie el caché. Se pueden respaldar usando la función Exportar CSV.

### Con cuenta Google (Firestore)
Los datos se guardan en Firebase Firestore asociados al usuario. Accesibles desde cualquier dispositivo al iniciar sesión. Cada usuario solo puede ver y modificar sus propios datos (reglas de seguridad de Firestore).

## Tecnologías
- HTML/CSS/JS puro — sin frameworks
- Firebase Authentication (Google Sign-In)
- Firebase Firestore (sincronización en la nube)
- PWA (manifest + service worker inline)

## Campeonato
- **Distancia:** 5 kilómetros
- **Total de fechas:** 18
- **Descartes:** 5
- **Fechas válidas para reconocimiento:** 13
- **Inscripción:** atletas.uy
