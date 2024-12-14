---
{"date":null,"dg-publish":true,"source":null,"tags":["linux","utility"],"title":"Archives with Tar","type":"reference","URL":null,"permalink":"/01-reference/software/tar-archive/","dgPassFrontmatter":true}
---


# Archives with Tar

```sh
tar -cvf backup.tar ~/Documents ~/Pictures ~/.dotfiles
```

tar command options:
-c create new archive
-r append files to archive
-v verbose, show progress
-f filename (name of archive)

```sh
tar -xvf backup.tar
```

-x extract
-t list the content of the archive
