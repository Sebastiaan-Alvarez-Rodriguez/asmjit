project('asmjit', 'cpp',  version : '1.0.0',  default_options : ['warning_level=0'])
add_project_arguments('-Dwarning_level=0', language : 'cpp')
warning_level = 0
inc = include_directories('src/asmjit')


libasmjit_files = []
subdir('src')


cc = meson.get_compiler('cpp')
librt = cc.find_library('rt', required : false)
libasmjit_depends = [librt]


libasmjit = shared_library(
    'asmjit',
    libasmjit_files,
    include_directories : inc,
    dependencies : libasmjit_depends,
    install : true)

asmjit_dep = declare_dependency(include_directories : inc, link_with : libasmjit)