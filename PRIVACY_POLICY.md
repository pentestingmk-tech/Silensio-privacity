# Política de Privacidad — Silensio

**Última actualización:** 26 de agosto de 2026

**Responsable:** Mk Pentesting  
**Contacto:** pentestingmk@gmail.com  
**Aplicación:** Silensio (Android)

---

## 1. Introducción

Silensio es una aplicación de mensajería anónima y segura que opera bajo el principio de **privacidad por diseño**. Esta política describe qué datos maneja la aplicación, cómo se usan y qué derechos tienes como usuario.

Al utilizar Silensio, aceptas las prácticas descritas en esta política.

---

## 2. Datos que recopilamos

### 2.1 Datos almacenados localmente

Silensio almacena datos **exclusivamente en tu dispositivo**:

| Dato | Propósito | Cifrado |
|------|-----------|---------|
| Nombre de usuario e ID único | Identificación dentro de la red | Sí (AES-256-GCM) |
| Lista de contactos | Acceso rápido a conversaciones | Sí (AES-256-GCM) |
| Mensajes de texto | Historial de conversaciones | Sí (AES-256-GCM) |
| Archivos multimedia recibidos | Imágenes, audio, video, documentos | Sí (AES-256-GCM) |
| Datos de grupos | Chats grupales | Sí (AES-256-GCM) |
| Frase de recuperación de 12 palabras | Recuperación de identidad | Sí (AES-256-GCM) |
| Configuración de la app | Preferencias del usuario | Parcial |

### 2.2 Datos que NO recopilamos

Silensio **NO recopila, almacena ni transmite** los siguientes datos:

- Número de teléfono
- Correo electrónico
- Ubicación geográfica (GPS)
- Identificadores del dispositivo (IMEI, MAC, etc.)
- Lista de contactos del libro de direcciones
- Lista de apps instaladas
- Datos de uso o analytics
- Registros de llamadas del sistema
- Historial de navegación
- Publicidad o datos publicitarios
- Cualquier dato identificable personal

---

## 3. Cómo se procesan los datos

### 3.1 Comunicación cifrada de extremo a extremo (E2EE)

Todos los mensajes y archivos se cifran en tu dispositivo y solo se descifran en el dispositivo del destinatario utilizando:

- **Intercambio de claves:** ECDH (Elliptic Curve Diffie-Hellman) sobre curva secp256r1
- **Cifrado de mensajes:** AES-256-CBC con PKCS5
- **Firmas:** ECDSA con SHA-256
- **Sin defaultstate:** Cada sesión genera un nuevo par de claves

### 3.2 Sin almacenamiento en servidores

Silensio utiliza un servidor de señalización que **únicamente reenvía datos cifrados** entre dispositivos. El servidor:

- NO almacena mensajes
- NO almacena archivos multimedia
- NO tiene acceso al contenido de las conversaciones
- NO puede descifrar los datos transmitidos

### 3.3 Comunicación peer-to-peer (P2P)

Las llamadas de voz y video se realizan directamente entre dispositivos mediante WebRTC, sin pasar por servidores intermedios.

---

## 4. Permisos del dispositivo

Silensio solicita los siguientes permisos, justificados por su funcionalidad:

| Permiso | Uso |
|---------|-----|
| Internet | Conexión al servidor de señalización y llamadas WebRTC |
| Cámara | Videollamadas y captura de fotos para enviar |
| Micrófono | Llamadas de voz/video y grabación de mensajes de audio |
| Notificaciones | Notificaciones de mensajes y llamadas entrantes |
| Vibración | Alertas de mensajes entrantes |
| Pantalla completa | Mostrar llamadas entrantes cuando el dispositivo está bloqueado |
| Servicio en primer plano | Mantener conexión en segundo plano para recibir mensajes |
| Bluetooth | Conexión con auriculares y accesorios de audio |
| Ajustes de audio | Control de volumen durante llamadas |

**Permisos que NO solicitamos:** Ubicación, contactos del dispositivo, almacenamiento externo, teléfono, SMS.

---

## 5. Seguridad

### 5.1 Cifrado en reposo

Todos los datos almacenados en el dispositivo están cifrados con AES-256-GCM utilizando Android Keystore como fuente de claves.

### 5.2 Protección de pantalla

La aplicación activa FLAG_SECURE para evitar capturas de pantalla del contenido sensible.

### 5.3 Sin rastro digital

Silensio no registra:
- IP del usuario
- Metadatos de las conversaciones
- Tiempos de conexión
- Patrones de uso

### 5.4 Auto-destrucción

La app incluye función de autodestrucción que elimina de forma segura todas las claves, mensajes y archivos locales.

---

## 6. Compartición con terceros

Silensio **NO comparte datos con terceros**. No existen:

- Servicios de analytics
- SDKs publicitarios
- Redes sociales integradas
- Herramientas de rastreo
- Proveedores de publicidad

Las únicas dependencias técnicas son librerías de código abierto para funcionalidad de la app (WebRTC, cifrado, interfaz).

---

## 7. Retención de datos

- Los datos se mantienen **únicamente en tu dispositivo** mientras los conserves
- No existe copia en la nube ni en servidores
- Puedes eliminar todos los datos en cualquier momento desde Ajustes > Autodestrucción
- Al desinstalar la app, todos los datos se eliminan permanentemente

---

## 8. Menores de edad

Silensio no recopila datos personales identificables. No obstante, no está dirigida a menores de 13 años. Si un menor de edad utiliza la aplicación bajo supervisión de un adulto, es responsabilidad de dicho adulto.

---

## 9. Cambios en esta política

Nos reservamos el derecho de actualizar esta política de privacidad. Los cambios serán publicados en esta página con la fecha de "Última actualización" actualizada. Se recomienda revisar periódicamente esta política.

---

## 10. Derechos del usuario

De acuerdo con la normativa de protección de datos aplicable, tienes derecho a:

- **Acceso:** Conocer qué datos maneja la app (esta política)
- **Eliminación:** Borrar todos tus datos desde la app o desinstalándola
- **Portabilidad:** Tus claves cifradas pueden exportarse mediante la frase de recuperación
- **Transparencia:** Esta política describe exactamente qué hace la app con los datos

---

## 11. Contacto

Si tienes preguntas sobre esta política de privacidad o sobre el manejo de datos en Silensio, contacta:

**Mk Pentesting**  
Email: pentestingmk@gmail.com

---

*Esta política fue elaborada basándose en una auditoría completa del código fuente de la aplicación Silensio, garantizando que las prácticas descritas reflejan exactamente el comportamiento de la app.*