# This PKGBUILD was generated by cpan4pacman via CPANPLUS::Dist::Pacman
# Contributor: 

pkgname=perl-sendmail-pmilter
pkgver=0.97
pkgrel=1
pkgdesc="Perl binding of Sendmail Milter protocol "
arch=('i686' 'x86_64')
url="http://search.cpan.org/~AVAR/Sendmail-PMilter"
license=('GPL' 'PerlArtistic')
depends=('perl')
options=('!emptydirs')
source=(http://www.cpan.org/authors/id/A/AV/AVAR/Sendmail-PMilter-$pkgver.tar.gz
	Context.pm.patch) 
md5sums=('dca1f18dacce0a7be855decd8682f973')

build() {
  cd  $startdir/src/Sendmail-PMilter-$pkgver
#
  patch -p1 < ../Context.pm.patch
  
  PERL_MM_USE_DEFAULT=1 perl Makefile.PL INSTALLDIRS=vendor || return 1 
  make || return 1
  make install DESTDIR=$startdir/pkg || return 1
  find $startdir/pkg -name '.packlist' -delete
  find $startdir/pkg -name '*.pod' -delete
}
