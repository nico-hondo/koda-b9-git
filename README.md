1. **init** - Inisialisasi direktori kerja git

```bash
$ git init
```

2. **status** - melihat kondisi direktori kerja git

```bash
$ git status
```
3. **add** - menambahkan ke staging area(perubahan sementara).
staging area digunakan untuk mengelompokkan perubahan-perubahan yang seragam

```bash
$ git add <file/folder>
$ git add ./README.md atau .src atau .
```

4. **unstage** - mengeluarkan dari staging are
```bash
$ git status //mengecek apa saja yang ada di staging
$ git rm --cached <file/folder>...
```

5. **commit** - penyimpanan permanen. Gunakan tata cara pembuatan pesan di conventional commit. Format ``type[scope]: message``
    - setup your information
        ```bash
            $ git config set --global user.email "youremail@yahoo.co.id"
            $ git config set --global user.name "nico-hondo"
        ```
    - commit
        ```bash
            // long message
            $ git commit
            // short message
            $ git commit -m "type[scope]: message"
        ```
    - **log**, pengecekan history
        ```bash
            $ git log
        ```