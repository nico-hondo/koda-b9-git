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
    - **commit**
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
6. **remote** - Melakukan pendaftaran repository remote ke repo lokal
```bash
    <!-- Penambahan Remote -->
    $ git remote add <name_remote> <link_remote(.git)>
    <!-- Melihat list remote -->
    $ git remote [-v | --verbose]
```
7. **push** - sinkronisasi dari lokal ke remote.
```bash
    $ git push [-u | --set-upstream] <nama-remote> <nama-branch>
```
8. **pull** - sinkronisasi dari remote ke lokal
```bash
    $ git pull <nama-remote> <nama-branch>
```
9. **clone** - Menyalin repo remote ke repo lokal
```bash
    $ git clone <link-remote(.git)> <nama-folder-baru>(opsi)
```
10. **reset** - Mundur ke commit tertentu
```bash
<!-- cari tau commit-id melalui log/reflog -->
$ git log
$ git reflog
<!-- lakukan reset -->
$ git reset <commit-id>
```
11. **revert** - "menghilangkan" commit
```bash
    <!-- cari tau commit-id melalui log/reflog -->
    $ git log
    $ git reflog
    <!-- lakukan revert -->
    $ git revert <commit-id>
```