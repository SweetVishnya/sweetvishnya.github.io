<p style="text-align: right"><a href="/ru/">Русский</a></p>

<div style="float: left; margin-right: 1em">
<img src="https://gravatar.com/avatar/991fda15b33321f67ba8e3647980ea62?s=200">
</div>

Hi!

I completed bachelor's and master's degrees in the [Faculty of Computational Mathematics and Cybernetics](https://cs.msu.ru/en) at [Lomonosov Moscow State University](https://www.msu.ru/en/).

I work for the Compiler Technology Department at [Ivannikov Institute for System Programming of the RAS](https://www.ispras.ru/en/) as a research scientist. I am excited to develop the cutting edge dynamic symbolic execution tool [Sydr](https://www.ispras.ru/en/technologies/sydr/) that enables automatic bug detection.

I have a strong interest in computer security, symbolic execution, fuzzing, automatic bug detection, return-oriented programming, dynamic analysis, binary analysis, compilers, and developing tools for all the above.

# Contacts

 * vishnya&nbsp;\<at\>&nbsp;ispras&nbsp;.&nbsp;ru
 * GitHub: [SweetVishnya](https://github.com/SweetVishnya)
 * [ResearchGate](https://www.researchgate.net/profile/Alexey_Vishnyakov)
 * [Google Scholar](https://scholar.google.ru/citations?user=2FcTnyQAAAAJ)
 * [LinkedIn](https://www.linkedin.com/in/sweetvishnya/)
 * [Twitter](https://twitter.com/VishnyaSweet)
 * ResearcherID: [AAN-3944-2021](https://www.researcherid.com/rid/AAN-3944-2021)
 * Scopus Author ID: [57203944937](https://www.scopus.com/authid/detail.uri?authorId=57203944937)
 * ORCID: [0000-0003-1819-220X](https://orcid.org/0000-0003-1819-220X)

# Publications and Talks

[BibTeX](papers.bib)

## Sydr: Cutting Edge Dynamic Symbolic Execution \[[paper](https://arxiv.org/abs/2011.09269)\] \[[video](https://www.ispras.ru/conf/2020/video/compiler-technology-11-december.mp4#t=6021)\] \[[slides](vishnyakov-isprasopen2020.pdf)\] \[[github](https://github.com/ispras/sydr-benchmark)\] \[[demo](https://youtu.be/yznSawgD9D0)\]

<u>Vishnyakov A.</u>, Fedotov A., Kuts D., Novikov A., Parygina D., Kobrin E., Logunova V., Belecky P., Kurmangaleev Sh. Sydr: Cutting Edge Dynamic Symbolic Execution. 2020 Ivannikov ISPRAS Open Conference (ISPRAS), IEEE, 2020, pp. 46-54. DOI: [10.1109/ISPRAS51486.2020.00014](https://doi.org/10.1109/ISPRAS51486.2020.00014)

### Abstract

The security development lifecycle (SDL) is becoming an industry standard. Dynamic symbolic execution (DSE) has enormous amount of applications in computer security (fuzzing, vulnerability discovery, reverse-engineering, etc.). We propose several performance and accuracy improvements for dynamic symbolic execution. Skipping non-symbolic instructions allows to build a path predicate 1.2--3.5 times faster. Symbolic engine simplifies formulas during symbolic execution. Path predicate slicing eliminates irrelevant conjuncts from solver queries. We handle each jump table (switch statement) as multiple branches and describe the method for symbolic execution of multi-threaded programs. The proposed solutions were implemented in Sydr tool. Sydr performs inversion of branches in path predicate. Sydr combines DynamoRIO dynamic binary instrumentation tool with Triton symbolic engine. We evaluated Sydr features on 64-bit Linux executables.

## Survey of Methods for Automated Code-Reuse Exploit Generation \[[paper](https://arxiv.org/abs/2011.07862)\] \[[github](https://github.com/ispras/rop-benchmark)\] \[[russian&nbsp;paper](https://ispras.ru/preprints/docs/prep_32_2019.pdf)\]

<u>Vishnyakov A.V.</u>, Nurmukhametov A.R. Survey of methods for automated code-reuse exploit generation. Proceedings of the Institute for System Programming, vol. 31, issue 6, 2019, pp. 99-124. DOI: [10.15514/ISPRAS-2019-31(6)-6](https://doi.org/10.15514/ISPRAS-2019-31(6)-6)

### Abstract

This paper provides a survey of methods and tools for automated code-reuse exploit generation. Such exploits use code that is already contained in a vulnerable program. The code-reuse approach allows one to exploit vulnerabilities in the presence of operating system protection that prohibits data memory execution. This paper contains a description of various code-reuse methods: return-to-libc attack, return-oriented programming, jump-oriented programming, and others. We define fundamental terms: gadget, gadget frame, gadget catalog. Moreover, we show that, in fact, a gadget is an instruction, and a set of gadgets defines a virtual machine. We can reduce an exploit creation problem to code generation for this virtual machine. Each particular executable file defines a virtual machine instruction set. We provide a survey of methods for gadgets searching and determining their semantics (creating a gadget catalog). These methods allow one to get the virtual machine instruction set. If a set of gadgets is Turing-complete, then a compiler can use a gadget catalog as a target architecture. However, some instructions can be absent. Hence we discuss several approaches to replace missing instructions with multiple gadgets. An exploit generation tool can chain gadgets by pattern searching (regular expressions) or considering gadgets semantics. Furthermore, some chaining methods use genetic algorithms, while others use SMT-solvers. We compare existing open-source tools and propose a testing system rop-benchmark that can be used to verify whether a generated chain successfully opens a shell.

## A Method for Analyzing Code-Reuse Attacks \[[publicly&nbsp;available&nbsp;draft](vishnyakov19-draft.pdf)\] \[[paper](https://link.springer.com/article/10.1134/S0361768819080061)\] \[[slides](vishnyakov-isprasopen2018.pdf)\] \[[russian&nbsp;paper](https://www.ispras.ru/proceedings/docs/2018/30/5/isp_30_2018_5_31.pdf)\] \[[russian&nbsp;video](https://vimeo.com/298786113)\]

<u>Vishnyakov, A.V.</u>, Nurmukhametov, A.R., Kurmangaleev, S.F., and Gaisaryan S.S., 2019. A Method for Analyzing Code-Reuse Attacks. Programming and Computer Software 45(8), pp. 473-484. DOI: [10.1134/S0361768819080061](https://doi.org/10.1134/S0361768819080061)

### Abstract

Nowadays, ensuring software security is of paramount importance. Software failures can have significant consequences, and malicious vulnerability exploitation can inflict immense losses. Large corporations pay particular attention to the investigation of computer security incidents. Code-reuse attacks based on return-oriented programming (ROP) are gaining popularity each year and can bypass even modern operating system protection mechanisms. Unlike ordinary shellcode, where instructions are placed sequentially in memory, a ROP chain consists of multiple small instruction blocks (called gadgets) and uses the stack to chain them together. This makes the analysis of ROP exploits more difficult. The main goal of this work is to simplify reverse engineering of ROP exploits. A method for analyzing code-reuse attacks that allows one to split the chain into gadgets, restore the semantics of each particular gadget, and restore the prototypes and parameter values of the system calls and functions invoked during the execution of the ROP chain is proposed. The semantics of each gadget is determined by its parameterized type. Each gadget type is defined by a postcondition (Boolean predicate) that must always be true after the gadget execution. The proposed method was implemented as a software tool and tested on real-world ROP exploits found on the Internet.

## Fine-Grained Address Space Layout Randomization on Program Load \[[paper](https://link.springer.com/article/10.1134%2FS0361768818050080)\] \[[slides](https://www.ispras.ru/conf/2017/pdf/Nurmukhametov.pdf)\] \[[russian&nbsp;paper](https://www.ispras.ru/proceedings/docs/2017/29/6/isp_29_2017_6_163.pdf)\] \[[russian&nbsp;slides](https://nurmukhametov.com/fine_grained_aslr.ru.pdf)\]

Nurmukhametov, A.R., Zhabotinskiy, E.A., Kurmangaleev, S.F., Gaissaryan, S.S., and <u>Vishnyakov, A.V.</u>, 2018. Fine-Grained Address Space Layout Randomization on Program Load. Programming and Computer Software, 44(5), pp. 363-370. DOI: [10.1134/S0361768818050080](https://doi.org/10.1134/S0361768818050080)

### Abstract

Software vulnerabilities are a serious security threat. It is important to develop protection mechanisms preventing their exploitation, especially with a rapid increase of ROP attacks. State of the art protection mechanisms have some drawbacks that can be used by attackers. In this paper, we propose fine-grained address space layout randomization on program load that is able to protect from such kind of attacks. During the static linking stage, the executable and library files are supplemented with information about function boundaries and relocations. A system dynamic linker/loader uses this information to perform permutation of functions. The proposed method was implemented for 64-bit programs on CentOS 7 operating system. The implemented method has shown good resistance to ROP attacks evaluated by two metrics: the number of survived gadgets and the exploitability estimation of ROP chain examples. The implementation presented in this article is applicable across the entire operating system and has no compatibility problems affecting the program performance. The working capacity of proposed approach was demonstrated on real programs. The further research can cover forking randomization and finer granularity than on the function level. It also makes sense to implement the randomization of short functions placement taking into account the relationships between them. The close arrangement of functions that often call each other can improve the performance of individual programs.

## Classification of ROP gadgets \[[russian&nbsp;paper](https://www.ispras.ru/proceedings/docs/2016/28/6/isp_28_2016_6_27.pdf)\] \[[russian&nbsp;slides](gadgets.pdf)\]

<u>Vishnyakov A.V.</u> Classification of ROP gadgets. Trudy ISP RAN/Proc. ISP RAS, vol. 28, issue 6, 2016, pp. 27-36 (in Russian). DOI: [10.15514/ISPRAS-2016-28(6)-2](https://doi.org/10.15514/ISPRAS-2016-28(6)-2)

### Abstract

Return-oriented programming (ROP) is a dangerous exploitation technique which can be used to bypass modern defense mechanisms. ROP reuses code chunks ending with control transfer instruction from a program binary to form a chain corresponding some payload. These code chunks are called gadgets. Though, a certain set of gadgets should be available to exploit a vulnerability. Determining gadgets that can be used to form a ROP chain can be done by gadgets search and classification. This paper introduces a method for ROP gadgets classification that allows one to evaluate whether or not ROP technique can be used to exploit a program vulnerability. Classification is based on side-effects analysis of gadget execution with concrete inputs. Gadget instructions are translated into IR which is interpreted to track registers and memory usage. Initial registers and memory values are randomly generated. According to initial and final values of registers and memory gadget semantics can be explored. Classification performs several executions to determine gadget semantics. Proposed method is applied to program binaries and its capabilities were demonstrated on 32-bit and 64-bit binaries from Ubuntu 14.04. Using classification results program exploitability was confirmed for several examples. Furthermore, a possible exploitation of stack buffer overflow vulnerability in presence of write-what-where condition was shown on a model example demonstrating a bypass of canary, DEP and ASLR.

## Software defect severity estimation in presence of modern defense mechanisms \[[russian&nbsp;paper](https://www.ispras.ru/proceedings/docs/2016/28/5/isp_28_2016_5_73.pdf)\]

Fedotov A.N., Padaryan V.A., Kaushan V.V., Kurmangaleev Sh.F., <u>Vishnyakov A.V.</u>, Nurmukhametov A.R. Software defect severity estimation in presence of modern defense mechanisms. Trudy ISP RAN/Proc. ISP RAS, vol. 28, issue 5, 2016. pp. 73-92 (in Russian). DOI: [10.15514/ISPRAS-2016-28(5)-4](https://doi.org/10.15514/ISPRAS-2016-28(5)-4)

### Abstract

This paper introduces a refined method for automated exploitability evaluation of found program bugs. During security development lifecycle a significant number of crashes is detected in programs. Because of limited resources, bug fixing is time consuming and needs prioritization. It should be the matter of highest priority to fix exploitable bugs. Automated exploit generation technique is used to solve this problem in practice. Generated exploit confirms the presence of a critical vulnerability. However, state-of-the-art publications omit modern defense mechanisms preventing exploitation. It results in lowering of an evaluation quality. This paper considers modern vulnerability exploitation prevention mechanisms. An evaluation of their prevalence and efficiency is also presented. The method can be applied to program binaries and doesn’t require any debug information. Proposed method is based on symbolic interpretation of traces obtained by a full-system emulator. Our method can demonstrate a real exploitability for stack buffer overflow vulnerability with write-what-where condition even when DEP, ASLR, and “canary” operate together. The implemented method capabilities were shown on model examples and real programs.

# Theses

 * Master thesis 2020 &mdash; Development and implementation of return-oriented programming chains generation method \[[russian&nbsp;thesis](vishnyakov-master-thesis2020.pdf)\] \[[russian&nbsp;slides](vishnyakov-master-thesis2020-presentation.pdf)\]

 * Coursework 2019 &mdash; Semantic verification of linear machine instruction sequence \[[russian&nbsp;thesis](vishnyakov-coursework2019.pdf)\] \[[russian&nbsp;slides](vishnyakov-coursework2019-presentation.pdf)\]

 * Bachelor thesis 2018 &mdash; Development and implementation of code-reuse attacks analysis method \[[russian&nbsp;thesis](vishnyakov-diploma2018.pdf)\] \[[russian&nbsp;slides](vishnyakov-diploma2018-presentation.pdf)\]

 * Coursework 2017 &mdash; Guided path predicate construction during a symbolic interpretation of binary traces \[[russian&nbsp;thesis](vishnyakov-coursework2017.pdf)\] \[[russian&nbsp;slides](vishnyakov-coursework2017-presentation.pdf)\]
