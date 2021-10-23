project(
  'sds',
  'c',
  version : '2.1.0',
  default_options : [
    'c_std=c17',
    'warning_level=3',
  ],
)

cmake = import('cmake')

gc_dep = dependency('gc', required : false)
if not gc_dep.found()
  gc_proj = cmake.subproject('bdwgc')
  gc_dep = gc_proj.dependency('gc')
endif

sds_lib = library(
  'sds',
  'sds.c',
  dependencies : [gc_dep],
)

sds_dep = declare_dependency(
  include_directories : include_directories('.'),
  link_with : sds_lib,
  dependencies : gc_dep,
)
