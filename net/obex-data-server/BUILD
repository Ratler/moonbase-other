
  patch_it $SOURCE2 1 &&

  sedit "s:OBEX_FindInterfaces(obex_context->obex_handle, &obex_intf): OBEX_EnumerateInterfaces(obex_context->obex_handle):" src/ods-obex.c &&

  OPTS+=" --enable-system-config" &&

  default_build
