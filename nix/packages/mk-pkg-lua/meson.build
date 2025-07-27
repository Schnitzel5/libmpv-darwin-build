# https://mesonbuild.com/External-Project-module.html

project('lua', 'c')

mod = import('unstable-external_project')

p = mod.add_project('configure',
    configure_options : [
        '--prefix=@PREFIX@',
        '--disable-static',
        '--enable-fast-install',
        '--disable-dependency-tracking',
        '--disable-test',
        '--disable-compare',
        '--disable-profile',
        '--disable-fuzz',
        '--disable-fontconfig',
        '--disable-directwrite',
        '--enable-coretext',
        '--disable-libunibreak',
        '--disable-require-system-font-provider',
        '--disable-asm',
        '--disable-large-tiles',
        '--with-pic',
        '--with-aix-soname=aix',
        '--without-gnu-ld',
    ],
    verbose: true,
)

lua_dep = p.dependency('lua')
meson.override_dependency('lua', lua_dep)
