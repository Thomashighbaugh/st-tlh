# ST-TLH

st is a simple terminal emulator for X which sucks less (st is created by the good folks at [suckless.org](https://suckless.org)), based on Derek Taylor's [configuration](https://gitlab.com/dwt1/st-distrotube)

### Patches:

```
>> alpha (for transparency)
>> font2 (to allow setting more than one font, useful when the default font has missing glyphs)
>> scrollback (scrollback through terminal using Shift+PageUp/PageDown.)
>> scrollback mouse altscreen (allows scrolling using Shift+MouseWheel.)
```

### Installing st-tlh (Arch)

```
    makepkg -cf
    sudo pacman -U *.pkg.tar.xz
```

# Installing st-tlh on (Other)

```
    git clone https://gitlab.com/dwt1/st-distrotube.git
    cd st-distrotube
    sudo make clean install
```
