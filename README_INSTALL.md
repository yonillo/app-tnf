# 🚀 Guía de Instalación: Tenerife Conquest App (10 Pasos)

Sigue estos pasos para configurar el entorno de desarrollo y ejecutar la aplicación en tu ordenador local.

---

### 📋 Requisitos Previos
*   **Git:** [Descargar aquí](https://git-scm.com/)
*   **Flutter SDK:** [Descargar aquí](https://docs.flutter.dev/get-started/install)
*   **Node.js (v18+):** [Descargar aquí](https://nodejs.org/)
*   **Editor:** VS Code o Android Studio.

---

### 🛠️ Pasos de Instalación

#### 1. Clonar el repositorio
Abre una terminal y descarga el código:
```bash
git clone https://github.com/yonillo/app-tnf.git
cd app-tnf
```

#### 2. Configurar el Backend (Servidor)
Entra en la carpeta del servidor para preparar la API:
```bash
cd backend
npm install
```

#### 3. Iniciar el Backend
Ejecuta el servidor localmente (estará disponible en `http://localhost:3000`):
```bash
node index.js
```
*(Deja esta terminal abierta para que la app pueda consultar los datos).*

#### 4. Configurar el Frontend (Flutter)
Abre una **nueva terminal** en la carpeta raíz del proyecto y entra en `frontend`:
```bash
cd frontend
flutter pub get
```

#### 5. Verificar el Entorno de Flutter
Asegúrate de que todo esté bien configurado ejecutando:
```bash
flutter doctor
```
*(Si falta algo, Flutter te indicará cómo instalarlo).*

#### 6. Configurar la IP del Backend (Opcional para Móvil)
Si vas a probar en un móvil físico, abre `frontend/lib/services/api_service.dart` y cambia `localIp` por la IP de tu ordenador en la red WiFi.

#### 7. Preparar el Emulador / Simulador
*   **Android:** Abre un emulador desde Android Studio o conecta un móvil por USB (con Depuración USB activada).
*   **iOS (Solo Mac):** Abre el Simulador de Xcode.
*   **Web:** No necesitas nada extra, Flutter usará Chrome.

#### 8. Ejecutar la Aplicación
Lanza la app con el siguiente comando:
```bash
flutter run
```
*(Si tienes varios dispositivos conectados, elige uno escribiendo su número).*

#### 9. Probar las Funcionalidades
Una vez abierta la app, verifica que carguen los puntos de interés (POIs). Esto confirmará que la conexión con el backend (paso 3) es correcta.

#### 10. Generar el Ejecutable (Build)
Cuando estés listo para crear el instalable final:
*   **Android:** `flutter build apk`
*   **iOS (Solo Mac):** `flutter build ipa` (o usa el GitHub Action que configuramos).

---

### 💡 Notas Adicionales
*   **Errores de dependencias:** Si algo falla al inicio, intenta `flutter clean` seguido de `flutter pub get`.
*   **Datos:** Los archivos `.geojson` en el backend son necesarios para los mapas; no los borres.

---
*¡Disfruta desarrollando Tenerife Conquest!* 🌋🗺️
