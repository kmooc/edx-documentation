.. _Numerical Input:

########################
수식 입력 문제
########################

Studio가 제공하는 수식 입력 도구 가운데 보다 기본적인 도구이다. 이 유형의 문제에서는 학습자가 질문에 대한 답변으로 숫자 또는 비교적 단순한 특정 수식을 입력한다. 학습자가 입력한 문자열은 기호식으로 변환되어 답변 필드 아래에 표시된다.

.. image:: ../../../shared/building_and_running_chapters/Images/image292.png
 :alt: Image of a numerical input problem

이 유형의 문제에서는 학습자 답변의 값이 정확하지 않아도 되며 오차 범위 또는 허용 한계를 지정할 수 있다. 직접 정답을 지정하거나 Python 스크립트를 사용할 수도 있다. 아래에 보다 자세하게 설명한다.

수식 입력 문제에 대한 답변은 정수, 분수, 그리고 원주율(pi)이나 중력 가속도(g) 등의 상수를 포함할 수 있다. 제곱근(sqrt)이나 10을 밑으로 하는 로그 등의 간단한 함수, 그리고 사인(sin), 아크사인(arcsin)과 같은 삼각함수 및 역삼각함수를 나타내는 문자열도 가능하다. 학습자가 이들 함수를 나타내는 문자열을 입력하면 해당 문자열이 수학 기호로 변환된다. 수식 입력 문제에서 학습자의 문자열을 수식으로 변환하는 장면을 아래의 예에 제시한다.

.. image:: ../../../shared/building_and_running_chapters/Images/Math5.png
 :alt: Image of a numerical input probem rendered by Studio

학습자가 입력할 수 있는 문자에 관한 보다 구체적인 정보를 :ref:`Math Response Formatting for Students` 에서 확인할 수 있다.

***********************************
수식 입력 문제 생성하기 
***********************************

기본 편집기나 고급 편집기로 수식 입력 문제를 생성할 수 있다. 어떤 편집기를 사용하든 문제에 대한 답은 동일한다. 문제의 지문에 이탤릭체, 볼드체, 특수 문자가 없는 경우라면 기본 편집기로 생성 가능하다. 문제 지문에 특수 포맷이나 특수 문자, 또는 Python 스크립트가 포함되는 경우 고급 편집기를 사용한다.

이를 테면, 아래의 예제를 생성하려면 고급 편집기를 사용해야 한다. 

.. image:: ../../../shared/building_and_running_chapters/Images/NumericalInput_Complex.png
 :alt: Image of a more complex numerical input problem

문제 지문에 Python 스크립트를 입력하는 방법에 대한 보다 구체적인 정보는 :ref:`Write Your Own Grader` 을 참조한다.

==================
기본 에디터
==================

#. **신규 구성요소 추가** 에서 **문제** 를 클릭한다.

#. **문제 구성 요소 유형 선택** 화면에서 **공통 문제 유형** 탭의 **수식 입력** 을 클릭한다.

3. 신규 문제 구성요소가 표시되면 **편집** 을 클릭한다.

#. 구성요소 편집기의 예제 문자열을 원하는 문자열로 바꾼다.

#. 표시(label)로 사용할 문제 텍스트를 결정한 후 해당 텍스트를 두 쌍의 꺾쇠괄호(>><<)로 묶는다.

#. 정답 텍스트를 선택한 후 수식 입력 단추를 클릭한다.

.. image:: ../../../shared/building_and_running_chapters/Images/ProbCompButton_NumInput.png
    :alt: Image of the numerical input button

이 과정을 완료하면 정답 옆에 “=” 표시가 나타난다.
        
7. (선택 사항) 오차 범위 또는 허용 한계를 지정한다. 백분율, 숫자 또는 범위를 지정할 수 있다.

   * 정답 양측(±)으로 허용 한계를 지정하려면 해당 정답 뒤에 +-숫자%를 입력한다. 가령 2%의 허용 오차를 두고자 하는 경우 +-2%를 입력한다. 

   * 정답 양측(±)으로 숫자를 지정하려면 해당 정답 뒤에 +-숫자를 입력한다. 가령 허용 한계 5를 두고자 하는 경우 +-5를 입력한다.

   * 범위를 지정하려면 대괄호([]) 또는 괄호(())를 이용한다. 대괄호는 해당 대괄호에 인접한 숫자를 포함한다는 의미이며 괄호는 해당 괄호에 인접한 숫자를 포함하지 않는다는 뜻이다. 이를테면, 범위를 [5, 8)로 지정할 경우 5, 6, 7은 정답이나 8은 정답이 아니다. 범위를 (5, 8]로 지정할 경우 6, 7, 8은 정답이나 5는 정답이 아니다.

8. 구성요소 편집기에서 설명용 텍스트를 선택한 후 설명 단추를 눌러 해당 텍스트에 설명 태그를 추가한다.

   .. image:: ../../../shared/building_and_running_chapters/Images/ProbCompButton_Explanation.png
    :alt: Image of the explanation button

9. **설정** 탭에서 원하는 설정을 구성한다.

#. **저장** 을 클릭한다.

상기 첫 번째 예제 가운데 문제 구성요소의 텍스트는 다음과 같다.

::

   >>What base is the decimal numeral system in?<<

   = 10
    
   [explanation]
   The decimal numerial system is base ten.
   [explanation]

==================
고급 편집기
==================

이 유형의 문제를 고급 편집기로 생성하려는 경우 “문제” 구성요소 편집기의 **고급** 탭을 클릭한 후 기존 코드를 다음 코드로 교체한다.

**문제 코드** :

.. code-block:: xml

  <problem>
    <p><b>Example Problem</b></p>

  <p>What base is the decimal numeral system in?
      <numericalresponse answer="10">
          <formulaequationinput label="What base is the decimal numeral system in?"/>
      </numericalresponse>
  </p>

    <p>What is the value of the standard gravity constant <i>g</i>, measured in m/s<sup>2</sup>? Give your answer to at least two decimal places.
    <numericalresponse answer="9.80665">
      <responseparam type="tolerance" default="0.01" />
      <formulaequationinput label="Give your answer to at least two decimal places"/>
    </numericalresponse>
  </p>

  <!-- The following uses Python script spacing. Make sure it isn't indented when you add it to the Problem component. -->
  <script type="loncapa/python">
  computed_response = math.sqrt(math.fsum([math.pow(math.pi,2), math.pow(math.e,2)]))
  </script>

  <p>What is the distance in the plane between the points (pi, 0) and (0, e)? You can type math.
      <numericalresponse answer="$computed_response">
          <responseparam type="tolerance" default="0.0001" />
          <formulaequationinput label="What is the distance in the plane between the points (pi, 0) and (0, e)?"/>
      </numericalresponse>
  </p>
  <solution>
    <div class="detailed-solution">
      <p>Explanation</p>
      <p>The decimal numerical system is base ten.</p>
      <p>The standard gravity constant is defined to be precisely 9.80665 m/s<sup>2</sup>.
      This is 9.80 to two decimal places. Entering 9.8 also works.</p>
      <p>By the distance formula, the distance between two points in the plane is
         the square root of the sum of the squares of the differences of each coordinate.
        Even though an exact numerical value is checked in this case, the
        easiest way to enter this answer is to type
        <code>sqrt(pi^2+e^2)</code> into the editor.
        Other answers like <code>sqrt((pi-0)^2+(0-e)^2)</code> also work.
      </p>
    </div>
  </solution>
  </problem>

.. _Numerical Input Problem XML:

****************************
수식 입력 문제 XML
****************************

=========
템플릿
=========

십진법 숫자 체계 또는 백분율로 나타낸 허용 한계 부여 여부에 따른 수식 입력 문제의 템플릿이다.

허용 한계를 주지 않은 문제
***************************

.. code-block:: xml

  <p>TEXT OF PROBLEM
      <numericalresponse answer="ANSWER (NUMBER)">
          <formulaequationinput label="TEXT OF PROBLEM"/>
      </numericalresponse>
  </p>
   
    <solution>
    <div class="detailed-solution">
    <p>TEXT OF SOLUTION</p>
    </div>
  </solution>
  </problem>

십진법 숫자로 허용 한계를 준 문제
************************************

.. code-block:: xml

  <problem>
   
    <p>TEXT OF PROBLEM
    <numericalresponse answer="ANSWER (NUMBER)">
      <responseparam type="tolerance" default="NUMBER (DECIMAL, e.g., .02)" />
      <formulaequationinput label="TEXT OF PROBLEM"/>
    </numericalresponse>
  </p>
   
    <solution>
    <div class="detailed-solution">
    <p>TEXT OF SOLUTION</p>
    </div>
  </solution>
  </problem>

백분율 허용 한계를 준 문제
************************************

.. code-block:: xml

  <problem>
   
   <p>TEXT OF PROBLEM
    <numericalresponse answer="ANSWER (NUMBER)">
      <responseparam type="tolerance" default="NUMBER (PERCENTAGE, e.g., 3%)" />
      <formulaequationinput label="TEXT OF PROBLEM"/>
    </numericalresponse>
   </p>

    <solution>
    <div class="detailed-solution">
    <p>TEXT OF SOLUTION</p>
    </div>
  </solution>
  </problem>

스크립트로 생성한 정답
************************************

.. code-block:: xml

  <problem>

  <!-- The following uses Python script spacing. Make sure it isn't indented when you add it to the Problem component. -->
  <script type="loncapa/python">
  computed_response = math.sqrt(math.fsum([math.pow(math.pi,2), math.pow(math.e,2)]))
  </script>

  <p>TEXT OF PROBLEM
      <numericalresponse answer="$computed_response">
          <responseparam type="tolerance" default="0.0001" />
          <formulaequationinput label="TEXT OF PROBLEM"/>
      </numericalresponse>
  </p>

    <solution>
    <div class="detailed-solution">
     <p>TEXT OF SOLUTION</p>
    </div>
  </solution>
  </problem>

====
태그
====

* ``<numericalresponse>`` (필수): 해당 문제를 수식 입력 문제로 지정한다.
* ``<formulaequationinput />`` (필수): 학습자 답변을 입력할 답변 필드를 제공한다.
* ``<responseparam>`` (선택): 정답에 대한 허용 한계 또는 오차 범위를 지정한다.
* ``<script>`` (선택):

.. note:: 기존 문제 일부는 ``<formulaequationinput />`` 태그 대신 ``<textline math="1" />`` 태그를 사용하고 있다. 그러나 ``<textline math="1" />`` 태그에 대한 비판이 있기 때문에 새로 생성하는 문제에서는 ``<formulaequationinput />`` 태그를 사용한다.

**태그:** ``<numericalresponse>``

해당 문제를 수식 입력 문제로 지정한다. ``<numericalresponse>`` 태그는 ``<formularesponse>`` 와 유사하지만 지정되지 않은 변수를 허용하지 않는다는 점에서 다르다.

  속성

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - answer (필수)
       - 문제의 정답. 수식으로 제시된다.

  .. note:: 문제 지문에서 변수명 앞에 달러 기호($)를 붙이면 해당 수식을 해당 변수에 대해 계산하는 스크립트를 삽입할 수 있다.


  채점자는 제공하는 답과 학습자 답변을 동일한 방식으로 평가한다. 또한 채점자는 강좌 운영팀 또는 학습자가 어떠한 수식을 제시하더라도 이를 자동적으로 단순화한다. 정답은 0.3이나 42처럼 단순할 수도, 1/3이나 sin(pi/5)처럼 다소 복잡할 수도 있다.

  Children
  
  * ``<responseparam>``
  * ``<formulaequationinput>``

**태그:** * ``<formulaequationinput>``

학습자가 답변을 입력하는 LMS에 답변 필드를 생성한다.

  속성

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명    
     * - label (필수)
       - 답변 필드의 이름을 지정한다.
     * - size (선택)
       - LMS 내 답변 필드의 폭(width)을 문자(개수)로 정의한다.
  
  Children

  (없음)

**태그:** ``<responseparam>``

정답에 대한 허용 한계 또는 오차 범위를 지정한다.

  속성

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - type (선택)
       - “tolerance”: 숫자에 대한 허용 한계를 정의한다.
     * - default (선택)
       - 십진법 체계의 수 또는 백분율 허용 한계를 지정하는 숫자 또는 백분율

  Children
  
  (없음)

**태그:** ``<script>``

채점자가 학습자 답변을 평가하는 데 사용하는 스크립트를 지정한다. 이 경우 문제는 모든 스크립트 태그에 포함된 모든 코드가 단 하나의 스크립트 태그에 포함된 것처럼 작동한다. 특히, 2개 이상의 ``<script>`` 태그에서 복수의 변수를 사용하는 경우 이들 변수는 단 하나의 네임스페이스를 공유하며 따라서 재정의(overriden) 될 수 있다.

모든 Python이 그러하듯, 들여쓰기(indentation)가 중요한다. 해당 코드가 XML에 임베드 된 경우 역시 그러한다.

  속성

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - type (필수)
       - 반드시 “loncapa/python” 으로 설정해야 한다.

  Children
  
  (없음)
