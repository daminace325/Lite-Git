# 🚀 Lite-Git

A minimal version of Git built for learning and exploration. `lite` lets you initialize a repo, add/commit files, inspect objects, and simulate basic Git internals.

---

## 📦 Initialization

To initialize a Lite-Git repository:

```bash
~lite init "filename"
```

---

## 📁 Basic Workflow

1. Create a new text file inside any folder.
2. Use the following commands:

```bash
~lite add test_file.txt
~lite commit -m "initial commit"
```

> Run all further commands inside the directory containing the committed file.

---

## 🔀 Checkout

To checkout the current `master` branch into a new empty directory:

```bash
mkdir new_empty_directory
~lite checkout master ~/new_empty_directory
```

---

## 🌲 List Tree

To list the tree structure of the current commit:

```bash
~lite ls-tree -r HEAD
```

---

## 🔍 Inspect an Object

To inspect a blob (file) object using its hash:

```bash
~lite cat-file blob <hash>
```

> You can get the `<hash>` from the `ls-tree` command output.

---

## 🔗 rev-parse

Navigate to a valid Lite-Git repository and run:

```bash
~lite rev-parse --wyag-type commit HEAD   # Hash of commit object HEAD points to
~lite rev-parse --wyag-type tree HEAD     # Hash of tree object associated with HEAD
~lite rev-parse --wyag-type tag HEAD      # Tag object hash (if any), else returns None
```

---

## 📄 Ignored Files & Status

Navigate to a Lite-Git repo with a tracked `.gitignore` file:

### Check Ignored Files

```bash
~lite check-ignore <file-name>
```

> Prints `<file-name>` if it's ignored (based on `.gitignore` rules).

### Check Status

```bash
~lite status
```

---

## ➕ Add & Commit

### Add Files

```bash
~lite add <file-name>
```

### Commit Changes

```bash
~lite commit -m "your commit message"
```

---

## 🧠 Notes

- All commands assume you're in a directory initialized with `~lite init`.
- Commands mimic the behavior of Git, but are simplified and for educational purposes.
```

---

Let me know if you want to add a demo section, contribution guide, or license info.
