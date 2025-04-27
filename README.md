
# What is this

A simple shell script that detect words in git staged files.

You can use this in git pre-commit hook.



# Usage

```sh
git-word-harpooner <WORD> [WORD ...]
```

# Example

```sh

$ git ls-files
staged-file1.txt
staged-file2.txt

$ cat ./staged-file1.txt
This file was staged, but contains a secret word
secret secret
secret

$ git-word-harpooner secret
staged-file1.txt:This file was staged, but contains a secret word
staged-file1.txt:secret secret
staged-file1.txt:secret


```

