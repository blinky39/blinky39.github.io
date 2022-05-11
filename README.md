# [pages](https://blinky39.github.io)
Leon Satoshi's wiki, documents some notes.🎃


too lazy to set up a page...

## xwallpaper and feh failed to change desktop backgroud under xfce4 DE:
[original post](https://unix.stackexchange.com/questions/596070/how-to-change-wallpaper-on-xfce-from-terminal)

1. use xfconf-query to find which property determins backgroud change:
`xfconf-query -c xfce4-desktop -m` and change wallpaper by other means, the output should be like this: *set: /backdrop/screen0/monitoreDP1/workspace0/last-image* in *set: value* format.
2. use `xfconf-query -c xfce4-desktop -p value -s path/to/image` to perform in terminal
3. so you can make setbg scripts work in xfce4, cheers!
