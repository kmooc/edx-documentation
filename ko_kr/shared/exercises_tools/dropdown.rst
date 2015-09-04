.. _Dropdown:

#####################
Dropdown 문제
#####################

드롭다운(Dropdown) 문제는 학습자가 dropdown 목록으로 표시된 답안 옵션 모음에서 답안을 선택할 수 있도록 한다. 답안이 항상 질문 바로 아래 표시되는 다중 선택 문제와는 달리, 드롭다운 문제는 학습자가 드롭다운 화살표 클릭 때까지 답안 선택안을 보여주지 않는다. 

.. image:: ../../../shared/building_and_running_chapters/Images/DropdownExample.png
 :alt: Image of a dropdown problem

********************************
Dropdown 문제 만들기
********************************

간단한 편집기 또는 고급 편집기에서 드롭다운 문제를 만들 수 있다.

.. 참고:: 모든 문제는 접근성에 대한 라벨을 포함해야 한다. 라벨은 일반적으로 문제에 있는 주요 질문의 텍스트를 포함한다. 일반적인 문제에 대한 라벨을 추가 하려면, 텍스트 향해 가리키는 꺾쇠 괄호로 라벨의 텍스트를 둘러싸야 한다 (> > 텍스트 라벨 <<).

================
간단한 편집기
================

드롭다운 문제를 만들기 위해 다음 단계를 따르도록 한다.

#.**새 구성 요소 추가하기** 에서 **문제** 를 클릭한다.
#.**문제 구성 요소 유형 선택하기** 화면에서, **일반적인 문제 유형** 탭에 있는 **드롭다운** 을 클릭한다. 
#. 표시되는 새로운 문제 구성 요소에서, **편집** 을 클릭한다.
#. 기본 텍스트를 문제에 대한 텍스트로 대체한다. 쉼표로 구분하여 같은 줄에 각각의 가능한 답안을 입력한다.
#. 라벨로 사용할 문제의 텍스트를 결정한 다음, 꺾쇠 괄호 두 세트(> > <<)로 해당 텍스트를 둘러싼다.
#. 모든 답안 옵션을 선택한 다음, 드롭다운 버튼을 클릭한다. 
      
   .. image:: ../../../shared/building_and_running_chapters/Images/ProbCompButton_Dropdown.png
    :alt: Image of the dropdown button
      
  이 작업을 수행하는 경우 대괄호 ([[])의 이중 세트가 나타나고 답안 옵션을 둘러싼다.
      
#. 대괄호 내에서, 괄호로 정답을 둘러싼다.
#. 구성 요소 편집기에서, 설명 텍스트를 선택한 다음, 텍스트 주위에 설명 태그를 추가하기 위해 설명 버튼을 클릭한다.

   .. image:: ../../../shared/building_and_running_chapters/Images/ProbCompButton_Explanation.png
    :alt: Image of the explanation button

#. **설정** 탭에서 원하는 설정을 지정한다. 
#. . **저장** 을 클릭한다.

위의 예제 문제에 대하여, 문제 구성 요소에서 텍스트는 다음과 같다.

::

    >>What type of data are the following?<<

    Age:
    [[Nominal, Discrete, (Continuous)]]
    Age, rounded to the nearest year:
    [[Nominal, (Discrete), Continuous]]
    Life stage - infant, child, and adult:
    [[(Nominal), Discrete, Continuous]]

================
고급 편집기
================

고급 편집기에서 이 문제를 만들려면, 문제 구성 요소 편집기에서 **고급** 탭을 클릭한 다음, 기존 코드를 다음의 코드로 대체한다.

**문제 코드**

.. code-block:: xml

  <problem>
  <p>
    <em>This exercise first appeared in HarvardX's PH207x Health in Numbers: Quantitative Methods in Clinical &amp; Public Health Research course, fall 2012.</em>
  </p>
  <p>What type of data are the following?</p>
  <p>Age:</p>
  <optionresponse>
    <optioninput options="('Nominal','Discrete','Continuous')" correct="Continuous" label="Age"/>
  </optionresponse>
  <p>Age, rounded to the nearest year:</p>
  <optionresponse>
    <optioninput options="('Nominal','Discrete','Continuous')" correct="Discrete" label="Age, rounded to the nearest year"/>
  </optionresponse>
  <p>Life stage - infant, child, and adult:</p>
  <optionresponse>
    <optioninput options="('Nominal','Discrete','Continuous')" correct="Nominal" label="Life stage"/>
  </optionresponse>
  </problem>

.. _Dropdown Problem XML:

************************
Dropdown 문제 XML
************************

========
템플릿
========

.. code-block:: xml

  <problem>
  <p>
    Problem text</p>
  <optionresponse>
    <optioninput options="('Option 1','Option 2','Option 3')" correct="Option 2" label="label text"/>
  </optionresponse>
    <solution>
      <div class="detailed-solution">
      <p>Explanation or Solution Header</p>
      <p>Explanation or solution text</p>
      </div>
    </solution>
  </problem>

.. code-block:: xml

  <problem>
   <p>Problem text</p>
    <optionresponse>
     options="('A','B')"
      correct="A"/>
      label="label text"
    </optionresponse>
   
    <solution>
      <div class="detailed-solution">
      <p>Explanation or Solution Header</p>
      <p>Explanation or solution text</p>
      </div>
    </solution>
  </problem>

========
태그
========

* ``<optionresponse>`` (필수 사항): 문제가 드롭다운 문제임을 나타낸다. 
* ``<optioninput>`` (필수 사항): 답안 옵션을 나열한다.

**Tag:** ``<optionresponse>``

문제가 드롭다운 문제임을 나타낸다.

  Attributes

  (none)

  Children

  * ``<optioninput>``  

**Tag:** ``<optioninput>``

답안 옵션을 나열한다.

  Attributes

  .. list-table::
     :widths: 20 80

     * - Attribute
       - Description
     * - options (required)
       - 답안 옵션을 나열한다. 모든 답안 옵션의 목록은 괄호로 둘러싸여 있다. 개별 답안 옵션은 단일 인용 부호 (')로 둘러싸여 있으며 쉼표 (,)로 구분된다.
     * - correct (required)
       - 정답인지 여부를 나타낸다. 가능한 값은 "true" 및 "false"이다. 단 하나의 **올바른** 속성을 "true"로 설정할 수 있다.
     * - label (required)
       - 응답 입력 필드의 이름을 지정한다.
  
  Children

  (none)
