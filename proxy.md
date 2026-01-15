# Google start with proxy
## command
/usr/bin/google-chrome-stable --proxy-server="socks://localhost:7890"
## wirte in desktop
the desktop is in /usr/share/applications/google-chrome.desktop,and just change the exec.

- ` **<b>abc</b>Exec=/usr/bin/google-chrome-stable%U change** to **Exec=/usr/bin/google-chrome-stable --proxy-server="socks://localhost:7890"%U**`
-  `sudo update-desktop-database /usr/share/applications`
-  `nautilus -q`

# terminal with proxy
## command
`export all_proxy="socks5://127.0.0.1:7890"`

`export http_proxy="http://127.0.0.1:7890"`

`export https_proxy="https://127.0.0.1:7890"`

## wirte in .bashrc or .zshrc
