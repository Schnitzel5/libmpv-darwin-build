# https://mesonbuild.com/External-Project-module.html

project('lua', 'c')

mod = import('unstable-external_project')

p = mod.add_project('configure',
    configure_options : [
        '--prefix=@PREFIX@',
        '--disable-static',
        '--enable-shared',
    ],
    verbose: true,
)

lua_dep = p.dependency('lua')
meson.override_dependency('lua', lua_dep)
