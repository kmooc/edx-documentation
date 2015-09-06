.. _Multiple Choice and Numerical Input:

############################################
선택형-수식 입력 혼합 문제
############################################

선택형 문제와 수치 입력 문제를 혼합한 문제를 생성할 수 있다. 학습자는 제공하는 선택지 중에서 답변을 선택할 뿐 아니라 필요에 따라 보다 구체적인 정보를 추가 입력할 수도 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/MultipleChoice_NumericalInput.png
  :alt: Image of a multiple choice and numerical input problem

.. 참고:: 현재까지는 학습자가 문자열 필드에 숫자만을 입력할 수 있다. 숫자가 아닌 문자 또는 수학식은 입력할 수 없다.

.. _Create an MCNI Problem:

********************************************************
선택형-수치 입력 혼합 문제 생성하기
********************************************************

선택형-수치 입력 혼합 문제를 생성하는 절차는 다음과 같다.

#. 문제를 생성하고자 하는 학습 활동에서 **새 구성 요소 추가** 의 **문제** 를 클릭한 후 **고급** 탭을 클릭한다.
#. **고급 문제 생성** 을 클릭한다.
#. 구성 요소가 표시되면 **편집** 을 클릭한다.
#. 구성 요소 편집기에 아래의 코드를 복사해 넣는다.
#. 기존 예제를 지우고 생성하고자 하는 선택지를 추가한다.
#. **저장** 을 클릭한다.

.. _MCNI Problem Code:

************************************************
선택형-수치 입력 혼합 문제 코드
************************************************

.. code-block:: xml

  <problem>
  The numerical value of pi, rounded to two decimal points, is 3.24.
  <choicetextresponse>
  <radiotextgroup>
  <choice correct="false">True.</choice>
  <choice correct="true">False. The correct value is <numtolerance_input answer="3.14"/>.</choice>
  </radiotextgroup>
  </choicetextresponse>
  </problem>
