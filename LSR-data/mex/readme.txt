/*
 *-----------------------------------------------------------------------*
 * NOTICE:  This code was developed by the US Government.
 * MEX software is distributed only under license agreement
 * from the National Institutes of Health,
 * Laboratory of Sensorimotor Research, Bldg 49 Rm 2A50, MSC-4435,
 * 9000 Rockville Pike, Bethesda, MD, 20892
 * (301) 496-9375.
 *-----------------------------------------------------------------------*
 */

    MEX:  The LSR's real-time Multi-unit Spike Sorter
		Lance M. Optican
		August 2, 1995

MEX is a system used at the LSR to sort spikes from an
electrode in real-time.  It is a combination of hardware
and software that takes as its input the amplified electrode
signal and provides as its output digital messages suitable
for reading by another computer, such as one running the
LSR's REX program.

If you publish any papers based on data collected with MEX,
please cite the paper by Chandra & Optican (see below).

The software consists of two components: programs written in C
for the PC, and programs written in assembler for an AT&T DSP-32.
The MEX software is available free of  charge.  The MEX document
files are in plaintext. However, the MEX program files are
encrypted.  Each user of MEX must complete the simple license
agreement in the file license.doc or license.ps, and return it to
the LSR.  The LSR will then provide a password for decrypting the
MEX files.  Note:  the encryption program is the same one used by
REX, and can be obtained via anonymous ftp from lsr.nei.nih.gov
in the directory "/usr/ftp/rex/crypt".

The LSR provides no warranty, and assumes no liability, for
problems with, or caused by, this software.  Bug reports,
anecdotal experiences, and software upgrade requests may be
sent to the authors (rishi@lsr.nei.nih.gov or lmo@lsr.nei.nih.gov).

-------------------------------------------------------------------------
File descriptions:
	All files are in zip format except for the license agreement
	and this file.

mex5.zip
	Contains all the files necessary to run MEX (compiled).

paper.zip
	Contains the postcript files for the manuscript and figures.

manual.zip
	Contains the MEX users guide in postcript and MS-Word format.

bgi.zip
	Contains graphics files for MEX
  
license.ps
	contain the simple license agreement that each
	MEX user must fill in and return to the LSR.

