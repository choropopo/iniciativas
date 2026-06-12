# D&D Initiative Tracker — Instalación como app

## 📱 Instalar como app en el móvil (PWA)

### Android (Chrome / Edge / Samsung Internet)
1. Abre el archivo `index.html` en tu servidor web local o sube la carpeta a GitHub Pages / Netlify / Vercel
2. Visita la URL desde tu móvil Android con Chrome
3. Aparecerá un banner "Añadir a pantalla de inicio" — pulsa INSTALAR
4. Si no aparece automáticamente: menú ⋮ → "Añadir a pantalla de inicio"
5. La app se instala como si fuera una APK, con icono propio y pantalla completa

### iOS (Safari)
1. Abre la URL en Safari (importante: solo Safari soporta PWA en iOS)
2. Pulsa el botón compartir (cuadrado con flecha) 
3. Toca "Añadir a pantalla de inicio"
4. Confirma el nombre y pulsa "Añadir"

### Opción más fácil: servir localmente
```bash
# Con Python (si tienes Python en tu PC)
cd dnd-tracker/
python3 -m http.server 8080

# Luego desde el móvil en la misma red WiFi:
# http://[IP-de-tu-PC]:8080
```

### Subir a internet gratis (recomendado)
- **GitHub Pages**: sube la carpeta a un repo GitHub → Settings → Pages → Deploy
- **Netlify**: arrastra la carpeta a netlify.com/drop
- **Vercel**: `vercel deploy` o arrastra en vercel.com

## 📂 Archivos del proyecto
```
dnd-tracker/
├── index.html     ← App principal (todo en uno)
├── manifest.json  ← Configuración PWA
├── sw.js          ← Service Worker (modo offline)
├── icon-192.png   ← Icono app (pequeño)
└── icon-512.png   ← Icono app (grande)
```

## ✨ Características
- Rastreador de iniciativa con orden automático
- Contador de rondas y turnos
- Rastreo opcional de Puntos de Golpe con barra visual
- Condiciones y notas por combatiente
- Filtro/ordenación por iniciativa, nombre, tipo
- Jugadores, Enemigos y Aliados NPC diferenciados
- Página de Reglas básicas D&D 5e con enlaces oficiales
- Notas de partida personalizadas (reglas de la casa, etc.)
- Panel de estadísticas de sesión
- Exportar/Importar sesión como JSON
- Funciona 100% offline una vez instalada
- Guarda el estado automáticamente en el navegador
