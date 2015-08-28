.. _Developing Course Subsections:

###################################
소주제
###################################

소주제를 만들기 전에, 우선 다음 사항을 이해해야 한다.

* `What is a Subsection?`_
* `Viewing Subsections in the Outline`_
* `The Student View of a Subsection`_
* `Subsections and Visibility to Students`_
* `Release Statuses of Subsections`_
  
소주제와 관련된 작업은 다음과 같은 것이 있다.

* `Create a Subsection`_
* `Change a Subsection Name`_
* `Set a Subsection Release Date`_
* `Set the Assignment Type and Due Date for a Subsection`_
* `Publish all Units in a Subsection`_
* `Hide a Subsection from Students`_
* `Delete a Subsection`_


****************************
소주제란?
****************************

주제는 1개 이상의 학습활동이 포함된 소주제로 나뉘게 된다. 
소주제를 살펴보면 강좌에서 무엇을 중점으로 두는지 이해할 수 있게 된다.

***********************************
개요에서 소주제 보기
***********************************

다음 예시는 세 소주제가 모두 접힌 상태로, 강좌 개요에서 어떻게 보이는지를 나타낸다.

.. image:: ../../../shared/building_and_running_chapters/Images/subsections.png
 :alt: Three collapsed subsections in the outline


*********************************
학습자 화면에서 소주제 보기
*********************************

학습자는 강좌 내용 탭에서, 주제가 펼쳐져 있는 상태에서 소주제를 볼 수 있다.
다음 예시에서 일곱 개의 소주제에 동그라미 표시가 되어있는데, 그 중 첫번째 소주제가 열려있는 상태다.

.. image:: ../../../shared/building_and_running_chapters/Images/subsections_student.png
 :alt: The student view of the outline


************************************************
소주제와 학습자 공개 설정
************************************************

소주제의 공개일이 지정되지 않거나, 아직 그 날짜가 되지 않았다면 학습자는 소주제에서 어떤 콘텐츠도 볼 수 없다.


소주제의 공개일이 지나야 학습자가 콘텐츠를 볼 수 있는데,

* 소주제가 속해있는 주제의  공개일이 지났거나,
* 학습활동이 게시되었거나,
* 학습활동이 따로 학습자에게 비공개로 설정되어 있지 않은 경우 학습자가 볼 수 있다.

************************************************
소주제의 공개 상태
************************************************

강좌 개설자는 소주제의 공개일을 조절할 수 있다. 콘텐츠를 학습자에게 공개하려면, 그 콘텐츠가 들어가 있는 소주제가 공개되어야 한다. 소주제의 공개 상태로는 다음과 같은 것이 있다.

* `주제와 함께 예정됨`_
* `공개일이 지정되지 않음 `_
* `Scheduled Later than the Section`_
* `Scheduled with Unpublished Changes`_
* `공개 후 변경 사항은 아직 게시되지 않음`_
* `공개됨`_

==========================
주제와 함께 예정됨
==========================

When you create a subsection, it is set by default to release at the same time
as the section it is in. Therefore, published content in the subsection is
visible to students at the date and time the section is released.

The following example shows how an subsection in the Scheduled with Section
state is displayed in the outline, summarized with a green bar:

.. image:: ../../../shared/building_and_running_chapters/Images/subsection-scheduled.png
 :alt: A subsection scheduled to release with the section


========================
Unscheduled
========================

If the parent section is unscheduled, when you create a new subsection it
will also be unscheduled.

Regardless of the publishing status of units within the subsection, no content
in an unscheduled subsection is visible to students.

The following example shows how an unscheduled subsection is displayed in the
outline, summarized with a gray bar:

.. image:: ../../../shared/building_and_running_chapters/Images/subsection-unscheduled.png
 :alt: An unscheduled subsection

Content in the subsection is not visible to students until you set a release
date and the date passes.


===================================
Scheduled Later than the Section
===================================

You can set a subsection to release on a date after the section releases. 

Content in a subsection that is scheduled for release on a future date is not
visible to students, even if some or all of the units in the subsection are
published.

The following example shows the way that a subsection that will release after
its parent subsection appears in the course outline:

.. image:: ../../../shared/building_and_running_chapters/Images/subsection-scheduled-different.png
 :alt: A subsection scheduled to release later than the section

The scheduled date must pass for the subsection to be visible to students.

==================================
Scheduled with Unpublished Changes
==================================

You can make changes to a published unit before its parent subsection
is released. 

In this situation, when the release date for the subsection passes, the last
published version of units within the subsection are made visible to students.
The changes in units are not visible to students until you publish them.

The following example shows how a scheduled subsection with unpublished changes
is displayed in the outline, summarized with a yellow bar:

.. image:: ../../../shared/building_and_running_chapters/Images/section-scheduled-with-changes.png
 :alt: A scheduled subsection with unpublished changes


==================================
Released with Unpublished Changes
==================================

If you modify a unit within a released subsection, those modifications are not
visible to students until you publish them.

The following example shows how a released section that has unpublished changes
appears in the outline, summarized with a yellow bar:

.. image:: ../../../shared/building_and_running_chapters/Images/section-released-with-changes.png
 :alt: A released subsection with unpublished changes

===========================
Released
===========================

A subsection that is released is visible to students; however, students see
only units within the subsection that are published.

The following example shows how a released subsection is displayed in the
outline, summarized with a blue bar:

.. image:: ../../../shared/building_and_running_chapters/Images/subsection-released.png
 :alt: A released subsection

===========================
Staff Only Content
===========================

A subsection can contain a unit that is hidden from students and available to
staff only. That unit is not visible to students, even if the subsection has
been released.

The following example shows how an subsection that contains a unit that is
hidden from students is displayed in the outline, summarized with a black bar:

.. image:: ../../../shared/building_and_running_chapters/Images/section-hidden-unit.png
 :alt: A section with a hidden unit 

.. _Create a Subsection:

****************************
Create a Subsection
****************************

To create a new subsection:

#. In the outline, expand the section in which you want to create a new
   subsection.
#. Click **New Subsection** at the bottom of the expanded section. A new
   subsection is added at the end of the section, with the subsection name
   selected.
#. Enter the name for the new subsection. Remember that students see the
   subsection name in the courseware.
#. :ref:`Add units<Create a Unit>` to the new subsection as needed.
   
It is recommended that you :ref:`test course content <Testing Your Course
Content>` as you create new subsections.

********************************
Change a Subsection Name
********************************

To change a subsection name, click the Edit icon next to the subsection name.
The name field becomes editable. Enter the new name and tab or click out of the
field to save the name.

.. _Set a Subsection Release Date:

********************************
Set a Subsection Release Date
********************************

To set the subsection release date:

#. Click the Settings icon in the subsection box:
   
   .. image:: ../../../shared/building_and_running_chapters/Images/subsections-settings-icon.png
    :alt: The subsection settings icon circled

   The **Settings** dialog box opens.

#. Enter the release date and time for the section:

   .. image:: ../../../shared/building_and_running_chapters/Images/subsection-settings-release.png
    :alt: The subsection release date settings

#. Click **Save**.

For more information, see :ref:`Release Dates`.

.. _Set the Assignment Type and Due Date for a Subsection:

********************************************************
Set the Assignment Type and Due Date for a Subsection
********************************************************

You set the assignment type for problems at the subsection level. 

When you set the assignment type for a subsection, all problems within the
subsection are graded and weighted as a single type.  For example, if you
designate the assignment type for a subsection as **Homework**, then all
problem types in that subsection are graded as homework.

To set the assignment type and due date for a subsection:

#. Click the Settings icon in the subsection box:
   
   .. image:: ../../../shared/building_and_running_chapters/Images/subsections-settings-icon.png
    :alt: The subsection settings icon circled

   The Settings dialog box opens.

#. Select the assignment type for this subsection in the **Grade as** field:
   
   .. image:: ../../../shared/building_and_running_chapters/Images/subsection-settings-grading.png
    :alt: The subsection settings with the assignment type and due date circled

#. Enter or select a due date and time for problems in this subsection.
#. Click **Save**.

For more information, see :ref:`Establish a Grading Policy`.

.. _Publish all Units in a Subsection:

**********************************
Publish all Units in a Subsection
**********************************

To publish all new and changed units in a subsection, click the publish icon in
the box for the subsection:

.. image:: ../../../shared/building_and_running_chapters/Images/outline-publish-icon-subsection.png
 :alt: Publishing icon for a subsection

.. note:: 
 The publish icon only appears when there is new or changed content within the
 subsection.

See :ref:`Unit Publishing Status` for information about statuses and visibility
to students.

.. _Hide a Subsection from Students:

********************************
Hide a Subsection from Students
********************************

You can hide all content in a subsection from students, regardless of the
status of units within the section.

To hide a subsection from students:

#. Click the Settings icon in the subsection box:
   
   .. image:: ../../../shared/building_and_running_chapters/Images/subsections-settings-icon.png
    :alt: The subsection settings icon circled

   The **Settings** dialog box opens.

#. Check **Hide from students**.

   .. image:: ../../../shared/building_and_running_chapters/Images/subsection-settings-hidden.png
    :alt: The subsection hide from students setting

#. Click **Save**.

Now, no content in the subsection is visible to students.

To make the subection visible to students, repeat these steps and clear the
**Hide from students** checkbox.

.. warning::
 When you clear the **Hide from students** checkbox for a subsection, not all
 content in the subsection is necessarily made visible to students. If you
 explicitly set a unit to be hidden from students, it remains hidden from
 students. Unpublished units remain unpublished, and changes to published units
 remain unpublished.

.. _Delete a Subsection:

********************************
Delete a Subsection
********************************

When you delete a subsection, you delete all units within the subsection.

.. warning::  
 You cannot restore course content after you delete it. To ensure you do not
 delete content you may need later, you can move any unused content to a
 section in your course that you set to never release.

To delete a subsection:

#. Click the delete icon in the subsection that you want to delete:

  .. image:: ../../../shared/building_and_running_chapters/Images/subsection-delete.png
   :alt: The subsection with Delete icon circled

2. When you receive the confirmation prompt, click **Yes, delete this
   subsection**.
