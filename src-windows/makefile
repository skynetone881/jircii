#
# Compile jircii.exe frontend...
# Based off of a makefile generated by the LCC Suite
# http://www.cs.virginia.edu/~lcc-win32
#
# Usage:
# set PATH=%PATH%;c:\lcc\bin
# make
#
LCCROOT=c:\lcc
CFLAGS=-I$(LCCROOT)\include 
CC=$(LCCROOT)\bin\lcc.exe
LINKER=$(LCCROOT)\bin\lcclnk.exe
OBJS=jircii.res jircii.obj
LIBS=SHELL32.LIB

jircii.exe:	$(OBJS) Makefile
	$(LINKER) -s -subsystem windows -o bin\jircii.exe $(OBJS) $(LIBS)

jircii.res:	src\jirciires.h src\jicon32x32.ico src\jircii.rc
	$(LCCROOT)\bin\lrc.exe -Isrc\ -I$(LCCROOT)\include  src\jircii.rc

jircii.obj:	src\jirciires.h src\jircii.c
	$(CC) -c $(CFLAGS) src\jircii.c

link:	$(OBJS)
	$(LINKER)  -s -subsystem windows -o bin\jircii.exe $(OBJS) $(LIBS)

clean:	bin\jircii.exe
	del $(OBJS) bin\jircii.obj bin\jircii.exe




