# React Native CLI Setup Checklist

## Pre-requisitos

- [ ] Node.js v18+ instalado: `node --version`
- [ ] npm instalado: `npm --version`
- [ ] Java JDK 17-20 instalado: `javac -version`
- [ ] Android Studio instalado
- [ ] Android SDK configurado con ANDROID_HOME

## Instalación

- [ ] Ejecutar: `npx @react-native-community/cli init MyApp`
- [ ] Esperar descarga de template y dependencias (~2-3 min)
- [ ] Git repository inicializado automáticamente

## Verificación

- [ ] Proyecto creado en `./MyApp`
- [ ] `node_modules/` presente
- [ ] `metro.config.js` presente

## Desarrollo

- [ ] Emulador Android corriendo o dispositivo conectado
- [ ] Ejecutar: `cd MyApp && npx react-native run-android`

## Variables de Entorno Necesarias

```
JAVA_HOME = C:\Program Files\Java\jdkXX
ANDROID_HOME = C:\Users\YourUser\AppData\Local\Android\Sdk
```

### PASO 1: Descargar JDK compatible (17-20)

Link: https://www.oracle.com/java/technologies/downloads/
⚠ Nota: Java 26 no es soportada (máximo v20)

### PASO 2: Configurar JAVA_HOME

Windows CMD (ejecutar en terminal):

```batch
setx JAVA_HOME "C:\Program Files\Java\jdk-20"
```

(Reemplaza jdk-20 con la versión que instalaste: jdk-17, jdk-18, jdk-19 o jdk-20)

### PASO 3: Instalar Android Studio

Link: https://developer.android.com/studio

### PASO 4: Configurar ANDROID_HOME (después de Android Studio)

Windows CMD:

```batch
setx ANDROID_HOME "%LOCALAPPDATA%\Android\Sdk"
```

### PASO 5: Descargar componentes en Android Studio

- SDKs: API 36 (Android 15)
- Build Tools: 36.0.0
- Platform Tools (contiene adb)

### PASO 6: Crear emulador Android

- File > Device Manager > Create Virtual Device
- API level: 36 mínimo
- Iniciar emulador antes de build

### PASO 7: Reiniciar terminal y verificar

```batch
cd MyApp && npx react-native doctor
```

### PASO 8: Ejecutar app

```batch
cd MyApp && npx react-native run-android
```
