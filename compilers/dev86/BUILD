(

  # Prevent installation of files conflicting with bin86
  patch_it $SOURCE2 0  &&

  sedit "s/CFLAGS=  -O/CFLAGS=  $CFLAGS/1" Makefile  &&
  sedit "s:(PREFIX)/man:(PREFIX)/share/man:1" Makefile  &&

  default_build

) > $C_FIFO 2>&1
