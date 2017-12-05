# bedtools-local-install 
This repository shows how to install bedtools locally on your Sofia account 

First download the latest source code of bedtools into your bin folder: \
\
$ cd $HOME/bin #if you get an error, create the folder using: mkdir $HOME/bin \
$ wget https://github.com/arq5x/bedtools2/releases/download/v2.26.0/bedtools-2.26.0.tar.gz \
$ tar -zxvf bedtools-2.25.0.tar.gz \
$ cd bedtools2 \
\
Change the line 25 of Makefile using a text editor as nano or vi: \
\
export LIBS             = -lz #original \
export LIBS             =/usr/local/lib/libz.so.1.2.11 -lz #new line, added path for zlib package \
\
$ make \
\
A succeful instalation create a new directorie called bin (see with ls) where the binaries files are allocated. \
Finally export the full path of binaries using your bash profile file: \
\
export PATH=$PATH:$PWD/bin #also add to ~/.bash_profile 

