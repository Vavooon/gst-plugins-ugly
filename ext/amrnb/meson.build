amrnb_dep = dependency('opencore-amrnb', version : '>= 0.1.3', required : false)

if amrnb_dep.found()
  amrnb = library('gstamrnb',
    ['amrnb.c', 'amrnbdec.c', 'amrnbenc.c'],
    c_args : ugly_args,
    include_directories : [configinc],
    dependencies : [gstaudio_dep, amrnb_dep],
    install : true,
    install_dir : plugins_install_dir,
  )
  pkgconfig.generate(amrnb, install_dir : plugins_pkgconfig_install_dir)
  install_data(sources: 'GstAmrnbEnc.prs', install_dir: presetdir)
endif
