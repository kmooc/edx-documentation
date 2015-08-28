
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

You have enabled cohorts for your course to take advantage of that feature
as it applies to discussion topics.

The posts that you intend to make to the Course Q&A and General topics, and the
subjects you expect students to explore there, are appropriate for a unified
student audience. However, you also want to give students some course-wide
topics that are divided by cohort. 브레인스토밍과 공지사항을 학습 집단별로 진행할 수 있도록 해당 주제에 학습 집단을 설정할 수 있다.

또한, 학습자가 해당 주제에 게시물을 추가하기 전에, 확인할 수 있는 사람이 누구인지 알 수 있도록 설정할 수 있다.이러한 기능을 사용하기 위해서는 :ref:`Apply Naming Conventions to Discussion Topics` 를 참고하면 된다. 


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
 
 #. 새로운 행에서, ``"cohorted_discussions":`` 를 정의한 후, 하나 이상의 일반 주제 ID를 닫힌 대괄호 (``[ ]``) 안에 입력한다. 하나의 토의 주제를 정의할 수도 있고, 여러 개의 토의 주제를 정의할 수도 있다.  

   For example, to define a single discussion topic, type
   ``"cohorted_discussions": ["discussion-topic-ID"]``, putting your discussion
   topic's ID inside the double quotations marks in place of the example ID.
   Press Enter.

   To define a set of topics, type the ID for each discussion topic on a new
   line, enclose it within quotation marks (``" "``), and separate the quoted ID
   values with commas. For example:

 .. code:: 

   "cohorted_discussions": [
       "i4x-edX-Open-edx_demo_course_announcements",
       "i4x-edX-Open-edx_demo_course_brainstorming"
   ]
   
5. If ``"cohorted_discussions"`` is followed by other policy keys within the
   **Cohort Configuration** field, make sure there is a comma after the closing
   square bracket character (``],``). You must include a comma to separate each of
   the policy keys that you define.

.. Adding a line to force a line space

6. Click **Save Changes**. Studio resequences and reformats your entry.

 .. image:: ../../../shared/building_and_running_chapters/Images/Configure_cohort_topic.png
  :alt: Cohort Configuration dictionary field with the cohorted_discussions key
        defined

7. Scroll back to the **Cohort Configuration** field to verify that your
   entry was saved as you expect. Entries that do not contain all of the
   required punctuation characters revert to the previous value when you save,
   and no warning is presented.


********************************************************
Content-Specific Discussion Topics and Cohort Groups
********************************************************

When you enable the cohort feature for a course, and :ref:`create content-
specific discussion topics<Create ContentSpecific Discussion Topics>` by adding
discussion components to units in Studio, these content-specific discussion
topics are divided by cohort by default. A student who is assigned to one
cohort cannot read or add to the posts, responses, or comments contributed
by the members of another cohort.

If you want all content-specific discussion topics in your course to remain
divided by cohort, you do not need to take any further action. However, if
you want one or more content-specific discussion topics to be unified
(accessible to all students regardless of cohort), you must complete some
configuration tasks.


=====================================================================
Example: Configuring Content-Specific Discussion Topics as Unified
=====================================================================

In this example, you decide that you want all content-specific discussion topics
you add to your course to be unified rather than divided by cohort. To
achieve this, you follow the steps to :ref:`Make ContentSpecific Discussion
Topics Unified`.

Later, while designing one of the final sections in the course, you add a
content-specific discussion topic that you decide should be divided by cohort,
rather than unified like all other discussion components. To achieve this, you
follow the steps to :ref:`Specify Cohorted Discussions as Exceptions`.


.. _Make ContentSpecific Discussion Topics Unified:

================================================================
Make All Content-Specific Discussion Topics Unified by Default
================================================================

.. note:: If you want all content-specific discussion topics in your course to
   be divided by cohort, you do not need to perform any configuration.

This procedure shows how to make all content-specific discussion topics in a
course unified by default. When you complete these steps, any content-specific
discussion topics that you add to your course are accessible to all students
regardless of their cohort.

#. Open your course in Studio. 

#. Select **Settings**, then **Advanced Settings**.

#. In the **Cohort Configuration** field, place your cursor after the opening
   brace character (``{``) and after any existing policy key definitions, then press **Enter**.

#. Press **Enter** to create a new line. On the new line, type
   
    ``"always_cohort_inline_discussions": false``
   

5. Click **Save Changes**. Studio resequences and reformats your entry. 
 
 .. image:: ../../../shared/building_and_running_chapters/Images/cohort_config_always_inline.png
  :alt: Cohort Configuration dictionary field with the cohort key set as true and the always cohort inline discussions key set as false

6. Scroll back to the **Cohort Configuration** field to verify that your entry
   was saved as you expect. Entries that do not contain all of the required
   punctuation characters revert to the previous value when you save, and no
   warning is presented.


.. _Specify Cohorted Discussions as Exceptions:

================================================================
Specify Exceptions to Unified Discussion Topics
================================================================

If you have made all content-specific discussion topics in your course unified
by default, this procedure describes how you can specify exceptions and
configure particular content-specific discussion topics in your course as
divided by cohort.

#. Open your course in Studio. 
   
#. For each content-specific discussion topic that you want to make divided by
   cohort, locate the discussion component in Studio, then copy or make a
   note of its **Discussion ID**.

.. image:: ../../../shared/building_and_running_chapters/Images/DiscussionID.png

3. Select **Settings**, then **Advanced Settings**.

#. In the **Cohort Configuration** field, if the ``cohorted_discussions`` policy
   key does not already exist, type ``"cohorted_discussions":``, followed by a pair
   of square brackets (``[ ]``).

#. Between these opening and closing square brackets (``[ ]``) add one or more IDs
   for the discussion topics that you want to specify as being unified. 

   If you are specifying only one discussion topic as divided by cohort,
   your entry looks like this example.

   .. code::

      "cohorted_discussions": [c2293fa2538a41eca7224b8a07c3d09d] 


   If you are specifying multiple discussion topics as divided by cohort,
   use a new line for each discussion topic ID that you add, and enclose each ID
   within double quotation marks (``"``), followed by a comma if there are
   additional IDs following.
 
 .. code::  

    "cohorted_discussions": [

       "c2293fa2538a41eca7224b8a07c3d09d",
       "a9823gt3187i38itp2893a8d27f8f20c"
    ]


6. If ``"cohorted_discussions"`` is followed by other policy keys within the
   **Cohort Configuration** field, make sure there is a comma after the closing
   square bracket character (``],``). You must include a comma to separate each
   policy key that you define.

 .. image:: ../../../shared/building_and_running_chapters/Images/cohort_config_cohorted_discussions.png
  :alt: Cohort Configuration dictionary field with the cohort key set as true, the always cohort inline discussions key set as false, and two discussion topics IDs entered under the cohorted discussions policy key


7. Click **Save Changes**. Studio resequences and reformats your entry.
   
.. Adding a line to force a line space

8. Scroll back to the **Cohort Configuration** field to verify that your entry
   was saved as you expect. Entries that do not contain all of the required
   punctuation characters revert to the previous value when you save, and no
   warning is presented.
   
