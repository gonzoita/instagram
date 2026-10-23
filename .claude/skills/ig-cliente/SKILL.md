---
name: ig-cliente
description: >-
  Manage the clients this repo runs Instagram for - add a new client folder,
  switch the active client, or list them. Use when the user says "/ig-cliente",
  "nuevo cliente", "cambiar de cliente", "trabajo con X", "qué clientes tengo",
  or names a client that has no folder yet.
---

# ig-cliente

Every other skill in the pack reads and writes the active client's folder,
`clientes/<cliente>/`. This skill is the only one that creates those folders or
changes which one is active. The rules it enforces are in `CLAUDE.md`.

The folder name is the client's name in lowercase, accents removed, spaces as
hyphens: "Café Ñandú" becomes `cafe-nandu`.

## No argument: list

List every folder in `clientes/` except `_plantilla` and `_archivo`, mark the
one named in `clientes/ACTIVO`, and say for each whether `voice.md` is still
the empty template.

## `nuevo <nombre>`: add a client

1. If `clientes/<cliente>/` already exists, stop and offer to switch to it
   instead. Never overwrite a client folder.
2. Copy `clientes/_plantilla/` to `clientes/<cliente>/`.
3. Write `<cliente>` as the only line of `clientes/ACTIVO`.
4. Fill `voice.md` with the user. The best input is 3 to 5 real captions or
   reel transcripts from the client: ask for them, write `voice.md` from them,
   then ask only for what the samples cannot tell you (language, offer,
   audience, off-limits topics, proof, the ask). Leave a field empty rather
   than invent it.
5. Suggest the next two steps: `/ig-profile` for a baseline score, and
   `/ig-viral` to build the client's `swipe.md`.

## `cambiar <nombre>`: switch client

1. Match the name to an existing folder. If there is no exact match, show the
   list and ask. Never create a folder here.
2. Write the folder name as the only line of `clientes/ACTIVO`.
3. Confirm in one line: the client and whether its `voice.md`, `swipe.md` and
   `plan.md` exist.

## `archivar <nombre>`: archive a client

Move `clientes/<cliente>/` to `clientes/_archivo/<cliente>/` and clear
`clientes/ACTIVO` if it named that client. Ask once before moving.

Nothing in this skill posts, logs in, or touches the client's Instagram account.
