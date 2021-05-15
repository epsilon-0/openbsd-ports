# $OpenBSD $

COMMENT =	minimalistic command line pastebin
CATEGORIES =	www net

GH_ACCOUNT =	PurritoBin
GH_PROJECT =	PurritoBin
GH_TAGNAME =	0.6.7

HOMEPAGE =	https://bsd.ac/
MAINTAINER =	Aisha Tammy <openbsd@aisha.cc>

# ISC
PERMIT_PACKAGE =	Yes

# uses pledge()
WANTLIB +=	${COMPILER_LIBCXX} c lmdb usockets

# C++17
COMPILER =	base-clang

MODULES =	devel/meson

CXXFLAGS +=	-I${LOCALBASE}/include

CONFIGURE_ENV = LDFLAGS="${LDFLAGS} -L${LOCALBASE}/lib"

# ssl tests fail
#CONFIGURE_ARGS= -Denable_testing=true \
#		-Dtest_shuf=gshuf \
#		-Dtest_seq=gseq

BUILD_DEPENDS =	databases/lmdbxx \
		www/uwebsockets

LIB_DEPENDS =	databases/lmdb \
		net/usockets

TEST_DEPENDS =	net/curl \
		sysutils/coreutils \

.include <bsd.port.mk>
