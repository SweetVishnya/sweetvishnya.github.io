Hi!

I am a M.D. student in the [Faculty of Computational Mathematics and Cybernetics](https://cs.msu.ru/en) at [Lomonosov Moscow State University](https://www.msu.ru/en/).

I work for the Compiler Technology Department at [Ivannikov Institute for System Programming of the RAS](http://www.ispras.ru/en/) as a research scientist.

I have a strong interest in computer security, return-oriented programming, binary analysis, symbolic execution, reverse engineering, and compilers.

# Contacts

 * vishnya \<at\> ispras . ru
 * GitHub: [SweetVishnya](https://github.com/SweetVishnya)
 * [ResearchGate](https://www.researchgate.net/profile/Alexey_Vishnyakov)

# Publications and Talks

## Method for analysis of code-reuse attacks \[[russian paper](http://www.ispras.ru/proceedings/docs/2018/30/5/isp_30_2018_5_31.pdf)\] \[[slides](vishnyakov-isprasopen2018.pdf)\]

<u>Vishnyakov A.V.</u>, Nurmukhametov A.R., Kurmangaleev Sh.F., Gaisaryan S.S. Method for analysis of code-reuse attacks. Trudy ISP RAN/Proc. ISP RAS, vol. 30, issue 5, 2018, pp. 31-54 (in Russian). DOI: 10.15514/ISPRAS-2018-30(5)-2

### Abstract

Providing security for computer programs is one of the paramount tasks nowadays. Failures in operation of program software can lead to serious consequences and exploitation of vulnerabilities can inflict immense harm. Large corporations pay particular attention to the analysis of computer security incidents. Code-reuse attacks based on return-oriented programming are gaining more and more popularity each year and can bypass even modern operating system protections. Unlike common shellcode, where instructions are placed consequently in memory, ROP chain contains of several small instruction blocks (gadgets) and uses stack to chain them together, which makes analysis of ROP exploits more difficult. The main goal of this work is to simplify reverse engineering of ROP exploits. In this paper I propose the method for analysis of code-reuse attacks, which allows one to split chain into gadgets, restore the semantics of each particular gadget, and restore prototypes and parameters values of system calls and functions called during the execution of ROP chain. Parametrized types define gadget semantics. Each gadget type is defined by a postcondition (boolean predicate) that must always be true after executing the gadget. The proposed method was implemented as a program tool and tested on real ROP exploits found on the internet.
