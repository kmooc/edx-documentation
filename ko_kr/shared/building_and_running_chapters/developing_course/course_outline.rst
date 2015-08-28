.. _Developing Your Course Outline:

###################################
강좌 개요
###################################

강좌를 개발할 때는 주로 edX Studio 강좌 개요에서 작업하게 된다.

이 장에서는 강좌 개요에서의 작업에 대해 다룬다. 

* `Open the Course Outline`_
* `Example of a Developed Course in the Outline`_
* `View the Course Organization as a Student`_
* `Navigate the Course Outline`_
* `Add Content in the Course Outline`_
* `Modify Settings for Objects in the Course Outline`_
* `Publish Content from the Course Outline`_
* `Reorganize the Course Outline`_
* `Delete Content in the Course Outline`_

아래 장에는 강좌 개요를 이루는 기본 요소에 대한 안내가 있다.   

* :ref:`Developing Course Sections`
* :ref:`Developing Course Subsections`
* :ref:`Developing Course Units`
* :ref:`Developing Course Components`

****************************
강좌 개요 열기
****************************

강좌 개요를 보려면

#. Studio에 로그인한다.
#. 개발하려는 **강좌** 를 클릭한다.

   기본적으로 강좌명을 클릭하면, 강좌 개요가 나오게 되어있다.

다른 페이지에서 강좌 개요를 보려면, **콘텐츠** 메뉴에서 **강좌 개요** 를 클릭하면 된다.
   
맨처음 강좌 개요를 열었을 때는 아직 콘텐츠가 없을 것이다.

.. image:: ../../../shared/building_and_running_chapters/Images/outline_empty.png
 :alt: An empty course outline

그래서 :ref:`create the first section<Create a Section>` 안내에 따라, 주제부터 만드는 것이 좋다.
  
********************************************************
개발된 강좌의 강좌 개요 예시
********************************************************

다음 예시는 개발된 예시 강좌에서 강좌 개요가 어떻게 나타나는지를 보여준다. 
주제, 소주제, 학습활동 등 강좌의 기본 요소를 채워가다보면, 강좌 개요가 아래 예시처럼 보이게 된다.

.. image:: ../../../shared/building_and_running_chapters/Images/outline-callouts.png
 :alt: An outline with callouts for sections, subsections, and units

이 예시가 보여주듯이, 강좌는 다음 구조로 구성된다.

#. :ref:`Sections<Developing Course Sections>`
#. :ref:`Subsections<Developing Course Subsections>`
#. :ref:`Units<Developing Course Units>`

:ref:`Components<Developing Course Components>` 는 강좌 개요에 나타나지 않는다. 
구성요소가 포함되어 있는 학습활동을 클릭해야 해당 구성요소를 볼 수 있다.

이 장에서는 우선 강좌 개요에 대한 안내가 이어질 것이다.
강좌 기본 구성요소에 대한 더 자세한 안내는 위 링크에 있다. 

********************************************************
학습자 화면에서 강좌 구성 보기
********************************************************

Studio의 강좌 개요에서 보이는 콘텐츠를, 학습자는 학습관리시스템(LMS)에서 강좌 내용 탭에서 보게 된다.
다음 이미지는 학습자가 보게 될 화면을 나타낸다.

.. image:: ../../../shared/building_and_running_chapters/Images/Course_Outline_LMS.png
 :alt: Image of course conent from student's point of view

.. _Navigating the Course Outline:

*******************************
강좌 개요 살펴보기
*******************************

Studio의 강좌 개요 화면에서 각 주제와 소주제를 펼치거나 접어서 개요를 살펴보면 편리하다.
주제나 소주제명 옆의 드롭 다운 아이콘을 클릭하면 펼치기 및 접기가 가능하다.

.. image:: ../../../shared/building_and_running_chapters/Images/outline-expand-collapse.png
 :alt: The outline with expand and collapse icons circled

펼칠 경우, 소주제 안의 모든 학습활동이 이렇게 보이게 된다.

.. image:: ../../../shared/building_and_running_chapters/Images/outline-with-units.png
 :alt: The outline with an expanded subsection

학습활동을 열려면 학습활동명을 클릭하면 된다. 
학습활동에 대한 자세한 안내가 :ref:`unit page<Developing Course Units>` 에 있다.

.. _Add Content in the Course Outline:

************************************************
강좌 개요에 콘텐츠 추가하기
************************************************

강좌 개요에서 주제, 소주제, 학습활동을 바로 추가할 수 있다.

강좌 개요 하단의 **+ 새로운 주제** 나 상단의 **신규 주제 추가하기** 를 클릭하면, 주제를 추가할 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/outline-create-section.png
 :alt: The outline with the New Section buttons circled

소주제를 추가하기 위해선, 주제를 먼저 펼친 후 **+ 새로운 소주제** 를 클릭하면 된다.

.. image:: ../../../shared/building_and_running_chapters/Images/outline-new-subsection.png
 :alt: The outline with the New Subsection button circled

학습 활동을 추가하기 위해선, 소주제를 먼저 펼친 후 **+ 새로운 학습활동** 을 클릭하면 된다.

.. image:: ../../../shared/building_and_running_chapters/Images/outline-new-unit.png
 :alt: 새로운 소주제 버튼이 동그랗게 표시되어 있다.

그러면 학습 활동이 열리게 된다. 이에 대한 자세한 안내는 :ref:`unit<Developing Course Units>` 에 있다.

.. 참고:: 수강 전 사전 평가를 시행하고 싶으면 강좌 개요 페이지에서 사전 평가를 만들 수 있다. 우선 Studio에서 사전 평가 설정이 이루어져야 한다. 이에 대한 안내는 :ref:`Require an Entrance Exam` 에 있다.  

.. _Modify Settings for Objects in the Course Outline:

***************************************************
강좌 세부 사항 설정 변경
***************************************************

강좌 개요에서 주제, 소주제 및 학습활동의 설정을 변경할 수 있다.
이에 대한 구체적인 안내가 아래 링크에 있다.

* :ref:`Set a Section Release Date`
* :ref:`Hide a Section from Students`
* :ref:`Set a Subsection Release Date`
* :ref:`Set the Assignment Type and Due Date for a Subsection`
* :ref:`Hide a Subsection from Students`
* :ref:`Hide a Unit from Students`

주제, 소주제 및 학습활동의 설정을 변경하려면, 각 항목의 설정 아이콘을 클릭한다.
다음 예시에서, 주제, 소주제 및 학습활동의 설정 아이콘이 동그랗게 표시되어있다. 

.. image:: ../../../shared/building_and_running_chapters/Images/settings-icons.png
 :alt: Settings icons in the course outline

더 자세한 안내는 위 링크에 있다.

.. _Publish Content from the Course Outline:

************************************************
콘텐츠 게시하기
************************************************

주제, 소주제 및 학습 활동을 게시할 수 있다. 이들을 전체적으로 게시할 수도 있고, 개별적으로 게시할 수도 있다.

신규 및 변경된 학습활동을 게시하려면, 각 주제, 소주제 및 학습 활동의 게시 아이콘을 클릭한다.
다음 예시에서, 게시 아이콘이 동그랗게 표시되어 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/outline-publish-icons.png
 :alt: Publishing icons in the course outline

.. 참고:: 
게시 아이콘은 새롭거나 변경된 콘텐츠가 있을 때만 나타난다.  


더 자세한 안내는 아래 링크에 있다.

* :ref:`Unit Publishing Status`
* :ref:`Publish all Units in a Section`
* :ref:`Publish all Units in a Subsection`
* :ref:`Publish a Unit`

.. _Reorganize the Course Outline:

************************************************
강좌 개요 재구성하기
************************************************

You can reorganize your course content by dragging and dropping sections,
subsections, and units to new locations in the outline.

To move a section, subsection, or unit, hover over the handle on the right of
the object's box until the cursor changes to a four-headed arrow. For example,
in the image below, the handle for the subsection Lesson 1 - Getting Started is
selected:

.. image:: ../../../shared/building_and_running_chapters/Images/outline-drag-select.png
 :alt: A subsection handle selected to drag it

Then, click and drag the object to the location that you want. 

If you expanded the section or subsection you are moving the object to, when
you move the object, a blue line indicates where the object will land when you
release the mouse button. For example, in the image below, the subsection
Lesson 1 - Getting Started is being moved to the end of the section
Introduction:

.. image:: ../../../shared/building_and_running_chapters/Images/outline-drag-new-location.png
 :alt: A subsection being dragged to a new section 	

If you did not expand the section or subsection you are moving the object to,
the outline of that section or subsection turns blue when you have moved the
object to a valid location. You can then release the mouse button. For example,
in the image below, the subsection Lesson 1 - Getting Started is being moved to
the collapsed section Introduction:

.. image:: ../../../shared/building_and_running_chapters/Images/outline-drag-new-location-collapsed.png
 :alt: A subsection being dragged to a new section 

.. _Delete Content in the Course Outline:

************************************************
Delete Content in the Course Outline
************************************************

You delete sections, subsections, and units from the course outline.

.. warning::  
 You cannot restore course content after you delete it. To ensure you do not
 delete content you may need later, you can move any unused content to a
 section in your course that you set to never release.

Click the delete icon in the box for the object you want to delete:

.. image:: ../../../shared/building_and_running_chapters/Images/outline-delete.png
 :alt: The outline with Delete icons circled

You are prompted to confirm the deletion.

.. note::
 When you delete an object, all objects that it contains are deleted. For
 example, when you delete a subsection, all units in that subsection are
 deleted.
