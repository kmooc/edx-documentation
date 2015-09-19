.. _Math Expression Input:

####################################
수식 입력 문제
####################################

수식 입력 문제에서는 학습자가 수학식을 간소화한 일반 문자열을 필드에 입력하고 Enter키를 치면 해당 문자열이 기호식으로 변환되어 해당 필드 바로 밑에 표시된다. 정수 및 일부 상수만을 입력할 수 있는 수치 입력 문제와 달리 수식 입력 문제에서는 미지의 변수 및 다소 복잡한 기호식도 입력할 수 있다. 

.. image:: ../../../shared/building_and_running_chapters/Images/MathExpressionInputExample.png
 :alt: Image of math expression input problem

수식 입력 문제에 입력할 수 있는 문자에 관한 보다 자세한 정보를 :ref:`Math Response Formatting for Students` 에서 확인할 수 있다.

채점자는 수치 샘플링을 이용하여 학습자 답변이 사전 설정된 수치적 허용 한계 내에서 교수자가 제시하는 수식과 일치하는지 판단한다. 교수자는 해당 수식에 사용할 수 있는 변수와 각 변수값의 범위를 반드시 규정해야 한다.

.. warning:: 현재까지 수식 입력 문제에서는 음수를 분수로 거듭제곱한 표현(예: (-1)^(1/2))을 입력할 수 없다. 그러나 복소수의 분수 거듭제곱 또는 양의 비복소수의 분수 거듭제곱은 입력 가능하다.

Studio에서 수식 입력 문제를 생성하는 경우 MathJax를 이용하여 일반 문자열을 “진짜 수학식”으로 변환한다. Studio에서 MathJax를 사용하는 방법에 관해서는 Studio에서 MathJax 사용하는 방법 간략 소개( :ref:`MathJax in Studio` ) 을 참조한다.

************************************************
수식 입력 문제 생성하기
************************************************

수식 입력 문제를 생성하는 단계는 다음과 같다.

#. 문제를 생성하고자 하는 학습활동에서 **신규 구성요소 추가** 아래에 있는 **문제** 를 클릭한 후 **고급** 탭을 클릭한다.
#. **수식 입력** 을 클릭한다.
#. 구성요소가 표시되면 **편집** 을 클릭한다.
#. 구성요소 편집기에 있는 예시 코드를 원하는 코드로 바꾼다. 아래의 예시 코드를 이용하여 연습할 수 있다.
#. **저장** 을 클릭한다.


**예시 코드**

.. code-block:: xml

  <problem>
    <p>Some problems may ask for a mathematical expression. Practice creating mathematical expressions by answering the questions below.</p>

    <p>Write an expression for the product of R_1, R_2, and the inverse of R_3.</p>
    <formularesponse type="ci" samples="R_1,R_2,R_3@1,2,3:3,4,5#10" answer="$VoVi">
      <responseparam type="tolerance" default="0.00001"/>
      <formulaequationinput size="40" label="Enter the equation"/>
    </formularesponse>

  <script type="loncapa/python">
  VoVi = "(R_1*R_2)/R_3"
  </script>

    <p>Let <i>x</i> be a variable, and let <i>n</i> be an arbitrary constant. What is the derivative of <i>x<sup>n</sup></i>?</p>
  <script type="loncapa/python">
  derivative = "n*x^(n-1)"
  </script>
    <formularesponse type="ci" samples="x,n@1,2:3,4#10" answer="$derivative">
      <responseparam type="tolerance" default="0.00001"/>
      <formulaequationinput size="40"  label="Enter the equation"/>
    </formularesponse>

    <solution>
      <div class="detailed-solution">
        <p>Explanation or Solution Header</p>
        <p>Explanation or solution text</p>
      </div>
    </solution>
  </problem>

.. _Math Expression Input Problem XML:

**********************************
수식 입력 문제 XML
**********************************

============
템플릿
============

.. code-block:: xml

  <problem>
    <p>Write an expression for the product of R_1, R_2, and the inverse of R_3.</p>
    <formularesponse type="ci" samples="R_1,R_2,R_3@1,2,3:3,4,5#10" answer="R_1*R_2/R_3">
      <responseparam type="tolerance" default="0.00001"/> 
      <formulaequationinput size="40"  label="Enter the equation" />
    </formularesponse>
  </problem>

.. code-block:: xml

  <problem>
    <p>Problem text</p>
    <formularesponse type="ci" samples="VARIABLES@LOWER_BOUNDS:UPPER_BOUNDS#NUMBER_OF_SAMPLES" answer="$VoVi">
      <responseparam type="tolerance" default="0.00001"/>
      <formulaequationinput size="20"  label="Enter the equation" />
    </formularesponse>

  <script type="loncapa/python">
  PYTHON SCRIPT
  </script>

    <solution>
      <div class="detailed-solution">
        <p>Explanation or Solution Header</p>
        <p>Explanation or solution text</p>
      </div>
    </solution>
  </problem>

====
태그
====

* ``<formularesponse>``
* ``<formulaequationinput />``
* ``<responseparam>``
* ``<script>``

**태그:** ``<formularesponse>``

해당 문제가 수식 입력 문제라는 사실을 규정한다. ``<formularesponse>`` 태그는 ``< numericalresponse >`` 와 같은 형태이다. ``<formularesponse>`` 태그는 미지의 변수를 허용한다.

  속성

  **type**: “cs”(대소문자 구분 (초기값)) 또는 “ci”(대소문자 구분하지 않음. 변수명을 대문자와 무관하게 하기 위함)가 될 수 있다.

  **answer**: 문제에 대한, 수식으로 된 정답. 문제 내부에 있는 변수명 맨앞에 달러 기호($)를 붙일 경우 해당 수식을 그 변수에 대해 계산할 수 있는 스크립트를 해당 문제 안에 포함할 수 있다.

  **samples**: 문제에 대한 중요 정보를 다음 네 가지 목록에서 지정한다.

    * **variables**: 학습자가 입력할 수 있는 일련의 변수
    * **lower_bounds**: 정의된 각 변수에 있어 해당 변수를 사용하기 위한 수치 테스트의 하한
    * **upper_bounds**: 정의된 각 변수에 있어 해당 변수를 사용하기 위한 수치 테스트의 상한
    * **num_samples**: 해당 수식의 테스트 횟수

    상기한 네 가지 리스트 각각의 내부 항목은 반점(,)으로 서로 분리한다. 또, 네 가지 리스트는 특수 문자 앳(@), 콜론(:), 파운드(#)로 분리한다. 형식은 다음과 같다.

    ``"variables@lower_bounds:upper_bounds#num_samples``

    가령, samples 속성을 포함하는 ``<formularesponse>`` 태그는 다음 중 하나와 같은 형태를 취할 수 있다.

    ``<formularesponse samples="x,n@1,2:3,4#10">``

    ``<formularesponse samples="R_1,R_2,R_3@1,2,3:3,4,5#10">``

  Children

  * ``<formulaequationinput />``

**태그:** ``<formulaequationinput />``

학습자가 문제에 대한 답을 일반 문자열로 입력할 답변 필드, 그리고 학습자가 자신이 입력한 일반 문자열이 수식으로 변환된 형태를 확인할 수 있는 두 번째 필드를 해당 답변 필드 아래에 생성한다. 학습자가 입력한 일반 문자열을 수식으로 변환하는 이 파서는 학습자 답변을 평가, 채점하는 파서와 동일한다.


  속성

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - label(필수)
       - 답변 필드의 이름을 지정한다.
     * - size (선택)
       - 학습자가 답을 입력하는 답변 필드의 폭(width)을 문자(개수)로 지정한다.

  Children
  
  (없음)

**태그:** ``<responseparam>``

동일성 검정을 근사하는 데 사용하는 수치 해석의 분산의 상한을 정의하는 데 사용한다.

  속성

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - default (필수)
       - 학습자 입력 수식이 채점자 제시 수식과 얼마나 유사해야 하는지를 규정하는 숫자 또는 백분율이다. 허용 한계를 포함하지 않을 경우 학습자 입력 수식에 회피 불가능한 오류인 반올림 오차가 개입할 위험이 증가하며 이로 인해 채점자 제시 수식과 대수적으로 동일한 의미를 갖는 경우에도 학습자 입력 수식 일부가 오답으로 처리된다.
     * - type
       - “tolerance” 어떤 수치에 대한 허용 오차를 정의한다.

  Children
  
  (없음)

