# okaru-play

**English** · [Español](#español)

The media player of [OKARU](https://github.com/MrAndyVF/okaru) (郁): videos and music on libmpv, with MPRIS controls and the shell's look and theme.

## Install

It ships in OKARU's pacman repository `[okaru]` (set up by OKARU's installer):

```sh
sudo pacman -S okaru-play
```

## Build

It builds against OKARU's shared core, provided by the `okaru-core` package:

```sh
meson setup build && meson compile -C build
meson test -C build
# Run it with the translations from this repository:
OKARU_APPS_DIR=$PWD/apps ./build/okaru-play
```

Translations live in `apps/player/translations/` (English and Spanish).

## License

MIT.

---

## Español

El reproductor multimedia de [OKARU](https://github.com/MrAndyVF/okaru) (郁): videos y música con libmpv, controles MPRIS y el aspecto y el tema de la shell.

### Instalar

Viene en el repositorio pacman de OKARU, `[okaru]` (lo configura el instalador de OKARU):

```sh
sudo pacman -S okaru-play
```

### Compilar

Se compila contra el núcleo compartido de OKARU, que trae el paquete `okaru-core`:

```sh
meson setup build && meson compile -C build
meson test -C build
# Ejecutarla con las traducciones de este repositorio:
OKARU_APPS_DIR=$PWD/apps ./build/okaru-play
```

Las traducciones están en `apps/player/translations/` (inglés y español).

### Licencia

MIT.
