# ayugram-ebuild-gentoo

![AyuGram](https://github.com/AyuGram/AyuGramDesktop/raw/dev/.github/AyuGram.png) ![AyuChan](https://github.com/AyuGram/AyuGramDesktop/raw/dev/.github/AyuChan.png) <img src="https://www.gentoo.org/assets/img/logo/gentoo-signet.png" alt="Gentoo BTW" width="128"/>

[Русский](README.md)

**Unofficial AyuGram Desktop ebuild for Gentoo Linux**  
Up-to-date dev branch

→ https://github.com/AyuGram/AyuGramDesktop

## Installation

```bash
emerge --ask app-eselect/eselect-repository

sudo eselect repository add ayugram-unoffical git https://github.com/OverLessArtem/ayugram-ebuild-gentoo.git

sudo emaint sync --repo ayugram-unoffical

echo "net-im/ayugram-desktop ~amd64" | sudo tee /etc/portage/package.accept_keywords/ayugram-desktop

sudo emerge --ask --verbose net-im/ayugram-desktop
```
# CRITICAL — COMPILER
DO NOT use Clang (even with ThinLTO) — it crashes hard at the linking stage.
Only GCC works reliably
