# Copyright (C) 2015-2016  Thomas Pircher <tehpeh-web@tty1.net>
#
# woale -- a wiki engine.
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <http://www.gnu.org/licenses/>.


install(FILES "etc/woale.conf"
    DESTINATION ${CMAKE_INSTALL_SYSCONFDIR})


install(FILES "share/main.css"
    DESTINATION "${CMAKE_INSTALL_DATADIR}/woale")

if(EXISTS "${CMAKE_CURRENT_SOURCE_DIR}/share/marked.min.js")
    install(FILES "share/marked.min.js"
        DESTINATION "${CMAKE_INSTALL_DATADIR}/woale")
endif()

install(FILES "sql/schema-sqlite.sql"
    DESTINATION "${CMAKE_INSTALL_DOCDIR}")
