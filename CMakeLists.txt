# Copyright (C) 2007-2009 LuaDist.
# Created by Peter Kapec
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.
# Please note that the package source code is licensed under its own license.

PROJECT(lua_tinycdb C)
CMAKE_MINIMUM_REQUIRED(VERSION 2.8)
INCLUDE(dist.cmake)

# Build
SET(SRC cdb_find.c cdb_findnext.c cdb_hash.c cdb_init.c
		cdb_make_add.c cdb_make.c cdb_make_put.c cdb_seek.c
		cdb_seq.c cdb_unpack.c lcdb.c)

ADD_LUA_MODULE(cdb ${SRC})

# Install all files and documentation
INSTALL (TARGETS cdb DESTINATION ${INSTALL_CMOD})
INSTALL (FILES LICENSE DOCUMENTATION.mkd README.mkd cdb.txt DESTINATION ${INSTALL_DATA})
INSTALL (FILES example.lua DESTINATION ${INSTALL_EXAMPLE})
INSTALL (FILES test.lua DESTINATION ${INSTALL_TEST})
