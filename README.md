# Singularity RDK
Singularity was a multi-year research project focused on the construction of dependable systems through innovation in the areas of systems, languages, and tools. We built a research operating system prototype (called Singularity), extended programming languages, and developed new techniques and tools for specifying and verifying program behavior.

Advances in languages, compilers, and tools open the possibility of significantly improving software. For example, Singularity uses type-safe languages and an abstract instruction set to enable what we call Software Isolated Processes (SIPs). SIPs provide the strong isolation guarantees of OS processes (isolated object space, separate GCs, separate runtimes) without the overhead of hardware-enforced protection domains. In the current Singularity prototype SIPs are extremely cheap; they run in ring 0 in the kernel’s address space.

Singularity uses these advances to build more reliable systems and applications. For example, because SIPs are so cheap to create and enforce, Singularity runs each program, device driver, or system extension in its own SIP. SIPs are not allowed to share memory or modify their own code. As a result, we can make strong reliability guarantees about the code running in a SIP. We can verify much broader properties about a SIP at compile or install time than can be done for code running in traditional OS processes. Broader application of static verification is critical to predicting system behavior and providing users with strong guarantees about reliability.

## Presentations:

[Singularity: A research OS written in C#, Channel 9 video and blog, Redmond, WA, August 23, 2005.](http://channel9.msdn.com//showPost.aspx?PostID=68302)

[Singularity Revisited, Channel 9 video and blog, Redmond, WA, December 13, 2005.](http://channel9.msdn.com//showPost.aspx?PostID=141858)

[Singularity III: Revenge of the SIP, Channel 9 video and blog, Redmond, WA, September 1, 2006.](http://channel9.msdn.com//showpost.aspx?postid=227259)

[Singularity IV: Return of the UI, Channel 9 video and blog, Redmond, WA, September 1, 2006.](http://channel9.msdn.com//showpost.aspx?postid=227260)


## Members

- Mark Aiken
- Paul Barham
- Trishul Chilimbi
- John DeTreville
- Ulfar Erlingsson
- Wolfgang Grieskamp
- Tim Harris
- Orion Hodson
- Rebecca Isaacs
- ike Jones
- Steven Levi
- Roy Levin
- Nick Murphy
- Jakob Rehof
- Wolfram Schulte
- Dan Simon
- Bjarne Steensgaard
- David Tarditi
- Ted Wobber

## Interns

2007

    Ryan Braud (University of Califorina, San Diego
    Michael Carbin (MIT)
    Michael Emmi (UCLA)
    Gabriel Kliot (Technion – Israel Institute of Technology)
    Ross McIlroy (University of Glasgow)
    Filip Pizlo (Purdue University)
    Polyvios Pratikakis (Univ. of Maryland)

2006

    Marc Eaddy (Columbia University)
    Haryadi S. Gunawi (Univ. of Wisconsin – Madison)
    Hiroo Ishikawa (Waseda University)
    Virendra J. Marathe (Rochester)
    Polyvios Pratikakis (University of Maryland)
    Roussi Roussev (Florida Tech)
    César Spessot (Universidad Tecnológica Nacional Facultad Córdoba)

2005

    Michael Carbin (Stanford)
    Adam Chlipala (UC Berkeley)
    Martin Pohlack (TU Dresden)
    Avi Shinnar (Harvard)
    Mike Spear (Rochester)
    Aydan Yumerefendi (Duke)

2004

    Jeremy Condit (UC Berkeley)
    Daniel Frampton (Australian National University)
    Chip Killian (UC San Diego)
    Fernando Castor de Lima Filho (Universidade Estadual de Campinas)
    Prince Mahajan (IIT Roorkee)
    Bill McCloskey (UC Berkeley)
    Martin Murray
    Tom Roeder (Cornell)
    Avi Shinnar (Columbia)
    Yaron Weinsberg (Hebrew University of Jerusalem)

If you are an exceptional Ph.D. student interested in a research internship, please apply using MSR Internship Application
