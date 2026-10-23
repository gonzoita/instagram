# Instagram por cliente

Este repo maneja el Instagram de varios clientes con las skills `ig-*` de
`.claude/skills/`. El manual de uso está en el doc "Manual de Instagram por
cliente".

## Cliente activo

- Cada cliente tiene su carpeta en `clientes/<cliente>/` (nombre en minúsculas,
  con guiones). `clientes/_plantilla/` es la plantilla para clientes nuevos.
- El cliente activo es el nombre escrito en `clientes/ACTIVO`.
- Antes de usar cualquier skill `ig-*`, lee `clientes/ACTIVO` y di en una línea
  con qué cliente vas a trabajar. Si el archivo no existe o la carpeta no
  existe, pide el cliente o propone `/ig-cliente nuevo <nombre>`.
- Si el usuario dice al inicio de la sesión "trabajo con <cliente>", usa ese
  cliente durante toda la sesión sin tocar `clientes/ACTIVO`.

## Rutas

- Cuando una skill hable de `clientes/<cliente>/`, o de `voice.md`, `swipe.md`,
  `plan.md` o `log.md` sin ruta, se refiere a la carpeta del cliente activo.
- Nunca leas ni escribas en la carpeta de otro cliente. Si el usuario nombra
  otro cliente a mitad de una tarea, detente y pregunta si quiere cambiar.

## Marca del cliente

Cada cliente puede tener tres documentos en `clientes/<cliente>/marca/`, que son
la fuente de verdad. Las skills los leen y no los reescriben:

- `perfil.md`: identidad, oferta, clientes ideales, voz, pruebas y límites
  (M16: lo que nunca se promete). Manda sobre `voice.md` si hay conflicto.
- `competencia.md`: competidores, keywords con volumen y vacíos de mercado. Úsalo
  para elegir temas (`ig-plan`, `ig-reel`, `ig-carousel`, `ig-repurpose`) y para
  los términos de búsqueda de `ig-caption`.
- `diseno.md`: colores, tipografías y reglas del logo. Úsalo en `ig-carousel` y
  en cualquier pieza con imagen. Si falta un dato visual, pregunta; no lo inventes.

Antes de escribir una pieza, lee `perfil.md` y respeta sus palabras prohibidas,
precios y avisos obligatorios. Un dato marcado `[P]` (proyectado) o `[X]`
(pendiente) no se publica como hecho: se pide validación. Si un archivo de
`marca/` no existe, trabaja con `voice.md` y dilo en una línea.

## Idioma

Escribe todo lo que se vaya a publicar en el idioma que indique el `voice.md`
del cliente. Si no indica ninguno, en español. Las skills están escritas en
inglés, pero eso no cambia el idioma de salida.

## Privacidad

No guardes contraseñas ni tokens de las cuentas de los clientes en ningún
archivo del repo.
