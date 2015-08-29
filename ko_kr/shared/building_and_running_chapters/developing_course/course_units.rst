.. _Developing Course Units:

###################################
학습활동
###################################

학습활동을 만들기 전에, 우선 다음 사항을 이해해야 한다.

* `What is a Unit?`_
* `Viewing Units in the Outline`_
* `Viewing the Unit Page`_
* `Viewing Units as a Student`_
* `Unit Publishing Status and Visibility to Students`_
* `Unit Publishing Status`_

학습활동과 관련된 작업은 다음과 같은 것이 있다.

* `Create a Unit`_
* `Edit a Unit`_
* `Preview a Unit`_
* `Publish a Unit`_
* `Discard Changes to a Unit`_
* `View a Published Unit`_
* `Hide a Unit from Students`_
* `Delete a Unit`_

강좌 운영팀은 학습활동에 구성요소를 추가할 수 있다. 
이에 관해 :ref:`course components<Developing Course
Components>` 에 자세한 안내가 있다. 

.. _What is a Unit?:

****************************
학습활동이란?
****************************

학습활동은 :ref:`subsection<Developing Course Subsections>` 의 일부로써, 
학습자가 소주제를 클릭하면 한 번에 하나씩 볼 수 있다. 

1개의 학습활동은 1개 이상의 :ref:`components<Developing Course Components>` 를 가질 수 있는데, 이러한 구성요소로는 :ref:`HTML content<Working with HTML Components>`,
:ref:`problems<Working with Problem Components>`, :ref:`discussions<Working
with Discussion Components>` 및 
:ref:`videos<Working with Video Components>` 이 있다.


****************************
강좌 개요에서 학습활동 보기
****************************

학습활동을 보려면, 주제와 소주제를 먼저 펼쳐야 한다. 이에 대한 안내는 :ref:`expand<Navigating the Course Outline>` 에 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/outline-callouts.png
 :alt: An outline with callouts for sections, subsections, and units

****************************
Studio에서 학습활동 보기
****************************

강좌 개요에서 소주제명을 클릭하면, **학습활동** 이 나온다.

다음 예시는 1개 학습활동에 2개의 구성요소가 있는 화면이며, 동그랗게 표시된 부분은 이를 학습 관리 시스템에서 볼 수 있는 버튼을 가리킨다.

.. image:: ../../../shared/building_and_running_chapters/Images/unit-page.png
 :alt: The Unit page

****************************
학습자 화면에서 학습활동 보기
****************************

학습자는 강좌 내용에서 소주제에 있는 학습활동을 볼 수 있다. 다음 학습활동으로 넘어가려면 화살표 버튼을 눌러야 한다.

다음 예시는 1개의 소주제에 학습활동이 5개로 구성되어 있을 때, 어떻게 강좌 개요에서 보이는지를 나타낸다.

.. image:: ../../../shared/building_and_running_chapters/Images/Units_LMS.png
 :alt: Image of units from the student's point of view

.. _The Unit Workflow:

************************************************
학습활동 작업 흐름
************************************************

먼저 :ref:`section<Developing Course Sections>` 와 :ref:`subsection<Developing Course Subsections>` 을 만들면
학습활동을 만들 수 있게 된다.

학습활동을 만드는 기본 순서는 아래와 같은데,

#. :ref:`Create a new unit<Create a Unit>`.
#. :ref:`Add components to the unit<Add a Component>`.
#. :ref:`Publish the unit<Publish a Unit>`.
   
학습활동을 게시한 후 

#. :ref:`Modify components in the unit<Developing Course Components>`.
#. :ref:`Publish the changes to the unit<Publish a Unit>`

작업이 가능하기도 하다.
   
다음 도표는 학습활동의 일반적인 작업흐름을 보여준다. 

.. image:: ../../../shared/building_and_running_chapters/Images/workflow-create-unit.png
 :alt: Diagram of the unit development workflow
   

이러한 단계를 거치다보면, 학습활동의 **게시 상태** 가 바뀌게 된다.

The publishing status controls the content available to students, along with
:ref:`release dates<Release Dates>`. See the next section for more information.

.. _Unit States and Visibility to Students:

*************************************************
학습활동 게시 상태 및 학습자 공개 설정
*************************************************

학습자가 학습활동을 볼 수 있는지 여부는 학습활동의 게시 상태에 따라 달라진다. 

* `초안 (게시된 적 없음)`_ 일 때, 학습자는 학습활동을 볼 수 없다. 

* `강좌 운영팀에게만 공개`_ 일 때, 학습자는 학습활동을 볼 수 없다. 이에 대해 `Hide a Unit from Students`_ 에 더 자세한 안내가 있다. 

* `아직 공개되지 않음`_  일 때, :ref:`release date <Release Dates>` 전까지는 학습자가 학습활동을 볼 수 없다. 하지만 공개일이 되면, 게시 상태가 `공개됨`_ 로 바뀌게 된다.

* `공개됨`_ 일 때, 학습자는 학습활동을 볼 수 있다.
  
* `학습활동이 변경됨`_ 의 상태일 때, 주제의 :ref:`release date <Release Dates>` 이 이미 지난 경우라면 
학습자가 변경된 학습활동을 바로 볼 수 있는 것이 아니라, 변경 이전의 학습활동을 보게 된다.

:ref:`Controlling Content Visibility` 에 공개 설정에 대한 더 자세한 안내가 있다.

.. _Unit Publishing Status:

************************************************
학습활동 게시 상태
************************************************ 

학습활동의 게시 상태로는 이러한 것들이 있다.

* `초안 (게시된 적 없음)`_
* `공개됨`_ 
* `아직 공개되지 않음`_ 
* `학습활동이 변경됨`_
* `강좌 운영팀에게만 공개`_

.. _Draft (Never Published):

========================
`초안 (게시된 적 없음)`
========================

새 학습활동을 만들어 구성요소를 추가할 때, 학습활동의 게시 상태는 **초안 (게시된 적 없음)** 이며 화면에는 다음과 같이 나타나게 된다.

.. image:: ../../../shared/building_and_running_chapters/Images/unit-never-published.png
 :alt: Status panel of a unit that has never been published

Studio에서, you see the version of the content that you're working on. Students
never see a unit with this status, even if the release date has passed.

Though you do not see the unit in the LMS, you can :ref:`preview the
unit<Preview Course Content>`.

You must :ref:`publish the unit<Publish a Unit>` for it to be included in the
LMS.

.. _Published and Live:

====================
Published and Live
====================

The release date for the section and subsection have passed. You've published
the unit and haven't made any changes to it. You and students both see the
current version of the unit.

.. image:: ../../../shared/building_and_running_chapters/Images/unit-published.png
 :alt: Status panel of a unit that is published

.. _Published Not Yet Released:

====================================
Published (not yet released)
====================================

You've published the unit, but the release date hasn't passed. Students cannot
see this unit until the release date passes.

.. image:: ../../../shared/building_and_running_chapters/Images/unit-published_unreleased.png
 :alt: Status panel of a unit that is published but not released

.. _Draft (Unpublished Changes):

===========================
Draft (Unpublished changes)
=========================== 

When you edit a published unit, whether or not it is released, the unit's
publishing status changes to **Draft (Unpublished Changes)**, as shown in the
status panel:

.. image:: ../../../shared/building_and_running_chapters/Images/unit-pending-changes.png
 :alt: Status panel of a unit that has pending changes

In Studio, you see the draft of the content that you're working on. If the
release date has passed, students see the last published version of the unit.
If the release date hasn't passed, students can't see your content.

You must :ref:`publish the unit<Publish a Unit>` for students to see your
changes.

You can :ref:`preview the changes to a unit<Preview Course Content>` to test
how your changes will appear to students after you publish the unit.

.. _Visible to Staff Only:

===========================
Visible to Staff Only
===========================

When you :ref:`hide a unit from students<Hide a Unit from Students>`, the
unit's publishing status changes to **Visible to Staff Only**.

The publishing status of a unit can be **Visible to Staff Only** if you hid the
parent :ref:`section<Hide a Section from Students>` or :ref:`subsection<Hide a
Subsection from Students>` from students.

Students never see a unit with this status, even if it has been published and
the release date has passed.

.. image:: ../../../shared/building_and_running_chapters/Images/unit-unpublished.png
 :alt: Status panel of a unit that has pending changes

.. _Create a Unit:

****************************
Create a Unit
****************************

You can create a unit from the outline or create a unit in the same subsection
from the unit page.

To create a unit from the outline:

#. In the outline, expand the subsection in which you want to create a new
   unit.
#. Click **New Unit** at the bottom of the expanded subsection. A new
   unit is added at the end of the subsection.
#. On the unit page, the unit name is selected. Edit the name as needed.
#. :ref:`Add components<Add a Component>` to the new unit as needed.

To create a new unit from a unit page:

#. In the **Unit Location** panel, click **New Unit**.

   .. image:: ../../../shared/building_and_running_chapters/Images/unit_location.png
    :alt: The Unit Location panel in the Unit page

   The unit page for the new unit opens automatically.

#. On the unit page, the unit name is selected. Edit the name as needed.

#. :ref:`Add components<Add a Component>` to the new unit as needed.

You must then :ref:`publish the unit<Publish a Unit>` to make it visible to
students.


.. _Edit a Unit:

**************
Edit a Unit
**************

You can edit a unit in the following ways:

* `Edit the unit name`_
* :ref:`Develop components<Developing Course Components>`
* `Reorganize Components in Units`_

When you make any of these changes, if you previously published the unit, the
state changes to `Draft (Unpublished Changes)`_. You must then :ref:`publish
the unit<Publish a Unit>` to make your edits visible to students.


==============================
Edit the Unit Name
==============================

To edit a unit name, hover over the name to show the Edit icon:

.. image:: ../../../shared/building_and_running_chapters/Images/unit-edit-icon.png
  :alt: The Edit Unit Name icon

Click the Edit icon next to the unit name. The name field becomes editable.
Enter the new name and tab or click out of the field to save the name.

==============================
Reorganize Components in Units
==============================

You can reorganize components within a unit by dragging and dropping them to
new locations.

To move a component, hover over the handle on the right of the component's box
until the cursor changes to a four-headed arrow. For example, in the image
below, the handle for the discussion component is selected:

.. image:: ../../../shared/building_and_running_chapters/Images/unit-drag-selected.png
  :alt: A discussion component selected to drag it

Then, click and drag the component to the location that you want. 

A dashed outline indicates where the component will land when you release the
mouse button. For example, in the image below, the discussion component is
being moved to the top of the unit:

.. image:: ../../../shared/building_and_running_chapters/Images/unit-drag-moved.png
 :alt: A component being dragged to a new location  

.. _Preview a Unit:

****************************
Preview a Unit
****************************

You preview a unit to review and test the content before it is visible to
students.

You can preview a unit before it is published and when there are unpublished
changes. When the unit is published and there are no pending changes, you
cannot preview the unit; you must view the live version of the unit.

To preview the unit, in the unit page, click **Preview Changes**.

.. image:: ../../../shared/building_and_running_chapters/Images/preview_changes.png
 :alt: The Unit page with Preview Changes button circled

The unit opens in preview mode:

.. image:: ../../../shared/building_and_running_chapters/Images/preview_mode.png
 :alt: The unit in preview mode

When you are revising a previously published unit, it is helpful to preview
your changes in one window and :ref:`view the published unit<View a Published
Unit>` in a second window.

.. _Publish a Unit:

****************************
Publish a Unit
****************************

Publishing a unit makes the current version of the unit in Studio available to
students, if the release date for the section and subsection have passed.

You publish a unit that has a status of `Draft (Never Published)`_ or `Draft
(Unpublished Changes)`_. When you publish a unit, the status changes to
`Published and Live`_ or `Published Not Yet Released`_.

You can publish a unit from the unit page or the course outline.

=======================================
Use the Unit Page to Publish a Unit
=======================================

To publish the unit, click **Publish** in the status panel:

.. image:: ../../../shared/building_and_running_chapters/Images/unit-publish-button.png
 :alt: Unit status panel with Publish button circled


=======================================
Use the Outline to Publish a Unit
=======================================

To publish a unit from the outline, click the publish icon in the box for the
unit:

.. image:: ../../../shared/building_and_running_chapters/Images/outline-publish-icon-unit.png
 :alt: Publishing icon for a unit

.. note:: 
 The publish icon only appears when there is new or changed content in the
 unit.

.. _Discard Changes to a Unit:

****************************
Discard Changes to a Unit
****************************

When you modify a published unit, your changes are saved in Studio, though the
changes aren't visible to students until you publish the unit again.

In certain situations, you may decide that you never want to publish your
changes. You can discard the changes so that Studio reverts to the last
published version of the unit.

To discard changes and revert the Studio version of the unit to the last
published version, click **Discard Changes** in the status panel:

.. image:: ../../../shared/building_and_running_chapters/Images/unit-discard-changes.png
 :alt: Unit status panel with Discard Changes circled

.. caution::
 When you discard changes to a unit, the changes are permanently deleted. You
 cannot retrieve discarded changes or undo the action.


.. _View a Published Unit:

****************************
View a Published Unit
****************************

To view the last published version of a unit in the LMS, click **View Published
Version**.

.. image:: ../../../shared/building_and_running_chapters/Images/unit_view_live_button.png
 :alt: Unit page with View Published Version button circled

The unit page opens in the LMS in Staff view. You may be prompted to log in to
the LMS.

If the unit status is `Draft (Unpublished Changes)`_, you do not see your
changes in the LMS until you publish the unit again.

If the unit status is `Draft (Never Published)`_, the **View Published
Version** button is not enabled.

.. _Hide a Unit from Students:

****************************
Hide a Unit from Students
****************************

You can prevent students from seeing a unit regardless of the unit status or
the release schedules of the section and subsection. 

For more information, see :ref:`Controlling Content Visibility`.

You can hide a unit from students using the course outline or the unit page.

=======================================
Use the Unit Page to Hide a Unit
=======================================

Select the **Hide from students** checkbox in the status panel:

.. image:: ../../../shared/building_and_running_chapters/Images/unit-hide.png
 :alt: Unit status panel with Hide from Students checked

For more information, see :ref:`Controlling Content Visibility`.

=======================================
Use the Outline to Hide a Unit
=======================================

#. Click the Settings icon in the unit box:
   
   .. image:: ../../../shared/building_and_running_chapters/Images/outline-unit-settings.png
    :alt: The unit settings icon circled

   The **Settings** dialog box opens.

#. Check **Hide from students**.

   .. image:: ../../../shared/building_and_running_chapters/Images/outline-unit-settings-dialog.png
    :alt: The unit hide from students setting

#. Click **Save**.

=======================================
Make a Hidden Unit Visible to Students
=======================================

Before you make a hidden unit visible to students, be aware that course content
will immediately be visible to students, as follows:

* For a hidden unit that previously was published, clearing the check box
  publishes the current content for the unit. If you made changes to the unit
  while is was hidden, those draft changes are published.

* When you make a section or subsection that was previously hidden visible to
  students, draft content in units is *not* published. Changes you made since
  last publishing units are not made visible to students.

You can make a hidden unit visible to students from the unit page or the course
outline. Follow the instructions above and clear the **Hide from students**
checkbox.

You are prompted to confirm that you want to make the unit visible to students.

********************************
Delete a Unit
********************************

You delete a unit from the course outline.

When you delete a unit, you delete all components within the unit.

.. warning::  
 You cannot restore course content after you delete it. To ensure you do not
 delete content you may need later, you can move any unused content to a
 section in you

To delete a unit:

#. Click the delete icon in the box for the unit you want to delete:

.. image:: ../../../shared/building_and_running_chapters/Images/section-delete.png
 :alt: The section with Delete icon circled

2. When you receive the confirmation prompt, click **Yes, delete this
   unit**.
