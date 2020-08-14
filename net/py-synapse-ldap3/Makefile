# $OpenBSD: $

COMMENT =	ldap auth mechanism for synapse

MODPY_EGG_VERSION =	0.1.4

PKGNAME =	py-synapse-ldap3-${MODPY_EGG_VERSION}

GH_ACCOUNT =	matrix-org
GH_PROJECT =	matrix-synapse-ldap3
GH_TAGNAME =	v${MODPY_EGG_VERSION}
CATEGORIES =	net

HOMEPAGE =	https://matrix.org/

MAINTAINER =	Aisha Tammy <openbsd@aisha.cc>

# Apache 2.0
PERMIT_PACKAGE =	Yes

MODULES =	lang/python

FLAVORS =	python3
FLAVOR ?=	python3

MODPY_SETUPTOOLS =	YES

RUN_DEPENDS =	databases/py-ldap${MODPY_FLAVOR} \
		devel/py-twisted${MODPY_FLAVOR} \
		security/py-service_identity${MODPY_FLAVOR}

NO_TEST	=	Yes


.include <bsd.port.mk>
