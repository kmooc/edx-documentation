.. _Write Your Own Grader:

##############################
Write-Your-Own-Grader Problem
##############################

맞춤형 Python 평가 입력(”write-your-own-grader” 문제 라고도 한다)에서 채점자는 여러분이 학습자의 응답을 평가하거나 힌트를 제공할 목적으로 생성하여 문제 내부에 임베드한 Python 스크립트를 사용한다. 이러한 문제 는 어떠한 유형이라도 취할 수 있다. “write-your-own-grader” 문제 가운데 빈도가 가장 높은 것은 수식 입력 및 텍스트 입력 문제 이다. 

.. image:: ../../../shared/building_and_running_chapters/Images/CustomPythonExample.png
 :alt: Image of a write your own grader problem

맞춤형 Python 평가 입력 문제 는 다음 항목을 포함할 수 있다.:

* :ref:`Chemical Equation`
* :ref:`Custom JavaScript`
* :ref:`Gene Explorer`
* :ref:`Molecule Editor`
* :ref:`Protein Builder`

.. list-table::
   :widths: 20 80

   * - ``<script type="loncapa/python">``
     - 문제 에 Python 스크립트가 포함돼 있음을 나타낸다.
   * - ``<customresponse cfn="test_add_to_ten">``
     - 
   * - ``<customresponse cfn="test_add" expect="20">``
     - 
   * - <textline size="10" correct_answer="3"/>
     - 이 태그는 size, correct_answer 및 label 속성을 포함한다. 단, correct_answer는 선택 속성이다.

정답 태그 포맷(Answer Tag Format) 또는 스크립트 태그 포맷(Script Tag Format) 중 어느 하나에서 이러한 유형의 문제 가운데 하나를 생성할 수 있다. :ref:`Answer Tag Format` 혹은 :ref:`Script Tag Format`.

.. _Answer Tag Format:

**************************
정답 태그 포맷
**************************

정답 태그 포맷은 Python 스크립트를 ``<answer>`` 태그로 둘러싼다:

.. code-block:: xml

  <answer>
  if answers[0] == expect:
      correct[0] = 'correct'
      overall_message = 'Good job!'
  else:
      correct[0] = 'incorrect'
      messages[0] = 'This answer is incorrect'
      overall_message = 'Please try again'
  </answer>

.. important:: 중요: Python은 들여쓰기를 준수한다.  ``<answer>`` 태그 내부의 스크립트는 반드시 들여쓰기 없이 시작해야 한다. 

Python 스크립트는 일반적으로 다음 변수들과 상호작용한다.:

* ``answers``: 학습자가 제공한 답의 순서 목록. 학습자가 답으로 ``6`` 을 입력한 경우 ``answers[0]`` 은 ``6`` 과 동일하다. 
* ``expect``: ``<customresponse>`` 의 ``expect`` 속성값. (규정된 경우)  
* ``correct``: 학습자가 질문지에 정확히 답했는지 여부를 나타내는 스트링 순서 목록. 유효한 값은 ``"correct"``, ``"incorrect"``, ``"unknown"``이다. 이들 변수를 스크립트 내부에 설정할 수 있다. 
* ``messages``: 문제 의 각 응답 필드 아래에 표시되는 메시지 순서 목록. 이 변수를 이용하여 사용자에게 힌트를 제공할 수 있다. 가령  ``messages[0] = "The capital of California is Sacramento"`` 를 입력한 경우 이 메시지가 문제 내부 응답 필드 아래에 표시된다.  
* ``overall_message``: 전체 문제 아래에 표시되는 메시지. 이 변수를 이용하여 특정 응답 필드 1개가 아니라 문제 전체에 적용되는 힌트를 제공할 수 있다.

========================================================================
정답 태그 포맷으로 맞춤형 Python 평가 입력 문제 생성하기
========================================================================

``<answer>``  태그를 이용하여 맞춤형 Python 평가 입력 문제 를 생성하기 위한 차는 다음과 같다:

#. 문제를 생성하고자 하는 학습 활동에서 **신규 구성요소 추가**의 **Problem** 를 클릭한 후 **고급** 탭을 클릭한다. 
#. 맞춤형 Python 평가 입 력**Custom Python-Evaluated Input** 을 클릭한다. 
#. 구성요소가 표시되면 **편집** 을 클릭한다.
#. 구성요소 편집기에서 기존 코드를 다음 코드로 바꾼다.
#. **저장** 을 클릭한다.

.. code-block:: xml

    <problem>
        <p>What is the sum of 2 and 3?</p>

        <customresponse expect="5">
        <textline math="1" />
        </customresponse>

        <answer>
    if answers[0] == expect:
        correct[0] = 'correct'
        overall_message = 'Good job!'
    else:
        correct[0] = 'incorrect'
        messages[0] = 'This answer is incorrect'
        overall_message = 'Please try again'
        </answer>
    </problem>

.. important:: Python은 들여쓰기를 준수한다. ``<answer>`` 태그 내부의 스크립트는 반드시 들여쓰기 없이 시작해야 한다.   

.. _Script Tag Format:

**************************
스크립트 태그 포맷
**************************

스크립트 태그 포맷은 ``<script>`` 태그 안에서 “check function”을 포함하는 Python 스크립트를 둘러싼다. 또, ``<customresponse>`` 태그의 ``cfn`` 속성을 추가하여 해당 함수를 참조한다:

.. code-block:: xml

  <problem>

  <script type="loncapa/python">

  def test_add(expect, ans):
      try:
          a1=int(ans[0])
          a2=int(ans[1])
          return (a1+a2) == int(expect)
      except ValueError:
          return False

  def test_add_to_ten(expect, ans):
      return test_add(10, ans)

  </script>

  <p>Enter two integers that sum to 10. </p>
  <customresponse cfn="test_add_to_ten">
          <textline size="10"/><br/>
          <textline size="10"/>
  </customresponse>

  </problem>

**Important**: Python은 들여쓰기를 준수한다. ``<script>`` 태그 안에서 ``def check_func(expect, ans):`` 행은 대 들여쓰지 않아야 한다.

**check** 함수는 두 가지 인자(argument)를 수용한다:

* ``expect`` ``<customresponse>`` 의 ``expect`` 속성값. (규정된 경우) 
* ``answer``:

    * 문제에 단 1개의 응답 필드가 있는 경우, 학습자가 제공하는 답의 값.
    * 문제에 복수의 응답 필드가 있는 경우, 학습자가 제공하는 답의 순서 목록.

**check** 함수는 다음 항목 중 어떤 것이라도 리턴하여 학습자의 답이 옳은지 여부를 나타낸다:
* ``True``: 학습자가 모든 응답 필드에 옳게 답했음을 나타낸다.
* ``False``: 학습자가 옳지 않게 답했음을 나타낸다. 모든 응답 필드가 옳지 않음으로 표시된다.
* 형태(form) 사전: ``{ 'ok': True, 'msg': 'Message' }``
``ok`` 에 대한 사전값이 ``True`` 로 설정된 경우 모든 응답 필드가 옳음으로 표시된다. 같은 값이 ``False`` 로 설정된 경우 모든 응답 필드가 옳지 않음으로 표시된다. ``msg`` 는 모든 응답 필드 아래에 표시되며 XHTML 마크업을 포함할 수 있다. 

* 형태 사전

.. code-block:: xml
      
    
    { 'overall_message': 'Overall message',
        'input_list': [
            { 'ok': True, 'msg': 'Feedback for input 1'},
            { 'ok': False, 'msg': 'Feedback for input 2'},
            ... ] }

마지막 형태는 복수의 응답 필드를 포함하는 응답에 유용하다. 이를 통해 각 응답 필드에 개별적으로 피드백을 제공할 수 있으며 전체 응답에 적용될 메시지를 제공할 수 있다.

판별 함수(checking function)의 예를 아래에 제시한다:

.. code-block:: python

    def check_func(expect, answer_given):
        check1 = (int(answer_given[0]) == 1)
        check2 = (int(answer_given[1]) == 2)
        check3 = (int(answer_given[2]) == 3)
        return {'overall_message': 'Overall message',
                    'input_list': [
                        { 'ok': check1, 'msg': 'Feedback 1'},
                        { 'ok': check2, 'msg': 'Feedback 2'},
                        { 'ok': check3, 'msg': 'Feedback 3'} ] }

이 함수는 사용자가 첫 번째 입력으로 ``1`` 을, 두 번째 입력으로 ``2`` 를, 세 번째 입력으로 ``3`` 을 기입했다는 사실을 확인한다. 각 개별 입력에 대한 피드백 메시지와 전체 문제 아래에 표시되는 메시지를 제공한다.  

========================================================================
스크립트 태그 포맷으로 맞춤형 Python 평가 입력 문제 생성하기
========================================================================

``<script>`` 태그를 이용하여 맞춤형 Python 평가 입력 문제 를 생성하는 차는 다음과 같다:

#. 문제를 생성하고자 하는 학습 활동에서 **신규 구성요소 추가** 의 **문제** 를 클릭한 후 **고급** 탭을 클릭한다.  
#. 맞춤형 Python **평가 입력(Custom Python-Evaluated Input)** 을 클릭한다.
#. 구성요소가 표시되면 **편집** 을 클릭한다.
#. 구성요소 편집기에서 기존 코드를 다음 코드로 바꾼다.
#. **저장** 을 클릭한다.

**문제 코드**:

.. code-block:: xml

  <problem>
  <p>This question has two parts.</p>

  <script type="loncapa/python">

  def test_add(expect, ans):
      try:
          a1=int(ans[0])
          a2=int(ans[1])
          return (a1+a2) == int(expect)
      except ValueError:
          return False

  def test_add_to_ten(expect, ans):
      return test_add(10, ans)

  </script>

  <p>Part 1: Enter two integers that sum to 10. </p>
  <customresponse cfn="test_add_to_ten">
          <textline size="10" correct_answer="3" label="Integer #1"/><br/>
          <textline size="10" correct_answer="7" label="Integer #2"/>
  </customresponse>

  <p>Part 2: Enter two integers that sum to 20. </p>
  <customresponse cfn="test_add" expect="20">
          <textline size="10" label="Integer #1"/><br/>
          <textline size="10" label="Integer #2"/>
  </customresponse>

  <solution>
      <div class="detailed-solution">
          <p>Explanation</p>
          <p>For part 1, any two numbers of the form <i>n</i> and <i>10-n</i>, where <i>n</i> is any integer, will work. One possible answer would be the pair 0 and 10.</p>
          <p>For part 2, any pair <i>x</i> and <i>20-x</i> will work, where <i>x</i> is any real number with a finite decimal representation. Both inputs have to be entered either in standard decimal notation or in scientific exponential notation. One possible answer would be the pair 0.5 and 19.5. Another way to write this would be 5e-1 and 1.95e1.</p>
      </div>
  </solution>
  </problem>

**템플릿**

다음 템플릿은 학습자가 **정답 보기(Show Answer)** 를 클릭하면 표시되는 정답을 포함하고 있다.. 

.. code-block:: xml

  <problem>

  <script type="loncapa/python">
  def test_add(expect,ans):
    a1=float(ans[0])
    a2=float(ans[1])
    return (a1+a2)== float(expect)
  </script>

  <p>Problem text</p>
  <customresponse cfn="test_add" expect="20">
          <textline size="10" correct_answer="11" label="Integer #1"/><br/>
          <textline size="10" correct_answer="9" label="Integer #2"/>
  </customresponse>

      <solution>
          <div class="detailed-solution">
            <p>Solution or Explanation Heading</p>
            <p>Solution or explanation text</p>
          </div>
      </solution>
  </problem>

다음 템플릿은 학습자가 정답 보기를 클릭해도 답을 리턴하지 않다. 학습자에게 표시되는 답을 포함하지 않는 문제인 경우 문제 구성요소에서 **정답 보기(Show Answer)** 를 **아님(Never)** 으로 설정한다. 

.. code-block:: xml

  <problem>

  <script type="loncapa/python">
  def test_add(expect,ans):
    a1=float(ans[0])
    a2=float(ans[1])
    return (a1+a2)== float(expect)
  </script>

  <p>Enter two real numbers that sum to 20: </p>
  <customresponse cfn="test_add" expect="20">
          <textline size="10"  label="Integer #1"/><br/>
          <textline size="10"  label="Integer #2"/>
  </customresponse>

      <solution>
          <div class="detailed-solution">
            <p>Solution or Explanation Heading</p>
            <p>Solution or explanation text</p>
          </div>
      </solution>
  </problem>

.. _Create a Randomized Custom Python-Evaluated Input Problem:

*****************************************************************
무작위 맞춤형 Python 평가 입력 문제 생성하기
*****************************************************************

Python 코드에서 변수를 무작위 추출하는 맞춤형 Python 평가 입력 문제를 생성할 수 있다.

.. note:: 
 문제 설정에서 반드시 **무작위 추출(Randomization)** 값을 **아님(Never)** 을 제외한 다른 값으로 지정함으로써 Python 변수를 무작위 추출할 수 있게 해야 한다.   :ref:`Randomization` 에서 보다 구체적인 정보를 확인한다. 

Python 평가 입력 문제 에서 무작위 추출을 시행하는 방법을 다음 예시에서 확인할 수 있다.

.. note::
 아래의 예시는 ``random.randint`` 방법으로 무작위 수를 만든다. Python 표준 라이브러리를 사용한다. 

.. code-block:: xml

  <problem>
    <p>Some problems in the course will utilize randomized parameters.
       For such problems, after you check your answer you will have the option 
       of resetting the question, which reconstructs the problem with a new 
       set of parameters.</p>
  <script type="loncapa/python">
  x1 = random.randint(0, 100)
  x2 = random.randint(0, 100)
  y = x1+x2
  </script>
  <p>Let (x_1 = $x1) and (x_2 = $x2). What is the value of (x_1+x_2)?</p>
  <numericalresponse answer="$y">
    <responseparam type="tolerance" default="0.01%" name="tol" 
      description="Numerical Tolerance"/>
    <textline size="10"/>
  </numericalresponse>
  <solution>
    <p><b>Explanation:</b></p>
  </solution>
  </problem>
