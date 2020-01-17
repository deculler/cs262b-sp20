---
layout: default
---


# Advanced Topics in Computer Systems (Spring 2020)

* **When**: *Tuesdays and Thursdays from 12:30 to 2:00*
* **Where**: *Soda 310*
* **Instructor**: [David E Culler](https://eecs.berkeley.edu/~culler)
   * **Office Hours:** Tuesdays and Thursdays from 2:00 to :00 in 783 Soda Hall.

## Course Description


## Course Format

## Course Syllabus

<!-- This is the dates for all the lectures -->
{% capture dates %}
1/21/20
{% endcapture %}
{% assign dates = dates | split: " " %}

This is a tentative schedule.  Specific readings are subject to change as new material is published.

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


