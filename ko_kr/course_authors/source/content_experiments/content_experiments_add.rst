.. _Add Content Experiments to Your Course:

#########################################
콘텐츠 실험 추가하기
#########################################

:ref:`콘텐츠 실험을 설정과<Enable Content Experiments>` :ref:`스튜디오에서 실험 집단을 설정 <Set up Group Configurations in edX Studio>`하고, 강좌에 콘텐츠 실험들을 추가할 수 있다.

* :ref:`Add a Content Experiment in Studio`
* :ref:`Add a Content Experiment in OLX`

.. _Add a Content Experiment in Studio:

********************************************
스튜디오에서 콘텐츠 실험 추가하기
********************************************

학습활동이나 container 페이지에 콘텐츠 실험을 추가할 수 있다. 에 제시된 바와 같이, 컨테이너 페이지의 콘텐츠 실험 안에서 모든 그룹의 콘텐츠를 생성`콘텐츠 실험에 학습집단별 콘텐츠 만들기`_하고 확인한다.  

학습자가 콘텐츠 실험을 학습활동에서 보았을 때, 콘텐츠 실험에 참여하고 있다는 안내나 실험명이 나타나지 않는다. 학습자는 자신이 속한 학습집단에 설정된 콘텐츠만을 볼 수 있다. 학습자에게 콘텐츠 실험가 있는 학습활동은 다른 학습활동과 차이가 없다.

스튜디오에서 콘텐츠 실험을 설정하려면:

#. `콘텐츠 실험 만들기`_.
#. `콘텐츠 실험에 학습집단별 콘텐츠 만들기`_.
   
콘텐츠 실험을 설정한 후에 집단 설정을 변경할 수 있다. `콘텐츠 실험에서 집단 설정 변경하기`_ 에서 확인한다.

===============================
콘텐츠 실험 만들기
===============================

#. 학습활동 구성 페이지에서, **새로운 요소 추가** 아래에 있는 **고급** 을 선택한다.

#. **콘텐츠 실험** 을 선택한다.
   
   새로운 콘텐츠 실험을 학습활동에 추가한다:

   .. image:: ../../../shared/building_and_running_chapters/Images/content_experiment_block.png
    :width: 800
    :alt: The content experiment component in a unit page

  다른 요소처럼 콘텐츠 실험 작업을 하면된다. 더 많은 정보가 필요하면 :ref:`Developing Course Components` 를 확인한다. 

#. 콘텐츠 실험 구성요소를 열기 위해 **집단 설정 선택하기** 혹은 **수정** 을 클릭한다. 

   .. image:: ../../../shared/building_and_running_chapters/Images/content_experiment_editor.png
    :alt: The content experiment editor

#. **집단설정" 다음에 그룹설정을 선택한다. 

#. **사용 가능한 이름(Display Name)** 영역 안에 사용할 이름을 등록한다. 등록된 이름은 스튜디오에서만 사용하고 학습자는 입력값을 보지 못한다. 
   
#. **저장**을 클릭한다.

콘텐츠 실험은 다른 요소들과 같이 제시되었다. 더 많은 정보가 필요하면 :ref:`Components that Contain Other Components`에서 확인한다.

.. note::  콘텐츠 실험은 복사할 수 없다.

이제 콘텐츠 실험에서 집단별 콘텐츠를 만들 수 있다. 

=====================================================
콘텐츠 실험에 학습집단별 콘텐츠 만들기
=====================================================
   
콘텐츠 실험 구성요소에서 집단 설정을 선택한 후, **보기**를 클릭한다.

자동 생성된 콘텐츠 실험은 선택한 집단 설정에서 정의된 각 집단이 포함된 컨테이너가 나타난다. 예를 들어, 집단 A와 집단 B로 정의한 집단 설정을 선택하면 다음의 페이지가 나타난다:
:

.. image:: ../../../shared/building_and_running_chapters/Images/content_experiment_container.png
 :alt: The content experiment page with two groups

두 집단을 위한 각각의 콘텐츠를 추가한다. 더 많은 정보를 보기위해 :ref:`Components that Contain Other Components` 를 살펴본다 
예를 들어, 집단 A에 HTML 요소와 동영상을 추가할 수 있다.:

.. image:: ../../../shared/building_and_running_chapters/Images/a_b_test_child_expanded.png
 :alt: Image of an expanded A/B test component

.. note:: 
  It is valid, and can be useful, to have no content for a group in the
  experiment.  For example, if one group has a video and another group has no
  content, you can analyze the effect of the video on student performance.


========================================================
콘텐츠 실험에서 집단 설정 변경하기
========================================================

You can change the group configuration for a content experiment. When you
change the group configuration, you must add components to any new groups that you create. You
can use the components from the previous groups, as well as create new
components.

.. warning::
  Changing the group configuration of a student-visible experiment will affect
  the experiment data.

To change the group configuration:

#. Open the unit page of the unit that contains the content experiment.

#. In the content experiment component, click **Edit**.

   .. image:: ../../../shared/building_and_running_chapters/Images/content_experiment_editor_group2.png
    :alt: The content experiment editor with a group configuration selected

#. Select a different group configuration.

#. Click **Save**.

#. You must now add components to the new groups in the experiment. Click
   **View** to open the content experiment.

   You see that groups for the new configuration are empty, and any components
   that you had added to groups in the previous configuration are now moved to
   a section called **Inactive Groups**.

   .. image:: ../../../shared/building_and_running_chapters/Images/inactive_groups.png
    :alt: Components in inactive groups

#. Drag and drop components from the **Inactive Groups** section into the new
   groups. You can also create new components in the new groups.

.. import OLX-content experiment doc that's shared in OLX guide.

.. include:: ../../../shared/subsections/content_experiments/content_experiments_OLX.rst
