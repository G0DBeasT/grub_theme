# Grub Theme
A GRUB theme based on one of the frame of House Of The Dragons.

![Preview](preview.jpg "GRUB2 Theme Preview")

## Installation
> [!IMPORTANT]
> This theme is a WIP **only supporting 2560x1440 and 1920x1080** resolutions. It will not look optimal on different resolutions. Feel free to add support for your resolutions using [this contribution guide](CONTRIBUTING.md).

1. Download this theme from [releases](https://github.com/G0DBeasT/grub_theme/releases) or clone the repository directly:
    ```bash
    git clone [https://github.com/G0DBeasT/grub_theme.git](https://github.com/G0DBeasT/grub_theme.git)
    ```
2. Rename the directory to `grub_theme`
3. Copy the directory you renamed `grub_theme` to `/boot/grub/themes`
    ```
    # cp -r /path/to/grub_theme /boot/grub/themes
    ```
4. Edit `/etc/default/grub` (as a superuser)
    - Set `GRUB_THEME=` TO `/boot/grub/themes/grub_theme/theme.txt`
    - Make sure `GRUB_TERMINAL_OUTPUT="gfxterm"`
    - Set `GRUB_GFXMODE=` to your resolution (e.g. `1920x1080`) and uncomment it 
5. Update GRUB
    - Arch Linux
        ```
        # grub-mkconfig -o /boot/grub/grub.cfg
        ```
    - Fedora
        ```
        # grub2-mkconfig -o "$(readlink -e /etc/grub2.conf)"
        ```
    - OpenSUSE
        ```
        # update-bootloader
        ```
    - Ubuntu/Debian, Void Linux
        ```
        # update-grub
        ```
