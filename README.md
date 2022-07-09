# sftpmgr libpam
Patch PAM on Debian 11 "bullseye" to support longer passwords (increased from <512 to <4096).

## Usage

1. Download components from GitHub Actions, e.g:

    ```
    wget https://github.com/sftpmgr/libpam/releases/download/UserBuild_2022.06.26_02-09/libpam-modules_1.4.0-9+deb11u1_amd64.deb
    wget https://github.com/sftpmgr/libpam/releases/download/UserBuild_2022.06.26_02-09/libpam-modules-bin_1.4.0-9+deb11u1_amd64.deb
    wget https://github.com/sftpmgr/libpam/releases/download/UserBuild_2022.06.26_02-09/libpam-runtime_1.4.0-9+deb11u1_all.deb
    wget https://github.com/sftpmgr/libpam/releases/download/UserBuild_2022.06.26_02-09/libpam0g_1.4.0-9+deb11u1_amd64.deb
    ```
2. Install downloaded packages, e.g.:

    ```
    sudo dpkg -i libpam-modules_1.4.0-9+deb11u1_amd64.deb
    sudo dpkg -i libpam-modules-bin_1.4.0-9+deb11u1_amd64.deb
    sudo dpkg -i libpam-runtime_1.4.0-9+deb11u1_all.deb
    sudo dpkg -i libpam0g_1.4.0-9+deb11u1_amd64.deb
    ```
    
## Customization

See `.github/workflows/ci.yaml` - this consists of a very simple change to `PAM_MAX_RESP_SIZE` in `libpam/include/security/_pam_types.h`.

## Background

When using PAM's `pam_exec.so` with `expose_authtok` enabled, the password is truncated to 511 octets. More [discussion here](https://github.com/linux-pam/linux-pam/issues/59).

