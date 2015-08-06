# freebsd_install

For xorg not shutting down problem:
https://forums.freebsd.org/threads/cant-exit-from-xorg-pc-locked.49387/

For installing clisp:
here's the way:unzip and go to its folder

./configure with-gcc
cd with-gcc
vim config.lisp # if you want to change the config.
make # build
ulimit -s 16384 # you need it for running clisp
make check # check the build


and abuot ulimit, you shuold run it in shell before running clisp
you can add it to global profile scripts so it become global, but there's
reason why it's not like this. it allows DOS attacks.
