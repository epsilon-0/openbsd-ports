# $OpenBSD: Makefile,v 1.10 2021/02/19 23:13:05 sthen Exp $

COMMENT =		WebSocket client for Python

MODPY_EGG_VERSION =	0.37.0
DISTNAME =		websocket_client-${MODPY_EGG_VERSION}
PKGNAME =		py-websocket-client-${MODPY_EGG_VERSION}
REVISION =		4

CATEGORIES =		net

HOMEPAGE =		https://github.com/liris/websocket-client

# LGPLv2.1+
PERMIT_PACKAGE =	Yes

MODPY_PI =		Yes
MODPY_PI_DIR =		w/websocket-client
MODPY_SETUPTOOLS =	Yes

MODULES =		lang/python
FLAVORS =		python3
FLAVOR ?=

RUN_DEPENDS =		devel/py-six${MODPY_FLAVOR}

post-install:
	mv ${PREFIX}/bin/wsdump.py ${PREFIX}/bin/wsdump.py${MODPY_BIN_SUFFIX}

.include <bsd.port.mk>
