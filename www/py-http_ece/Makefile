MODPY_EGG_VERSION =	1.1.0
COMMENT =		encrypted Content Encoding for HTTP
DISTNAME =		http_ece-${MODPY_EGG_VERSION}
PKGNAME =		py-http_ece-${MODPY_EGG_VERSION}
CATEGORIES =		www
REVISION =		6

HOMEPAGE =		https://github.com/martinthomson/encrypted-content-encoding
MAINTAINER =		Pamela Mosiejczuk <pamela@openbsd.org>

# MIT
PERMIT_PACKAGE =	Yes

MODULES =		lang/python
MODPY_PYBUILD =		setuptools
MODPY_PI =		Yes

FLAVORS =		python3
FLAVOR =		python3

RUN_DEPENDS =		security/py-cryptography${MODPY_FLAVOR}

NO_TEST=		Yes

.include <bsd.port.mk>
