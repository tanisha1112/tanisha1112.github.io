---
layout: single
title:  "Bash"
date:   2020-06-15 20:16:01 -0600
author_profile: false
excerpt_separator: "<!--more-->"
---

This is a bash cheatsheet for all the tricks I learnt
<!--more-->


## GPU related

Find out the models of the GPUs
```sh
$ lspci | grep -i --color 'vga\|3d\|2d'
```

Get GPUs status
```sh
$ nvidia-smi

```
or 
```sh
$ watch nvidia-smi
```

htop:
```sh
$ htop
```
storage:
```sh
$ du
```

## Processes handling

Check the processes running
```sh
$ ps aux | grep X 
```

Kill a process using its PID
```sh
$ kill -9 PID
```

## Remote control

Find IP address
```sh
$ hostname -I
```
or
```sh
$ ifconfig
```

Copy from local to ssh
```sh
$ scp (-r) 
```
To visualize the GUI 
```sh
$ ssh -X hostname@192.168.XXX.X
```
Once inside:
```sh
$ nautilus
```
## Multiple Screens

```sh
$ tmux new -s session_name
Ctrl+b d
```

To reattach to a tmux session
```sh
$ tmux attach-session -t tmuxID
```

```sh
$ screen -S
ctrl A +D 
```

To reattach to a screen 
```sh
$ screen -r screenID
```

## Unzip

Unzip tar files
```sh
$ tar -xvf file.tar
```

Unzip tar.gz files
```sh
$ tar zxvf file.tar.gz
```

# Other

Number of files in a repository/file
```sh
$ ls -1 | wc -l
$ wc -l <filename>
```
