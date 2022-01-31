project('patchelf', 'cpp',
  license : 'GPL-3.0-or-later',
  version : '0.14.5',
  default_options : ['cpp_std=c++17']
)

patchelf_args = [
  '-D', 'DEFAULT_PAGESIZE=@0@'.format(get_option('page-size')),
  '-D', 'PACKAGE_STRING="@0@ @1@"' \
    .format(meson.project_name(), meson.project_version()),
]

executable('patchelf', files('src/patchelf.cc'),
  cpp_args : patchelf_args,
  install : true)

install_man(files('patchelf.1'))

subdir('tests')
