# Makefile for fs

# Directories
u = /usr
i = $u/include
s = $i/sys
h = $i/minix

# Programs, flags, etc.
CC =	exec cc
CFLAGS = -I$i
LDFLAGS = -i

OBJ =	main.o open.o read.o write.o pipe.o \
	device.o path.o mount.o link.o super.o inode.o \
	cache.o cache2.o filedes.o stadir.o protect.o time.o \
	lock.c misc.o utility.o table.o putk.o list.o hash.o \
	semaphore.o semaphore2.o

fs:	$(OBJ)
	$(CC) -o $@ $(LDFLAGS) $(OBJ)
	install -S 512w $@

all install:	# Nothing.

clean:
	rm -f *.o *.bak fs

# Dependencies
a=	fs.h $h/config.h $s/types.h $h/const.h $h/type.h \
	$i/limits.h $i/errno.h $i/ansi.h $h/syslib.h \
	const.h type.h proto.h glo.h $s/dir.h $i/semaphore.h \
	list.h hash.h

cache.o:	$a
cache.o:	$h/com.h
cache.o:	$h/boot.h
cache.o:	buf.h
cache.o:	file.h
cache.o:	fproc.h
cache.o:	super.h

cache2.o:	$a
cache2.o:	$h/com.h
cache2.o:	$h/boot.h
cache2.o:	buf.h

device.o:	$a
device.o:	$i/fcntl.h
device.o:	$h/callnr.h
device.o:	$h/com.h
device.o:	dev.h
device.o:	file.h
device.o:	fproc.h
device.o:	inode.h
device.o:	param.h

filedes.o:	$a
filedes.o:	file.h
filedes.o:	fproc.h
filedes.o:	inode.h

inode.o:	$a
inode.o:	$h/boot.h
inode.o:	buf.h
inode.o:	file.h
inode.o:	fproc.h
inode.o:	inode.h
inode.o:	super.h

link.o:	$a
link.o:	$s/stat.h
link.o:	$i/string.h
link.o:	$h/callnr.h
link.o:	buf.h
link.o:	file.h
link.o:	fproc.h
link.o:	inode.h
link.o:	param.h
link.o:	super.h

lock.o:	$a
lock.o:	$i/fcntl.h
lock.o:	$i/unistd.h
lock.o:	file.h
lock.o:	fproc.h
lock.o:	inode.h
lock.o:	lock.h
lock.o:	param.h

main.o:	$a
main.o:	$i/fcntl.h
main.o:	$i/string.h
main.o:	$s/ioctl.h
main.o:	$h/callnr.h
main.o:	$h/com.h
main.o:	$h/boot.h
main.o:	buf.h
main.o:	dev.h
main.o:	file.h
main.o:	fproc.h
main.o:	inode.h
main.o:	param.h
main.o:	super.h

misc.o:	$a
misc.o:	$i/fcntl.h
misc.o:	$i/unistd.h
misc.o:	$h/callnr.h
misc.o:	$h/com.h
misc.o:	$h/boot.h
misc.o:	buf.h
misc.o:	file.h
misc.o:	fproc.h
misc.o:	inode.h
misc.o:	dev.h
misc.o:	param.h

mount.o:	$a
mount.o:	$i/fcntl.h
mount.o:	$h/com.h
mount.o:	$s/stat.h
mount.o:	buf.h
mount.o:	dev.h
mount.o:	file.h
mount.o:	fproc.h
mount.o:	inode.h
mount.o:	param.h
mount.o:	super.h

open.o:	$a
open.o:	$s/stat.h
open.o:	$i/fcntl.h
open.o:	$h/callnr.h
open.o:	$h/com.h
open.o:	buf.h
open.o:	dev.h
open.o:	file.h
open.o:	fproc.h
open.o:	inode.h
open.o:	lock.h
open.o:	param.h

path.o:	$a
path.o:	$i/string.h
path.o:	$h/callnr.h
path.o:	buf.h
path.o:	file.h
path.o:	fproc.h
path.o:	inode.h
path.o:	super.h

pipe.o:	$a
pipe.o:	$i/fcntl.h
pipe.o:	$i/signal.h
pipe.o:	$h/boot.h
pipe.o:	$h/callnr.h
pipe.o:	$h/com.h
pipe.o:	dev.h
pipe.o:	file.h
pipe.o:	fproc.h
pipe.o:	inode.h
pipe.o:	param.h

protect.o:	$a
protect.o:	$i/unistd.h
protect.o:	$h/callnr.h
protect.o:	buf.h
protect.o:	file.h
protect.o:	fproc.h
protect.o:	inode.h
protect.o:	param.h
protect.o:	super.h

putk.o:	$a
putk.o:	$h/com.h

read.o:	$a
read.o:	$i/fcntl.h
read.o:	$h/com.h
read.o:	buf.h
read.o:	file.h
read.o:	fproc.h
read.o:	inode.h
read.o:	param.h
read.o:	super.h

stadir.o:	$a
stadir.o:	$s/stat.h
stadir.o:	file.h
stadir.o:	fproc.h
stadir.o:	inode.h
stadir.o:	param.h

super.o:	$a
super.o:	$i/string.h
super.o:	$h/boot.h
super.o:	buf.h
super.o:	inode.h
super.o:	super.h

table.o:	$a
table.o:	$h/callnr.h
table.o:	$h/com.h
table.o:	buf.h
table.o:	dev.h
table.o:	file.h
table.o:	fproc.h
table.o:	inode.h
table.o:	lock.h
table.o:	super.h

time.o:		$a
time.o:		$h/callnr.h
time.o:	$h/com.h
time.o:	file.h
time.o:	fproc.h
time.o:	inode.h
time.o:	param.h

utility.o:	$a
utility.o:	$h/com.h
utility.o:	$h/boot.h
utility.o:	$i/unistd.h
utility.o:	buf.h
utility.o:	file.h
utility.o:	fproc.h
utility.o:	inode.h
utility.o:	param.h

write.o:	$a
write.o:	$i/string.h
write.o:	buf.h
write.o:	file.h
write.o:	fproc.h
write.o:	inode.h
write.o:	super.h

semaphore.o:	$a
semaphore2.o:   $a

list.o:		list.h
hash.o:		hash.h
