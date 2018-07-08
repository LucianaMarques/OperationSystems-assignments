# OperationSystems-assignments

Command-line cheat-sheet

1) Build Docker

1/docker$ docker build -t tiagoshibata/pcs3746 .

2) Kill Docker

1/initramfs$ ps docker

1/initramfs$ docker kill [NAME]

3) Run Docker

1$ docker run -ti --rm -v "$PWD/linux":/home/student/src/linux -v "$PWD/initramfs":/home/student/src/initramfs tiagoshibata/pcs3746

4) Communicate qemu and run gdb

1/initramfs$ docker ps
1/initramfs$ docker exec -ti [NAME] bash
root:/$ su student
student:/$ ps ax
student:/$ alias
student:/$ gdb

5) Use busybox
cd initramfs
initramfs$ vim cmd_default.sh
(erase -S -s)

build docker again

Run as:
1$ docker run -ti --rm -v "$PWD/linux":/home/student/src/linux -v "$PWD/../3/initramfs":/home/student/src/initramfs tiagoshibata/pcs3746

