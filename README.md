# SCM-Manager patches for jgit

This repository contains pathes for the usage of
[jgit](https://www.eclipse.org/jgit/) in [SCM-Manager](https://scm-manager.org/).
These patches can be applied using [guilt](https://github.com/jeffpc/guilt).

## How To

To apply these patches, first clone the forked repository of jgit:

```
git clone git@github.com:scm-manager/jgit.git
cd jgit
```

Then clone this repository in the patches directory in `.git`:

```
git clone git@github.com:scm-manager/jgit-patches.git .git/patches
```

Finally apply the patches with guilt:

```
guilt push -a
```

__Do not push these applied patches to the jgit repository!__

To create a new patch. call this **before** you make any changes:

```
guilt new patch-name
```

Then make your changes and call this to update the patch:

```
guilt refresh
```

This new patch can then be added to the patch repository and pushed.
