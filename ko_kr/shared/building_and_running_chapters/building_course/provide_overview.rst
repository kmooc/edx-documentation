.. _Providing a Course Overview:

#####################################
강좌 개요
#####################################


**********
개관
**********

학습자는 이 강좌에서 어떤 주제를 다루며, 매주 강좌에 얼마나 많은 시간을 들여야 하는지, 강좌가 어떤 사전 지식을 필요로 하는지 등 강좌에 대한 자세한 정보를 알고 싶어한다. 강좌 운영팀은 Studio에서 이러한 정보를 입력할 수 있다. 

이에 대해 다음 항목에 상세하게 안내되어 있다.

* :ref:`Describe Your Course`
* :ref:`Add a Course Image`
* :ref:`Add a Course Video`
* :ref:`Set Course Time Requirements`
* :ref:`Set Course Prerequisites`
* :ref:`Set Important Dates for Your Course`

수강을 고민하는 학습자에게 필요한 정보의 대부분이 강좌 요약 페이지라고 불리기도 하는 강좌 소개 페이지에 나와 있다. 다음 이미지는 일반적인 강좌 소개 페이지를 보여준다.

.. image:: ../../../shared/building_and_running_chapters/Images/about_page.png
 :width: 600
 :alt: An image of the course About page showing the course start and end dates,
     prerequisites, description, and other information

학습자는 강좌를 수강하기 전에 강좌 소개 페이지를 보게 되고, 수강신청을 한 후에는 학습자 대시보드에서 강좌에 대한 정보를 볼 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/dashboard.png
 :width: 600
 :alt: An image of the dashboard showing courses with start and end dates

.. 참고:: 강좌 개관, 이미지, 동영상 등 강좌 소개 콘텐츠를 추가하기 전에, K-MOOC 플랫폼 관리자와 상의해야 할 필요가 있을 수 있다. 더 자세한 내용은 edX101에 About page lesson 을 참조하도록 한다.


.. _Describe Your Course:

*********************************
강좌 안내하기
*********************************

강좌 개관에서는 강좌에 관해 개략적인 설명을 하게 된다. 강좌에 관심이 있는 학습자를 위한 중요한 정보로, 강좌의 주요 주제와 주요 개념을 소개한다. 또한 수강을 위한 조건이나 교수자 및 강좌 운영팀에 관한 정보를 포함하기도 한다.

강좌 소개 페이지에 강좌 개관이 다음과 같이 나타나게 된다.

.. image:: ../../../shared/building_and_running_chapters/Images/about-page-course-description.png
 :width: 600
 :alt: Image of a course About page with the overview circled

강좌 운영팀은 Studio에서 HTML을 사용하여 **강좌 개관** 을 입력하게 된다. 스튜디오에서 강좌 개관 입력 필드는 자리 표시자(placeholders) 등 상용구(boilerplate)를 포함한다.

다음 순서로, 강좌 개관에 내용을 입력할 수 있다.

#. **설정**  메뉴에서 **기본 설정** 을 선택한다.
#. **강좌 소개** 가 보일 때까지 스크을 내린 후, 
   **강좌 개관** 영역을 찾는다.

  .. image:: ../../../shared/building_and_running_chapters/Images/course_overview.png
   :width: 600
   :alt: Image of the HTML course description.

3. 강좌 개관을 만들기 위해 상용구 텍스트에 자리 표시자를 대체한다. 
   스튜디오는 자동으로 변경 사항을 저장한다.

   .. 참고:: 상용구의 HTML 태그를 편집하지 않도록 한다. 이 태그가 강좌 소개 페이지의 
    콘텐츠를 조절하기 때문이다.
 
4. **강좌 개요** 영역 아래에 있는 **강좌 영역** 링크를 클릭하면 
   새 창/탭에서 열리며 화면에 어떻게 나타나게 되는지 알 수 있다. 

   수정할 경우, 수정 사항을 자동 저장하는데 시간이 필요하므로 잠시 기다려야 한다.


.. _Add a Course Image:

************************
강좌 대표 이미지 추가하기
************************

강좌 운영팀은 강좌를 나타낼 강좌 대표 이미지를 추가할 수 있다. 스튜디오에서 추가한 강좌 이미지는 학습자 대시보드에 나타난다. Edge에서는 강좌 소개 페이지에 강좌 대표 이미지가 나타난다.

.. image:: ../../../shared/building_and_running_chapters/Images/dashboard-course-image.png
 :width: 600
 :alt: Image of the course image in the student dashboard

강좌 대표 이미지는 최소 660px너비에서 240px 높이로, .jpg 또는.png 형식이어야 한다. 

다음  단계에 따라, 강좌 대표 이미지를 추가할 수 있다.

#. **설정** 메뉴에서, **기본 설정** 을 클릭한다.
#. **강좌 대표 이미지** 가 보일 때까지 스크롤을 내린다.
#. **강좌 대표 이미지 업로드**를 클릭해 컴퓨터에서 이미지를 선택한다.
#. 대시보드에서 이미지가 학습자에게 어떻게 나타나는지 살펴본다.

.. _Add a Course Video:

*********************************
강좌 소개 영상 추가하기
*********************************

수강을 고민하는 학습자의 관심을 유도할 수 있게, 각 강좌는 강좌 소개 영상을 보여줄 수 있다. 소개 영상에 이 강좌만의 특징을 강조하면 더욱 좋다.

.. image:: ../../../shared/building_and_running_chapters/Images/about-page-course-video.png
 :alt: Image of the course video in the course About page.

동영상이 다음과 같은 질문에 답할 수 있다면 좋다.

* Who is teaching the course?
* 어떤 대학이 이 강좌를 제공하는가?
* 강좌가 어떤 주제 및 개념을 포함하고 있는가? 
* 왜 학습자가 이 강좌를 수강해야 하는가? 

2 분 이하의 재생 시간 동안, 동영상이 위 내용을 간결하게 담고 있어야 한다.

강좌 운영팀은 강좌 소개 동영상이 강좌 콘텐츠 동영상과 같이 Compression Specifications(압축 사양)및 Video Formats(동영상 형식) 지침을 따르는지 확인해야 한다. 

강좌 소개 동영상을 추가 하려면,


#. YouTube에 강좌 동영상을 업로드한다. URL에서 **watch?v =** 와 **&feature** 사이에 나타나는 
코드를 기록한다. 이 코드는 아래에 표시된 상자에 있다.

  .. image:: ../../../shared/building_and_running_chapters/Images/image127.png
    :alt: Image of a sample course video
    
2. **설정** 메뉴에서, **기본 설정** 을 입력한다.
#. **강좌 소개 영상** 이 나타날 때까지 스크롤을 내린다.
#. 동영상 박스 아래 영역에, YouTube video ID (위 1단계에서 복사한 코드)를 입력한다. 코드를 추가하면, 동영상이 동영상 박스에서 자동으로 재생된다. Studio가 자동으로 변경 사항을 저장한다.


.. _Set Course Time Requirements:

************************************
Set Course Time Requirements
************************************

To specify the number of hours that you expect students to spend on the course
each week, follow these steps.

#. From the **Settings** menu, select **Schedule & Details**.
#. Scroll down to the **Requirements** section.
#. In the **Hours of Effort per Week** field, enter the number of hours you
   expect students to work on this course each week.
#. View your course About page to see how the requirements will appear to
   students.


.. _Set Course Prerequisites:

********************************************
Set Course Prerequisites
********************************************

You might want to make sure that your students have a specific set of skills and
knowledge before they take your course. In addition to suggesting general
requirements in your course overview, you can require students to :ref:`complete
specific prerequisite courses<Specify Prerequisite Courses>`, or :ref:`take an
entrance exam<Require an Entrance Exam>`, or both.


.. _Specify Prerequisite Courses:

===================================
Specify Prerequisite Courses
===================================

You can require that your students pass a particular edX course before they
enroll in your course. Students see information about course prerequisites on
the course About page.

.. image:: ../../../shared/building_and_running_chapters/Images/PrereqAboutPage.png
  :width: 500
  :alt: A course About page with prerequisite course information circled

If students have not completed the prerequisite course, they can enroll in your
course and then see your course on the Student Dashboard. However, unlike with
other courses, the Student Dashboard does not provide a link to the courseware.
The Student Dashboard includes a link to the About page for the prerequisite
course. Students can enroll in the prerequisite course from the About page.

.. image:: ../../../shared/building_and_running_chapters/Images/Prereq_StudentDashboard.png
  :width: 500
  :alt: The Student Dashboard with an available course and a course that is
      unavailable because it has a prerequisite

To specify a prerequisite course, you must be a course author in both the
current course and in the prerequisite course.

#. In Studio, open your course.
#. On the **Settings** menu, select **Schedule & Details**.
#. On the **Schedule & Details** page, scroll to the **Requirements** section.
#. Under **Prerequisite Course**, click the drop-down list to select a course.
#. At the bottom of the page, select **Save Changes**.

.. note:: Currently, you can specify only one prerequisite course.


.. _Require an Entrance Exam:

===================================
Require an Entrance Exam
===================================

You can require your students to pass an entrance exam before they access your
course materials. If you include an entrance exam, students who enroll in your 
course see only the **Course Updates & News** page and an **Entrance Exam** tab 
until they pass the exam.

.. image:: ../../../shared/building_and_running_chapters/Images/EntEx_LandingPage.png
  :width: 500
  :alt: The Course Updates & News page with the Entrance Exam tab circled on the
      left


After students pass the exam, they can access all released materials in your 
course. 

To require an entrance exam, follow these steps.

#. In Studio, open your course.
#. On the **Settings** menu, select **Schedule & Details**.
#. On the **Schedule & Details** page, scroll to the **Requirements** section.
#. Select the **Require students to pass an exam before accessing course
   materials** check box.
#. At the bottom of the page, select **Save Changes**.

After you save your changes, Studio automatically creates an **Entrance Exam** 
section in your course outline. To add content to your entrance exam, go to the 
course outline. 

Best Practices for Entrance Exams
********************************************

We strongly recommend that you follow several guidelines to help you and your
students have a positive experience with entrance exams.

* Make sure that your beta testers include the entrance exam when they test your
  other course content.

* Make sure that you mention the entrance exam in the course description on your
  course About page. Otherwise, students will not know about the entrance exam
  before they enroll in your course and try to access course content.

* Add an anouncement at the top of the **Course Updates & News** page that
  contains information and instructions for students who need to take the exam.
  When students first try to access content in a course that has an entrance
  exam, they see the **Course Updates & News** page. We suggest that you include
  the following information.

  * To begin the course entrance exam, students click the **Entrance Exam** tab
    on the left side of the screen.

  * After students complete the entrance exam, they have to click the **Entrance
    Exam** tab again or refresh the page in their browser. When the page
    refreshes, students can see all currently available course content.

    .. image:: ../../../shared/building_and_running_chapters/Images/EntEx_CourseAccordionAfterPass.png
      :width: 500
      :alt: The student view after the student has passed the entrance exam,
          with all available course sections listed in the course accordion


Create an Entrance Exam from the Course Outline
**************************************************

You create your course entrance exam from the course outline in Studio. Creating
entrance exam content is just like creating other course content. For more
information, see :ref:`Creating Course Content Index`.

Adjust Scores in the Entrance Exam
********************************************

If you find an error in the exam after students have taken it, and corrections
to the exam are unavoidable, you have several options to rescore the exam for
individual students. These options are available on the Instructor Dashboard.

On the Instructor Dashboard, click **Student Admin**, and then scroll to the
**Entrance Exam Grade Adjustment** section. The following options are available.

* **Reset Student Attempts**: Reset the value for one particular student's
  attempts back to zero so that the student can begin work over again. For more
  information, see :ref:`reset_attempts`.

* **Rescore Student Submission**: Rescore the responses that a student has
  submitted. For more information, see :ref:`rescore`.

* **Delete Student State for Problem**: Delete a student's entire history for
  the exam from the database. For more information, see :ref:`delete_state`.

Another option on the Instructor Dashboard is **Show Background Task History for
Student**. If you reset student attempts, rescore student submissions, or delete
student state, the operation runs in the background. If you want to see a record
of all the operations that have run for the entrance exam, select **Show
Background Task History for Student**.



.. _Set Important Dates for Your Course:

***********************************
Set Important Dates for Your Course
***********************************

You must set dates and times for enrollment and for the course.

#. In Studio, from the **Settings** menu, select **Schedule and Details**.  
#. Follow the on-screen text to enter the course and enrollment schedule.

   .. image:: ../../../shared/building_and_running_chapters/Images/schedule.png
    :width: 450
    :alt: An image of the course schedule page.


.. note:: The **Time** fields on this page, and the times that students 
 see, use Universal Coordinated Time (UTC).

.. _The Course Start Date:

=======================
The Course Start Date
=======================


.. note:: The default course start date is set far into the future, to
 **01/01/2030**. This is to ensure that your course does not start before
 you intend it to. You must change the course start date to the date you want
 students to begin using the course.

Students see the course start date and time on their **Current Courses**
dashboards and on the course About page. Students can see some parts of the
course before the course start date. For example, students can see your **Course
Info** page and course-wide discussion topics as soon as they enroll in your
course. For more information about course-wide discussion topics, see
:ref:`Create CourseWide Discussion Topics`.

The following example shows the course start date and time on the course About
page:

.. image:: ../../../shared/building_and_running_chapters/Images/about-page-course-start.png
 :width: 600
 :alt: An image of the course About page, with the start date circled.

In the dashboard, students see the start dates and times for each of their
courses, as in the following examples.

.. image:: ../../../shared/building_and_running_chapters/Images/dashboard-course-to-start.png
 :width: 600
 :alt: An image of two courses in the student dashboard, with the start dates
     and times circled.

.. note:: If you do not specify a start time for your course, students see
   the default start time, 00:00 Coordinated Universal Time (UTC).


.. _Set the Advertised Start Date:

======================================
Set the Advertised Start Date
======================================

You can set an advertised start date for your course that is different than the
course start date you set in the **Schedule and Details** page. You may want to
do this if there is uncertainty about the exact start date. For example, you
could advertise the start date as **Spring, 2014**.

To set an advertised start date:

#. From the **Settings** menu, select **Advanced Settings**.
#. Find the **Course Advertised Start Date** policy key. The default value is
   **null**.
#. Enter the value you want to display as the advertised start date. You can
   use any string, enclosed in double quotation marks. If you format the string
   as a date (for example, as 02/01/2014), the value is parsed and presented to
   students as a date.

  .. image:: ../../../shared/building_and_running_chapters/Images/advertised_start.png
   :alt: Image of the advertised start date policy key with a value of "anytime,
       self-paced"

4. Click **Save Changes** at the bottom of the page.

The start date shown on the dashboard is now the value of the **Course
Advertised Start Date** policy key:

.. image:: ../../../shared/building_and_running_chapters/Images/dashboard-course_adver_start.png
 :width: 600
 :alt: An image of a course listing in the student dashboard, with the
     advertised start date circled.

If you do not change the default course start date (01/01/2030), and the
**Course Advertised Start Date** policy value is ``null``, then the student
dashboard does not list a start date for the course. Students just see that
the course has not yet started.

.. _The Course End Date:

=====================
The Course End Date
=====================

The course end date is the date after which students can no longer earn credit
toward certificates. Students who have earned certificates can view them after
the course end date.

.. important::
 If you do not set a course end date, students will not be able to access
 earned certificates.

After grades and certificates are finalized, students see the course end date
on their personal **Current Courses** dashboards, as shown in the following
examples.

* If grades and certificates are not yet finalized, students can see the course
  end date and a message:

  .. image:: ../../../shared/building_and_running_chapters/Images/dashboard-wrapping-course.png
   :alt: Image of a course on the student dashboard that has ended, but not
     been graded

* When grades and certificates are finalized, students who have not earned a
  certificate see their score and the score required to earn a certificate:
  
  .. image:: ../../../shared/building_and_running_chapters/Images/dashboard-no-cert-course.png
   :alt: Image of a course on the student dashboard that has ended, but not
     been graded

* Students whose final score is equal to or higher than the required score can
  click **Download Certificate** to get their certificates as PDFs:

  .. image:: ../../../shared/building_and_running_chapters/Images/dashboard-completed-course.png
   :alt: Image of a course on the student dashboard that has ended, but not
     been graded

