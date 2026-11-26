# ¡Pide tu tostada! — Alumnado v1.01

Aplicación PWA para el proyecto Firebase `pide-tu-tostada`. La carpeta `public` contiene toda la web. No necesita compilación. Candidato para pruebas, no para publicación general todavía.

1. Sigue primero el manual de Gestión: instala y ejecuta las pruebas de reglas; no publiques si fallan. Inicializa catálogo y configuración con los pedidos cerrados.
2. Con Firebase CLI instalada y sesión iniciada, abre esta carpeta en terminal: `firebase deploy --only hosting --project pide-tu-tostada` (o `npx firebase-tools@14.8.0 deploy --only hosting --project pide-tu-tostada`). El destino es `pide-tu-tostada.web.app`.
3. Registra App Check para esta app web; inserta la clave pública de reCAPTCHA v3 en `public/firebase.mjs` cuando corresponda y vuelve a desplegar.
4. Prueba con un nombre ficticio y el código común de ensayo. Verifica contraseña, imagen privada/pública, QR, modificaciones y cancelaciones, y que una sesión ajena no puede acceder. No uses datos reales hasta superar auditoría, privacidad y carga.

Los únicos datos persistentes del perfil son nombre, apellidos, curso y grupo; también se guardan referencias locales de pedidos, tema y sesión técnica. No se guarda la cesta, fecha ni observaciones para futuros pedidos. El justificante privado debe conservarse para modificar, cancelar o recuperar. El QR nunca contiene la contraseña. El PNG público no incluye la contraseña. Si la biblioteca de QR no carga, se puede recoger con código escrito. Se necesita conexión para confirmar pedidos. Sin registro individual no puede garantizarse que un alumno no suplante a otro.
