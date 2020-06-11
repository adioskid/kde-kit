## Fork of KDE-kit 

overlay with some updates.

## with local overlays

[Local overlays](https://www.funtoo.org/Local_Overlay) should be managed via `/etc/portage/repos.conf/`.
create a `/etc/portage/repos.conf/kde-kit.conf` file containing precisely:

```
[kde-kit]
location = /usr/local/portage/kde-kit
sync-type = git
sync-uri = https://github.com/lucascouts/kde-kit.git
priority= 99
```
#### then change to new branch.
```
# cd /usr/local/portage/kde-kit && git checkout prime
```

Afterwards, simply run `ego sync`, and Portage should seamlessly make all our ebuilds available.

## with layman

Invoke the following:

```
# layman -o https://raw.github.com/lucascouts/kde-kit/master/repositories.xml -f -a kde-kit
```