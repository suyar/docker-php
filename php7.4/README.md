`configure' configures PHP 7.4.13 to adapt to many kinds of systems.

Usage: ./configure [OPTION]... [VAR=VALUE]...

To assign environment variables (e.g., CC, CFLAGS...), specify them as
VAR=VALUE.  See below for descriptions of some of the useful variables.

Defaults for the options are specified in brackets.

Configuration:
-h, --help              display this help and exit
--help=short        display options specific to this package
--help=recursive    display the short help of all the included packages
-V, --version           display version information and exit
-q, --quiet, --silent   do not print `checking ...' messages
--cache-file=FILE   cache test results in FILE [disabled]
-C, --config-cache      alias for `--cache-file=config.cache'
-n, --no-create         do not create output files
--srcdir=DIR        find the sources in DIR [configure dir or `..']

Installation directories:
--prefix=PREFIX         install architecture-independent files in PREFIX
[/usr/local]
--exec-prefix=EPREFIX   install architecture-dependent files in EPREFIX
[PREFIX]

By default, `make install' will install all the files in
`/usr/local/bin', `/usr/local/lib' etc.  You can specify
an installation prefix other than `/usr/local' using `--prefix',
for instance `--prefix=$HOME'.

For better control, use the options below.

Fine tuning of the installation directories:
--bindir=DIR            user executables [EPREFIX/bin]
--sbindir=DIR           system admin executables [EPREFIX/sbin]
--libexecdir=DIR        program executables [EPREFIX/libexec]
--sysconfdir=DIR        read-only single-machine data [PREFIX/etc]
--sharedstatedir=DIR    modifiable architecture-independent data [PREFIX/com]
--localstatedir=DIR     modifiable single-machine data [PREFIX/var]
--libdir=DIR            object code libraries [EPREFIX/lib]
--includedir=DIR        C header files [PREFIX/include]
--oldincludedir=DIR     C header files for non-gcc [/usr/include]
--datarootdir=DIR       read-only arch.-independent data root [PREFIX/share]
--datadir=DIR           read-only architecture-independent data [DATAROOTDIR]
--infodir=DIR           info documentation [DATAROOTDIR/info]
--localedir=DIR         locale-dependent data [DATAROOTDIR/locale]
--mandir=DIR            man documentation [DATAROOTDIR/man]
--docdir=DIR            documentation root [DATAROOTDIR/doc/php]
--htmldir=DIR           html documentation [DOCDIR]
--dvidir=DIR            dvi documentation [DOCDIR]
--pdfdir=DIR            pdf documentation [DOCDIR]
--psdir=DIR             ps documentation [DOCDIR]

Program names:
--program-prefix=PREFIX            prepend PREFIX to installed program names
--program-suffix=SUFFIX            append SUFFIX to installed program names
--program-transform-name=PROGRAM   run sed PROGRAM on installed program names

System types:
--build=BUILD     configure for building on BUILD [guessed]
--host=HOST       cross-compile to build programs to run on HOST [BUILD]
--target=TARGET   configure for building compilers for TARGET [HOST]

Optional Features and Packages:
--disable-option-checking  ignore unrecognized --enable/--with options
--disable-FEATURE       do not include FEATURE (same as --enable-FEATURE=no)
--enable-FEATURE[=ARG]  include FEATURE [ARG=yes]
--with-PACKAGE[=ARG]    use PACKAGE [ARG=yes]
--without-PACKAGE       do not use PACKAGE (same as --with-PACKAGE=no)
--with-libdir=NAME      Look for libraries in .../NAME rather than .../lib
--disable-rpath         Disable passing additional runtime library search
paths
--enable-re2c-cgoto     Enable -g flag to re2c to use computed goto gcc
extension
--disable-gcc-global-regs
whether to enable GCC global register variables

SAPI modules:

--with-apxs2[=FILE]     Build shared Apache 2 handler module. FILE is the
optional pathname to the Apache apxs tool [apxs]
--disable-cli           Disable building CLI version of PHP (this forces
--without-pear)
--enable-embed[=TYPE]   EXPERIMENTAL: Enable building of embedded SAPI
library TYPE is either 'shared' or 'static'.
[TYPE=shared]
--enable-fpm            Enable building of the fpm SAPI executable
--with-fpm-user[=USER]  Set the user for php-fpm to run as. (default:
nobody)
--with-fpm-group[=GRP]  Set the group for php-fpm to run as. For a system
user, this should usually be set to match the fpm
username (default: nobody)
--with-fpm-systemd      Activate systemd integration
--with-fpm-acl          Use POSIX Access Control Lists
--enable-litespeed      Build PHP as litespeed module
--enable-phpdbg         Build phpdbg
--enable-phpdbg-webhelper
Build phpdbg web SAPI support
--enable-phpdbg-debug   Build phpdbg in debug mode
--enable-phpdbg-readline
Enable readline support in phpdbg (depends on static
ext/readline)
--disable-cgi           Disable building CGI version of PHP
--with-valgrind         Enable valgrind support

General settings:

--enable-gcov           Enable GCOV code coverage - FOR DEVELOPERS ONLY!!
--enable-debug          Compile with debugging symbols
--enable-rtld-now       Use dlopen with RTLD_NOW instead of RTLD_LAZY
--with-layout=TYPE      Set how installed files will be laid out. Type can
be either PHP or GNU [PHP]
--with-config-file-path=PATH
Set the path in which to look for php.ini
[PREFIX/lib]
--with-config-file-scan-dir=PATH
Set the path where to scan for configuration files
--enable-sigchild       Enable PHP's own SIGCHLD handler
--enable-libgcc         Enable explicitly linking against libgcc
--disable-short-tags    Disable the short-form <? start tag by default
--enable-dmalloc        Enable dmalloc
--disable-ipv6          Disable IPv6 support
--enable-dtrace         Enable DTrace support
--enable-fd-setsize     Set size of descriptor sets
--enable-werror         Enable -Werror

Extensions:

--with-EXTENSION=shared[,PATH]

    NOTE: Not all extensions can be build as 'shared'.

    Example: --with-foobar=shared,/usr/local/foobar/

      o Builds the foobar extension as shared extension.
      o foobar package install prefix is /usr/local/foobar/


--disable-all           Disable all extensions which are enabled by default
--without-libxml        Build without LIBXML support
--with-openssl          Include OpenSSL support (requires OpenSSL >= 1.0.1)
--with-kerberos         OPENSSL: Include Kerberos support
--with-system-ciphers   OPENSSL: Use system default cipher list instead of
hardcoded value
--with-external-pcre    Use external library for PCRE support
--with-pcre-jit         Enable PCRE JIT functionality
--without-sqlite3       Do not include SQLite3 support.
--with-zlib             Include ZLIB support (requires zlib >= 1.2.0.4)
--enable-bcmath         Enable bc style precision math functions
--with-bz2[=DIR]        Include BZip2 support
--enable-calendar       Enable support for calendar conversion
--disable-ctype         Disable ctype functions
--with-curl             Include cURL support
--enable-dba            Build DBA with bundled modules. To build shared DBA
extension use --enable-dba=shared
--with-qdbm[=DIR]       DBA: QDBM support
--with-gdbm[=DIR]       DBA: GDBM support
--with-ndbm[=DIR]       DBA: NDBM support
--with-db4[=DIR]        DBA: Oracle Berkeley DB 4.x or 5.x support
--with-db3[=DIR]        DBA: Oracle Berkeley DB 3.x support
--with-db2[=DIR]        DBA: Oracle Berkeley DB 2.x support
--with-db1[=DIR]        DBA: Oracle Berkeley DB 1.x support/emulation
--with-dbm[=DIR]        DBA: DBM support
--with-tcadb[=DIR]      DBA: Tokyo Cabinet abstract DB support
--with-lmdb[=DIR]       DBA: Lightning memory-mapped database support
--without-cdb[=DIR]     DBA: CDB support (bundled)
--disable-inifile       DBA: INI support (bundled)
--disable-flatfile      DBA: FlatFile support (bundled)
--disable-dom           Disable DOM support
--with-enchant          Include Enchant support
--enable-exif           Enable EXIF (metadata from images) support
--with-ffi              Include FFI support
--disable-fileinfo      Disable fileinfo support
--disable-filter        Disable input filter support
--enable-ftp            Enable FTP support
--with-openssl-dir      FTP: Whether to enable FTP SSL support without
ext/openssl
--enable-gd             Include GD support
--with-external-gd      Use external libgd
--with-webp             GD: Enable WEBP support (only for bundled libgd)
--with-jpeg             GD: Enable JPEG support (only for bundled libgd)
--with-xpm              GD: Enable XPM support (only for bundled libgd)
--with-freetype         GD: Enable FreeType 2 support (only for bundled
libgd)
--enable-gd-jis-conv    GD: Enable JIS-mapped Japanese font support (only
for bundled libgd)
--with-gettext[=DIR]    Include GNU gettext support
--with-gmp[=DIR]        Include GNU MP support
--with-mhash            Include mhash support
--without-iconv[=DIR]   Exclude iconv support
--with-imap[=DIR]       Include IMAP support. DIR is the c-client install
prefix
--with-kerberos         IMAP: Include Kerberos support
--with-imap-ssl         IMAP: Include SSL support
--enable-intl           Enable internationalization support
--disable-json          Disable JavaScript Object Serialization support
--with-ldap[=DIR]       Include LDAP support
--with-ldap-sasl        LDAP: Build with Cyrus SASL support
--enable-mbstring       Enable multibyte string support
--disable-mbregex       MBSTRING: Disable multibyte regex support
--with-mysqli[=FILE]    Include MySQLi support. FILE is the path to
mysql_config. If no value or mysqlnd is passed as
FILE, the MySQL native driver will be used
--with-mysql-sock[=SOCKPATH]
MySQLi/PDO_MYSQL: Location of the MySQL unix socket
pointer. If unspecified, the default locations are
searched
--with-oci8[=DIR]       Include Oracle Database OCI8 support. DIR defaults
to $ORACLE_HOME. Use
--with-oci8=instantclient,/path/to/instant/client/lib
to use an Oracle Instant Client installation
--with-odbcver[=HEX]    Force support for the passed ODBC version. A hex
number is expected, default 0x0350. Use the special
value of 0 to prevent an explicit ODBCVER to be
defined.
--with-adabas[=DIR]     Include Adabas D support [/usr/local]
--with-sapdb[=DIR]      Include SAP DB support [/usr/local]
--with-solid[=DIR]      Include Solid support [/usr/local/solid]
--with-ibm-db2[=DIR]    Include IBM DB2 support [/home/db2inst1/sqllib]
--with-empress[=DIR]    Include Empress support $EMPRESSPATH (Empress
Version >= 8.60 required)
--with-empress-bcs[=DIR]
Include Empress Local Access support $EMPRESSPATH
(Empress Version >= 8.60 required)
--with-custom-odbc[=DIR]
Include user defined ODBC support. DIR is ODBC
install base directory [/usr/local]. Make sure to
define CUSTOM_ODBC_LIBS and have some odbc.h in your
include dirs. For example, you should define
following for Sybase SQL Anywhere 5.5.00 on QNX,
prior to running this configure script:
CPPFLAGS="-DODBC_QNX -DSQLANY_BUG" LDFLAGS=-lunix
CUSTOM_ODBC_LIBS="-ldblib -lodbc"
--with-iodbc            Include iODBC support
--with-esoob[=DIR]      Include Easysoft OOB support
[/usr/local/easysoft/oob/client]
--with-unixODBC         Include unixODBC support
--with-dbmaker[=DIR]    Include DBMaker support
--disable-opcache       Disable Zend OPcache support
--disable-huge-code-pages
Disable copying PHP CODE pages into HUGE PAGES
--enable-pcntl          Enable pcntl support (CLI/CGI only)
--disable-pdo           Disable PHP Data Objects support
--with-pdo-dblib[=DIR]  PDO: DBLIB-DB support. DIR is the FreeTDS home
directory
--with-pdo-firebird[=DIR]
PDO: Firebird support. DIR is the Firebird base
install directory [/opt/firebird]
--with-pdo-mysql[=DIR]  PDO: MySQL support. DIR is the MySQL base directory.
If no value or mysqlnd is passed as DIR, the MySQL
native driver will be used
--with-zlib-dir[=DIR]   PDO_MySQL: Set the path to libz install prefix
--with-pdo-oci[=DIR]    PDO: Oracle OCI support. DIR defaults to
$ORACLE_HOME. Use
--with-pdo-oci=instantclient,/path/to/instant/client/lib
for an Oracle Instant Client installation.
--with-pdo-odbc=flavour,dir
PDO: Support for 'flavour' ODBC driver. The include
and lib dirs are looked for under 'dir'. The
'flavour' can be one of: ibm-db2, iODBC, unixODBC,
generic. If ',dir' part is omitted, default for the
flavour you have selected will be used. e.g.:
--with-pdo-odbc=unixODBC will check for unixODBC
under /usr/local. You may attempt to use an
otherwise unsupported driver using the 'generic'
flavour. The syntax for generic ODBC support is:
--with-pdo-odbc=generic,dir,libname,ldflags,cflags.
When built as 'shared' the extension filename is
always pdo_odbc.so
--with-pdo-pgsql[=DIR]  PDO: PostgreSQL support. DIR is the PostgreSQL base
install directory or the path to pg_config
--without-pdo-sqlite    PDO: sqlite 3 support.
--with-pgsql[=DIR]      Include PostgreSQL support. DIR is the PostgreSQL
base install directory or the path to pg_config
--disable-phar          Disable phar support
--disable-posix         Disable POSIX-like functions
--with-pspell[=DIR]     Include PSPELL support. GNU Aspell version 0.50.0 or
higher required
--with-libedit          Include libedit readline replacement (CLI/CGI only)
--with-readline[=DIR]   Include readline support (CLI/CGI only)
--disable-session       Disable session support
--with-mm[=DIR]         SESSION: Include mm support for session storage
--enable-shmop          Enable shmop support
--disable-simplexml     Disable SimpleXML support
--with-snmp[=DIR]       Include SNMP support
--enable-soap           Enable SOAP support
--enable-sockets        Enable sockets support
--with-sodium           Include sodium support
--with-password-argon2[=DIR]
Include Argon2 support in password_*. DIR is the
Argon2 shared library path
--enable-sysvmsg        Enable sysvmsg support
--enable-sysvsem        Enable System V semaphore support
--enable-sysvshm        Enable the System V shared memory support
--with-tidy[=DIR]       Include TIDY support
--disable-tokenizer     Disable tokenizer support
--disable-xml           Disable XML support
--with-expat            XML: use expat instead of libxml2
--disable-xmlreader     Disable XMLReader support
--with-xmlrpc[=DIR]     Include XMLRPC-EPI support
--with-expat            XMLRPC-EPI: use expat instead of libxml2
--with-iconv-dir=DIR    XMLRPC-EPI: iconv dir for XMLRPC-EPI
--disable-xmlwriter     Disable XMLWriter support
--with-xsl              Build with XSL support
--enable-zend-test      Enable zend-test extension
--with-zip              Include Zip read/write support
--enable-mysqlnd        Enable mysqlnd explicitly, will be done implicitly
when required by other extensions
--disable-mysqlnd-compression-support
Disable support for the MySQL compressed protocol in
mysqlnd

PEAR:

--with-pear[=DIR]       Install PEAR in DIR [PREFIX/lib/php]

Zend:

--enable-maintainer-zts Enable thread safety - for code maintainers only!!
--disable-inline-optimization
If building zend_execute.lo fails, try this switch
--disable-zend-signals  whether to enable zend signal handling

TSRM:

--with-tsrm-pth[=pth-config]
Use GNU Pth
--with-tsrm-st          Use SGI's State Threads
--with-tsrm-pthreads    Use POSIX threads (default)

Libtool:

--enable-shared=PKGS    Build shared libraries default=yes
--enable-static=PKGS    Build static libraries default=yes
--enable-fast-install=PKGS
Optimize for fast installation default=yes
--with-gnu-ld           Assume the C compiler uses GNU ld default=no
--disable-libtool-lock  Avoid locking (might break parallel builds)
--with-pic              Try to use only PIC/non-PIC objects default=use both
--with-tags=TAGS        Include additional configurations automatic


Some influential environment variables:
PKG_CONFIG  path to pkg-config utility
PKG_CONFIG_PATH
directories to add to pkg-config's search path
PKG_CONFIG_LIBDIR
path overriding pkg-config's built-in search path
CC          C compiler command
CFLAGS      C compiler flags
LDFLAGS     linker flags, e.g. -L<lib dir> if you have libraries in a
nonstandard directory <lib dir>
LIBS        libraries to pass to the linker, e.g. -l<library>
CPPFLAGS    (Objective) C/C++ preprocessor flags, e.g. -I<include dir> if
you have headers in a nonstandard directory <include dir>
CPP         C preprocessor
SYSTEMD_CFLAGS
C compiler flags for SYSTEMD, overriding pkg-config
SYSTEMD_LIBS
linker flags for SYSTEMD, overriding pkg-config
VALGRIND_CFLAGS
C compiler flags for VALGRIND, overriding pkg-config
VALGRIND_LIBS
linker flags for VALGRIND, overriding pkg-config
LIBXML_CFLAGS
C compiler flags for LIBXML, overriding pkg-config
LIBXML_LIBS linker flags for LIBXML, overriding pkg-config
KERBEROS_CFLAGS
C compiler flags for KERBEROS, overriding pkg-config
KERBEROS_LIBS
linker flags for KERBEROS, overriding pkg-config
OPENSSL_CFLAGS
C compiler flags for OPENSSL, overriding pkg-config
OPENSSL_LIBS
linker flags for OPENSSL, overriding pkg-config
PCRE2_CFLAGS
C compiler flags for PCRE2, overriding pkg-config
PCRE2_LIBS  linker flags for PCRE2, overriding pkg-config
SQLITE_CFLAGS
C compiler flags for SQLITE, overriding pkg-config
SQLITE_LIBS linker flags for SQLITE, overriding pkg-config
ZLIB_CFLAGS C compiler flags for ZLIB, overriding pkg-config
ZLIB_LIBS   linker flags for ZLIB, overriding pkg-config
CURL_CFLAGS C compiler flags for CURL, overriding pkg-config
CURL_LIBS   linker flags for CURL, overriding pkg-config
CURL_FEATURES
value of supported_features for libcurl, overriding pkg-config
ENCHANT_CFLAGS
C compiler flags for ENCHANT, overriding pkg-config
ENCHANT_LIBS
linker flags for ENCHANT, overriding pkg-config
FFI_CFLAGS  C compiler flags for FFI, overriding pkg-config
FFI_LIBS    linker flags for FFI, overriding pkg-config
PNG_CFLAGS  C compiler flags for PNG, overriding pkg-config
PNG_LIBS    linker flags for PNG, overriding pkg-config
WEBP_CFLAGS C compiler flags for WEBP, overriding pkg-config
WEBP_LIBS   linker flags for WEBP, overriding pkg-config
JPEG_CFLAGS C compiler flags for JPEG, overriding pkg-config
JPEG_LIBS   linker flags for JPEG, overriding pkg-config
XPM_CFLAGS  C compiler flags for XPM, overriding pkg-config
XPM_LIBS    linker flags for XPM, overriding pkg-config
FREETYPE2_CFLAGS
C compiler flags for FREETYPE2, overriding pkg-config
FREETYPE2_LIBS
linker flags for FREETYPE2, overriding pkg-config
GDLIB_CFLAGS
C compiler flags for GDLIB, overriding pkg-config
GDLIB_LIBS  linker flags for GDLIB, overriding pkg-config
ICU_CFLAGS  C compiler flags for ICU, overriding pkg-config
ICU_LIBS    linker flags for ICU, overriding pkg-config
CXX         C++ compiler command
CXXFLAGS    C++ compiler flags
CXXCPP      C++ preprocessor
SASL_CFLAGS C compiler flags for SASL, overriding pkg-config
SASL_LIBS   linker flags for SASL, overriding pkg-config
ONIG_CFLAGS C compiler flags for ONIG, overriding pkg-config
ONIG_LIBS   linker flags for ONIG, overriding pkg-config
ODBC_CFLAGS C compiler flags for ODBC, overriding pkg-config
ODBC_LIBS   linker flags for ODBC, overriding pkg-config
EDIT_CFLAGS C compiler flags for EDIT, overriding pkg-config
EDIT_LIBS   linker flags for EDIT, overriding pkg-config
LIBSODIUM_CFLAGS
C compiler flags for LIBSODIUM, overriding pkg-config
LIBSODIUM_LIBS
linker flags for LIBSODIUM, overriding pkg-config
EXPAT_CFLAGS
C compiler flags for EXPAT, overriding pkg-config
EXPAT_LIBS  linker flags for EXPAT, overriding pkg-config
XSL_CFLAGS  C compiler flags for XSL, overriding pkg-config
XSL_LIBS    linker flags for XSL, overriding pkg-config
EXSLT_CFLAGS
C compiler flags for EXSLT, overriding pkg-config
EXSLT_LIBS  linker flags for EXSLT, overriding pkg-config
LIBZIP_CFLAGS
C compiler flags for LIBZIP, overriding pkg-config
LIBZIP_LIBS linker flags for LIBZIP, overriding pkg-config

Use these variables to override the choices made by `configure' or to help
it to find libraries and programs with nonstandard names/locations.

Report bugs to <https://bugs.php.net>.
PHP home page: <https://www.php.net>.