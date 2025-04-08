# CBT014
Converted to GitHub via [cbt2git](https://github.com/wizardofzos/cbt2git)

This is still a work in progress. GitHub repos will be deleted and created during this period...

```
//***FILE 014 is from Sam Golob and contains a series of articles   *   FILE 014
//*           written for Technical Support magazine of NaSPA.      *   FILE 014
//*           This file is in IEBUPDTE SYSIN format.  For           *   FILE 014
//*           additional information, see the member called         *   FILE 014
//*           $$$INTRO.  These are Sam's older articles.  (See      *   FILE 014
//*           File 120 for the collection of Sam's "MVS Tools and   *   FILE 014
//*           Tricks of the Trade" columns, plus newer articles     *   FILE 014
//*           that were not published by NaSPA.)                    *   FILE 014
//*                                                                 *   FILE 014
//*           email:  sbgolob@cbttape.org                           *   FILE 014
//*                                                                 *   FILE 014
//*           This file now contains an IEFACTRT exit that (it      *   FILE 014
//*           is believed) can replace the I/O Count system         *   FILE 014
//*           modification, on modern systems.                      *   FILE 014
//*                                                                 *   FILE 014
//*           Even better, Greg Price's IEFU83 exit (included       *   FILE 014
//*           here as member $$IEFU83), will show a lot of          *   FILE 014
//*           information as well.  See member IOCOUN$$ for         *   FILE 014
//*           more detail about this package.                       *   FILE 014
//*                                                                 *   FILE 014
//*           THIS FILE CONSISTS OF ARTICLES SUBMITTED BY SAM       *   FILE 014
//*           GOLOB TO "TECHNICAL SUPPORT" MAGAZINE OF NASPA,       *   FILE 014
//*           THE NATIONAL SYSTEMS PROGRAMMERS ASSOCIATION,         *   FILE 014
//*           THAT WAS HEADQUARTERED IN MILWAUKEE, WISCONSIN.       *   FILE 014
//*           (NOW IT IS RUN BY LEO WROBEL, AND IT IS IN TEXAS.)    *   FILE 014
//*                                                                 *   FILE 014
//*           THE MATERIAL PERTAINS LARGELY TO PROGRAMS ON THE CBT  *   FILE 014
//*           TAPE, AND TO TOPICS OF GENERAL SYSTEMS PROGRAMMER     *   FILE 014
//*           INTEREST.  WITH THE KIND PERMISSION OF BOB BECKER,    *   FILE 014
//*           FORMER EDITOR OF "TECHNICAL SUPPORT", THEY ARE BEING  *   FILE 014
//*           DISTRIBUTED WITH THE CBT TAPE TO FURTHER THE          *   FILE 014
//*           USEFULNESS OF OTHER FILES ON THE TAPE, AND THE TAPE   *   FILE 014
//*           IN GENERAL.                                           *   FILE 014
//*                                                                 *   FILE 014
//*           @PDSART0 - @PDSART3 - My tutorial on the PDS command  *   FILE 014
//*                        circa 1989.  Even then, there were at    *   FILE 014
//*                        least 60 subcommands in PDS.  I spent    *   FILE 014
//*                        probably 400 hours on the phone with     *   FILE 014
//*                        (the late) Bruce Leland, and probably    *   FILE 014
//*                        200 hours on the phone with Steve Smith, *   FILE 014
//*                        to learn all the details.  Since 1997,   *   FILE 014
//*                        John Kalinich has enhanced this product  *   FILE 014
//*                        a lot more, although this stuff, which   *   FILE 014
//*                        is described here, still works just as   *   FILE 014
//*                        well.  PDS is an enormously useful       *   FILE 014
//*                        product, and it saves tons of work time. *   FILE 014
//*                        You will do yourselves a great favor,    *   FILE 014
//*                        the more you learn how to use it.        *   FILE 014
//*                                                                 *   FILE 014
//*           CBTCNR1   -  A COLUMN ON USEFUL PROGRAMS ON THE CBT   *   FILE 014
//*                          TAPE.  INSTALLMENT 1.                  *   FILE 014
//*                                                                 *   FILE 014
//*           CBTCNR2   -  A COLUMN ON USEFUL PROGRAMS ON THE CBT   *   FILE 014
//*                          TAPE.  INSTALLMENT 2.                  *   FILE 014
//*                                                                 *   FILE 014
//*           CBTINTRO  -  AN INTRODUCTION TO THE CBT TAPE IN       *   FILE 014
//*                          GENERAL.  THE ARTICLE SHOWS HOW THE    *   FILE 014
//*                          CBT TAPE CAN IMPROVE YOUR INSTALLATION *   FILE 014
//*                          GREATLY BY PROVIDING POWERFUL TOOLS.   *   FILE 014
//*                          THIS IS MEANT AS AN INTRODUCTION ONLY, *   FILE 014
//*                          AND SUGGESTS A FEW OF THE TOOLS WHICH  *   FILE 014
//*                          THE AUTHOR HAS FOUND USEFUL IN HIS     *   FILE 014
//*                          WORK.                                  *   FILE 014
//*                                                                 *   FILE 014
//*           IOCOUNT   -  DESCRIPTION OF THE AMAZING IO-COUNT ZAP  *   FILE 014
//*                          TO THE OPERATING SYSTEM, WHICH         *   FILE 014
//*                          PROVIDES EXCP-COUNT INFORMATION IN JCL *   FILE 014
//*                          LISTINGS, FOR ALL ALLOCATED DDNAMES.   *   FILE 014
//*                          THE MODIFICATION IS FOUND ON FILE 369  *   FILE 014
//*                          OF THE CBT TAPE.  THIS IS A DETAILED   *   FILE 014
//*                          DESCRIPTION OF HOW TO INSTALL IT.      *   FILE 014
//*                                                                 *   FILE 014
//*           JESART    -  THIS IS A DESCRIPTION OF HOW TO CONVERT  *   FILE 014
//*                          FROM JES2 VERSION 1.3.4 TO THE HIGHER  *   FILE 014
//*                          RELEASES OF JES2.                      *   FILE 014
//*                                                                 *   FILE 014
//*           SMPART    -  I BELIEVE THIS MATERIAL IS FOUND NOWHERE *   FILE 014
//*                          ELSE IN THIS FORM.  THIS ARTICLE IS    *   FILE 014
//*                          MEANT TO INTRODUCE NEW AND OLD SYSTEMS *   FILE 014
//*                          PROGRAMMERS TO THE CONCEPTS OF SMP.    *   FILE 014
//*                          IT CAN BE USED AS A "HOW-TO-DO-IT"     *   FILE 014
//*                          INTRODUCTION TO ANY LEVEL OF SMP.  IT  *   FILE 014
//*                          IS CLEAR, CONCEPTUAL, AND COMPLETELY   *   FILE 014
//*                          STEP-BY-STEP.  IT COVERS CONCEPTS OF   *   FILE 014
//*                          ALL RELEASES OF SMP, BOTH SMP4 AND     *   FILE 014
//*                          SMP/E.  THE ARTICLE WAS TESTED BY      *   FILE 014
//*                          BEING GIVEN TO NON-SYSTEMS-PROGRAMMERS *   FILE 014
//*                          TO READ, AND IS MEANT FOR ANYONE WHO   *   FILE 014
//*                          HAS ANYTHING TO DO WITH MVS SYSTEM     *   FILE 014
//*                          MAINTENANCE.  THIS MEANS NON-TECHNICAL *   FILE 014
//*                          MANAGERS AS WELL AS TECHNICAL PEOPLE.  *   FILE 014
//*                                                                 *   FILE 014
//*           SMPART2   -  COMPLETION OF THE SMPART MATERIAL.       *   FILE 014
//*                          (IT WAS THERE ALL THE TIME, BUT IT     *   FILE 014
//*                          GOT LOST IN THE SHUFFLE.)              *   FILE 014
//*                          THIS IS AN OLD ARTICLE THAT SOMEHOW    *   FILE 014
//*                          WENT MISSING FROM THIS FILE.           *   FILE 014
//*                                                                 *   FILE 014
//*           A series of three articles has been written as        *   FILE 014
//*           a course to teach the subcommands of the fantastic    *   FILE 014
//*           "PDS" program that can be found on File 182 of the    *   FILE 014
//*           CBT Tape (with utilities on File 296).  These are     *   FILE 014
//*           included here as well as on CBT File 120.             *   FILE 014
//*                                                                 *   FILE 014
```
