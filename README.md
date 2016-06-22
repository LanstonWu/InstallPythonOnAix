Install Python 2.7 on AIX 6
=====
Recently I want use Python on AIX,which is important for my work,so I did search on internet,but I can't find which I want,so I download packages and setp by setp install it,finally I packaged all of package that I use during install,and record all of log here.  
You can download all of packages from :https://drive.google.com/file/d/0B1u0FAf-iPgfcFdZS1M2TGVUVnc/view?usp=sharing    
You can also download package of python for aix from:http://www.perzl.org/aix/index.php?n=main.python
```xml
[aix6:root]oslevel
6.1.0.0
[aix6:root]rpm -Uvh readline-6.3-5.aix5.1.ppc.rpm
package readline-6.3-5 is already installed
[aix6:root]rpm -Uvh bzip2-1.0.6-1.aix5.1.ppc.rpm 
package bzip2-1.0.6-1 is already installed
[aix6:root]rpm -Uvh db4-4.7.25-2.aix5.1.ppc.rpm
db4                         ##################################################
[aix6:root]rpm -Uvh expat-2.1.0-1.aix5.1.ppc.rpm
expat                       ##################################################
[aix6:root]rpm -Uvh fontconfig-2.10.2-1.aix5.1.ppc.rpm
error: failed dependencies:
        freetype2 >= 2.3.12 is needed by fontconfig-2.10.2-1
        libfreetype.a(libfreetype.so.6) is needed by fontconfig-2.10.2-1
[aix6:root]rpm -Uvh freetype2-2.5.3-1.aix5.1.ppc.rpm
error: failed dependencies:
        libpng >= 1.2.46-1 is needed by freetype2-2.5.3-1
        zlib is needed by freetype2-2.5.3-1
        libpng12.a(libpng12.so.0) is needed by freetype2-2.5.3-1
[aix6:root]rpm -Uvh gdbm-1.11-1.aix5.1.ppc.rpm 
gdbm                        ##################################################
[aix6:root]rpm -Uvh gettext-0.10.40-8.aix5.2.ppc.rpm
package gettext-0.10.40-8 is already installed
[aix6:root]rpm -Uvh gmp-6.0.0a-1.aix5.1.ppc.rpm  
error: failed dependencies:
        libgcc >= 4.2.3-2 is needed by gmp-6.0.0a-1
        libstdc++ >= 4.2.3-2 is needed by gmp-6.0.0a-1
[aix6:root]rpm -Uvh info-5.1-2.aix5.1.ppc.rpm 
info                        ##################################################
Please check that /etc/info-dir does exist.
You might have to rename it from /etc/info-dir.rpmsave to /etc/info-dir.
[aix6:root]rpm -Uvh libXft-2.3.1-1.aix5.1.ppc.rpm 
error: failed dependencies:
        libXrender >= 0.9.5 is needed by libXft-2.3.1-1
        freetype2 >= 2.3.5 is needed by libXft-2.3.1-1
        fontconfig >= 2.5.0 is needed by libXft-2.3.1-1
        libXrender.a(libXrender.so.1) is needed by libXft-2.3.1-1
        libfontconfig.a(libfontconfig.so.1) is needed by libXft-2.3.1-1
        libfreetype.a(libfreetype.so.6) is needed by libXft-2.3.1-1
[aix6:root]rpm -Uvh libXrender-0.9.8-1.aix6.1.ppc.rpm
libXrender                  ##################################################
[aix6:root]rpm -Uvh libdbi-0.8.4-1.aix5.1.ppc.rpm
libdbi                      ##################################################
[aix6:root]rpm -Uvh libffi-3.2.1-1.aix5.1.ppc.rpm
error: failed dependencies:
        libgcc >= 4.2.3-2 is needed by libffi-3.2.1-1
[aix6:root]rpm -Uvh libiconv-1.14-2.aix5.1.ppc.rpm 
libiconv                    ##################################################
[aix6:root]rpm -Uvh libpng-1.6.16-1.aix5.1.ppc.rpm
error: failed dependencies:
        zlib is needed by libpng-1.6.16-1
[aix6:root]rpm -Uvh openssl-1.0.1l-1.aix5.1.ppc.rpm
warning: /var/ssl/openssl.cnf saved as /var/ssl/openssl.cnf.rpmorig
openssl                     ##################################################
[aix6:root]rpm -Uvh sqlite-3.8.7.1-1.aix5.1.ppc.rpm
sqlite                      ##################################################
[aix6:root]rpm -Uvh tcl-8.6.3-1.aix5.1.ppc.rpm
tcl                         ##################################################
[aix6:root]rpm -Uvh tk-8.6.3-1.aix5.1.ppc.rpm
error: failed dependencies:
        fontconfig >= 2.5.0 is needed by tk-8.6.3-1
        libXft >= 2.1.14 is needed by tk-8.6.3-1
        libXft.a(libXft.so.2) is needed by tk-8.6.3-1
        libfontconfig.a(libfontconfig.so.1) is needed by tk-8.6.3-1
[aix6:root]rpm -Uvh libgcc-4.8.2-1.aix6.1.ppc.rpm
libgcc                      ##################################################
[aix6:root]rpm -Uvh libstdc++-4.8.2-1.aix6.1.ppc.rpm
libstdc++                   ##################################################
[aix6:root]rpm -Uvh libgomp-4.8.2-1.aix6.1.ppc.rpm
error: failed dependencies:
        gcc = 4.8.2-1 is needed by libgomp-4.8.2-1
[aix6:root]rpm -Uvh  gcc-cpp-4.8.2-1.aix6.1.ppc.rpm
error: failed dependencies:
        gcc = 4.8.2-1 is needed by gcc-cpp-4.8.2-1
        gmp >= 4.3.2 is needed by gcc-cpp-4.8.2-1
        mpfr >= 2.4.2 is needed by gcc-cpp-4.8.2-1
        libmpc >= 0.8.1 is needed by gcc-cpp-4.8.2-1
        zlib >= 1.2.3-3 is needed by gcc-cpp-4.8.2-1
        libgmp.a(libgmp.so.3) is needed by gcc-cpp-4.8.2-1
        libmpc.a(libmpc.so.2) is needed by gcc-cpp-4.8.2-1
        libmpfr.a(libmpfr.so.1) is needed by gcc-cpp-4.8.2-1
[aix6:root]rpm -Uvh gmp-6.0.0a-1.aix5.1.ppc.rpm  
gmp                         ##################################################
[aix6:root]rpm -Uvh tk-8.6.3-1.aix5.1.ppc.rpm
error: failed dependencies:
        fontconfig >= 2.5.0 is needed by tk-8.6.3-1
        libXft >= 2.1.14 is needed by tk-8.6.3-1
        libXft.a(libXft.so.2) is needed by tk-8.6.3-1
        libfontconfig.a(libfontconfig.so.1) is needed by tk-8.6.3-1
[aix6:root]rpm -Uvh fontconfig-2.10.2-1.aix5.1.ppc.rpm
error: failed dependencies:
        freetype2 >= 2.3.12 is needed by fontconfig-2.10.2-1
        libfreetype.a(libfreetype.so.6) is needed by fontconfig-2.10.2-1
[aix6:root]rpm -Uvh freetype2-2.5.3-1.aix5.1.ppc.rpm
error: failed dependencies:
        libpng >= 1.2.46-1 is needed by freetype2-2.5.3-1
        zlib is needed by freetype2-2.5.3-1
        libpng12.a(libpng12.so.0) is needed by freetype2-2.5.3-1
[aix6:root]rpm -Uvh zlib-1.2.8-1.aix5.1.ppc.rpm
zlib                        ##################################################
[aix6:root]rpm -Uvh libpng-1.6.12-1.aix5.1.ppc.rpm 
libpng                      ##################################################
[aix6:root]rpm -Uvh fontconfig-2.10.2-1.aix5.1.ppc.rpm
error: failed dependencies:
        freetype2 >= 2.3.12 is needed by fontconfig-2.10.2-1
        libfreetype.a(libfreetype.so.6) is needed by fontconfig-2.10.2-1
[aix6:root]rpm -Uvh freetype2-2.5.3-1.aix5.1.ppc.rpm 
freetype2                   ##################################################
[aix6:root]rpm -Uvh fontconfig-2.10.2-1.aix5.1.ppc.rpm
fontconfig                  ##################################################
[aix6:root]rpm -Uvh tk-8.6.3-1.aix5.1.ppc.rpm
error: failed dependencies:
        libXft >= 2.1.14 is needed by tk-8.6.3-1
        libXft.a(libXft.so.2) is needed by tk-8.6.3-1
[aix6:root]rpm -Uvh libXft-2.3.1-1.aix5.1.ppc.rpm 
libXft                      ##################################################
[aix6:root]rpm -Uvh tk-8.6.3-1.aix5.1.ppc.rpm
tk                          ##################################################
[aix6:root]rpm -Uvh python-libs-2.7.5-1.aix6.1.ppc.rpm
python-libs                 ##################################################
[aix6:root]rpm -Uvh python-2.7.5-1.aix6.1.ppc.rpm
error: failed dependencies:
        libffi.a(libffi.so.6) is needed by python-2.7.5-1
[aix6:root]rpm -qa | grep libffi-4.2.0-3
libffi-4.2.0-3
[aix6:root]rpm -qa|grep libffi        
libffi-devel-4.2.0-3
libffi-4.2.0-3
[aix6:root]rpm -e libffi-devel-4.2.0-3
[aix6:root]rpm -e libffi-4.2.0-3
[aix6:root]rpm -qa|grep libffi  
[aix6:root]rpm -Uvh libffi-3.1-1.aix5.1.ppc.rpm 
libffi                      ##################################################
[aix6:root]rpm -Uvh python-2.7.5-1.aix6.1.ppc.rpm
python                      ##################################################
[aix6:root]python
Python 2.7.5 (default, Aug  2 2013, 23:28:11) [C] on aix6
Type "help", "copyright", "credits" or "license" for more information.
>>> exit()
[aix6:root]rpm -qa|grep -i python
python-libs-2.7.5-1
python-2.7.5-1
[aix6:root]tar -xvf setuptools-21.2.1.tar
x setuptools-21.2.1
x setuptools-21.2.1/docs
x setuptools-21.2.1/docs/_templates
x setuptools-21.2.1/docs/_templates/indexsidebar.html, 311 bytes, 1 media blocks.
x setuptools-21.2.1/docs/_theme
x setuptools-21.2.1/docs/_theme/nature
x setuptools-21.2.1/docs/_theme/nature/static
x setuptools-21.2.1/docs/_theme/nature/static/nature.css_t, 3853 bytes, 8 media blocks.
x setuptools-21.2.1/docs/_theme/nature/static/pygments.css, 2717 bytes, 6 media blocks.
x setuptools-21.2.1/docs/_theme/nature/theme.conf, 71 bytes, 1 media blocks.
x setuptools-21.2.1/docs/Makefile, 2339 bytes, 5 media blocks.
x setuptools-21.2.1/docs/conf.py, 9006 bytes, 18 media blocks.
x setuptools-21.2.1/docs/developer-guide.txt, 4312 bytes, 9 media blocks.
x setuptools-21.2.1/docs/development.txt, 1474 bytes, 3 media blocks.
x setuptools-21.2.1/docs/easy_install.txt, 75534 bytes, 148 media blocks.
x setuptools-21.2.1/docs/formats.txt, 31242 bytes, 62 media blocks.
x setuptools-21.2.1/docs/history.txt, 81 bytes, 1 media blocks.
x setuptools-21.2.1/docs/index.txt, 537 bytes, 2 media blocks.
x setuptools-21.2.1/docs/pkg_resources.txt, 94452 bytes, 185 media blocks.
x setuptools-21.2.1/docs/python3.txt, 3970 bytes, 8 media blocks.
x setuptools-21.2.1/docs/releases.txt, 2235 bytes, 5 media blocks.
x setuptools-21.2.1/docs/roadmap.txt, 167 bytes, 1 media blocks.
x setuptools-21.2.1/docs/setuptools.txt, 125717 bytes, 246 media blocks.
x setuptools-21.2.1/pkg_resources
x setuptools-21.2.1/pkg_resources/_vendor
x setuptools-21.2.1/pkg_resources/_vendor/packaging
x setuptools-21.2.1/pkg_resources/_vendor/packaging/__about__.py, 720 bytes, 2 media blocks.
x setuptools-21.2.1/pkg_resources/_vendor/packaging/__init__.py, 513 bytes, 2 media blocks.
x setuptools-21.2.1/pkg_resources/_vendor/packaging/_compat.py, 860 bytes, 2 media blocks.
x setuptools-21.2.1/pkg_resources/_vendor/packaging/_structures.py, 1416 bytes, 3 media blocks.
x setuptools-21.2.1/pkg_resources/_vendor/packaging/markers.py, 7939 bytes, 16 media blocks.
x setuptools-21.2.1/pkg_resources/_vendor/packaging/requirements.py, 4355 bytes, 9 media blocks.
x setuptools-21.2.1/pkg_resources/_vendor/packaging/specifiers.py, 28025 bytes, 55 media blocks.
x setuptools-21.2.1/pkg_resources/_vendor/packaging/utils.py, 421 bytes, 1 media blocks.
x setuptools-21.2.1/pkg_resources/_vendor/packaging/version.py, 11556 bytes, 23 media blocks.
x setuptools-21.2.1/pkg_resources/_vendor/__init__.py, 0 bytes, 0 media blocks.
x setuptools-21.2.1/pkg_resources/_vendor/pyparsing.py, 160425 bytes, 314 media blocks.
x setuptools-21.2.1/pkg_resources/_vendor/six.py, 30098 bytes, 59 media blocks.
x setuptools-21.2.1/pkg_resources/_vendor/vendored.txt, 45 bytes, 1 media blocks.
x setuptools-21.2.1/pkg_resources/extern
x setuptools-21.2.1/pkg_resources/extern/__init__.py, 2474 bytes, 5 media blocks.
x setuptools-21.2.1/pkg_resources/tests
x setuptools-21.2.1/pkg_resources/tests/__init__.py, 0 bytes, 0 media blocks.
x setuptools-21.2.1/pkg_resources/tests/test_markers.py, 288 bytes, 1 media blocks.
x setuptools-21.2.1/pkg_resources/tests/test_pkg_resources.py, 5227 bytes, 11 media blocks.
x setuptools-21.2.1/pkg_resources/tests/test_resources.py, 29961 bytes, 59 media blocks.
x setuptools-21.2.1/pkg_resources/__init__.py, 101358 bytes, 198 media blocks.
x setuptools-21.2.1/pkg_resources/api_tests.txt, 12211 bytes, 24 media blocks.
x setuptools-21.2.1/setuptools
x setuptools-21.2.1/setuptools/command
x setuptools-21.2.1/setuptools/command/__init__.py, 564 bytes, 2 media blocks.
x setuptools-21.2.1/setuptools/command/alias.py, 2426 bytes, 5 media blocks.
x setuptools-21.2.1/setuptools/command/bdist_egg.py, 17184 bytes, 34 media blocks.
x setuptools-21.2.1/setuptools/command/bdist_rpm.py, 1508 bytes, 3 media blocks.
x setuptools-21.2.1/setuptools/command/bdist_wininst.py, 637 bytes, 2 media blocks.
x setuptools-21.2.1/setuptools/command/build_ext.py, 12131 bytes, 24 media blocks.
x setuptools-21.2.1/setuptools/command/build_py.py, 9389 bytes, 19 media blocks.
x setuptools-21.2.1/setuptools/command/develop.py, 7383 bytes, 15 media blocks.
x setuptools-21.2.1/setuptools/command/easy_install.py, 86546 bytes, 170 media blocks.
x setuptools-21.2.1/setuptools/command/egg_info.py, 17291 bytes, 34 media blocks.
x setuptools-21.2.1/setuptools/command/install.py, 4683 bytes, 10 media blocks.
x setuptools-21.2.1/setuptools/command/install_egg_info.py, 4035 bytes, 8 media blocks.
x setuptools-21.2.1/setuptools/command/install_lib.py, 3839 bytes, 8 media blocks.
x setuptools-21.2.1/setuptools/command/install_scripts.py, 2231 bytes, 5 media blocks.
x setuptools-21.2.1/setuptools/command/launcher manifest.xml, 628 bytes, 2 media blocks.
x setuptools-21.2.1/setuptools/command/register.py, 270 bytes, 1 media blocks.
x setuptools-21.2.1/setuptools/command/rotate.py, 2164 bytes, 5 media blocks.
x setuptools-21.2.1/setuptools/command/saveopts.py, 658 bytes, 2 media blocks.
x setuptools-21.2.1/setuptools/command/sdist.py, 7050 bytes, 14 media blocks.
x setuptools-21.2.1/setuptools/command/setopt.py, 5086 bytes, 10 media blocks.
x setuptools-21.2.1/setuptools/command/test.py, 6888 bytes, 14 media blocks.
x setuptools-21.2.1/setuptools/command/upload.py, 1077 bytes, 3 media blocks.
x setuptools-21.2.1/setuptools/command/upload_docs.py, 6815 bytes, 14 media blocks.
x setuptools-21.2.1/setuptools/extern
x setuptools-21.2.1/setuptools/extern/__init__.py, 132 bytes, 1 media blocks.
x setuptools-21.2.1/setuptools/tests
x setuptools-21.2.1/setuptools/tests/indexes
x setuptools-21.2.1/setuptools/tests/indexes/test_links_priority
x setuptools-21.2.1/setuptools/tests/indexes/test_links_priority/simple
x setuptools-21.2.1/setuptools/tests/indexes/test_links_priority/simple/foobar
x setuptools-21.2.1/setuptools/tests/indexes/test_links_priority/simple/foobar/index.html, 174 bytes, 1 media blocks.
x setuptools-21.2.1/setuptools/tests/indexes/test_links_priority/external.html, 92 bytes, 1 media blocks.
x setuptools-21.2.1/setuptools/tests/__init__.py, 11346 bytes, 23 media blocks.
x setuptools-21.2.1/setuptools/tests/contexts.py, 2140 bytes, 5 media blocks.
x setuptools-21.2.1/setuptools/tests/environment.py, 1611 bytes, 4 media blocks.
x setuptools-21.2.1/setuptools/tests/files.py, 934 bytes, 2 media blocks.
x setuptools-21.2.1/setuptools/tests/fixtures.py, 661 bytes, 2 media blocks.
x setuptools-21.2.1/setuptools/tests/py26compat.py, 353 bytes, 1 media blocks.
x setuptools-21.2.1/setuptools/tests/script-with-bom.py, 46 bytes, 1 media blocks.
x setuptools-21.2.1/setuptools/tests/server.py, 2090 bytes, 5 media blocks.
x setuptools-21.2.1/setuptools/tests/test_bdist_egg.py, 1009 bytes, 2 media blocks.
x setuptools-21.2.1/setuptools/tests/test_build_ext.py, 570 bytes, 2 media blocks.
x setuptools-21.2.1/setuptools/tests/test_build_py.py, 669 bytes, 2 media blocks.
x setuptools-21.2.1/setuptools/tests/test_develop.py, 3204 bytes, 7 media blocks.
x setuptools-21.2.1/setuptools/tests/test_dist_info.py, 2366 bytes, 5 media blocks.
x setuptools-21.2.1/setuptools/tests/test_easy_install.py, 21603 bytes, 43 media blocks.
x setuptools-21.2.1/setuptools/tests/test_egg_info.py, 8283 bytes, 17 media blocks.
x setuptools-21.2.1/setuptools/tests/test_find_packages.py, 5930 bytes, 12 media blocks.
x setuptools-21.2.1/setuptools/tests/test_integration.py, 2996 bytes, 6 media blocks.
x setuptools-21.2.1/setuptools/tests/test_msvc9compiler.py, 5893 bytes, 12 media blocks.
x setuptools-21.2.1/setuptools/tests/test_packageindex.py, 7980 bytes, 16 media blocks.
x setuptools-21.2.1/setuptools/tests/test_sandbox.py, 4604 bytes, 9 media blocks.
x setuptools-21.2.1/setuptools/tests/test_sdist.py, 13463 bytes, 27 media blocks.
x setuptools-21.2.1/setuptools/tests/test_setuptools.py, 1160 bytes, 3 media blocks.
x setuptools-21.2.1/setuptools/tests/test_test.py, 2373 bytes, 5 media blocks.
x setuptools-21.2.1/setuptools/tests/test_unicode_utils.py, 316 bytes, 1 media blocks.
x setuptools-21.2.1/setuptools/tests/test_upload_docs.py, 1338 bytes, 3 media blocks.
x setuptools-21.2.1/setuptools/tests/test_windows_wrappers.py, 6154 bytes, 13 media blocks.
x setuptools-21.2.1/setuptools/tests/textwrap.py, 138 bytes, 1 media blocks.
x setuptools-21.2.1/setuptools/__init__.py, 5440 bytes, 11 media blocks.
x setuptools-21.2.1/setuptools/archive_util.py, 6609 bytes, 13 media blocks.
x setuptools-21.2.1/setuptools/cli-32.exe, 65536 bytes, 128 media blocks.
x setuptools-21.2.1/setuptools/cli-64.exe, 74752 bytes, 146 media blocks.
x setuptools-21.2.1/setuptools/cli-arm-32.exe, 69120 bytes, 135 media blocks.
x setuptools-21.2.1/setuptools/cli.exe, 65536 bytes, 128 media blocks.
x setuptools-21.2.1/setuptools/depends.py, 6418 bytes, 13 media blocks.
x setuptools-21.2.1/setuptools/dist.py, 35704 bytes, 70 media blocks.
x setuptools-21.2.1/setuptools/extension.py, 1694 bytes, 4 media blocks.
x setuptools-21.2.1/setuptools/gui-32.exe, 65536 bytes, 128 media blocks.
x setuptools-21.2.1/setuptools/gui-64.exe, 75264 bytes, 147 media blocks.
x setuptools-21.2.1/setuptools/gui-arm-32.exe, 69120 bytes, 135 media blocks.
x setuptools-21.2.1/setuptools/gui.exe, 65536 bytes, 128 media blocks.
x setuptools-21.2.1/setuptools/launch.py, 793 bytes, 2 media blocks.
x setuptools-21.2.1/setuptools/lib2to3_ex.py, 1998 bytes, 4 media blocks.
x setuptools-21.2.1/setuptools/msvc9_support.py, 2185 bytes, 5 media blocks.
x setuptools-21.2.1/setuptools/package_index.py, 39490 bytes, 78 media blocks.
x setuptools-21.2.1/setuptools/py26compat.py, 511 bytes, 1 media blocks.
x setuptools-21.2.1/setuptools/py27compat.py, 327 bytes, 1 media blocks.
x setuptools-21.2.1/setuptools/py31compat.py, 1636 bytes, 4 media blocks.
x setuptools-21.2.1/setuptools/sandbox.py, 14210 bytes, 28 media blocks.
x setuptools-21.2.1/setuptools/script (dev).tmpl, 201 bytes, 1 media blocks.
x setuptools-21.2.1/setuptools/script.tmpl, 138 bytes, 1 media blocks.
x setuptools-21.2.1/setuptools/site-patch.py, 2389 bytes, 5 media blocks.
x setuptools-21.2.1/setuptools/ssl_support.py, 8119 bytes, 16 media blocks.
x setuptools-21.2.1/setuptools/unicode_utils.py, 995 bytes, 2 media blocks.
x setuptools-21.2.1/setuptools/utils.py, 293 bytes, 1 media blocks.
x setuptools-21.2.1/setuptools/version.py, 138 bytes, 1 media blocks.
x setuptools-21.2.1/setuptools/windows_support.py, 714 bytes, 2 media blocks.
x setuptools-21.2.1/setuptools.egg-info
x setuptools-21.2.1/setuptools.egg-info/PKG-INFO, 12898 bytes, 26 media blocks.
x setuptools-21.2.1/setuptools.egg-info/SOURCES.txt, 4062 bytes, 8 media blocks.
x setuptools-21.2.1/setuptools.egg-info/dependency_links.txt, 225 bytes, 1 media blocks.
x setuptools-21.2.1/setuptools.egg-info/entry_points.txt, 2835 bytes, 6 media blocks.
x setuptools-21.2.1/setuptools.egg-info/requires.txt, 75 bytes, 1 media blocks.
x setuptools-21.2.1/setuptools.egg-info/top_level.txt, 38 bytes, 1 media blocks.
x setuptools-21.2.1/setuptools.egg-info/zip-safe, 1 bytes, 1 media blocks.
x setuptools-21.2.1/tests
x setuptools-21.2.1/tests/manual_test.py, 2367 bytes, 5 media blocks.
x setuptools-21.2.1/CHANGES.rst, 84332 bytes, 165 media blocks.
x setuptools-21.2.1/MANIFEST.in, 398 bytes, 1 media blocks.
x setuptools-21.2.1/README.rst, 9943 bytes, 20 media blocks.
x setuptools-21.2.1/bootstrap.py, 1593 bytes, 4 media blocks.
x setuptools-21.2.1/conftest.py, 45 bytes, 1 media blocks.
x setuptools-21.2.1/easy_install.py, 126 bytes, 1 media blocks.
x setuptools-21.2.1/launcher.c, 10317 bytes, 21 media blocks.
x setuptools-21.2.1/msvc-build-launcher.cmd, 2600 bytes, 6 media blocks.
x setuptools-21.2.1/pavement.py, 800 bytes, 2 media blocks.
x setuptools-21.2.1/pytest.ini, 326 bytes, 1 media blocks.
x setuptools-21.2.1/setup.py, 6679 bytes, 14 media blocks.
x setuptools-21.2.1/PKG-INFO, 12898 bytes, 26 media blocks.
x setuptools-21.2.1/setup.cfg, 509 bytes, 1 media blocks.
[aix6:root]tar -xvf PyMySQL-0.7.3.tar
x PyMySQL-0.7.3
x PyMySQL-0.7.3/CHANGELOG, 5166 bytes, 11 media blocks.
x PyMySQL-0.7.3/example.py, 320 bytes, 1 media blocks.
x PyMySQL-0.7.3/LICENSE, 1070 bytes, 3 media blocks.
x PyMySQL-0.7.3/MANIFEST.in, 84 bytes, 1 media blocks.
x PyMySQL-0.7.3/PKG-INFO, 859 bytes, 2 media blocks.
x PyMySQL-0.7.3/pymysql
x PyMySQL-0.7.3/pymysql/__init__.py, 4515 bytes, 9 media blocks.
x PyMySQL-0.7.3/pymysql/_compat.py, 481 bytes, 1 media blocks.
x PyMySQL-0.7.3/pymysql/_socketio.py, 4049 bytes, 8 media blocks.
x PyMySQL-0.7.3/pymysql/charset.py, 13376 bytes, 27 media blocks.
x PyMySQL-0.7.3/pymysql/connections.py, 54750 bytes, 107 media blocks.
x PyMySQL-0.7.3/pymysql/constants
x PyMySQL-0.7.3/pymysql/constants/__init__.py, 0 bytes, 0 media blocks.
x PyMySQL-0.7.3/pymysql/constants/CLIENT.py, 846 bytes, 2 media blocks.
x PyMySQL-0.7.3/pymysql/constants/COMMAND.py, 680 bytes, 2 media blocks.
x PyMySQL-0.7.3/pymysql/constants/CR.py, 2213 bytes, 5 media blocks.
x PyMySQL-0.7.3/pymysql/constants/ER.py, 12223 bytes, 24 media blocks.
x PyMySQL-0.7.3/pymysql/constants/FIELD_TYPE.py, 361 bytes, 1 media blocks.
x PyMySQL-0.7.3/pymysql/constants/FLAG.py, 214 bytes, 1 media blocks.
x PyMySQL-0.7.3/pymysql/constants/SERVER_STATUS.py, 334 bytes, 1 media blocks.
x PyMySQL-0.7.3/pymysql/converters.py, 12172 bytes, 24 media blocks.
x PyMySQL-0.7.3/pymysql/cursors.py, 16305 bytes, 32 media blocks.
x PyMySQL-0.7.3/pymysql/err.py, 4025 bytes, 8 media blocks.
x PyMySQL-0.7.3/pymysql/optionfile.py, 522 bytes, 2 media blocks.
x PyMySQL-0.7.3/pymysql/tests
x PyMySQL-0.7.3/pymysql/tests/__init__.py, 492 bytes, 1 media blocks.
x PyMySQL-0.7.3/pymysql/tests/base.py, 2704 bytes, 6 media blocks.
x PyMySQL-0.7.3/pymysql/tests/test_basic.py, 13258 bytes, 26 media blocks.
x PyMySQL-0.7.3/pymysql/tests/test_connection.py, 24275 bytes, 48 media blocks.
x PyMySQL-0.7.3/pymysql/tests/test_converters.py, 489 bytes, 1 media blocks.
x PyMySQL-0.7.3/pymysql/tests/test_cursor.py, 4305 bytes, 9 media blocks.
x PyMySQL-0.7.3/pymysql/tests/test_DictCursor.py, 4447 bytes, 9 media blocks.
x PyMySQL-0.7.3/pymysql/tests/test_example.py, 646 bytes, 2 media blocks.
x PyMySQL-0.7.3/pymysql/tests/test_issues.py, 19152 bytes, 38 media blocks.
x PyMySQL-0.7.3/pymysql/tests/test_load_local.py, 2540 bytes, 5 media blocks.
x PyMySQL-0.7.3/pymysql/tests/test_nextset.py, 1856 bytes, 4 media blocks.
x PyMySQL-0.7.3/pymysql/tests/test_optionfile.py, 720 bytes, 2 media blocks.
x PyMySQL-0.7.3/pymysql/tests/test_SSCursor.py, 3920 bytes, 8 media blocks.
x PyMySQL-0.7.3/pymysql/tests/thirdparty
x PyMySQL-0.7.3/pymysql/tests/thirdparty/__init__.py, 170 bytes, 1 media blocks.
x PyMySQL-0.7.3/pymysql/tests/thirdparty/test_MySQLdb
x PyMySQL-0.7.3/pymysql/tests/thirdparty/test_MySQLdb/__init__.py, 243 bytes, 1 media blocks.
x PyMySQL-0.7.3/pymysql/tests/thirdparty/test_MySQLdb/capabilities.py, 10191 bytes, 20 media blocks.
x PyMySQL-0.7.3/pymysql/tests/thirdparty/test_MySQLdb/dbapi20.py, 31445 bytes, 62 media blocks.
x PyMySQL-0.7.3/pymysql/tests/thirdparty/test_MySQLdb/test_MySQLdb_capabilities.py, 3248 bytes, 7 media blocks.
x PyMySQL-0.7.3/pymysql/tests/thirdparty/test_MySQLdb/test_MySQLdb_dbapi20.py, 7759 bytes, 16 media blocks.
x PyMySQL-0.7.3/pymysql/tests/thirdparty/test_MySQLdb/test_MySQLdb_nonstandard.py, 3193 bytes, 7 media blocks.
x PyMySQL-0.7.3/pymysql/times.py, 356 bytes, 1 media blocks.
x PyMySQL-0.7.3/pymysql/util.py, 330 bytes, 1 media blocks.
x PyMySQL-0.7.3/PyMySQL.egg-info
x PyMySQL-0.7.3/PyMySQL.egg-info/dependency_links.txt, 1 bytes, 1 media blocks.
x PyMySQL-0.7.3/PyMySQL.egg-info/pbr.json, 47 bytes, 1 media blocks.
x PyMySQL-0.7.3/PyMySQL.egg-info/PKG-INFO, 859 bytes, 2 media blocks.
x PyMySQL-0.7.3/PyMySQL.egg-info/SOURCES.txt, 1456 bytes, 3 media blocks.
x PyMySQL-0.7.3/PyMySQL.egg-info/top_level.txt, 8 bytes, 1 media blocks.
x PyMySQL-0.7.3/README.rst, 4358 bytes, 9 media blocks.
x PyMySQL-0.7.3/runtests.py, 704 bytes, 2 media blocks.
x PyMySQL-0.7.3/setup.cfg, 160 bytes, 1 media blocks.
x PyMySQL-0.7.3/setup.py, 1219 bytes, 3 media blocks.
x PyMySQL-0.7.3/tox.ini, 184 bytes, 1 media blocks.
[aix6:root]cd setuptools-21.2.1
[aix6:root]ls
CHANGES.rst              README.rst               docs                     msvc-build-launcher.cmd  pytest.ini               setuptools
MANIFEST.in              bootstrap.py             easy_install.py          pavement.py              setup.cfg                setuptools.egg-info
PKG-INFO                 conftest.py              launcher.c               pkg_resources            setup.py                 tests
[aix6:root]python setup.py install
running install
running bdist_egg
running egg_info
writing requirements to setuptools.egg-info/requires.txt
writing setuptools.egg-info/PKG-INFO
writing top-level names to setuptools.egg-info/top_level.txt
writing dependency_links to setuptools.egg-info/dependency_links.txt
writing entry points to setuptools.egg-info/entry_points.txt
reading manifest file 'setuptools.egg-info/SOURCES.txt'
reading manifest template 'MANIFEST.in'
warning: no files found matching '*' under directory 'setuptools/_vendor'
writing manifest file 'setuptools.egg-info/SOURCES.txt'
installing library code to build/bdist.aix-6.1/egg
running install_lib
running build_py
creating build
creating build/lib
copying easy_install.py -> build/lib
creating build/lib/pkg_resources
copying pkg_resources/__init__.py -> build/lib/pkg_resources
creating build/lib/setuptools
copying setuptools/__init__.py -> build/lib/setuptools
copying setuptools/archive_util.py -> build/lib/setuptools
copying setuptools/depends.py -> build/lib/setuptools
copying setuptools/dist.py -> build/lib/setuptools
copying setuptools/extension.py -> build/lib/setuptools
copying setuptools/launch.py -> build/lib/setuptools
copying setuptools/lib2to3_ex.py -> build/lib/setuptools
copying setuptools/msvc9_support.py -> build/lib/setuptools
copying setuptools/package_index.py -> build/lib/setuptools
copying setuptools/py26compat.py -> build/lib/setuptools
copying setuptools/py27compat.py -> build/lib/setuptools
copying setuptools/py31compat.py -> build/lib/setuptools
copying setuptools/sandbox.py -> build/lib/setuptools
copying setuptools/site-patch.py -> build/lib/setuptools
copying setuptools/ssl_support.py -> build/lib/setuptools
copying setuptools/unicode_utils.py -> build/lib/setuptools
copying setuptools/utils.py -> build/lib/setuptools
copying setuptools/version.py -> build/lib/setuptools
copying setuptools/windows_support.py -> build/lib/setuptools
creating build/lib/pkg_resources/_vendor
copying pkg_resources/_vendor/__init__.py -> build/lib/pkg_resources/_vendor
copying pkg_resources/_vendor/pyparsing.py -> build/lib/pkg_resources/_vendor
copying pkg_resources/_vendor/six.py -> build/lib/pkg_resources/_vendor
creating build/lib/pkg_resources/extern
copying pkg_resources/extern/__init__.py -> build/lib/pkg_resources/extern
creating build/lib/pkg_resources/_vendor/packaging
copying pkg_resources/_vendor/packaging/__about__.py -> build/lib/pkg_resources/_vendor/packaging
copying pkg_resources/_vendor/packaging/__init__.py -> build/lib/pkg_resources/_vendor/packaging
copying pkg_resources/_vendor/packaging/_compat.py -> build/lib/pkg_resources/_vendor/packaging
copying pkg_resources/_vendor/packaging/_structures.py -> build/lib/pkg_resources/_vendor/packaging
copying pkg_resources/_vendor/packaging/markers.py -> build/lib/pkg_resources/_vendor/packaging
copying pkg_resources/_vendor/packaging/requirements.py -> build/lib/pkg_resources/_vendor/packaging
copying pkg_resources/_vendor/packaging/specifiers.py -> build/lib/pkg_resources/_vendor/packaging
copying pkg_resources/_vendor/packaging/utils.py -> build/lib/pkg_resources/_vendor/packaging
copying pkg_resources/_vendor/packaging/version.py -> build/lib/pkg_resources/_vendor/packaging
creating build/lib/setuptools/command
copying setuptools/command/__init__.py -> build/lib/setuptools/command
copying setuptools/command/alias.py -> build/lib/setuptools/command
copying setuptools/command/bdist_egg.py -> build/lib/setuptools/command
copying setuptools/command/bdist_rpm.py -> build/lib/setuptools/command
copying setuptools/command/bdist_wininst.py -> build/lib/setuptools/command
copying setuptools/command/build_ext.py -> build/lib/setuptools/command
copying setuptools/command/build_py.py -> build/lib/setuptools/command
copying setuptools/command/develop.py -> build/lib/setuptools/command
copying setuptools/command/easy_install.py -> build/lib/setuptools/command
copying setuptools/command/egg_info.py -> build/lib/setuptools/command
copying setuptools/command/install.py -> build/lib/setuptools/command
copying setuptools/command/install_egg_info.py -> build/lib/setuptools/command
copying setuptools/command/install_lib.py -> build/lib/setuptools/command
copying setuptools/command/install_scripts.py -> build/lib/setuptools/command
copying setuptools/command/register.py -> build/lib/setuptools/command
copying setuptools/command/rotate.py -> build/lib/setuptools/command
copying setuptools/command/saveopts.py -> build/lib/setuptools/command
copying setuptools/command/sdist.py -> build/lib/setuptools/command
copying setuptools/command/setopt.py -> build/lib/setuptools/command
copying setuptools/command/test.py -> build/lib/setuptools/command
copying setuptools/command/upload.py -> build/lib/setuptools/command
copying setuptools/command/upload_docs.py -> build/lib/setuptools/command
creating build/lib/setuptools/extern
copying setuptools/extern/__init__.py -> build/lib/setuptools/extern
copying setuptools/script (dev).tmpl -> build/lib/setuptools
copying setuptools/script.tmpl -> build/lib/setuptools
creating build/bdist.aix-6.1
creating build/bdist.aix-6.1/egg
copying build/lib/easy_install.py -> build/bdist.aix-6.1/egg
creating build/bdist.aix-6.1/egg/pkg_resources
copying build/lib/pkg_resources/__init__.py -> build/bdist.aix-6.1/egg/pkg_resources
creating build/bdist.aix-6.1/egg/pkg_resources/_vendor
copying build/lib/pkg_resources/_vendor/__init__.py -> build/bdist.aix-6.1/egg/pkg_resources/_vendor
creating build/bdist.aix-6.1/egg/pkg_resources/_vendor/packaging
copying build/lib/pkg_resources/_vendor/packaging/__about__.py -> build/bdist.aix-6.1/egg/pkg_resources/_vendor/packaging
copying build/lib/pkg_resources/_vendor/packaging/__init__.py -> build/bdist.aix-6.1/egg/pkg_resources/_vendor/packaging
copying build/lib/pkg_resources/_vendor/packaging/_compat.py -> build/bdist.aix-6.1/egg/pkg_resources/_vendor/packaging
copying build/lib/pkg_resources/_vendor/packaging/_structures.py -> build/bdist.aix-6.1/egg/pkg_resources/_vendor/packaging
copying build/lib/pkg_resources/_vendor/packaging/markers.py -> build/bdist.aix-6.1/egg/pkg_resources/_vendor/packaging
copying build/lib/pkg_resources/_vendor/packaging/requirements.py -> build/bdist.aix-6.1/egg/pkg_resources/_vendor/packaging
copying build/lib/pkg_resources/_vendor/packaging/specifiers.py -> build/bdist.aix-6.1/egg/pkg_resources/_vendor/packaging
copying build/lib/pkg_resources/_vendor/packaging/utils.py -> build/bdist.aix-6.1/egg/pkg_resources/_vendor/packaging
copying build/lib/pkg_resources/_vendor/packaging/version.py -> build/bdist.aix-6.1/egg/pkg_resources/_vendor/packaging
copying build/lib/pkg_resources/_vendor/pyparsing.py -> build/bdist.aix-6.1/egg/pkg_resources/_vendor
copying build/lib/pkg_resources/_vendor/six.py -> build/bdist.aix-6.1/egg/pkg_resources/_vendor
creating build/bdist.aix-6.1/egg/pkg_resources/extern
copying build/lib/pkg_resources/extern/__init__.py -> build/bdist.aix-6.1/egg/pkg_resources/extern
creating build/bdist.aix-6.1/egg/setuptools
copying build/lib/setuptools/__init__.py -> build/bdist.aix-6.1/egg/setuptools
copying build/lib/setuptools/archive_util.py -> build/bdist.aix-6.1/egg/setuptools
creating build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/__init__.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/alias.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/bdist_egg.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/bdist_rpm.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/bdist_wininst.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/build_ext.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/build_py.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/develop.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/easy_install.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/egg_info.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/install.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/install_egg_info.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/install_lib.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/install_scripts.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/register.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/rotate.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/saveopts.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/sdist.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/setopt.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/test.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/upload.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/command/upload_docs.py -> build/bdist.aix-6.1/egg/setuptools/command
copying build/lib/setuptools/depends.py -> build/bdist.aix-6.1/egg/setuptools
copying build/lib/setuptools/dist.py -> build/bdist.aix-6.1/egg/setuptools
copying build/lib/setuptools/extension.py -> build/bdist.aix-6.1/egg/setuptools
creating build/bdist.aix-6.1/egg/setuptools/extern
copying build/lib/setuptools/extern/__init__.py -> build/bdist.aix-6.1/egg/setuptools/extern
copying build/lib/setuptools/launch.py -> build/bdist.aix-6.1/egg/setuptools
copying build/lib/setuptools/lib2to3_ex.py -> build/bdist.aix-6.1/egg/setuptools
copying build/lib/setuptools/msvc9_support.py -> build/bdist.aix-6.1/egg/setuptools
copying build/lib/setuptools/package_index.py -> build/bdist.aix-6.1/egg/setuptools
copying build/lib/setuptools/py26compat.py -> build/bdist.aix-6.1/egg/setuptools
copying build/lib/setuptools/py27compat.py -> build/bdist.aix-6.1/egg/setuptools
copying build/lib/setuptools/py31compat.py -> build/bdist.aix-6.1/egg/setuptools
copying build/lib/setuptools/sandbox.py -> build/bdist.aix-6.1/egg/setuptools
copying build/lib/setuptools/script (dev).tmpl -> build/bdist.aix-6.1/egg/setuptools
copying build/lib/setuptools/script.tmpl -> build/bdist.aix-6.1/egg/setuptools
copying build/lib/setuptools/site-patch.py -> build/bdist.aix-6.1/egg/setuptools
copying build/lib/setuptools/ssl_support.py -> build/bdist.aix-6.1/egg/setuptools
copying build/lib/setuptools/unicode_utils.py -> build/bdist.aix-6.1/egg/setuptools
copying build/lib/setuptools/utils.py -> build/bdist.aix-6.1/egg/setuptools
copying build/lib/setuptools/version.py -> build/bdist.aix-6.1/egg/setuptools
copying build/lib/setuptools/windows_support.py -> build/bdist.aix-6.1/egg/setuptools
byte-compiling build/bdist.aix-6.1/egg/easy_install.py to easy_install.pyc
byte-compiling build/bdist.aix-6.1/egg/pkg_resources/__init__.py to __init__.pyc
byte-compiling build/bdist.aix-6.1/egg/pkg_resources/_vendor/__init__.py to __init__.pyc
byte-compiling build/bdist.aix-6.1/egg/pkg_resources/_vendor/packaging/__about__.py to __about__.pyc
byte-compiling build/bdist.aix-6.1/egg/pkg_resources/_vendor/packaging/__init__.py to __init__.pyc
byte-compiling build/bdist.aix-6.1/egg/pkg_resources/_vendor/packaging/_compat.py to _compat.pyc
byte-compiling build/bdist.aix-6.1/egg/pkg_resources/_vendor/packaging/_structures.py to _structures.pyc
byte-compiling build/bdist.aix-6.1/egg/pkg_resources/_vendor/packaging/markers.py to markers.pyc
byte-compiling build/bdist.aix-6.1/egg/pkg_resources/_vendor/packaging/requirements.py to requirements.pyc
byte-compiling build/bdist.aix-6.1/egg/pkg_resources/_vendor/packaging/specifiers.py to specifiers.pyc
byte-compiling build/bdist.aix-6.1/egg/pkg_resources/_vendor/packaging/utils.py to utils.pyc
byte-compiling build/bdist.aix-6.1/egg/pkg_resources/_vendor/packaging/version.py to version.pyc
byte-compiling build/bdist.aix-6.1/egg/pkg_resources/_vendor/pyparsing.py to pyparsing.pyc
byte-compiling build/bdist.aix-6.1/egg/pkg_resources/_vendor/six.py to six.pyc
byte-compiling build/bdist.aix-6.1/egg/pkg_resources/extern/__init__.py to __init__.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/__init__.py to __init__.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/archive_util.py to archive_util.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/__init__.py to __init__.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/alias.py to alias.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/bdist_egg.py to bdist_egg.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/bdist_rpm.py to bdist_rpm.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/bdist_wininst.py to bdist_wininst.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/build_ext.py to build_ext.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/build_py.py to build_py.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/develop.py to develop.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/easy_install.py to easy_install.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/egg_info.py to egg_info.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/install.py to install.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/install_egg_info.py to install_egg_info.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/install_lib.py to install_lib.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/install_scripts.py to install_scripts.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/register.py to register.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/rotate.py to rotate.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/saveopts.py to saveopts.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/sdist.py to sdist.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/setopt.py to setopt.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/test.py to test.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/upload.py to upload.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/command/upload_docs.py to upload_docs.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/depends.py to depends.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/dist.py to dist.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/extension.py to extension.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/extern/__init__.py to __init__.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/launch.py to launch.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/lib2to3_ex.py to lib2to3_ex.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/msvc9_support.py to msvc9_support.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/package_index.py to package_index.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/py26compat.py to py26compat.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/py27compat.py to py27compat.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/py31compat.py to py31compat.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/sandbox.py to sandbox.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/site-patch.py to site-patch.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/ssl_support.py to ssl_support.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/unicode_utils.py to unicode_utils.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/utils.py to utils.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/version.py to version.pyc
byte-compiling build/bdist.aix-6.1/egg/setuptools/windows_support.py to windows_support.pyc
creating build/bdist.aix-6.1/egg/EGG-INFO
copying setuptools.egg-info/PKG-INFO -> build/bdist.aix-6.1/egg/EGG-INFO
copying setuptools.egg-info/SOURCES.txt -> build/bdist.aix-6.1/egg/EGG-INFO
copying setuptools.egg-info/dependency_links.txt -> build/bdist.aix-6.1/egg/EGG-INFO
copying setuptools.egg-info/entry_points.txt -> build/bdist.aix-6.1/egg/EGG-INFO
copying setuptools.egg-info/requires.txt -> build/bdist.aix-6.1/egg/EGG-INFO
copying setuptools.egg-info/top_level.txt -> build/bdist.aix-6.1/egg/EGG-INFO
copying setuptools.egg-info/zip-safe -> build/bdist.aix-6.1/egg/EGG-INFO
creating dist
creating 'dist/setuptools-21.2.1-py2.7.egg' and adding 'build/bdist.aix-6.1/egg' to it
removing 'build/bdist.aix-6.1/egg' (and everything under it)
Processing setuptools-21.2.1-py2.7.egg
Copying setuptools-21.2.1-py2.7.egg to /opt/freeware/lib/python2.7/site-packages
Adding setuptools 21.2.1 to easy-install.pth file
Installing easy_install script to /opt/freeware/bin
Installing easy_install-2.7 script to /opt/freeware/bin

Installed /opt/freeware/lib/python2.7/site-packages/setuptools-21.2.1-py2.7.egg
Processing dependencies for setuptools==21.2.1
Finished processing dependencies for setuptools==21.2.1
[aix6:root]cd ..
[aix6:root]cd PyMySQL-0.7.3
[aix6:root]ls
CHANGELOG         MANIFEST.in       PyMySQL.egg-info  example.py        runtests.py       setup.py
LICENSE           PKG-INFO          README.rst        pymysql           setup.cfg         tox.ini
[aix6:root]python setup.py install
running install
running bdist_egg
running egg_info
writing PyMySQL.egg-info/PKG-INFO
writing top-level names to PyMySQL.egg-info/top_level.txt
writing dependency_links to PyMySQL.egg-info/dependency_links.txt
reading manifest file 'PyMySQL.egg-info/SOURCES.txt'
reading manifest template 'MANIFEST.in'
writing manifest file 'PyMySQL.egg-info/SOURCES.txt'
installing library code to build/bdist.aix-6.1/egg
running install_lib
running build_py
creating build
creating build/lib
creating build/lib/pymysql
copying pymysql/__init__.py -> build/lib/pymysql
copying pymysql/_compat.py -> build/lib/pymysql
copying pymysql/_socketio.py -> build/lib/pymysql
copying pymysql/charset.py -> build/lib/pymysql
copying pymysql/connections.py -> build/lib/pymysql
copying pymysql/converters.py -> build/lib/pymysql
copying pymysql/cursors.py -> build/lib/pymysql
copying pymysql/err.py -> build/lib/pymysql
copying pymysql/optionfile.py -> build/lib/pymysql
copying pymysql/times.py -> build/lib/pymysql
copying pymysql/util.py -> build/lib/pymysql
creating build/lib/pymysql/constants
copying pymysql/constants/CLIENT.py -> build/lib/pymysql/constants
copying pymysql/constants/COMMAND.py -> build/lib/pymysql/constants
copying pymysql/constants/CR.py -> build/lib/pymysql/constants
copying pymysql/constants/ER.py -> build/lib/pymysql/constants
copying pymysql/constants/FIELD_TYPE.py -> build/lib/pymysql/constants
copying pymysql/constants/FLAG.py -> build/lib/pymysql/constants
copying pymysql/constants/SERVER_STATUS.py -> build/lib/pymysql/constants
copying pymysql/constants/__init__.py -> build/lib/pymysql/constants
creating build/lib/pymysql/tests
copying pymysql/tests/__init__.py -> build/lib/pymysql/tests
copying pymysql/tests/base.py -> build/lib/pymysql/tests
copying pymysql/tests/test_DictCursor.py -> build/lib/pymysql/tests
copying pymysql/tests/test_SSCursor.py -> build/lib/pymysql/tests
copying pymysql/tests/test_basic.py -> build/lib/pymysql/tests
copying pymysql/tests/test_connection.py -> build/lib/pymysql/tests
copying pymysql/tests/test_converters.py -> build/lib/pymysql/tests
copying pymysql/tests/test_cursor.py -> build/lib/pymysql/tests
copying pymysql/tests/test_example.py -> build/lib/pymysql/tests
copying pymysql/tests/test_issues.py -> build/lib/pymysql/tests
copying pymysql/tests/test_load_local.py -> build/lib/pymysql/tests
copying pymysql/tests/test_nextset.py -> build/lib/pymysql/tests
copying pymysql/tests/test_optionfile.py -> build/lib/pymysql/tests
creating build/lib/pymysql/tests/thirdparty
copying pymysql/tests/thirdparty/__init__.py -> build/lib/pymysql/tests/thirdparty
creating build/lib/pymysql/tests/thirdparty/test_MySQLdb
copying pymysql/tests/thirdparty/test_MySQLdb/__init__.py -> build/lib/pymysql/tests/thirdparty/test_MySQLdb
copying pymysql/tests/thirdparty/test_MySQLdb/capabilities.py -> build/lib/pymysql/tests/thirdparty/test_MySQLdb
copying pymysql/tests/thirdparty/test_MySQLdb/dbapi20.py -> build/lib/pymysql/tests/thirdparty/test_MySQLdb
copying pymysql/tests/thirdparty/test_MySQLdb/test_MySQLdb_capabilities.py -> build/lib/pymysql/tests/thirdparty/test_MySQLdb
copying pymysql/tests/thirdparty/test_MySQLdb/test_MySQLdb_dbapi20.py -> build/lib/pymysql/tests/thirdparty/test_MySQLdb
copying pymysql/tests/thirdparty/test_MySQLdb/test_MySQLdb_nonstandard.py -> build/lib/pymysql/tests/thirdparty/test_MySQLdb
creating build/bdist.aix-6.1
creating build/bdist.aix-6.1/egg
creating build/bdist.aix-6.1/egg/pymysql
copying build/lib/pymysql/__init__.py -> build/bdist.aix-6.1/egg/pymysql
copying build/lib/pymysql/_compat.py -> build/bdist.aix-6.1/egg/pymysql
copying build/lib/pymysql/_socketio.py -> build/bdist.aix-6.1/egg/pymysql
copying build/lib/pymysql/charset.py -> build/bdist.aix-6.1/egg/pymysql
copying build/lib/pymysql/connections.py -> build/bdist.aix-6.1/egg/pymysql
creating build/bdist.aix-6.1/egg/pymysql/constants
copying build/lib/pymysql/constants/CLIENT.py -> build/bdist.aix-6.1/egg/pymysql/constants
copying build/lib/pymysql/constants/COMMAND.py -> build/bdist.aix-6.1/egg/pymysql/constants
copying build/lib/pymysql/constants/CR.py -> build/bdist.aix-6.1/egg/pymysql/constants
copying build/lib/pymysql/constants/ER.py -> build/bdist.aix-6.1/egg/pymysql/constants
copying build/lib/pymysql/constants/FIELD_TYPE.py -> build/bdist.aix-6.1/egg/pymysql/constants
copying build/lib/pymysql/constants/FLAG.py -> build/bdist.aix-6.1/egg/pymysql/constants
copying build/lib/pymysql/constants/SERVER_STATUS.py -> build/bdist.aix-6.1/egg/pymysql/constants
copying build/lib/pymysql/constants/__init__.py -> build/bdist.aix-6.1/egg/pymysql/constants
copying build/lib/pymysql/converters.py -> build/bdist.aix-6.1/egg/pymysql
copying build/lib/pymysql/cursors.py -> build/bdist.aix-6.1/egg/pymysql
copying build/lib/pymysql/err.py -> build/bdist.aix-6.1/egg/pymysql
copying build/lib/pymysql/optionfile.py -> build/bdist.aix-6.1/egg/pymysql
creating build/bdist.aix-6.1/egg/pymysql/tests
copying build/lib/pymysql/tests/__init__.py -> build/bdist.aix-6.1/egg/pymysql/tests
copying build/lib/pymysql/tests/base.py -> build/bdist.aix-6.1/egg/pymysql/tests
copying build/lib/pymysql/tests/test_DictCursor.py -> build/bdist.aix-6.1/egg/pymysql/tests
copying build/lib/pymysql/tests/test_SSCursor.py -> build/bdist.aix-6.1/egg/pymysql/tests
copying build/lib/pymysql/tests/test_basic.py -> build/bdist.aix-6.1/egg/pymysql/tests
copying build/lib/pymysql/tests/test_connection.py -> build/bdist.aix-6.1/egg/pymysql/tests
copying build/lib/pymysql/tests/test_converters.py -> build/bdist.aix-6.1/egg/pymysql/tests
copying build/lib/pymysql/tests/test_cursor.py -> build/bdist.aix-6.1/egg/pymysql/tests
copying build/lib/pymysql/tests/test_example.py -> build/bdist.aix-6.1/egg/pymysql/tests
copying build/lib/pymysql/tests/test_issues.py -> build/bdist.aix-6.1/egg/pymysql/tests
copying build/lib/pymysql/tests/test_load_local.py -> build/bdist.aix-6.1/egg/pymysql/tests
copying build/lib/pymysql/tests/test_nextset.py -> build/bdist.aix-6.1/egg/pymysql/tests
copying build/lib/pymysql/tests/test_optionfile.py -> build/bdist.aix-6.1/egg/pymysql/tests
creating build/bdist.aix-6.1/egg/pymysql/tests/thirdparty
copying build/lib/pymysql/tests/thirdparty/__init__.py -> build/bdist.aix-6.1/egg/pymysql/tests/thirdparty
creating build/bdist.aix-6.1/egg/pymysql/tests/thirdparty/test_MySQLdb
copying build/lib/pymysql/tests/thirdparty/test_MySQLdb/__init__.py -> build/bdist.aix-6.1/egg/pymysql/tests/thirdparty/test_MySQLdb
copying build/lib/pymysql/tests/thirdparty/test_MySQLdb/capabilities.py -> build/bdist.aix-6.1/egg/pymysql/tests/thirdparty/test_MySQLdb
copying build/lib/pymysql/tests/thirdparty/test_MySQLdb/dbapi20.py -> build/bdist.aix-6.1/egg/pymysql/tests/thirdparty/test_MySQLdb
copying build/lib/pymysql/tests/thirdparty/test_MySQLdb/test_MySQLdb_capabilities.py -> build/bdist.aix-6.1/egg/pymysql/tests/thirdparty/test_MySQLdb
copying build/lib/pymysql/tests/thirdparty/test_MySQLdb/test_MySQLdb_dbapi20.py -> build/bdist.aix-6.1/egg/pymysql/tests/thirdparty/test_MySQLdb
copying build/lib/pymysql/tests/thirdparty/test_MySQLdb/test_MySQLdb_nonstandard.py -> build/bdist.aix-6.1/egg/pymysql/tests/thirdparty/test_MySQLdb
copying build/lib/pymysql/times.py -> build/bdist.aix-6.1/egg/pymysql
copying build/lib/pymysql/util.py -> build/bdist.aix-6.1/egg/pymysql
byte-compiling build/bdist.aix-6.1/egg/pymysql/__init__.py to __init__.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/_compat.py to _compat.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/_socketio.py to _socketio.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/charset.py to charset.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/connections.py to connections.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/constants/CLIENT.py to CLIENT.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/constants/COMMAND.py to COMMAND.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/constants/CR.py to CR.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/constants/ER.py to ER.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/constants/FIELD_TYPE.py to FIELD_TYPE.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/constants/FLAG.py to FLAG.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/constants/SERVER_STATUS.py to SERVER_STATUS.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/constants/__init__.py to __init__.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/converters.py to converters.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/cursors.py to cursors.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/err.py to err.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/optionfile.py to optionfile.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/tests/__init__.py to __init__.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/tests/base.py to base.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/tests/test_DictCursor.py to test_DictCursor.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/tests/test_SSCursor.py to test_SSCursor.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/tests/test_basic.py to test_basic.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/tests/test_connection.py to test_connection.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/tests/test_converters.py to test_converters.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/tests/test_cursor.py to test_cursor.pyc
  File "build/bdist.aix-6.1/egg/pymysql/tests/test_cursor.py", line 111
    cursor.executemany(q, [(3, 4), (5, 6)])
         ^
SyntaxError: invalid syntax

byte-compiling build/bdist.aix-6.1/egg/pymysql/tests/test_example.py to test_example.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/tests/test_issues.py to test_issues.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/tests/test_load_local.py to test_load_local.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/tests/test_nextset.py to test_nextset.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/tests/test_optionfile.py to test_optionfile.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/tests/thirdparty/__init__.py to __init__.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/tests/thirdparty/test_MySQLdb/__init__.py to __init__.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/tests/thirdparty/test_MySQLdb/capabilities.py to capabilities.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/tests/thirdparty/test_MySQLdb/dbapi20.py to dbapi20.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/tests/thirdparty/test_MySQLdb/test_MySQLdb_capabilities.py to test_MySQLdb_capabilities.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/tests/thirdparty/test_MySQLdb/test_MySQLdb_dbapi20.py to test_MySQLdb_dbapi20.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/tests/thirdparty/test_MySQLdb/test_MySQLdb_nonstandard.py to test_MySQLdb_nonstandard.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/times.py to times.pyc
byte-compiling build/bdist.aix-6.1/egg/pymysql/util.py to util.pyc
creating build/bdist.aix-6.1/egg/EGG-INFO
copying PyMySQL.egg-info/PKG-INFO -> build/bdist.aix-6.1/egg/EGG-INFO
copying PyMySQL.egg-info/SOURCES.txt -> build/bdist.aix-6.1/egg/EGG-INFO
copying PyMySQL.egg-info/dependency_links.txt -> build/bdist.aix-6.1/egg/EGG-INFO
copying PyMySQL.egg-info/pbr.json -> build/bdist.aix-6.1/egg/EGG-INFO
copying PyMySQL.egg-info/top_level.txt -> build/bdist.aix-6.1/egg/EGG-INFO
zip_safe flag not set; analyzing archive contents...
pymysql.tests.base: module references __file__
pymysql.tests.test_load_local: module references __file__
creating dist
creating 'dist/PyMySQL-0.7.3-py2.7.egg' and adding 'build/bdist.aix-6.1/egg' to it
removing 'build/bdist.aix-6.1/egg' (and everything under it)
Processing PyMySQL-0.7.3-py2.7.egg
creating /opt/freeware/lib/python2.7/site-packages/PyMySQL-0.7.3-py2.7.egg
Extracting PyMySQL-0.7.3-py2.7.egg to /opt/freeware/lib/python2.7/site-packages
  File "/opt/freeware/lib/python2.7/site-packages/PyMySQL-0.7.3-py2.7.egg/pymysql/tests/test_cursor.py", line 111
    cursor.executemany(q, [(3, 4), (5, 6)])
         ^
SyntaxError: invalid syntax

Adding PyMySQL 0.7.3 to easy-install.pth file

Installed /opt/freeware/lib/python2.7/site-packages/PyMySQL-0.7.3-py2.7.egg
Processing dependencies for PyMySQL==0.7.3
Finished processing dependencies for PyMySQL==0.7.3
[aix6:root]python
Python 2.7.5 (default, Aug  2 2013, 23:28:11) [C] on aix6
Type "help", "copyright", "credits" or "license" for more information.
>>> import pymysql
>>> dir(pymysql)
['BINARY', 'Binary', 'Connect', 'Connection', 'DATE', 'DATETIME', 'DBAPISet', 'DataError', 'DatabaseError', 'Date', 'DateFromTicks', 'Error', 'FIELD_TYPE', 'IntegrityError', 'InterfaceError', 'InternalError', 'MySQLError', 'NULL', 'NUMBER', 'NotSupportedError', 'OperationalError', 'PY2', 'ProgrammingError', 'ROWID', 'STRING', 'TIME', 'TIMESTAMP', 'Time', 'TimeFromTicks', 'Timestamp', 'TimestampFromTicks', 'VERSION', 'Warning', '__all__', '__builtins__', '__doc__', '__file__', '__name__', '__package__', '__path__', '__version__', '_compat', '_socketio', 'apilevel', 'charset', 'connect', 'connections', 'constants', 'converters', 'cursors', 'err', 'escape_dict', 'escape_sequence', 'escape_string', 'get_client_info', 'install_as_MySQLdb', 'optionfile', 'paramstyle', 'sys', 'thread_safe', 'threadsafety', 'times', 'util', 'version_info']
>>> 
>>> quit()
```
