COMMENT =	KDE image viewer
DISTNAME =	gwenview-${VERSION}
CATEGORIES =	graphics x11
REVISION =	0

SHARED_LIBS +=  gwenviewlib               59.4 # 4.97

WANTLIB += ${COMPILER_LIBCXX} KF5Activities KF5Auth KF5AuthCore
WANTLIB += KF5Baloo KF5Bookmarks KF5Codecs KF5Completion KF5ConfigCore
WANTLIB += KF5ConfigGui KF5ConfigWidgets KF5CoreAddons KF5FileMetaData
WANTLIB += KF5GuiAddons KF5I18n KF5IconThemes KF5ItemModels KF5ItemViews
WANTLIB += KF5JobWidgets KF5KDcraw KF5KIOCore KF5KIOFileWidgets
WANTLIB += KF5KIOGui KF5KIOWidgets KF5Notifications KF5Parts KF5Purpose
WANTLIB += KF5PurposeWidgets KF5Service KF5Solid KF5SonnetUi KF5TextWidgets
WANTLIB += KF5WidgetsAddons KF5WindowSystem KF5XmlGui Qt5Concurrent
WANTLIB += Qt5Core Qt5DBus Qt5Gui Qt5Network Qt5PrintSupport Qt5Svg
WANTLIB += Qt5WaylandClient Qt5Widgets Qt5X11Extras Qt5Xml X11
WANTLIB += c cfitsio exiv2 jpeg kImageAnnotator lcms2 m phonon4qt5
WANTLIB += png tiff wayland-client z

MODKDE5_DESKTOP_FILE = yes
MODKDE5_ICON_CACHE = yes
MODKDE5_TRANSLATIONS = yes
MODKF5_I18N_CONFLICT = yes
MODKF5_L10N_CONFLICT = yes
MODKDE5_DOCS = yes

BUILD_DEPENDS =	wayland/wayland-protocols \
		wayland/plasma-wayland-protocols

RUN_DEPENDS =	devel/kf5/kfilemetadata \
		x11/kde-applications/ffmpegthumbs>=${MODKDE_VERSION} \
		x11/kde-applications/kdesdk-thumbnailers>=${MODKDE_VERSION} \
		x11/kde-applications/kio-extras>=${MODKDE_VERSION}

LIB_DEPENDS =	devel/kf5/baloo \
		devel/kf5/kactivities \
		devel/kf5/kauth \
		devel/kf5/kbookmarks \
		devel/kf5/kcodecs \
		devel/kf5/kcompletion \
		devel/kf5/kconfig \
		devel/kf5/kconfigwidgets \
		devel/kf5/kcoreaddons \
		devel/kf5/kfilemetadata \
		devel/kf5/ki18n \
		devel/kf5/kiconthemes \
		devel/kf5/kio \
		devel/kf5/kitemmodels \
		devel/kf5/kitemviews \
		devel/kf5/kjobwidgets \
		devel/kf5/knotifications \
		devel/kf5/kparts \
		devel/kf5/kservice\
		devel/kf5/purpose \
		devel/kf5/solid \
		devel/kf5/sonnet \
		graphics/exiv2 \
		graphics/jpeg \
		graphics/kimageannotator \
		graphics/lcms2 \
		graphics/png \
		math/cfitsio \
		multimedia/phonon \
		x11/kde-applications/libkdcraw>=${MODKDE_VERSION} \
		x11/qt5/qtsvg \
		x11/qt5/qtx11extras \
		wayland/wayland

TEST_IS_INTERACTIVE =	X11

.include <bsd.port.mk>
