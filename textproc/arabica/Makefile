COMMENT =	XML and HTML processing toolkit
DISTNAME =	arabica-2010-November
PKGNAME =	arabica-2010.11
CATEGORIES =	textproc
SITES =		${SITE_SOURCEFORGE:=arabica/}
REVISION =	3

HOMEPAGE =	http://www.jezuk.co.uk/cgi-bin/view/arabica

SHARED_LIBS +=	arabica	0.0 # 0.0

# BSD-like
PERMIT_PACKAGE=	Yes

WANTLIB +=	c expat m ${COMPILER_LIBCXX}

FIX_CRLF_FILES =	include/Taggle/impl/html/HTMLScanner.hpp \
			include/XPath/impl/xpath_logical.hpp

COMPILER =		base-clang ports-gcc base-gcc

CXXFLAGS_base-clang =	-std=c++14

CONFIGURE_STYLE =	gnu

BUILD_DEPENDS =	devel/boost
CONFIGURE_ENV =	CPPFLAGS='-I${LOCALBASE}/include'

.include <bsd.port.mk>
