.. _Developing Course Units:

###################################
학습활동
###################################

학습활동을 만들기 전에, 우선 다음 사항을 이해해야 한다.

* `학습활동이란?`_
* `강좌 개요에서 학습활동 보기`_
* `강좌 개요에서 학습활동 보기`_
* `학습자 화면에서 학습활동 보기`_
* `학습활동 게시 상태 및 학습자 공개 설정`_
* `학습활동 게시 상태`_

학습활동과 관련된 작업은 다음과 같은 것이 있다.

* `학습활동 만들기`_
* `학습활동 편집하기`_
* `학습활동 미리보기`_
* `학습활동 게시하기`_
* `학습활동 변경 취소하기`_
* `게시된 학습활동 보기`_
* `학습활동 감추기`_
* `학습활동 삭제하기`_

강좌 운영팀은 학습활동에 구성요소를 추가할 수 있다. 
이에 관해 :ref:`강좌 구성요소<Developing Course
Components>` 에 자세한 안내가 있다. 

.. _학습활동이란?:

****************************
학습활동이란?
****************************

학습활동은 :ref:`소주제<Developing Course Subsections>` 의 일부로써, 
학습자가 소주제를 클릭하면 한 번에 하나씩 볼 수 있다. 

1개의 학습활동은 1개 이상의 :ref:`소주제<Developing Course Components>` 를 가질 수 있는데, 이러한 구성요소로는 :ref:`HTML 콘텐츠<Working with HTML Components>`,
:ref:`문제<Working with Problem Components>`, :ref:`게시판<Working with Discussion Components>` 및 
:ref:`동영상<Working with Video Components>` 이 있다.

.. _강좌 개요에서 학습활동 보기:

****************************
강좌 개요에서 학습활동 보기
****************************

학습활동을 보려면, 주제와 소주제를 먼저 펼쳐야 한다. 이에 대한 안내는 :ref:`강좌 개요 살펴보기` 에 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/outline-callouts.png
 :alt: An outline with callouts for sections, subsections, and units

.. _Studio에서 학습활동 보기:

****************************
Studio에서 학습활동 보기
****************************

강좌 개요에서 소주제명을 클릭하면, **학습활동** 이 나온다.

다음 예시는 1개 학습활동에 2개의 구성요소가 있는 화면이며, 동그랗게 표시된 부분은 이를 학습 관리 시스템에서 볼 수 있는 버튼을 가리킨다.

.. image:: ../../../shared/building_and_running_chapters/Images/unit-page.png
 :alt: The Unit page

.. _학습자 화면에서 학습활동 보기:

****************************
학습자 화면에서 학습활동 보기
****************************

학습자는 강좌 내용에서 소주제에 있는 학습활동을 볼 수 있다. 다음 학습활동으로 넘어가려면 화살표 버튼을 눌러야 한다.

다음 예시는 1개의 소주제에 학습활동이 5개로 구성되어 있을 때, 어떻게 강좌 개요에서 보이는지를 나타낸다.

.. image:: ../../../shared/building_and_running_chapters/Images/Units_LMS.png
 :alt: Image of units from the student's point of view

.. _학습활동 작업 흐름:

************************************************
학습활동 작업 흐름
************************************************

먼저 :ref:`주제<Developing Course Sections>` 와 :ref:`소주제<Developing Course Subsections>` 을 만들면
학습활동을 만들 수 있게 된다.

학습활동을 만드는 기본 순서는 아래와 같은데,

#. :ref:`새 학습활동 만들기<Create a Unit>`.
#. :ref:`학습활동에 구성요소 추가하기<Add a Component>`.
#. :ref:`학습활도 게시하기<Publish a Unit>`.
   
학습활동을 게시한 후 

#. :ref:`학습활동에서 구성요소 수정하기<Developing Course Components>`.
#. :ref:`학습활동에서 수정하여 게시하기<Publish a Unit>`

작업이 가능하기도 하다.
   
다음 도표는 학습활동의 일반적인 작업흐름을 보여준다. 

.. image:: ../../../shared/building_and_running_chapters/Images/workflow-create-unit.png
 :alt: Diagram of the unit development workflow
   

이러한 단계를 거치다보면, 학습활동의 **게시 상태** 가 바뀌게 된다.

게시 상태는 학습자가 :ref:`공개일<Release Dates>`에 따른 활용가능한 콘텐츠를 조절한다. 

.. _학습활동 게시 상태 및 학습자 공개 설정:

*************************************************
학습활동 게시 상태 및 학습자 공개 설정
*************************************************

학습자가 학습활동을 볼 수 있는지 여부는 학습활동의 게시 상태에 따라 달라진다. 

* `초안 (게시된 적 없음)`_ 일 때, 학습자는 학습활동을 볼 수 없다. 

* `강좌 운영팀에게만 공개`_ 일 때, 학습자는 학습활동을 볼 수 없다. 이에 대해 `학습활동 감추기`_ 에 더 자세한 안내가 있다. 

* `아직 공개되지 않음`_  일 때, :ref:`공개일<Release Dates>` 전까지는 학습자가 학습활동을 볼 수 없다. 하지만 공개일이 되면, 게시 상태가 `공개됨`_ 로 바뀌게 된다.

* `공개됨`_ 일 때, 학습자는 학습활동을 볼 수 있다.
  
* `학습활동이 변경됨`_ 의 상태일 때, 주제의 :ref:`공개일 <Release Dates>` 이 이미 지난 경우라면 
학습자가 변경된 학습활동을 바로 볼 수 있는 것이 아니라, 변경 이전의 학습활동을 보게 된다.

:ref:`Controlling Content Visibility` 에 공개 설정에 대한 더 자세한 안내가 있다.

.. _학습활동 게시 상태:

************************************************
학습활동 게시 상태
************************************************ 

학습활동의 게시 상태로는 이러한 것들이 있다.

* `초안 (게시된 적 없음)`_
* `공개됨`_ 
* `아직 공개되지 않음`_ 
* `학습활동이 변경됨`_
* `강좌 운영팀에게만 공개`_

.. _초안 (게시된 적 없음):

========================
초안 (게시된 적 없음)
========================

새 학습활동을 만들어 구성요소를 추가할 때, 학습활동의 게시 상태는 **초안 (게시된 적 없음)** 이며 화면에는 다음과 같이 나타나게 된다.

.. image:: ../../../shared/building_and_running_chapters/Images/unit-never-published.png
 :alt: Status panel of a unit that has never been published

공개일이 지났더라도 강좌 운영팀이 Studio에서 작업중인 콘텐츠는 학습자에게 공개되지 않는다.

학습활동을 학습 관리 시스템에서 못보더라도, :ref:`강좌 콘텐츠 미리보기<Preview Course Content>` 에서 볼 수 있다.

학습활동을 학습자가 볼 수 있게 하려면, 반드시 :ref:`학습활동 게시<Publish a Unit>` 해야 한다는 것에 유의한다.

.. _공개됨:

====================
공개됨
====================

주제와 소주제의 공개일이 지난 경우로, 학습활동을 게시했으며 이후 변경하지 않았을 때의 상태이다.
강좌 운영팀과 학습자 모두 학습활동을 볼 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/unit-published.png
 :alt: Status panel of a unit that is published

.. _아직 공개되지 않음:

====================================
아직 공개되지 않음
====================================

학습활동을 게시한 상태지만, 아직 공개일이 지나지 않아 학습자가 볼 수 없다. 

.. image:: ../../../shared/building_and_running_chapters/Images/unit-published_unreleased.png
 :alt: Status panel of a unit that is published but not released

.. _Draft (Unpublished Changes):

===========================
학습활동이 변경됨
=========================== 

게시한 학습활동을 변경하면, 공개 여부와 관계 없이 학습활동의 상태가 
**학습활동이 변경됨** 으로 바뀐다.

.. image:: ../../../shared/building_and_running_chapters/Images/unit-pending-changes.png
 :alt: Status panel of a unit that has pending changes

Studio에서 강좌 운영팀은 작업중인 학습활동을 보게 되는 반면, 학습자는 공개일이 지난 경우 해당 학습활동의 지난 게시 버전을
보게 된다. 공개일이 지나지 않은 경우에는 학습자가 볼 수 없다. 

변경된 버전을 학습자가 보게 하려면, 반드시 
:ref:`publish the unit<Publish a Unit>` 해야 한다.


:ref:`강좌 콘텐츠 미리보기<Preview Course Content>` 를 통해
변경사항이 어떻게 적용되는지 미리 볼 수 있다.

.. _Visible to Staff Only:

===========================
강좌 운영팀에게만 공개
===========================

:ref:`학습활동 감추기<Hide a Unit from Students>` 상태일 때, 학습활동의 게시 상태가 **강좌 운영팀에게만 공개** 로 바뀌게 된다.

:ref:`주제<Hide a Section from Students>` 또는 :ref:`소주제<Hide a
Subsection from Students>` 상태이면 학습자가 학습활동을 볼 수 없다.

게시되었거나 공개일이 지났더라도 학습자가 이 상태의 학습활동은 볼 수 없다.

.. image:: ../../../shared/building_and_running_chapters/Images/unit-unpublished.png
 :alt: Status panel of a unit that has pending changes

.. _학습활동 만들기:

****************************
학습활동 만들기
****************************

강좌개요나 학습활동 페이지에서 학습활동을 만들 수 있다.

강좌개요에서 학습활동을 만드려면, 신규 학습활동을 추가하고 싶은 소주제를 펼친다.

#. In the outline, expand the subsection in which you want to create a new
   unit.
#. Click **New Unit** at the bottom of the expanded subsection. A new
   unit is added at the end of the subsection.
#. On the unit page, the unit name is selected. Edit the name as needed.
#. :ref:`Add components<Add a Component>` to the new unit as needed.

학습활동 페이지에서 학습활동을 만드려면,

#. 왼쪽 하단의 **학습 활동 위치** 에서, **새로운 학습활동** 을 추가한다.

   .. image:: ../../../shared/building_and_running_chapters/Images/unit_location.png
    :alt: The Unit Location panel in the Unit page

   그러면 새로 만든 학습활동의 페이지가 열린다.

#. 학습활동명을 입력한다. 

#. 필요하다면, :ref:`구성요소 추가하기<Add a Component>` 를 시작한다.

새로 만든 학습활동을 학습자가 볼 수 있게 하려면 :ref:`학습활동 게시하기<Publish a Unit>` 한다.


.. _학습활동 편집하기:

**************
학습활동 편집하기
**************

다음 방법으로 학습활동을 편집할 수 있다.

* `Edit the unit name`_
* :ref:`Develop components<Developing Course Components>`
* `Reorganize Components in Units`_

게시한 학습활동을 편집하면, 공개 여부와 관계 없이 학습활동의 상태가 
**학습활동이 변경됨** 으로 바뀐다.

변경된 버전을 학습자가 보게 하려면, 반드시 
:ref:`publish the unit<Publish a Unit>` 해야 한다.

==============================
학습활동명 편집
==============================

학습활동명을 바꾸려면, 학습활동명 위에 마우스를 갖다대면 편집 아이콘이 나타난다.

.. image:: ../../../shared/building_and_running_chapters/Images/unit-edit-icon.png
  :alt: The Edit Unit Name icon

편집 아이콘을 클릭하면, 이름을 편집할 수 있는 상태가 된다.
새 이름을 입력한 후 탭 키를 누르거나 이름 입력란 밖의 아무 곳이나 클릭하면, 이름이 저장된다.

==============================
구성요소 재구성하기
==============================

마우스를 이용해 구성요소를 원하는 위치로 옮기면, 구성방식을 바꿀 수 있다.

구성요소를 옮기려면, 구성요소 영역의 오른쪽 상단에 마우스를 갖다대면 마우스 커서가 십자가로 바뀌는 아이콘이 있다.
다음 이미지에서 마우스 커서가 위치한 아이콘을 말한다.

.. image:: ../../../shared/building_and_running_chapters/Images/unit-drag-selected.png
  :alt: A discussion component selected to drag it

구성요소를 클릭해 원하는 위치로 드래그하면 된다.

그러면 파란색의 윤곽선이 마우스를 따라 움직이고, 원하는 곳에 마우스를 놓으면 된다.
다음 이미지는 구성요소를 학습활동의 상단으로 움직이려고 할 때를 나타낸다.

.. image:: ../../../shared/building_and_running_chapters/Images/unit-drag-moved.png
 :alt: A component being dragged to a new location  

.. _학습활동 미리보기:

****************************
학습활동 미리보기
****************************

학습자가 학습활동을 보기 전에, 강좌 운영팀이 콘텐츠를 먼저 테스트해볼 수 있다.

학습활동을 게시하기 전이라면 학습활동을 미리볼 수 있다. 그러나 게시되었거나, 변경사항이 없다면 미리볼 수 없는 대신 학습활동의 적용 결과를 봐야 한다.

학습활동 페이지에서, 학습활동을 미리보려면 **미리보기** 를 클릭한다.

.. image:: ../../../shared/building_and_running_chapters/Images/preview_changes.png
 :alt: The Unit page with Preview Changes button circled

미리보기 모드에서 학습활동은 이렇게 열린다.

.. image:: ../../../shared/building_and_running_chapters/Images/preview_mode.png
 :alt: The unit in preview mode

게시된 학습활동을 변경할 때 새 창을 띄우면 편리하다.
새 창에서는 미리보기 기능을 활용해 변경사항을 보고, 다른 창으로는 변경 전의 학습활동을 봄으로써 둘을 비교해보면 유용할 것이다.

.. _학습활동 게시하기:

****************************
학습활동 게시하기
****************************

학습활동을 게시하는 것은, 주제와 소주제의 공개일이 지나면 Studio에 있는 현재 버전을 학습자가 볼 수 있게 한다는 의미다.

게시할 대상은 `초안 (게시된 적 없음)`_ 또는 `학습활동이 변경됨`_ 상태의 학습활동이다. 이러한 상태의 학습활동을 게시하면 `공개됨`_ 또는 `아직 공개되지 않음`_  상태가 된다.

학습활동 페이지나 강좌 개요에서 학습활동을 게시할 수 있다.

=======================================
학습활동 페이지에서 게시하기
=======================================

학습활동을 게시하려면, 화면 왼쪽에서 **게시** 버튼을 클릭한다.

.. image:: ../../../shared/building_and_running_chapters/Images/unit-publish-button.png
 :alt: Unit status panel with Publish button circled

=======================================
강좌 개요에서 학습활동 게시하기
=======================================

강좌개요에서 학습활동을 게시하려면, 학습활동 영역에서 게시 아이콘을 클릭한다.

.. image:: ../../../shared/building_and_running_chapters/Images/outline-publish-icon-unit.png
 :alt: Publishing icon for a unit

.. 참고:: 
게시 아이콘은 새로 추가되거나 변경된 콘텐츠가 있을 때에만 나타난다. 

.. _학습활동 변경 취소하기:

****************************
학습활동 변경 취소하기
****************************

게시된 학습활동을 변경하면 변경사항이 Studio에 저장된다. 그러나 게시하지 않는 한, 학습자가 이를 볼 수는 없다.

그런데, 이러한 변경을 취소해서 Studio에 가장 최근에 게시된 학습활동이 나오도록 할 수 있다. 

이를 원한다면, **변경 취소하기** 를 클릭하면 된다.

.. image:: ../../../shared/building_and_running_chapters/Images/unit-discard-changes.png
 :alt: Unit status panel with Discard Changes circled

.. 주의::
학습활동 변경을 취소하면, 변경사항이 영구적으로 삭제된다. 삭제된 변경사항을 되돌릴 수 없음에 주의한다.

.. _게시된 학습활동 보기 :

****************************
게시된 학습활동 보기 
****************************

가장 최근에 학습 관리 시스템에 게시된 학습활동을 보려면, 
**적용 결과 보기** 를 클릭한다.

.. image:: ../../../shared/building_and_running_chapters/Images/unit_view_live_button.png
 :alt: Unit page with View Published Version button circled

그러면 학습 관리 시스템에서 학습활동을 볼 수 있다. 이를 위해 학습 관리 시스템에서 다시 로그인해야 할 수 있다.

`학습활동이 변경됨`_ 상태의 학습활동은 게시해야만 학습 관리 시스템에서 볼 수 있다.

학습활동의 상태가 `초안 (게시된 적 없음)`_ 인 경우,  **적용 결과 보기** 버튼이 활성화되지 않는다.

.. _학습활동 감추기:

****************************
학습활동 감추기
****************************

주제와 소주제의 공개일과 학습활동의 공개 상태와 관계 없이, 소주제 내부의 전체 콘텐츠를 감출 수 있다.

:ref:`Controlling Content Visibility` 에 더 자세한 안내가 있다.

강좌 개요나 학습활동 페이지에서 학습활동을 감출 수 있다. 

=======================================
학습활동 페이지에서 학습활동을 감추기
=======================================

**학습자에게 감추기** 의 체크박스를 클릭한다.

.. image:: ../../../shared/building_and_running_chapters/Images/unit-hide.png
 :alt: Unit status panel with Hide from Students checked

:ref:`Controlling Content Visibility` 에 더 자세한 안내가 있다.

=======================================
강좌개요 페이지에서 학습활동을 감추기
=======================================

#. 학습활동 영역에서 설정 아이콘을 클릭한다.
   
   .. image:: ../../../shared/building_and_running_chapters/Images/outline-unit-settings.png
    :alt: The unit settings icon circled

   The **Settings** dialog box opens.

#. **학습자에게 감추기** 의 체크박스를 클릭한다.

   .. image:: ../../../shared/building_and_running_chapters/Images/outline-unit-settings-dialog.png
    :alt: The unit hide from students setting

#. **저장** 을 클릭한다.

=======================================
감추었던 학습활동 공개하기
=======================================

감췄던 학습활동을 학습자에게 공개하기 전에, 다음 사항을 주의해야 한다.

* 이전에 게시 상태였던 학습활동은, 체크박스를 해제하면 바로 콘텐츠가 학습자에게 공개된다.
감춰진 동안 학습활동에 변경사항이 있다면, 변경된 학습활동이 게시된다.
 
* 이전에 감췄던 주제나 소주제를 학습자에게 공개한다해서, 게시한 적이 없는 학습활동까지 *게시되는 것은 아니다.* 
게시중이었던 학습활동이라면, 마지막으로 게시했던 학습활동이 공개된다. 

감추었던 학습활동을 공개하려면, 학습활동 영역에서 설정 아이콘을 클릭한 후, **학습자에게 감추기** 의 체크박스를 해제한다.

그러면 공개 여부를 다시 확인하는 대화상자가 뜰 것이다.

.. _학습활동 삭제하기:

********************************
학습활동 삭제하기
********************************

강좌개요에서 학습활동을 삭제할 수 있다.

학습활동을 삭제하면, 학습활동에 포함된 모든 구성요소들이 삭제된다는 것에 유의해야 한다.

.. 주의::  
 삭제 후에는 콘텐츠를 복구할 수 없다. 나중에 필요할 수도 있다고 생각되는 콘텐츠는 삭제하지 말고, 
 비공개 주제에 옮겨두는 것을 권장한다. 

학습활동을 삭제하려면:

#. 삭제하고 싶은 학습활동 영역에서 삭제 아이콘을 클릭한다.

.. image:: ../../../shared/building_and_running_chapters/Images/section-delete.png
 :alt: The section with Delete icon circled

2. 삭제를 확인하는 대화상자가 뜨면, **네, 학습활동을 삭제합니다.** 를 클릭한다.
