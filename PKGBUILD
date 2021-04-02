# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: vivek kumar kushwaha <vivekkushwaha39@gmail.com>
pkgname="x86_64-w64-binutils"
pkgver=2.36
pkgrel=1
epoch=
pkgdesc=""
arch=(x86_64)
url="https://ftp.gnu.org/gnu/binutils/"
license=('GPL')
groups=()
depends=()
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("https://ftp.gnu.org/gnu/binutils/binutils-${pkgver}.tar.xz")
noextract=()
md5sums=(f6114b8c40096f9aa9f64fe1ab8ba087)
validpgpkeys=()

prepare() {
	cd "binutils-$pkgver"
}

build() {
	CARCH=""                                                        
	CHOST=""                                           
	                                                                        
	#-- Compiler and Linker Flags                                         
	CPPFLAGS=""                                        
	CFLAGS=""              
	CXXFLAGS=""            
	LDFLAGS=""           
	#-- Make Flags: change this for DistCC/SMP systems                    
	#MAKEFLAGS="-j2"                                                      
	#-- Debugging flags                                                   
	DEBUG_CFLAGS=""                          
	DEBUG_CXXFLAGS=""                        
	cd "$srcdir/binutils-$pkgver"
	./configure --build=x86_64-unknown-linux-gnu --target=x86_64-w64-mingw32 --disable-multilib --prefix=$pkgdir/opt/x86-64-w64-mingw32
	make all
}

check() {
#	cd "$pkgname-$pkgver"
#	make -k check
	echo "Skipping check"
}

package() {
	cd "binutils-$pkgver"
	make install
}
