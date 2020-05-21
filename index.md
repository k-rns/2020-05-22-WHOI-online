---
layout: workshop      # DON'T CHANGE THIS.
# More detailed instructions (including how to fill these variables for an
# online workshop) are available at
# https://carpentries.github.io/workshop-template/customization/index.html
venue: "Woods Hole Oceanographic Institution"        # brief name of the institution that hosts the workshop without address (e.g., "Euphoric State University")
address: "online "      # full street address of workshop (e.g., "Room A, 123 Forth Street, Blimingen, Euphoria"), videoconferencing URL, or 'online'
country: "us"      # lowercase two-letter ISO country code such as "fr" (see https://en.wikipedia.org/wiki/ISO_3166-1#Current_codes) for the institution that hosts the workshop
language: "en"     # lowercase two-letter ISO language code such as "fr" (see https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) for the
latitude: "41"        # decimal latitude of workshop venue (use https://www.latlong.net/)
longitude: "-70"       # decimal longitude of the workshop venue (use https://www.latlong.net)
humandate: "May 22, 2020"    # human-readable dates for the workshop (e.g., "Feb 17-18, 2020")
humantime: "08:45 - 12:30 EST"    # human-readable times for the workshop (e.g., "9:00 am - 4:30 pm")
startdate: 2020-05-22      # machine-readable start date for the workshop in YYYY-MM-DD format like 2015-01-01
enddate: 2020-05-22        # machine-readable end date for the workshop in YYYY-MM-DD format like 2015-01-02
instructor: ["Karen Soenen"] # boxed, comma-separated list of instructors' names as strings, like ["Kay McNulty", "Betty Jennings", "Betty Snyder"]
helper: ["Amber York, Brett Longworth, Stace Beaulieu"]     # boxed, comma-separated list of helpers' names, like ["Marlyn Wescoff", "Fran Bilas", "Ruth Lichterman"]
email: ["ksoenen@whoi.edu"]    # boxed, comma-separated list of contact email addresses for the host, lead instructor, or whoever else is handling questions, like ["marlyn.wescoff@example.org", "fran.bilas@example.org", "ruth.lichterman@example.org"]
collaborative_notes:  # optional: URL for the workshop collaborative notes, e.g. an Etherpad or Google Docs document (e.g., https://pad.carpentries.org/2015-01-01-euphoria)
eventbrite:           # optional: alphanumeric key for Eventbrite registration, e.g., "1234567890AB" (if Eventbrite is being used)
---

{% comment %} See instructions in the comments below for how to edit specific sections of this workshop template. {% endcomment %}

{% comment %}
HEADER
Edit the values in the block above to be appropriate for your workshop.
If the value is not 'true', 'false', 'null', or a number, please use
double quotation marks around the value, unless specified otherwise.
And run 'make workshop-check' *before* committing to make sure that changes are good.
{% endcomment %}


{% comment %}
Check DC curriculum
{% endcomment %}

{% if site.carpentry == "dc" or site.carpentry == "dc" %}
{% unless site.curriculum == "dc-ecology" or site.curriculum == "dc-genomics" or site.curriculum == "dc-socsci" or site.curriculum == "dc-geospatial" %}
<div class="alert alert-warning">
It looks like you are setting up a website for a Data Carpentry curriculum but you haven't specified the curriculum type in the <code>_config.yml</code> file (current value in <code>_config.yml</code>: "<strong>{{ site.curriculum }}</strong>", possible values: <code>dc-ecology</code>, <code>dc-genomics</code>, <code>dc-socsci</code>, or <code>dc-geospatial</code>). After editing this file, you need to run <code>make serve</code> again to see the changes reflected.
</div>
{% endunless %}
{% endif %}



<h2 id="general">General Information</h2>

{% comment %}
INTRODUCTION
Edit the general explanatory paragraph below if you want to change
the pitch.
{% if site.carpentry == "swc" %}
{% include swc/intro.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/intro.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/intro.html %}
{% endif %}
{% endcomment %}



Workshops always have the cleanest, best examples of data tables to use, don't they? These tables always seem to be immediately usable for analysis. Getting a raw table usable for analysis is a process called "data wrangling". In this workshop we'll show you how to get to this perfect table using Python and the package Pandas. 

Doing this process correctly will not only make you more efficient, but it will also make your data easier to reuse in the future. 

The workshop is sponsored by a WHOI Academic Programs Doherty Award and a DDVPR Technical Staff Training Award


{% comment %}
AUDIENCE
Explain who your audience is.  (In particular, tell readers if the
workshop is only open to people from a particular institution.
{% endcomment %}

{% if site.carpentry == "swc" %}
{% include swc/who.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/who.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/who.html %}
{% endif %}

<p>
  <strong>Who:</strong>
  This workshop is targeted towards improving project efficiency and building technical skills.
The workshop will only be held for 10 people at a time through an online Zoom meeting. 
  Registration is required. Please contact <a href = "mailto: stace@whoi.edu">stace@whoi.edu</a> for availability.
</p> 


{% comment %}
LOCATION
{% endcomment %}



{% comment %}
DATE
This block displays the date and links to Google Calendar.

{% if page.humandate %}
<p id="when">
  <strong>When:</strong>
  {{page.humandate}}.
  {% include workshop_calendar.html %}
</p>
{% endif %}
{% endcomment %}

{% comment %}
SPECIAL REQUIREMENTS

Modify the block below if there are any special requirements.
{% endcomment %}

<p id="requirements">
  <strong>Requirements:</strong> 
  <ul>
    <li>Participants must bring a laptop with a Mac, Linux, or Windows operating system (not a tablet, Chromebook, etc.) that they have administrative privileges on.</li>
    <li>A few specific software packages need to be installed (listed in the "Setup page" <a href="#setup">below</a>). We will be holding an on-line data lab to help you install these packages if necessary.</li>
    <li> Participants will need to join a Zoom video conference. Installing free zoom conference software is recommended.  You will not need a paid account. See <a href="https://support.zoom.us/hc/en-us/articles/201362193-Joining-a-Meeting">Joining a meeting from Zoom Help Center</a></li>
    <li>This is an introduction to Python and data tables designed for participants with no programming experience.
</li>
   </ul>   
</p>
 
 
{% comment %}
ACCESSIBILITY
Modify the block below if there are any barriers to accessibility or
special instructions.
{% endcomment %}

<p id="accessibility">
  <strong>Accessibility:</strong>
{% if online == "false" %}
  We are committed to making this workshop
  accessible to everybody. The workshop organizers have checked that:
</p>
<ul>
  <li>The room is wheelchair / scooter accessible.</li>
  <li>Accessible restrooms are available.</li>
</ul>
<p>
  Materials will be provided in advance of the workshop and
  large-print handouts are available if needed by notifying the
  organizers in advance.  If we can help making learning easier for
  you (e.g. sign-language interpreters, lactation facilities) please
  get in touch (using contact details below) and we will
  attempt to provide them.
{% else %}
  We are dedicated to providing a positive and accessible learning environment for all. Please
  notify the instructors in advance of the workshop if you require any accommodations or if there is
  anything we can do to make this workshop more accessible to you.
</p>
{% endif %}

{% comment %}
CONTACT EMAIL ADDRESS

Display the contact email address set in the configuration file.
{% endcomment %}
<p id="contact">
  <strong>Contact</strong>:
  Please email
  {% if page.email %}
  {% for email in page.email %}
  {% if forloop.last and page.email.size > 1 %}
  or
  {% else %}
  {% unless forloop.first %}
  ,
  {% endunless %}
  {% endif %}
  <a href='mailto:{{email}}'>{{email}}</a>
  {% endfor %}
  {% else %}
  to-be-announced
  {% endif %}
  for more information.
</p>

<hr/>


<h2 id="why-wrangling">Am I a data wrangler?</h2>
The process called "data wrangling", i.e., manipulating data into a usable form and diagnosing data quality issues often constitutes the most tedious and time-consuming aspect of analysis. 


<p>
<center>
<figure>
  <a href="https://doi.org/10.1177/1473871611415994" target="_blank"><img src="https://www.researchgate.net/profile/Paolo_Buono/publication/261843443/figure/fig1/AS:296928958009345@1447804788361/The-iterative-process-of-wrangling-and-analysis-One-or-more-initial-data-sets-may-be.png" alt="Regular expression xkcd comic" style="width:60%">
  <figcaption>Kandel, S. et al (2011). Research directions in data wrangling: Visualisations and transformations for usable and credible data. Inf. Vis., 10(4),271-288</figcaption>
</a>
</figure>
</center>
</p>

<p>This workshop is for you if you:</p> 
<ul>
  <li>are working with tabular/time series data.</li>
  <li>want to decrease the amount of manual work on your dataset like searching, cutting & pasting, correcting systematic errors, etc.</li>
  <li>want to perform statistical analysis and plots</li>
  <li>want to increase the value of your dataset for re-use and collaboration.</li>
</ul>   

<hr/>

{% comment%}
CODE OF CONDUCT
{% endcomment %}

<h2 id="code-of-conduct">Code of Conduct</h2>

<p>We will be using the Carpentries code of conduct for this workshop.</p>
<p>Everyone who participates in this workshop is required to conform to the <a href="https://docs.carpentries.org/topic_folders/policies/code-of-conduct.html">Code of Conduct</a>. 
</p>

{% comment %}
<p>This document also outlines how to report an incident if needed.</p>
<p class="text-center">
  <a href="https://goo.gl/forms/KoUfO53Za3apOuOK2">
    <button type="button" class="btn btn-info">Report a Code of Conduct Incident</button>
  </a>
</p>
{% endcomment %}

<hr/>

{% comment %}
Collaborative Notes

If you want to use an Etherpad, go to

https://pad.carpentries.org/YYYY-MM-DD-site

where 'YYYY-MM-DD-site' is the identifier for your workshop,
e.g., '2015-06-10-esu'.

Note we also have a CodiMD (the open-source version of HackMD)
available at https://codimd.carpentries.org
{% endcomment %}
{% if page.collaborative_notes %}
<h2 id="collaborative_notes">Collaborative Notes</h2>

<p>
We will use this <a href="{{ page.collaborative_notes }}">collaborative document</a> for chatting, taking notes, and sharing URLs and bits of code.
</p>
<hr/>
{% endif %}

{% comment %}
SURVEYS - DO NOT EDIT SURVEY LINKS
{% endcomment %}
<h2 id="surveys">Surveys</h2>
<p>Please be sure to complete these surveys before and after the workshop.</p>
<p><a href="{{ site.pre_survey }}{{ site.github.project_title }}">Pre-workshop Survey</a></p>
<p><a href="{{ site.post_survey }}{{ site.github.project_title }}">Post-workshop Survey</a></p>

<hr/>


{% comment %}
SCHEDULE

Show the workshop's schedule.  Edit the items and times in the table
to match your plans.  You may also want to change 'Day 1' and 'Day
2' to be actual dates or days of the week.

<h2 id="schedule">Schedule</h2>

{% if site.carpentry == "swc" %}
{% include swc/schedule.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/schedule.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/schedule.html %}
{% endif %}

<hr/>
{% endcomment %}


{% comment %}
SYLLABUS

Show what topics will be covered.

1. If your workshop is R rather than Python, remove the comment
around that section and put a comment around the Python section.
2. Some workshops will delete SQL.
3. Please make sure the list of topics is synchronized with what you
intend to teach.
4. You may need to move the div's with class="col-md-6" around inside
the div's with class="row" to balance the multi-column layout.

This is one of the places where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.

{% if site.carpentry == "swc" %}
{% include swc/syllabus.html %}
{% elsif site.carpentry == "dc" %}
{% include dc/syllabus.html %}
{% elsif site.carpentry == "lc" %}
{% include lc/syllabus.html %}
{% endif %}


{% endcomment %}
<h2 id="syllabus">Schedule & Syllabus</h2>


This workshop is based on a few workshops developed by the Carpentries (See <a href="https://carpentries.org">https://carpentries.org</a>  for more information about the Carpentries organisation.) and by Joe Futrelle (WHOI):
<ul>
  <li><a href=" https://datacarpentry.org/spreadsheet-ecology-lesson/">Data Organization in Spreadsheets for Ecologists</a></li>
  <li><a href="https://datacarpentry.org/python-ecology-lesson/">Data Analysis and Visualization for Ecologists</a></li>
  <li><a href="https://github.com/WHOIGit/pandas-talk/">Python and the Pandas package-Joe Futrelle (WHOI)</a></li>
</ul>

<br>
    
<h3>Part 1. Preparing your table - Best practices</h3>
 <table class="table table-striped">
  <col style="width:5%">
	<col style="width:15%">
	<col style="width:30%">
  <col style="width:15%">
  <col style="width:35%">
   <tr> 
    <td>08:45</td>  
    <td>Introduction</td> 
    <td></td> 
    <td></td>
    <td></td>
   </tr>
   <tr> 
     <td>09:00</td>  
     <td>Formatting data tables in Spreadsheets</td> 
     <td>How do we format data in spreadsheets for effective data use?</td> 
     <td></td>
     <td><a href="https://datacarpentry.org/spreadsheet-ecology-lesson/01-format-data/index.html">Carpentries: data table </a></td>
  </tr>
  <tr> 
    <td>09:10</td>  
    <td>Excercise</td>       
    <td>How can this table be improved to start analysis in python? Excercise in breakout rooms</td>
    <td><a href="https://ndownloader.figshare.com/files/2252083">Datatable for exercise</a></td>
    <td><a href="https://datacarpentry.org/spreadsheet-ecology-lesson/02-common-mistakes/index.html">Carpentries exercise and discussion </a></td>
  </tr>
  <tr> 
    <td>09:35</td>  
    <td>Date Notation</td> 
    <td>Good approaches for handling dates in spreadsheets</td> 
    <td></td>
    <td><a href="https://datacarpentry.org/spreadsheet-ecology-lesson/03-dates-as-data/index.html">Carpentries: dates</a></td>
  </tr>
  <tr> 
    <td>09:45</td>  
    <td>Break</td> 
    <td>15 minute break</td> 
    <td></td>
    <td></td>
  </tr>
 </table>
 
 <br>
 
<h3>Part 2. Python and the Pandas library</h3>
 <table class="table table-striped">
  <col style="width:5%">
	<col style="width:15%">
	<col style="width:30%">
  <col style="width:15%">
  <col style="width:35%">
   <tr> 
        <td>10:00</td>  
        <td>Starting with Python</td> 
        <td>What is Python?<br/>Data types<br/>Mathematical operations<br/>Lists</td> 
        <td><a href="https://github.com/k-rns/2020-05-22-WHOI-online/blob/gh-pages/data/01_Python%20Basics.ipynb">Notebook: Intro to Python</a></td>
        <td><a href="https://datacarpentry.org/python-ecology-lesson/00-before-we-start/index.html">Carpentries intro to Python I</a><br><a href="https://datacarpentry.org/python-ecology-lesson/01-short-introduction-to-Python/index.html">Carpentries intro to Python II</a><br/><a href="https://github.com/WHOIGit/pandas-talk/blob/master/01%20introduction%20to%20python.ipynb">First commands, Notebook Joe Futrelle, WHOI</a></td>
    </tr>
    <tr> 
        <td>10:20</td>  
        <td>The Pandas Library</td>
        <td>What is Pandas?<br/>How do I import data<br/>What is a dataframe?<br/>How can I access specific data within my data set?</td>
        <td><a href="https://github.com/k-rns/2020-05-22-WHOI-online/blob/gh-pages/data/02_Pandas_DataFrames_Series.ipynb">Notebook: Intro to Pandas</a></td>
        <td><a href="https://datacarpentry.org/python-ecology-lesson/02-starting-with-data/index.html">Carpentries:starting with data</a><br/><a href="https://datacarpentry.org/python-ecology-lesson/03-index-slice-subset/index.html">Carpentries: Indexing, Slicing and Subsetting DataFrames in Python</a></td>
    </tr> 
    <tr> 
        <td>10:35</td>  
        <td>Excercise</td> 
        <td></td> 
        <td></td> 
        <td></td> 
   </tr>
   <tr> 
        <td>10:45</td>  
        <td>Break</td> 
        <td>15 minute break</td>
        <td></td> 
        <td></td> 
    </tr>
 </table>

<br> 
   
<h3>Part 3. Further manipulation of a data frame</h3>
 <table class="table table-striped">
  <col style="width:5%">
	<col style="width:15%">
	<col style="width:30%">
  <col style="width:15%">
  <col style="width:35%">
   <tr> 
    <td>11:00</td>  
    <td>Exploration of dataframes</td> 
    <td>Sorting<br/>Unique values<br/>Logical conditions<br/>Summary statistics<br/>Groups<br/>Merging dataframes</td>
    <td><a href="https://github.com/k-rns/2020-05-22-WHOI-online/blob/gh-pages/data/03_Data_Manipulation.ipynb">Notebook: Further manipulation of a dataframe</a></td> 
     <td>
       <a href="https://datacarpentry.org/python-ecology-lesson/02-starting-with-data/index.html">Carpentries: Statistics, groups and basic math</a>
       <br/><a href="https://datacarpentry.org/python-ecology-lesson/05-merging-data/index.html">Carpentries: merging data</a>
       <br/><a href="https://github.com/WHOIGit/pandas-talk/blob/master/05%20querying%20and%20merging%20dataframes.ipynb">Querying and mergin DFs, Notebook Joe Futrelle (WHOI)</a> 
     </td> 
   </tr>
   <tr> 
     <td>11:30</td>  
     <td>Excercise</td> 
     <td></td>
     <td></td> 
     <td></td> 
   </tr>
 
   <tr> 
    <td>11:45</td>  
    <td>Break</td> 
    <td>15 minute break</td> 
    <td></td>
    <td></td> 
   </tr>
   <tr> 
    <td>12:00</td>  
    <td>Questions?</td> 
    <td></td> 
    <td></td>
    <td></td>
   </tr>
   <tr> 
     <td>12:15</td>  
     <td>Wrap-up</td> 
     <td></td> 
     <td></td> 
     <td></td> 
   </tr>
  </table>
<br> 
  
<hr/>

{% comment %}
SETUP

Delete irrelevant sections from the setup instructions.  Each
section is inside a 'div' without any classes to make the beginning
and end easier to find.

This is the other place where people frequently make mistakes, so
please preview your site before committing, and make sure to run
'tools/check' as well.


  {% if site.carpentry == "swc" %}
  Software Carpentry
  {% elsif site.carpentry == "dc" %}
  Data Carpentry
  {% elsif site.carpentry == "lc" %}
  Library Carpentry
  {% endif %}
  
  {% if site.carpentry == "swc" %}
  {% include swc/setup.html %}
  {% elsif site.carpentry == "dc" %}
  {% include dc/setup.html %}
  {% elsif site.carpentry == "lc" %}
  {% include lc/setup.html %}
  {% endif %}
  {% endcomment %}

<h2 id="setup">Setup</h2>
<p>
  To participate in this workshop, you will need an up-to-date web browser and access access to a spreadsheet program (Excel, LibreOffice,...), Python and Jupyter notebooks. In addition you will need an up-to-date web browser. 
</p>
<p> You only need to install these programs:
  <ul>
    <li>A spreadsheet program (Excel is fine, or you can install the open source software LibreOffice)</li>
    <li>Python and Jupyter notebooks using Anaconda: <a href="https://www.anaconda.com/products/individual#download-section">https://www.anaconda.com/products/individual#download-section</a>  (python 3.7)</li>
   </ul>
Detailed set-up instructions for your software can be found <a href="https://datacarpentry.org/ecology-workshop/setup-python-workshop.html">here</a> (Instructions from Data Carpentry Ecology workshops-with Python). But only install a spreadsheet program and python and Jupyter notebooks (through Anaconda).   
</p>

<p>
  Please make sure you have installed all the required packages before the start of this workshop. We will be holding an on-line data lab with Stace Beaulieu on May 20 and can help you install the packages if necessary. </p>
  

<p>
  We maintain a list of common issues that occur during installation as a reference for instructors
  that may be useful on the
  <a href = "{{site.swc_github}}/workshop-template/wiki/Configuration-Problems-and-Solutions">Configuration Problems and Solutions wiki page</a>.
</p>


