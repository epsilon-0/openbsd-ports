# $OpenBSD $

COMMENT	=	optimized BLAS/LAPACK library based on GotoBLAS
CATEGORIES =	math

VERSION =	0.3.12
DISTNAME =	openblas-${VERSION}
PKGNAME =	${DISTNAME:L}

GH_ACCOUNT =	xianyi
GH_PROJECT =	OpenBLAS
#GH_TAGNAME =	v0.3.12
# correct AVX/AVX2 detection  
GH_COMMIT =	fab952bee4ba65dd9950aef739dda1813facfe76

SHARED_LIBS =	openblas 0.0 \
		blas 7.2 \
		cblas 7.2 \
		lapack 7.2 \
		lapacke 7.2

MAINTAINER =	Aisha Tammy <openbsd@aisha.cc>

# BSD
PERMIT_PACKAGE =	Yes

WANT_LIB +=	c m pthread

MODULES =	fortran
MODFORTRAN_COMPILER =	gfortran

USE_GMAKE =	Yes


MAKE_ENV =	CFLAGS="${CFLAGS}" FFLAGS="${CFLAGS}" \
		LDFLAGS="${LDFLAGS} -L${LOCALBASE}/lib"\
		FC="${MODFORTRAN_COMPILER}" CC="clang" \
		LIBopenblas_VERSION="${LIBopenblas_VERSION}" \
		LIBblas_VERSION="${LIBblas_VERSION}" \
		LIBcblas_VERSION="${LIBcblas_VERSION}" \
		LIBlapack_VERSION="${LIBlapack_VERSION}" \
		LIBlapacke_VERSION="${LIBlapacke_VERSION}" \
		USE_THREAD=1 USE_OPENMP=0 \
		NUM_PARALLEL=2 NUM_THREADS=24 \
		MAKE_NB_JOBS=-1 \
		NO_STATIC=0 \
		DYNAMIC_ARCH=1 DYNAMIC_OLDER=1 \
		NO_AFFINITY=1 TARGET=GENERIC \
		BUILD_RELAPACK=1

TEST_TARGET =	tests

FAKE_SETUP =	PREFIX=${TRUEPREFIX} DESTDIR=${WRKINST}

post-build:
	cd ${WRKSRC}/interface && env -i ${MAKE_ENV} \
		${MAKE_PROGRAM} ${MAKE_FLAGS} shared-blas-lapack

post-install:
	cd ${WRKSRC}/interface && \
		${INSTALL_DATA} libblas.so.${LIBblas_VERSION} \
			libcblas.so.${LIBcblas_VERSION} \
			liblapack.so.${LIBlapack_VERSION} \
			liblapacke.so.${LIBlapacke_VERSION} \
			${WRKINST}/usr/local/lib

.include <bsd.port.mk>
