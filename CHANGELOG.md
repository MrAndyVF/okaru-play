# Changelog

Each version has an English and a Spanish section. / Cada versión tiene una sección en inglés y otra en español.

## [1.0.2] - 2026-11-22

### English

#### Changes
- Packaging: the package is **tied to the system libraries it was built against**. When a system update would
  rename one of them, pacman refuses it and names this package, instead of leaving the app unable to start; it goes
  through once OKARU publishes it rebuilt. Released with OKARU 1.3.8.

### Español

#### Cambios
- Empaquetado: el paquete queda **atado a las bibliotecas del sistema con las que se compiló**. Si una actualización
  del sistema le cambiaría el nombre a alguna, pacman se niega y nombra este paquete, en vez de dejar la app sin
  abrir; pasa en cuanto OKARU lo publica recompilado. Sale con OKARU 1.3.8.

## [1.0.1] - 2026-11-18

### English

#### Fixes
- **Clicking the video** pauses or resumes it again, and double-clicking toggles fullscreen. The video area never
  received the left click.

### Español

#### Correcciones
- **Hacer clic en el video** vuelve a pausarlo o reanudarlo, y el doble clic alterna la pantalla completa. El área
  del video nunca recibía el clic izquierdo.

## [1.0.0] - 2026-11-14

### English

#### Changes
- First release as its own package and repository. The media player used to ship inside `okaru` (up to 1.2.4); it now
  builds against the shared core (`okaru-core`) and carries its own translations.

### Español

#### Cambios
- Primera versión como paquete y repositorio propios. El reproductor multimedia venía dentro de `okaru` (hasta la 1.2.4); ahora
  se compila contra el núcleo compartido (`okaru-core`) y trae sus propias traducciones.
