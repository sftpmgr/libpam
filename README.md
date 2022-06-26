# libpam
Patch Debian's PAM to support longer passwords

## Usage

1. Download components which are intended to be installed from GitHub Actions, e.g:

    ```
    wget https://github.com/sftpmgr/libpam/releases/download/UserBuild_2022.06.26_02-09/libpam-modules_1.4.0-9+deb11u1_amd64.deb
    wget https://github.com/sftpmgr/libpam/releases/download/UserBuild_2022.06.26_02-09/libpam-modules-bin_1.4.0-9+deb11u1_amd64.deb
    wget https://github.com/sftpmgr/libpam/releases/download/UserBuild_2022.06.26_02-09/libpam-runtime_1.4.0-9+deb11u1_all.deb
    wget https://github.com/sftpmgr/libpam/releases/download/UserBuild_2022.06.26_02-09/libpam0g_1.4.0-9+deb11u1_amd64.deb
    ```
2. Install downloaded components:

    ```
    sudo dpkg -i libpam-modules_1.4.0-9+deb11u1_amd64.deb
    sudo dpkg -i libpam-modules-bin_1.4.0-9+deb11u1_amd64.deb
    sudo dpkg -i libpam-runtime_1.4.0-9+deb11u1_all.deb
    sudo dpkg -i libpam0g_1.4.0-9+deb11u1_amd64.deb
    ```
    
    or
    
    ```
    sudo dpkg -i *.deb
    ```

