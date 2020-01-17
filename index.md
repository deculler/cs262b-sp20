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

"Informal Description:* It provides a PhD-level study of
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

* Materials: [[pdf](assets/lectures/lec01/01_ai-sys-intro-small.pdf), [pptx](https://github.com/ucbrise/cs294-ai-sys-fa19/raw/master/assets/lectures/lec01/01_ai-sys-intro.pptx)]

<div class="reading">
<div class="optional_reading" markdown="1">

* [How to read a paper](https://web.stanford.edu/class/ee384m/Handouts/HowtoReadPaper.pdf) provides some pretty good advice on how to read papers effectively.
* Timothy Roscoe's [writing reviews for systems conferences](https://people.inf.ethz.ch/troscoe/pubs/review-writing.pdf) will also help you in the reviewing process.

</div>
</div>

{% include syllabus_entry %}
#1/23/20
## Student 3-minute "My Systems Research" presentations.
Each class member will offer a 3-slide presentation of
their current research focus.

{% include syllabus_entry %}
#1/28/20
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
<div class="optional_reading" markdown="1">
* [Xen and the Art of Virtualization](https://www.cl.cam.ac.uk/research/srg/netos/papers/2003-xensosp.pdf) Xen and the Art of Virtualization, Barham, et al. ACM SIGOPS Operating Systems ReviewVol. 37, No. 5.
* [Bringing Virtualization to the x86 Architecture with the Original
VMware Workstation](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.423.4009&rep=rep1&type=pdf) E. Bugnion, et al, ACM Transactions on Computer Systems (TOCS), November 2012.
* [kvm: the Linus Virtual Machine Monitor](https://www.kernel.org/doc/ols/2007/ols2007v1-pages-225-230.pdf), Kivity et al, Proc. of the Linux Symposium, 2007.

</div>
</div>

{% include syllabus_entry %}
1/30/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
2/4/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
2/6/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
2/11/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
2/13/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
2/18/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
2/20/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
2/25/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
2/27/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
3/3/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
3/5/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
3/10/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
3/12/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
3/17/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
3/19/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
3/24/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
3/26/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
3/31/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
4/2/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
4/7/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
4/9/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
4/14/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
4/16/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
4/21/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
4/23/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
4/28/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
5/5/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}
5/7/20
<div class="reading">
<div class="optional_reading" markdown="1">
</div>
</div>

{% include syllabus_entry %}

<center>
<h3>
    <a href="https://forms.gle/tLcLeEzRzueFGUcG6">Submit Your Report Here</a>
</h3>
</center>

You only need to submit the project once per team.  The write-up should discuss the problem formulation, related work, your approach, and your results.  


</td>
</tr>
</tbody>
</table>

## Projects

Detailed candidate project descriptions will be posted shortly.  However, students are encourage to find projects that relate to their ongoing research.


## Grading

Grades will be largely based on class participation and projects.  In addition, we will require weekly paper summaries submitted before class.
* **Projects:** _60%_
* **Weekly Summaries:** _20%_
* **Class Participation:** _20%_

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


