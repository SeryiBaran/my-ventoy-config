# All font sizes

Font sizes 2...148 available in [this folder](./). If you need other font sizes, you need to generate them from the .ttf file. To do this, you need any Linux system with GRUB, for example a virtual machine.

## Font files generating

### Example of font files generating commands

```sh
sudo grub-mkfont -s 16 -o font_name-16.pf2 font_name.ttf
sudo grub-mkfont -s 18 -o font_name-18.pf2 font_name.ttf
sudo grub-mkfont -s 20 -o font_name-20.pf2 font_name.ttf
sudo grub-mkfont -s 22 -o font_name-22.pf2 font_name.ttf
sudo grub-mkfont -s 24 -o font_name-24.pf2 font_name.ttf
sudo grub-mkfont -s 26 -o font_name-26.pf2 font_name.ttf
sudo grub-mkfont -s 28 -o font_name-28.pf2 font_name.ttf
sudo grub-mkfont -s 30 -o font_name-30.pf2 font_name.ttf
sudo grub-mkfont -s 32 -o font_name-32.pf2 font_name.ttf
sudo grub-mkfont -s 140 -o font_name-140.pf2 font_name.ttf
```

### JavaScript script what generates commands

This script generates commands to create font files with sizes 2...148.

You can use it in Chrome DevTools, Node.JS or an online editor.

```js
let arr = []

for (let i = 2; i < 150; i += 2) {
  arr.push(`sudo grub-mkfont -s ${i} -o font_name-${i}.pf2 font_name.ttf`)
}

console.log(arr.join("\n"))
```
