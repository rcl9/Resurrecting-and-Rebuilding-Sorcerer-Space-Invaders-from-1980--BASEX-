# Resurrecting and Rebuilding 'Sorcerer Space Invaders' from 1980 (BASEX Language)

I can't believe that I am presenting this project as the odds of resurrecting a large multi-year (non-commercial, personal) coding project from over 45 years ago, and make it all work again, was simply zero. Even while pursuing this goal I didn't feel it was technically possible to get everything working again due to all of the lost, critical knowledge of how the "Jinga" runtime system of BASEX functioned. But it seems that nothing is impossible if you focus on a core goal.

This repository acts to document and rebuild the mental history, the development history and the final outcome of my two years of writing Space Invaders for the Exidy Sorcerer during 1980 and 1981, primarily in the little known BASEX programming language for Z80. 

<div style="text-align:center">
<img src="/Images/snap1.webp" alt="" style="width:70%; height:auto;">  <img src="/Images/1980 Arcade.webp" alt="" style="width:70%; height:auto;">
<br><img src="/Images/snap2.webp" alt="" style="width:70%; height:auto;">  <img src="/Images/1980 Arcade.webp" alt="" style="width:70%; height:auto;">
<br><img src="/Images/snap3.webp" alt="" style="width:70%; height:auto;">  <img src="/Images/1980 Arcade.webp" alt="" style="width:70%; height:auto;">
</div>

## Some Initial Perspective

To set the correct perspective, when I started this digital archaeology project I had literally nothing to start with. The game's original development had occurred 1.5 years before I got my then-new Morrow 8" floppy disk drive and its CP/M operating system in July 1981. As such, I did not have any CP/M diskette images to work with today based on my last 16 years of disk imaging and document scanning. And my critically important memories of that era had faded away to near dust. Or so I thought...

This project was like uncovering a long lost civilization in the dessert and having few clues or hints about what it was all about. It was like having amnesia and needing to restart your old memories from scratch, or being a detective put on a cold case with nothing much more than some scribbled notes on papers to deduce everything which happened more than 40 years ago. 

In some half-joking manner, this project was why I would never come to (*ever*) play another game in my life, to hate games with infinite negativity, and probably why I never became a multi-millionaire from future game development which I was otherwise perfectly set up to do so in the 1980s.

## The Start of the Game's Development in 1980

Space Invaders was released in April 1978 by Taito and Midway Manufacturing in late 1978. I became intrigued with it in early 1980 and decided to implement my own version. Having been born with a camera in hand, I snuck into an arcade at a local mall to take screen snapshots of the game. This was well before there were magazines or the Internet to download such assets.

<div style="text-align:center">
<img src="/Images/1980 Arcade2.webp" alt="" style="width:70%; height:auto;">  <img src="/Images/1980 Arcade.webp" alt="" style="width:70%; height:auto;">
</div>

I then set out to clone the game as a complete newbie to the trade. In some regards (in my current mindset) this was a complete waste of my life but the upside is that it explicitly forced me into a completely different profession and not the much more lucrative game development market.  From those photos I developed a few dozen digital representations of each sprite using graph paper:

<div style="text-align:center">
<img src="/Images/graphics1.webp" alt="" style="width:70%; height:auto;">  <img src="/Images/graphics2.webp" alt="" style="width:70%; height:auto;">
</div>

From that I implemented the Space Invaders program in 800 lines of BASIC using the Exidy Sorcerer's 8k Pac-BASIC in April 1980. It was cassette based which took a few minutes to save (one or two copies) of the code to tape at 1200 baud. Additionally, as noted elsewhere, my Sorcerer was apt to crash or lock up due to its excessive heat issues on the 5v power rail. Nevertheless, I didn't know any better at the time and hence found this to be a good challenge and goal to clone Space Invaders. 

Seeing that it was too slow I then made the decision to port it over to the BASEX language (in July 1980) which proported to run 5 to 20 times faster than BASIC. I had come across BASEX in my print copy of the <a href="https://archive.org/details/dr_dobbs_journal_vol_03">Dr. Dobb's Journal, volume 3, page 451</a>. I have recently and extensively documented all of that related work]( ADD IN REFERENCE CODE) to resurrect BASEX and its history, as it related to this Exidy Sorcerer Space Invaders game development. In some regard it did run faster than BASIC but coding in the BASEX runtime environment was terribly "hair pulling and head banging" to say the least -- please read my comments in my other repo to learn why.

The last version of the BASEX implementation of Sorcerer Space Invaders came in at 2030 lines of code and 500 lines of symbol table, as well as a hand coded Z80 machine language library of support routines to speed up the graphics operations + user I/O.  All of this was developed on paper and not interactively within the BASEX command-line driven program (as the concept of "editing and debugging" just wasn't supported well in BASEX). As changes were made on paper then they were transcribed to the BASEX compiler's code listing and saved to cassette tape -- this also ensured that my coding would be spared in case there were errors on the tape (which happened often). It also ensured that I could OCR those hand written code listings 45 years later and rebuild the same BASEX code base for the game. 

## The "Psychology of Game Development in 1980" 

I believe that an important aspect of presenting this history is to provide a snapshot of the psychology of game development in 1980 as no one reading this history will be able to comprehend how primitive and difficult it was. I can't even believe that I wrote a 2000 line BASEX program entirely on paper and without any coding/debugging/editing environment to support the work. But for perspective, I didn't know any better at the time since having a personal computer was by itself a gift. Coding in BASEX was like writing software in Neanderthal times. I'm sure that many other Apple-II, TRS-80, PET and VIC-20 computer developers of 1980 experienced similar challenges. 

In 1980 I only had a 16k Exidy Sorcerer computer with a tape cassette for saving and loading files at 1200 baud. The machine would often lock-up due to its known heat issues and/or the files save to tape would have become corrupted (this is why I still actively do daily backups of all my computer work). I did not have a disk system running CP/M nor was the Wordstar editor (my favourite and current programming editor) available to me. I had no access to any 8080/Z80 assembler or editor. I basically had nothing available to me for programming - no compilers and no text editors. There was only 8k Exidy BASIC in the ROM pack, BASEX, and pen + paper. 

Since I had no IDE nor editor for BASEX, I chose to do the "programming" all on paper. The final BASEX file listing is from 61 pages (!!) of carefully hand written code.  That is just insane to think about for any current and modern programmer. It's even insane for me to think about today. Again, I simply did not know any better at the time. 

Working with the BASEX compiler/runtime environment was like walking across cracked ice and knowing it was going to fail at any moment. It was painful and mind numbing experience all around. The compiler controlled you as you had little control over it. All you could do was enter a line number and a command statement. If you typed "run" then you'd most likely end up in the Exidy monitor program as there was little debugging feedback or reporting in the runtime system when something failed. I suppose this is why I became quite good at debugging code logically in my head and without needing tool support. 

Similarly, all of my Z80 coding of that pre-1982 era was done mainly in pure machine language on paper as I did not have access to a 8080/Z80 assembler yet (at least not until I got my CP/M system up and running). I still have lots of scanned documents of that era where I had written several full length programs for the Exidy Sorcerer in page 0 (addresses 0 to 255). 

But my mind and processes changed once I got CP/M and my favourite Wordstar editor in late 1981. I then had a reliable system to write lots of Z80 code using a real assembler like M80.com from Microsoft. 

And it wasn't well into the late 1980's that I'd migrate over to the C language. Why so late? Well, by that point in time I had realized that all of my Z80 coding during the 1980s would not port over to the IBM PC machine that was starting to take over my life between 1988 and 1991. As of 1991, I used my Pentium I computer for my work and all of its C-based development, editing, compilation and debugging.

Is coding easier and better today compared to 1980? Do I even need to answer that question? My thought is that it is far too easy today to write code (barring the mention of A.I) compared to the tedious, hand crafted approach of the early 1980's before floppy disks and IDEs were available. It wasn't until 1987 that Borland announced *Turbo C* which I found to be a real game changer in my life - for the first time I had access to a really good IDE and an IBM PC with a 22MB hard disk that made me a lot more efficient. The compiler worked for me rather than the other way around with BASEX. 

I would not want to go back to those days of coding but it was still a very good "grounding" experience that taught me how computers work from the bit level upwards and how to solve problems entirely on my own without requiring constant Internet searches or A.I queries. 

## Rebuilding Sorcerer Space Invaders with the BASEX Compiler and Runtime Library

To make a long story short, it took a few weeks to [retrieve my original development files](/How_To_Archive_Old_Computer_Data_Tapes_Using_Tapetool2_(Exidy_Sorcerer)) from cassette tape and make any sense of what I had in hand. For me, it was just a bunch of gobbly-gook with no rhyme nor reason. I had also recently thrown out 4ft of printed manuals of the 1980s and one of them was the critically important BASEX manual with all of my runtime notes along with it. However, I did discover a folio of my daily notes which I had made in 1980 and 1981 -- that started to revive my memories of this project and provide some important runtime execution clues. My [deep dive into BASEX](/Rebuilding_the_History_and_Runtime_Environment_of_the_BASEX_Compiler_from_the_1979_Era) and how it worked allowed me to get it up and running again on the jSorcerer emulator, even as primitive as it may be. 

After all was said and done, my detective work on the many dozens of files I had retrieved from tape pointed to "PROG2" on side two of a tape to be the final version, and CRC-verified error free, both with the program listing and its all-important matching symbol table file. Phew! Additionally, I was able to eventually narrow down and verify an error free version of the BASEX compiler and its runtime library which I had previously extensively modified for my Space Invaders game in 1980. The pieces were starting to fall into place. 

I then came to learn that I had written a "ROUTN" library in Z80 machine language. The BASEX code would call into this library using its "CAL" statement, allowing me to speed up graphics related operations and any machine I/O. I then wrote a [new and simple utility](/MAKE REF TO THE ACTUAL REPO) to dump the contents of the BASEX symbol table files with which I could then equate the addresses in my ROUTN library to my paper notes of 1980/1981 and of the calls made from the BASEX listing - that helped tremendously to create a mental map in my head of how everything pieced together:

| Code Segment  | Memory Range  |
|:------------- |:---------------- | 
| BASEX runtime | 0x100 to 0x939 |
| BASEX compiler | 0x09DC to 0x20FF |
| Space Invader BASEX byte-code stream | 0x2100 to 0x60B7 |
| "ROUTN" | 0x6100 to 0x62CF |
| Graphics character table | 0x62D0 and 0x66CF |
| Data table area | 0x6700 and 0x6d10 |
| Symbol table | 0x6F52 to 0x7EFF (end of memory) |

The program is loaded into memory as (1) the BASEX component, (2) the Space Invader's byte-code stream, (3) the "ROUTN" library and (4) the symbol table file. Thereafter BASEX is executed via a "GO 100" from the Exidy monitor. 

## Runtime Executables

In this repository I have provided two runtime executables of the Space Invaders game that can be executed on a real Exidy Sorcerer machine or  the MAME emulator running CP/M (Dreamdisk System), or the jSorcerer emulator:

- A CP/M compatible [binary file](/Game runtime/CPM Binary/BasexInv.com) has been created which loads up at 0x100H but related to zero memory. 

- A jSorcerer emulator "[snapshot image](/Game runtime/jSorcerer Snapshot/_jSorcerer Memory Snapshot.snp". An explanation of how to load up jSorcerer and execute this memory snapshot is provided in [this document](/Game runtime/jSorcerer Snapshot/How to load and execute.txt).

When BASEX starts up enter "0" to the "Range?" question. The code can then be run via a "RUN 8496" (if you don't enter the starting line number then BASEX will simply exit and return to the Exidy monitor!!).

## See Also

Rebuilding_the_History_and_Runtime_Environment_of_the_BASEX_Compiler_from_the_1979_Era

How_To_Archive_Old_Computer_Data_Tapes_Using_Tapetool2_(Exidy_Sorcerer)

[TapeTool - A Microbee Tape Diagnotic and Recovery Utility (older open source version)](https://github.com/toptensoftware/tapetool)
