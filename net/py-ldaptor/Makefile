# $OpenBSD: $

COMMENT =	ldap auth mechanism for synapse

MODPY_EGG_VERSION =	19.1.0
DISTNAME =	ldaptor-${MODPY_EGG_VERSION}
PKGNAME =	py-${DISTNAME}
CATEGORIES =	net

HOMEPAGE =	https://github.com/twisted/ldaptor

MASTER_SITES =	${MASTER_SITE_PYPI:=l/ldaptor/}

MAINTAINER =	Aisha Tammy <openbsd@aisha.cc>

# Apache 2.0
PERMIT_PACKAGE =	Yes

MODULES =	lang/python

FLAVORS =	python3
FLAVOR ?=	python3

MODPY_SETUPTOOLS =	YES

RUN_DEPENDS =	devel/py-parsing${MODPY_FLAVOR} \
		devel/py-twisted${MODPY_FLAVOR} \
		devel/py-zopeinterface${MODPY_FLAVOR} \
		security/py-passlib${MODPY_FLAVOR}


.include <bsd.port.mk>
