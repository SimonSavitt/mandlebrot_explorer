# mandlebrot_explorer

## Purpose:
The purpose of this program is to be an easy to use fractal explorer and a demo of interactivity using the SDL2 library.

## DependancieS:
To install this program, one must have *SDL2* (available from their website or most package managers) and must have lpthreads (default on most POSIX systems)

## Compile & Install:
Clone the repository and run **make && make install** from the *src/* directory. 
This will compile the program and copy it to your **$PATH**, and install the man page.
Depending on your system, *make install* may require administrative privileges.


    $ make && make install

To uninstall the program, run:

    $ make clean && make uninstall

## Usage:

Run the program, you can then use the:

arrow keys to pan 

+/- to zoom. 

[ / ] to increase or decrease the amount of iterations done

Q to quit

H toggles to 'histogram view'

M toggles to 'modulo view'

R to reset your view


Currently Histogram view looks poor, but I think the concept is good and efforts will be made to improve it.
Efforts will also be made to have seperate keybindings for smooth / coarse zoom and pan

### Customization:

To customize, copy *src/config.cpp.def* into *src/config.cpp* and make your edits there

*src/config.cpp* is in the .gitignore, so you can edit without worrying about syncing with the repo.

However, beware when you pull if there are changes that will cause your *src/config.cpp* to become incompatable.

In the file, you can modify the color palette, num threads, pixelWidth, etc.

It should be fairly self explanatory.

After customizing, you must re-run make and make install, but it should be fairly quick because only a few cosntants were changed.

##  TODO:
1)  Allow easier customazation than changing source code
2)  Have a better interface to scroll multiple steps at once, 
    perhaps click and drag and/or boxes to type in Xmin/Xmax Ymin/Tmax
3)  More intillegently setup a color gradient. Now histogram is easy to looks good at some zoom levels but garbage at others
    More intellegent "bucket" placing for histogram
4)  More intellegently split work between threads, rather than having each take a stripe.
    Maybe guess where the most work would need to be done?

## Examples Images

Depending on what you are looking for, both the Historgram and Modulo renderings can look nice. However, the Histogram rendering tends
to be more consistently nice. Here are some comparisons:


Modulo:
![Modulo 1]( /screenshots/modulo1.png?raw=true) 

Histogram:
![Histogram 1]( /screenshots/histogram1.png?raw=true) 

Modulo:
![Modulo 2](/screenshots/modulo2.png?raw=true)

Histogram
![Histogram 2](/screenshots/histogram2.png?raw=true)

Here are some extras (all with histogram):

Spiral
![Spiral 1]( /screenshots/spiral1.png?raw=true) 

Minibrot
![Minibrot 1]( /screenshots/minibrot1.png?raw=true) 

Minibrot
![Minibrot 2](/screenshots/minibrot2.png?raw=true)