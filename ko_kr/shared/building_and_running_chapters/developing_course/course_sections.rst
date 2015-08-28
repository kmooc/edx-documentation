.. _Developing Course Sections:

###################################
주제
###################################

주제를 만들기 전에, 우선 다음 사항을 이해해야 한다.

* `What is a Section?`_
* `Viewing Sections in the Outline`_
* `The Student View of a Section`_
* `Sections and Visibility to Students`_
* `Release Statuses of Sections`_

  
주제와 관련된 작업은 다음과 같은 것이 있다.

* `Create a Section`_
* `Change a Section Name`_
* `Set a Section Release Date`_
* `Publish all Units in a Section`_
* `Hide a Section from Students`_
* `Delete a Section`_


****************************
주제란?
****************************

주제는 강좌에서 가장 상위 범주에 해당한다. 주제는 강좌의 시간이나 

A section is the topmost category in your course. A section can represent a
time period in your course, a chapter, or another organizing principle. A
section contains one or more subsections.

********************************
강좌 개요에서 주제 보기
********************************

다음 예시는 강좌개요에서 주제가 모두 접혀있는 상태를 보여준다.

.. image:: ../../../shared/building_and_running_chapters/Images/sections-outline.png
 :alt: Four sections in the outline

******************************
학습자 화면에서 주제 보기 
******************************

학습자는 **강좌 내용** 탭에서 주제를 본다. 한 번에 1개의 주제씩 펼쳐볼 수 있다.
다음 예시에서 세 주제에 동그라미 표시가 되어있는데, 그중 세 번째 주제가 펼쳐진 상태로써 소주제를 볼 수 있게 되어 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/sections_student.png
 :alt: The students view of the course with two sections circled

************************************************
주제 및 학습자 공개 설정
************************************************

주제의 공개일이 지정되지 않거나, 아직 그 날짜가 되지 않았다면 학습자는 주제에서 어떤 콘텐츠도 볼 수 없다. 

주제의 공개일이 지나야 학습자가 콘텐츠를 볼 수 있는데,


* 콘텐츠가 포함되어 있는 소주제의 공개일이 지났거나,
* 학습활동이 게시되었거나,
* 학습활동이 따로 학습자에게 비공개로 설정되어 있지 않은 경우 학습자가 볼 수 있다.

************************************************
주제의 공개 상태
************************************************

강좌 개설자는 주제의 공개일을 조절할 수 있다. 콘텐츠를 학습자에게 공개하려면, 그 콘텐츠가 들어가 있는 주제가 공개되어야 한다. 주제의 공개 상태로는 다음과 같은 것이 있다.

* `공개일이 지정되지 않음`_
* `예정됨`_
* `공개됨`_
* `공개 후 변경 사항은 아직 게시되지 않음`_
* `강좌 운영팀에게만 공개됨`_

========================
공개일이 지정되지 않음
========================

주제를 만든 후, ``1/1/2030 00:00:00 UTC`` 으로 기본값이 설정된 :ref:`course start date<The Course Start Date>`을 바꾸지 않으면, 주제가 계속 ``공개일이 지정되지 않음`` 상태에 있게 된다. 이 상태에서는 학습자가 주제에 들어있는 콘텐츠를 볼 수 없음에 주의해야 한다. 

개강일을 변경하면, 주제 공개일의 기본값이 개강일로 바뀐다.

다음 예시는 공개일이 지정되지 않은 주제가 어떻게 강좌 개요에서 보이는지를 나타낸다. 

.. image:: ../../../shared/building_and_running_chapters/Images/section-unscheduled.png
 :alt: An unscheduled section

학습자가 콘텐츠를 볼 수 있게 하려면, 강좌 운영팀이 반드시 공개일을 지정해야 한다.

==========
예정됨
==========

공개가 예정된 주제는 지정된 공개일이 되기 전까지는 학습자에게 공개되지 않는다.
이는 그 주제 내부의 콘텐츠의 게시 상태와 관계 없는 것으로, 전체 주제가 학습자에게 공개되지 않는다면 콘텐츠 또한 학습자가 볼 수 없는 것이다. 

다음 예시는 공개가 예정된 주제가 어떻게 강좌 개요에서 보이는지를 나타낸다. 

.. image:: ../../../shared/building_and_running_chapters/Images/section-future.png
 :alt: An section scheduled to release in the future

주제의 공개 예정일이 지나야만 학습자가 볼 수 있다는 것에 유의해야 한다.

===========================
공개됨
===========================

학습자는 공개된 주제를 보게 되지만, 그 주제 내부의 콘텐츠 중에서 공개된 소주제와 게시된 학습활동만 볼 수 있다.

다음 예시는 공개된 주제가 어떻게 강좌 개요에서 보이는지를 나타낸다.

.. image:: ../../../shared/building_and_running_chapters/Images/section-released.png
 :alt: An unscheduled section

==================================
공개 후 변경 사항은 아직 게시되지 않음
==================================

공개된 주제의 학습활동을 변경하였으나, 그것을 게시하지 않는 한 학습자들은 변경된 학습활동을 볼 수 없다. 

다음 예시는 게시되지 않은 학습활동이 포함된 주제가 어떻게 학습자에게 보이는지를 나타낸다.
게시되지 않은 학습활동은 그림에서 노란색으로 표시된 부분이다. 
또한 이 그림은 학습활동의 상태를 보기 위해 주제가 펼쳐진 상태이다.

.. image:: ../../../shared/building_and_running_chapters/Images/section-unpublished-changes.png
 :alt: A section with unpublished changes

학습자가 변경된 학습활동을 보려면, 강좌운영팀이 반드시 해당 학습활동을 게시해야 한다.

===========================
강좌 운영팀에게만 공개
===========================

A section can contain a unit that is hidden from students and available to
staff only. That unit is not visible to students, regardless of the release
date of the section or subsection.

The following example shows how a section that contains a unit that is hidden
from students is displayed in the outline, summarized with a black bar:

.. image:: ../../../shared/building_and_running_chapters/Images/section-hidden-unit.png
 :alt: A section with a hidden unit 


.. _Create a Section:

****************************
Create a Section
****************************

If you do not change the :ref:`course start date<The Course Start Date>`
default value, ``1/1/2030``, when you create a new section, its release date
will be ``Unscheduled``. 

If you have modified the course start date, when you create a new section, the
default release date is the course start date.

.. caution:: 
 If the course start date is in the past, newly created sections are
 immediately visible to students.

To create a new section:

#. Click **New Section** at the top or bottom of the outline: 
   
   .. image:: ../../../shared/building_and_running_chapters/Images/outline-create-section.png
     :alt: The outline with the New Section buttons circled

   A new section is added at the end of the course content, with the section
   name selected.

#. Enter the name for the new section. Remember that students see the section
   name in the courseware.

#. :ref:`Add subsections<Create a Subsection>` to the new section as needed.
   
It is recommended that you :ref:`test course content <Testing Your Course
Content>` as you create new sections.

********************************
Change a Section Name
********************************

To edit a section name, hover over the section name to show the Edit icon:

.. image:: ../../../shared/building_and_running_chapters/Images/section-edit-icon.png
  :alt: The Edit Section Name icon

Click the Edit icon next to the section name. The name field becomes editable.
Enter the new name and tab or click out of the field to save the name.

.. _Set a Section Release Date:

********************************
Set a Section Release Date
********************************

To set the section release date:

#. Click the Settings icon in the section box:
   
   .. image:: ../../../shared/building_and_running_chapters/Images/section-settings-box.png
    :alt: The section settings icon circled

   The **Settings** dialog box opens.

#. Enter the release date and time for the section:
   
   .. image:: ../../../shared/building_and_running_chapters/Images/section-settings-release-date.png
    :alt: The section release date settings

#. Click **Save**.

For more information, see :ref:`Release Dates`.

.. _Publish all Units in a Section:

********************************
Publish all Units in a Section
********************************

To publish all new and changed units in a section, click the publish icon in
the box for the section:

.. image:: ../../../shared/building_and_running_chapters/Images/outline-publish-icon-section.png
 :alt: Publishing icon for a section

.. note:: 
 The publish icon only appears when there is new or changed content within the
 section.

See :ref:`Unit Publishing Status` for information about statuses and visibility
to students.


.. _Hide a Section from Students:

********************************
Hide a Section from Students
********************************

You can hide all content in a section from students, regardless of the status
of subsections and units within the section.

To hide a section from students:

#. Click the Settings icon in the section box:
   
   .. image:: ../../../shared/building_and_running_chapters/Images/section-settings-box.png
    :alt: The section settings icon circled

   The **Settings** dialog box opens.

#. Check **Hide from students**.

   .. image:: ../../../shared/building_and_running_chapters/Images/section-settings-hide.png
    :alt: The section hide from students setting

#. Click **Save**.

Now, no content in the section is visible to students.

To make the section visible to students, repeat these steps and clear the
**Hide from students** checkbox.

.. warning::
 When you clear the **Hide from students** checkbox for a section, not all
 content in the section is necessarily made visible to students. If you
 explicitly set a subsection or unit to be hidden from students, it remains
 hidden from students. Unpublished units remain unpublished, and changes to
 published units remain unpublished.

********************************
Delete a Section
********************************

When you delete a section, you delete all subsections and units within the
section.

.. warning::  
 You cannot restore course content after you delete it. To ensure you do not
 delete content you may need later, you can move any unused content to a
 section in your course that you set to never release.

To delete a section:

#. Click the delete icon in the section that you want to delete:

  .. image:: ../../../shared/building_and_running_chapters/Images/section-delete.png
   :alt: The section with Delete icon circled

2. When you receive the confirmation prompt, click **Yes, delete this
   section**.
