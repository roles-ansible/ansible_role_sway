[![Ansible Galaxy](https://ansible.l3d.space/svg/roles-ansible.sway.svg)](https://galaxy.ansible.com/ui/standalone/roles/roles-ansible/sway)
[![MIT License](https://ansible.l3d.space/svg/roles-ansible.sway_license.svg)](LICENSE)
[![Maintainance](https://ansible.l3d.space/svg/roles-ansible.sway_maintainance.svg)](https://ansible.l3d.space/#roles-ansible.sway)

SWAY Window Manager - ansible role
=========================================

[![SWAYWM](https://swaywm.org/logo.png)](https://swaywm.org/)
Sway is a tiling Wayland compositor and a drop-in replacement for the i3 window manager for X11. It supports most of i3's features, plus a few extras.

Sway allows you to arrange your application windows logically, rather than spatially. Windows are arranged into a grid by default which maximizes the efficiency of your screen and can be quickly manipulated using only the keyboard.

With this ansible role you deploy a sway configuration with optionally swaylock, waybar and fuzzel.

## Variables
| Variable | Value | Description |
| -------- | ----- | ----------- |
| ``sway__user_list`` | *(see [defaults/main.yml](defaults/main.yml)* | A list of all users and their home directory |
| ``sway__dynamic_names`` | ``false`` | 
| ``sway__logo_key`` | ``Mod4`` | Logo Key |
| ``sway__term`` | ``foot`` | Sway default terminal |
| ``sway__reload`` | ``$mod+Shift+r`` | Key binding to reload sway config |
| ``sway__term_pkgs | *(see [defaults/main.yml](defaults/main.yml)* | Packages for sway terminal |
| ``sway__keyboard_settings`` | ``true`` | Set Keyboard language settings in sway config |
| ``sway__keyboard_lang`` | ``de`` | German |
| ``sway__lock`` | *(see [defaults/main.yml](defaults/main.yml)* | Kommand to run for locking sway |
| ``sway__swaylock`` |  *(see [defaults/main.yml](defaults/main.yml)*  | Default swaylock settings |
| ``sway__waybar`` | ``true`` | Enable waybar as bar |
| ``sway__waybar_modules_left`` | *(see [defaults/main.yml](defaults/main.yml)* | Left waybar modules |
| ``sway__waybar_modules_center`` | *(see [defaults/main.yml](defaults/main.yml)* | Center waybar modules |
| ``sway__waybar_modules_right`` | *(see [defaults/main.yml](defaults/main.yml)* | Right waybar modules |
| ``sway__launcher`` | ``fuzzel`` | Command for launcher |
| ``sway__install_launcher`` | ``['fuzzel']`` | List for launcher packages |
| ``sway__waybar_font_size`` | ``13px`` | Waybar font size |
| ``sway__waybar_light_up`` | ``light -A 1`` | Waybar light module |
| ``sway__waybar_light_down`` | ``light -U 1`` | Waybar  light module |
| ``sway__wlsunset`` | ``true`` | Enable wlsunset |
| ``sway__wlsunset_params`` | ``-l 49 -L 8.4`` |
| ``sway__keybindings`` | *(see [defaults/main.yml](defaults/main.yml)* | List of sway keybindings |
| ``sway__keybindings_extra`` | ``[]`` | Empty list for additional keybindings |
| ``sway__pipewire`` | ``[]`` | Install some requirements for desktop sharing... |
| ``sway__notification_center`` | ``true`` | Use way notification center for notifications |
| ``submodules_versioncheck`` | ``false`` | Basic Versionscheck to prevent running older version of this role |



## Example Playbook
```yaml
 - name: install sway on localhost
   hosts: localhost
   roles:
     - {role: roles-ansible.sway, tags: sway}
```

## License
[![MIT License](https://ansible.l3d.space/svg/roles-ansible.sway_license.svg)](LICENSE)
