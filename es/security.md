---
title: Seguridad
parent: Español
nav_order: 13
---

> {% include lang-globe.html %} Read this page in [English](../../en/security/)

# Seguridad

Tu cuenta de savr contiene una imagen completa de tus finanzas. Lo tomamos en serio, y tú también deberías.

Esta página cubre todo lo que puedes hacer para mantener tu cuenta segura: contraseñas, autenticación de dos factores, códigos de recuperación y cómo funcionan las sesiones. La mayoría es configuración única de dos minutos que paga dividendos para siempre.

Encontrarás estos ajustes en **Perfil → Seguridad**.

---

## Cambia tu contraseña

1. Abre **Perfil** y busca la sección **Seguridad**.
2. Haz clic en **Cambiar contraseña**.
3. Ingresa tu **contraseña actual**, luego una **contraseña nueva** (mínimo 8 caracteres) y confírmala.
4. Haz clic en **Guardar**.

Una vez cambiada, cada sesión actualmente abierta sigue funcionando, pero cualquier sesión cerrada (otro dispositivo, un navegador viejo) requerirá la nueva contraseña.

> **Pro tip:** Usa un administrador de contraseñas. La contraseña más fuerte es la que no tienes que recordar — larga, aleatoria, única para savr. 1Password, Bitwarden, iCloud Keychain de Apple, el administrador integrado de tu navegador: todos están bien. Elige uno y déjalo hacer su trabajo.

---

## Autenticación de dos factores (MFA)

La autenticación de dos factores agrega un segundo paso al inicio de sesión: aunque alguien aprenda tu contraseña, no puede entrar sin un código de una aplicación autenticadora en tu teléfono. Activar MFA es la mejora más grande que puedes hacer a la seguridad de tu cuenta.

savr soporta **TOTP** (contraseñas de un solo uso basadas en tiempo) — el mismo estándar que usan Google Authenticator, Authy, 1Password, Bitwarden y la mayoría de los administradores de contraseñas modernos.

### Configurar MFA

1. Abre **Perfil → Seguridad** y haz clic en **Activar autenticación de dos factores**.
2. Un modal te lleva por tres pasos:

   **Paso 1 — Escanea el código QR**
   - Abre tu aplicación autenticadora.
   - Agrega una nueva cuenta escaneando el código QR en pantalla.
   - Si no puedes escanear, haz clic en **Mostrar secreto** e ingresa la clave de 32 caracteres manualmente.

   **Paso 2 — Verifica**
   - Escribe el código de 6 dígitos que tu autenticador muestra en ese momento.
   - Haz clic en **Verificar**.

   **Paso 3 — Guarda tus códigos de recuperación**
   - savr genera **8 códigos de recuperación**.
   - **Descárgalos** como archivo `.txt` o cópialos a tu administrador de contraseñas.
   - Estos códigos son tu respaldo si pierdes acceso a tu autenticador. Guárdalos en un lugar donde puedas encontrarlos otra vez — pero **no en el mismo dispositivo que tu autenticador**.

3. Haz clic en **Listo**. MFA está activo.

> **La configuración de cinco minutos que paga para siempre.** La mayoría de los compromisos de cuenta empiezan con una contraseña robada o reutilizada. MFA neutraliza el ataque. Toda la configuración toma menos de cinco minutos. Solo hazlo.

### Iniciar sesión con MFA

Después de ingresar tu correo y contraseña en la pantalla de inicio de sesión, savr pide un segundo factor:

- Abre tu aplicación autenticadora e ingresa el código actual de 6 dígitos, **o**
- Haz clic en **Usar un código de recuperación** e ingresa uno de los códigos que guardaste durante la configuración.

Los códigos de 6 dígitos se renuevan cada 30 segundos. Si un código es rechazado, espera al siguiente e intenta de nuevo — la causa más común es que el código anterior expiró entre que lo leíste y lo escribiste.

### Códigos de recuperación

Cada código de recuperación es de **un solo uso**. Una vez usado, ese código no puede usarse de nuevo.

- Recibes **8 códigos al configurar**.
- Úsalos cuando no tengas acceso a tu autenticador (teléfono perdido, cambio de dispositivo sin migrar los códigos, app eliminada por error).
- Si has usado la mayoría y quieres códigos nuevos, regenéralos desde **Perfil → Seguridad → Regenerar códigos de recuperación**. Regenerar invalida el conjunto anterior.

> **Trata los códigos de recuperación como una llave de respaldo.** Si alguien tiene tus códigos y tu contraseña, tiene acceso completo. Guárdalos en un administrador de contraseñas o en algún lugar físicamente seguro (como una copia impresa en una caja fuerte). No te los mandes por correo a ti mismo.

### ¿Y si pierdo mi teléfono *y* mis códigos de recuperación?

Si ambos se han perdido, contacta soporte para verificar tu identidad y recuperar acceso. Es intencionalmente manual — es la red de seguridad que evita que alguien use ingeniería social para regresar a tu cuenta.

La solución para este escenario es nunca llegar a él: guarda los códigos de recuperación en un lugar separado de tu teléfono. Un administrador de contraseñas no sincronizado con ese teléfono, o una copia impresa en un cajón, ambos funcionan.

### Desactivar MFA

1. Abre **Perfil → Seguridad** y haz clic en **Desactivar autenticación de dos factores**.
2. Ingresa tu contraseña para confirmar.
3. MFA se elimina de tu cuenta.

Puedes reactivarlo en cualquier momento. Se generan códigos de recuperación nuevos cada vez que configuras MFA desde cero — los códigos antiguos no se conservan.

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
- ¿Inactivo por mucho tiempo? Se cerrará tu sesión silenciosamente si tu token de refresco expiró mientras no usabas la app. Sin drama; solo inicia sesión otra vez.
- **Cerrar sesión** limpia ambas cookies en este dispositivo.

### Múltiples dispositivos

Puedes tener sesión iniciada en varios dispositivos al mismo tiempo — cada dispositivo tiene su propio par de cookies. Cerrar sesión en un dispositivo no cierra los demás.

> **Por ejemplo:** Estás con sesión iniciada en tu laptop y tu teléfono. Le pasas el teléfono a un amigo (que no ve savr — está usando otra app), luego cierras sesión en la laptop. La sesión en tu teléfono no se afecta.

Aún no hay una lista de "sesiones activas". Si alguna vez pierdes un dispositivo y quieres asegurarte absolutamente de que todas las sesiones se cierren, cambia tu contraseña — no invalida sesiones existentes, pero las nuevas requerirán la nueva contraseña.

---

## Límites de tasa

Para proteger tu cuenta de ataques de fuerza bruta, ciertos endpoints están limitados:

| Acción | Límite |
|---|---|
| Inicio de sesión / verificación MFA | 10 intentos cada 15 minutos |
| Registro | 10 cada 15 minutos |
| Recuperar contraseña | 3 solicitudes por hora |

Si alcanzas un límite, verás un error pidiendo que esperes. Los límites se reinician automáticamente.

La mayoría de los usuarios nunca verán uno de estos mensajes. Existen para frenar a los atacantes que de otra forma intentarían miles de adivinanzas de contraseña contra tu cuenta.

---

## Buenas prácticas

Una lista corta, en orden de importancia:

1. **Activa MFA.** Casi todo compromiso de cuenta empieza con una contraseña robada o reutilizada. MFA lo derrota. (Dos minutos. Solo hazlo.)
2. **Usa un administrador de contraseñas.** Genera una contraseña única y larga para savr y deja que tu administrador la recuerde. No reutilices una contraseña de otro sitio.
3. **Guarda los códigos de recuperación donde realmente los puedas encontrar.** Una entrada en tu administrador de contraseñas, una copia en papel en una caja fuerte, o ambas. No los pongas en un correo o en una app de Notas en el mismo dispositivo que tu autenticador.
4. **No guardes los códigos de recuperación en el mismo dispositivo que tu autenticador.** Si pierdes el dispositivo, perdiste ambos — y pierdes la red de seguridad.
5. **Cierra sesión en dispositivos compartidos.** No confíes en la cookie de "recordar" si alguien más usa ese navegador.
6. **Trata los correos de fin de prueba y renovación como puntos de control de seguridad también.** Confirman que tu correo sigue funcionando y tu cuenta sigue activa. Si dejas de recibir los correos esperados de savr, revisa tu carpeta de spam y considera si tu cuenta de correo ha sido comprometida.

Nunca te arrepentirás de estos. Podrías arrepentirte de saltártelos.
