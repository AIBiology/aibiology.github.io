---
title: "AI in Biology"
keywords: syllabus
tags: 
sidebar: home_sidebar
permalink: index.html
summary: Applications of AI in Biology
toc: false
---

## Course Description

{% include image.html max-width=400 file='ai_bio_cover.png' alt="Image of futuristic AI and Biological specimens" position="right" %}

Artificial Intelligence (AI) as a field of research has existed since at least the 1950s. After initial enthusiasm, the gains of early years slowed and AI entered what has been referred to as an AI winter, with limited progress or research for decades. Modern GPU technology and advances in algorithms has renewed interest in AI and revolutionized the field. AI is rapidly becoming ubiquitous in daily life and in diverse academic fields. This course will examine the applications of AI with particular focus on applications in Biology. We will address the question of what is AI, how intelligent computers really are and may become, where limitations still exist, and if AI is here to stay or the latest trend.

The course will attempt to provide sufficient background and foundations so that students understand the detailed workings of the AI algorithms, but will not focus on the mathematical details. This is not a computer science or mathematics course. Calculus and Linear algebra are foundational to AI, but we will gloss over the details as much as possible and students are not expected to have background knowledge of these fields.

Classes will have some lecture, though most classes will consist of live coding demos and hands-on exercises.

## Prerequisites

The course assumes a basic understanding of computer programming, and Python in particular.
If you have not taken a programming course or are new to Python, there are several LinkedIn Learning courses that will give you sufficient background to be ready for this course:

* [Programming Foundations: Fundamentals](https://www.linkedin.com/learning-login/share?forceAccount=false&redirect=https%3A%2F%2Fwww.linkedin.com%2Flearning%2Fprogramming-foundations-fundamentals-3%3Ftrk%3Dshare_ent_url&account=41282748)
  * This course is best for people with no coding experience.
  * Most of the hands-on examples are in Python
* [Python Essential Training](https://www.linkedin.com/learning/python-essential-training-2/welcome?u=41282748)
  * A good review or introduction for people who know some programming but not Python
* [Learning Python](https://www.linkedin.com/learning-login/share?forceAccount=false&redirect=https%3A%2F%2Fwww.linkedin.com%2Flearning%2Flearning-python%3Ftrk%3Dshare_ent_url&account=41282748)
  *Another option for those with some coding experience 
Note, you do not need to do all of these. Any one would get you at a good place to start the semester. We will review the basics of Python in the first weeks.

## Meeting Times

### In-person and Synchronous meetings

* **Mon, Wed, Fri 1:55pm - 2:45pm Bartram 211 and online**
* In-person sections:
  * Only those registered for the in-person sections may attend in-person
    * COVID-19 restrictions limit the capacity of the room well below the number of seats. A maximum of 10 students will be allowed to attend in-person each class.
  * If you do not attend regularly, you will be asked to change to the online section to allow others to attend in-person
  * If you know you will be absent for a class, please notify the instructors so that they can offer your seat to an online participant.
* Online sections:
  * It is expected that you will attend class synchronously
  * If possible, please have your camera on during class

* Zoom links for class and recordings of class will be posted in Canvas.

 {% include important.html content="You should make every effort to attend class synchronously. While we will post information ahead of time and will record class sessions, **during class is the best opportunity to ask questions and get help from the instructors and others in the class.**" %}

* We understand that with all that is going on, some students will need to miss classes sometimes. That is fine and we will do our best to help you catch up, but regular attendance is the best way to learn.

{% include custom/office_hours.html %}

 {% include tip.html content="Coding is not always easy. Simple solutions are not always obvious. There will be some frustration. **We expect that you will need help. You should expect that you will need help.** We want to help you! We cannot always help if you do not ask for the help you need. Please ask for help." %}

## Course Textbooks

{% include image.html file='textbook.png' alt="textbook icon" position="right" max-width=75 %}
While we will not use any one text for the course, we will use sections of these books and other resources. All will be free, open-source texts.

* [{% include inline_image.html file='PDSH-cover-small.png' alt="PDSH textbook icon" %} Python Data Science Handbook by Jake VanderPlas](https://github.com/jakevdp/PythonDataScienceHandbook)

* [{% include inline_image.html file='D2DL_cover.png' alt="D2DL textbook icon"  %} Dive into Deep Learning by Aston Zhang, Zachary Lipton, Mu Li and Alexander Smola](https://d2l.ai/)

## Course Calendar

{% include image.html file='calendar.png' alt="calendar icon" position="right" max-width=75 %}

{% include important.html content="This is subject to change, please check back frequently." %}

For readings, there may be links to pages with my notes and additional explanations on the content from the texts.

Week | Date | Reading/Assignment |Topic |
-----|------|--------------------|------|
[1](Week_01.html) | Mon, Jan 11 |  | Course introduction <BR> What is AI, what is intelligence, what AI isn’t
[1](Week_01.html) | Wed, Jan 13 | [Take the HiPerGator Account training](https://mytraining-ufshands.sumtotal.host/Core/pillarRedirect?relyingParty=LM&url=core%2Factivitydetails%2FViewActivityDetails%3FActivityId%3D50413%26UserMode%3D0)| Historical Context<br>* Origins of AI as an academic discipline.<br>* A repeating pattern: major hype and enthusiasm followed by an AI “winter”.<br>* Where are we now?<br>
[1](Week_01.html) | Fri, Jan 15 | [![PDHS Image](images/PDSH-cover-small.png) Section 5.01 of PDSH: What is Machine Learning?](https://jakevdp.github.io/PythonDataScienceHandbook/05.01-what-is-machine-learning.html) | The scope of AI (subdisciplines)<br>How smart are today’s machines, really?  (We’ll come back to this throughout the semester.)
|||
[2](Week_02.html) | Mon, Jan 18 |  | MLK: No Class
[2](Week_02.html) | Wed, Jan 20 | [![PDHS Image](images/PDSH-cover-small.png) Ch 1 of PDSH: IPython: Beyond normal Python](https://jakevdp.github.io/PythonDataScienceHandbook/) | Python Introduction<br>* Getting Started in Jupyter<br>* UFRC Overview
[2](Week_02.html) | Fri, Jan 22 | | Python Introduction<br>* Statements, variables, operations, etc.
|||
[3](Week_03.html) | Mon, Jan 25 |  | Python Functions, Good programming practices (DRY, avoid globals, etc.).
[3](Week_03.html) | Wed, Jan 27 | [![PDHS Image](images/PDSH-cover-small.png) Ch 2 of PDSH: introduction to NumPy <br>Ch 3 of PDSH: Data Manipulation with Pandas](https://jakevdp.github.io/PythonDataScienceHandbook/) | Python Pandas, numpy
[3](Week_03.html) | Fri, Jan 29 | [![PDHS Image](images/PDSH-cover-small.png) Section 5.02 of PDSH: Introducing scikit learn](https://jakevdp.github.io/PythonDataScienceHandbook/05.02-introducing-scikit-learn.html) |Python sklearn, pytorch, keras, etc.
|||
[4](Week_04.html) | Mon, Feb 1 |  | A general framework for ML (data -> features -> prediction function -> loss -> optimization)
[4](Week_04.html) | Wed, Feb 3 |  | Hands on data
[4](Week_04.html) | Fri, Feb 5 |  | Hands on prediction, loss, optimization
|||
[5](Week_05.html) | Mon, Feb 8 |  | Classical statistics revisited<br>* Statistical models as ML<br>* Bias/variance tradeoff and regularization<br>* Logistic regression and classification (including classification metrics)
[5](Week_05.html) | Wed, Feb 10 |  | [Hands on regression analysis](https://github.com/UFResearchComputing/Understanding_PyTorch)
[5](Week_05.html) | Fri, Feb 12 |  | Hands on
|||
[6](Week_06.html) | Mon, Feb 15 |  | Tree-Based Models
[6](Week_06.html) | Wed, Feb 17 |  | Hands on Tree-Based Models
[6](Week_06.html) | Fri, Feb 19 |  | Hands on Tree-Based Models
|||
[7](Week_07.html) | Mon, Feb 22 |  | Support vector machines
[7](Week_07.html) | Wed, Feb 24 |  | Hands on Support vector machines
[7](Week_07.html) | Fri, Feb 26 |  | Hands on Support vector machines
|||
[8](Week_08.html) | Mon, Mar 1 |  | Supervised vs. unsupervised learning
[8](Week_08.html) | Wed, Mar 2 |  | Intro. to unsupervised methods
[8](Week_08.html) | Fri, Mar 5 |  | Intro. to unsupervised methods
|||
[9](Week_09.html) | Mon, Mar 8 |  | Neural Networks
[9](Week_09.html) | Wed, Mar 10 |  | Neural Networks
[9](Week_09.html) | Fri, Mar 12 |  | Neural Networks
|||
[10](Week_10.html) | Mon, Mar 15 |  | CNNs for medical image analysis
[10](Week_10.html) | Wed, Mar 17 |  | CNNs for image segmentation
[10](Week_10.html) | Fri, Mar 19 |  | Additional hands on with CNNs
|||
[11](Week_11.html) | Mon, Mar 22 |  | Symbolic AI
[11](Week_11.html) | Wed, Mar 24 |  | Symbolic AI
[11](Week_11.html) | Fri, Mar 26 |  | Symbolic AI
|||
[12](Week_12.html) | Mon, Mar 29 |  | Symbolic AI
[12](Week_12.html) | Wed, Mar 31 |  | Symbolic AI
[12](Week_12.html) | Fri, Apr 2 |  | Symbolic AI
|||
[13](Week_13.html) | Mon, Apr 5 |  | Topics TBD
[13](Week_13.html) | Wed, Apr 7 |  | Topics TBD
[13](Week_13.html) | Fri, Apr 9 |  | Topics TBD
|||
[14](Week_14.html) | Mon, Apr 12 |  | Topics TBD
[14](Week_14.html) | Wed, Apr 14 |  | Topics TBD
[14](Week_14.html) | Fri, Apr 16 |  | Topics TBD
|||
[15](Week_14.html) | Mon, Apr 19 |  | Topics TBD
[15](Week_14.html) | Wed, Apr 21 |  | Last day of class
|||

## Software and Hardware

Participants will need a computer with internet connection, webcam and microphone for all classes.

Several free/open source software packages will be used throughout the course, and students will be required to install some of these.
Students will use a (free) Research Computing account to access HiPerGator for coursework.
Students will be required to apply for a (free) Github.com account for coursework.

If you have technical difficulties with Canvas, please contact the UF Helpdesk at:

* http://helpdesk.ufl.edu
* (352) 392-HELP (4357)
* Walk-in: HUB 132

Any requests for make-ups due to technical issues should be accompanied by the ticket number received from the Help Desk when the problem was reported to them. The ticket number will document the time and date of the problem. Please e-mail the instructor within 24 hours of the technical difficulty if you wish to request a make-up.

All faculty, staff and student of the University are required and expected to obey the laws and legal agreements governing software use. Failure to do so can lead to monetary damages and/or criminal penalties for the individual violator. Because such violations are also against University policies and rules, disciplinary action will be taken as appropriate.

## Grading

See also the [List of Graded Work page](Grading.html).

### Assignment Values

**Tentative: Final grading scheme not determined**

* **Quizzes**: 6 @ 20 points each: 120 points (37%)
* **Problem Sets**: 5 @ 20 points each: 100 points (30%)
* **Class Projects**: 2 @ 40 points each: 80 points (24%)
* **Class Participation** 30 points: 30 points (9%)
  * 5 points for GitHub account assignment
  * 10 points for github commits
  * 15 points for code peer review


Grading in this class is consistent with UF policies available at: [https://catalog.ufl.edu/UGRD/academic-regulations/grades-grading-policies/]( https://catalog.ufl.edu/UGRD/academic-regulations/grades-grading-policies/)

<div class="panel-group" id="accordion">
    <div class="panel panel-default">
        <div class="panel-heading">
            <a class="noCrossRef accordion-toggle" data-toggle="collapse" data-parent="#accordion" href="#collapseA"> <H3>Grade Disputes</H3></a>
        </div>
        <!-- /.panel-heading--> 
        <div id="collapseA" class="panel-collapse collapse noCrossRef">
            <div class="panel-body">
                Should a student wish to dispute any grade received in this class (other than simple addition errors), the dispute must be in writing (via email) and be submitted to the instructor within a week of receiving the grade.
                <BR><BR>
                The dispute should clearly set out the grade that the student believes the assignment should have received as well as why they believe that they should have received such a grade.
            </div>
            <!-- /.panel-body -->
        </div>
        <!-- /.panel-collapse -->
    </div>
    <!-- /.panel-default -->
</div>
<!-- /.panel-group -->

<div class="panel-group" id="accordion">
    <div class="panel panel-default">
        <div class="panel-heading">
            <a class="noCrossRef accordion-toggle" data-toggle="collapse" data-parent="#accordion" href="#collapseB"> <H3>Grading Scale and GPA Equivalent</H3></a>
        </div>
        <!-- /.panel-heading--> 
        <div id="collapseB" class="panel-collapse collapse noCrossRef">
            <div class="panel-body">
                <table>
                  <thead>
                    <tr>
                      <th>A</th>
                      <th>A-</th>
                      <th>B+</th>
                      <th>B</th>
                      <th>B-</th>
                      <th>C+</th>
                      <th>C</th>
                      <th>C-</th>
                      <th>D+</th>
                      <th>D</th>
                      <th>D-</th>
                      <th>F</th>
                    </tr>
                  </thead>
                  <tbody>
                    <tr>
                      <td>100-93<br />(4.0)</td>
                      <td>&lt;93-90<br />(3.67)</td>
                      <td>&lt;90-87<br />(3.33)</td>
                      <td>&lt;87-83<br />(3.0)</td>
                      <td>&lt;83-80<br />(2.67)</td>
                      <td>&lt;80-77<br />(2.33)</td>
                      <td>&lt;77-73<br />(2.0)</td>
                      <td>&lt;73-70<br />(1.67)</td>
                      <td>&lt;70-67<br />(1.33)</td>
                      <td>&lt;67-63<br />(1.0)</td>
                      <td>&lt;63-60<br />(0.67)</td>
                      <td>&lt;60<br />(0)</td>
                    </tr>
                  </tbody>
                </table>
                <B>Note:</B> A grade of C- is not a qualifying grade for major, minor, Gen Ed, or College Basic distribution credit. For further information on UF's Grading Policy, see:
                <a href="https://catalog.ufl.edu/UGRD/academic-regulations/grades-grading-policies/">https://catalog.ufl.edu/UGRD/academic-regulations/grades-grading-policies/</a>
            </div>
            <!-- /.panel-body -->
        </div>
        <!-- /.panel-collapse -->
    </div>
    <!-- /.panel-default -->
</div>
<!-- /.panel-group -->

## Course Policies

### Class Attendance and Makeup Policy

Requirements for class attendance and makeup assignments, and other work in this course are consistent with university policies that can be found in the online catalog at: [https://catalog.ufl.edu/UGRD/academic-regulations/attendance-policies/](https://catalog.ufl.edu/UGRD/academic-regulations/attendance-policies/)

In general, we do not take attendance. You are all adults and we assume you are taking the class the learn. **The best way to learn is to regularly attend class.** We are sure students will miss class for various reasons. We are happy to help you catch up. If you regularly miss class and fall behind, we may ask that you hold questions on content you have missed until after class, or ask that you coordinate a time to go over the content. We will make every effort to record and post all classes to help those that miss classes.

### Quiz and Assignment Policy

Quiz and assignment dates will be announced at least one week in advance and students will have at least three days to complete the quiz or assignment. Each quiz or assignment will clearly state if it is an individual or group assignment.  Individual assignments must be the student’s own work, completed without the assistance of others.

All quizzes and assignments are "open book, open internet", you may use whatever resources you desire to complete the quiz/assignment. Though only assignments specifically noted as group assignments should be worked on with other people.

### Makeup and Late policy

Please notify the instructors of circumstances that lead to late work or missed classes. We will generally work with you and accept late work. Without prior notification, late work will be penalized one point per day after the due date.

## Students Requiring Accommodations

Students with disabilities requesting accommodations should first register with the Disability Resource Center (352-392-8565, [https://disability.ufl.edu/students/get-started/](https://disability.ufl.edu/students/get-started/)) by providing appropriate documentation. Once registered, students will receive an accommodation letter which must be presented to the instructor when requesting accommodation. Students with disabilities should follow this procedure as early as possible in the semester.

## Course Evaluation

Students are expected to provide professional and respectful feedback on the quality of instruction in this course by completing course evaluations online via GatorEvals. Guidance on how to give feedback in a professional and respectful manner is available at [gatorevals.aa.ufl.edu/students/](https://gatorevals.aa.ufl.edu/students/). Students will be notified when the evaluation period opens, and can complete evaluations through the email they receive from GatorEvals, in their Canvas course menu under GatorEvals, or via [ufl.bluera.com/ufl/](https://ufl.bluera.com/ufl/). Summaries of course evaluation results are available to students at [gatorevals.aa.ufl.edu/public-results/](https://gatorevals.aa.ufl.edu/public-results/).

## Class Demeanor and Netiquette

Students are expected to be in class or join the class Zoom meeting on time and behave in a manner that is respectful to the instructors and to fellow students. For remote participants, if at all possible, please have your video on during class--it is easier for us to teach and for discussion if we can see you! Please do be aware of your surroundings and ensure that content visible on your video, or shared via screen sharing, is appropriate for class.

Opinions held by other students should be respected in discussion, and conversations that do not contribute to the discussion should be held at minimum, if at all.

Students should be working on course content during class.

### Discussion Boards and Slack Channel

The Canvas discussion boards and Microsoft Teams can be used to ask for and provide help by all. Students should be supportive and considerate of others at all times. Rude or inappropriate comments will be removed and the poster will be warned.

## University Honesty Policy

UF students are bound by The Honor Pledge which states:
>We, the members of the University of Florida community, pledge to hold ourselves and our peers to the highest standards of honor and integrity by abiding by the Honor Code. On all work submitted for credit by students at the University of Florida, the following pledge is either required or implied: “On my honor, I have neither given nor received unauthorized aid in doing this assignment.”

[The Honor Code](https://sccr.dso.ufl.edu/policies/student-honor-code-student-conduct-code/) specifies a number of behaviors that are in violation of this code and the possible sanctions. Furthermore, you are obligated to report any condition that facilitates academic misconduct to appropriate personnel. If you have any questions or concerns, please consult with the instructor or TAs in this class

<div class="panel-group" id="accordion">
    <div class="panel panel-default">
        <div class="panel-heading">
            <a class="noCrossRef accordion-toggle" data-toggle="collapse" data-parent="#accordion" href="#collapseC"> <H2> Health and Wellness</H2></a>
        </div>
        <!-- /.panel-heading--> 
        <div id="collapseC" class="panel-collapse collapse noCrossRef">
            <div class="panel-body">
              Resources are available on-campus for students having personal problems or lacking clear career and academic goals. The resources include:
              <ul>
                <li><b>UF Counseling & Wellness Center</b>, 3190 Radio Rd, 392-1575, psychological and psychiatric services.</li>
                <ul>
                  <li>Provides counseling and support as well as crisis and wellness services including a variety of workshops throughout the semester (e.g., Yappy Hour, Relaxation and Resilience).</li>
                  <li>Many students experience test anxiety and other stress related problems. “A Self Help Guide for Students” is available through the Counseling Center (301 Peabody Hall, 392-1575) and at their web site: <a href="https://counseling.ufl.edu/">https://counseling.ufl.edu/</a>.</li>
                  <li>U Matter, We Care: If you or a friend is in distress, please contact umatter@ufl.edu or 352 392-1575 so that a team member can reach out to the student.</li>
                </ul>
                <li><b>Career Connections Center</b>, Reitz Union, 392-1601, CareerCenterMarketing@ufsa.ufl.edu, connects job seekers with employers and offers guidance to enrich your collegiate experience and prepare you for life after graduation.</li>
                <li><b>University Police Department</b>: 392-1111 or 9-1-1 for emergencies. <a href="http://www.police.ufl.edu/">https://www.police.ufl.edu/</a></li>
                <li><b>Sexual Assault Recovery Services (SARS)</b>: Student Health Care Center, 392-1161.</li>
                <li><b>Student Health Care Center</b>: Call 352-392-1161 for 24/7 information to help you find the care you need, or visit <a href="https://shcc.ufl.edu">https://shcc.ufl.edu/</a></li>
                <li><b>Food insecurity</b>: The Pantry is a resource on the University of Florida campus committed to supporting students, staff, and faculty who are experiencing food insecurity. These individuals do not have reliable access to nutritious foods for themselves and their families. If you, or anyone you know, is experiencing food insecurity, the Pantry is a resource to visit. We offer non-perishable food, toiletries and fresh produce grown at the Field and Fork Gardens during certain times of the year. There is no proof of need required in order to shop at the Pantry; you must only bring in your valid UFID card. At the Pantry, we know that a good meal makes for a good student, and we work to support all Gators who are experiencing food insecurity. <a href="https://pantry.fieldandfork.ufl.edu/">Field & Fork Food Pantry</a>.</li>
              </ul>
            </div>
            <!-- /.panel-body -->
        </div>
        <!-- /.panel-collapse -->
    </div>
    <!-- /.panel-default -->
</div>
<!-- /.panel-group -->

## Inclusive Learning Environment

This course embraces the University of Florida’s Non-Discrimination Policy, which reads:
> The University shall actively promote equal opportunity policies and practices conforming to laws against discrimination. The University is committed to nondiscrimination with respect to race, creed, color, religion, age, disability, sex, sexual orientation, gender identity and expression, marital status, national origin, political opinions or affiliations, genetic information and veteran status as protected under the Vietnam Era Veterans’ Readjustment Assistance Act.

If you have questions or concerns about your rights and responsibilities for inclusive learning environment, please see the instructor or refer to the Office of Multicultural & Diversity Affairs website: [http://multicultural.ufl.edu](http://multicultural.ufl.edu).

## Privacy

There are federal laws protecting your privacy with regards to grades earned in courses and on individual assignments. For more information, please see: [https://registrar.ufl.edu/ferpa.html](https://registrar.ufl.edu/ferpa.html)

## Statement Regarding Course Recording

Our class sessions may be audio visually recorded for students in the class to refer back to and for use of enrolled students who are unable to attend live. Students who participate with their camera engaged or utilize a profile image are agreeing to have their video or image recorded. If you are unwilling to consent to have your profile or video image recorded, keep your camera off and do not use a profile image. Likewise, students who un-mute during class and participate verbally are agreeing to have their voices recorded.  If you are unwilling to consent to have your voice recorded during class, you will need to keep your mute button activated.  As in all courses, unauthorized recording and unauthorized sharing of recorded materials is prohibited.

<div class="panel-group" id="accordion">
    <div class="panel panel-default">
        <div class="panel-heading">
            <a class="noCrossRef accordion-toggle" data-toggle="collapse" data-parent="#accordion" href="#collapseD"> <H2> Additional UF Policies and Resources</H2></a>
        </div>
        <!-- /.panel-heading--> 
        <div id="collapseD" class="panel-collapse collapse noCrossRef">
            <div class="panel-body">
                <h3>Dean of Students Office</h3>
                <a href="https://dso.ufl.edu/">Dean of Students Office</a> (352-392-1261) provides a variety of services to students and families, including <a href="https://dso.ufl.edu/areas_services/hitchcock-field-fork-pantry/">Field and Fork</a> (UF&rsquo;s food pantry) and <a href="https://dso.ufl.edu/areas_services/new-student-family-programs/">New Student and Family programs</a></p>
                <h3>Disability Resource Center</h3>
                <ul>
                  <li><a href="https://disability.ufl.edu/students/get-started/">Disability Resource Center</a> (<a href="mailto:DRCaccessUF@ufsa.ufl.edu">DRCaccessUF@ufsa.ufl.edu</a> | 352-392-8565) helps to provide an accessible learning environment for all by providing support services and facilitating accommodations, which may vary from course to course. Once registered with DRC, students will receive an accommodation letter that must be presented to the instructor when requesting accommodations. Students should follow this procedure as early as possible in the semester.</li>
                </ul>
                <h3>Multicultural and Diversity Affairs</h3>
                <p><a href="https://multicultural.ufl.edu/">Multicultural and Diversity Affairs</a> (352-294-7850) celebrates and empowers diverse communities and advocates for an inclusive campus.</p>
                <h3>Office of Student Veteran Services</h3>
                <p><a href="http://veterans.ufl.edu/">Office of Student Veteran Services</a> (352-294-2948 | <a href="mailto:vacounselor@ufl.edu">vacounselor@ufl.edu</a>) assists student military veterans with access to benefits.</p>
                <h3>ONE.UF</h3>
                <p><a href="https://one.uf.edu/">ONE.UF</a> is the home of all the student self-service applications, including access to:</p>
                <ul>
                  <li><a href="http://www.ufadvising.ufl.edu/">Advising</a></li>
                  <li><a href="http://www.fa.ufl.edu/bursar/">Bursar</a> (352-392-0181)</li>
                  <li><a href="https://www.sfa.ufl.edu/">Financial Aid</a> (352-392-1275)</li>
                  <li><a href="https://registrar.ufl.edu/">Registrar</a> (352-392-1374)</li>
                </ul>
                <h3>Official Sources of Rules and Regulations</h3>
                <p>The official source of rules and regulations for UF students is the <a href="https://catalog.ufl.edu/UGRD/">Undergraduate Catalog</a> and <a href="http://gradcatalog.ufl.edu/">Graduate Catalog</a>. Quick links to other information have also been provided below.</p>
                <ul>
                  <li><a href="https://dso.ufl.edu/resources/student-handbook/">Student Handbook</a></li>
                  <li><a href="https://catalog.ufl.edu/UGRD/student-responsibilities/">Student Responsibilities</a>, including academic honesty and student conduct code</li>
                  <li><a href="https://elearning.ufl.edu/supported-services/">e-Learning Supported Services Policies</a> includes links to relevant policies including Acceptable Use, Privacy, and many more</li>
                  <li><a href="https://accessibility.ufl.edu/">Accessibility</a>, including the Electronic Information Technology Accessibility Policy and ADA Compliance</li>
                  <li><a href="https://it.ufl.edu/policies/student-computing-requirements/">Student Computing Requirements</a>, including minimum and recommended technology requirements and competencies</li>
                </ul>
            </div>
            <!-- /.panel-body -->
        </div>
        <!-- /.panel-collapse -->
    </div>
    <!-- /.panel-default -->
</div>
<!-- /.panel-group -->