# Copyright (C) 2007-2012 LuaDist.
# Created by Peter Kapec
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.
# Please note that the package source code is licensed under its own license.

project ( lua-tinycdb C )
cmake_minimum_required ( VERSION 2.8 )
include ( cmake/dist.cmake )
include ( lua )

# Build
set ( SRC cdb_find.c cdb_findnext.c cdb_hash.c cdb_init.c cdb_make_add.c cdb_make.c 
  cdb_make_put.c cdb_seek.c cdb_seq.c cdb_unpack.c lcdb.c )

# Install all files and documentation
install_lua_module ( cdb ${SRC} )
install_data ( LICENSE README.mkd cdb.txt )
install_doc ( DOCUMENTATION.mkd )
install_example ( example.lua )
install_test ( test.lua )
