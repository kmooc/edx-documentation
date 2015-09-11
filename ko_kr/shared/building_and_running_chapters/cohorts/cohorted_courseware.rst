.. _Cohorted Courseware Overview:


###################################
학습집단별 강좌 내용 만들기
###################################

강좌에서 학습집단을 활성화했다면 :ref:`Enabling and Configuring Cohorts` 각 학습집단에 속한 학습자에게 다른 학습 경험을 제공할 수 있다.

일부 학습자에게 다른 학습자와 다른 내용을 제공할 수 있도록 강좌를 설계할 수 있다. 스튜디오에서 콘텐츠 그룹 :ref:`About Content Groups` 을 만들고, 하나 또는 그 이상의 콘텐츠 그룹에게만 공개되는 특정 구성 요소를 지정할 수 있다. 하나 이상의 학습집단을 하나의 콘텐츠 그룹으로 결합시킨다면, 콘텐츠 그룹으로 결합된 학습집단의 학습자 만이 그들을 위해 설계된 강좌의 내용을 볼 수 있다.

콘텐츠 그룹에 대한 세부적인 사항은, 콘텐츠 그룹 :ref:`About Content Groups` 에서 확인할 수 있다. 예시: 학습집단별 강좌 내용에서 학습집단별 강좌 내용 :ref:`Cohorted Courseware Example` 의 사례를 참고할 수 있다.


학습집단별 강좌 내용을 생성하기 위해서는 다음의 절차를 완료해야 한다.

스튜디오에서:

#. :ref:`Enabling and Configuring Cohorts`.
#. :ref:`Creating Content Groups`. 
#. :ref:`Specify Components in Courseware as Visible Only to Certain Content
   Groups`.
     
LMS에서: 

#. :ref:`Options for Assigning Students to Cohorts`.  
#. :ref:`Associate Cohorts
   with Content Groups`.
#. :ref:`Preview Cohort Specific Courseware`.


.. _Cohorted Courseware Example:

***********************************
예시: 학습집단별 강좌 내용
***********************************

한 대학의 졸업생과 현재 이 대학에 재학 중인 학습자로 구성된 두 개의 학습집단 :ref:`Cohorts Overview` 이 있는 강좌를 가정하자. 두 개의 학습집단 중 어디에도 속하지 않는 학습자는 이들이 코스웨어 또는 토의 게시판에 방문하였을 때, 기본 학습집단인 세 번째 학습집단에 자동적으로 배치될 것이다. 학습집단을 활성화하고 학습자를 학습집단에 배치하는 방법에 대한 자세한 정보는 학습집단 기능 활성화 및 설정하기 :ref:`Enabling and Configuring Cohorts` 에서 참고할 수 있다. 

모든 학습자가 대체로 동일 학습 경험을 가질 수 있도록 하고자 하며, 대학과 관련한 두 개의 학습집단의 학습자에게는 그들이 흥미를 가질 수 있는 특정한 내용들을 제공 하고자 한다.

모든 학습이 끝난 후에, 대학 총장과 단과대학장 등 다양한 대학 관계자의 비디오 메시지를 포함시킬 계획이다. 이러한 비디오는 이 대학 재학생 및 졸업생 학습집단에게만 제공될 것이다. 또한 모든 학습이 끝난 후에, 해당 강좌에서 다룬 내용을 테스트하는 퀴즈를 포함시키고자 한다. 이 퀴즈는 강좌에 등록한 모든 학생들에게 보여질 것이다. 

이를 위해, 스튜디오의 **그룹 설정** 페이지에서 **University-Specific Content** 라는 하나의 콘텐츠 그룹을 생성한다. 교수자 대시보드의 **회원** 에서, “대학 졸업생”과 “대학 재학생” 학습집단을  “University-Specific Content”라는 콘텐츠 그룹에 결합시킨다. 

강좌 개요에서, 각 학습의 마지막 비디오 구성 요소를 “University-Specific Content” 콘텐츠 그룹만 볼 수 있도록 공개 설정을 변경한다. 콘텐츠 그룹이 구성 요소의 공개 설정에서 명시되지 않았다면, 모든 학습자가 퀴즈를 볼 수 있으므로 퀴즈 구성 요소의 공개 설정을 편집할 필요가 없다.

마지막 단계로, 의도한 바와 같이 학습자가 콘텐츠를 볼 수 있는지 LMS 에서 강좌를 사전 검토한다. 콘텐츠 그룹에 속하지 않은 **학습자** 는 학습이 끝난 후 퀴즈를 볼 수 있지만, 대학과 관련한 비디오를 볼 수 없음을 확인해야 한다. “University-Specific Content” 콘텐츠 그룹에 속한 학습자라면 대학과 관련한 비디오와 퀴즈를 학습이 끝난 후에 볼 수 있음을 확인해야 한다. 


.. _About Content Groups:

**************
콘텐츠 그룹
**************

콘텐츠 그룹은 특정 강좌 콘텐츠를 있는 가상의 학습자 분류이다. 특정 강좌 콘텐츠를 일부 학습자의 학습집단 :ref:`Cohorts Overview` 에게만 볼 수 있게 지정하기 위해서 콘텐츠 그룹을 사용할 수 있다. 

스튜디오에서 콘텐츠 그룹을 생성할 수 있으며, 구성 요소가 하나 또는 그 이상의 콘텐츠 그룹만 선택적으로 볼 수 있도록 **강좌 한 눈에 보기** 에서 공개 설정을 사용할 수 있다. 공개 설정에 명확히 제한된 설정이 없는 구성 요소는 학습집단에 상관 없이 모든 학습자가 볼 수 있다.

콘텐츠 그룹은 하나 이상의 학습집단과 결합될 때까지 강좌 구성 요소의 공개 설정에 영향을 미치지 않는다. 강좌의 콘텐츠를 콘텐츠 그룹이 볼 수 있도록 지정하고, 하나 또는 그 이상의 학습집단을 콘텐츠 그룹에 결합시키면, 이 학습집단들은 지정된 콘텐츠를 볼 수 있게 된다.

학습집단별 강좌 내용 생성하기 위해 콘텐츠 그룹을 사용하는 사례는 예시: 학습집단별 강좌 내용 
:ref:`Cohorted Courseware Example` 을 살펴볼 수 있다.


.. _Creating Content Groups:

*********************
콘텐츠 그룹 생성
*********************

#. 스튜디오에서, **설정** 을 선택한 뒤 **그룹 설정** 을 선택한다. 
 
#. **그룹 설정 페이지** 에서, **새로운 콘텐츠 그룹** 을 클릭한다.
   
.. image:: ../../../shared/building_and_running_chapters/Images/Cohorts_AddContentGroup.png
 :width: 600
 :alt: Button on Group Configurations page for adding first content group

3. 콘텐츠 그룹 이름을 입력한 후 **만들기** 를 클릭한다. 새로 만들어진 콘텐츠 그룹의 이름이 화면에 나타난다. 

#. 원하는 수 만큼 이 과정을 반복하여 콘텐츠 그룹을 만든다.

콘텐츠 그룹을 생성한 다음, 강좌 개요에서 특정 콘텐츠 그룹이 볼 수 있는 구성 요소를 설정할 수 있다. 자세한 사항은 특정 콘텐츠 그룹에게만 구성 요소 공개하기 :ref:`Specify Components in Courseware as Visible Only to Certain Content
Groups` 에서 볼 수 있다.

교수자 대시보드에서, 각 콘텐츠 그룹에 하나 또는 그 이상의 학습집단을 결합할 수 있다. 자세한 사항은 학습집단을 콘텐츠 그룹에 결합하기 :ref:`Associate Cohorts with Content Groups` 에서 볼 수 있다. 

.. note:: 콘텐츠 그룹을 생성하면, 이를 삭제할 수 없다. 콘텐츠 그룹과 학습집단의 결합은 결합을 **선택하지 않도록** 변경함으로써 제거할 수 있다.


.. _Specify Components in Courseware as Visible Only to Certain Content Groups:

*****************************************************************************
특정 콘텐츠 그룹에게만 구성 요소 공개하기
*****************************************************************************

최소 하나의 콘텐츠 그룹을 생성한 후, 스튜디오에서 강좌를 편집하고, 특정 콘텐츠 그룹만 보길 원하는 구성 요소의 공개 설정을 수정할 수 있다.

.. note:: 모든 학습자가 볼 수 있기를 원하는 구성 요소에 대해서 공개 설정을 편집할 필요는 없다. 어떤 집단이 볼 수 있도록 분명하게 명시하지 않은 구성 요소는 학습자가 속해 있는 학습집단에 상관 없이 강좌에 등록한 모든 학습자가 볼 수 있다.

학습 활동의 구성 요소 수준에서 콘텐츠 그룹만 볼 수 있는 콘텐츠를 지정할 수 있다. 모든 학습 활동, 소주제, 주제를 콘텐츠 그룹만 볼 수 있도록 지정할 수는 없다.

과제를 구분하기 위해, 학습집단을 생성하고 콘텐츠 그룹과 학습집단을 결합해야 한다. 다음으로 구성 요소 공개 설정에서 선택한 콘텐츠 그룹에 결합된 학습집단만이 구성 요소를 볼 수 있다. 학습집단을 콘텐츠 그룹에 결합시키는 세부적인 사항은 학습집단을 콘텐츠 그룹에 결합하기 :ref:`Associate Cohorts with Content Groups` 에서 확인할 수 있다.

특정 콘텐츠 그룹만 볼 수 있도록 구성 요소를 지정하기 위해, 다음의 절차를 따른다.

#. 스튜디오에서 **콘텐츠** 를 선택한 후, **강좌 개요** 를 선택한다. 
   
#. 특정 콘텐츠 그룹만 볼 수 있도록 설정하고자 하는 구성 요소의 학습 활동 이름을 클릭한 후, **공개 설정** 아이콘을 클릭한다.  

.. image:: ../../../shared/building_and_running_chapters/Images/Cohorts_VisibilitySettingInUnit.png
  :alt: Screen capture of unit in course outline with visibility setting icon highlighted 

3. **공개 설정 편집** 창에서, **특정 콘텐츠 그룹** 을 선택하고 현재 구성 요소를 볼 수 있도록 설정하고자 하는 콘텐츠 그룹의 체크 박스에 체크한다. 

.. image:: ../../../shared/building_and_running_chapters/Images/Cohorts_EditVisibility.png
  :width: 400
  :alt: Screen capture of unit in course outline with visibility setting icon highlighted 

4. **저장** 을 클릭한다.

구성 요소의 **공개 설정** 아이콘이 검정색으로 변하고, 사이드 바(sidebar)의 강좌 영역의 세부 사항이 일부 콘텐츠가 특정 그룹에게만 공개된다는 최신 정보로 업데이트 된다. 

.. image:: ../../../shared/building_and_running_chapters/Images/Cohorts_VisibilitySomeGroup.png
   :alt: Visibility icon is black when visibility for a component is restricted

.. image:: ../../../shared/building_and_running_chapters/Images/Cohorts_OnlyVisibleToParticularGroups.png   
   :alt: Course outline sidebar shows visibility icon and note indicating that some content in the unit is visible only to particular group.

학습집단에 속해 있는 학습자가 의도한 바와 같이 정확히 콘텐츠를 볼 수 있는지 확인하기 위한 미리 보기는, 학습집단별 강좌 내용 미리 보기 :ref:`Preview Cohort Specific Courseware`  

.. note:: 콘텐츠 그룹의 공개 설정 외에도 학습자에게 학습 활동을 숨길지, 강좌 공개일에 맞춰 학습활동을 공개할지를 설정할 수 있다. 일반적인 코스웨어 미리 보기에 대한 자세한 사항은 강좌 콘텐츠 미리 보기 :ref:`Preview Course Content` 에서 확인할 수 있다.   .

.. _Associate Cohorts with Content Groups:

*************************************
학습집단을 콘텐츠 그룹에 결합하기
*************************************

콘텐츠 그룹을 생성한 후, 특정 콘텐츠를 강좌에서 공유하고자 하는 하나 이상의 학습집단과 콘텐츠 그룹을 결합할 수 있다.

.. note:: 콘텐츠 그룹은 하나 이상의 학습집단과 결합될 수 있지만, 학습집단은 하나 이상의 콘텐츠 그룹에 결합될 수 없다.

학습집단을 콘텐츠 그룹에 결합시키기 위해서는 다음의 절차를 따른다.

#. LMS에서 **교수자** 를 선택한 후 **회원** 을 선택한다. 
   
#. 하단의 **학습집단 관리** 를 찾는다. 

#. 드롭다운 목록에서, 콘텐츠 그룹에 결합시키고자 하는 학습집단을 선택한다.
   
#. 학습집단을 선택하기 위해 **설정** 을 클릭한다.

#. **콘텐츠 그룹 결합** 에서, **콘텐츠 그룹 선택** 옵션을 고른다. 

#. 드롭다운 목록에서, 학습집단을 결합시키고자 하는 콘텐츠 그룹을 선택한다.

.. image:: ../../../shared/building_and_running_chapters/Images/Cohorts_AssociateWithContentGroup.png
   :alt: Visibility icon is black when visibility for a component is restricted

7. **저장** 을 클릭한다.
   
   이후 콘텐츠 그룹과 학습집단이 결합된다. 이 콘텐츠 그룹에만 공개되도록 설정된 강좌의 콘텐츠들 :ref:`Specify Components in Courseware as Visible Only to Certain Content Groups` 은 결합된 학습집단과 기존의 학습집단에 속한 학습자에게 공개된다.

다른 학습집단을 동일 콘텐츠 그룹이다 또 다른 콘텐츠 그룹에 결합시키기 위해서는 위의 3.에서 7.의 단계를 반복하면 된다.

콘텐츠 그룹을 사용하여 학습집단별 강좌 내용을 생성하는 예는 예시: 학습집단별 강좌 내용 :ref:`Cohorted Courseware Example` 을 본다. 


.. _Preview Cohort Specific Courseware:

*************************************
학습집단별 강좌 내용 미리 보기
*************************************

특정 콘텐츠 그룹만 볼 수 있도록 강좌의 구성 요소를 지정한 후, 각 그룹이 의도한 바와 같이 학습 내용을 올바르게 볼 수 있는지 확인하기 위해 미리 보기를 할 수 있다

.. note:: I콘텐츠 그룹의 공개 설정 외에도 학습자에게 학습 활동을 숨길지, 강좌 공개일에 맞춰 학습활동을 공개할지를 설정할 수 있다. 일반적인 코스웨어 미리 보기에 대한 자세한 사항은 강좌 콘텐츠 미리 보기 :ref:`Preview Course Content` 에서 확인할 수 있다. 

아래는 강좌에서 역할에 따라 볼 수 있는 내용에 대한 것이다:


.. list-table::
    :widths: 15 30
    :header-rows: 1

    * - 강좌에서의 역할
      - When You "View As" This Role
    * - 강좌 운영팀
      - 학습자에게 숨겨진 콘텐츠를 포함하여 강좌의 모든 콘텐츠를 볼 수 있다.
    * - 학습자
      - 모든 학습자를 위해 공개된 모든 콘텐츠를 볼 수 있다.
    * - <콘텐츠 그룹 이름>에 속한 학습자           
      - 모든 학습자를 위해 공개된 콘텐츠와, 자신이 속한 콘텐츠 그룹에 공개된 특정 콘텐츠를 볼 수 있다.

#. 스튜디오의 강좌 개요에서 **미리 보기 변경** 을 클릭한다. LMS의 **강의내용** 에서 강좌 영역을 볼 수 있다.

#. 페이지 상단의 네비게이션 바에서, 이 강좌의 드롭다운 목록에서 강좌 운영 팀, 학습자, **<콘텐츠 그룹 이름>** 에 속한 학습자 중 하나를 선택하면 선택한 역할에 따라 위의 표에서 설명한 바와 같이 강좌의 콘텐츠를 볼 수 있다.  

.. image:: ../../../shared/building_and_running_chapters/Images/Cohorts_ViewCourseAs.png
   :alt: Visibility icon is black when visibility for a component is restricted


강좌 미리 보기는 구성원을 다시 선택하면 선택한 콘텐츠 그룹의 구성원이 볼 수 있는 콘텐츠가 나타난다.

스튜디오의 적용 결과 보기 :ref:`View Your Live Course` 를 클릭하면 학습자가 보게 될 적용된 버전을 볼 수 있다. 보다 많은 정보는 적용 결과 보기에서 확인할 수 있다.

