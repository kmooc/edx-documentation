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

* `주제와 함께 공개 예정`_
* `공개일이 지정되지 않음 `_
* `주제 공개 후 소주제 공개 `_
* `Scheduled with Unpublished Changes`_
* `공개 후 변경 사항은 아직 게시되지 않음`_
* `공개됨`_

==========================
주제와 함께 공개 예정
==========================

소주제 공개일의 기본값은 주제의 공개일로 설정되어 있다. 
이에 따라, 학습자는 주제가 공개되는 날, 소주제의 게시된 콘텐츠를 볼 수 있다. 

다음 예시는 주제에 공개일이 지정되어 있을 때, 소주제가 어떻게 강좌 개요에서 보이는지를 나타낸다.

.. image:: ../../../shared/building_and_running_chapters/Images/subsection-scheduled.png
 :alt: A subsection scheduled to release with the section


========================
공개일이 지정되지 않음
========================

소주제를 포함하는 주제의 공개일이 지정되지 않으면, 학습자는 소주제를 볼 수 없다.

이에 따라 소주제의 학습활동의 게시 상태에 관계 없이, 학습자는 소주제 내부의 학습활동 역시 볼 수 없게 된다.

다음 예시는 공개일이 지정되지 않은 소주제가 어떻게 강좌 개요에서 보이는지를 나타낸다.

.. image:: ../../../shared/building_and_running_chapters/Images/subsection-unscheduled.png
 :alt: An unscheduled subsection

학습자가 콘텐츠를 볼 수 있게 하려면, 강좌 운영팀이 반드시 주제의 공개일을 지정해야 한다.

===================================
주제 공개 후 소주제 공개 
===================================

주제를 먼저 공개하고, 그 주제에 속한 소주제를 나중에 공개할 수 있다.

소주제 내부의 학습활동이 게시 상태이더라도, 공개일이 먼 미래로 되어 있는 경우 학습자가 콘텐츠를 볼 수 없다.  

다음 예시는 주제가 먼저 공개된 후 공개될 예정인 소주제가 어떻게 강좌 개요에서 보이는지를 나타낸다.

.. image:: ../../../shared/building_and_running_chapters/Images/subsection-scheduled-different.png
 :alt: A subsection scheduled to release later than the section

소주제를 공개하기로 예정된 날짜가 지나야만, 학습자가 소주제를 볼 수 있다.  

==================================
공개 예정인 소주제의 학습활동 변경
==================================

소주제가 공개되기 전, 학습활동이 게시 상태이더라도 학습활동을 변경할 수 있다. 그후 학습자는 소주제 공개일에 맞춰 변경된 학습활동을 보게 된다.

하지만 소주제가 이미 공개된 상태라면, 학습자는 변경된 학습활동을 볼 수 없다.
따라서 학습활동을 변경할 경우, 다시 게시해야 한다. 

다음 예시는 아직 게시되지 않은 변경된 학습활동이 있는, 공개 예정 소주제가 어떻게 학습자에게 보이는지를 나타낸다. 

.. image:: ../../../shared/building_and_running_chapters/Images/section-scheduled-with-changes.png
 :alt: A scheduled subsection with unpublished changes

==================================
공개된 소주제의 학습활동 변경 
==================================

공개된 소주제의 학습활동을 변경한다면, 그것을 다시 게시하지 않는 한 학습자는 변경된 학습활동을 볼 수 없다.

다음 예시는 아직 게시되지 않은 변경된 학습활동이 있는, 공개된 소주제가 어떻게 학습자에게 보이는지를 나타낸다. 

.. image:: ../../../shared/building_and_running_chapters/Images/section-released-with-changes.png
 :alt: A released subsection with unpublished changes

===========================
공개됨
===========================

학습자는 공개된 소주제를 보게 된다. 그런데 소주제 내부에서 이때 게시 상태인 학습활동만을 볼 수 있다.

다음 예시는 공개된 소주제가 강좌 개요에서 어떻게 보이는지를 나타낸다.

.. image:: ../../../shared/building_and_running_chapters/Images/subsection-released.png
 :alt: A released subsection

===========================
강좌 운영팀에게만 공개됨
===========================

소주제에 학습활동을 추가하되, 이것을 학습자에게는 비공개로 하여 강좌 운영팀만 볼 수 있도록 할 수 있다

상위 소주제가 공개되더라도, 학습자는 비공개로 설정한 학습활동을 볼 수 없다.

다음 예시는 소주제에 강좌 운영팀만 볼 수 있는 학습활동이 있을 경우, 강좌 개요에서 어떻게 보이는지를 나타낸다.

.. image:: ../../../shared/building_and_running_chapters/Images/section-hidden-unit.png
 :alt: A section with a hidden unit 

.. _Create a Subsection:

****************************
소주제 만들기
****************************

소주제를 만드려면,


#. 강좌 개요에서, 신규 소주제를 만들고 싶은 주제를 펼친다.

#. 펼친 주제의 하단에 있는 **+ 새로운 소주제**를 클릭한다.
   그러면 소주제가 추가되며, 소주제명을 입력할 수 있게 된다.
   
#. 소주제명을 입력한다.

#. 필요한 경우, 이어서 :ref:`Add units<Create a Unit>` 을 추가한다.
   
신규 소주제를 추가한 후, :ref:`test course content <Testing Your Course
Content>` 를 권장한다.

********************************
소주제명 바꾸기
********************************

소주제명 위에 마우스를 갖다대면 소주제명 옆에 편집 아이콘이 나타날 것이다.
편집 아이콘을 클릭한다. 그러면 편집가능한 상태의 입력란이 생기게 된다. 그곳에 새 이름을 입력하고 탭 키를 누르거나 입력란 바깥의 영역을 클릭하면 그 이름이 저장된다.

.. _Set a Subsection Release Date:

********************************
소주제 공개일 설정하기
********************************

소주제의 공개일을 설정하려면

#. 소주제 영역에서 설정 아이콘을 클릭한다.
   
   .. image:: ../../../shared/building_and_running_chapters/Images/subsections-settings-icon.png
    :alt: The subsection settings icon circled

   **설정** 대화 상자가 열릴 것이다.

#. 주제의 공개일시를 입력한다.

   .. image:: ../../../shared/building_and_running_chapters/Images/subsection-settings-release.png
    :alt: The subsection release date settings

#. **저장** 을 클릭한다.

:ref:`Release Dates` 에 더 자세한 안내가 나와있다.

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
