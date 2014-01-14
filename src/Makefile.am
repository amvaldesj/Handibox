## Process this file with automake to produce Makefile.in

appdir = $(pyexecdir)/handibox
all-local: config.py

app_PYTHON = \
	__init__.py \
	HandiboxMain.py \
	Calibrations.py \
	Camera.py \
	CameraSettings.py \
	FaceTracking.py \
	HandiboxSettings.py \
	MouseTweak.py \
	Process_manager.py \
	ScreenKeyboard.py \
	ScreenMagnifier.py

nodist_app_PYTHON = config.py

EXTRA_DIST = \
	config.py.in

CLEANFILES = \
	config.py

config.py: config.py.in Makefile
	sed \
		-e s!\@HAARDIR\@!$(datadir)! \
		-e s!\@PACKAGE_NAME\@!$(PACKAGE_NAME)! \
		-e s!\@PACKAGE_VERSION\@!$(PACKAGE_VERSION)! \
		< $< \
		> $@
