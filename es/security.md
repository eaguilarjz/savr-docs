---
title: Seguridad
parent: Español
nav_order: 9
---

> 🌐 Read this page in [English](../../en/security/)

# Seguridad

Esta página cubre todo lo relacionado con mantener tu cuenta de savr segura: contraseñas, autenticación de dos factores, códigos de recuperación y sesiones.

Encontrarás estos ajustes en **Perfil → Seguridad**.

---

## Cambia tu contraseña

1. Abre **Perfil** y busca la sección **Seguridad**.
2. Haz clic en **Cambiar contraseña**.
3. Ingresa tu **contraseña actual**, luego una **contraseña nueva** (mínimo 8 caracteres) y confírmala.
4. Haz clic en **Guardar**.

Una vez cambiada, cada sesión actualmente abierta sigue funcionando, pero cualquier sesión cerrada requerirá la nueva contraseña.

> **Consejo:** Usa un administrador de contraseñas. La contraseña más fuerte es la que no tienes que recordar.

---

## Autenticación de dos factores (MFA)

La autenticación de dos factores agrega un segundo paso al inicio de sesión: aunque alguien aprenda tu contraseña, no puede entrar sin un código de una aplicación autenticadora en tu teléfono. Activar MFA es la mejora más grande que puedes hacer a la seguridad de tu cuenta.

savr soporta **TOTP** (contraseñas de un solo uso basadas en tiempo) — el mismo estándar que usan Google Authenticator, Authy, 1Password, Bitwarden y la mayoría de los administradores de contraseñas modernos.

### Configurar MFA

1. Abre **Perfil → Seguridad** y haz clic en **Activar autenticación de dos factores**.
2. Un modal te lleva por tres pasos:

   **Paso 1 — Escanea el código QR**
   - Abre tu aplicación autenticadora (Google Authenticator, Authy, 1Password, Bitwarden, etc.).
   - Agrega una nueva cuenta escaneando el código QR que aparece en pantalla.
   - Si no puedes escanear, haz clic en **Mostrar secreto** e ingresa la clave de 32 caracteres manualmente.

   **Paso 2 — Verifica**
   - Escribe el código de 6 dígitos que tu autenticador muestra en ese momento.
   - Haz clic en **Verificar**.

   **Paso 3 — Guarda tus códigos de recuperación**
   - savr genera **8 códigos de recuperación**.
   - **Descárgalos** como archivo `.txt` o cópialos a tu administrador de contraseñas.
   - Estos códigos son tu respaldo si pierdes acceso a tu autenticador. Guárdalos en un lugar donde puedas encontrarlos otra vez — pero no en el mismo dispositivo que tu autenticador.

3. Haz clic en **Listo**. MFA está activo en tu cuenta.

### Iniciar sesión con MFA

Después de ingresar tu correo y contraseña en la pantalla de inicio de sesión, savr te pide un segundo factor:

- Abre tu aplicación autenticadora e ingresa el código actual de 6 dígitos, **o**
- Haz clic en **Usar un código de recuperación** e ingresa uno de los códigos que guardaste durante la configuración.

Los códigos de 6 dígitos se renuevan cada 30 segundos. Si un código es rechazado, espera al siguiente e inténtalo de nuevo — la causa más común es que el código anterior ya expiró.

### Códigos de recuperación

Cada código de recuperación es de **un solo uso**. Una vez usado, ese código no puede usarse de nuevo.

- Recibes **8 códigos al configurar**.
- Úsalos solo cuando no tengas acceso a tu autenticador (teléfono perdido, cambio de dispositivo sin migrar los códigos, app eliminada por error).
- Si has usado la mayoría y quieres códigos nuevos, regenéralos desde **Perfil → Seguridad → Regenerar códigos de recuperación**. Regenerar invalida el conjunto anterior.

> **Trata los códigos de recuperación como una llave de respaldo.** Si alguien tiene tus códigos y tu contraseña, tiene acceso completo. Guárdalos en un administrador de contraseñas o en algún lugar físicamente seguro.

### ¿Y si pierdo mi teléfono *y* mis códigos de recuperación?

Si ambos se han perdido, necesitarás contactar soporte para verificar tu identidad y recuperar acceso. Es un proceso manual, intencionalmente — es la red de seguridad que evita que un atacante use ingeniería social para regresar a entrar.

Por eso recomendamos guardar los códigos de recuperación en un lugar separado de tu teléfono (p. ej. un administrador de contraseñas que no esté sincronizado con ese teléfono, o una copia impresa en un lugar seguro).

### Desactivar MFA

1. Abre **Perfil → Seguridad** y haz clic en **Desactivar autenticación de dos factores**.
2. Ingresa tu contraseña para confirmar.
3. MFA se elimina de tu cuenta.

Puedes reactivarlo en cualquier momento. Se generan códigos de recuperación nuevos cada vez que configuras MFA desde cero — los códigos antiguos no se preservan.

---

## Sesiones

Cuando inicias sesión en savr, tu sesión se mantiene en dos cookies seguras:

| Cookie | Duración | Propósito |
|---|---|---|
| **Token de acceso** | 15 minutos | Se usa para cada solicitud |
| **Token de refresco** | 30 días | Emite un nuevo token de acceso automáticamente cuando el de acceso expira |

Ambas cookies son HTTP-only (así que JavaScript en la página no puede leerlas) y SameSite=strict (así que no se envían en solicitudes entre sitios). En producción, ambas cookies también están marcadas como Secure (solo HTTPS).

En la práctica esto significa:

- Te mantienes con sesión iniciada entre reinicios del navegador hasta por 30 días.
- ¿Inactivo por mucho tiempo? Se cerrará tu sesión silenciosamente si tu token de refresco expiró mientras no usabas la app.
- **Cerrar sesión** limpia ambas cookies en este dispositivo.

### Múltiples dispositivos

Puedes tener sesión iniciada en varios dispositivos al mismo tiempo — cada dispositivo tiene su propio par de cookies. Cerrar sesión en un dispositivo no cierra los demás. Por ahora no hay una lista de "sesiones activas" para revisar.

---

## Límites de tasa

Para proteger tu cuenta de ataques de fuerza bruta, ciertos endpoints están limitados:

| Acción | Límite |
|---|---|
| Inicio de sesión / verificación MFA | 10 intentos cada 15 minutos |
| Registro | 10 cada 15 minutos |
| Recuperar contraseña | 3 solicitudes por hora |

Si alcanzas un límite, verás un error pidiendo que esperes. Los límites se reinician automáticamente.

---

## Buenas prácticas

- **Activa MFA.** Casi todo compromiso de cuenta empieza con una contraseña robada o reutilizada. MFA lo derrota.
- **Usa un administrador de contraseñas.** Genera una contraseña única y larga para savr y deja que tu administrador la recuerde.
- **Guarda los códigos de recuperación donde realmente los puedas encontrar.** Una entrada en tu administrador de contraseñas, una copia en papel en una caja fuerte, o ambas.
- **No guardes los códigos de recuperación en el mismo dispositivo que tu autenticador.** Si pierdes el dispositivo, perdiste ambos.
- **Cierra sesión en dispositivos compartidos.** No confíes en la cookie de "recordar" si alguien más usa ese navegador.
