## Fork of kde-kit 

overlay with some updates.

## with local overlays

[Local overlays](https://www.funtoo.org/Local_Overlay) should be managed via `/etc/portage/repos.conf/`.
create a `/etc/portage/repos.conf/kde-kit-beta.conf` file containing precisely:

```
[kde-kit-beta]
location = /usr/local/portage/kde-kit-beta
sync-type = git
sync-uri = https://github.com/adioskid/kde-kit-beta.git
priority= 99
```

Afterwards, simply run `ego sync`, and Portage should seamlessly make all our ebuilds available.

## with layman

Invoke the following:

```
# layman -o https://raw.github.com/adioskid/kde-kit-beta/master/repositories.xml -f -a kde-kit-beta
```