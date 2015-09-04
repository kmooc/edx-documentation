.. _Working with Problem Components:

################################
문제 구성요소
################################

******************************
문제 구성요소 개관
******************************

문제 구성요소는 K-MOOC 담당자가 상호작용하며 자동으로 채점되는 연습문제를 강좌 콘텐츠에 추가할 수 있도록 허용한다. K-MOOC 담당자는 스튜디오에서 다양한 유형의 문제를 만들 수 있다.

모든 문제는 포인트 점수를 받게 되지만, 기본적으로 문제는 학습자의 성적(grade)으로 포함되지는 않는다. 학습자의 성적으로 문제가 포함되기를 원하는 경우, 문제를 포함 하고 있는 소주제의 과제 유형을 바꾸도록 한다.

본 주제에서는 K-MOOC 담당자 및 학습자에게 문제 구성요소가 어떻게 보여지는지, 그리고 모든 문제 구성요소가 가지고 있는 옵션은 무엇인지 등 문제 구성요소의 기초를 다룬다. 각 문제 유형에 대한 더 자세한 내용은:ref:`Create Exercises` 를 참조하도록 한다.

더 자세한 내용은 다음 주제를 참조하도록 한다.

* :ref:`Problem Student View`
* :ref:`Problem Studio View`
* :ref:`Problem Settings`
* :ref:`Modifying a Released Problem`
* :ref:`Additional Work with Problems`
* :ref:`Multiple Problems in One Component`
* :ref:`Problem Randomization`

.. _Problem Student View:

************************************
학습자가 볼 문제 보기
************************************

. EdX 플랫폼에 있는 모든 문제는 여러 가지 구성 요소들을 가진다.

.. image:: ../../../shared/building_and_running_chapters/Images/AnatomyOfExercise1.png
 :alt: Image of a problem from a student's point of view, with callouts for 
       elements of the problem

#. **문제 텍스트**. 문제 텍스트는 어떤 표준 HTML 서식이라도 포함할 수 있다.

#. **학습자 답안을 포함하는 답안 입력 입력 필드.** 학습자는 *답안 입력 입력 필드* 에 답을 입력한다. 답안 입력 입력 필드의 모양은 문제의 유형에 따라 달라진다.

#. **만들어진 답변.** 일부 문제 유형에 대해, 스튜디오는 일반 텍스트를 "아름다운 수학공식"으로 만들기 위해 MathJax를 사용한다.

#. **확인하기 버튼.** 학습자는 답안을 제출하거나 그의 대답이 올바른지 알기 위해 **확인** 을 클릭한다. 답이 맞으면, 녹색 확인 표시가 나타난다. 답이 틀리면, 빨간색 X가 나타난다. 학습자가 **확인하기 버튼** 을 클릭하면, 스튜디오는 성적 및 문제의 현재 상태를 저장한다.

#. **저장하기 버튼.** 학습자는 성적을 위해 답안을 제출하지 않고 현재 답안을 저장하기 위해 **저장** 을 클릭할 수 있다. 이것은 학습자가 문제 풀기를 멈추고 나중에 다시 돌아와 계속 풀 수 있도록 허용한다.

#. **답안 표시 버튼.** 이 버튼은 선택 사항이다. 학습자가 **답안 표시** 를 클릭하면 학습자는 정확한 답 (위의 2번 참조)과 설명 (아래 10번 참조)을 모두 보게 된다. 교수자는 **답안 표시** 버튼이 표시되는지 여부를 설정한다. 

#. **시도하기.** 교수자는 문제 풀기에 대한 특정 시도 횟수를 설정하거나 또는 무제한 시도를 허용할 수 있다. 기본적으로는 강좌 전체에 **최대 시도** 에 대한 고급 설정은 null이며, 문제에 대한 최대 시도 횟수에 제한이 없음을 의미한다. 강좌 전체에 걸친 **최대 시도** 설정을 특정한 수로 변경하려면, 개별 문제에 대한 **최대 시도** 설정은 그 숫자를 기본값으로 가지며, 더 이상 무제한으로 설정 될 수 없다.

   .. image:: ../../../shared/building_and_running_chapters/Images//AnatomyOfExercise2.png
    :alt: Image of a problem from a student's point of view, with callouts for 
          attempts and showing the answer

#. **피드백.** 학습자가 **확인하기** 를 클릭한 후, 모든 문제는 녹색 확인 표시 또는 빨간색 X를 반환한다

   .. image:: ../../../shared/building_and_running_chapters/Images//AnatomyofaProblem_Feedback.png
    :alt: Image of feedback checkmark and x from a student's point of view

#. **정확한 답안.** 대부분의 문제에 대하여 교수자는 단일 정답을 지정해야 한다.

#. **설명.** 교수자는 학습자가 **답안 표시** 를 클릭하면 나타나는 설명을 포함할 수 있다.

#. **재설정 버튼.** 학습자는 제출되지 않은 모든 입력을 취소하고, 질문에 다시 대답하기 위해 **재설정** 을 클릭할 수 있다. 학습자가 이미 답안을 제출한 경우, **재설정** 을 클릭하는 것은 제출을 삭제하며, 만약 무작위 변수를 포함하는 문제에서 무작위 추출하기(randomization)가 **재설정 가능** 으로 설정된 경우, 문제에서 학습자가 보는 값은 변경된다. 문제에 대해 설정된 최대 시도 횟수에 도달하면, **재설정** 버튼은 더 이상 표시되지 않는다.

#. **답안 버튼 숨기기.**

   .. image:: ../../../shared/building_and_running_chapters/Images//AnatomyOfExercise3.png
    :alt: Image of a problem in the course accordian

#. **채점하기.** 교수자는 그룹 문제들의 채점 여부를 지정할 수 있다. 그룹 문제가 채점되는 경우, 강좌 아코디언에서 해당 과제에 대한 시계 아이콘이 나타난다.

   .. image:: ../../../shared/building_and_running_chapters/Images//clock_icon.png

#. **기한.** 문제를 제출하기로 되어 있는 날짜이다. 기한을 넘긴 문제는 **확인** 버튼이 없다. 또한 답안을 수락하지 않거나 피드백을 제공하지 않는다.

.. 참고:: 문제는 **열리거나 닫힐** 수 있다. 닫힌 문제는 **확인** 버튼이 없다. 학습자는 여전히 질문, 답안 및 공개된 설명을 볼 수 있지만, 문제 풀기 상태를 확인하거나, 답안을 제출 하거나, 또는 이전 점수를 변경하는 등의 작업은 할 수 없다.

또한 즉시 표시되지 않는 문제의 몇 가지 특성이 있다. K-MOOC 담당자는 스튜디오에서 이러한 특성을 설정할 수 있다.

*  **무작위 추출하기.** 몇 가지 문제에 대하여, 교수자는 문제가 학습자마다 다르도록 임의로 생성된 숫자를 사용할 것인지 여부를 지정할 수 있다.

*  **가중치.** 특정 문제 세트에서 다른 문제는 다른 가중치가 주어질 수 있다.

*  **라벨.** 장애가 있는 학습자의 접근성을 개선하기 위해, 각 문제는 설명 라벨이 필요하다. 라벨은 일반적으로 문제에 있는 질문의 텍스트의 일부 또는 전부를 포함한다. 대부분의 템플릿은 라벨에 대한 공간을 포함한다. K-MOOC 담당자는 각 문제 또는 도구 유형에 대한 문서에서 예제 라벨을 찾을 수 있다.

.. _Problem Studio View:

************************************
스튜디오에서 문제 보기
************************************

. 모든 문제는 XML로 작성된다. 그러나, 스튜디오는 문제 구성요소를 편집하기 위해 두 개의 인터페이스를 제공한다: 간단한 편집기 및 고급 편집기.

*   **간단한 편집기** 는 K-MOOC 담당자가 XML 작업을 하지 않고 문제를 시각적으로 편집할 수 있도록 허용한다. 

*  **고급 편집기** 는 문제를 edX의 XML 표준으로 변환하고 K-MOOC 담당자가 해당 XML을 직접 편집할 수 있도록 허용한다.

K-MOOC 담당자는 간단한 편집기 인터페이스의 오른쪽 상단 모서리에서 **고급 편집기** 를 클릭하여 언제든지 간단한 편집기에서 고급 편집기로 전환할 수 있다. 그러나, 그것은 고급 편집기에서 간단한 편집기로 전환하는 것은 불가능하다.

.. _Simple Editor:

=================
간단한 편집기
=================

다중 선택 및 텍스트를 입력하는 문제의 템플릿을 포함한 여러 가지 문제의 템플릿은 간단한 편집기에서 연다.  다음 이미지는 간단한 편집기에서 다중 선택 문제를 보여준다.

.. image:: ../../../shared/building_and_running_chapters/Images//MultipleChoice_SimpleEditor.png
 :alt: Image of a problem in the simple editor

간단한 편집기는 K-MOOC 담당자가 문제의 텍스트의 서식을 지정하는데 도움이 되는 도구 모음을 포함한다. 텍스트를 선택한 다음 서식 버튼을 클릭하면, 간단한 편집기는 자동으로 텍스트 형식을 바꾼다. 도구 모음 버튼은 다음과 같다:

1. 수준 1 머리글을 만든다. 
2. 다중 선택 옵션을 만든다.
3. 확인란(checkbox) 옵션을 만든다. 
4. 텍스트 입력 옵션을 만든다.
5. 숫자 입력 옵션을 만든다.
6. 드롭 다운 옵션을 만든다. 
7. 학습자가 **답안 표시** 를 클릭 하면 표시되는 설명을 만든다.
8. 고급 편집기에서 문제를 연다.
9. 서식하기 힌트 목록을 연다.

다음 문제 템플릿은 간단한 편집기에서 열린다. 

*  :ref:`Checkbox` 체크박스 문제에서, 학습자는 가능한 답변 목록에서 하나 이상의 옵션을 선택한다.

*  :ref:`Dropdown` 드롭다운 문제에서, 학습자는 드롭다운 목록에서 하나의 답변을 선택한다.

*  :ref:`Multiple Choice` 다중 선택 문제에서 학습자는 질문 아래에 표시되는 선택 목록에서 하나의 답변을 선택해야 한다.

*  :ref:`Numerical Input`숫자 입력 문제는 오직 정수, 분수, 그리고 몇 가지 일반적인 상수와 연산자를 포함하는 답변만을 요구한다.

*  :ref:`Text Input` 텍스트 입력 문제에서, 학습자는 질문에 대한 답변을 짧은 텍스트를 입력한다.


.. _Advanced Editor:

===================
고급 에디터
===================
**고급 편집기** 는 xml에서 문제를 연다. 끌어서 놓기 및 수식 입력과 같은 문제에 대한 템플릿은 고급 편집기에서 직접 연다.

다음 이미지는 간단한 편집기 대신 고급 편집기에서 위의 다중 선택 문제를 보여준다.

.. image:: ../../../shared/building_and_running_chapters/Images//MultipleChoice_AdvancedEditor.png
 :alt: Image of a problem in the advanced editor

다음 문제 템플릿은 고급 편집기에서 열린다.

* :ref:`Circuit Schematic Builder` 회로 구조 문제에서, 학습자는 대화형 그리드에서 회로를 만들고 수정하며, 컴퓨터에서 생성된 회로 분석을 채점용으로 제출한다.

* :ref:`Custom JavaScript` 사용자 지정 자바 스크립트 표시 및 문제 채점에 대해, K-MOOC 담당자는 IFrame을 통해 HTML에서 만든 문제 유형을 스튜디오로 통합할 수 있다.

* :ref:`Drag and Drop` 끌어서 놓기 문제는 학습자가 이미지의 특정 위치에 텍스트 또는 개체를 끌어놓아야 한다.

* :ref:`Image Mapped Input` 이미지가 그려진 입력 문제는 학습자가 이미지의 특정 위치를 클릭해야 한다.

* :ref:`Math Expression Input` 수식 입력 문제는 학습자가 수식을 e = m * c ^2와 같은 텍스트로 입력해야 한다.

* :ref:`Problem with Adaptive Hint` 이러한 문제는 학습자에게 그들의 답안에 따라 피드백 또는 힌트를 줄 수 있다.  적응형 힌트 문제는 텍스트 입력 문제 또는 다중 선택 문제가 될 수 있다.

* :ref:`Problem Written in LaTeX` 이 문제 유형은 K-MOOC 담당자가 이미 LaTeX로 작성한 문제를 edX 형식으로 변환할 수 있도록 허용한다. 그러나 이 문제 유형은 여전히 프로토타입(prototype)이며 앞으로 지원되지 않을 수 있음을 주의한다.

* :ref:`Write Your Own Grader` 사용자 정의 Python에서 평가된 입력 (또한 스스로 채점 작성(“write-your-own-grader”))이라고 불리는 문제는 K-MOOC 담당자가 만든 포함된 Python 스크립트를 사용하여 학습자의 답안을 평가한다. 이러한 문제는 모든 종류가 될 수 있다.

.. _Problem Settings:

******************
문제 설정
******************

문제 텍스트 뿐만 아니라, 문제 구성요소를 이용하여 만든 문제는 다음과 같은 설정을 가진다. 이러한 설정은 구성요소 편집기에서 **설정** 탭에 표시 됩니다.

*  **표시 이름**
*  **최대 시도**
*  **문제 가중치**
*  **무작위 추출하기**
*  **답안 표시**
*  **재설정 표시 버튼**

.. image:: ../../../shared/building_and_running_chapters/Images/ProbComponent_Attributes.png
 :alt: Image of the Settings tab in a Problem component

===============
표시 이름
===============

이 설정은 문제의 이름을 나타낸다. 표시 이름은 LMS와 문제 페이지의 상단에 강좌 리본에 있는 문제 위에 제목으로 나타난다.

.. image:: ../../../shared/building_and_running_chapters/Images/ProbComponent_LMS_DisplayName.png
 :alt: Image of the problem in a unit page from a student's point of view

==============================
최대 시도
==============================

이 설정은 학습자가 문제에 대한 답변을 시도할 수 있는 횟수를 지정한다. 기본적으로, 강좌 전체에 걸친 **최대 시도** 고급 설정은 null이다. 이것은 문제에 대한 최대 시도 횟수에 제한이 없음을 의미한다. 강좌 전체에 걸친 **최대 시도** 설정을 특정 숫자로 변경하는 경우, 개별 문제에 대한 **최대 시도** 설정을 그 숫자를 기본값으로 가지고, 더 이상 무제한으로 설정 될 수 없다.

.. 참고:: 1 또는 더 높은 **최대 시도** 설정을 가지는 문제만이 강좌 동안 다운로드 할 수 있는 학습자 답변 배포 보고서에 포함된다. 

.. _Problem Weight:

==============================
문제 비중
==============================

.. 참고:: 스튜디오는모든 문제에 대한 점수를 저장 하지만, 점수가 채점된 소주제에 있는 경우만 학습자의 최종 성적으로 계산된다.

이 설정은 문제에 대해 가능한 포인트의 최대수를 지정한다. 문제 가중치는 문제 제목 옆에 표시되어 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/ProblemWeight_DD.png
 :alt: Image of a problem from a student's point of view, with the possible 
       points circled

기본적으로, 문제 구성요소에서 각 답안 입력입력 필드 또는 "답변 공간"은 1점의 가치가 있다. 모든 문제 구성요소는 다중 답안 입력 입력 필드를 가질 수 있다. 예를 들어 위의 문제 구성요소는 세 가지 별도의 질문에 대답해야 하는 하나의 드롭다운 문제를 포함함으로 세 가지 답안 입력 입력 필드가 있어야 한다. 

다음의 문제 구성요소는 하나의 텍스트 입력 문제를 포함함으로 단지 하나의 답안 입력 입력 필드가 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/ProblemWeight_TI.png
 :alt: Image of a text input problem from a student's point of view

점수 계산하기
****************

학습자 문제에 대해 얻는 점수는 다음 공식의 결과이다:

**점수 = 가중치 x (정답/답변 입력입력 필드)**

*  **점수** 는 학습자가 받는 포인트 점수이다. 

*  **가중치** 는 문제의 최대 가능한 포인트 점수이다.

*  **정답** 은 정답을 포함하는 답안 입력 입력 필드 수이다. 

*  **답안 입력 필드** 는 문제에서 답안 입력 입력 필드의 총 수이다.

**예제**

점수 계산하기의 몇 가지 예는 다음과 같다.

*예제 1*

문제의 **가중치** 설정은 비어 있는 채로 남아 있다. 문제는 두 개의 답안 입력 필드를 가진다. 문제가 두 개의 답안 입력 필드를 가지기 때문에, 최대 점수는 2.0점이다. 하나의 답안 입력 필드는 정답을 포함하고, 다른 답안 입력 필드는 오답을 포함하는 경우, 학습자의 점수는 2점 중에 1.0점이다. 

*예제 2*

문제의 가중치는 12로 설정되어 있다. 문제는 세 개의 답안 입력 필드를 가진다. 학습자의 답변이 2개의 정답과 1 개의 오답을 포함하는 경우 학습자의 점수는 12점 중에 8.0점이다.

*예제 3*

문제의 가중치는 2로 설정되어 있다. 문제는 네 개의 답안 입력 필드를 가진다. 학습자의 답변이 하나의 정답과  3 개의 오답을 포함하는 경우, 학습자의 점수는 2점 중에 0.5 점이다.

.. _Randomization:

===============
무작위 추출하기
===============

이 설정은 다른 학습자가 문제에 접근할 때마다 혹은 한 학습자가 문제에 각각 답변할 때마다 문제에서 특정 값이 변경되는지 여부를 지정한다. 예를 들어 아래 문제에서 강조 표시된 값은 학습자가 문제에 대한 답변을 제출할 때마다 변경된다.

.. image:: ../../../shared/building_and_running_chapters/Images/Rerandomize.png
 :alt: The same problem shown twice, with color highlighting on values that 
       can change

: K-MOOC 담당자가 문제에서 특정 값을 변경 또는  "무작위 추출하기" 하려는 경우, 다음의 두 가지를 반드시 해야 한다: 

* 해당 문제가 K-MOOC 담당자가 원하는 값을 무작위 추출하기 하는 Python 스크립트를 포함하고 있는지 확인한다. 

* 문제 구성요소에서 무작위 추출하기를 이용 가능하게 만든다. 

.. 참고:: **무작위 추출하기** 설정을 지정하는 것은 문제 무작위 추출하기와 다르다는 것에 주의한다 **무작위 추출하기** 설정은 단일 문제 내에서 변수를 무작위로 바꾼다. 문제 무작위 추출하기는 다른 학습자에게 다른 문제 또는 다른 문제 버전을 제공한다. 더 자세한 내용은 :ref:`Problem Randomization` 를 참조하도록 한다.

무작위 추출하기를 이용 가능하게 만들려면, **무작위 추출하기** 설정에 대한 옵션을 선택한다. 이 설정은 다음과 같은 옵션을 가지고 있다.

+-------------------+--------------------------------------+
| **Always**        |학습자는 **확인하기**을 클릭할 때마다 문제의 다른 버전을 본다.                           |
+-------------------+--------------------------------------+
| **On Reset**      | Students see a different version of  |
|                   | the problem each time they click     |
|                   | **Reset**.                           |
+-------------------+--------------------------------------+
| **Never**         | All students see the same version    |
|                   | of the problem. This is the default. |
+-------------------+--------------------------------------+
| **Per Student**   | Individual students see the same     |
|                   | version of the problem each time     |
|                   | they look at it, but that version    |
|                   | is different from the version that   |
|                   | other students see.                  |
+-------------------+--------------------------------------+

.. note:: The edX Platform has a 20-seed limit for randomization.

.. _Show Answer:

===============
Show Answer
===============

This setting defines when the problem shows the answer to the student.
This setting has the following options.

+-------------------+--------------------------------------+
| **Always**        | Always show the answer when the      |
|                   | student clicks the **Show Answer**   |
|                   | button.                              |
+-------------------+--------------------------------------+
| **Answered**      | Show the answer after the student    |
|                   | tries to answer the problem.         |
|                   |                                      |
|                   | If the question can be, and is,      |
|                   | reset, the answer                    |
|                   | is not shown until the student tries |
|                   | the problem again. (When a student   |
|                   | answers a question, the question is  |
|                   | considered to be                     |
|                   | both attempted and answered. When    |
|                   | the question is reset, the question  |
|                   | is still attempted, but not yet      |
|                   | answered.)                           |
+-------------------+--------------------------------------+
| **Attempted**     | Show the answer after the student    |
|                   | tries to answer the problem.         |
|                   |                                      |
|                   | If the question can be, and is,      |
|                   | reset, the answer                    |
|                   | *continues to show*.                 |
|                   | (When a student answers a question,  |
|                   | the question is considered to be     |
|                   | both attempted and                   |
|                   | answered. When the question is       |
|                   | reset, the question is still         |
|                   | attempted, but not yet answered.)    |
+-------------------+--------------------------------------+
| **Closed**        | Show the answer after the student    |
|                   | has used up all his attempts to      |
|                   | answer the problem or the due date   |
|                   | has passed.                          |
+-------------------+--------------------------------------+
| **Finished**      | Show the answer after the student    |
|                   | has answered the problem correctly,  |
|                   | the student has no attempts left, or |
|                   | the problem due date has passed.     |
+-------------------+--------------------------------------+
| **Correct or      | Show the answer after the student    |
| Past Due**        | has answered the problem correctly   |
|                   | or the problem due date has passed.  |
+-------------------+--------------------------------------+
| **Past Due**      | Show the answer after the due date   |
|                   | for the problem has passed.          |
+-------------------+--------------------------------------+
| **Never**         | Never show the answer. In this case, |
|                   | the **Show Answer** button does not  |
|                   | appear next to the problem in Studio |
|                   | or in the LMS.                       |
+-------------------+--------------------------------------+

.. _Show Reset Button:

=================
Show Reset Button
=================

This setting defines whether a **Reset** button is visible on the problem.
Students can click **Reset** to clear any input that has not yet been submitted,
and try again to answer the problem. If the student has already submitted an
answer, clicking **Reset** clears the submission and, if the problem contains
randomized variables and randomization is set to **On Reset**, changes the
values the student sees in the problem. If the number of Maximum  Attempts that
was set for this problem has been reached, the **Reset** button is not visible.

This problem-level settimg overrides the course-level **Show Reset Button for Problems** setting.

.. _Modifying a Released Problem:

*********************************
Modifying a Released Problem
*********************************

.. warning:: Be careful when you modify problems after they have been 
 released! Changes that you make to published problems can affect the student
 experience in the course and analysis of course data.

After a student submits a response to a problem, the edX Learning Management
System (LMS) stores the student’s response, the score that the student
received, and the maximum score for the problem. For problems with a **Maximum
Attempts** setting greater than 1, the LMS updates these values each time the
student submits a new response to a problem. However, if an instructor changes
a problem or its attributes, existing student information for that problem is
not automatically updated.

For example, you may release a problem and specify that its answer is 3.
After some students have submitted responses, you notice that the answer
should be 2 instead of 3. When you update the problem with the correct
answer, the LMS doesn’t update scores for students who answered 2 for the
original problem and thus received the wrong score.

For another example, you may change the number of response fields to
three. Students who submitted answers before the change have a score of
0, 1, or 2 out of 2.0 for that problem. Students who submitted answers
after the change have scores of 0, 1, 2, or 3 out of 3.0 for the same
problem.

If you change the weight setting for the problem in Studio, however, existing
student scores update when the student's **Progress** page is refreshed. In a
live section, students will see the effect of these changes.

===============
Workarounds
===============

If you have to modify a released problem in a way that affects grading, you
have two options within Studio to assure that every student has the opportunity
to submit a new response and be regraded. Note that both options require you to
ask your students to go back and resubmit answers to a problem.

*  In the Problem component that you changed, increase the number of attempts
   for the problem. Then ask all your students to redo the problem.

*  Delete the entire Problem component in Studio and create a new Problem
   component with the content and settings that you want. (If the revisions you
   must make are minor, duplicate the Problem component before you delete it
   and revise the copy.) Then ask all your students to complete the new
   problem.

For information about how to review and adjust student grades in the LMS, see
:ref:`Grades`.

.. _Additional Work with Problems:

************************************
Additional Work with Problems
************************************

You have some further options when you work with problems. You can include more
than one problem in a single problem component, or you can set up a problem
that presents different versions to different students.

.. _Multiple Problems in One Component:

====================================
Multiple Problems in One Component
====================================

You may want to create a problem that has more than one response type. For
example, you may want to create a numerical input problem, and then include a
multiple choice question about the numerical input problem. Or, you may want a
student to be able to check the answers to many problems at one time. To do
this, you can include multiple problems inside a single Problem component. The
problems can be different types.

.. note:: 
  You cannot use a :ref:`Custom JavaScript` in a component that contains more
  than one problem. Each custom JavaScript problem must be in its own
  component.

To create multiple problems in one component, create a new Blank Advanced
Problem component, and then add the XML for each problem in the component
editor. You only need to include the XML for the problem and its answers. You
don’t have to include the code for other elements, such as the **Check**
button.

Elements such as the **Check**, **Show Answer**, and **Reset** buttons, as well
as the settings that you select for the Problem component, apply to all of the
problems in that component. Thus, if you set the maximum number of attempts to
3, the student has three attempts to answer the entire set of problems in the
component as a whole rather than three attempts to answer each problem
individually. If a student clicks **Check**, the LMS scores all of the problems
in the component at once. If a student clicks **Show Answer**, the answers for
all the problems in the component appear.

.. _Problem Randomization:

===========================
Problem Randomization
===========================

You may want to present different students with different problems, or
different versions of the same problem. To do this, you'll create a Problem
component for each problem or version in Studio, and then edit your course
outside of Studio to randomize the problem that students see.

Note that *problem randomization* is different from the **Randomization**
setting in Studio. The **Randomization** setting randomizes variables within a
single problem. Problem randomization offers different problems or problem
versions to different students.

.. note:: Creating problems with versions that can be randomized requires you 
 to export your course, edit some of your course's XML files in a text editor,
 and then re-import your course. We recommend that you create a backup copy of
 your course before you do this. We also recommend that you only edit your
 course files in the text editor if you're very familiar with editing XML.

Terminology
************

Sections, subsections, units, and components have different names in the
**Course Outline** view and in the list of files that you'll see after you
export your course and open the .xml files for editing. The following table
lists the names of these elements in the **Course Outline** view and in a list
of files.

.. list-table::
   :widths: 15 15
   :header-rows: 0

   * - Course Outline View
     - File List
   * - Section
     - Chapter
   * - Subsection
     - Sequential
   * - Unit
     - Vertical
   * - Component
     - Discussion, HTML, problem, or video

For example, when you want to find a specific section in your course, you'll
look in the **Chapter** folder when you open the list of files that your course
contains. To find a unit, you'll look in the **Vertical** folder.

.. _Create Randomized Problems:

Create Randomized Problems
****************************

#. In the unit where you want to create a randomized problem, create a separate
   Problem component for each version or problem that you want to randomize.
   For example, if you want to offer four versions or problems, you'll create
   four separate Problem components. Make a note of the 32-digit unit ID that
   appears in the **Unit Identifier** field under **Unit Location**.

#. Export your course. For information about how to do this, see
   :ref:`Exporting and Importing a Course`. Save the .tar.gz file that contains
   your course in a memorable location so that you can find it easily.

#. Locate the .tar.gz file that contains your course, and then unpack the
   .tar.gz file so that you can see its contents in a list of folders and
   files.

   To do this on a Windows computer, you'll need to download a third-party
   program. For more information, see `How to Unpack a tar File in Windows
   <http://www.haskell.org/haskellwiki/How_to_unpack_a_tar_file_in_Windows>`_,
   `How to Extract a Gz File <http://www.wikihow.com/Extract-a-Gz-File>`_, `The
   gzip Home Page <http://www.gzip.org/>`_, or the `Windows
   <http://www.ofzenandcomputing.com/how-to-open-tar-gz-files/#windows>`_
   section of the `How to Open .tar.gz Files <http://www.ofzenandcomputing.com
   /how-to-open-tar-gz-files/>`_ page.

   For information about how to do this on a Mac, see the `Mac OS X
   <http://www.ofzenandcomputing.com/how-to-open-tar-gz-files/#mac-os-x>`_
   section of the `How to Open .tar.gz Files <http://www.ofzenandcomputing.com
   /how-to-open-tar-gz-files/>`_ page.

#. In the list of folders and files, open the **Vertical** folder.

   .. note:: If your unit is not published, open the **Drafts** folder, and 
    then open the **Vertical** folder in the **Drafts** folder.

#. In the **Vertical** folder, locate the .xml file that has the same name as
   the unit ID that you noted in step 1, and then open the file in a text
   editor such as Sublime 2. For example, if the unit ID is
   e461de7fe2b84ebeabe1a97683360d31, you'll open the
   e461de7fe2b84ebeabe1a97683360d31.xml file.

   The file contains a list of all the components in the unit, together with
   the URL names of the components. For example, the following file contains
   four Problem components.

   .. code-block:: xml
     
       <vertical display_name="Test Unit">
          <problem url_name="d9d0ceb3ffc74eacb29501183e26ad6e"/>
          <problem url_name="ea66d875f4bf4a9898d8e6d2cc9f3d6f"/>
          <problem url_name="2616cd6324704f85bc315ec46521485d"/>
          <problem url_name="88987707294d4ff0ba3b86921438d0c0"/>
       </vertical>

#. Add ``<randomize> </randomize>`` tags around the components for the problems
   that you want to randomize.

   .. code-block:: xml
      
       <vertical display_name="Test Unit">
         <randomize>
            <problem url_name="d9d0ceb3ffc74eacb29501183e26ad6e"/>
            <problem url_name="ea66d875f4bf4a9898d8e6d2cc9f3d6f"/>
            <problem url_name="2616cd6324704f85bc315ec46521485d"/>
            <problem url_name="88987707294d4ff0ba3b86921438d0c0"/>
         </randomize>
       </vertical>

#. After you add the ``<randomize> </randomize>`` tags, save and close the .xml
   file.

#. Re-package your course as a .tar.gz file.

   For information about how to do this on a Mac, see `How to Create a Tar GZip
   File from the Command Line <http://osxdaily.com/2012/04/05/create- tar-
   gzip/>`_.

   For information about how to do this on a Windows computer, see `How to Make
   a .tar.gz on Windows <http://stackoverflow.com/questions/12774707 /how-to-
   make-a-tar-gz-on-windows>`_.

#. In Studio, re-import your course.

.. note::

  * Once you've implemented randomization, you can only see one of the versions
    or problems in Studio. You can edit that single problem directly in Studio,
    but to edit any of the other problems, you'll have to export your course,
    edit the problems in a text editor, and then re-import the course. This is
    true for instructors as well as course teams.
  
  * A .csv file for student responses contains the responses to each of the
    problems in the problem bank.
