.. _Problem with Adaptive Hint:

################################
응답 맞춤형 힌트가 있는 문제
################################

응답 맞춤형 힌트가 있는 문제는 학습자의 응답을 평가한 후 해당 학습자에게 피드백을 제공하거나 응답을 바탕으로 힌트를 주어 학습자가 다음 기회에 정답에 보다 근접하도록 한다. 이러한 유형으로는 텍스트 입력 문제가 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/ProblemWithAdaptiveHintExample.png
 :alt: Image of a problem with an adaptive hint

******************************************
응답 맞춤형 힌트가 있는 문제 생성하기
******************************************

응답 맞춤형 힌트가 있는 문제는 다음과 같은 절차로 생성한다.

#. 문제를 생성하고자 하는 학습 활동에서 **신규 구성 요소 추가** 의 **문제** 를 클릭한 후 **고급** 탭을 클릭한다.
#. **응답 맞춤형 힌트가 있는 문제** 를 클릭한다.
#. 구성요소가 표시되면 **편집** 을 클릭한다.
#. 구성요소 편집기에서 기존 코드를 삭제하고 아래 코드를 입력한다.
#. **저장** 을 클릭한다.

.. code-block:: xml

    <problem>
	    <text>
	        <script type="text/python" system_path="python_lib">
	def test_str(expect, ans):
	  print expect, ans
	  ans = ans.strip("'")
	  ans = ans.strip('"')
	  return expect == ans.lower()

	def hint_fn(answer_ids, student_answers, new_cmap, old_cmap):
	  aid = answer_ids[0]
	  ans = str(student_answers[aid]).lower()
	  print 'hint_fn called, ans=', ans
	  hint = ''
	  if '10' in ans:
	     hint = 'If the ball costs 10 cents, and the bat costs one dollar more than the ball, how much does the bat cost? If that is the cost of the bat, how much do the ball and bat cost together?'
	  elif '.05' in ans:
	     hint = 'Make sure to enter the number of cents as a whole number.'

	  if hint:
	    hint = "&lt;font color='blue'&gt;Hint: {0}&lt;/font&gt;".format(hint)
	    new_cmap.set_hint_and_mode(aid,hint,'always')
	        </script>
	        <p>If a bat and a ball cost $1.10 together, and the bat costs $1.00 more than the ball, how much does the ball cost? Enter your answer in cents, and include only the number (that is, do not include a $ or a ¢ sign).</p>
	        <p>
	            <customresponse cfn="test_str" expect="5">
	                <textline correct_answer="5" label="How much does the ball cost?"/>
	                <hintgroup hintfn="hint_fn"/>
	            </customresponse>
	        </p>
	    </text>
    </problem>

.. _Problem with Adaptive Hint XML:

*********************************
응답 맞춤형 힌트 XML이 있는 문제
*********************************

========
템플릿
========

.. code-block:: xml

	<problem>
	  <text>
	    <script type="text/python" system_path="python_lib">
	def test_str(expect, ans):
	  print expect, ans
	  ans = ans.strip("'")
	  ans = ans.strip('"')
	  return expect == ans.lower()

	def hint_fn(answer_ids, student_answers, new_cmap, old_cmap):
	  aid = answer_ids[0]
	  ans = str(student_answers[aid]).lower()
	  print 'hint_fn called, ans=', ans
	  hint = ''
	  if 'incorrect answer 1' in ans:
	     hint = 'hint for incorrect answer 1'
	  elif 'incorrect answer 2' in ans:
	     hint = 'hint for incorrect answer 2'

	  if hint:
	    hint = "&lt;font color='blue'&gt;Hint: {0}&lt;/font&gt;".format(hint)
	    new_cmap.set_hint_and_mode(aid,hint,'always')
	</script>
	    <p>TEXT OF PROBLEM</p>
	    <p>
	      <customresponse cfn="test_str" expect="ANSWER">
	        <textline correct_answer="answer" label="LABEL TEXT"/>
	        <hintgroup hintfn="hint_fn"/>
	      </customresponse>
	    </p>
	  </text>
	</problem>

.. note:: 힌트에서 영어 문자는 소문자로만 주어져야 한다. 

========
Tags
========

* ``<text>``: 문제에서 스크립트와 텍스트를 감싸는 태그이다.
* ``<customresponse>``: 문제가 맞춤형(custom) 응답이 있음을 의미한다. 
* ``<textline>``: 학습자가 응답을 입력할 수 있는 입력칸을 만든다.
* ``<hintgroup>``: 최소 1개의 힌트가 있는 문제를 나타낸다.

**Tag:** ``<customresponse>``

  속성

  (내용 없음)

  Children

     * ``<textline>``
     * ``<hintgroup>``

**Tag:** ``<textline>``

  속성

  .. list-table::
     :widths: 20 80
     :header-rows: 1

     * - 속성
       - 설명
     * - label (필수)
       - 문제의 텍스트를 포함.
     * - size (선택)
       - LMS 에서 응답칸에 입력받는 글자의 수를 나타낸다. 
     * - hidden (선택)
       - "true" 로하게 되면 학습자는 응답칸을 볼 수 없다. 
     * - correct_answer (선택)
       - 문제의 답. correct_answer 값을 지원하기 위해 문자를 포함하고, 모든 문자는 영어라면 **소문자라야한다**. 
         학습자의 응답은 대소문자에 민감하지 않다. 대소문자 모두 포함할 수 있다. 

  Children
  
  (내용 없음)

**Tag:** ``<hintgroup>``

  속성

  .. list-table::
     :widths: 20 80
     :header-rows: 1

     * - 속성
       - 설명
     * - hintfn
       - **hint_fn** 로 설정해야 한다. (즉, ``<hintgroup hintfn="hint_fn"/>`` 로 나타나야 한다).
