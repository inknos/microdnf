microdnf_srcs = [
  'dnf-main.c',
  'dnf-command.c',
  'dnf-utils.c',

  # install
  gnome.compile_resources(
    'dnf-install',
    'plugins/install/dnf-command-install.gresource.xml',
    c_name : 'dnf_command_install',
    source_dir : 'plugins/install',
  ),
  'plugins/install/dnf-command-install.c',

  # reinstall
  gnome.compile_resources(
    'dnf-reinstall',
    'plugins/reinstall/dnf-command-reinstall.gresource.xml',
    c_name : 'dnf_command_reinstall',
    source_dir : 'plugins/reinstall',
  ),
  'plugins/reinstall/dnf-command-reinstall.c',

  # remove
  gnome.compile_resources(
    'dnf-remove',
    'plugins/remove/dnf-command-remove.gresource.xml',
    c_name : 'dnf_command_remove',
    source_dir : 'plugins/remove',
  ),
  'plugins/remove/dnf-command-remove.c',

  # update
  gnome.compile_resources(
    'dnf-update',
    'plugins/update/dnf-command-update.gresource.xml',
    c_name : 'dnf_command_update',
    source_dir : 'plugins/update',
  ),
  'plugins/update/dnf-command-update.c',

  # repolist
  gnome.compile_resources(
    'dnf-repolist',
    'plugins/repolist/dnf-command-repolist.gresource.xml',
    c_name : 'dnf_command_repolist',
    source_dir : 'plugins/repolist',
  ),
  'plugins/repolist/dnf-command-repolist.c',

  # repoquery
  gnome.compile_resources(
    'dnf-repoquery',
    'plugins/repoquery/dnf-command-repoquery.gresource.xml',
    c_name : 'dnf_command_repoquery',
    source_dir : 'plugins/repoquery',
  ),
  'plugins/repoquery/dnf-command-repoquery.c',

  # clean
  gnome.compile_resources(
    'dnf-clean',
    'plugins/clean/dnf-command-clean.gresource.xml',
    c_name : 'dnf_command_clean',
    source_dir : 'plugins/clean',
  ),
  'plugins/clean/dnf-command-clean.c',
]

microdnf = executable(
  'microdnf',
  sources : microdnf_srcs,
  dependencies : [
    glib,
    gobject,
    libpeas,
    libdnf,
    scols,
  ],
  c_args : [
    '-DBUILDDIR="@0@"'.format(meson.current_build_dir()),
    '-DSRCDIR="@0@"'.format(meson.current_source_dir()),
  ],
  install : true
)
