# Google start with proxy
## command
/usr/bin/google-chrome-stable --proxy-server="socks://localhost:7890"
## wirte in desktop
the desktop is in /usr/share/applications/google-chrome.desktop,and just change the exec.

# terminal with proxy
## command
export all_proxy="socks5://127.0.0.1:7890"
## wirte in .bashrc or .zshrc