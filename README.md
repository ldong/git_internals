# Git

Author: Lin Dong

Date: Sat Feb 27 15:54:32 PST 2016

Place: CMU-SV
## Note

This is NOT about how to use git or github, it is about how git is designed and used internally

## Commonly used git commands

* init
* commit
* branch
* merge

In forms of: commit, tree, blobs

## Revision Control
Perks:

1. Distributed Database
2. Fast, Scalable and Distributed (no single point of failure)

## Git version database
1. Content addressable file system
2. Simple key-value data store
3. Everything has a SHA-1 hash
4. Value - binary files: commits, trees, blobs(Binary Large OBject)

## Git structure

1. `.git` structure

```
├── HEAD
├── config
├── description
├── hooks
│   ├── applypatch-msg.sample
│   ├── commit-msg.sample
│   ├── post-update.sample
│   ├── pre-applypatch.sample
│   ├── pre-commit.sample
│   ├── pre-push.sample
│   ├── pre-rebase.sample
│   ├── prepare-commit-msg.sample
│   └── update.sample
├── info
│   └── exclude
├── objects
│   ├── info
│   └── pack
└── refs
    ├── heads
    └── tags

8 directories, 13 files
```

## Git cat-file
1. Type: `git cat-file -t 3b18`
2. Size: `git cat-file -s 3b18`
3. Hash object: `echo 'Hello world'  | git hash-object --stdin`
4. Limited file size


## Reference
1. [Git Internals](https://git-scm.com/book/en/v1/Git-Internals)
2. [Git Internals - Plumbing and Porcelain](https://git-scm.com/book/en/v2/Git-Internals-Plumbing-and-Porcelain)
