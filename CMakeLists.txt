# Copyright (C) 2016 LuaDist.
# Created by Peter Kapec
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.
# Please note that the package source code is licensed under its own license.

project ( luacheck NONE )
cmake_minimum_required ( VERSION 2.8 )
include ( cmake/dist.cmake )
include ( lua )

install_lua_module( luacheck.init  src/luacheck/init.lua )
install_lua_module( luacheck.main  src/luacheck/main.lua )
install_lua_module( luacheck.config  src/luacheck/config.lua )
install_lua_module( luacheck.linearize  src/luacheck/linearize.lua )
install_lua_module( luacheck.analyze  src/luacheck/analyze.lua )
install_lua_module( luacheck.reachability  src/luacheck/reachability.lua )
install_lua_module( luacheck.core_utils  src/luacheck/core_utils.lua )
install_lua_module( luacheck.check  src/luacheck/check.lua )
install_lua_module( luacheck.parser  src/luacheck/parser.lua )
install_lua_module( luacheck.lexer  src/luacheck/lexer.lua )
install_lua_module( luacheck.filter  src/luacheck/filter.lua )
install_lua_module( luacheck.options  src/luacheck/options.lua )
install_lua_module( luacheck.inline_options  src/luacheck/inline_options.lua )
install_lua_module( luacheck.stds  src/luacheck/stds.lua )
install_lua_module( luacheck.expand_rockspec  src/luacheck/expand_rockspec.lua )
install_lua_module( luacheck.multithreading  src/luacheck/multithreading.lua )
install_lua_module( luacheck.cache  src/luacheck/cache.lua )
install_lua_module( luacheck.format  src/luacheck/format.lua )
install_lua_module( luacheck.version  src/luacheck/version.lua )
install_lua_module( luacheck.fs  src/luacheck/fs.lua )
install_lua_module( luacheck.globbing  src/luacheck/globbing.lua )
install_lua_module( luacheck.utils  src/luacheck/utils.lua )
install_lua_module( luacheck.argparse  src/luacheck/argparse.lua )

#BUG: there is a problem with cyclic requires
#install_lua_executable( luacheck bin/luacheck.lua ) # not working
install ( PROGRAMS bin/luacheck.lua DESTINATION ${INSTALL_BIN} RENAME luacheck)

install_doc ( docsrc/ )
install_data ( README.md LICENSE )
