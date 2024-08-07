COMMENT =	Digital Forensics Virtual File System (dfVFS)

MODPY_EGG_VERSION = 20200625
DISTNAME =	dfvfs-${MODPY_EGG_VERSION}
PKGNAME =	py-${DISTNAME}
REVISION =	3

CATEGORIES =	security

HOMEPAGE =	https://github.com/log2timeline/dfvfs/wiki

SITES =		https://github.com/log2timeline/dfvfs/releases/download/${MODPY_EGG_VERSION}/

MAINTAINER =	Remi Pointel <rpointel@openbsd.org>

# Apachev2
PERMIT_PACKAGE =	Yes

MODULES =	lang/python

FLAVORS =	python3
FLAVOR =	python3

MODPY_PYBUILD =	setuptools
RUN_DEPENDS +=	devel/py-construct${MODPY_FLAVOR} \
		security/py-cryptography${MODPY_FLAVOR} \
		security/py-dfdatetime${MODPY_FLAVOR} \
		devel/py-six${MODPY_FLAVOR} \
		sysutils/py-tsk${MODPY_FLAVOR} \
		security/libbde \
		security/libewf \
		sysutils/libfsntfs \
		sysutils/libfvde \
		sysutils/libfwnt \
		sysutils/libluksde \
		sysutils/libqcow \
		sysutils/libsigscan \
		sysutils/libsmdev \
		sysutils/libsmraw \
		sysutils/libvhdi \
		sysutils/libvmdk \
		sysutils/libvshadow \
		sysutils/libvslvm

TEST_DEPENDS +=	devel/py-mock${MODPY_FLAVOR}

do-test:
	touch ${WRKSRC}/utils/__init__.py
	cd ${WRKSRC} && LC_CTYPE='en_US.UTF-8' ${MODPY_BIN} run_tests.py

.include <bsd.port.mk>
