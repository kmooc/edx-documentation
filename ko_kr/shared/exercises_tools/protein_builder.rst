.. _Protein Builder:

############################
Protex 단백질 구성기 도구
############################

학습자는 Protex 단백질 구성기(protein builder)를 이용, 아미노산을 연결하여 특정 단백질 형상을 생성할 수 있다. 다음 예시에서 목표로 하는 단백질 구조는 1개의 단순 직선이다.


.. image:: ../../../shared/building_and_running_chapters/Images/ProteinBuilder.png
  :alt: Image of the protein builder

.. _Create the Protein Builder:

********************************
단백질 구성기 도구 만들기
********************************

단백질 구성기를 만들려면,

#. **신규 구성요소 추가** 에서  **문제** 를 클릭한 후 **BLANK ADVANCED PROBLEM** 을 클릭한다.
#. 구성요소가 생기면 **편집** 을 클릭한다.
#. 아래의 문제 구성요소 코드를 구성요소 편집기에 붙여 넣는다.
#. 어떠한 요소라도 변경한 경우 **저장** 을 클릭한다.

.. _Protein Builder Code:

*************************
단백질 구성기 도구 코드
*************************

.. code-block:: xml

  <problem>
      <p>The protein builder allows you string together the building blocks of proteins, amino acids, and see how that string will form into a structure. You are presented with a goal protein shape, and your task is to try to re-create it. In the example below, the shape that you are asked to form is a simple line.</p> 
     <p>Be sure to click "Fold" to fold your protein before you click "Check".</p>

  <script type="loncapa/python">

  def protex_grader(expect,ans):
    import json
    ans=json.loads(ans)
    if "ERROR" in ans["protex_answer"]:
      raise ValueError("Protex did not understand your answer. Try folding the protein.")
    return ans["protex_answer"]=="CORRECT"

  </script>
 
    <text>
      <customresponse cfn="protex_grader">
        <designprotein2dinput width="855" height="500" target_shape="W;W;W;W;W;W;W"/>
      </customresponse>
    </text>
    <solution>
      <p>
        Many protein sequences, such as the following example, fold to a straight line.You can play around with the protein builder if you're curious.
      </p>
      <ul>
        <li>
            Stick: RRRRRRR
        </li>
      </ul>
    </solution>
  </problem>

In this code:
 
* **width** and **height** specify the dimensions of the application, in pixels.
* **target_shape** lists the amino acids that, combined in the order specified, create the shape you've asked students to create. The list can only include the following letters, which correspond to the one-letter code for each amino acid. (This list appears in the upper-left corner of the protein builder.)

  .. list-table::
     :widths: 15 15 15 15
     :header-rows: 0

     * - A
       - R
       - N
       - D
     * - C
       - Q
       - E
       - G
     * - H
       - I
       - L
       - K
     * - M
       - F
       - P
       - S
     * - T
       - W
       - Y
       - V
