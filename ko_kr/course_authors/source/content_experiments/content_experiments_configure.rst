.. _Configure Your Course for Content Experiments:

#####################################################
콘텐츠 실험을 위한 강좌 설정하기
#####################################################

본 장에서는 콘텐츠 실험을 이용하기 위한 강좌 설정을 살펴본다.:

* :ref:`Enable Content Experiments`
* :ref:`Overview of Group Configurations`
* :ref:`Set up Group Configurations in edX Studio`
* :ref:`Guidelines for Modifying Group Configurations`
* :ref:`Set Up Group Configuration for OLX Courses`

.. _Enable Content Experiments:

****************************************
콘텐츠 실험을 활성화하기
****************************************

강좌에서 콘텐츠 실험을 활성화하기 위해, ``split_test`` 를 고급설정에서 **고급 모듈 목록** 에 추가한다. 

.. note::  
``split_test`` 는 콘텐츠 실험의 내부 edX 플랫폼 이름이다.  

#. **환경** 메뉴에서 **고급환경** 을 선택한다.

#. **고급환경** 에서, **고급 모듈 목록** 을 찾는다.

#. **고급 모듈 목록** 칸에, ``"split_test"`` 를 추가한다. 큰따옴표가 포함되었는지 확인한다. 

   여러개의 값이 있다면, 쉼표로 분리한다 (``,``).

   예를 들어, **고급 모듈 목록** 칸에 입력되는 텍스트는 다음과 같을 것이다:

   .. code-block:: json
     
     [
       "lti",
       "word_cloud",
       "split_test"
     ]

#. 페이지 하단에 **다시 저장** 을 클릭한다.

.. _Overview of Group Configurations:

****************************************
집단 설정 개관
****************************************

콘텐츠 실험을 만들기 전에 강좌에서 최소한 1개의 집단을 설정해야 한다 .

집단 설정은 실험에 참여하는 집단의 수를 정한다. 콘텐츠 실험을 만들때, 이용하기 위한 집단 설정을 선택한다. 

예를 들어, 강좌에서 다른 시기에 다른 2개의 실험을 원한다고 하자. 콘텐츠 실험에서, 학습자는 동영상을 보거나 읽기 과제를 한다. 어떤 집단이 자료를 더 잘 학습하였는지 확인하기 위해 문제를 추가할 수 있다. 콘텐츠 실험에서, 2개의 실험 그룹에 학생들을 배정하기 위해 집단 설정한다. 

다른 콘텐츠 실험에서, 문제의 4개의 다른 유형을 이용하여 동일 질문을 보여 줄 수 있다. 이 콘텐츠 실험에서, 학습자들을 4개의 실험 집단에 배정하도록 집단을 설정한다. 

=======================================
실험 집단에 학습자 배정하기
=======================================

edX 플랫폼은 집단 설정에서 학습자를 각 실험 집단에 배정한다.  

실험 집단 배정은:

* 다이나믹하다

  edX 플랫폼은 학습자를 하나의 실험 집단에 우선 배정하면, 학습자는 집단 설정에 따른 콘텐츠 실험에 참여하게 된다. 

* 무작위이다
  
  학습자가 할당되는 실험집단은 조절할 수 없다.
  
* 고르게 분포된다.
  
  edX 플랫폼은 실험 집단들의 크기를 계속 점검하고, 새로운 학습자를 집단에 고르게 배정한다. 예를 들어, 2개의 실험 집단이 설정에 되어 있다면, 각 집단은 강좌에 등록한 50%의 학습자를 포함하게 된다; 4개의 실험 집단이 있다면, 각 집단은 학습자의 25%씩 배정된다. 

* 영구적이다.
  
  동일한 집단 설정이 적용되는 콘텐츠 실험의 수를 고려하지 않고 학습자는 배정된 실험 집단에 남아 있게 된다. 


.. _Set up Group Configurations in edX Studio:

************************************************
edX Studio에서 실험 집단 설정하기
************************************************

.. note:: 
  집단을 설정하기 전에 :ref:`enable content experiments<Enable Content Experiments>` 콘텐츠 실험을 활성화 해야 한다. 

집단 설정을 하기 위해, **설정** 메뉴에서, **집단 설정** 을 선택한다. **집단 설정** 페이지가 열린다. 

이 페이지에서 집단 설정을 :ref:`create<Create a Group Configuration>` 생성, :ref:`edit<Edit a Group Configuration>` 편집, :ref:`delete<Delete a Group Configuration>` 삭제가 가능하다. 또한 :ref:`집단 설정을 사용하는 실험들 보기<View Experiments that Use a Group Configuration>` 를 할 수 있다. .

.. _Create a Group Configuration:

=============================
실험 집단 설정 생성하기 
=============================

항상 집단 설정을 생성할 수 있다. 

#. **집단 설정** 페이지에서, **실험 집단** 을 선택하고, **새 실험 집단** 을 클릭한다. 다음 페이지가 나타난다:

  .. image:: ../../../shared/building_and_running_chapters/Images/create-group-config.png
   :width: 800
   :alt: Create a New Group Configuration page

2. Enter a name in the **Group Configuration Name** field. Use a meaningful
name, because you will select from group configuration names when you create
content experiments. Students do not see the group configuration name.

#. Optionally, enter a description for the new group configuration.
   
#. By default, a new configuration already contains two groups. Modify the
   groups or add and delete groups as needed. A group configuration must have at
   least one group.

  * Modify group names as needed. You see group names in the unit page in
    Studio, but group names are not visible to students.       
  * Click **Add another group** to include another group as part of
    the configuration. 
  * Click the **X** to the right of an existing group to remove it from the
    configuration. A group configuration must have at least one group.

5. Click **Create** to save the new group configuration.
   
The group configuration is then listed in the page. You can see the number of
groups that the configuration contains, as well as whether the configuration is
in use in the course:

.. image:: ../../../shared/building_and_running_chapters/Images/group_configurations_one_listed.png
 :width: 800
 :alt: The Group Configurations page with one group configuration


  
.. _Edit a Group Configuration:

=============================
Edit a Group Configuration
=============================

.. important:: You can change the name of a group configuration at any time.
   However, before you modify any other characteristics of a group configuration
   that is currently used in a running course, review `Guidelines for Modifying
   Group Configurations`_.

#. On the **Group Configurations** page, hover over the group configuration and
   click **Edit**.
   
   .. image:: ../../../shared/building_and_running_chapters/Images/group_configurations_edit.png
    :alt: The Group Configurations page with Edit button

   The following page opens:

   .. image:: ../../../shared/building_and_running_chapters/Images/save-group-config.png
    :alt: Edit a Group Configuration page

#. Modify the name and description as needed.

#. Modify groups in the configuration as needed. See `Create a Group
   Configuration`_ for details.
   
#. Click **Save** to save your changes.

.. _Delete a Group Configuration:

=============================
Delete a Group Configuration
=============================

.. note:: 
 You can only delete a group configuration that is not currently used in a
 content experiment. You cannot delete a group configuration that is used in a
 content experiment.

#. On the **Group Configurations** page, hover over the group configuration and
   click the Delete icon. 

  .. image:: ../../../shared/building_and_running_chapters/Images/group-configuration-delete.png
   :alt: Edit a Group Configuration page

2. When prompted to confirm the deletion, click **Delete**.


.. _View Experiments that Use a Group Configuration:

===============================================
View Experiments that Use a Group Configuration
===============================================

You can view the experiments that use each of your group configurations.

On the **Group Configurations** page, click the name of a group to see its
details. You see links to experiments that use the group configuration:

.. image:: ../../../shared/building_and_running_chapters/Images/group_configurations_experiments.png
 :alt: A group configuration with the experiments using it circled

Click a link to go to the unit page that contains the experiment.


===============================================
View a Group Configuration from an Experiment
===============================================

When working with a content experiment, you can view details about the group
configuration used by that experiment in two ways:

* In a unit that contains a content experiment, in the content experiment block,
  click the name of the group configuration.

.. image:: ../../../shared/building_and_running_chapters/Images/content_experiment_group_config_link.png
 :alt: Content experiment in the unit page with the group configuration link
     circled

* At the top of the content experiment page, click the name of the group
  configuration.

.. image:: ../../../shared/building_and_running_chapters/Images/content_experiment_page_group_config_link.png
 :alt: Content experiment page with the group configuration link circled

In both cases, the group configuration opens:

.. image:: ../../../shared/building_and_running_chapters/Images/group_configurations_experiments.png
 :alt: A Group Configuration with the experiments using it circled

You can use the link in the group configuration to return to the unit that
contains the content experiment.

.. import OLX-content experiment doc that's shared in OLX guide.

.. include:: ../../../shared/subsections/content_experiments/content_experiments_group_modify_guidelines.rst

.. include:: ../../../shared/subsections/content_experiments/content_experiments_policies.rst
