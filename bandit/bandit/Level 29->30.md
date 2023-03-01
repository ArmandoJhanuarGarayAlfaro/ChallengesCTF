
## Objetivo
There is a git repository at `ssh://bandit29-git@localhost/home/bandit29-git/repo`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

Clone the repository and find the password for the next level.
## Datos Acceso
bandit29
tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S

## Solucion
```bash
bandit29@bandit:~$ mktemp -d
/tmp/tmp.ozSVykGG2X
bandit29@bandit:~$ cd /tmp/tmp.ozSVykGG2X
bandit29@bandit:/tmp/tmp.ozSVykGG2X$ git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo
Cloning into 'repo'...
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit29/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit29/.ssh/known_hosts).
                         _                     _ _ _   
                        | |__   __ _ _ __   __| (_) |_ 
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_ 
                        |_.__/ \__,_|_| |_|\__,_|_|\__|
                                                       

                      This is an OverTheWire game server. 
            More information on http://www.overthewire.org/wargames

bandit29-git@localhost's password: 
remote: Enumerating objects: 16, done.
remote: Counting objects: 100% (16/16), done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 16 (delta 2), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (16/16), done.
Resolving deltas: 100% (2/2), done.
bandit29@bandit:/tmp/tmp.ozSVykGG2X$ ls -la
total 104
drwx------   3 bandit29 bandit29  4096 Feb 25 23:48 .
drwxrwx-wt 867 root     root     98304 Feb 25 23:49 ..
drwxrwxr-x   3 bandit29 bandit29  4096 Feb 25 23:48 repo
bandit29@bandit:/tmp/tmp.ozSVykGG2X$ cd repo/
bandit29@bandit:/tmp/tmp.ozSVykGG2X/repo$ ls
README.md
bandit29@bandit:/tmp/tmp.ozSVykGG2X/repo$ cat README.md 
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: <no passwords in production!>

bandit29@bandit:/tmp/tmp.ozSVykGG2X/repo$ git log
commit 0afe3501277395fbfa017480925edee3df6e8bb5 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:11 2023 +0000

    fix username

commit c2606dfc0aef7179bf1ccd6cffa9ed19151facb4
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:11 2023 +0000

    initial commit of README.md
bandit29@bandit:/tmp/tmp.ozSVykGG2X/repo$ git shoe2606dfc0aef7179bf1ccd6cffa9ed19151facb4
git: 'shoe2606dfc0aef7179bf1ccd6cffa9ed19151facb4' is not a git command. See 'git --help'.
bandit29@bandit:/tmp/tmp.ozSVykGG2X/repo$ git show c2606dfc0aef7179bf1ccd6cffa9ed19151facb4
commit c2606dfc0aef7179bf1ccd6cffa9ed19151facb4
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:11 2023 +0000

    initial commit of README.md

diff --git a/README.md b/README.md
new file mode 100644
index 0000000..2da2f39
--- /dev/null
+++ b/README.md
@@ -0,0 +1,8 @@
+# Bandit Notes
+Some notes for bandit30 of bandit.
+
+## credentials
+
+- username: bandit29
+- password: <no passwords in production!>
+
bandit29@bandit:/tmp/tmp.ozSVykGG2X/repo$ git log
commit 0afe3501277395fbfa017480925edee3df6e8bb5 (HEAD -> master, origin/master, origin/HEAD)
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:11 2023 +0000

    fix username

commit c2606dfc0aef7179bf1ccd6cffa9ed19151facb4
Author: Ben Dover <noone@overthewire.org>
Date:   Tue Feb 21 22:03:11 2023 +0000

    initial commit of README.md
bandit29@bandit:/tmp/tmp.ozSVykGG2X/repo$ git show afe3501277395fbfa017480925edee3df6e8bb5
fatal: ambiguous argument 'afe3501277395fbfa017480925edee3df6e8bb5': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'
bandit29@bandit:/tmp/tmp.ozSVykGG2X/repo$ git branch -a
* master
  remotes/origin/HEAD -> origin/master
  remotes/origin/dev
  remotes/origin/master
  remotes/origin/sploits-dev
bandit29@bandit:/tmp/tmp.ozSVykGG2X/repo$ git checkout dev
Branch 'dev' set up to track remote branch 'dev' from 'origin'.
Switched to a new branch 'dev'
bandit29@bandit:/tmp/tmp.ozSVykGG2X/repo$ ls
code  README.md
bandit29@bandit:/tmp/tmp.ozSVykGG2X/repo$ cat README.md 
# Bandit Notes
Some notes for bandit30 of bandit.

## credentials

- username: bandit30
- password: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS


```
## Notas adicionales
| comando |  descripcion|
|---|----|
|git checkout|change branch|



## Referencias



