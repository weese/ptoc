#
# $Id: Makefile,v 0.1 1993/12/10 01:24:53 king Exp king $
#
SRC = _graphfreemem.c _graphgetmem.c arc.c bar.c bar3d.c circle.c\
	cleardevice.c clearviewport.c closegraph.c detectgraph.c drawpoly.c\
	ellipse.c fillellipse.c fillpoly.c floodfill.c\
	getarccoords.c getaspectratio.c getbkcolor.c getch.c getcolor.c\
	getdate.c getdefaultpalette.c getdrivername.c getfillpattern.c\
	getfillsettings.c getgraphmode.c getimage.c getlinesettings.c\
	getmaxcolor.c getmaxmode.c getmaxx.c getmaxy.c getmodename.c\
	getmoderange.c getpalette.c getpalettesize.c getpixel.c\
	gettextsettings.c getviewsettings.c getx.c gety.c graphdefaults.c\
	grapherrormsg.c graphresult.c imagesize.c initgraph.c\
	installuserdriver.c installuserfont.c kbhit.c line.c linerel.c lineto.c\
	moverel.c moveto.c outtext.c outtextxy.c pieslice.c putimage.c\
	putpixel.c rectangle.c registerbgidriver.c registerbgifont.c\
	restorecrtmode.c rotated.c sector.c setactivepage.c setallpalette.c\
	setaspectratio.c setbkcolor.c setcolor.c setfillpattern.c\
	setfillstyle.c setgraphbufsize.c setgraphmode.c setlinestyle.c\
	setpalette.c setrgbpalette.c settextjustify.c settextstyle.c\
	setusercharsize.c setviewport.c setvisualpage.c setwritemode.c\
	textheight.c textwidth.c delay.c

OBJ = _graphfreemem.o _graphgetmem.o arc.o bar.o bar3d.o circle.o\
	cleardevice.o clearviewport.o closegraph.o detectgraph.o drawpoly.o\
	ellipse.o fillellipse.o fillpoly.o floodfill.o\
	getarccoords.o getaspectratio.o getbkcolor.o getch.o getcolor.o\
	getdate.o getdefaultpalette.o getdrivername.o getfillpattern.o\
	getfillsettings.o getgraphmode.o getimage.o getlinesettings.o\
	getmaxcolor.o getmaxmode.o getmaxx.o getmaxy.o getmodename.o\
	getmoderange.o getpalette.o getpalettesize.o getpixel.o\
	gettextsettings.o getviewsettings.o getx.o gety.o graphdefaults.o\
	grapherrormsg.o graphresult.o imagesize.o initgraph.o\
	installuserdriver.o installuserfont.o kbhit.o line.o linerel.o lineto.o\
	moverel.o moveto.o outtext.o outtextxy.o pieslice.o putimage.o\
	putpixel.o rectangle.o registerbgidriver.o registerbgifont.o\
	restorecrtmode.o rotated.o sector.o setactivepage.o setallpalette.o\
	setaspectratio.o setbkcolor.o setcolor.o setfillpattern.o\
	setfillstyle.o setgraphbufsize.o setgraphmode.o setlinestyle.o\
	setpalette.o setrgbpalette.o settextjustify.o settextstyle.o\
	setusercharsize.o setviewport.o setvisualpage.o setwritemode.o\
	textheight.o textwidth.o delay.o

LIB = ../libXbgi.a

# C compiler
CC = gcc
CFLAGS = -O2 -g
AR = ar
ARFLAGS = rc
X11BASE = /usr/X11R6


.c.o:
	$(CC) $(CFLAGS) -I$(X11BASE)/include -c $<

../libXbgi.a: $(OBJ)
	$(AR) $(ARFLAGS) $(LIB) $(OBJ)

demo: demo.c
	gcc -O -g -o demo demo.c ../libXbgi.a -L$(X11BASE)/lib -lX11 -lm

clean:
	rm -f $(OBJ) *~ usleep.o demo

usleep.o: usleep.c
	gcc -c -D_BSD_SIGNALS -DC usleep.c


