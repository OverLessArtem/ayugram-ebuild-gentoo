# ayugram-ebuild-gentoo

![AyuGram](https://github.com/AyuGram/AyuGramDesktop/raw/dev/.github/AyuGram.png) ![AyuChan](https://github.com/AyuGram/AyuGramDesktop/raw/dev/.github/AyuChan.png) <img src="https://www.gentoo.org/assets/img/logo/gentoo-signet.png" alt="Gentoo BTW" width="128" align="right"/>

**Неофициальный ebuild AyuGram Desktop для Gentoo Linux**  
Актуальный dev-бранч

→ https://github.com/AyuGram/AyuGramDesktop

## Установка

```bash
emerge --ask app-eselect/eselect-repository

sudo eselect repository add ayugram git https://github.com/OverLessArtem/ayugram-ebuild-gentoo.git

sudo emaint sync --repo ayugram

echo "net-im/ayugram-desktop ~amd64" | sudo tee /etc/portage/package.accept_keywords/ayugram-desktop

sudo emerge --ask --verbose net-im/ayugram-desktop
```
# ВАЖНО — КОМПИЛЯТОР
НЕ используйте Clang (даже с ThinLTO) — падает на этапе линковки
Работает только на GCC.
