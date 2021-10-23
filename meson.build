project(
  'sds',
  'c',
  version : '2.1.0',
  default_options : [
    'c_std=c17',
    'warning_level=3',
  ],
)

sds_lib = library(
  'sds',
  'sds.c',
)

sds_dep = declare_dependency(
  include_directories : include_directories('.'),
  link_with : sds_lib,
)
