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
* [Extensible Kernels are Leading OS Research Astray](https://drive.google.com/open?id=1AR5itsgFggt9zU1qLCQYboiPcE4RQca5) Druschel et al (HotOS-VI '97)
* [Hype and Virtue](https://www.usenix.org/legacy/events/hotos07/tech/full_papers/roscoe/roscoe.pdf) T. Roscoe, et al., HotOS 2007
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
* [SEDA: An Architecture for Well-Conditioned, Scalable Internet Services](http://www.sosp.org/2001/papers/welsh.pdf) M. Welsh, et al.SOSP 2001.
* [Capriccio: Scalable Threads for Internet Services](http://capriccio.cs.berkeley.edu/pubs/capriccio-sosp-2003.pdf) R. von Behren, et al, SOSP 2003
</div>

<div class="optional_reading" markdown="1">
* [On the Duality of Operating System Structures](https://drive.google.com/drive/u/0/folders/1zM0S1BrUv_G3IndzXSWNTkQ1rnR7mf1x) Lauer anbd Needham, SOSP 1978
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
* [An Analysis of Linux Scalability to Many Cores](https://pdos.csail.mit.edu/papers/linux:osdi10.pdf) Boyd-Wickizer, et al., OSDI 2010
* [The Multikernel: A new OS architecture for scalable multicore systems](https://www.sigops.org/s/conferences/sosp/2009/papers/baumann-sosp09.pdf) A. Baumann, et al, SOSP 2009.
</div>
<div class="optional_reading" markdown="1">
* [Scheduler activations: effective kernel support for the user-level management of parallelism](https://homes.cs.washington.edu/~tom/pubs/sched_act.pdf) T. Andersen, et al, SOSP 91 and ACM ToC 92.
</div>
</div>

{% include syllabus_entry %}
<!-- 2/6/20 -->
Debate: HLL role is OS Design

Throughout the histiory of computing, operating systems have represented the
most demanding sort of complex, concurrency intensive, high-reliability software.
This has given rise to numerous new language designs, and new languages have
offered the potential to finally leap beyond C as the implementation language.
Recent years have seen a renaissance in programming language design, including
new systems languages, e.g, Go and Rust.

<div class="reading">
<div class="required_reading" markdown="1">
* [Multiprogramming a 64 kB Computer Safely and Efficiently](https://sing.stanford.edu/site/publications/levy17-tock.pdf) A. Levy, et al. SOSP 2017.
* [The benefits and costs of writing a POSIX kernel in a high-level language](https://www.usenix.org/conference/osdi18/presentation/cutler) C. Cutler, et al. OSDI 2018.

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

<div class="reading">
<div class="required_reading" markdown="1">
* [In Search of an Understandable Consensus Algorithm](https://www.usenix.org/node/184041) D. Ongaro and J. Ousterhout, USENIX ATC 2014
* [The Chubby lock service for loosely-coupled distributed systems](https://static.googleusercontent.com/media/research.google.com/en//archive/chubby-osdi06.pdf) M. Burrows, OSDI 2006
</div>
<div class="optional_reading" markdown="1">
* [The Part-Time Parliment](https://www.microsoft.com/en-us/research/publication/part-time-parliament/) Leslie Lamport (Blog + ACM ToC 1998) ACM SIGOPS Hall of Fame Award 2012.
* [CS262A Treatment](https://people.eecs.berkeley.edu/~kubitron/cs262/lectures/lec18-Paxos-Raft.pdf)
</div>
</div>

{% include syllabus_entry %}
2/18/20
<div class="reading">
<div class="required_reading" markdown="1">
</div>
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
2/20/20
<div class="reading">
<div class="required_reading" markdown="1">
</div>
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
2/25/20
<div class="reading">
<div class="required_reading" markdown="1">
</div>
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
2/27/20
<div class="reading">
<div class="required_reading" markdown="1">
</div>
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
3/3/20
<div class="reading">
<div class="required_reading" markdown="1">
</div>
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
3/5/20
<div class="reading">
<div class="required_reading" markdown="1">
</div>
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
3/10/20
<div class="reading">
<div class="required_reading" markdown="1">
</div>
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
3/12/20
<div class="reading">
<div class="required_reading" markdown="1">
</div>
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
3/17/20
<div class="reading">
<div class="required_reading" markdown="1">
</div>
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
3/19/20
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
3/31/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
4/2/20
<div class="reading">
<div class="required_reading" markdown="1">
</div>
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
4/7/20
<div class="reading">
<div class="required_reading" markdown="1">
</div>
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
4/9/20
<div class="reading">
<div class="required_reading" markdown="1">
</div>
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
4/14/20
<div class="reading">
<div class="required_reading" markdown="1">
</div>
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
4/16/20
<div class="reading">
<div class="required_reading" markdown="1">
</div>
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
4/21/20
<div class="reading">
<div class="required_reading" markdown="1">
</div>
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
## How to be a good reviewer
4/23/20

{% include syllabus_entry %}
4/28/20
</div>
</div>

{% include syllabus_entry %}
## Mock PC Meeting
4/30/20
</div>
</div>

{% include syllabus_entry %}
5/5/20
## RR (OSDI Abstract due)

{% include syllabus_entry %}
## 5/7/20 RR 

<h3> xstuff
</h3>

Work on project


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

Detailed candidate project descriptions will be posted shortly.  However, students are encourage to find projects that relate to their ongoing research.

## Grading

Grades will be largely based on class participation and projects.  In addition, we will require weekly paper summaries submitted before class. If class chooses, we could
include an individual assignment.

* **Project:** _55%_
* **Weekly Summaries:** _20%_
* **Paper Leads:** _10%_
* **Class Participation:** _15%_
