=====================
wx_icons_hicolor
=====================

.. start short_desc

**Hicolor icon theme for wxPython**

.. end short_desc

This package provides a wxPython wxArtProvider class with icons from the Hicolor/Gnome Icon Theme.

.. start shields 

.. list-table::
	:stub-columns: 1
	:widths: 10 90

	* - Docs
	  - |docs|
	* - Tests
	  - |travis| |requires| |codefactor|
	* - PyPI
	  - |pypi-version| |supported-versions| |supported-implementations| |wheel|
	* - Other
	  - |license| |language| |commits-since| |commits-latest| |maintained| 

.. |docs| image:: https://readthedocs.org/projects/custom_wx_icons_hicolor/badge/?version=latest
	:target: https://custom_wx_icons_hicolor.readthedocs.io/en/latest/?badge=latest
	:alt: Documentation Status

.. |travis| image:: https://img.shields.io/travis/com/domdfcoding/custom_wx_icons_hicolor/master?logo=travis
	:target: https://travis-ci.com/domdfcoding/custom_wx_icons_hicolor
	:alt: Travis Build Status

.. |requires| image:: https://requires.io/github/domdfcoding/custom_wx_icons_hicolor/requirements.svg?branch=master
	:target: https://requires.io/github/domdfcoding/custom_wx_icons_hicolor/requirements/?branch=master
	:alt: Requirements Status

.. |codefactor| image:: https://img.shields.io/codefactor/grade/github/domdfcoding/custom_wx_icons_hicolor
	:target: https://www.codefactor.io/repository/github/domdfcoding/custom_wx_icons_hicolor
	:alt: CodeFactor Grade

.. |pypi-version| image:: https://img.shields.io/pypi/v/wx_icons_hicolor.svg
	:target: https://pypi.org/project/wx_icons_hicolor/
	:alt: PyPI - Package Version

.. |supported-versions| image:: https://img.shields.io/pypi/pyversions/wx_icons_hicolor.svg
	:target: https://pypi.org/project/wx_icons_hicolor/
	:alt: PyPI - Supported Python Versions

.. |supported-implementations| image:: https://img.shields.io/pypi/implementation/wx_icons_hicolor
	:target: https://pypi.org/project/wx_icons_hicolor/
	:alt: PyPI - Supported Implementations

.. |wheel| image:: https://img.shields.io/pypi/wheel/wx_icons_hicolor
	:target: https://pypi.org/project/wx_icons_hicolor/
	:alt: PyPI - Wheel

.. |license| image:: https://img.shields.io/github/license/domdfcoding/custom_wx_icons_hicolor
	:alt: License
	:target: https://github.com/domdfcoding/custom_wx_icons_hicolor/blob/master/LICENSE

.. |language| image:: https://img.shields.io/github/languages/top/domdfcoding/custom_wx_icons_hicolor
	:alt: GitHub top language

.. |commits-since| image:: https://img.shields.io/github/commits-since/domdfcoding/custom_wx_icons_hicolor/v0.1.1
	:target: https://github.com/domdfcoding/custom_wx_icons_hicolor/pulse
	:alt: GitHub commits since tagged version

.. |commits-latest| image:: https://img.shields.io/github/last-commit/domdfcoding/custom_wx_icons_hicolor
	:target: https://github.com/domdfcoding/custom_wx_icons_hicolor/commit/master
	:alt: GitHub last commit

.. |maintained| image:: https://img.shields.io/maintenance/yes/2020
	:alt: Maintenance

.. end shields

Installation
===============

.. start installation

``wx_icons_hicolor`` can be installed from PyPI.

To install with ``pip``:

.. code-block:: bash

	$ python -m pip install wx_icons_hicolor

.. end installation

Usage
============

To use ``wx_icons_hicolor`` in your application:

.. code-block:: python

	from wx_icons_hicolor import wxHicolorIconTheme

	class MyApp(wx.App):
		def OnInit(self):
			wx.ArtProvider.Push(wxHicolorIconTheme())
			self.frame = TestFrame(None, wx.ID_ANY)
			self.SetTopWindow(self.frame)
			self.frame.Show()
			return True

And then the icons can be accessed through wx.ArtProvider:

.. code-block:: python

	wx.ArtProvider.GetBitmap('document-new', wx.ART_OTHER, wx.Size(48, 48))

Any `FreeDesktop Icon Theme Specification <https://specifications.freedesktop.org/icon-naming-spec/icon-naming-spec-latest.html>`_ name can be used.

Currently the `Client ID` is not used, so just pass `wx.ART_OTHER`.
