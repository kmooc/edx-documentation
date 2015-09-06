.. _Checkbox:

##################
체크박스 문제
##################

체크박스 문제에서, 학습자는 가능한 답변 목록에서 하나 이상을 선택해야 한다. 또한 각 체크박스 문제에는 1개 이상의 정답이 있어야 한다.

.. image:: ../../../shared/building_and_running_chapters/Images/CheckboxExample.png
 :alt: Image of a checkbox problem

****************************
체크박스 문제 만들기
****************************

간단한 편집기 또는 고급 편집기에서 체크박스 문제를 만들 수 있다.

.. 참고:: 모든 문제는 접근성에 대한 라벨을 포함해야 한다. 라벨은 일반적으로 문제에서 주요 질문에 대한 텍스트를 포함한다. 일반적인 문제에 라벨을 추가하려면, 텍스트를 향해 지적하는 꺾쇠 괄호 (> > 텍스트 라벨 <<)를 가지고 라벨의 텍스트를 둘러싸도록 한다.

==================
간단한 편집기
==================

#. **새 구성 요소 추가하기** 에서 **문제** 를 클릭한다.
#. **문제 구성 요소 유형 선택하기** 화면에서, **일반적인 문제 유형** 탭에서 **체크박스** 를 클릭한다.
#. 표시되는 문제 구성 요소에서 **편집** 을 클릭한다.
#. 구성 요소 편집기에서 기본 텍스트를 본인의 텍스트로 대체한다. 각 자체 줄에 답안 옵션을 입력한다.
#. 라벨로 사용할 문제의 텍스트를 결정한 다음, 괄호 두 세트(> > <<)로 해당 텍스트를 둘러싼다.
#. 모든 답안 옵션을 선택한 다음, 체크박스 버튼을 클릭한다. 

   .. image:: ../../../shared/building_and_running_chapters/Images/ProbComponent_CheckboxIcon.png
    :alt: Image of the checkbox button
   
   이렇게 할 때, 각 답안 선택 옆에 괄호가 표시된다.

#. 정답 또는 답안에 대한 괄호 사이에 **x** 를 추가한다.
#. 구성 요소 편집기에서, 설명 텍스트를 선택하고 난 다음, 텍스트 주변에 설명 태그를 추가하기 위해 설명 버튼을 클릭한다.

   .. image:: ../../../shared/building_and_running_chapters/Images/ProbCompButton_Explanation.png
    :alt: Image of the explanation button

#. **설정** 탭에서 원하는 설정을 지정한다. 
#. **저장**을 클릭한다. 

위의 예제 문제에 대하여, 문제 구성 요소에 텍스트는 다음과 같다.

.. code-block:: xml

    Learning about the benefits of preventative healthcare can be particularly 
    difficult. >>Check all of the reasons below why this may be the case.<<

    [x] A large amount of time passes between undertaking a preventative measure and seeing the result. 
    [ ] Non-immunized people will always fall sick. 
    [x] If others are immunized, fewer people will fall sick regardless of a particular individual's choice to get immunized or not. 
    [x] Trust in healthcare professionals and government officials is fragile. 

    [explanation]
    People who are not immunized against a disease may still not fall sick from the disease. If someone is trying to learn whether or not preventative measures against the disease have any impact, he or she may see these people and conclude, since they have remained healthy despite not being immunized, that immunizations have no effect. Consequently, he or she would tend to believe that immunization 
    (or other preventative measures) have fewer benefits than they actually do.
    [explanation]

==================
고급 편집기
==================

고급 편집기에서 체크박스 문제를 만들려면, 문제 구성 요소 편집기에서 **고급**  탭을 클릭하고 난 다음, 기존 코드를 다음 코드로 대체한다.

.. code-block:: xml

  <problem>
    <p>Learning about the benefits of preventative healthcare can be particularly difficult. Check all of the reasons below why this may be the case.</p>

  <choiceresponse>
    <checkboxgroup direction="vertical" label="Check all of the reasons below why this may be the case">
      <choice correct="true"><text>A large amount of time passes between undertaking a preventative measure and seeing the result.</text></choice>
      <choice correct="false"><text>Non-immunized people will always fall sick.</text></choice>
      <choice correct="true"><text>If others are immunized, fewer people will fall sick regardless of a particular individual's choice to get immunized or not.</text></choice>
      <choice correct="true"><text>Trust in healthcare professionals and government officials is fragile.</text></choice>
    </checkboxgroup>
  </choiceresponse>

   <solution>
   <div class="detailed-solution">
   <p>Explanation</p>
   <p>People who are not immunized against a disease may still not fall sick from the disease. If someone is trying to learn whether or not preventative measures against the disease have any impact, he or she may see these people and conclude, since they have remained healthy despite not being immunized, that immunizations have no effect. Consequently, he or she would tend to believe that immunization (or other preventative measures) have fewer benefits than they actually do.</p>
   </div>
   </solution>
  </problem>

.. _Checkbox Problem XML:

****************************
체크박스박스 문제 XML 
****************************

============
템플릿
============

.. code-block:: xml

  <problem>
    <p>Question text</p>

  <choiceresponse>

  <checkboxgroup direction="vertical" label="label text">
  <choice correct="false"><text>Answer option 1 (incorrect)</text></choice>
  <choice correct="true"><text>Answer option 2 (correct)</text></choice>
  </checkboxgroup>
  </choiceresponse>

   <solution>
   <div class="detailed-solution">
   <p>Solution or Explanation Heading</p>
   <p>Solution or explanation text</p>
   </div>
   </solution>

  </problem>

======
태그
======

* ``<choiceresponse>`` (필수사항): 문제가 학습자들이 선택할 수 있는 옵션을 포함하도록 지정한다.
* ``<checkboxgroup>`` (필수사항): 문제가 체크박스 문제임을 지정한다.
* ``<choice>`` (필수사항): 답안 옵션을 지정한다

**Tag:** ``<choiceresponse>``

문제가 학습자들이 선택할 수 있는 옵션을 포함하도록 지정한다.

  Attributes

  (none)

  Children

  * ``<checkboxgroup>``

**Tag:** ``<checkboxgroup>``

. 문제가 체크박스 문제임을 지정한다.

  Attributes

  .. list-table::
     :widths: 20 80

     * - Attribute
       - Description
     * - direction (optional)
       - 답안 목록 방향을 지정한다. 기본값은 수직이다.
     * - label (required)
       - 응답 입력 필드의 이름을 지정한다.

  Children

  * ``<choice>`` 

**Tag:** ``<choice>``

답안 옵션을 지정한다.

  Attributes

  .. list-table::
     :widths: 20 80

     * - Attribute
       - Description
     * - true (at least one required)
       - 정답을 나타낸다. 체크박스 문제에 대하여, 하나 이상의 ``<choice>`` 태그는 정답을 포함할 수 있다.
     * - false (at least one required)
       - 오답을 나타낸다.

  Children
  
  (none)
