# okaru-play: media player de OKARU. Se compila contra el núcleo instalado (paquete okaru-core).
project('okaru-play', 'cpp',
  version: files('VERSION'),
  meson_version: '>=1.1',
  default_options: ['cpp_std=c++23', 'cpp_extensions=false', 'warning_level=0', 'b_ndebug=if-release'],
)

# El núcleo y sus bibliotecas son privados (/usr/lib/okaru): se enlazan con su ruta en el binario.
_okaru_libdir = get_option('prefix') / get_option('libdir') / 'okaru'
_deps = [dependency('okaru-core'), dependency('mpv')]
_inc = include_directories('src')
_args = ['-Wall', '-Wextra', '-Wno-missing-field-initializers', '-Wpedantic', '-Wconversion', '-Wshadow']

executable('okaru-play',
  sources: files('src/apps/player/main.cpp', 'src/apps/player/mpris_server.cpp', 'src/apps/player/mpv_player.cpp', 'src/apps/player/player_window.cpp'),
  include_directories: _inc,
  dependencies: _deps,
  cpp_args: _args,
  install_rpath: _okaru_libdir,
  install: true,
)

# Sus textos, que el núcleo busca en /usr/share/okaru/apps/player/translations.
install_subdir('apps/player/translations', install_dir: get_option('datadir') / 'okaru' / 'apps' / 'player')
install_data('assets/dev.okaru.Player.desktop', install_dir: get_option('datadir') / 'applications')

if get_option('tests').allowed()
  test('okaru_player', executable('okaru_player_test',
    sources: files('tests/okaru_player_test.cpp', 'src/apps/player/mpv_player.cpp'),
    include_directories: _inc,
    dependencies: _deps,
    build_rpath: _okaru_libdir,
    override_options: ['b_ndebug=false'],
  ))
endif
