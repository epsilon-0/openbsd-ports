# $OpenBSD: Makefile,v 1.2 2021/02/23 19:39:40 sthen Exp $

COMMENT =	web fuzzer

MODPY_EGG_VERSION =	3.1.0
DISTNAME =	wfuzz-${MODPY_EGG_VERSION}

CATEGORIES =	security www

HOMEPAGE =	https://wfuzz.readthedocs.io/en/latest/

MAINTAINER =	Sebastian Reitenbach <sebastia@openbsd.org>

# GPLv2
PERMIT_PACKAGE =	Yes

MODPY_PI =		Yes

MODULES =		lang/python
MODPY_SETUPTOOLS =	Yes

RUN_DEPENDS =		devel/py-parsing${MODPY_FLAVOR} \
			devel/py-six${MODPY_FLAVOR} \
			net/py-curl${MODPY_FLAVOR} \
			textproc/py-chardet${MODPY_FLAVOR}

BUILD_DEPENDS =		${RUN_DEPENDS}

.include <bsd.port.mk>
