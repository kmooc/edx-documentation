.. _Getting Started with Course Content Development:

###############################################
강좌 콘텐츠 
###############################################

:ref:`setting up your course<Setting up your Course Index>` 에서의 작업이 모두 끝났다면,
이제 강좌 콘텐츠를 개발할 차례다.

이 장은 강좌 콘텐츠 개발 단계의 개요를 다룬다. 아래 링크에 구체적인 안내가 있다.

* `Understanding Course Building Blocks`_
* `Creating New Course Content`_
* `Making Course Content Visible to Students`_
* `Revising Content`_

.. _Understanding Course Building Blocks:

************************************************
강좌의 기본 구성요소 이해하기
************************************************

시작하기 전에, K-MOOC 강좌를 이루는 기본 요소를 먼저 이해하면 도움이 될 것이다.

* :ref:`The course outline<Developing Your Course Outline>` 에서 강좌의 콘텐츠 구성 등 전체 그림을 한 눈에 볼 수 있다. 
* :ref:`Course sections<Developing Course Sections>` 는 강좌에서 가장 상위 범주에 해당한다. 순차적으로 공개되는 주제를 보면    개강일 이후 강좌가 진행되는 흐름을 알 수도 있고, 강좌가 어떻게 구성되어 있는지를 한 눈에 볼 수 있기도 하다. 각 주제는 1개    이상의 소주제를 가진다.
* :ref:`Course subsections<Developing Course Subsections>` 는 주제의 하위 개념으로, 주제에서 1개 이상의 학습활동이 포함된      소주제로 나뉘게 된다. 소주제를 살펴보면 강좌에서 무엇을 중점으로 두는지 이해할 수 있게 된다.
* :ref:`Course units <Developing Course Units>` 은 소주제의 일부로써, 학습자가 소주제를 클릭하면 한 번에 하나씩 볼 수 있다.
* :ref:`Course components<Developing Course Components>` 는 학습활동의 부분으로, 실제 강좌 콘텐츠라고 볼 수 있다. 1개의 학습활동은 1개 이상의 구성요소를 포함할 수 있다

.. _Creating New Course Content:

****************************************
신규 콘텐츠 만들기
****************************************

K-MOOC 강좌를 이루는 기본 요소를 이해했다면, 이제 강좌 콘텐츠를 Studio에서 개발할 수 있다.

먼저, :ref:`course
outline<Developing Your Course Outline>` 에서 :ref:`sections<Create a Section>`, :ref:`subsections<Create a
Subsection>`, :ref:`units<Create a Unit>` 가 이루어 져야 한다.

성적에 반영되는 소주제 설정도 할 수 있다.
:ref:`set the assignment type and due date<Set the Assignment Type and Due Date
for a Subsection>` 에 그에 대한 안내가 나와있다.

:ref:`create components<Add a Component>` 를 참고해 구성요소도 추가할 수 있다.

이 외에도, :ref:`control content visibility<Controlling Content
Visibility>` 를 참고하면 학습활동 게시와 공개일 설정을 통해 콘텐츠를 학습자에게 보이거나 감추는 것을 설정할 수 있다. 

이러한 콘텐츠 제작 과정을 아래 도표와 같이 요약할 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/workflow-create-content.png
 :alt: Diagram of the content creation process

콘텐츠 개발 과정에서 콘텐츠를 테스트해보는 것이 원활한 강좌 운영에 도움이 될 것이다. 이에 대한 안내는 :ref:`test course content <Testing Your Course
Content>` 에 있다.

.. _Making Course Content Visible to Students:

******************************************************
콘텐츠 공개하기
******************************************************

콘텐츠를 만들 때, 이를 학습자에게 공개할 것인지 여부와 공개 시점을 설정할 수있다. 
아래 항목들에 관해 공개 설정이 가능하다.

* :ref:`course start date<The Course Start Date>`
* :ref:`section<Set a Section Release Date>` and
  :ref:`subsection<Set a Subsection Release Date>`
* :ref:`publishing status<Hide a Unit from Students>` of the unit
* :ref:`Hide content from students<Hide a Unit from Students>` setting
* :ref:`Content Groups`
  
공개 설정에 대한 자세한 안내는 Content Visibility` 에 있다.

.. _Making Course Content Searchable:

***********************************
콘텐츠 검색 기능 활성화하기
***********************************

Learners can search course text in :ref:`HTML components<Working with HTML
Components>` and video transcripts by using the **Search** box in the upper-left
corner of the **Courseware** tab. 

Before learners can search your course, Studio must index the content. Studio
indexes all new course content automatically when you :ref:`publish<Publish a
Unit>` the content. 

If necessary, you can manually reindex all of the content in your course at any
time. Typically, you would only manually reindex your course content if learners
see unexpected search results. To reindex your course content, select **Reindex
Content** in the upper-right corner of the **Course Outline** page. Reindexing
usually takes less than 30 seconds.

.. _Revising Content:

****************************
Revising Content
****************************

You can revise your course content at any time. 

* When you :ref:`reorganize sections, subsections, and units<Reorganize the
  Course Outline>` in the outline, the new order is immediately visible to
  students if the section and subsection are released.

* When you :ref:`edit a unit<Edit a Unit>`, or :ref:`components<Add a
  Component>` within a unit, you must :ref:`publish<Publish a Unit>` those
  changes to make them visible to students.

The following diagram summarizes the content revision workflow and content
visibility:

.. image:: ../../../shared/building_and_running_chapters/Images/workflow-revise-content.png
 :alt: Diagram of the content creation process

It is recommended that you :ref:`test course content <Testing Your Course
Content>` during the revision process.
