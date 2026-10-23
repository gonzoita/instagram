# Manual: empezar con un cliente nuevo

Se trabaja en un chat dentro del proyecto. Un chat nuevo no recuerda nada: lo que
vale está en `clientes/<cliente>/`.

## A. Cliente nuevo (una sola vez)

1. Abre un chat nuevo en el proyecto.
2. Reúne antes, para tenerlo a mano:
   - Los tres documentos de marca: perfil, competencia y diseño. Deben estar completos.
   - De 3 a 5 captions o transcripciones de reels reales del cliente.
   - El @ exacto de Instagram.
3. Escribe: `/ig-cliente nuevo <nombre del cliente>`
4. Adjunta los tres documentos en el chat y di: "guárdalos en marca/ sin cambiarlos".
5. Pega los textos reales y di: "escribe el voice.md desde el perfil y estos textos".
   Responde solo lo que te pregunte. Lo que no sepas se queda vacío.
6. Revisa `voice.md`. Todo lo que diga "confirmar" o "pendiente" lo validas con el cliente.
7. Baseline del perfil: `/ig-profile` (pega bio, link, highlights y el grid actual).
8. Swipe file: `/ig-viral` (te pide nicho y cuentas de referencia; guarda `swipe.md`).
9. Primera semana: `/ig-plan`. Guarda `plan.md`.

Resultado: `clientes/<cliente>/` con `marca/`, `voice.md`, `swipe.md`, `plan.md`, `log.md`.

## B. Cada vez que vuelves (cliente que ya existe)

1. Chat nuevo. Primera frase: `trabajo con <cliente>` (solo esa sesión) o
   `/ig-cliente cambiar <cliente>` (queda como activo).
2. Claude confirma con qué cliente trabaja. Si es otro, corrígelo antes de seguir.
3. Pide lo que toque:
   - Reel: `/ig-reel` con la idea cruda.
   - Carrusel: `/ig-carousel`.
   - Caption: `/ig-caption`.
   - Stories: `/ig-story`.
   - Comentarios en otras cuentas: `/ig-comment`. Mensajes directos: `/ig-dm`.
   - Responder a tus comentarios: `/ig-reply`.
   - Long form a contenido: `/ig-repurpose`.
   - Qué funcionó: `/ig-audit` (pega los insights).
4. Todo texto pasa por `/ig-human` antes de mostrarse.
5. Cuando publiques, dilo ("ya salió el reel X") para que se anote en `log.md`.

## Reglas

- Claude nunca toca la carpeta de otro cliente. Si nombras otro, se detiene y pregunta.
- No pegues contraseñas ni tokens en el chat ni en archivos.
- Lo marcado `[P]` o `[X]` en la marca no se publica como hecho.
- Los cambios en archivos solo quedan guardados si se hace commit y push. Pide
  "guarda y sube los cambios" al terminar la sesión.
