# Portage

See configurations in `portage` directory.

### make.conf file

https://wiki.gentoo.org/wiki//etc/portage/make.conf

### Portage features

https://wiki.gentoo.org/wiki/Handbook:AMD64/Working/Features

### repos.conf directory

https://wiki.gentoo.org/wiki//etc/portage/repos.conf

### CPU_FLAGS_X86

```bash
emerge app-portage/cpuinfo2cpuflags
cpuinfo2cpuflags-x86 >> /etc/portage/make.conf
```

# emerge

### Sync

```bash
emerge --sync
```

### Rebuild everything

```bash
emerge -ae @world
```

### Rebuild only needed packages for new/changed use flags

```bash
emerge --ask --deep --changed-use --update @world
```

# layman - gentoo overlays

Install `app-portage/layman` and configure some overlays in `/etc/portage/repos.conf/overlay-name.conf

See some examples in the `portage/repos.conf` directory.


### sync overlays

```bash
layman -S
```

# Other tools

 * `equery`: install `app-portage/gentoolkit`
 * `euse`: install `app-portage/gentoolkit`
 * `eix`: install `app-portage/eix`

### Update eix database

```bash
eix-update
```

### Enable uses for package

```bash
euse -E -p cat/pkg use1 use2 ...
```

### Disable uses for package

```bash
euse -D -p cat/pkg use1 use2 ...
```
