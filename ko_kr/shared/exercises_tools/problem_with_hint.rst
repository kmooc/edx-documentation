.. _Problem with Adaptive Hint:

################################
응답 맞춤형 힌트가 있는 문제
################################

응답 맞춤형 힌트가 있는 문제는 학습자의 응답을 평가한 후 해당 학습자에게 피드백을 제공하거나 응답을 토대로 힌트를 주어 학습자가 다음 기회에 정답에 보다 근접하도록 한다. 이러한 유형으로는 텍스트 입력 문제가 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/ProblemWithAdaptiveHintExample.png
 :alt: Image of a problem with an adaptive hint

******************************************
응답 맞춤형 힌트가 있는 문제 생성하기
******************************************

응답 맞춤형 힌트가 있는 문제는 다음과 같은 절차로 생성한다.

#. 문제를 생성하고자 하는 학습 활동에서 **신규 구성 요소 추가**의 **문제** 를 클릭한 후 **고급** 탭을 클릭한다.
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

.. note:: If the hints that you supply include characters, the letters must be lowercase.

========
Tags
========

* ``<text>``: Surrounds the script and text in the problem.
* ``<customresponse>``: Indicates that this problem has a custom response.
* ``<textline>``: Creates a response field in the LMS where the student enters a response.
* ``<hintgroup>``: Specifies that the problem contains at least one hint.

**Tag:** ``<customresponse>``

  Attributes

  (none)

  Children

     * ``<textline>``
     * ``<hintgroup>``

**Tag:** ``<textline>``

  Attributes

  .. list-table::
     :widths: 20 80
     :header-rows: 1

     * - Attribute
       - Description
     * - label (required)
       - Contains the text of the problem.
     * - size (optional)
       - Specifies the size, in characters, of the response field in the LMS.
     * - hidden (optional)
       - If set to "true", students cannot see the response field.
     * - correct_answer (optional)
       - The answer to the problem. To supply a correct_answer value that
         includes letters, all letters **must be lowercase**. (Students'
         responses to the problem are not case sensitive. They can contain both
         uppercase and lowercase letters.)

  Children
  
  (none)

**Tag:** ``<hintgroup>``

  Attributes

  .. list-table::
     :widths: 20 80
     :header-rows: 1

     * - Attribute
       - Description
     * - hintfn
       - Must be set to **hint_fn** (that is, the tag must appear as ``<hintgroup hintfn="hint_fn"/>``).
