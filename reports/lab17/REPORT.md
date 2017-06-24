## Laboratory work XVII

Данная лабораторная работа посвещена изучению процесса создания сеансов совместной разработки с использованием инструмента **ngrok**

```ShellSession
$ open https://ngrok.com/
```

## Tasks

- [V] 1. Ознакомиться со ссылками учебного материала
- [V] 2. Выполнить инструкцию учебного материала
- [V] 3. Составить отчет и отправить ссылку личным сообщением в **Slack**

## Tutorial

```ShellSession
$ cd ~ # в домашнюю директорию текущего пользователя
$ mkdir install # создать директорию install
$ mkdir tmp # создать директорию tmp
$ export HOME_PREFIX=`pwd`/install #задание переменной
$ echo $HOME_PREFIX # вывод переменной
/home/user/install
$ export USERNAME=`whoami` # задание переменной
```

```ShellSession
$ cd tmp # переход в каталог tmp
```

```ShellSession
$ wget https://github.com/libevent/libevent/releases/download/release-2.1.8-stable/libevent-2.1.8-stable.tar.gz #скачивание
$ tar -xvzf libevent-2.1.8-stable.tar.gz #разархивирование
$ cd libevent-2.1.8-stable #переход в каталог
$ ./configure --prefix=${HOME_PREFIX} #конфигурирование
checking for a BSD-compatible install... /usr/bin/install -c
checking whether build environment is sane... yes
checking for a thread-safe mkdir -p... /bin/mkdir -p
checking for gawk... no
checking for mawk... mawk
checking whether make sets $(MAKE)... yes
checking whether make supports nested variables... yes
checking whether make supports nested variables... (cached) yes
checking for style of include used by make... GNU
checking for gcc... gcc
checking whether the C compiler works... yes
checking for C compiler default output file name... a.out
checking for suffix of executables... 
checking whether we are cross compiling... no
checking for suffix of object files... o
checking whether we are using the GNU C compiler... yes
checking whether gcc accepts -g... yes
checking for gcc option to accept ISO C89... none needed
checking whether gcc understands -c and -o together... yes
checking dependency style of gcc... gcc3
checking how to run the C preprocessor... gcc -E
checking for grep that handles long lines and -e... /bin/grep
checking for egrep... /bin/grep -E
checking for ANSI C header files... yes
checking for sys/types.h... yes
checking for sys/stat.h... yes
checking for stdlib.h... yes
checking for string.h... yes
checking for memory.h... yes
checking for strings.h... yes
checking for inttypes.h... yes
checking for stdint.h... yes
checking for unistd.h... yes
checking minix/config.h usability... no
checking minix/config.h presence... no
checking for minix/config.h... no
checking whether it is safe to define __EXTENSIONS__... yes
checking build system type... i686-pc-linux-gnu
checking host system type... i686-pc-linux-gnu
checking whether ln -s works... yes
checking for a sed that does not truncate output... /bin/sed
checking whether gcc needs -traditional... no
checking how to print strings... printf
checking for a sed that does not truncate output... (cached) /bin/sed
checking for fgrep... /bin/grep -F
checking for ld used by gcc... /usr/bin/ld
checking if the linker (/usr/bin/ld) is GNU ld... yes
checking for BSD- or MS-compatible name lister (nm)... /usr/bin/nm -B
checking the name lister (/usr/bin/nm -B) interface... BSD nm
checking the maximum length of command line arguments... 1572864
checking how to convert i686-pc-linux-gnu file names to i686-pc-linux-gnu format... func_convert_file_noop
checking how to convert i686-pc-linux-gnu file names to toolchain format... func_convert_file_noop
checking for /usr/bin/ld option to reload object files... -r
checking for objdump... objdump
checking how to recognize dependent libraries... pass_all
checking for dlltool... no
checking how to associate runtime and link libraries... printf %s\n
checking for ar... ar
checking for archiver @FILE support... @
checking for strip... strip
checking for ranlib... ranlib
checking command to parse /usr/bin/nm -B output from gcc object... ok
checking for sysroot... no
checking for a working dd... /bin/dd
checking how to truncate binary pipes... /bin/dd bs=4096 count=1
checking for mt... mt
checking if mt is a manifest tool... no
checking for dlfcn.h... yes
checking for objdir... .libs
checking if gcc supports -fno-rtti -fno-exceptions... no
checking for gcc option to produce PIC... -fPIC -DPIC
checking if gcc PIC flag -fPIC -DPIC works... yes
checking if gcc static flag -static works... yes
checking if gcc supports -c -o file.o... yes
checking if gcc supports -c -o file.o... (cached) yes
checking whether the gcc linker (/usr/bin/ld) supports shared libraries... yes
checking whether -lc should be explicitly linked in... no
checking dynamic linker characteristics... GNU/Linux ld.so
checking how to hardcode library paths into programs... immediate
checking whether stripping libraries is possible... yes
checking if libtool supports shared libraries... yes
checking whether to build shared libraries... yes
checking whether to build static libraries... yes
checking for library containing inet_ntoa... none required
checking for library containing socket... none required
checking for library containing inet_aton... none required
checking for library containing clock_gettime... none required
checking for clock_gettime... yes
checking for library containing sendfile... none required
checking for WIN32... no
checking for CYGWIN... no
checking zlib.h usability... no
checking zlib.h presence... no
checking for zlib.h... no
checking for special C compiler options needed for large files... no
checking for _FILE_OFFSET_BITS value needed for large files... 64
checking for pkg-config... /usr/bin/pkg-config
checking if pkg-config is at least version 0.15.0... yes
checking for library containing SSL_new... no
checking for library containing SSL_new... no
checking arpa/inet.h usability... yes
checking arpa/inet.h presence... yes
checking for arpa/inet.h... yes
checking fcntl.h usability... yes
checking fcntl.h presence... yes
checking for fcntl.h... yes
checking ifaddrs.h usability... yes
checking ifaddrs.h presence... yes
checking for ifaddrs.h... yes
checking mach/mach_time.h usability... no
checking mach/mach_time.h presence... no
checking for mach/mach_time.h... no
checking netdb.h usability... yes
checking netdb.h presence... yes
checking for netdb.h... yes
checking netinet/in.h usability... yes
checking netinet/in.h presence... yes
checking for netinet/in.h... yes
checking netinet/in6.h usability... no
checking netinet/in6.h presence... no
checking for netinet/in6.h... no
checking netinet/tcp.h usability... yes
checking netinet/tcp.h presence... yes
checking for netinet/tcp.h... yes
checking poll.h usability... yes
checking poll.h presence... yes
checking for poll.h... yes
checking port.h usability... no
checking port.h presence... no
checking for port.h... no
checking stdarg.h usability... yes
checking stdarg.h presence... yes
checking for stdarg.h... yes
checking stddef.h usability... yes
checking stddef.h presence... yes
checking for stddef.h... yes
checking sys/devpoll.h usability... no
checking sys/devpoll.h presence... no
checking for sys/devpoll.h... no
checking sys/epoll.h usability... yes
checking sys/epoll.h presence... yes
checking for sys/epoll.h... yes
checking sys/event.h usability... no
checking sys/event.h presence... no
checking for sys/event.h... no
checking sys/eventfd.h usability... yes
checking sys/eventfd.h presence... yes
checking for sys/eventfd.h... yes
checking sys/ioctl.h usability... yes
checking sys/ioctl.h presence... yes
checking for sys/ioctl.h... yes
checking sys/mman.h usability... yes
checking sys/mman.h presence... yes
checking for sys/mman.h... yes
checking sys/param.h usability... yes
checking sys/param.h presence... yes
checking for sys/param.h... yes
checking sys/queue.h usability... yes
checking sys/queue.h presence... yes
checking for sys/queue.h... yes
checking sys/resource.h usability... yes
checking sys/resource.h presence... yes
checking for sys/resource.h... yes
checking sys/select.h usability... yes
checking sys/select.h presence... yes
checking for sys/select.h... yes
checking sys/sendfile.h usability... yes
checking sys/sendfile.h presence... yes
checking for sys/sendfile.h... yes
checking sys/socket.h usability... yes
checking sys/socket.h presence... yes
checking for sys/socket.h... yes
checking for sys/stat.h... (cached) yes
checking sys/time.h usability... yes
checking sys/time.h presence... yes
checking for sys/time.h... yes
checking sys/timerfd.h usability... yes
checking sys/timerfd.h presence... yes
checking for sys/timerfd.h... yes
checking sys/uio.h usability... yes
checking sys/uio.h presence... yes
checking for sys/uio.h... yes
checking sys/wait.h usability... yes
checking sys/wait.h presence... yes
checking for sys/wait.h... yes
checking errno.h usability... yes
checking errno.h presence... yes
checking for errno.h... yes
checking for sys/sysctl.h... yes
checking for TAILQ_FOREACH in sys/queue.h... yes
checking for timeradd in sys/time.h... yes
checking for timercmp in sys/time.h... yes
checking for timerclear in sys/time.h... yes
checking for timerisset in sys/time.h... yes
checking whether CTL_KERN is declared... yes
checking whether KERN_RANDOM is declared... yes
checking whether RANDOM_UUID is declared... yes
checking whether KERN_ARND is declared... no
checking for an ANSI C-conforming const... yes
checking for inline... inline
checking whether time.h and sys/time.h may both be included... yes
checking for accept4... yes
checking for arc4random... no
checking for arc4random_buf... no
checking for eventfd... yes
checking for epoll_create1... yes
checking for fcntl... yes
checking for getegid... yes
checking for geteuid... yes
checking for getifaddrs... yes
checking for getnameinfo... yes
checking for getprotobynumber... yes
checking for gettimeofday... yes
checking for inet_ntop... yes
checking for inet_pton... yes
checking for issetugid... no
checking for mach_absolute_time... no
checking for mmap... yes
checking for nanosleep... yes
checking for pipe... yes
checking for pipe2... yes
checking for putenv... yes
checking for sendfile... yes
checking for setenv... yes
checking for setrlimit... yes
checking for sigaction... yes
checking for signal... yes
checking for splice... yes
checking for strlcpy... no
checking for strsep... yes
checking for strtok_r... yes
checking for strtoll... yes
checking for sysctl... yes
checking for timerfd_create... yes
checking for umask... yes
checking for unsetenv... yes
checking for usleep... yes
checking for vasprintf... yes
checking for getservbyname... yes
checking for getaddrinfo... yes
checking for F_SETFD in fcntl.h... yes
checking for select... yes
checking for poll... yes
checking for epoll_ctl... yes
checking waitpid support WNOWAIT... no
checking for port_create... no
checking for pid_t... yes
checking for size_t... yes
checking for ssize_t... yes
checking for uint64_t... yes
checking for uint32_t... yes
checking for uint16_t... yes
checking for uint8_t... yes
checking for uintptr_t... yes
checking for fd_mask... yes
checking size of long long... 8
checking size of long... 4
checking size of int... 4
checking size of short... 2
checking size of size_t... 4
checking size of void *... 4
checking size of off_t... 8
checking for struct in6_addr... yes
checking for struct sockaddr_in6... yes
checking for sa_family_t... yes
checking for struct addrinfo... yes
checking for struct sockaddr_storage... yes
checking for struct in6_addr.s6_addr32... yes
checking for struct in6_addr.s6_addr16... yes
checking for struct sockaddr_in.sin_len... no
checking for struct sockaddr_in6.sin6_len... no
checking for struct sockaddr_storage.ss_family... yes
checking for struct sockaddr_storage.__ss_family... no
checking for struct so_linger... no
checking for socklen_t... yes
checking whether our compiler supports __func__... yes
checking for the pthreads library -lpthreads... no
checking whether pthreads work without any flags... no
checking whether pthreads work with -Kthread... no
checking whether pthreads work with -kthread... no
checking for the pthreads library -llthread... no
checking whether pthreads work with -pthread... yes
checking for joinable pthread attribute... PTHREAD_CREATE_JOINABLE
checking if more special flags are required for pthreads... no
checking size of pthread_t... 4
checking for library containing ERR_remove_thread_state... no
checking that generated files are newer than configure... done
configure: creating ./config.status
config.status: creating libevent.pc
config.status: creating libevent_openssl.pc
config.status: creating libevent_pthreads.pc
config.status: creating libevent_core.pc
config.status: creating libevent_extra.pc
config.status: creating Makefile
config.status: creating config.h
config.status: creating evconfig-private.h
config.status: executing depfiles commands
config.status: executing libtool commands
$ make && make install  # компиляция
$ cd .. # возврат в каталог tmp
```

```ShellSession
$ wget http://invisible-island.net/datafiles/release/ncurses.tar.gz # скачивание архива
$ tar -xvzf ncurses.tar.gz # распаковка архива
$ cd ncurses-5.9 # переход в каталог
$ ./configure --prefix=${HOME_PREFIX}
checking for egrep... grep -E
Configuring NCURSES 5.9 ABI 5 (Sat Jun 24 16:22:22 MSK 2017)
checking build system type... i686-pc-linux-gnu
checking host system type... i686-pc-linux-gnu
checking target system type... i686-pc-linux-gnu
Configuring for linux-gnu
checking for prefix... /home/user/install
checking for gcc... gcc
checking for C compiler default output... a.out
checking whether the C compiler works... yes
checking whether we are cross compiling... no
checking for executable suffix... 
checking for object suffix... o
checking whether we are using the GNU C compiler... yes
checking whether gcc accepts -g... yes
checking version of gcc... 5.4.0
checking how to run the C preprocessor... gcc -E
checking whether gcc needs -traditional... no
checking whether gcc understands -c and -o together... yes
checking for POSIXized ISC... no
checking for gcc option to accept ANSI C... -DCC_HAS_PROTOS
checking for ldconfig... /sbin/ldconfig
checking if you want to ensure bool is consistent with C++... yes
checking for g++... g++
checking whether we are using the GNU C++ compiler... yes
checking whether g++ accepts -g... yes
checking for g++... /usr/bin/g++
checking version of g++... 5.4.0
checking if you want to build C++ binding and demo... yes
checking if you want to build with Ada95... yes
checking if you want to install manpages... yes
checking if you want to build programs such as tic... yes
checking if you want to build test-programs... yes
checking if you wish to install curses.h... yes
checking for mawk... mawk
checking for egrep... (cached) grep -E
checking for a BSD compatible install... /usr/bin/install -c
checking for tdlint... no
checking for lint... no
checking for alint... no
checking for splint... no
checking for lclint... no
checking whether ln -s works... yes
checking if ln -s -f options work... yes
checking for long file names... yes
checking if you want to use pkg-config... yes
checking for pkg-config... /usr/bin/pkg-config
checking if we should install .pc files for /usr/bin/pkg-config... no
checking if we should assume mixed-case filenames... auto
checking if filesystem supports mixed-case filenames... yes
checking whether make sets ${MAKE}... yes
checking for exctags... no
checking for ctags... no
checking for exetags... no
checking for etags... no
checking for ctags... no
checking for etags... no
checking for makeflags variable... 
checking for ranlib... ranlib
checking for ld... ld
checking for ar... ar
checking for ar... (cached) ar
checking for options to update archives... -curv
checking if you have specified an install-prefix... 
checking if libtool -version-number should be used... yes
checking if you want to build libraries with libtool... no
checking if you want to build shared libraries... no
checking if you want to build static libraries... yes
checking if you want to build debug libraries... yes
checking if you want to build profiling libraries... no
checking for specified models...  normal debug
checking for default model... normal
checking if you want to build a separate terminfo library... no
checking if you want to build a separate tic library... no
checking if you want to link with the GPM mouse library... maybe
checking for gpm.h... no
checking for default loader flags... 
checking for an rpath option... -Wl,-rpath,
checking if release/abi version should be used for shared libs... auto
checking which gcc option to use... -fPIC
checking if you wish to install ncurses overwriting curses... no
checking if external terminfo-database is used... yes
checking which terminfo source-file will be installed... ${top_srcdir}/misc/terminfo.src
checking whether to use hashed database instead of directory/tree... no
checking for list of fallback descriptions... 
checking if you want modern xterm or antique... xterm-new
checking for list of terminfo directories... /home/user/install/share/terminfo
checking for default terminfo directory... /home/user/install/share/terminfo
checking if big-core option selected... yes
checking if big-strings option selected... yes
checking if you want termcap-fallback support... no
checking if ~/.terminfo is wanted... yes
checking if you want to use restricted environment when running as root... yes
checking for remove... yes
checking for unlink... yes
checking if link/symlink functions work...  link symlink
checking if tic should use symbolic links... no
checking if tic should use hard links... yes
checking if you want broken-linker support code... no
checking if tputs should process BSD-style prefix padding... no
checking if we must define _GNU_SOURCE... yes
checking if SIGWINCH is defined... yes
checking for nl_langinfo and CODESET... yes
checking if you want wide-character code... no
checking whether to enable _LP64 definition in curses.h... no
checking for special C compiler options needed for large files... no
checking for _FILE_OFFSET_BITS value needed for large files... 64
checking for _LARGE_FILES value needed for large files... no
checking for _LARGEFILE_SOURCE value needed for large files... no
checking for fseeko... yes
checking whether to use struct dirent64... no
checking if you want tparm not to use X/Open fixed-parameter list... yes
checking for type of bool... auto
checking for alternate terminal capabilities file... Caps
checking for type of chtype... auto
checking for type of ospeed... short
checking for type of mmask_t... auto
checking for size CCHARW_MAX... 5
checking if RCS identifiers should be compiled-in... no
checking format of man-pages...  gzip
checking for manpage renaming... /home/user/tmp/ncurses-5.9/man/man_db.renames
checking if manpage aliases will be installed... yes
checking if manpage symlinks should be used... yes
checking for manpage tbl... no
checking if you want to build with function extensions... yes
checking if you want to build with experimental SCREEN extensions... no
checking if you want to build with experimental terminal-driver... no
checking for extended use of const keyword... no
checking if you want to use extended colors... no
checking if you want to use extended mouse encoding... no
checking if you want $NCURSES_NO_PADDING code... yes
checking for ANSI C header files... yes
checking for sys/types.h... yes
checking for sys/stat.h... yes
checking for stdlib.h... yes
checking for string.h... yes
checking for memory.h... yes
checking for strings.h... yes
checking for inttypes.h... yes
checking for stdint.h... yes
checking for unistd.h... yes
checking for signed char... yes
checking size of signed char... 1
checking if you want to use signed Boolean array in term.h... no
checking if you want SIGWINCH handler... yes
checking if you want user-definable terminal capabilities like termcap... yes
checking if you want all development code... no
checking if you want hard-tabs code... no
checking if you want limited support for xmc... no
checking if you do not want to assume colors are white-on-black... yes
checking if you want hashmap scrolling-optimization code... yes
checking if you want colorfgbg code... no
checking if you want interop bindings... no
checking if you want to link with the pthread library... no
checking if you want experimental reentrant code... no
checking if you want experimental safe-sprintf code... no
checking if you want experimental wgetch-events code... no
checking if you want to display full commands during build... yes
checking if you want to see compiler warnings... 
configure: checking for gcc __attribute__ directives...
... scanf
... printf
... unused
... noreturn
checking if you want to enable runtime assertions... no
checking if you want to use dmalloc for testing... no
checking if you want to use dbmalloc for testing... no
checking if you want to use valgrind for testing... no
checking if you want to perform memory-leak testing... no
checking whether to add trace feature to all models... no
checking for gettimeofday... yes
checking if -lm needed for math functions... yes
checking for ANSI C header files... (cached) yes
checking for dirent.h that defines DIR... yes
checking for opendir in -ldir... no
checking whether time.h and sys/time.h may both be included... yes
checking for regcomp... yes
checking for regular-expression headers... regex.h
checking for fcntl.h... yes
checking for getopt.h... yes
checking for limits.h... yes
checking for locale.h... yes
checking for math.h... yes
checking for poll.h... yes
checking for sys/bsdtypes.h... no
checking for sys/ioctl.h... yes
checking for sys/param.h... yes
checking for sys/poll.h... yes
checking for sys/select.h... yes
checking for sys/time.h... yes
checking for sys/times.h... yes
checking for ttyent.h... yes
checking for unistd.h... (cached) yes
checking for wctype.h... yes
checking if sys/time.h works with sys/select.h... yes
checking for gcc option to accept ANSI C... none needed
checking for an ANSI C-conforming const... yes
checking for inline... inline
checking if gcc supports options to tune inlining... yes
checking for signal global datatype... volatile sig_atomic_t
checking for type of chtype... long
checking if unsigned literals are legal... yes
checking if external errno is declared... yes
checking if external errno exists... no
checking if data-only library module links... yes
checking for getcwd... yes
checking for getegid... yes
checking for geteuid... yes
checking for getttynam... yes
checking for issetugid... no
checking for poll... yes
checking for remove... (cached) yes
checking for select... yes
checking for setbuf... yes
checking for setbuffer... yes
checking for setvbuf... yes
checking for sigaction... yes
checking for sigvec... no
checking for strdup... yes
checking for strstr... yes
checking for tcgetpgrp... yes
checking for times... yes
checking for vsnprintf... yes
checking for isascii... yes
checking whether sigaction needs _POSIX_SOURCE... no
checking if nanosleep really works... yes
checking for termio.h... yes
checking for termios.h... yes
checking for unistd.h... (cached) yes
checking whether termios.h needs _POSIX_SOURCE... no
checking for tcgetattr... yes
checking for vsscanf function or workaround... vsscanf
checking for working mkstemp... yes
checking whether setvbuf arguments are reversed... no
checking return type of signal handlers... void
checking for type sigaction_t... no
checking declaration of size-change... yes
checking for memmove... yes
checking if poll really works... yes
checking for va_copy... yes
checking for __va_copy... yes
checking for pid_t... yes
checking for unistd.h... (cached) yes
checking for vfork.h... no
checking for fork... yes
checking for vfork... yes
checking for working fork... (cached) yes
checking for working vfork... (cached) yes
checking for openpty in -lutil... yes
checking for openpty header... pty.h
checking if we should include stdbool.h... yes
checking for builtin bool type... no
checking for library stdc++... no
checking whether /usr/bin/g++ understands -c and -o together... yes
checking how to run the C++ preprocessor... /usr/bin/g++ -E
checking for iostream... yes
checking for typeinfo... yes
checking if iostream uses std-namespace... yes
checking if we should include stdbool.h... (cached) yes
checking for builtin bool type... yes
checking for size of bool... unsigned char
checking for special defines needed for etip.h... none
checking if /usr/bin/g++ accepts parameter initialization... no
checking if /usr/bin/g++ accepts static_cast... yes
checking for gnatmake... no
checking for library subsets... ticlib+termlib+ext_tinfo+base+ext_funcs
checking default library suffix... 
checking default library-dependency suffix... .a
checking default object directory... objects
checking c++ library-dependency suffix... .a
checking if linker supports switching between static/dynamic... yes
checking where we will install curses.h... ${prefix}/include/ncurses
checking for src modules... ncurses progs panel menu form
checking for tic... /usr/bin/tic
configure: creating ./config.status
config.status: creating include/MKterm.h.awk
config.status: creating include/curses.head
config.status: creating include/ncurses_dll.h
config.status: creating include/termcap.h
config.status: creating include/unctrl.h
config.status: creating man/Makefile
config.status: creating include/Makefile
config.status: creating ncurses/Makefile
config.status: creating progs/Makefile
config.status: creating panel/Makefile
config.status: creating menu/Makefile
config.status: creating form/Makefile
config.status: creating test/Makefile
config.status: creating misc/Makefile
config.status: creating c++/Makefile
config.status: creating Ada95/gen/adacurses-config
config.status: creating man/adacurses-config.1
config.status: creating misc/run_tic.sh
config.status: creating misc/ncurses-config
config.status: creating man/ncurses5-config.1
config.status: creating Makefile
config.status: creating include/ncurses_cfg.h
Appending rules for normal model (ncurses: ticlib+termlib+ext_tinfo+base+ext_funcs)
Appending rules for debug model (ncurses: ticlib+termlib+ext_tinfo+base+ext_funcs)
Appending rules for normal model (progs: ticlib+termlib+ext_tinfo+base+ext_funcs)
Appending rules for debug model (progs: ticlib+termlib+ext_tinfo+base+ext_funcs)
Appending rules for normal model (panel: ticlib+termlib+ext_tinfo+base+ext_funcs)
Appending rules for debug model (panel: ticlib+termlib+ext_tinfo+base+ext_funcs)
Appending rules for normal model (menu: ticlib+termlib+ext_tinfo+base+ext_funcs)
Appending rules for debug model (menu: ticlib+termlib+ext_tinfo+base+ext_funcs)
Appending rules for normal model (form: ticlib+termlib+ext_tinfo+base+ext_funcs)
Appending rules for debug model (form: ticlib+termlib+ext_tinfo+base+ext_funcs)
Appending rules for normal model (test: ticlib+termlib+ext_tinfo+base+ext_funcs)
Appending rules for debug model (test: ticlib+termlib+ext_tinfo+base+ext_funcs)
Appending rules for normal model (c++: ticlib+termlib+ext_tinfo+base+ext_funcs)
Appending rules for debug model (c++: ticlib+termlib+ext_tinfo+base+ext_funcs)
creating headers.sh

** Configuration summary for NCURSES 5.9 20110404:

     extended funcs: yes
     xterm terminfo: xterm-new

      bin directory: /home/user/install/bin
      lib directory: /home/user/install/lib
  include directory: /home/user/install/include/ncurses
      man directory: /home/user/install/man
 terminfo directory: /home/user/install/share/terminfo

** Include-directory is not in a standard location
поправлен файл ncurses/base/MKlib_gen.sh:

if test "${LC_COLLATE+set}"  = set; then LC_COLLATE=C;  export LC_COLLATE;  fi

# Work around "unexpected" output of GCC 5.1.0's cpp w.r.t. #line directives
# by simply suppressing them:
case `$1 -dumpversion 2>/dev/null` in
    5.[01].*)  # assume a "broken" one
        preprocessor="$1 -P -DNCURSES_INTERNALS -I../include"
        ;;
    *)
        preprocessor="$1 -DNCURSES_INTERNALS -I../include"
esac
AWK="$2"
USE="$3"

Вместо такого:

preprocessor="$1 -DNCURSES_INTERNALS -I../include"

$ make && make install 
$ cd ..
```


```ShellSession
$ wget https://github.com/tmux/tmux/releases/download/2.5/tmux-2.5.tar.gz
$ tar -xvzf tmux-2.5.tar.gz
$ cd tmux-2.5
$ ./configure --prefix=${HOME_PREFIX} CFLAGS="-I${HOME_PREFIX}/include -I${HOME_PREFIX}/include/ncurses" LDFLAGS="-L${HOME_PREFIX}/lib"
$ make && make install # https://gist.github.com/P7h/91e14096374075f5316e
$ cd ..
```

```ShellSession
$ wget https://bin.equinox.io/c/4VmDzA7iaHb/ngrok-stable-linux-amd64.zip
wget https://bin.equinox.io/c/4VmDzA7iaHb/ngrok-stable-linux-386.zip
$ unizp ngrok-stable-linux-amd64.zip
unzip ngrok-stable-linux-386.zip
$ mv ngrok ${HOME_PREFIX}/bin
```

```ShellSession
$ export LD_LIBRARY_PATH=${HOME_PREFIX}/lib
$ export PATH="${HOME_PREFIX}/bin:${PATH}"
$ tmux new -s session_with_group
```

```ShellSession
$ open https://ngrok.com/signup
$ export NGROK_TOKEN=6tA8crSQQZz13cMNMXLNh_5XUGZFzpnbbifin8c2Hzy
$ ngrok authtoken ${NGROK_TOKEN}
$ ngrok tcp 22
11440
```

```ShellSession
$ ssh ${USERNAME}@0.tcp.ngrok.io -p11440
<********>
$ tmux a -t session_with_group
$ <C-B>"
```

## Report

```ShellSession
$ cd ~/workspace/labs/
$ export LAB_NUMBER=16
$ git clone https://github.com/tp-labs/lab${LAB_NUMBER} tasks/lab${LAB_NUMBER}
$ mkdir reports/lab${LAB_NUMBER}
$ cp tasks/lab${LAB_NUMBER}/README.md reports/lab${LAB_NUMBER}/REPORT.md
$ cd reports/lab${LAB_NUMBER}
$ edit REPORT.md
$ gistup -m"lab${LAB_NUMBER}"
```

## Links

- [Tmux](https://raw.githubusercontent.com/tmux/tmux/master/README)
- [Libevent](http://libevent.org)
- [Ncurses](http://invisible-island.net/ncurses/)

```
Copyright (c) 2017 Братья Вершинины
```
