.. _Cohorted Courseware Overview:


###################################
학습집단별 강좌 내용 만들기
###################################

강좌에서 학습집단을 활성화했다면 :ref:`cohorts enabled<Enabling and Configuring Cohorts>` 각 학습집단에 속한 학습자에게 다른 학습 경험을 제공할 수 있다.

일부 학습자에게 다른 학습자와 다른 내용을 제공할 수 있도록 강좌를 설계할 수 있다. You do this by creating :ref:`content groups<About Content Groups>`스튜디오에서 콘텐츠 그룹을 만들고, 하나 또는 그 이상의 콘텐츠 그룹에게만 공개되는 특정 구성 요소를 지정할 수 있다. 하나 이상의 학습집단을 하나의 콘텐츠 그룹으로 결합시킨다면, 콘텐츠 그룹으로 결합된 학습집단의 학습자 만이 그들을 위해 설계된 강좌의 내용을 볼 수 있다.

콘텐츠 그룹에 대한 세부적인 사항은, 콘텐츠 그룹 see :ref:`About Content Groups` 에서 확인할 수 있다. 예시: 학습집단별 강좌 내용에서 학습집단별 강좌 내용 :ref:`Cohorted Courseware Example` 의 사례를 참고할 수 있다.


학습집단별 강좌 내용을 생성하기 위해서는 다음의 절차를 완료해야 한다.

스튜디오에서:

#. :ref:`Enable cohorts in your course<Enabling and Configuring Cohorts>`.
#. :ref:`Create content groups<Creating Content Groups>`. 
#. :ref:`Specify components in courseware as visible only to particular content
   groups<Specify Components in Courseware as Visible Only to Certain Content
   Groups>`.
     
LMS에서: 

#. :ref:`Assign students to cohorts<Options for Assigning Students to Cohorts>`.  
#. :ref:`Associate one or more cohorts with a content group<Associate Cohorts
   with Content Groups>`.
#. :ref:`Preview cohort-specific courseware<Preview Cohort Specific Courseware>`.


.. _Cohorted Courseware Example:

***********************************
예시: 학습 집단별 강좌 내용
***********************************

한 대학의 졸업생과 현재 이 대학에 재학 중인 학습자로 구성된 두 개의 학습집단 :ref:`cohorts<Cohorts Overview>` 이 있는 강좌를 가정하자. 두 개의 학습 집단 중 어디에도 속하지 않는 학습자는 이들이 코스웨어 또는 토의 게시판에 방문하였을 때, 기본 학습 집단인 세 번째 학습 집단에 자동적으로 배치될 것이다. 학습 집단을 활성화하고 학습자를 학습 집단에 배치하는 방법에 대한 자세한 정보는 학습 집단 기능 활성화 및 설정하기 :ref:`Enabling and Configuring Cohorts` 에서 참고할 수 있다. 

모든 학습자가 대체로 동일 학습 경험을 가질 수 있도록 하고자 하며, 대학과 관련한 두 개의 학습 집단의 학습자에게는 그들이 흥미를 가질 수 있는 특정한 내용들을 제공 하고자 한다.

모든 학습이 끝난 후에, 대학 총장과 단과대학장 등 다양한 대학 관계자의 비디오 메시지를 포함시킬 계획이다. 이러한 비디오는 이 대학 재학생 및 졸업생 학습 집단에게만 제공될 것이다. 또한 모든 학습이 끝난 후에, 해당 강좌에서 다룬 내용을 테스트하는 퀴즈를 포함시키고자 한다. 이 퀴즈는 강좌에 등록한 모든 학생들에게 보여질 것이다. 

이를 위해, 스튜디오의 **그룹 설정** 페이지에서 **University-Specific Content** 라는 하나의 콘텐츠 그룹을 생성한다. 교수자 대시보드의 **회원** 에서, “대학 졸업생”과 “대학 재학생” 학습 집단을  “University-Specific Content”라는 콘텐츠 그룹에 결합시킨다. 

강좌 개요에서, 각 학습의 마지막 비디오 구성 요소를 “University-Specific Content” 콘텐츠 그룹만 볼 수 있도록 공개 설정을 변경한다. 콘텐츠 그룹이 구성 요소의 공개 설정에서 명시되지 않았다면, 모든 학습자가 퀴즈를 볼 수 있으므로 퀴즈 구성 요소의 공개 설정을 편집할 필요가 없다.

마지막 단계로, 의도한 바와 같이 학습자가 콘텐츠를 볼 수 있는지 LMS 에서 강좌를 사전 검토한다. 콘텐츠 그룹에 속하지 않은 **학습자** 는 학습이 끝난 후 퀴즈를 볼 수 있지만, 대학과 관련한 비디오를 볼 수 없음을 확인해야 한다. “University-Specific Content” 콘텐츠 그룹에 속한 학습자라면 대학과 관련한 비디오와 퀴즈를 학습이 끝난 후에 볼 수 있음을 확인해야 한다. 


.. _About Content Groups:

**************
콘텐츠 그룹
**************

콘텐츠 그룹은 특정 강좌 콘텐츠를 있는 가상의 학습자 분류이다. 특정 강좌 콘텐츠를 일부 학습자의 학습집단 :ref:`cohorts<Cohorts Overview>` 에게만 볼 수 있게 지정하기 위해서 콘텐츠 그룹을 사용할 수 있다. 

스튜디오에서 콘텐츠 그룹을 생성할 수 있으며, 구성 요소가 하나 또는 그 이상의 콘텐츠 그룹만 선택적으로 볼 수 있도록 **강좌 한 눈에 보기** 에서 공개 설정을 사용할 수 있다. 공개 설정에 명확히 제한된 설정이 없는 구성 요소는 학습집단에 상관 없이 모든 학습자가 볼 수 있다.

콘텐츠 그룹은 하나 이상의 학습 집단과 결합될 때까지 강좌 구성 요소의 공개 설정에 영향을 미치지 않는다. 강좌의 콘텐츠를 콘텐츠 그룹이 볼 수 있도록 지정하고, 하나 또는 그 이상의 학습 집단을 콘텐츠 그룹에 결합시키면, 이 학습 집단들은 지정된 콘텐츠를 볼 수 있게 된다.

학습 집단별 강좌 내용 생성하기 위해 콘텐츠 그룹을 사용하는 사례는 예시: 학습 집단별 강좌 내용 
:ref:`Cohorted Courseware Example` 을 살펴볼 수 있다.


.. _Creating Content Groups:

*********************
콘텐츠 그룹 생성
*********************

#. 스튜디오에서, **설정** 을 선택한 뒤 **그룹 설정** 을 선택한다. 
 
#. **그룹 설정 페이지** 에서, **새로운 콘텐츠 그룹**을 클릭한다.
   
.. image:: ../../../shared/building_and_running_chapters/Images/Cohorts_AddContentGroup.png
 :width: 600
 :alt: Button on Group Configurations page for adding first content group

3. 콘텐츠 그룹 이름을 입력한 후 **만들기** 를 클릭한다. 새로 만들어진 콘텐츠 그룹의 이름이 화면에 나타난다. 

#. 원하는 수 만큼 이 과정을 반복하여 콘텐츠 그룹을 만든다.

콘텐츠 그룹을 생성한 다음, 강좌 개요에서 특정 콘텐츠 그룹이 볼 수 있는 구성 요소를 설정할 수 있다. 자세한 사항은 특정 콘텐츠 그룹에게만 구성 요소 공개하기 :ref:`Specify Components in Courseware as Visible Only to Certain Content
Groups` 에서 볼 수 있다.

교수자 대시보드에서, 각 콘텐츠 그룹에 하나 또는 그 이상의 학습 집단을 결합할 수 있다. 자세한 사항은 학습 집단을 콘텐츠 그룹에 결합하기 :ref:`Associate Cohorts with Content Groups` 에서 볼 수 있다. 

.. note:: 콘텐츠 그룹을 생성하면, 이를 삭제할 수 없다. 콘텐츠 그룹과 학습 집단의 결합은 결합을 **선택하지 않도록** 변경함으로써 제거할 수 있다..


.. _Specify Components in Courseware as Visible Only to Certain Content Groups:

*****************************************************************************
특정 콘텐츠 그룹에게만 구성 요소 공개하기
*****************************************************************************

After you create at least one content group, you can edit your course in Studio
and modify the visibility settings of components that you want to make visible
only to particular content groups.

.. note:: You do not need to edit the visibility settings of components that are
   intended for all students. Components that you do not explicitly indicate as
   visible to a group are visible to all students enrolled in your course,
   regardless of the cohort that they belong to.

You can specify content as visible to content groups only at the component level
in a unit. You cannot specify entire units, subsections, or sections for
visibility to content groups.

In a separate task, you create cohorts and associate content groups with
cohorts. Then, only the cohorts associated with content groups which you
selected in a component's visibility settings can view the component. See
:ref:`Associate Cohorts with Content Groups` for details about associating
cohorts with content groups.

To specify components as visible only to particular content groups, follow these
steps.

#. In Studio, select **Content**, then select **Outline**. 
   
#. For each component that you want to make visible only to a particular
   content group or groups, click the unit name, then click the **Visibility
   Settings** icon.

.. image:: ../../../shared/building_and_running_chapters/Images/Cohorts_VisibilitySettingInUnit.png
  :alt: Screen capture of unit in course outline with visibility setting icon highlighted 

3. In the **Editing visibility** dialog, select **Specific Content Groups**,
   then select the checkbox for each content group for which you want the current
   component to be visible.

.. image:: ../../../shared/building_and_running_chapters/Images/Cohorts_EditVisibility.png
  :width: 400
  :alt: Screen capture of unit in course outline with visibility setting icon highlighted 

4. Click **Save**.

The **Visibility Settings** icon for the component is now black, and the
publishing details for the course section in the sidebar refresh to indicate
that some content is visible only to particular groups.

.. image:: ../../../shared/building_and_running_chapters/Images/Cohorts_VisibilitySomeGroup.png
   :alt: Visibility icon is black when visibility for a component is restricted

.. image:: ../../../shared/building_and_running_chapters/Images/Cohorts_OnlyVisibleToParticularGroups.png   
   :alt: Course outline sidebar shows visibility icon and note indicating that some content in the unit is visible only to particular group.

For details about previewing your course to ensure that students in a cohort
correctly see the content intended for them, see :ref:`Preview Cohort Specific
Courseware`.

.. note:: In addition to visibility settings for content groups, a student's
   ability to see a course component also depends on whether it is hidden from
   students, whether the unit is published, and the course's release date. For
   details about previewing courseware in general, see :ref:`Preview Course
   Content`.

.. _Associate Cohorts with Content Groups:

*************************************
Associate Cohorts with Content Groups
*************************************

After you create a content group, you can associate it with one or more cohorts
with which you want to share the same special content in your course.

.. note:: A content group can be associated with more than one cohort; a cohort
   cannot be associated with more than one content group.

To associate a cohort with a content group, follow these steps:

#. In the LMS, select **Instructor**, then select **Membership**. 
   
#. Scroll to the **Cohort Management** section at the bottom.

#. From the drop down list, select the cohort to which you want to associate
   your content group.
   
#. Click the **Settings** tab for the selected cohort.

#. Under **Associated Content Group**, choose the **Select a Content Group** option.

#. From the drop down list, select the content group that you want your cohort
   to be associated with.

.. image:: ../../../shared/building_and_running_chapters/Images/Cohorts_AssociateWithContentGroup.png
   :alt: Visibility icon is black when visibility for a component is restricted

7. Click **Save**.
   
   You have now associated your content group with a cohort. Any course content
   that you :ref:`designate as visible to that content group<Specify Components
   in Courseware as Visible Only to Certain Content Groups>` is visible to
   students in the associated cohort or cohorts.

You can associate additional cohorts with the same or a different content group
by repeating steps 3 to 7.

For an example of using content groups to create cohort-specific courseware, see
:ref:`Cohorted Courseware Example`.


.. _Preview Cohort Specific Courseware:

*************************************
Preview Cohort-Specific Courseware
*************************************

After you designate components in your course as being visible only to certain
content groups, you can preview your courseware to ensure that each group
correctly sees the content intended for them.

.. note:: In addition to visibility settings for content groups, a student's
   ability to see a course component also depends on whether it is hidden from
   students, whether the unit is published, and the course's release date. For
   details about previewing courseware in general, see :ref:`Preview Course
   Content`.

You can view the course as a member of these groups:


.. list-table::
    :widths: 15 30
    :header-rows: 1

    * - Role
      - When You "View As" This Role
    * - Staff
      - You see all content in the course, including content
        that is hidden from students.
    * - Student
      - You see any content that is intended for all
        students.
    * - Student in <Content Group Name>            
      - You see content that is intended for all students, as well
        as any content specifically set to be visible to this content group.

#. In Studio, in the course outline, click **Preview Changes**. You see your
   course section in the **Courseware** section of the LMS.

#. In the navigation bar at the top of the page, select one of the options in
   the **View this course as** drop down list, as described in the table above.

.. image:: ../../../shared/building_and_running_chapters/Images/Cohorts_ViewCourseAs.png
   :alt: Visibility icon is black when visibility for a component is restricted


The course view refreshes and the content is presented as a member of the
selected content group would see it.

After your course is live, you can also see the live version as a student would
see it, by clicking **View Live** from Studio. For more information, see
:ref:`View Your Live Course`.
