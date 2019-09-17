Hi!

I am a M.D. student in the [Faculty of Computational Mathematics and Cybernetics](https://cs.msu.ru/en) at [Lomonosov Moscow State University](https://www.msu.ru/en/).

I work for the Compiler Technology Department at [Ivannikov Institute for System Programming of the RAS](http://www.ispras.ru/en/) as a research scientist.

I have a strong interest in computer security, return-oriented programming, binary analysis, symbolic execution, reverse engineering, and compilers.

# Contacts

 * vishnya&nbsp;\<at\>&nbsp;ispras&nbsp;.&nbsp;ru
 * GitHub: [SweetVishnya](https://github.com/SweetVishnya)
 * [ResearchGate](https://www.researchgate.net/profile/Alexey_Vishnyakov)

# Publications and Talks

## Method for analysis of code-reuse attacks \[[russian&nbsp;paper](http://www.ispras.ru/proceedings/docs/2018/30/5/isp_30_2018_5_31.pdf)\] \[[russian&nbsp;video](https://vimeo.com/298786113)\] \[[slides](vishnyakov-isprasopen2018.pdf)\]

<u>Vishnyakov A.V.</u>, Nurmukhametov A.R., Kurmangaleev Sh.F., Gaisaryan S.S. Method for analysis of code-reuse attacks. Trudy ISP RAN/Proc. ISP RAS, vol. 30, issue 5, 2018, pp. 31-54 (in Russian). DOI: 10.15514/ISPRAS-2018-30(5)-2

### Abstract

Providing security for computer programs is one of the paramount tasks nowadays. Failures in operation of program software can lead to serious consequences and exploitation of vulnerabilities can inflict immense harm. Large corporations pay particular attention to the analysis of computer security incidents. Code-reuse attacks based on return-oriented programming are gaining more and more popularity each year and can bypass even modern operating system protections. Unlike common shellcode, where instructions are placed consequently in memory, ROP chain contains of several small instruction blocks (gadgets) and uses stack to chain them together, which makes analysis of ROP exploits more difficult. The main goal of this work is to simplify reverse engineering of ROP exploits. In this paper I propose the method for analysis of code-reuse attacks, which allows one to split chain into gadgets, restore the semantics of each particular gadget, and restore prototypes and parameters values of system calls and functions called during the execution of ROP chain. Parametrized types define gadget semantics. Each gadget type is defined by a postcondition (boolean predicate) that must always be true after executing the gadget. The proposed method was implemented as a program tool and tested on real ROP exploits found on the internet.

## Fine-Grained Address Space Layout Randomization on Program Load \[[paper](https://link.springer.com/article/10.1134%2FS0361768818050080)\]

Nurmukhametov, A.R., Zhabotinskiy, E.A., Kurmangaleev, S.F., Gaissaryan, S.S. and <u>Vishnyakov, A.V.</u>, 2018. Fine-Grained Address Space Layout Randomization on Program Load. Programming and Computer Software, 44(5), pp.363-370.

### Abstract

Software vulnerabilities are a serious security threat. It is important to develop protection mechanisms preventing their exploitation, especially with a rapid increase of ROP attacks. State of the art protection mechanisms have some drawbacks that can be used by attackers. In this paper, we propose fine-grained address space layout randomization on program load that is able to protect from such kind of attacks. During the static linking stage, the executable and library files are supplemented with information about function boundaries and relocations. A system dynamic linker/loader uses this information to perform permutation of functions. The proposed method was implemented for 64-bit programs on CentOS 7 operating system. The implemented method has shown good resistance to ROP attacks evaluated by two metrics: the number of survived gadgets and the exploitability estimation of ROP chain examples. The implementation presented in this article is applicable across the entire operating system and has no compatibility problems affecting the program performance. The working capacity of proposed approach was demonstrated on real programs. The further research can cover forking randomization and finer granularity than on the function level. It also makes sense to implement the randomization of short functions placement taking into account the relationships between them. The close arrangement of functions that often call each other can improve the performance of individual programs.

## Classification of ROP gadgets \[[russian&nbsp;paper](http://www.ispras.ru/proceedings/docs/2016/28/6/isp_28_2016_6_27.pdf)\] \[[russian&nbsp;slides](gadgets.pdf)\]

<u>Vishnyakov A.V.</u> Classification of ROP gadgets. Trudy ISP RAN/Proc. ISP RAS, vol. 28, issue 6, 2016, pp. 27-36 (in Russian). DOI: 10.15514/ISPRAS-2016-28(6)-2

### Abstract

Return-oriented programming (ROP) is a dangerous exploitation technique which can be used to bypass modern defense mechanisms. ROP reuses code chunks ending with control transfer instruction from a program binary to form a chain corresponding some payload. These code chunks are called gadgets. Though, a certain set of gadgets should be available to exploit a vulnerability. Determining gadgets that can be used to form a ROP chain can be done by gadgets search and classification. This paper introduces a method for ROP gadgets classification that allows one to evaluate whether or not ROP technique can be used to exploit a program vulnerability. Classification is based on side-effects analysis of gadget execution with concrete inputs. Gadget instructions are translated into IR which is interpreted to track registers and memory usage. Initial registers and memory values are randomly generated. According to initial and final values of registers and memory gadget semantics can be explored. Classification performs several executions to determine gadget semantics. Proposed method is applied to program binaries and its capabilities were demonstrated on 32-bit and 64-bit binaries from Ubuntu 14.04. Using classification results program exploitability was confirmed for several examples. Furthermore, a possible exploitation of stack buffer overflow vulnerability in presence of write-what-where condition was shown on a model example demonstrating a bypass of canary, DEP and ASLR.

## Severity software defects estimation in presence of modern defense mechanisms \[[russian&nbsp;paper](http://www.ispras.ru/proceedings/docs/2016/28/5/isp_28_2016_5_73.pdf)\]

Fedotov A.N., Padaryan V.A., Kaushan V.V., Kurmangaleev Sh.F., <u>Vishnyakov A.V.</u>, Nurmukhametov A.R. Software defect severity estimation in presence of modern defense mechanisms. Trudy ISP RAN/Proc. ISP RAS, vol. 28, issue 5, 2016. pp. 73-92 (in Russian). DOI: 10.15514/ISPRAS-2016-28(5)-4

### Abstract

This paper introduces a refined method for automated exploitability evaluation of found program bugs. During security development lifecycle a significant number of crashes is detected in programs. Because of limited resources, bug fixing is time consuming and needs prioritization. It should be the matter of highest priority to fix exploitable bugs. Automated exploit generation technique is used to solve this problem in practice. Generated exploit confirms the presence of a critical vulnerability. However, state-of-the-art publications omit modern defense mechanisms preventing exploitation. It results in lowering of an evaluation quality. This paper considers modern vulnerability exploitation prevention mechanisms. An evaluation of their prevalence and efficiency is also presented. The method can be applied to program binaries and doesn’t require any debug information. Proposed method is based on symbolic interpretation of traces obtained by a full-system emulator. Our method can demonstrate a real exploitability for stack buffer overflow vulnerability with write-what-where condition even when DEP, ASLR, and “canary” operate together. The implemented method capabilities were shown on model examples and real programs.

# Theses

## Coursework 2019 &mdash; Semantic verification of linear machine instruction sequences \[[russian&nbsp;thesis](vishnyakov-coursework2019.pdf)\] \[[russian&nbsp;slides](vishnyakov-coursework2019-presentation.pdf)\]

## Bachelor thesis 2018 &mdash; Development and implementation of code-reuse attacks analysis method \[[russian&nbsp;thesis](vishnyakov-diploma2018.pdf)\] \[[russian&nbsp;slides](vishnyakov-diploma2018-presentation.pdf)\]

## Coursework 2017 &mdash; Guided path predicate construction during a symbolic interpretation of binary traces \[[russian&nbsp;thesis](vishnyakov-coursework2017.pdf)\] \[[russian&nbsp;slides](vishnyakov-coursework2017-presentation.pdf)\]
