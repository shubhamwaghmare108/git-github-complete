# Git Internals — Full Lecture

Git is content-addressed. Core objects are blobs, trees, commits and tags.

```text
branch → commit → tree → blob
            ↓
          parent
```

Explore the object database:
```bash
git rev-parse HEAD
git cat-file -t HEAD
git cat-file -p HEAD
git cat-file -p HEAD^{tree}
git count-objects -v
```

A commit records metadata, a root tree and parent commit references. A tree maps names to blobs or subtrees.

### Lab
Create one file, commit it, identify the commit SHA, inspect its tree, then locate the blob containing the file.