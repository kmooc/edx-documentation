.. _Chemical Equation:

################################
화학 공식 문제
################################

화학 공식 문제 유형은 학습자가 화학 공식을 나타내는 텍스트를 텍스트 상자에 입력할 수 있도록 허용한다. 시스템은 해당 텍스트를 텍스트 상자 아래에 있는 화학 공식으로 변환한다. 채점자는 문제에 만들고 포함시킨 파이썬 스크립트를 사용하여 학습자의 응답을 평가한다.

.. image:: ../../../shared/building_and_running_chapters/Images/ChemicalEquationExample.png
 :alt: Image of a chemical equation response problem

************************************
화학 공식 문제 만들기
************************************

화학 공식 문제는 MathJax를 사용하여 수식을 만든다. 스튜디오에서 MathJax를 사용하는 것에 대한 자세한 내용은 :ref:`MathJax in Studio`  를 참조하도록 한다.

위의 화학 공식 문제를 만들려면

#. 문제를 만들려는 학습활동에서 **새 구성 요소 추가하기** 에서 **문제** 를 클릭한 다음, **고급** 탭을 클릭한다. 
#. **빈 고급 문제** 를 클릭한다.
#. 표시되는 구성 요소에서 **편집** 을 클릭한다.
#. 구성 요소 편집기에서 아래에서 코드를 붙여 넣는다.
#. **저장** 을 클릭한다.

==========================================
화학 공식 문제 코드 샘플
==========================================

.. code-block:: xml

  <problem>
    <startouttext/>
    <p>Some problems may ask for a particular chemical equation. Practice by writing out the following reaction in the box below.</p>
    
  \( \text{H}_2\text{SO}_4 \longrightarrow \text { H}^+ + \text{ HSO}_4^-\)

    <customresponse>
      <chemicalequationinput size="50" label="Enter the chemical equation"/>
      <answer type="loncapa/python">

  if chemcalc.chemical_equations_equal(submission[0], 'H2SO4 -> H^+ + HSO4^-'):
      correct = ['correct']
  else:
      correct = ['incorrect']

      </answer>
    </customresponse>
    <p>Some tips:</p>
    <ul>
    <li>Use real element symbols.</li>
    <li>Create subscripts by using plain text.</li>
    <li>Create superscripts by using a caret (^).</li>
    <li>Create the reaction arrow (\(\longrightarrow\)) by using "->".</li>
    </ul>

    <endouttext/>
  
   <solution>
   <div class="detailed-solution">
   <p>Solution</p>
   <p>To create this equation, enter the following:</p>
     <p>H2SO4 -> H^+ + HSO4^-</p>
   </div>
   </solution>
  </problem>

.. _Chemical Equation Problem XML:

************************************
화학 공식 문제 XML
************************************

============
템플릿
============

.. code-block:: xml

  <problem>
    <startouttext/>
    <p>Problem text</p>

    <customresponse>
      <chemicalequationinput size="NUMBER" label="LABEL TEXT"/>
      <answer type="loncapa/python">

  if chemcalc.chemical_equations_equal(submission[0], 'TEXT REPRESENTING CHEMICAL EQUATION'):
      correct = ['correct']
  else:
      correct = ['incorrect']

      </answer>
    </customresponse>

    <endouttext/>
  
   <solution>
   <div class="detailed-solution">
   <p>Solution or Explanation Header</p>
   <p>Solution or explanation text</p>
   </div>
   </solution>
  </problem>

======
태그
======

* ``<customresponse>``: 해당 문제가 사용자 지정 응답임을 나타낸다. 
* ``<chemicalequationinput>``: 해당 문제에 대한 답안은 화학 공식임을 지정한다. 
* ``<answer type=loncapa/python>``: 문제를 채점하는 파이썬 스크립트를 포함한다.

**Tag:** ``<customresponse>``

해당 문제가 사용자 지정 응답임을 나타낸다. ``<customresponse>`` 태그는 ``<chemicalequation>`` 태그를 둘러싸야 한다.

  Attributes

  (none)

  Children

  * ``<chemicalequationinput>``
  * ``<answer>``

**Tag:** ``<chemicalequationinput>``

해당 문제에 대한 답안은 화학 공식임을 지정하고 학습자가 답안을 입력하는 응답 입력 필드를 만든다.

  속성

  .. list-table::
     :widths: 20 80

     * - Attribute
       - Description
     * - 크기 
       - 문자로 넣는 응답 입력 필드의 크기를 지정한다.
     * - 라벨 (필수사항)
       - 문제에서 주요한 질문의 텍스트를 포함한다.

  Children
  
  (none)

**Tag:** ``<answer>``

문제를 채점하는 파이썬 스크립트를 포함한다.

  속성

  .. list-table::
     :widths: 20 80

     * - Attribute
       - Description
     * - 유형 (필수 사항) 
       - "Loncapa/파이썬" 이어야 한다.

  Children
  
  (none)
     
