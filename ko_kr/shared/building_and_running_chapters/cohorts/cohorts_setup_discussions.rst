
.. _Set up Discussions in Cohorted Courses:


######################################################
학습집단별 게시판 설정하기
######################################################

학습 집단 기능이 활성화된 강좌에서, 학습 집단에 따라 토의 주제를 나누거나 모든 학습자가 같은 토의 주제를 다룰 수 있도록 설정할 수 있다.

최초로 학습 집단을 활성화했을 때, 일반 주제를 위한 활동과 주제별 토의 주제의 활동은 차이가 있다.

시스템은 기본적으로, 일반 주제는 학습자 모두에게 통합적으로 제시하고, 주제별 토의 주제는 학습 집단별로 나누어 제시한다. 토의 유형을 나누거나 통합하도록 설정할 수 있다. 

강좌에서 토의에 관한 개괄적 정보는 :ref:`Discussions` 에서 볼 수 있다.강좌에 학습집단 사용에 관한 정보는 :ref:`Cohorts Overview` 와 :ref:`Enabling and Configuring Cohorts` 에서 볼 수 있다. 

***********************************************
일반 토의 주제와 학습 집단
***********************************************

최초로 :ref:`일반 토의 주제를 생성<Create CourseWide Discussion Topics>` 했을 때, 토의 주제는 모든 학습자에게 통합적으로 제시되고, 강좌의 모든 학습자는 속한 학습 집단에 상관 없이 이 주제에 대하여 게시글을 쓰고, 읽고, 응답하고, 코멘트를 남길 수 있다. 일반 토의 주제를 추가한 후, 토의 주제가 학습 집단에 따라 분류되도록 환경 설정을 할 수 있다.

.. _Identifying Private CourseWide Discussion Topics:

=============================================================
예시: 학습 집단별 일반 주제 게시판 설정
=============================================================

이 예시에서는 사전에 추가했던 강좌 Q&A, 공지사항, 브레인스토밍의 세 가지 주제에 시스템에서 제공하는 주제까지, 총 네 개의 일반 주제를 가지고 있다고 가정한다.

.. image:: ../../../shared/building_and_running_chapters/Images/Discussion_Add_cohort_topics.png
 :alt: Discussion Topic Mapping field with four course-wide discussion topics 
       defined

브레인스토밍과 공지사항을 학습 집단별로 진행할 수 있도록 해당 주제에 학습 집단을 설정할 수 있다.

또한, 학습자가 해당 주제에 게시물을 추가하기 전에, 확인할 수 있는 사람이 누구인지 알 수 있도록 설정할 수 있다. 이러한 기능을 사용하기 위해서는 :ref:`Apply Naming Conventions to Discussion Topics` 를 참고하면 된다. 


.. _Configure CourseWide Discussion Topics as Private:

======================================================
학습 집단별 일반 주제 게시판 설정
======================================================

이 절차는 학습 집단별로 나뉘어진 브레인스토밍과 공지사항에 대한 일반 주제(예시: :ref:`Identifying Private
CourseWide Discussion Topics` 의 예시임)의 환경 설정에 관하여 기술하고 있다.

스튜디오의 **고급 설정** 페이지의 **게시물 주제 맵핑하기** 필드에서 두 개 주제의 세부 사항은 다음과 같다. 

.. code::

      "Brainstorming (private)": {
          "id": "i4x-edX-Open-edx_demo_course_brainstorming"
      },
      "Announcements (private)": {
          "id": "i4x-edX-Open-edx_demo_course_announcements"
      }

다음 단계에서 각 토의 주제를 구분하기 위해서 ID를 사용한다.

#. 스튜디오를 실행한다. 

#. **설정** 을 선택한 후 **고급 설정** 을 선택한다.

#. **학습집단 설정" 필드에서, 열린 중괄호 문자(``{``) 다음에 커서를 
   위치시킨 후 **엔터**를 누른다.

#. 새로운 행에서, ``"cohorted_discussions":`` 를 정의한 후, 하나 이상의 
   일반 주제 ID를 닫힌 대괄호 (``[ ]``) 안에 입력한다. 하나의 토의 주제를 
   정의할 수도 있고, 여러 개의 토의 주제를 정의할 수도 있다.  
 
   예를 들어 단일 토의 주제를 정의하고자 한다면, ``"cohorted_discussions": ["discussion-topic-ID"]`` 
   라고 입력하고 토의 주제 ID를 큰 따옴표 안의 ID 예시 자리에 입력하고 엔터를 누른다.  

   여러 개의 토의 주제를 정의하고자 한다면, 각각의 토의 주제 ID를 
   새로운 행에서 닫힌 큰 따옴 (``" "``) 안에 입력하고, 닫힌 큰 따옴표의 ID 값은 쉼표로 구분한다. 예:
 
 .. code:: 

   "cohorted_discussions": [
       "i4x-edX-Open-edx_demo_course_announcements",
       "i4x-edX-Open-edx_demo_course_brainstorming"
   ]
   
5. 만일 **학습집단 설정** 필드에서 ``"cohorted_discussions"`` 값이 다른 policy keys에 
   뒤따른다면, 닫힌 중괄호 문자 다음에 쉼표 (``],``) 를 입력해야 한다. 정의한 policy keys를 
   구분하기 위해서 반드시 쉼표를 입력해야 한다.

.. Adding a line to force a line space

6. **변경 사항 저장** 을 클릭하면 스튜디오는 입력한 사항에 따라 재설정된다. 

 .. image:: ../../../shared/building_and_running_chapters/Images/Configure_cohort_topic.png
  :alt: Cohort Configuration dictionary field with the cohorted_discussions key
        defined

7. 기대한 것처럼 입력 내용이 저장되었는지 확인하기 위해서 다시 **학습집단 설정** 으로 이동한다.   
   저장할 때 필요한 구분 문자들이 전부 포함되지 않은 경우에는 입력 이전으로 돌아가고, 경고창은 뜨지 않는다.


********************************************************
주제별 토의와 학습집단
********************************************************

강좌에서 학습 집단 기능을 활성화하고, 스튜디오의 토의 구성 요소를 학습 활동에 추가하여 :ref:`주제별 토의를 생성<Create ContentSpecific Discussion Topics>` 할 때, 주제별 토의는 학습집단 기본 값으로 나뉘어진다. 하나의 학습집단에 배치된 학습자는 다른 학습집단 회원의 온라인 학습 활동들을 읽어보거나 게시글, 응답, 코멘트를 추가할 수 없다. 

모든 주제별 토의를 학습집단으로 나누고자 한다면, 어떤 설정도 할 필요가 없다. 그러나 하나 이상의 주제별 토의를 학습집단에 상관 없이 모든 학습자에게 통합적으로 제시하고자 한다면, 몇가지 환경 설정을 해야 한다.


=====================================================================
예시: 모든 학습자에게 통합적으로 제시되는 주제별 게시판 설정
=====================================================================

강좌에 추가한 모든 주제별 토의가 학습집단이 아닌 모든 학습자에게 통합적으로 제시되기를 원한다면, 
:ref:`Make ContentSpecific Discussion Topics Unified`의 단계를 따라야 한다.

후에, 강좌의 가장 마지막 영역을 설계할 때, 모든 학습자에게 통합적으로 제시되는 다른 토의 구성요소보다는 학습집단별로 나뉘어진 주제별 토의를 추가하고자 한다면, :ref:`Specify Cohorted Discussions as Exceptions` 의 단계를 따라야 한다. 


.. _Make ContentSpecific Discussion Topics Unified:

================================================================
모든 주제별 토의를 모든 학습자에게 통합적으로 제시하기
================================================================

.. note:: 강좌의 모든 주제별 토의가 학습집단으로 나뉘어지기를 원한다면, 어떠한 설정도 할 필요가 없다.

여기서 절차는 모든 주제별 토의를 강좌의 모든 학습자에게 통합적으로 보여주고 있다. 이 절차를 완료하면, 강좌에 추가된 모든 주제별 토의는 학습자가 속한 학습집단에 관계없이 모든 학습자가 접근할 수 있게 된다.  

#. 스튜디오에서 강좌를  연다. 

#. **설정** 을 선택한 후, **고급 설정** 을 클릭한다.

#. **학습집단 설정** 필드에서, 여는 중괄호(``{``) 문자와 기존의 policy key 정의 뒤에 커서를 위치한 후, **엔터** 를 누른다.

#. 다시 **엔터** 를 눌러서 새로운 행을 만들고, 새로운 행에 다음과 같이 입력한다. 
   
    ``"always_cohort_inline_discussions": false``
   

5. **변경사항 저장** 을 클릭하면, 스튜디오는 입력한 사항에 따라 재설정된다.
 
 .. image:: ../../../shared/building_and_running_chapters/Images/cohort_config_always_inline.png
  :alt: Cohort Configuration dictionary field with the cohort key set as true and the always cohort inline discussions key set as false

6. 원한대로  입력 내용이 저장되었는지 확인하기 위해서 다시  **학습집단 설정 ** 으로 이동한다.  
   저장할 때 필요한 구분 문자들이 전부 포함되지 않은 경우에는 입력 이전으로 돌아가고, 경고창은 뜨지 않는다.


.. _Specify Cohorted Discussions as Exceptions:

================================================================
통합 토의 주제에 대한 예외 지정하기
================================================================

모든 주제별 토의를 통합적으로 제시하는 것으로 만들었다면, 여기서는 예외 및 특정 주제별 토의를 학습집단별로 설정하는 방법에 대한 것이다.

#. 스튜디오에서 강좌를 실행한다. 
   
#. 스튜디오의 토의 구성요소에서 학습 집단 별로 나누고 싶은 주제별 토의의 **토의 ID** 를 복사하거나 기록한다.
   
.. image:: ../../../shared/building_and_running_chapters/Images/DiscussionID.png

3. **설정** 을 선택한 후, **고급 설정** 을 클릭한다.

#. **학습집단 설정** 필드에서, ``cohorted_discussions`` 가 없으면,  ``"cohorted_discussions":`` 와  중괄호 (``[ ]``) 를 입력한다. 

#. 중괄호 (``[ ]``) 사이에 지정하고자 하는 토의 주제의 ID를 하나 이상 추가한다. 

   학습집단별로 나누어지도록 지정하는 토의 주제가 하나일 경우, 다음과 같이 입력하면 된다.

   .. code::

      "cohorted_discussions": [c2293fa2538a41eca7224b8a07c3d09d] 


   학습집단별로 나누어지도록 지정하는 토의 주제가 다수인 경우, 다음과 같이 추가하고자 하는 주제 ID는 새로운 행으로 구분해야 하고, 각 주제 ID는 큰따옴표 (``"``) 안에 들어가며, 추가되는 주제 ID 다음에는 쉼표를 입력해야 한다. 
 
 .. code::  

    "cohorted_discussions": [

       "c2293fa2538a41eca7224b8a07c3d09d",
       "a9823gt3187i38itp2893a8d27f8f20c"
    ]


6. 만일 **학습집단 설정** 필드에서 ``"cohorted_discussions"`` 값이 다른 policy keys에 뒤따른다면, 닫힌 중괄호 문자 다음에 쉼표 (``],``) 를 입력해야 한다. 정의한 policy keys를 구분하기 위해서 반드시 쉼표를 입력해야 한다.    

 .. image:: ../../../shared/building_and_running_chapters/Images/cohort_config_cohorted_discussions.png
  :alt: Cohort Configuration dictionary field with the cohort key set as true, the always cohort inline discussions key set as false, and two discussion topics IDs entered under the cohorted discussions policy key


7. **변경사항 저장** 을 클릭하면, 스튜디오는 입력한 사항에 따라 재설정된다.
   
.. Adding a line to force a line space

8. 원하는 입력 내용이 저장되었는지 확인하기 위해서 다시 **학습집단 설정** 으로 이동한다. 저장할 때 필요한 구분 문자들이 전부 포함되지 않은 경우에는 입력 이전으로 돌아가고, 경고창은 뜨지 않는다. 
   
