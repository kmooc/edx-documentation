.. _Multiple Choice:

########################
선다형 문제
########################

선다형 문제(multiple choice problem)에서는 학습자가 선택지 가운데 하나를 선택한다. 학습자가 드롭다운(dropdown) 화살표를 클릭하기 전까지 선택지가 표시되지 않는 드롭다운형 문제와 달리, 선다형 문제에서는 해당 질문지 아래에서 선택지를 가시적으로 직접 확인할 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/MultipleChoiceExample.png
 :alt: Image of a multiple choice problem

또한, 선다형 문제에는 각 학습자에게 일련의 선택지를 무작위로 제시하는 등, 몇 가지 고급 선택 조건이 있다. :ref:`Multiple Choice Advanced Options` 에서 이들 선택 조건에 관한 보다 자세한 정보를 확인할 수 있다.

****************************************
선다형 문제 생성하기
****************************************

 “간편 편집기(Simple Editor)” 또는 “고급 편집기(Advanced Editor)”에서 선택형 문제를 생성할 수 있다.

.. note:: 모든 문제에는 접근성 라벨이 반드시 있어야 한다. 일반적으로 이 표시에는 해당 문제의 주 질문지 텍스트가 포함된다. 공통 문제용 표시를 추가하려면 해당 표시의 텍스트를 꺾쇠괄호(<>)로 묶되 뾰족한 쪽이 텍스트를 향하게 한다.(>>label text<<).

================
간편 편집기
================

#. **신규 구성요소 추가** 에서 **문제** 를 클릭한다.
#. **문제 구성요소 유형 선택** 화면의 **공통 문제 유형** 탭에서 **선다형 문항** 을 클릭한다.
#. 새 문제 구성요소가 표시되면 **편집** 을 클릭한다.
#. 구성요소 편집기의 예제 텍스트를 생성하고자 하는 문제의 텍스트로 바꾼다. 각 선택지를 해당 열에 입력한다.
#. 표시로 사용할 문제의 텍스트를 결정한 후 해당 텍스트를 꺾쇠괄호(>><<)로 묶는다.
#. 선택지를 모두 선택한 후 선다형 문제 단추를 클릭한다.
   
   .. image:: ../../../shared/building_and_running_chapters/Images/ProbCompButton_MultChoice.png
    :alt: Image of the multiple choice button
   
   이제 구성 요소 편집기가 각 정답 옆에 한 쌍의 괄호를 추가한다.
   
#. 정답 옆의 괄호 사이에 “x”를 입력한다.
   
#. 구성 요소 편집기에서 설명(explanation) 텍스트를 선택한 후 설명 단추를 클릭하여 해당 텍스트에 설명 태그를 추가한다.

   .. image:: ../../../shared/building_and_running_chapters/Images/ProbCompButton_Explanation.png
    :alt: Image of the explanation button

#. **설정** 탭에서 여러분이 원하는 설정을 지정한다. 
#. **저장** 을 클릭한다.

상기 예제에 대한 문제 구성요소 내부의 텍스트는 다음과 같다.

::

    >>Lateral inhibition, as was first discovered in the horsehoe crab:<<

    ( ) is a property of touch sensation, referring to the ability of crabs to 
    detect nearby predators.
    ( ) is a property of hearing, referring to the ability of crabs to detect 
    low frequency noises.
    (x) is a property of vision, referring to the ability of crabs eyes to 
    enhance contrasts.
    ( ) has to do with the ability of crabs to use sonar to detect fellow horseshoe 
    crabs nearby.
    ( ) has to do with a weighting system in the crabs skeleton that allows it to 
    balance in turbulent water.

    [Explanation]
    Horseshoe crabs were essential to the discovery of lateral inhibition, a property of 
    vision present in horseshoe crabs as well as humans, that enables enhancement of 
    contrast at edges of objects as was demonstrated in class. In 1967, Haldan Hartline 
    received the Nobel prize for his research on vision and in particular his research 
    investigating lateral inhibition using horseshoe crabs.
    [Explanation]

================
고급 편집기
================

고급 편집기에서 이 문제를 생성하려면 문제 구성요소 편집기에서 **고급** 탭을 클릭한 후 기존 코드를 다음으로 교체한다.

.. code-block:: xml

  <problem>
  <p>Lateral inhibition, as was first discovered in the horsehoe crab...</p>
  <multiplechoiceresponse>
    <choicegroup type="MultipleChoice" label="Lateral inhibition, as was first
    discovered in the horsehoe crab">
      <choice correct="false">is a property of touch sensation, referring to the 
      ability of crabs to detect nearby predators.</choice>
      <choice correct="false">is a property of hearing, referring to the ability
      of crabs to detect low frequency noises.</choice>
      <choice correct="false">is a property of vision, referring to the ability
      of crabs eyes to enhance contrasts.</choice>
      <choice correct="true">has to do with the ability of crabs to use sonar 
      to detect fellow horseshoe crabs nearby.</choice>
      <choice correct="false">has to do with a weighting system in the crabs 
      skeleton that allows it to balance in turbulent water.</choice>
    </choicegroup>
  </multiplechoiceresponse>
  <solution>
    <div class="detailed-solution">
      <p>Explanation</p>
      <p>Horseshoe crabs were essential to the discovery of lateral inhibition,
      a property of vision present in horseshoe crabs as well as humans, that
      enables enhancement of contrast at edges of objects as was demonstrated in
      class. In 1967, Haldan Hartline received the Nobel prize for his research
      on vision and in particular his research investigating lateral inhibition
      using horseshoe crabs.</p>
    </div>
  </solution>
  </problem>

.. _Multiple Choice Advanced Options:

*********************************************
선다형 문제 고급 선택 조건
*********************************************

선다형 문제에는 다양한 고급 선택 조건이 있다. 문제 안에 있는 선택지의 순서를 변경할 수 있고 학습자가 특정 오답을 선택할 경우 나타나는 설명을 삽입하거나 학습자별로 선택지 집합을 무작위로 제시할 수도 있다. 보다 자세한 정보가 필요할 경우 다음을 참조한다.


* :ref:`Shuffle Answers in a Multiple Choice Problem`
* :ref:`Targeted Feedback in a Multiple Choice Problem`
* :ref:`Answer Pools in a Multiple Choice Problem`

.. _Shuffle Answers in a Multiple Choice Problem:

=============================================
선다형 문제의 선택지 순서 변경하기
============================================= 

선택 조건의 하나로, 선다형 문제의 구성을 변경하여 선택지 순서를 바꿀 수 있다.

가령, 어떤 학습자가 보는 문제 화면은 다음과 같을 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/multiple-choice-shuffle-1.png
 :alt: Image of a multiple choice problem

동일한 문제에 대하여 다른 학습자 또는 위의 학습자가 보는 문제 화면을 다음과 같이 구성할 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/multiple-choice-shuffle-2.png
 :alt: Image of a multiple choice problem with shuffled answers

또한, 선택지 중 일부의 순서를 바꾸되 나머지는 그대로 둘 수도 있다. 이를테면 원래의 선택지 순서를 그대로 유지한 채 선택지 가장 아래에 “위의 모든 답(All of the Above)”이라는 항목을 둘 수 있다.

선택지 순서 변경과 관련한 문제 구성은 :ref:`Simple Editor` 또는 :ref:`Advanced Editor` 로 가능하다.


간편 편집기로 선택지 순서 변경하기
*********************************************

:ref:`Simple Editor` 에서 선택지 순서를 변경할 수 있다.

예를 들어, 선택지 순서 변경에 앞서 다음 텍스트로 정의되는 선택형 문제가 있다고 가정한다. 이때, (x)는 정답을 의미한다.

 >>What Apple device competed with the portable CD player?<<
     ( ) The iPad
     ( ) Napster
     (x) The iPod
     ( ) The vegetable peeler

이 문제의 선택지 순서를 바꾸려면 첫 번째 선택지의 괄호 사이에 느낌표(!)를 입력한다.

 >>What Apple device competed with the portable CD player?<<
     (!) The iPad
     ( ) Napster
     (x) The iPod
     ( ) The vegetable peeler

선택지 중 하나의 위치를 고정하려면 해당 선택지의 괄호 사이에 앳(@)을 삽입한다.


 >>What Apple device competed with the portable CD player?<<
     (!) The iPad
     ( ) Napster
     (x) The iPod
     ( ) The vegetable peeler
     (@) All of the above

필요에 따라 복수의 기호를 삽입할 수 있다. 이를테면 정답의 위치를 고정하고자 하는 경우 다음과 같이 할 수 있다.
 
  (x@) The iPod

고급 편집기로 선택지 순서 변경하기
*********************************************

:ref:`Advanced Editor` 의 XML을 통해 선택지 순서를 변경할 수 있다.

예를 들어, 선택지 순서 변경에 앞서 다음 XML로 선택형 문제를 정의할 수 있다.

.. code-block:: xml

 <p>What Apple device competed with the portable CD player?</p>
 <multiplechoiceresponse>
  <choicegroup type="MultipleChoice">
    <choice correct="false">The iPad</choice>
    <choice correct="false">Napster</choice>
    <choice correct="true">The iPod</choice>
    <choice correct="false">The vegetable peeler</choice>
  </choicegroup>
 </multiplechoiceresponse>


이 문제의 선택지 순서를 변경하려면 ``<choicegroup>`` 에 ``shuffle="true"`` 를 추가한다.

.. code-block:: xml

 <p>What Apple device competed with the portable CD player?</p>
 <multiplechoiceresponse>
  <choicegroup type="MultipleChoice" shuffle="true">
    <choice correct="false">The iPad</choice>
    <choice correct="false">Napster</choice>
    <choice correct="true">The iPod</choice>
    <choice correct="false">The vegetable peeler</choice>
  </choicegroup>
 </multiplechoiceresponse>

선택지 가운데 하나의 위치를 고정하려면 해당 선택지에 해당하는 ``choice`` 에 ``fixed="true"`` 를 추가한다.

.. code-block:: xml

 <p>What Apple device competed with the portable CD player?</p>
 <multiplechoiceresponse>
  <choicegroup type="MultipleChoice" shuffle="true">
    <choice correct="false">The iPad</choice>
    <choice correct="false">Napster</choice>
    <choice correct="true">The iPod</choice>
    <choice correct="false">The vegetable peeler</choice>
    <choice correct="false" fixed="true">All of the above</choice>
  </choicegroup>
 </multiplechoiceresponse>


.. _Targeted Feedback in a Multiple Choice Problem:

===============================================
선별적 피드백을 제공하는 선택형 문제
===============================================

오답에 대한 설명을 학습자에게 자동 제시하여 학습자가 정답을 찾는 데 안내가 되도록 선택형 문제를 구성할 수 있다. 따라서, 학습자가 정답을 찾을 때까지 답을 반복 선택할 수 있는 선택형 문제에서는 선별적 피드백이 가장 유용한다.


간편 편집기로 선별적 피드백 구성하기
********************************************************

:ref:`Advanced Editor` 의 XML을 통해 선별적 피드백을 제공하는 문제를 구성한다.

다음 XML 가이드라인을 따른다:

* ``<multiplechoiceresponse>`` 에 ``targeted-feedback`` 속성을 추가한다. 값은 주지 않는다.
* ``<solution>`` 앞에 ``<targetedfeedbackset>`` 을 추가한다.
* ``<targetedfeedbackset>`` 내부에 ``<targetedfeedback>`` 을 1개 이상 추가한다.
* 아래의 설명과 같이 각 ``<targetedfeedback>`` 내부에 오답에 대한 설명을 HTML 마크업으로 입력한다.
* 각 오답에 대한 동일한 ``explanation-id`` 속성값을 이용하여 ``<targetedfeedback>`` 을 해당 오답에 연결한다.
* 정답에는 ``<solution>`` 을 이용한다. 이 때, 정답의 ``<choice>`` 와 동일한 ``explanation-id`` 속성값을 사용한다.

이를테면 선다형 문제에 대한 XML은 다음과 같다.

.. code-block:: xml

   <p>What Apple device competed with the portable CD player?</p>
   <multiplechoiceresponse targeted-feedback="">
    <choicegroup type="MultipleChoice">
      <choice correct="false" explanation-id="feedback1">The iPad</choice>
      <choice correct="false" explanation-id="feedback2">Napster</choice>
      <choice correct="true" explanation-id="correct">The iPod</choice>
      <choice correct="false" explanation-id="feedback3">The vegetable peeler</choice>
    </choicegroup>
   </multiplechoiceresponse>
 
이 뒤에 선택형 피드백을 정의하는 XML이 온다.

.. code-block:: xml

   <targetedfeedbackset>
     <targetedfeedback explanation-id="feedback1">
       <div class="detailed-targeted-feedback">
         <p>Targeted Feedback</p>
         <p>The iPad came out later and did not directly compete with portable CD players.</p>
       </div>
     </targetedfeedback>
     <targetedfeedback explanation-id="feedback2">
       <div class="detailed-targeted-feedback">
         <p>Targeted Feedback</p>
         <p>Napster was not an Apple product.</p>
       </div>
     </targetedfeedback>
     <targetedfeedback explanation-id="feedback3">
       <div class="detailed-targeted-feedback">
         <p>Targeted Feedback</p>
         <p>Vegetable peelers don't play music.</p>
       </div>
     </targetedfeedback>
    </targetedfeedbackset>

    <solution explanation-id="correct">
     <div class="detailed-solution">
      <p>The iPod directly competed with portable CD players.</p>
     </div>
    </solution>


.. _Answer Pools in a Multiple Choice Problem:

=============================================
선택지 풀을 제공하는 선택형 문제
=============================================

선택지를 무작위로 조합한 하위 집합을 각 학습자에게 제시하는 선다형 문제를 구성할 수 있다. 가령, 해당 선다형 문제에 잠재적 정답 10가지를 부여한 후 5개의 선택지로 구성한 집합 1개를 각 학습자에게 제시할 수 있다.

전체 선택지(선택지 풀) 중에는 반드시 최소 1가지의 정답이 있어야 하며 그 개수는 2개 이상일 수도 있다. 1명의 학습자에게 제시되는 각 선택지 집합에는 1개의 정답이 포함된다. 이를테면, 10개로 구성된 선택지 집합에 2개의 정답이 있도록 문제를 구성할 수 있다. 각 학습자에게 제공되는 선택지 각각에 이 2가지 정답 가운데 하나가 포함된다.

고급 편집기로 선택지 풀 구성하기
**************************************************

:ref:`Advanced Editor` 의 XML을 통해 선택지 풀(answer pool)을 제공하는 문제를 구성한다.

다음 XML 지침을 따른다.

* ``<choicegroup>`` 에서 ``answer-pool`` 속성을 부여한다. 이 때, 숫자로 된 값은 해당 선택지 집합에 포함된 선택지의 개수를 나타낸다. 이를테면 ``<choicegroup answer-pool="4">`` 과 같이 구성할 수 있다.

* 각 정답의 ``<choice>`` 에 ``explanation-id`` 속성과 풀이에 해당하는 값을 부여한다. 이를테면, ``<choice correct="true" explanation-id="iPod">The iPod</choice>`` 와 같이 구성할 수 있다.

* 각 ``<solution>`` 에 ``explanation-id`` 속성과 정답으로 되돌리는 값을 부여한다. 이를테면 ``<solution explanation-id="iPod">`` 와 같이 구성할 수 있다.

.. note:: 전체 선택지 가운데 정답이 단 1가지인 경우 ``<choice>`` 나 ``<solution>`` 에 ``explanation-id`` 속성을 부여할 필요가 없다. 그러나 이 경우에도 ``<solutionset>`` 으로 ``<solution>`` 을 래핑해야 한다.

이를테면 다음 선다형 문제에서는 각 학습자에게 4가지 선택지로 구성된 선택지 집합이 제시되며 각 집합에 속한 선택지 가운데 1개가 전체 2가지 정답 가운데 하나가 된다. 정답에 표시되는 설명에는 동일한 설명 ID(explanation ID)가 부여된다.

.. code-block:: xml

 <problem>
   <p>What Apple devices let you carry your digital music library in your pocket?</p>
   <multiplechoiceresponse>
    <choicegroup type="MultipleChoice" answer-pool="4">
      <choice correct="false">The iPad</choice>
      <choice correct="false">Napster</choice>
      <choice correct="true" explanation-id="iPod">The iPod</choice>
      <choice correct="false">The vegetable peeler</choice>
      <choice correct="false">The iMac</choice>
      <choice correct="true" explanation-id="iPhone">The iPhone</choice>
    </choicegroup>
   </multiplechoiceresponse>

    <solutionset>
        <solution explanation-id="iPod">
        <div class="detailed-solution">
            <p>Explanation</p>
            <p>Yes, the iPod is Apple's portable digital music player.</p>
        </div>
        </solution>
        <solution explanation-id="iPhone">
        <div class="detailed-solution">
            <p>Explanation</p>
            <p>In addition to being a cell phone, the iPhone can store and play your digital music.</p>
        </div>
        </solution>
    </solutionset>
 </problem>


.. _Multiple Choice Problem XML:

******************************
선택형 문제 XML
******************************

================
템플릿
================

.. code-block:: xml

  <problem>
  <p>Question text</p>
  <multiplechoiceresponse>
    <choicegroup type="MultipleChoice" label="label text">
      <choice correct="false" name="a">Incorrect choice</choice>
      <choice correct="true" name="b">Correct choice</choice>
    </choicegroup>
  </multiplechoiceresponse>

  <solution>
    <div class="detailed-solution">
    <p>Explanation or solution header</p>
    <p>Explanation or solution text</p>
    </div>
  </solution>
  </problem>

================
태그
================

* ``<multiplechoiceresponse>`` (필수): 해당 문제가 선다형 문제임을 나타낸다.
* ``<choicegroup>`` (필수): 선택지 목록의 시작을 나타낸다.
* ``<choice>`` (필수): 선택지를 나열한다.

**태그:** ``<multiplechoiceresponse>``

해당 문제가 선다형 문제임을 나타낸다.

  속성

  (없음)

  Children

  * ``<choicegroup>``
  * 모든 표준 HTML 태그 (텍스트 포맷에 사용)

**태그:** ``<choicegroup>``

선택지 목록의 시작을 나타낸다.

  속성

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - label (필수)
       - 답변 필드의 명칭을 지정한다.
     * - type (필수)
       - 반드시 “MultipleChoice”로 설정해야 한다.

  Children

  * ``<choice>`` 

**태그:** ``<choice>``

선택지를 나열한다.

  속성

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - correct (최소 1개 필수)
       - 정답 혹은 오답임을 나타낸다. 속성이 “true”로 지정할 경우 해당 선택지는 정답이 된다. 속성을 “false”로 지정할 경우 해당 선택지는 오답이 된다. 단 1개의 선택지가 정답이 될 수 있다.
     * - name
       - 최종 사용자가 선택지를 지칭하는 데 사용하는 고유한 명칭이다

  Children
  
  (없음)
