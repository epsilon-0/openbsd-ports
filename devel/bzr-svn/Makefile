# $OpenBSD: Makefile,v 1.8 2021/02/23 19:39:13 sthen Exp $

COMMENT=	bzr plugin that adds support for foreign svn repositories

MODPY_EGG_VERSION= 1.1.2
DISTNAME=	bzr-svn-${MODPY_EGG_VERSION}
CATEGORIES=	devel

HOMEPAGE=	http://launchpad.net/bzr-svn

# GPL 
PERMIT_PACKAGE=	Yes

MASTER_SITES=	http://launchpad.net/bzr-svn/${MODPY_EGG_VERSION:C/..$//}/${MODPY_EGG_VERSION}/+download/

MODULES=	lang/python
MODPY_VERSION =	${MODPY_DEFAULT_VERSION_2}

RUN_DEPENDS=	devel/bzr

.include <bsd.port.mk>
