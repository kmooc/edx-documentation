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
   
콘텐츠 실험을 설정한 후에 집단 설정을 변경할 수 있다. `콘텐츠 실험에서 집단 설정 변경하기`_ 에서 확인한다..

===============================
콘텐츠 실험 만들기
===============================

#. 학습활동 구성화면에서, under **Add New Component**, click **Advanced**.

#. Select **Content Experiment**.
   
   A new content experiment is added to the unit:

   .. image:: ../../../shared/building_and_running_chapters/Images/content_experiment_block.png
    :width: 800
    :alt: The content experiment component in a unit page

   You can work with the content experiment as you can any other component.
   See :ref:`Developing Course Components` for more information.

#. Click either **Select a Group Configuration** or **Edit** to open the content
   experiment component.

   .. image:: ../../../shared/building_and_running_chapters/Images/content_experiment_editor.png
    :alt: The content experiment editor

#. Next to **Group Configuration**, select a group configuration.

#. In the **Display Name** field, enter the name that the component will use in Studio. The
   display name is only used in Studio; students do not see this value.

#. Click **Save**.

The content experiment is displayed as a component that contains other
components. See :ref:`Components that Contain Other Components` for more
information.

.. note::  You cannot duplicate a content experiment.

You can now create content for the groups in the experiment.

=====================================================
콘텐츠 실험에 학습집단별 콘텐츠 만들기
=====================================================
   
After you select a group configuration, in the content experiment component,
click **View**.

The content experiment page that opens automatically includes a container for
each group that is defined in the group configuration you selected. For
example, if you select a group configuration that defines Group A and Group B,
you see the following page:

.. image:: ../../../shared/building_and_running_chapters/Images/content_experiment_container.png
 :alt: The content experiment page with two groups

You add content for both groups as needed, just as you would add content to any
container page. See :ref:`Components that Contain Other Components` for more
information.

For example, you can add an HTML component and a video to Group A:

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
