COMMENT=	SDL image library

DISTNAME=	SDL_image-1.2.12
PKGNAME=	${DISTNAME:L:S/_/-/}
REVISION=	5
CATEGORIES=	devel graphics
SITES=		${HOMEPAGE}release/

SHARED_LIBS=	SDL_image	3.1

HOMEPAGE=	https://www.libsdl.org/projects/SDL_image/

# Zlib
PERMIT_PACKAGE=	Yes

WANTLIB=  SDL iconv jpeg lzma m png pthread sndio tiff usbhid webp z
WANTLIB+= zstd

LIB_DEPENDS=	devel/sdl \
		graphics/jpeg \
		graphics/libwebp \
		graphics/png \
		graphics/tiff

CONFIGURE_STYLE=gnu
CONFIGURE_ARGS+=--disable-jpg-shared \
		--disable-png-shared \
		--disable-tif-shared \
		--disable-webp-shared
CONFIGURE_ENV+=	CPPFLAGS="-I${LOCALBASE}/include" \
		LDFLAGS="-L${LOCALBASE}/lib" \
		OBJC="${CC}"

.include <bsd.port.mk>
