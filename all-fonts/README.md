# All font sizes

Font sizes 2...148 available in [this .zip](./fixedsys-excelsior-pf2/2-148_generated.zip). If you need other font sizes, you need to generate them from the .ttf file. To do this, you need any Linux system with GRUB, for example a virtual machine.

## Font files generating

### Example of font files generating commands

```sh
sudo grub-mkfont -s 16 -o fs-16.pf2 fixedsys-ligatures.ttf
sudo grub-mkfont -s 18 -o fs-18.pf2 fixedsys-ligatures.ttf
sudo grub-mkfont -s 20 -o fs-20.pf2 fixedsys-ligatures.ttf
sudo grub-mkfont -s 22 -o fs-22.pf2 fixedsys-ligatures.ttf
sudo grub-mkfont -s 24 -o fs-24.pf2 fixedsys-ligatures.ttf
sudo grub-mkfont -s 26 -o fs-26.pf2 fixedsys-ligatures.ttf
sudo grub-mkfont -s 28 -o fs-28.pf2 fixedsys-ligatures.ttf
sudo grub-mkfont -s 30 -o fs-30.pf2 fixedsys-ligatures.ttf
sudo grub-mkfont -s 32 -o fs-32.pf2 fixedsys-ligatures.ttf
```

### JavaScript script what generates commands

This script generates commands to create font files with sizes 2...148.

You can use it in Chrome DevTools, Node.JS or an online editor.

```js
let arr = []

for (let i = 2; i < 150; i += 2) {
  arr.push(`sudo grub-mkfont -s ${i} -o fs-${i}.pf2 fixedsys-ligatures.ttf`)
}

console.log(arr.join("\n"))
```
