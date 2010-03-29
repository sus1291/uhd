#
# Copyright 2010 Ettus Research LLC
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
#

ADD_EXECUTABLE(discover_usrps discover_usrps.cpp)
TARGET_LINK_LIBRARIES(discover_usrps uhd)
INSTALL(TARGETS discover_usrps RUNTIME DESTINATION ${RUNTIME_DIR})

ADD_EXECUTABLE(usrp2_burner usrp2_burner.cpp)
TARGET_LINK_LIBRARIES(usrp2_burner uhd)
INSTALL(TARGETS usrp2_burner RUNTIME DESTINATION ${PKG_DATA_DIR}/utils)

INSTALL(PROGRAMS usrp2_recovery.py DESTINATION ${PKG_DATA_DIR}/utils)