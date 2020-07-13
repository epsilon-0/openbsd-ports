# $OpenBSD: $

COMMENT =	ldap auth mechanism for synapse

MODPY_EGG_VERSION =	0.1.4

GH_ACCOUNT =	matrix-org
GH_PROJECT =	matrix-synapse-ldap3
GH_TAGNAME =	v${MODPY_EGG_VERSION}
CATEGORIES =	net

HOMEPAGE =	https://matrix.org/

MAINTAINER =	Aisha Tammy <openbsd@aisha.cc>

# Apache 2.0
PERMIT_PACKAGE =	Yes

MODULES =	lang/python

MODPY_VERSION =	${MODPY_DEFAULT_VERSION_3}
MODPY_SETUPTOOLS =	Yes

RUN_DEPENDS =	databases/py-ldap${MODPY_FLAVOR} \
		devel/py-twisted${MODPY_FLAVOR} \
		security/py-service_identity${MODPY_FLAVOR}

NO_TEST	=	Yes


.include <bsd.port.mk>
