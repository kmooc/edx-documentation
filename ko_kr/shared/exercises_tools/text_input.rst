.. _Text Input:

########################
텍스트 입력 문제 
########################



텍스트 입력 문제 에서는 학습자가 응답 필드에 텍스트를 입력한다. 응답은 숫자, 문자, 그리고 구두점과 같은 특수 문자를 포함할 수 있다. 학습자가 입력한 텍스트는 철자법과 구두점 사용법을 포함, 교수자가 지정한 답과 반드시 정확히 일치해야 한다. 따라서 학습자가 오타를 낼 가능성을 고려하여 텍스트 입력 문제 에 대한 응답 기회를 2회 이상으로 지정할 것을 권고한다.

.. image:: ../../../shared/building_and_running_chapters/Images/TextInputExample.png
 :alt: Image of a text input probem

****************************
텍스트 입력 문제 생성하기
****************************

텍스트 입력 문제 는 기본 편집기 또는 고급편집기로 생성할 수 있다.

.. note:: 모든 문제는 접근성 지원 표시를 반드시 포함해야 한다. 일반적으로 접근성 지원 표시에는 문제의 주 질문지 텍스트가 포함된다. 공통 문제용 접근성 표시를 추가하려면 해당 표시의 텍스트를 꺾쇠괄호(<>)로 묶되 뾰족한 쪽이 텍스트를 향하게 한다(>>label text<<). 

==============
기본 편집기
==============

기본 편집기로 텍스트 입력 문제 를 생성하려면,

#. **신규 구성요소 추가** 에서  **문제** 를 클릭한다. 
#. **문제 구성요소 유형 선택(Select Problem Component Type)** 화면에서 **공통 문제 유형(Common Problem Types)**
   탭의 **텍스트 입력(Text Input)** 을 클릭한다. 
#. 새 문제 구성요소가 표시되면 **편집** 을 클릭한다. 
#. 기존 텍스트를 여러분의 문제로 바꾼다.
#. 접근성 지원 표시로 사용할 문제 지문을 결정한다. 이어, 해당 텍스트를 두 쌍의 꺾쇠괄호(>><<)로 묶는다. 
#. 정답 텍스트를 선택한 후 텍스트 입력 단추를 클릭한다.
   
   .. image:: ../../../shared/building_and_running_chapters/Images/ProbCompButton_TextInput.png
    :alt: Image of the text input button
   
   이 단계까지 진행하면 답 옆에 = 기호가 표시된다.
  
   
#. 구성요소 편집기에서 설명 텍스트를 선택한 후 설명 단추를 클릭하여 텍스트 주변에 설명 태그를 추가한다.  

   .. image:: ../../../shared/building_and_running_chapters/Images/ProbCompButton_Explanation.png
    :alt: Image of the explanation button

#. **설정(Settings)** 탭에서 원하는 설정값을 지정한다.  
#. **저장** 을 클릭한다. .

상기 예제의 경우 문제 구성요소 내부의 텍스트는 다음과 같다. 

::

    >>What is the technical term that refers to the fact that, when enough people 
    sleep under a bednet, the disease may altogether disappear?<<
    = herd immunity

    [explanation]
    The correct answer is herd immunity. As more and more people use bednets, 
    the risk of malaria begins to fall for everyone – users and non-users alike. 
    This can fall to such a low probability that malaria is effectively eradicated 
    from the group (even when the group does not have 100% bednet coverage).
    [explanation]

=====================
고급 편집기
=====================

고급 편집기로 텍스트 입력 문제 를 생성하는 경우 문제 구성요소 편집기에서 **고급** 탭을 클릭한 후 기존 코드를 다음 코드로 바꾼다. 

.. code-block:: xml

  <problem>
  <p>
    <em>This problem is adapted from an exercise that first appeared in MITx's 14.73x The Challenges of Global Poverty course, spring 2013.</em>
  </p>
  <p>What is the technical term that refers to the fact that, when enough people sleep under a bednet, the disease may altogether disappear?</p>
  <stringresponse answer="herd immunity" type="ci regexp">
         <additional_answer>community immunity</additional_answer>
          <additional_answer>population immunity</additional_answer>
          <textline size="20" label="What is the technical term that refers to the fact that, when enough people sleep under a bednet, the disease may altogether disappear?"/>
          <hintgroup>
              <stringhint answer="contact immunity" type="ci" name="contact_immunity_hint" />
              <hintpart on="contact_immunity_hint">
                  <startouttext />
                  In contact immunity, a vaccinated individual passes along his immunity to another person through contact with feces or bodily fluids. The answer to the question above refers to the form of immunity that occurs when so many members of a population are protected, an infectious disease is unlikely to spread to the unprotected population.
                  <endouttext />
              </hintpart >
              <stringhint answer="firewall immunity" type="ci" name="firewall_immunity_hint" />
              <hintpart on="firewall_immunity_hint">
                  <startouttext />
                  Although a firewall provides protection for a population, the term "firewall" is used more in computing and technology than in epidemiology.
                  <endouttext />
              </hintpart >
          </hintgroup>
  </stringresponse>
  <solution>
    <div class="detailed-solution">
      <p>Explanation</p>
      <p>The correct answer is <b>herd immunity</b>. As more and more people use bednets, the risk of malaria begins to fall for everyone – users and non-users alike. This can fall to such a low probability that malaria is effectively eradicated from the group (even when the group does not have 100% bednet coverage).</p>
    </div>
  </solution>
  </problem>




******************************************
텍스트 입력 문제 의 복수 응답
******************************************

텍스트 입력 문제 에서 1개 이상의 정답을 지정할 수 있다. 이를테면 “Dr. Martin Luther King, Junior”을 정확히 입력하는 대신 “Martin Luther King”이나 “Doctor Martin Luther King” 등의 기타 변형도 수용하는 것이다. 이 역시 기본 편집기나 고급 편집기로 생성할 수 있다.

==============
기본 편집기
==============

기본 편집기로 추가 정답을 지정할 경우 각 추가 정답 앞에 "or=" 를 삽입한다. (큰따옴표는 입력하지 않다.)   

::

    >>What African-American led the United States civil rights movement during the 1960s?<<
    = Dr. Martin Luther King, Jr.
    or= Dr. Martin Luther King, Junior
    or= Martin Luther King, Jr.
    or= Martin Luther King

=====================
고급 편집기
=====================

고급 편집기로 추가 정답을 지정할 경우 ``<stringresponse>`` 의 여는 태그와 닫는 태그 안쪽에서 각 추가 정답에 ``<additional_answer>`` 

.. code-block:: xml

  <problem>

  <p>What African-American led the United States civil rights movement during the 1960s?</p>
    
  <stringresponse answer="Dr. Martin Luther King, Jr." type="ci" >
    <additional_answer>Dr. Martin Luther King, Junior</additional_answer>
    <additional_answer>Martin Luther King, Jr.</additional_answer>
    <additional_answer>Martin Luther King</additional_answer>
    <textline label="What African-American led the United States civil rights movement during the 1960s?" size="20"/>
  </stringresponse>

  </problem>


******************************************
텍스트 입력 문제의 대소문자 구분
******************************************

텍스트 입력 문제 는 응답에서 대소문자를 구분하지 않는 것이 초기 설정이다. 이를 변경하여 대소문자 구분을 필수로 하는 정답을 요구할 수 있다.

텍스트 입력 응답에서 대소문자를 구분하려면 반드시 :ref:`Advanced Editor` 를 사용해야 한다.

고급 편집기에서 *대소문자를 구분하지 않는 경우* **stringresponse** 요소의 **type** 속성을 **ci** 로 한다. 이를테면 다음과 같다. 

::

    <stringresponse answer="Michigan" type="ci">
      <textline size="20"/>
    </stringresponse>

대소문자를 구분하려면 **type** 속성을 **cs**로 변경한다.

::

    <stringresponse answer="Michigan" type="cs">
      <textline size="20"/>
    </stringresponse>

*************************************************
텍스트 입력 문제 의 응답 필드 길이
*************************************************

텍스트 입력 문제 의 응답 필드 길이 초기 설정값은 20글자이다.

학습 활동을 미리보기하여 해당 응답 입력 필드 길이가 정답 기입에 충분한지 확인하고 기입 가능성이 있는 오답을 고려하여 여분의 길이를 더 주는 것이 좋다.

응답 필드 길이 초기값이 충분하지 않은 경우 :ref:`Advanced Editor` 로 이를 변경할 수 있다.

고급 편집기의 경우, 정답에 대한 XML 블록에서 **textline** 요소의 **size** 속성값은 **20** 이다. 
 
::

    <stringresponse answer="Democratic Republic of the Congo" type="ci">
      <textline size="20"/>
    </stringresponse>

To change the response field length, change the value of the **size** attribute:

::

    <stringresponse answer="Democratic Republic of the Congo" type="ci">
      <textline size="40"/>
    </stringresponse>

********************************************************
텍스트 입력 문제 의 힌트 및 정규 표현식
********************************************************

텍스트 입력 문제 에서 학습자가 흔히 예상되는 오답을 기입할 때 힌트를 표시할 수 있다. 텍스트 입력 문제 가 어떤 정규 표현식을 답으로 인정하게 할 수도 있다. 이렇게 하려면 고급 편집기에서 해당 문제 의 XML을 변경해야만 한다.


학습자가 입력하는 정규 표현식은 교수자가 지정한 정답의 일부를 반드시 포함해야 한다. 가령 교수자가  ``<answer="example answer" type="regexp">`` 을 지정한 경우 ``example answered`` , ``two example answers`` , ``==example answer==`` 등은 정답이지만 ``examples`` 나 ``example anser`` 은 정답이 아니다.

``regexp`` 을 ``type`` 속성값에 추가할 수 있다. 이를테면 ``type="ci regexp"`` , ``type="regexp"`` , ``type="regexp cs"`` . 등이 가능하다. 이 경우 어떤 답 혹은 힌트라도 정규 표현식으로 간주한다.
 
 
.. _Text Input Problem XML:

***********************
텍스트 입력 문제 XML
***********************

==============
템플릿
==============

.. code-block:: xml

  <problem>
      <p>Problem text</p>
      <stringresponse answer="Correct answer 1" type="ci regexp">
          <additional_answer>Correct answer 2</additional_answer>
          <additional_answer>Correct answer 3</additional_answer>
          <textline size="20" label="label text"/>
          <hintgroup>
              <stringhint answer="Incorrect answer A" type="ci" name="hintA" />
                <hintpart on="hintA">
                    <startouttext />Text of hint for incorrect answer A<endouttext />
                </hintpart >
              <stringhint answer="Incorrect answer B" type="ci" name="hintB" />
                <hintpart on="hintB">
                    <startouttext />Text of hint for incorrect answer B<endouttext />
                </hintpart >
              <stringhint answer="Incorrect answer C" type="ci" name="hintC" />
                <hintpart on="hintC">
                    <startouttext />Text of hint for incorrect answer C<endouttext />
                </hintpart >
          </hintgroup>
      </stringresponse>
      <solution>
      <div class="detailed-solution">
      <p>Explanation or Solution Header</p>
      <p>Explanation or solution text</p>
      </div>
    </solution>
  </problem>

=======
Tags
=======

* ``<stringresponse>`` : 텍스트 입력 문제 임을 나타낸다.
* ``<textline>`` : ``<stringresponse>`` 의 차일드. 학습자가 응답을 입력하는 LMS에 응답 필드를 생성한다. 
* ``<additional_answer>`` (선택): 문제 에 대한 추가 정답을 지정한다. 하나의 문제 가 가질 수 있는 추가 정답의 갯수는 제한이 없다.
* ``<hintgroup>`` (선택): 교수자가 흔히 발생하는 어떤 오답에 힌트를 제공했음을 나타낸다.
* ``<stringhint />`` (선택): ``<hintgroup>`` 의 차일드. 힌트를 제공할 오답의 텍스트를 지정한다. answer, type, name을 포함한다.
* ``<hintpart>`` : ``<stringhint>`` 의 name을 포함한다. 오답과 그 오답에 대한 힌트 텍스트를 조합한다. 
* ``<startouttext />`` : 힌트 텍스트의 시작을 나타낸다.
* ``<endouttext />`` : 힌트 텍스트의 끝을 나타낸다.

**태그:** ``<stringresponse>``

텍스트 입력 문제 임을 나타낸다.

  속성

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - answer (필수)
       - 정답을 지정한다. 답을 정규 표현식으로 지정하기 위해 **type** 속성에 “regexp”를 추가한다. **type** 속성에 “regexp”를 추가하지 않을 경우 학습자의 응답은 이 속성값과 반드시 정확히 일치해야 한다.  
     * - type (선택)
       - 문제 가 대소문자를 구분하는지, 그리고 정규 표현식을 허용하는지 여부를 지정할 수 있다. ``<stringresponse>`` 태그가 ``type="ci"`` 를 포함하는 경우 해당 문제 는 대소문자를 구분하지 않다. ``<stringresponse>`` 태그가 ``type="cs"`` 를 포함하는 경우 해당 문제 는 대소문자를 구분한다. ``<stringresponse>`` 태그가 ``type="regexp"`` 를 포함하는 경우 해당 문제는 정규 표현식을 허용한다. ``<stringresponse>`` 태그의 ``type`` 속성은 이들 값을 조합할 수도 있다. 가령, ``<stringresponse type="regexp cs">`` 는 해당 문제 가 정규 표현식을 허용하며 동시에 대소문자를 구분하는 것으로 규정한다.  

  Children

  * ``<textline />`` (필수)
  * ``<additional_answer>`` (선택)
  * ``<hintgroup>`` (선택)
    
**태그:** ``<textline />``
 
학습자가 응답을 입력하는 LMS에 응답 필드를 생성한다.

  속성

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - label (필수)
       - 문제의 텍스트를 포함한다.
     * - size (선택)
       - LMS의 응답란에 size 를 입력한다. 
     * - hidden (선택)
       - **true** 로 설정된 경우 학습자는 응답 필드를 볼 수 없다.
     * - correct_answer (선택)
       - 문제의 정답 목록이다.

  Children
  
  (내용 없음)

**태그:** ``<additional_answer>``

문제 에 대한 추가 정답을 지정한다. 하나의 문제 가 가질 수 있는 추가 정답의 갯수는 제한이 없다.

  속성

  (내용 없음)

  Children

  (내용 없음)

**태그:** ``<hintgroup>``

교수자가 흔히 발생하는 어떤 오답에 힌트를 제공했음을 나타낸다.

  속성

  (내용 없음)

  Children
  
  * ``<stringhint>`` (필수)

**태그:** ``<stringhint>``

해당 문제 에 흔히 발생하는 오답을 지정한다.

  속성

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - answer (필수)
       - 오답의 텍스트이다.
     * - name (필수)
       - 제공하고자 하는 힌트의 명칭이다.
     * - type
       - 특정 오답의 텍스트가 대소문자를 구분하는지 여부를 지정한다. "cs"(대소문자 구분) 또는 "ci"(대소문자 비구분)이 될 수 있다.  

  Children

  * ``<hintpart>`` (필수)

**태그:** ``<hintpart>``

오답과 그 오답에 대한 힌트 텍스트를 조합한다.

  속성

  .. list-table::
     :widths: 20 80

     * - 속성
       - 설명
     * - on
       - 힌트의 명칭. <stringhint> 태그의 **name** 속성과 반드시 동일해야 한다. ( ``<stringhint>`` 태그는 힌트의 명칭과, 그 힌트와 조합할 오답을 제공한다. ``<hintpart>`` 태그는 힌트의 명칭 및 그 힌트의 텍스트를 포함한다.)  

  Children

  * ``<startouttext />`` (required)
  * ``<endouttext />`` (required)

**태그:** ``<startouttext />`` 와 ``<endouttext>``

힌트 텍스트를 둘러싼다.

  속성
  
  (내용 없음)

  Children
  
  (내용 없음)

