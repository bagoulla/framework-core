#
# This file is protected by Copyright. Please refer to the COPYRIGHT file 
# distributed with this source distribution.
# 
# This file is part of REDHAWK core.
# 
# REDHAWK core is free software: you can redistribute it and/or modify it under 
# the terms of the GNU Lesser General Public License as published by the Free 
# Software Foundation, either version 3 of the License, or (at your option) any 
# later version.
# 
# REDHAWK core is distributed in the hope that it will be useful, but WITHOUT 
# ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS 
# FOR A PARTICULAR PURPOSE.  See the GNU Lesser General Public License for more
# details.
# 
# You should have received a copy of the GNU Lesser General Public License 
# along with this program.  If not, see http://www.gnu.org/licenses/.
#

# DO NOT PUT ANY CORBA DEPENDENCIES INTO THE PARSER LIBRARY!!!

noinst_LTLIBRARIES = libossieparser.la
libossieparser_la_SOURCES = Properties.cpp \
			    debug.cpp \
			    SoftPkg.cpp \
			    DomainManagerConfiguration.cpp \
			    ComponentDescriptor.cpp \
			    DeviceManagerConfiguration.cpp \
			    SoftwareAssembly.cpp \
			    componentProfile.cpp \
			    internal/prf-pskel.cpp \
			    internal/dmd-pskel.cpp \
			    internal/dcd-pskel.cpp \
			    internal/dpd-pskel.cpp \
			    internal/spd-pskel.cpp \
			    internal/sad-pskel.cpp \
			    internal/scd-pskel.cpp \
			    internal/profile-pskel.cpp \
			    internal/dmd-pimpl.cpp \
			    internal/dcd-pimpl.cpp \
			    internal/dpd-pimpl.cpp \
			    internal/spd-pimpl.cpp \
			    internal/sad-pimpl.cpp \
			    internal/scd-pimpl.cpp \
			    internal/prf-pimpl.cpp \
			    internal/profile-pimpl.cpp

libossieparser_la_CXXFLAGS = -Wall $(STDINTF_CFLAGS) $(EXPAT_CFLAGS) $(BOOST_CPPFLAGS) 
libossieparser_la_LIBADD = $(STDINTF_LIBS) $(EXPAT_LIBS)
libossieparser_la_LDFLAGS = -Wall $(EXPAT_LDFLAGS)

AM_CPPFLAGS = -I../include -I. -I$(top_srcdir)/base/include

internal/dmd-pskel.cpp: $(top_srcdir)/xml/xsd/dmd.xsd internal/dmd.map

internal/dcd-pskel.cpp: $(top_srcdir)/xml/xsd/dcd.xsd internal/dcd.map

internal/spd-pskel.cpp: $(top_srcdir)/xml/xsd/spd.xsd internal/spd.map

internal/scd-pskel.cpp: $(top_srcdir)/xml/xsd/scd.xsd internal/scd.map

internal/sad-pskel.cpp: $(top_srcdir)/xml/xsd/sad.xsd internal/sad.map

internal/prf-pskel.cpp: $(top_srcdir)/xml/xsd/prf.xsd internal/prf.map

internal/dpd-pskel.cpp: $(top_srcdir)/xml/xsd/dpd.xsd

internal/profile-pskel.cpp: $(top_srcdir)/xml/xsd/profile.xsd

.PHONY: generate_noop_impl generate_test_driver

generate_noop_impl:

generate_test_driver:

clean-local:
	rm -f internal/*-driver.cpp
