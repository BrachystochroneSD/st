# Maintainer: Samuel Dawant <samueld@mailo.com>
pkgname=zenowl-st
pkgver=8.2
pkgrel=1
pkgdesc="zenowl version of st"
arch=(x86_64)
url="git@github.com:BrachystochroneSD/st.git"
license=('GPL')
provides=(st)
source=(
    arg.h
    config.def.h
    config.mk
    Makefile
    st.1
    st.c
    st.h
    st.info
    win.h
    x.c
)
sha256sums=('1a10fac42d03b3a1231cd6998a73fb4ab4f191694628953e7229f6de2053a985'
            '431ea87fd6823c856f926bf370a7b4939b8de190a781b17ae2fe3157d11af325'
            'c79db507006740e91e16e5eef27771b211e0cef67b054d728c741942d2db4f29'
            'e044cdf7af1c672ed40f84a2bbebf20ca257ba78b72ea9d0bf5bd4ae6edb410c'
            '93d7e26631208ea037b80fe7ac4d8b0f8b14ef4eefc34abbee247ac5e7c6c15f'
            '46e07f94e0605bb99d08d279b6b12ce596776ec4b692c5c7fd1485bd3678815e'
            '91590252717278ab5636b42d5f0dbbd22271416128f892c8f2773c35b9dca37f'
            '3fadecc861a61d65bd2e9020e02aa7c8e752b77974af440af3a802adaca5fdaa'
            '707a68579c93de5b33bbfbbe824bff6059794498cf1302843476ba4706065b46'
            '990f466ed2a68a5b191fb82f0c1cdc095bd0973b0877a72dd0e1c30a1a650624')


prepare() {
    # skip terminfo which conflicts with nsurses
    sed -i '/tic /d' Makefile
}

build() {
    make
}

package() {
    make PREFIX="/usr" DESTDIR="$pkgdir/" install
}
