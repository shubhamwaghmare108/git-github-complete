# 02 — Git Internals

Git stores content as objects: blobs, trees, commits and annotated tags. References such as branches point to commits, while `HEAD` identifies the current checkout.

## Explore
```bash
git rev-parse HEAD
git cat-file -t HEAD
git cat-file -p HEAD
git cat-file -t <object>
git cat-file -p <object>
git count-objects -v
```

## Exercise
Create a commit and trace it from branch → commit → tree → blob.