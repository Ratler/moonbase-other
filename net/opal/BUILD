(

  patch_it $SOURCE2 1 &&
  patch_it $SOURCE3 1 &&
  patch_it $SOURCE4 1 &&
  patch_it $SOURCE5 1 &&
  patch_it $SOURCE6 0 &&

  sedit "s:\$(OBJECTS) \$(LIBS):\$(OBJECTS) \$(LIBS) -lpthread:" plugins/plugin-inc.mak.in &&

  default_build

) > $C_FIFO 2>&1
