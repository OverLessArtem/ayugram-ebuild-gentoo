# ayugram-ebuild-gentoo

![AyuGram](https://github.com/AyuGram/AyuGramDesktop/raw/dev/.github/AyuGram.png) ![AyuChan](https://github.com/AyuGram/AyuGramDesktop/raw/dev/.github/AyuChan.png) <img src="https://www.gentoo.org/assets/img/logo/gentoo-signet.png" alt="Gentoo BTW" width="128"/>

[Русский](README.md)

**Unofficial AyuGram Desktop ebuild for Gentoo Linux**  
Up-to-date dev branch

→ https://github.com/AyuGram/AyuGramDesktop

## Installation

### Installation (Latest stable version)
The package is keyworded ~amd64. For x86_64, add ~amd64 to keywords.  
If you're on aarch64 — replace with ~arm64.

```bash
emerge --ask app-eselect/eselect-repository
eselect repository add ayugram git https://github.com/OverLessArtem/ayugram-ebuild-gentoo.git
emaint sync --repo ayugram
echo "net-im/ayugram-desktop ~amd64" | tee /etc/portage/package.accept_keywords/ayugram-desktop
# For aarch64: echo "net-im/ayugram-desktop ~arm64" | tee ...
emerge --ask --verbose net-im/ayugram-desktop
```
### Installation (Dev branch / live-9999)
```bash
emerge --ask app-eselect/eselect-repository
eselect repository add ayugram git https://github.com/OverLessArtem/ayugram-ebuild-gentoo.git
emaint sync --repo ayugram
echo "net-im/ayugram-desktop **" | tee /etc/portage/package.accept_keywords/ayugram-desktop
emerge --ask --verbose =net-im/ayugram-desktop-9999
```

# CRITICAL — COMPILER
DO NOT use Clang (even with ThinLTO) — it crashes hard at the linking stage.
Only GCC works reliably
