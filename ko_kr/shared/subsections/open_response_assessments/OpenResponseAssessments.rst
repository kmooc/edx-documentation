.. _Open Response Assessments 2:

#########################
개방형 평가
#########################

*****************************************
개방형 평가 소개
*****************************************

개방형 평가에서 교수자는 절대적인 정답이 존재하지 않을 수도 있는 질문지를 과제로 제시한다. 학습자는 문제에 대한 답변을 제출하며 이후 해당 학습자와 동료 학습자는 자신들의 답변과 강좌 운영팀이 작성한 채점 기준표(rubric)를 비교한다. 학습자는 텍스트 형식의 답변을 제출하는 것이 통상적이나 해당 텍스트에 이미지를 첨부하여 업로드할 수도 있다.

개방형 평가는 상호 평가와 자기 평가로 구성된다. 상호 평가에서 학습자는 강좌 운영팀이 생성한 채점 기준표와 동료의 답변을 비교한다. 자기 평가에서 학습자는 자신의 답변을 채점 기준표와 비교한다.

개방형 평가에서는 일반적으로, 학습자는 자신의 답변만을 볼 수 있으며 동료의 답변을 평가하는 경우 해당 동료의 답변까지만을 볼 수 있다. 동료가 제출한 답변 가운데 최고점을 받은 답변을 보도록 허용할 수도 있다. Top Responses에서 보다 구체적인 정보를 확인할 수 있다.

단계별 교수 방법 등, 개방형 평가 생성에 관한 보다 자세한 정보가 필요할 경우 다음을 살펴보길 바란다.

* :ref:`PA Elements`
* :ref:`PA Scoring`
* :ref:`PA Create an ORA Assignment`
* :ref:`Accessing ORA Assignment Information`

개방형 평가를 통한 학습자 경험에 관한 보다 구체적인 정보는 `edX Guide for Students <http://edx-guide-for-students.readthedocs.org/en/latest/index.html>`_ 의 `Open Response Assessments <http://edx-guide-for-students.readthedocs.org/en/latest/SFD_ORA.html>`_ 을 참조한다.

.. _PA Elements:

==========================================
개방형 평가의 요소
==========================================

개방형 평가 과제를 생성하는 경우 다음과 같은 요소를 포함하게 된다.

* 프롬프트, 즉 질문지
* 채점 기준표
* 1가지 이상의 평가 단계. 과제에는 학습자 연습 단계, 상호 평가 단계, 자기 평가 단계가 포함될 수 있다.

.. 참고:: 학습자 연습 단계를 포함할 경우 상호 평가 단계를 또한 반드시 포함해야 한다. 이 때, 학습자 연습 단계가 반드시 선행돼야 한다.

개방형 평가를 생성하기 위한 단계별 교수 방법에 관해서 더 자세한 정보는 :ref:`PA Create an ORA Assignment` 에 있다.

************************
프롬프트
************************

**프롬프트** , 즉 학습자가 답변을 제시해야 할 질문지는 해당 페이지 상단 부근에 위치하며 그 바로 밑에는 학습자가 답변을 입력하는 필드가 있다. 텍스트 형식의 답변을 입력하도록 요구할 수 있으며 텍스트 답변과 이미지를 동시에 업로드 하도록 허용할 수도 있다.

.. image:: ../../../../shared/building_and_running_chapters/Images/PA_QandRField.png
   :width: 500
   :alt: ORA question and blank response field

.. 참고:: 학습자가 이미지를 업로드하는 경우 해당 이미지 파일은 반드시 .jpg나 .png 포맷이어야 하며 또한 반드시 5 MB 미만이어야 한다.

질문지를 작성할 때, 학습자가 답변을 제출한 후의 절차 및 개략적인 답변문 단어 또는 문장 수 등, 학습자에게 도움이 되는 정보를 함께 제시할 수 있다. (1개 답변문은 10,000 단어를 초과할 수 없다.)
보다 자세한 정보는 Step 2. Add the Prompt을 참조한다.

For more information, see :ref:`PA Add Prompt`.

==========================================
이미지 업로드 요청하기
==========================================

답변에 이미지를 첨부할 것을 요청할 수 있다. 이 경우 다음에 주의한다.

* 현재로서는 이미지 업로드를 강제할 수는 없다. 이미지 첨부를 허용할 수 있을 뿐이다.

* 모든 답변에는 일부라도 텍스트가 있어야 한다. 이미지만을 답변으로 제출할 수는 없다.

* 학습자는 자신의 답변에 오직 1개의 이미지만을 첨부하여 제출할 수 있다.

.. 참고:: 현재, 강좌 운영진은 학습자가 이미지를 제출하더라도 이를 볼 수 없다. 이미지는 강좌 내용 내부의 과제 본문에서는 보이지 않으며 강좌 데이터 패키지에 포함되지도 않다.

.. _PA Rubric:

************************
채점 기준표
************************

과제에는 채점 기준표가 반드시 포함되어야 한다. 상호 평가 및 자기 평가 모두에 동일한 채점 기준표를 사용하며 이러한 채점 기준표는 학습자가 채점을 시작할 때 표시된다. 학습자는 동료의 답변과 이 채점 기준표를 비교한다

채점 기준표는 *평가 항목* 과 *평가 등급* 으로 구성된다.

* 각 평가 항목은 *제목* , *프롬프트* , 그리고 1개 이상의 *선택 조건* 으로 구성된다.

   * 제목(name)은 해당 평가 항목을 대단히 짧게, 즉 “Ideas”, “Content” 등으로 요약한 것을 말한다. 평가 항목 제목은 한 단어로 구성하는 구성하는 것이 일반적이다. 평가 시스템은 이들 평가 항목 제목을 식별자로 사용한다. 따라서 **반드시 평가 항목별로 고유한 제목** 을 붙여야 한다. 학습자가 상호 평가를 수행하는 중 확인하는 채점 기준표에는 평가 항목 제목이 표시되지 않다. 그러나 학습자 최종 점수가 표시되는 페이지에는 평가 항목 제목이 표시된다.

     .. image:: ../../../../shared/building_and_running_chapters/Images/PA_CriterionName.png
        :alt: A final score page with call-outs for the criterion names

   * 프롬프트는 이들 평가 항목에 대한 설명이다

   * 평가 등급은 해당 답변이 이들 평가 항목에 얼마나 잘 부합하는지를 나타낸다.

* 각 평가 등급은 *제목* , *설명* , *포인트* 로 구성된다.

  .. image:: ../../../../shared/building_and_running_chapters/Images/PA_Rubric_LMS.png
     :alt: Image of a rubric in the LMS with call-outs for the criterion prompt and option names, explanations, and points

하나의 과제에 서로 다른 다수의 평가 항목이 있는 경우 각 평가 항목의 평가 등급 가짓수는 서로 다를 수 있다. 가령, 위의 그림에서 첫 번째 평가 항목에는 세 가지 평가 등급, 두 번째 평가 항목에는 네 가지 평가 등급이 있다.

.. 참고:: 평가 등급이 없는 평가 항목을 포함할 수 있다. 그러나 이 경우에도 학습자가 피드백을 입력할 수 있는 필드가 있어야 한다. 보다 구체적인 정보는 :ref:`PA Criteria Comment Field Only` 에서 확인한다.

여러분은 개별 학습자의 과제 정보에 접근하여 평가 등급 및 평가 항목 모두를 볼 수 있다. 보다 구체적인 정보는 :ref:`Accessing ORA Assignment Information` 을 참조한다.

.. image:: ../../../../shared/building_and_running_chapters/Images/PA_Crit_Option_Names.png
   :width: 600
   :alt: Student-specific assignment information with call-outs for criterion and option names

채점 기준표를 작성할 때 각 평가 등급에 몇 포인트를 부여할지 결정하고 각 평가 등급에 대한 설명은 가능한 한 구체적으로 한다. 평가 항목 1개와 다수의 평가 등급을 구성한 경우를 아래에 예시한다.

**평가 항목**

제목: Origins

프롬프트: 이 답변은 100년 전쟁의 원인을 설명하고 있는가? (최대 5포인트)

**Options**

.. list-table::
   :widths: 8 20 50
   :stub-columns: 1
   :header-rows: 1

   * - 포인트
     - 제목
     - 설명
   * - 0
     - 전혀 그렇지 않음
     - 이 답변은 백년 전쟁의 원인을 논의하지 않았음.
   * - 1
     - 왕위 계승권 다툼
     - 이 답변은 잉글랜드와 프랑스 간의 왕위 계승권 다툼을 암시하고 있으나 잉글랜드의 에드워드 3세와 프랑스의 필립 6세를 언급하지 않았음.
   * - 3
     - 에드워드와 필립
     - 이 답변은 에드워드 3세와 필립 6세 간의 왕위 계승권 다툼을 다뤘으나 살릭 법의 역할을 논의하지 않았음.
   * - 5
     - 살릭 법
     - 이 답변은 살릭 법이 에드워드 3세와 필립 6세의 왕위 계승권 다툼에 어떤 식으로 관여하여 백년 전쟁을 촉발했는지 설명했음.

채점 기준을 효과적으로 작성하는 방법에 관해서는 `Understanding Rubrics <http://learnweb.harvard.edu/alps/thinking/docs/rubricar.htm>`_ 을 참조한다.

:ref:`PA Add Rubric` 에서 이와 관련한 보다 구체적인 정보를 확인할 수 있다.

************************
평가 단계
************************

과제에서 **평가 단계** 를 지정할 수 있다. 이 때, 학습자 연습 단계, 상호 평가 단계 및 자기 평가 단계를 포함하도록 과제를 구성할 수 있다.

과제를 검토할 때 평가의 유형과 순서를 확인할 수 있다. 아래는 학습자가 답변을 제출한 이후의 상황에 대한 예시이다. 학습자는 순서대로 학습자 연습 단계(“답변 평가 방법 학습하기(Learn to Assess Responses)”), 다른 학습자의 답변에 대한 상호 평가 단계(“상호 평가하기(Assess Peers)”), 자기 평가 단계(“자신의 답변 평가하기(Assess Your Response)”)를 수행한다.

.. image:: ../../../../shared/building_and_running_chapters/Images/PA_AsmtWithResponse.png
  :alt: Image of peer assessment with assessment steps and status labeled
  :width: 600

.. 참고:: 학습자 연습 단계를 포함할 경우 상호 평가 단계 또한 반드시 추가해야 한다. 학습자 연습 단계는 반드시 상호 평가 단계 및 자기 평가 단계에 선행해야 한다.


.. _PA Student Training Assessments:

========================
학습자 연습 단계
========================

상호 평가 과제를 생성할 때, 1개 이상의 학습자 연습 평가를 넣어서 학습자가 평가 방법을 익히는 데 도움이 되게 할 수 있다. 1개의 학습자 연습 평가에는 강좌 운영팀이 작성한 예제 1개 이상과 강좌 운영팀이 이 예제에 부여한 점수를 함께 제시할 수 있다. 이를 통해, 학습자는 강좌 운영팀이 점수를 매긴 방식에 맞춰 점수를 받을 수 있도록 노력할 것이다.

.. 참고:: 학습자 연습 단계를 포함하는 경우 상호 평가 단계도 반드시 추가해야 한다. 학습자 연습 단계는 반드시 상호 평가 단계 및 자기 평가 단계에 선행해야 한다.

학습자 연습 단계에서 “답변 평가 방법 학습하기” 단계는 학습자가 답변을 제출한 직후에 표시된다. 학습자는 강좌 운영팀이 만든 예제 가운데 한 가지와 이에 해당하는 채점 기준표를 확인한다. 이 때, 강좌 운영팀이 부여한 점수는 표시되지 않는다. 학습자는 자신이 평가할 것의 개수 또한 확인할 수 있다.

.. image:: ../../../../shared/building_and_running_chapters/Images/PA_TrainingAssessment.png
   :alt: Sample training response, unscored
   :width: 500

학습자는 각 과제의 평가 항목에 대한 평가 등급을 선택하고 **자신의 선택과 교수자의 선택 비교하기** 를 클릭한다. 학습자가 선택한 것이 모두 교수자의 선택과 일치하는 경우 다음 예제가 자동으로 열린다.

학습자의 선택 가운데 교수자의 선택과 상이한 것이 존재하는 경우 해당 답변이 학습자에게 다시 제시된다. 이 때, 해당 답변 위에 다음과 같은 메시지가 표시된다.

.. code-block:: xml

  Learning to Assess Responses
  Your assessment differs from the instructor's assessment of this response. Review the
  response and consider why the instructor may have assessed it differently. Then, try 
  the assessment again.

평가 항목 각각에 대해, 학습자 선택과 교수자 선택의 일치 여부에 따라 다음 두 가지 메시지 가운데 하나가 학습자에게 제시된다. 

.. code-block:: xml

  Selected Options Differ
  The option you selected is not the option that the instructor selected.

.. code-block:: xml

  Selected Options Agree
  The option you selected is the option that the instructor selected.

아래의 예시에서 학습자는 옳은 평가 등급 하나와 옳지 않은 평가 등급 하나를 각각 선택하고 있다.

.. image:: ../../../../shared/building_and_running_chapters/Images/PA_TrainingAssessment_Scored.png
   :alt: Sample training response, scored
   :width: 500

학습자는 모든 평가 항목에 대한 자신의 채점 결과와 교수자의 채점 결과가 동일해질 때까지 채점을 계속한다.

:ref:`PA Student Training Step` 에서 보다 자세한 정보를 확인한다.


=====================
상호 평가 단계
=====================

상호 평가 단계에서 학습자는 다른 학습자의 답변을 검토, 해당 답변에 기반하여 여러분이 제시한 채점 기준표의 각 평가 항목에 대해 평가 등급을 선택한다.

답변 및 평가의 개수
************************************

상호 평가 단계를 포함할 경우 각 학습자기 **평가할 답변의 개수** 와 각 답변에 대한 **상호 평가의 개수** 를 지정해야 한다.

.. 참고:: 일부 학습자는 답변만을 제출하고 상호 평가를 수행하지 않을 수 있다. 따라서 일부 답변은 지정된 필수 개수의 평가를 받지 못할 수 있다. 모든 답변이 원래 지정된 개수대로 평가받을 확률을 높이려면 학습자기 평가해야 하는 답변의 개수를 각 답변이 반드시 받아야 하는 평가의 개수보다 높도록 설정해야만 한다. 가령, 각 답변이 3개의 평가를 받도록 지정한 경우 각 학습자가 5개의 답변을 평가하도록 설정할 수 있다.

모든 답변에 대한 평가가 완료되었으나 일부 학습자가 상호 평가를 필수 개수대로 수행하지 않은 경우 해당 학습자는 다른 학습자가 이미 평가한 답변을 평가할 수 있다. 이러한 답변을 제출한 학습자에게는 자신의 점수를 채점할 때 상호 평가가 추가 제시된다. 그러나 추가 상호 평가는 자신의 답변이 받은 점수에 가산되지 않다.

.. _Feedback Options:

피드백 선택 조건
****************

전체 채점 기준표 아래에 단 하나의 학습자 의견 작성 필드가 제공되는 것이 기본 설정으로 돼 있다. 1개 혹은 여러 개의 평가 항목에 대해 이러한 학습자 의견 작성 필드를 추가할 수 있다. 의견 필드에 입력할 수 있는 문자는 최대 300개이다.

의견 필드는 해당 평가 항목의 평가 등급 아래에 표시된다. 다음 사례의 경우 두 평가 항목 모두에 하나의 의견 필드가 있다. 답변에 대한 종합 의견을 입력할 수 있는 필드도 하나 있다.

.. image:: ../../../../shared/building_and_running_chapters/Images/PA_CriterionAndOverallComments.png
   :alt: Rubric with comment fields under each criterion and under overall response
   :width: 600

보다 구체적인 정보는 :ref:`PA Add Rubric` 및 :ref:`PA Criteria Comment Field Only` 에서 확인한다.

.. _PA Scoring:

상호 평가 채점
***********************

상호 평가는 평가 항목별로 채점한다. 각 평가 항목에 대한 점수(score)는 각 상호 평가자가 해당 평가 항목에 매긴 점수의 중앙값으로 한다. 가령, 어떤 상호 평가에서 세 명의 학습자가 Ideas 평가 항목에 각각 10, 7, 8점을 부여한 경우 Idea 평가 항목의 점수는 8이 된다.

학습자가 상호 평가에서 획득하는 최종 점수는 각 평가 항목에 대한 점수의 중앙값의 합으로 한다.

가령, 어떤 답변에 대해 상호 평가자로부터 다음과 같은 점수를 획득한다고 가정할 수 있다.

.. list-table::
   :widths: 25 10 10 10 10
   :stub-columns: 1
   :header-rows: 1

   * - 평가 항목 제목
     - 동료 1
     - 동료 2
     - 동료 3
     - 중앙값
   * - Ideas (10점 만점)
     - 10
     - 7
     - 8
     - **8**
   * - Content (10점 만점)
     - 7
     - 9
     - 8
     - **8**
   * - Grammar (5점 만점)
     - 4
     - 4
     - 5
     - **4**

각 평가 항목의 점수 중앙값을 합하여 최종 점수를 계산한다.

  **Idea 항목의 중앙값 (8/10) + Content 중앙값 (8/10) + Grammar 중앙값 (4/5) = 최종 점수 (20/25)**

재차 강조하지만 최종 점수는 평가자별이 아니라 평가 항목별로 계산한다. 따라서 어떤 답변으로 획득한 점수는 각 상호 평가자가 해당 답변에 부여한 여러 점수의 중앙값이 아니다.

추가 답변 평가
********************************

학습자는 지정된 개수를 초과하여 답변을 평가할 수 있다. 학습자가 상호 평가 단계를 마치면 해당 단계가 닫히고 **상호 평가하기** 라는 제목이 표시된다.

.. image:: ../../../../shared/building_and_running_chapters/Images/PA_PAHeadingCollapsed.png
   :width: 500
   :alt: The peer assessment step with just the heading visible

학습자가 **상호 평가하기** 제목을 클릭하면 해당 단계가 전개되고 여기에서 **상호 평가 계속하기** 를 클릭할 수 있다.

.. image:: ../../../../shared/building_and_running_chapters/Images/PA_ContinueGrading.png
   :width: 500
   :alt: The peer assessment step expanded so that "Continue Assessing Peers" is visible


=====================
자기 평가 단계
=====================

자기 평가 단계에서는 학습자 자신의 답변 뒤에 여러분이 작성한 채점 기준표가 제시된다. 상호 평가와 마찬가지로 학습자는 채점 기준표와 자신의 답변을 비교하며 각 평가 항목에 대해 평가 등급을 선택한다. 

상호 평가와 자기 평가를 모두 포함하는 경우 자기 평가를 상호 평가 뒤에 배치할 것을 권고한다. 

.. _PA Top Responses:

*****************************
우수 답변
*****************************

학습자가 과제로 제출한 답변 가운데 최상위 점수를 획득한 답변과 해당 점수를 함께 게시하는 **우수 답변** 섹션을 게시할 수 있다. **우수 답변** 섹션은 학습자가 해당 과제의 모든 단계를 종료한 후 학습자 점수 정보 아래에 게시된다.

.. image:: ../../../../shared/building_and_running_chapters/Images/PA_TopResponses.png
   :alt: Section that shows the text and scores of the top three responses for the assignment
   :width: 500

**우수 답변** 섹션에는 최소 1개, 최대 100개의 답변을 게시할 수 있다. 해당 목록에서 각 답변의 높이는 최대 300픽셀이다. (답변이 이보다 더 길 경우, 학습자는 페이지를 스크롤하여 전체 답변을 확인할 수 있다.) 게시하는 답변의 개수를 20개 이하로 지정하여 해당 페이지가 지나치게 길어지지 않도록 할 것을 권고한다.

.. 참고:: 최상위 점수를 획득한 어떤 답변이 **우수 답변** 목록에 게시되는 데에는 1시간가량 소요될 수 있다.

이에 관한 보다 자세한 정보는 :ref:`PA Show Top Responses` 에서 확인할 수 있다.
