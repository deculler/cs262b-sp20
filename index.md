---
layout: default
---

# Advanced Topics in Computer Systems (Spring 2020)

* **When**: *Tuesdays and Thursdays from 12:30 to 2:00*
* **Where**: *Soda 310*
* **Instructor**: [David E Culler](https://eecs.berkeley.edu/~culler)
   * **Office Hours:** Tuesdays and Thursdays from 2:00 to :00 in 783 Soda Hall.

## Course Description

*Catalog Description:* Continued graduate survey of large-scale systems for managing information and computation. Topics include basic performance measurement; extensibility, with attention to protection, security, and management of abstract data types; index structures, including support for concurrency and recovery; parallelism, including parallel architectures, query processing and scheduling; distributed data management, including distributed and mobile file systems and databases; distributed caching; large-scale data analysis and search. Homework assignments, exam, and term paper or project required.

*Informal Description:* It provides a PhD-level study of
groundbreaking and influential research across the spectrum of
operating systems, parallel and distributed systems, networked systems, storage
systems, and security across the tiers from global scale, cloud,
institutional, personal, mobile, and embedded.  It is intended to
directly support student preparation for a dissertation in systems
areas, but will also support completion of the MS post cs262a.

Particular emphasis is placed on understanding and participating in
the advancement of formative ideas in this rapidly evolving field.  We
will read many of the highly recognized or highly cited papers over
the past 20 years, including several that were rejected one or more
times before being accepted and going on to be extremely highly
aclaimed, e.g., receiving test-of-time awards.  We will
also look at foundational works that laid the path for these advances
decades earlier, before the web completely reshaped systems research.
We will use OSDI 2020 as an focusing opportunity and carry out a
mock-PC within the class on projects as if they were being submitted
to the conference.  (The timing of the conference will not permit a
shadow PC as it did in 2009, when this course was last offered.)
Discussion will be moderated so all voices can be heard.

## Course Format

Several of the class meetings will take the form of "a great debate",
with readings challenging the status quo or laying out a fundamental
trade-off in approach.  Class session will have a debate format to
develop experience with articulating and weighing broad ideas.  The
other meetings will focus on a particular technical advancement and
each paper will have three students presenting specific perspectives:
the key advancement of the work, the methodology by which the results
are established, and limitations to the applicability of the results.

Each class meeting will center on, typically, two readings assigned prior,
with students assigned to the roles above.  A short report on the papers
will be due at 8am of the day of class, so the instructor can read those
and pull out important observations or gaps prior to class discussion.


## Course Syllabus

<!-- This is the dates for all the lectures -->
{% capture dates %}
1/21/20
1/23/20
1/28/20
1/30/20
2/4/20
2/6/20
2/11/20
2/13/20
2/18/20
2/20/20
2/25/20
2/27/20
3/3/20
3/5/20
3/10/20
3/12/20
3/17/20
3/19/20
3/24/20
3/26/20
3/31/20
4/2/20
4/7/20
4/9/20
4/14/20
4/16/20
4/21/20
4/23/20
4/28/20
4/30/20
5/5/20
5/7/20
{% endcapture %}
{% assign dates = dates | split: " " %}

This is a tentative schedule.  
Specific readings are subject to change as student interests are
better understood.

<a href="#today"> Jump to Today </a>

<table class="table table-striped syllabus">
<thead>
   <tr>
      <th style="width: 5%"> Week </th>
      <th style="width: 10%"> Date (Lec.) </th>
      <th style="width: 85%"> Topic </th>
   </tr>
</thead>
<tbody>

{% include syllabus_entry %}
## Introduction and Course Overview

This meeting will be overview of the class and introduction of class members.
Time permitting, we will talk about system performance.

{% include syllabus_entry %}
## Student 3-minute "My Systems Research" presentations.

Each class member will offer a 3-slide presentation of
their current research focus.

Add presentation or link [here](https://drive.google.com/drive/u/0/folders/1GlEyMcw3jaJW1CRlqvSIul6CBwXiAcob)

Sign up for [debate roles](https://docs.google.com/spreadsheets/d/1PcQ2H55QAhTVq5RTp5_QLLnQC8cx6kSrm2je-nGox8s/edit?usp=sharing)

{% include syllabus_entry %}
<!-- 1/28/20 -->
## Great Debate 1: OS Abstractions

A fundamental question in systems is how system software creates
effective abstractions enabling protected access to shared hardware
resources.  We will have two debates centered on HotOS
papers - extensible kernels and virtual machines.

<div class="reading">
<div class="required_reading" markdown="1">
* [Exterminate All Operating System Abstractions](https://people.eecs.berkeley.edu/~culler/cs262b/papers/hotos-exokernel.pdf) D. Engler and M. F. Kaashoekm, HotOS 1995
[(write up}](https://docs.google.com/forms/d/e/1FAIpQLSdKnG0iq67wKHRMuG1hNKSXxL2-I9OFGT-3f68Yg7KNrwYbaw/viewform)
* [Extensible Kernels are Leading OS Research Astray](https://drive.google.com/open?id=1AR5itsgFggt9zU1qLCQYboiPcE4RQca5) Druschel et al, HotOS-VI '97
[(write up)](https://docs.google.com/forms/d/e/1FAIpQLSeQaQcx9spv8BQB3CTyTRtHhEMiXTZuPj-aWiIPiMlzFU35IA/viewform)
* [Hype and Virtue](https://www.usenix.org/legacy/events/hotos07/tech/full_papers/roscoe/roscoe.pdf) T. Roscoe, et al., HotOS 2007
[(write up)](https://docs.google.com/forms/d/e/1FAIpQLSfUDAZlUZrl0TRraetigzMFmsHgbzfyk0cLkhoUEzOaeJIjBg/viewform)
</div>

<div class="optional_reading" markdown="1">
* [Xen and the Art of Virtualization](https://www.cl.cam.ac.uk/research/srg/netos/papers/2003-xensosp.pdf) Xen and the Art of Virtualization, Barham, et al. ACM SIGOPS Operating Systems ReviewVol. 37, No. 5.
* [Bringing Virtualization to the x86 Architecture with the Original
VMware Workstation](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.423.4009&rep=rep1&type=pdf) E. Bugnion, et al, ACM Transactions on Computer Systems (TOCS), November 2012.
* [kvm: the Linus Virtual Machine Monitor](https://www.kernel.org/doc/ols/2007/ols2007v1-pages-225-230.pdf), Kivity et al, Proc. of the Linux Symposium, 2007.
</div>
</div>

{% include syllabus_entry %}
<!-- 1/30/20 -->
## Great Debate 2: Threads vs Events

A critical element of all operating systems is how to handle concurrency.  Fundamentally
there have been two camps, threads vs events.  Needham tried to put the questiojn
to rest in 1978 with the Duality paper.  But graphical user interfaces and then
internet services and wireless embedded networks brought it back to the fore.  The
SOSP 2001 program committee is debated whether to reject the SEDA paper or to make
it a keynote.  The compromise was to accept it and have Roger Needham deliver a
keynote adjacent to it.  But two years later, some of the SEDA authors had
evolved their views.  You'll want to read or at skim the optional references, but you don't
need to report on them.

<div class="reading">
<div class="required_reading" markdown="1">
* [SEDA: An Architecture for Well-Conditioned, Scalable Internet Services](http://www.sosp.org/2001/papers/welsh.pdf) M. Welsh, et al.SOSP 2001. [(write up)](https://docs.google.com/forms/d/e/1FAIpQLSe7jm_vdI3gjWHh-MjJb68Xvl2DOl2dE5f4U9hfc5deLbtFQA/viewform)
* [Capriccio: Scalable Threads for Internet Services](http://capriccio.cs.berkeley.edu/pubs/capriccio-sosp-2003.pdf) R. von Behren, et al, SOSP 2003 [(write up)](https://docs.google.com/forms/d/e/1FAIpQLScpAoy8eGTSaOB8Td8ZdIeWlaclYSXf35qlzaFDbsI391dhtg/viewform)
</div>

<div class="optional_reading" markdown="1">
* [On the Duality of Operating System Structures](https://drive.google.com/open?id=1_D7wy-mqFrn8k-BoG7fiMa8lQEyoJ-Ao) Lauer anbd Needham, SOSP 1978
* [Why Threads Are A Bad Idea (for most purposes)](https://web.stanford.edu/~ouster/cgi-bin/papers/threads.pdf) John Osterhout, presentation to
1996 USENIX Technical Conference
* [System Architecture Directions for Networked Sensors](https://pdos.csail.mit.edu/archive/6.097/readings/tinyos.pdf) J. Hill et al, ASPLOS 2000
</div>
</div>

{% include syllabus_entry %}
<!-- 2/4/20 -->
## Debate 3: Multicore OS

With the end of clock scaling we have experienced a "fourth wave" of
multiprocessor design, MultiCore, where wee can expect the number of
cores per processor to grow rapidly as chip density continues to grow.
As the multi-micrioprocessor revolution of the 80's drove 
BSD, this presents basic questions of scaling Linux vs rethinking
the design, but now where cloud-based services are the driving workload,
behooving us to revisit the contract between system and user level,
represented in the 90's by Scheduler Activations.

<div class="reading">
<div class="required_reading" markdown="1">
* [An Analysis of Linux Scalability to Many Cores](https://pdos.csail.mit.edu/papers/linux:osdi10.pdf) Boyd-Wickizer, et al., OSDI 2010 [(write up)](https://docs.google.com/forms/d/e/1FAIpQLSf2CD1IWEaJQyOHrD_IXa-EI75_NmULqvozZs7Uj8U8CE4RWA/viewform)
* [The Multikernel: A new OS architecture for scalable multicore systems](https://www.sigops.org/s/conferences/sosp/2009/papers/baumann-sosp09.pdf) A. Baumann, et al, SOSP 2009.
  [(write up)](https://docs.google.com/forms/d/e/1FAIpQLSc9LwIOLLcRYl26YXYLTUAplvjbKbzsLz-furzaZRobhVkTyA/viewform)
</div>
<div class="optional_reading" markdown="1">
* [Scheduler activations: effective kernel support for the user-level management of parallelism](https://homes.cs.washington.edu/~tom/pubs/sched_act.pdf) T. Andersen, et al, SOSP 91 and ACM ToC 92.
</div>
</div>

{% include syllabus_entry %}
<!-- 2/6/20 -->
## Debate 4: HLL role is OS Design

Throughout the histiory of computing, operating systems have represented the
most demanding sort of complex, concurrency intensive, high-reliability software.
This has given rise to numerous new language designs, and new languages have
offered the potential to finally leap beyond C as the implementation language.
Recent years have seen a renaissance in programming language design, including
new systems languages, e.g, Go and Rust.

<div class="reading">
<div class="required_reading" markdown="1">
* [Multiprogramming a 64 kB Computer Safely and Efficiently](https://sing.stanford.edu/site/publications/levy17-tock.pdf) A. Levy, et al. SOSP 2017.
  [(write up)](https://docs.google.com/forms/d/e/1FAIpQLSe6K4J7zDxLgFrCWZ0Q8b2VJ37FUid__Lzb9Hdo67lfKlVTcA/viewform)
* [The benefits and costs of writing a POSIX kernel in a high-level language](https://www.usenix.org/conference/osdi18/presentation/cutler) C. Cutler, et al. OSDI 2018.
  [(Write up)](https://docs.google.com/forms/d/e/1FAIpQLSeaF7Tl12zP5ySQJCWzmyz7V6f7vwezVGtAF9J_T66mxPighg/viewform)

</div>
<div class="optional_reading" markdown="1">
* [Hydra: The Kernel of a Multiprocessor Operating System](https://research.cs.wisc.edu/areas/os/Qual/papers/hydra.pdf) W. Wulf, et al. CACM 1974.

</div>
</div>

{% include syllabus_entry %}
<!-- 2/11/20 -->
## Scan on KV - MapReduce

As cluster computing took off post-search engine, Scan algorithms were
rediscovered over a new storage model while handling unreliability.

<div class="reading">
<div class="required_reading" markdown="1">
* [MapReduce: Simplified Data Processing on Large Clusters](https://static.googleusercontent.com/media/research.google.com/en//archive/mapreduce-osdi04.pdf) J. Deand and S. Ghemawat, OSDI 2004
* [Fast key-value stores:
An idea whose time has come and gone](https://research.google/pubs/pub48030/) A. Adya, et al., HotOS 2019.
</div>
<div class="optional_reading" markdown="1">
* [Scans as Primitive Parallel Operations](https://people.eecs.berkeley.edu/~culler/cs262b/papers/scan89.pdf) G. Belloch, IEEE ToC, 1989.
</div>
</div>

{% include syllabus_entry %}
<!-- 2/13/20 -->
## Distributed Consensus in Practice

Paxos has dominated the vernacular of distributed consensus.  Not only does it have
its own checked history of whether it warranted publication, but the efforts to
develop a more understandable and implementable replacement (Raft) were rejected
three times before being published.  These readings overlap with CS262A; we will
take the opportunity to explore overcoming rejection in the pubication process.

[Here are the reviews from the 3 rejected submissions](https://drive.google.com/open?id=17bgKs6puIBTNwNlFZ6MMs2ZZn68C_wXW) of Raft, before being accepted and awarded Best Paper.  The RAFT link provides the conference talk.  Watch it before class.

<div class="reading">
<div class="required_reading" markdown="1">
* [The Chubby lock service for loosely-coupled distributed systems](https://static.googleusercontent.com/media/research.google.com/en//archive/chubby-osdi06.pdf) M. Burrows, OSDI 2006
 [(writeup)](https://docs.google.com/forms/d/e/1FAIpQLSdX2IYnv4sqFa83S4VoOHTOfIczkznC9MmwxuAbd6WYAqxAwQ/viewform)
* [In Search of an Understandable Consensus Algorithm](https://www.usenix.org/node/184041) D. Ongaro and J. Ousterhout, USENIX ATC 2014 [(writeup)](https://docs.google.com/forms/d/e/1FAIpQLSd1zDMl6VvbY4CdB5atC8EmJ_gIZIicrOHf1Cr4s3yzn38exw/viewform) 
</div>
<div class="optional_reading" markdown="1">
* [The Part-Time Parliment](https://www.microsoft.com/en-us/research/publication/part-time-parliament/) Leslie Lamport (Blog + ACM ToC 1998) ACM SIGOPS Hall of Fame Award 2012.
* [CS262A Treatment](https://people.eecs.berkeley.edu/~kubitron/cs262/lectures/lec18-Paxos-Raft.pdf)
</div>
</div>

{% include syllabus_entry %}
## Emergence of Planetary Scale Computing

As clusters, content-distribution networks (e.g., Akamai), and [PVM](https://www.csm.ornl.gov/pvm/) took hold, but the Cloud gaining massive scale, global
geographic scale, and general usage was economically inconceivable,
visionary explorations of planetary scale computing emerged.  The WebOS paper
was rejected four times, but invited by a PC chair.  Planetlab faced distainful reviews,
but recieved multiple test-of-time awards a decade later.  The Grid remained
largely outside the systems research community.

<!-- 2/18/20 -->
<div class="reading">
<div class="required_reading" markdown="1">
* [WebOS: Operating system services for wide area applications](https://www.researchgate.net/profile/Amin_Vahdat2/publication/3765693_WebOS_Operating_System_Services_for_Wide_Area_Applications/links/0f31753872b04b5051000000/WebOS-Operating-System-Services-for-Wide-Area-Applications.pdf) A. Vahdat, et al., HPCA 1998
  [(write up)](https://docs.google.com/forms/d/e/1FAIpQLSc9ih2Rhv3PIEosD-MXyheRnD30fibUDVrhVhk436i70Y0i9A/viewform)
* [The Anatomy of the Grid: Enabling Scalable Virtual Organizations](https://arxiv.org/pdf/cs/0103025.pdf) International Journal of High Performance Computing Applications, 2001
  [(write up)](https://docs.google.com/forms/d/e/1FAIpQLSfFa85iIhaw2l7-wnpKAxWhUB2oTAyGJqz2cR-77IdGGCKnaA/viewform)
* [Operating System Support for Planetary-Scale Network Services](https://www.usenix.org/legacy/publications/library/proceedings/nsdi04/tech/full_papers/bavier/bavier.pdf) A. Bavier, et al, NSDI 2004
   [(write up)](https://docs.google.com/forms/d/e/1FAIpQLSeZKIK7P7C8f51x5yy7WK6jUXyBNaku_YgDDx0Jwuk2jPiZIw/viewform)
</div>
</div>

{% include syllabus_entry %}
<!-- 2/20/20 -->
## Cloud Cluster Frameworks

Term projects in 2009, Mesos and Spark, brought an essentially level of generality over
the opensource, Hadoop, and commercial state of the art.  The "cluster level" systems
design concepts were able to reach much further with the maturation of cluster
technology and its "local level" systems building blocks.

<div class="reading">
<div class="required_reading" markdown="1">
* [Mesos: A Platform for Fine-Grained Resource Sharing in the Data Center](https://www.usenix.org/conference/nsdi11/mesos-platform-fine-grained-resource-sharing-data-center) B. HJindman, NSDI 2011. [(write up)](https://docs.google.com/forms/d/e/1FAIpQLSc8UZL86Lngd1YJ8m6Gw8sjENTRUiohzvhkhZelBLPKJoUpBg/viewform)
* [Apache Spark: A Unified Engine for
Big Data Processing](https://people.eecs.berkeley.edu/~alig/papers/spark-cacm.pdf) M. Zaharia, et al., CACM 2016 (A short paper appears at HotCloud 2010).[(write up)](https://docs.google.com/forms/d/e/1FAIpQLScQIMcjUIfWANKNqrTU3hadkEwhfnV5uzBuHMd-jmsWN9KsSQ/viewform)
</div>
<div class="optional_reading" markdown="1">
* [ A Case for NOW (Networks of Workstations)](https://drive.google.com/open?id=1ZVdNe7UddlPxyzo88nCpQEXC2SQqwdkY) T. Anderson et al., IEEE Micro 1995
* [Resilient Distributed Datasets: A Fault-Tolerant Abstraction for In-Memory Cluster Computing](https://www.usenix.org/system/files/conference/nsdi12/nsdi12-final138.pdf) M. Zaharia, et al., NSDI 2012.
</div>
</div>

{% include syllabus_entry %}
<!-- 2/25/20 -->
## NSDI

{% include syllabus_entry %}
<!-- 2/27/20 -->
## NSDI

{% include syllabus_entry %}
<!-- 3/3/20 -->
## CS262B Alums - Entreprenurialism and Graduate Systems

{% include syllabus_entry %}
<!-- 3/5/20 -->
## Societal-Scale Graph Processing

<div class="reading">
<div class="required_reading" markdown="1">
* [Pregel: A System for Large-Scale Graph Processing](https://kowshik.github.io/JPregel/pregel_paper.pdf) G. Malewicz, et al., SIGMOD 2010
* [PowerGraph: Distributed Graph-Parallel Computation on Natural Graphs](https://www.usenix.org/system/files/conference/osdi12/osdi12-final-167.pdf) J. Gonzalez, et al. OSDI 2012.
</div>
<div class="optional_reading" markdown="1">
* [GraphX: Graph Processing in a Distributed Dataflow Framework](https://www.usenix.org/node/186217) J. Gonzales, et al., OSDI 2014
</div>
</div>


{% include syllabus_entry %}
<!-- 3/10/20 -->
## SysML - Cloud-scale Machine Learning Systems

<div class="reading">
<div class="required_reading" markdown="1">
* [TensorFlow: A System for Large-Scale Machine Learning](https://www.usenix.org/system/files/conference/osdi16/osdi16-abadi.pdf) M. Abadi, et al., OSDI 2016. [(write up)](https://docs.google.com/forms/d/e/1FAIpQLSdodSU7ERq-YHOZRm43nC_-wRdFZCTW2QashKvrY6Gf6BeWIA/viewform)
* [Ray: A Distributed Framework for Emerging AI Applications](https://www.usenix.org/system/files/osdi18-moritz.pdf) P. Moritz, et al., OSDI 2018 [(write up)](https://docs.google.com/forms/d/e/1FAIpQLScTMU3OjH1wWen3sbCjmv6HDaMhPqheu65FdqhHdBrn8qOfjQ/viewform)
</div>
<div class="optional_reading" markdown="1">
* [Dataflow Architectures](https://drive.google.com/open?id=1HjjH2Re8kIZNrysSv9XCZKWWCCEa3u3K) Arvind and D. Cullers, Annual Reviews in Computer Science, 1986
* [An Assessment of Multilisp: Lessons from Experience](https://drive.google.com/open?id=1IkI-QKjHdTLy9pSND5uaGT_3h3mOGVfn) R. Halstead,  International Journal of Parallel Programming, Vol. 15, No. 6, 1986.
</div>
</div>

{% include syllabus_entry %}
<!-- 3/12/20 -->
## Serverless

<div class="reading">
<div class="required_reading" markdown="1">
* [Serverless Computation with OpenLambda](https://www.usenix.org/node/196323) S. Hendrickson, et al., HotCloud 2016 [(write up)](https://docs.google.com/forms/d/e/1FAIpQLSe8SmMMDkeuTcN6vfA9RiHyfItKGIdjO9xzNKz6uof9eIp9Bw/viewform )
* [Occupy the Cloud: Distributed Computing for the 99%](https://shivaram.org/publications/pywren-socc17.pdf) E. Jonas, Et al., SoCC 2017. [(write up)](https://docs.google.com/forms/d/e/1FAIpQLSeENs5fVfrVt10bQW8ftYZuRtB96t-V2ZBX0YLO7wi-1flQeQ/viewform)
</div>
<div class="optional_reading" markdown="1">
* [Operating Systems must support GPU abstractions](https://www.microsoft.com/en-us/research/wp-content/uploads/2011/05/hotos11-final.pdf) C. Rossbach, HotOS 2011.
* [Will Serverless End the Dominance of Linux in the Cloud?](https://drive.google.com/open?id=1D624i1aTYgxXDPwTFggBrZYNnCFLz5Rg) R. Holler and D. Williams, HotOS 2017
</div>
</div>

{% include syllabus_entry %}
<!-- 3/17/20 -->
## Planetary Scale Computing Systems Redux

<div class="reading">
<div class="required_reading" markdown="1">
* [Borg, Omega, and Kubernetes](https://queue.acm.org/detail.cfm?id=2898444) B. Burns et al., ACM Queue, March 2016.
* [CAP Twelve Years Later: How the “Rules” Have Changed](https://drive.google.com/open?id=1GUPw0EdrEpin8cko2ikv6BMK6TPerG6Q) E. Brewer, IEEE Computer, 2012
* [The Ninja architecture for robust Internet-scale systems and services](https://drive.google.com/open?id=1TO_9-Oa52nogzeZCcK2rSjPsvy7w--cx) S. Gribble, et al., Computer Networks, 2001
</div>
</div>

{% include syllabus_entry %}
<!-- 3/19/20 -->
## *EECS Faculty Retreat*

Class time available to work on projects.
<div class="reading">
<div class="required_reading" markdown="1">
</div>
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
<!-- 3/24/20 -->
## *Spring Break*

{% include syllabus_entry %}
<!-- 3/26/20 -->
## *Spring Break*

{% include syllabus_entry %}
<!-- 3/31/20 -->

## Debate: Post-Cloud Operating System Design
<div class="reading">
<div class="required_reading" markdown="1">
* [Arrakis: The Operating System is the Control Plane](https://www.usenix.org/conference/osdi14/technical-sessions/presentation/peter) S. Peter, et al., OSDI 2014 [(Write up)](https://docs.google.com/forms/d/e/1FAIpQLSdnZZcuT1UCOFlCCBvE-jik5_-sQnZ72X6xJ2IXlimWa_6tBQ/viewform)
* [I’m Not Dead Yet! The Role of the Operating System in a Kernel-Bypass Era](https://www.microsoft.com/en-us/research/uploads/prod/2019/04/demikernel-hotos19.pdf) I. Zhang, et al., HotOS 2019 [(Write up)](https://docs.google.com/forms/d/e/1FAIpQLSdbzRlGLPKndOX3SRPTQM72tsFnAMzg-YJ8gJRSOVD2yhbIHg/viewform)
* [A fork() in the road](https://www.microsoft.com/en-us/research/uploads/prod/2019/04/fork-hotos19.pdf) A. Baumann, HotOS 2019 [(Write up)](https://docs.google.com/forms/d/e/1FAIpQLScMatuVoGRB3dkcSG6feNjvU9phwrP6pZx-52MAMY-G9lpHOw/viewform)
</div>
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
<!-- 4/2/20 -->
## Network Function Virtualization

<div class="reading">
<div class="required_reading" markdown="1">
* [OpenFlow: Enabling Innovation in Campus Networks](http://ccr.sigcomm.org/online/files/p69-v38n2n-mckeown.pdf) N. McKeown, et al., SIGCOMM CC$ 2008.
* [NetBricks: Taking the V out of NFV](https://www.usenix.org/conference/osdi16/technical-sessions/presentation/panda) A. Panda, et al., OSDI 2016.
</div>
<div class="optional_reading" markdown="1">
* [E2: A Framework for NFV Applications](https://people.eecs.berkeley.edu/~sylvia/cs268-2016/papers/e2.pdf) S. Palkar, et al., SOSP 2015
</div>
</div>

{% include syllabus_entry %}
<!-- 4/7/20 -->
## IFC and IPC
<div class="reading">
<div class="required_reading" markdown="1">
* [TaintDroid: An Information-Flow Tracking System for Realtime Privacy Monitoring on Smartphones](https://www.usenix.org/legacy/event/osdi10/tech/full_papers/Enck.pdf) W. Enck, OSDI 2010.
* [Introduction to OpenBinder and Interview with Dianne Hackborn](https://www.osnews.com/story/13674/introduction-to-openbinder-and-interview-with-dianne-hackborn/)
</div>
</div>


{% include syllabus_entry %}
<!-- 4/9/20 -->
## Time and Defensive Distributed System Design

<div class="reading">
<div class="required_reading" markdown="1">
* [Time, Clocks, and the Ordering of Events in a Distributed System ](http://lamport.azurewebsites.net/pubs/time-clocks.pdf) L. Lamport
* [Internet Time Synchronization: The Network Time Protocol](https://people.eecs.berkeley.edu/~culler/cs262b/papers/ntp-tocomm-91.pdf) David L. Mills, IEEE Transactions on Communications, 1991
</div>
</div>

{% include syllabus_entry %}
<!-- 4/14/20 -->
## Epidemic Routing and Gossip Protocols

<div class="reading">
<div class="required_reading" markdown="1">
* [Epidemic Routing for Partially-Connected Ad Hoc Networks](http://issg.cs.duke.edu/epidemic/epidemic.pdf) A. Vahdat and D. Becker, Duke TR CS–2000–06, 2000.
* [Trickle: A Self-Regulating Algorithm For Code Propagation And Maintenance In Wireless Sensor Networks](https://www.usenix.org/legacy/publications/library/proceedings/nsdi04/tech/levisTrickle/levisTrickle.pdf) P. Levis, et al., NSDI 2004 (Test of Time).
</div>
<div class="optional_reading" markdown="1">
* [Directed diffusion: a scalable and robust communication paradigm for sensor networks](http://people.cs.uchicago.edu/~ravenben/classes/333/papers/ige00.pdf)
</div>
</div>

{% include syllabus_entry %}
<!-- 4/16/20 -->
## Key Results - Student Presentations

{% include syllabus_entry %}
<!-- 4/21/20 -->
## Optional Project Discussions 

{% include syllabus_entry %}
## How to be a good reviewer
<!-- 4/23/20 -->

{% include syllabus_entry %}
<!-- 4/28/20 -->
## Failure and Disaster Planning
<div class="reading">
<div class="required_reading" markdown="1">
* [Failure Trends in a Large Disk Drive Population](https://www.usenix.org/legacy/event/fast07/tech/full_papers/pinheiro/pinheiro.pdf) E. Pinheiu\ro, et al. FAST 2007 (test of time)
* [Designing for disasters ](https://www.usenix.org/legacy/publications/library/proceedings/fast04/tech/full_papers/keeton/keeton.pdf) K. Keeton, at al., FAST 2004 (test of time)
</div>
</div>


{% include syllabus_entry %}
<!-- 4/30/20 -->
## No Class

Draft Reports due 4/29.  Distributed for review

{% include syllabus_entry %}
<!-- 5/5/20 -->
## RR Mock PC Meeting (OSDI Abstract due)

{% include syllabus_entry %}
## 5/7/20 RR 

</td>
</tr>
</tbody>
</table>

<script type="text/javascript">

var current_date = new Date();
var rows = document.getElementsByTagName("th");
var finished =  false;
for (var i = 1; i < rows.length && !finished; i++) {
   var r = rows[i];
   if (r.id.startsWith("counter_")) {
      var fields = r.id.split("_")
      var week_div_id = "week_" + fields[2]
      var lecture_date = new Date(fields[1] + " 23:59:00")
      if (current_date <= lecture_date) {
         finished = true;
         r.style.background = "orange"
         r.style.color = "black"
         var week_td = document.getElementById(week_div_id)
         week_td.style.background = "#043361"
         week_td.style.color = "white"
         var anchor = document.createElement("div")
         anchor.setAttribute("id", "today")
         week_td.prepend(anchor)
      }
   }
}

$(".reading").each(function(ind, elem) {
   var optional_reading = $(elem).find(".optional_reading");
   if(optional_reading.length == 1) {
      optional_reading = optional_reading[0];
      optional_reading.setAttribute("id", "optional_reading_" + ind);
      var button = document.createElement("button");
      button.setAttribute("class", "btn btn-primary btn-sm");
      button.setAttribute("type", "button");
      button.setAttribute("data-toggle", "collapse");
      button.setAttribute("data-target", "#optional_reading_" + ind);
      button.setAttribute("aria-expanded", "false");
      button.setAttribute("aria-controls", "#optional_reading_" + ind);
      optional_reading.setAttribute("class", "optional_reading_no_heading collapse")
      button.innerHTML = "Additional Optional Reading";
      optional_reading.before(button)
   }
   
})


$(".details").each(function(ind, elem) {
      elem.setAttribute("id", "details_" + ind);
      var button = document.createElement("button");
      button.setAttribute("class", "btn btn-primary btn-sm");
      button.setAttribute("type", "button");
      button.setAttribute("data-toggle", "collapse");
      button.setAttribute("data-target", "#details_" + ind);
      button.setAttribute("aria-expanded", "false");
      button.setAttribute("aria-controls", "#details_" + ind);
      elem.setAttribute("class", "details_no_heading collapse")
      button.innerHTML = "Detailed Description";
      elem.before(button)
   })

</script>


## Projects

[Project ideas](https://drive.google.com/open?id=1x1OSSYzCRd5PDv_4QprZ2n_Z2sU3ioEb5jx6G-kicR4)

Please fill out the project proposal form by Sunday, March 1.

[Project Proposal form](https://docs.google.com/forms/d/e/1FAIpQLSdYLFXRfxM_YF1XBhPloaLBnzMIxbRp9H5uTfVRj3usf1ESiA/viewform)

### Relevant Conferences (partial list)

* [OSDI](https://www.usenix.org/conferences/byname/179)
* [SOSP](http://www.sosp.org/)
* [NSDI](https://www.usenix.org/conferences/byname/178)
* [FAST](https://www.usenix.org/conferences/byname/146)
* [Eurosys](https://dl.acm.org/conference/eurosys)
* [SigComm](http://sigcomm.org/events/sigcomm-conference)
* [SenSys](https://sensys.acm.org/)
* [BuildSys](http://buildsys.acm.org/)
* [ASPLOS](https://dl.acm.org/conference/asplos)
* [CPSweek](https://dl.acm.org/conference/cpsweek)

Useful references

* [Usenix Test of Time Awards](https://www.usenix.org/conferences/test-of-time-awards)
* [Usenix Best Paper Awards](https://www.usenix.org/conferences/best-papers)
* [Analysis of Best Papers vs Ranking by Conf](https://www.aminer.cn/bestpaper)


## Grading

Grades will be largely based on class participation and projects.  In addition, we will require weekly paper summaries submitted before class. If class chooses, we could
include an individual assignment.

* **Project:** _55%_
* **Weekly Summaries:** _20%_
* **Paper Leads:** _10%_
* **Class Participation:** _15%_

### Removed

## Scaling Wide Area Storage
<div class="reading">
<div class="required_reading" markdown="1">
* [Spanner: Google’s Globally-Distributed Database](https://www.usenix.org/system/files/conference/osdi12/osdi12-final-16.pdf) J. COrbett, et al., OSDI 2012
* [Scaling Memcache at Facebook](https://www.usenix.org/system/files/conference/nsdi13/nsdi13-final170_update.pdf) R. Nishtala, et al., NSDI 2013
</div>
<div class="optional_reading" markdown="1">
* [Scalable, distributed data structures for internet service construction](https://static.usenix.org/events/osdi00/full_papers/full_papers/gribble/gribble.pdf) S. Gribble, OSDI 2000.
</div>
</div>
