.. _Providing a Course Overview:

#####################################
강좌 개요 설정하기
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

강좌 개요에서는 강좌에 관해 개략적으로 설명한다. 강좌에 관심이 있는 학습자를 위한 중요한 정보를 주며, 강좌의 주요 주제와 주요 개념을 소개한다. 또한 수강을 위한 조건이나 교수자 및 강좌 운영팀에 관한 정보를 포함하기도 한다.

강좌 소개 페이지에 강좌 개요가 다음과 같이 나타나게 된다.

.. image:: ../../../shared/building_and_running_chapters/Images/about-page-course-description.png
 :width: 600
 :alt: Image of a course About page with the overview circled

강좌 운영팀은 Studio에서 HTML을 사용하여 **강좌 개요** 를 입력하게 된다. Studio에서 강좌 개요 입력 필드는 자리 표시자(placeholders) 등 상용구(boilerplate)를 포함한다.

다음 순서로, 강좌 개요에 내용을 입력할 수 있다.

#. **설정**  메뉴에서 **기본 설정** 을 선택한다.
#. **강좌 소개** 가 보일 때까지 스크을 내린 후, 
   **강좌 개요** 영역을 찾는다.

  .. image:: ../../../shared/building_and_running_chapters/Images/course_overview.png
   :width: 600
   :alt: Image of the HTML course description.

3. 강좌 개요를 만들기 위해 상용구 텍스트에 자리 표시자를 대체한다. 
   스튜디오는 자동으로 변경사항을 저장한다.

   .. 참고:: 상용구의 HTML 태그를 편집하지 않도록 한다. 이 태그가 강좌 소개 페이지의 
    콘텐츠를 조절하기 때문이다.
 
4. **강좌 개요** 영역 아래에 있는 **강좌 영역** 링크를 클릭하면 
   새 창/탭에서 열리며 화면에 어떻게 나타나게 되는지 알 수 있다. 

   수정할 경우, 수정 사항을 자동 저장하는데 시간이 필요하므로 잠시 기다려야 한다.


.. _Add a Course Image:

************************
강좌 대표 이미지 추가하기
************************

강좌를 나타낼 강좌 대표 이미지를 추가할 수 있다. Studio에서 추가한 강좌 이미지는 학습자 대시보드에 나타난다. Edge에서는 강좌 소개 페이지에 강좌 대표 이미지가 나타난다.

.. image:: ../../../shared/building_and_running_chapters/Images/dashboard-course-image.png
 :width: 600
 :alt: Image of the course image in the student dashboard

강좌 대표 이미지는 최소 660px너비에서 240px 높이로, .jpg 또는.png 형식이어야 한다. 

다음 단계에 따라, 강좌 대표 이미지를 추가할 수 있다.

#. **설정** 메뉴에서, **기본 설정** 을 클릭한다.
#. **강좌 대표 이미지** 가 보일 때까지 스크롤을 내린다.
#. **강좌 대표 이미지 업로드** 를 클릭해 컴퓨터에서 이미지를 선택한다.
#. 대시보드에서 이미지가 학습자에게 어떻게 나타나는지 살펴본다.

.. _Add a Course Video:

*********************************
강좌 소개 영상 추가하기
*********************************

수강을 고민중인 학습자의 관심을 유도할 수 있게, 각 강좌는 강좌 소개 영상을 보여줄 수 있다. 소개 영상에 이 강좌만의 특징을 강조하면 더욱 좋다.

.. image:: ../../../shared/building_and_running_chapters/Images/about-page-course-video.png
 :alt: Image of the course video in the course About page.

동영상이 다음과 같은 질문에 답할 수 있다면 좋다.

* 누가 이 강좌를 가르치는가?
* 어떤 대학이 이 강좌를 제공하는가?
* 강좌가 어떤 주제 및 개념을 포함하고 있는가? 
* 왜 학습자가 이 강좌를 수강해야 하는가? 

2분 이하의 재생 시간 동안, 동영상이 위 내용을 간결하게 담고 있어야 한다.

강좌 운영팀은 강좌 소개 동영상이 강좌 콘텐츠 동영상과 같이 압축 사양 및 동영상 형식 지침을 따르는지 확인해야 한다. 

강좌 소개 동영상을 추가하려면,

1. YouTube에 강좌 동영상을 업로드한다. URL에서 **watch?v =** 뒤에 나타나는 
코드를 기록한다. 이 코드는 아래에 표시된 상자에 있다.

  .. image:: ../../../shared/building_and_running_chapters/Images/image127.png
    :alt: Image of a sample course video
    
2. **설정** 메뉴에서, **기본 설정** 을 클릭한다.
#. **강좌 소개 영상** 이 나타날 때까지 스크롤을 내린다.
#. 동영상 박스 아래 영역에, YouTube video ID (위 1단계에서 복사한 코드)를 입력한다. 코드를 추가하면, 동영상이 동영상 박스에서 자동으로 재생되며, Studio가 자동으로 변경 사항을 저장한다.


.. _Set Course Time Requirements:

************************************
주별 학습 권장 시간 설정하기
************************************

다음 순서대로, 매주 학습자가 강좌 학습에 들일 시간을 지정할 수 있다.

#. **설정** 메뉴에서, **기본 설정** 을 클릭한다.
#. **학습 시간 및 선수 강좌** 가 나타날 때까지 스크롤을 내린다.
#. **주별 학습 권장 시간** 에 매주 학습자가 강좌 학습에 들일 시간을 입력한다. 
#. 강좌 소개 페이지에서 학습 권장 시간 등의 수강 조건이 어떻게 나오는지 확인할 수 있다. 
   


.. _Set Course Prerequisites:

********************************************
선수 강좌 및 사전 평가 설정하기
********************************************

교수자는 학습자가 강좌를 수강하기 전에, 필요한 사전 지식을 충분히 갖추었는지 확인하고 싶은 경우가 있다. 강좌 개관에서 일반적인 학습 권장 사항을 제안할 뿐만 아니라, 학습자가 특정 선수 강좌를 수료하거나 사전 시험을 통과한 후(take an entrance exam)에만 강좌를 수강할 수 있도록 설정할 수 있다.


.. _Specify Prerequisite Courses:

===================================
선수 강좌 명시하기
===================================

학습자가 강좌에 등록하기 전에 특정 K-MOOC 강좌를 수료하도록 할 수 있다. 학습자는 강좌 소개 페이지에서 선수 강좌에 관한 정보를 볼 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/PrereqAboutPage.png
  :width: 500
  :alt: A course About page with prerequisite course information circled

학습자가 선수 강좌를 수료하지 않고 수강 신청을 하면, 학습자 대시보드에서 강좌를 볼 수 있지만, 강좌 내용을 볼 수는 없다. 학습자 대시보드에는 선수 강좌의 소개 페이지 링크가 있어 학 습자가 강좌 소개에서 선수 강좌에 등록할 수 있다. 

.. image:: ../../../shared/building_and_running_chapters/Images/Prereq_StudentDashboard.png
  :width: 500
  :alt: The Student Dashboard with an available course and a course that is
      unavailable because it has a prerequisite

단 선수 강좌 지정을 위해서는, 현재 강좌와 선수 강좌의 강좌 개설자가 같아야 한다.

#. Studio에서 강좌를 연다.
#. **설정** 메뉴에서, **기본 설정** 을 클릭한다.
#. **기본 설정** 메뉴에서, **학습 시간 및 선수 강좌** 가 나타날 때까지 스크롤을 내린다.
#. **선수 강좌** 에서 드롭 다운 목록을 클릭해서 강좌를 선택한다.
#. 페이지 하단에서 **변경 사항 저장** 을 클릭한다.

.. 참고:: 현재 1개 강좌만을 선수강좌로 지정할 수 있다.


.. _Require an Entrance Exam:

===================================
사전 평가 설정하기 
===================================

학습자가 강좌 자료에 접근하기 전에 먼저 사전 평가를 통과하게 할 수 있다. 사전 시험을 설정하는 경우, 강좌를 수강 신청한 학습자는 사전 평가를 통과할 때까지 공지사항과 사전 시험 탭만 볼 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/EntEx_LandingPage.png
  :width: 500
  :alt: 공지사항과 사전 평가 탭이 왼쪽에 동그랗게 표시되어 있다. 
      


학습자가 사전 평가를 통과하면, 강좌의 모든 자료에 접근할 수 있게 된다.

다음 단계에 따라 사전 평가를 설정할 수 있다.

#. Studio에서 강좌를 연다.
#. **설정** 메뉴에서, **기본 설정** 을 클릭한다.
#. **기본 설정** 메뉴에서, **학습 시간 및 선수 강좌** 가 나타날 때까지 스크롤을 내린다.
#. **수강 시작 전, 사전 평가를 통과해야 합니다.** 체크 박스를 선택한다.
#. 페이지 하단에서 **변경 사항 저장** 을 클릭한다.

변경 내용을 저장한 후, 스튜디오의 강좌 개요에 사전 평가가 추가된 것을 확인할 수 있을 것이다. 사전 평가에 콘텐츠를 추가하려면, 강좌 개요로 이동하면 된다.

사전 평가 활용하기
********************************************

사전 평가를 설정하기 전에, 다음을 확인하여 강좌 운영을 더욱 효과적으로 할 수 있길 바란다.

* 베타 테스터가 교수자의 다른 강좌 콘텐츠를 테스트하는 경우, 입학 시험도 꼭 확인하도록 한다.

* 강좌 소개 페이지에 있는 강좌 설명에서 사전 평가를 언급했는지 확인한다.
그렇지 않으면, 학습자가 수강신청하기 전에 사전 평가에 관해 모른 상태에서 강좌 콘텐츠에 접근하려고 시도할 것이다.

* 공지사항 페이지의 상단에 사전 시험에 임할 학습자를 위한 정보 및 지침을 추가한다. 
공지사항 페이지의 상단에 사전 시험에 임할 학습자를 위한 정보 및 지침을 추가한다. 학습자는 강좌에서 가장 먼저 공지사항 페이지를 보기 마련이다. 이에 다음의 정보를 포함하는 것이 좋다.

  * 강좌의 사전 평가를 시작하려면, 학습자는 화면 왼쪽에 있는 **사전 평가** 탭을 클릭한다.

  * 사전 평가를 완료한 학습자는 사전 평가 탭을 다시 클릭하거나 또는 브라우저에서 페이지를 새로 고침 해야 한다. 페이지가 새로 고쳐지면, 학습자는 현재 이용할 수 있는 모든 강좌 콘텐츠를 볼 수 있다.

    .. image:: ../../../shared/building_and_running_chapters/Images/EntEx_CourseAccordionAfterPass.png
      :width: 500
      :alt: The student view after the student has passed the entrance exam,
          with all available course sections listed in the course accordion


강좌 개요에서 사전 평가 만들기
**************************************************

스튜디오에 있는 강좌 개요에서 강좌 사전 평가를 만든다. 사전 평가 콘텐츠를 만드는 것은 다른 강좌 콘텐츠를 만드는 것과 같다. 더 자세한 내용은 :ref:`Creating Course Content Index` 에서 확인할 수 있다.

사전 평가에서 점수 조정하기
********************************************

학습자가 시험을 치르고 난 후 시험에 있는 오류를 발견할 경우, 교수자 및 강좌 운영팀이 시험 수정을 피할 수 없는데 이 경우 개별 학습자의 채점을 위해 몇 가지 선택 사항이 있다. 이는 교수자 대시보드에서 이용할 수 있다.

교수자 대시보드에서 **학습자 관리** 를 클릭하고, 
**사전 평가 성적 조정** 이 보일 때까지 스크롤을 내리면 다음 사항을 선택할 수 있다.

* **학습자의 응시 횟수 재설정**: 특정 학습자가 다시 시험을 치를 수 있도록, 해당 학습자의 응시 횟수를 0으로 되돌린다. 
더 자세한 정보는 :ref:`reset_attempts` 에서 볼 수 있다.

* **학습자 제출 답안 재채점**: 학습자가 제출한 답안을 재채점한다.
  더 자세한 정보는 :ref:`rescore` 에서 볼 수 있다. 

* **문제에 대한 학습자 상태 삭제**: 데이터베이스에서 시험에 대한 학습자의 전체 기록을 삭제한다. 더 자세한 정보는 :ref:`delete_state` 에서 볼 수 있다. 

교수자 대시보드에서 선택 가능한 다른 사항은 **학습자 배경 작업 기록 표시하기** 다. 교수자 및 강좌 운영팀이 학습자의 응시 횟수를 재설정하거나, 학습자가 제출한 것을 재채점하거나, 또는 학습자의 상태를 삭제하는 경우, 이러한 작업은 백그라운드에서 실행된다. 사전 평가에 대하여 실행한 모든 작업의 기록을 보려는 경우, **학습자 배경 작업 기록 표시하기** 를 선택한다.



.. _Set Important Dates for Your Course:

***********************************
주요 일정 설정하기
***********************************

교수자 및 강좌운영팀은 수강신청일, 개강일 등의 강좌의 주요 일정 및 시간을 설정해야 한다.

#. Studio의 **설정** 메뉴에서, **기본 설정** 을 클릭한다. 
#. 일정을 입력하기 위해 화면의 텍스트를 따른다. 

   .. image:: ../../../shared/building_and_running_chapters/Images/schedule.png
    :width: 450
    :alt: An image of the course schedule page.


.. 참고:: K-MOOC에서는 **시간** 설정시, Universal Coordinated Time (UTC)을 따르도록 하고 있다. 

.. _The Course Start Date:

=======================
강좌 시작일 설정하기
=======================


.. 참고:: 기본 강좌 시작 날짜는 **01/01/2030** 의 먼 미래로 설정되어 있다. 이것은 강좌 운영팀이 의도하기 전에 강좌가 시작되지 않도록 하기 위함이다. 학습자가 강좌 이용을 시작하기 원하는 날짜로 강좌 시작 날짜를 변경 해야 한다.

학습자는 **수강중인 강좌** 대시보드 및 강좌 소개 페이지에서 강좌 시작 날짜와 시간을 참조한다. 강좌 시작 날짜 전에 학습자는 강좌의 일부를 볼 수 있다. 예를 들어 학습자는 강좌에 등록한 후 즉시 공지사항 메뉴와 강좌 일반 주제를 볼 수 있다.  강좌 일반 주제에 대한 더 자세한 내용은 :ref:`Create CourseWide Discussion Topics` 에서 확인할 수 있다.


다음 예제는 강좌 소개(About) 페이지의 강좌 시작 날짜와 시간을 보여준다.

.. image:: ../../../shared/building_and_running_chapters/Images/about-page-course-start.png
 :width: 600
 :alt: An image of the course About page, with the start date circled.

다음 예제와 같이, 대시보드에서 학습자는 각 강좌의 개강일을 보게 된다. 

.. image:: ../../../shared/building_and_running_chapters/Images/dashboard-course-to-start.png
 :width: 600
 :alt: An image of two courses in the student dashboard, with the start dates
     and times circled.

.. note:: If you do not specify a start time for your course, students see
   the default start time, 00:00 Coordinated Universal Time (UTC).


.. _Set the Advertised Start Date:

======================================
대략적인 개강 시기 설정하기
======================================

실제 개강일이 아닌 대략적인 개강 시기만을 화면에 나오게 할 수도 있다. 강좌의 정확한 개강일이 불확실할 때 유용한 방법이다. 예를 들어, **2014년 봄** 과 같이 알릴 수 있는 것이다. 

이를 위해서는,

#. Studio의 **설정** 메뉴에서, **고급 설정** 을 클릭한다. 
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
강좌 종료일 설정하기 
=====================

강좌 종료 날짜는 학습자가 그 날짜 이후에 더 이상 수료증을 받을 수 없음을 의미한다. 수료증을 취득한 학습자는 강좌 종료일 후에도 강좌를 볼 수 있다.

.. 중요::
강좌 종료 날짜를 설정 하지 않을 경우, 학습자는 취득한 수료증에 접근할 수 없다.

성적 및 수료증을 취득한 학습자는 다음 예제에서 보여주는 것처럼 **개별 대시보드** 에서 강좌 종료일을 보게 된다.

* 성적 및 수료증 취득이 아직 확정되지 않은 경우, 학습자는 다음과 같은 메시지를 볼 수 있다.

  .. image:: ../../../shared/building_and_running_chapters/Images/dashboard-wrapping-course.png
   :alt: Image of a course on the student dashboard that has ended, but not
     been graded

* 성적 및 수료증 취득이 확정된 경우, 학습자는 다음과 같은 메시지를 볼 수 있다.

  .. image:: ../../../shared/building_and_running_chapters/Images/dashboard-no-cert-course.png
   :alt: Image of a course on the student dashboard that has ended, but not
     been graded

* 수료증 취득 기준 점수와 같거나 더 높은 최종 점수를 얻은 학습자는 PDF로 수료증을 발급받기 위해 **인증서 다운로드하기** 를 클릭할 수 있다. 

  .. image:: ../../../shared/building_and_running_chapters/Images/dashboard-completed-course.png
   :alt: Image of a course on the student dashboard that has ended, but not
     been graded

