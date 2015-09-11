.. _Annotation:

###################
주석 문제
###################


주석 문제에서 교수자는 텍스트 블록내의 특정 텍스트를 강조 표시한 다음, 강조된 텍스트에 대한 질문을 한다. 학습자가 강조 표시된 텍스트 위로 마우스를 움직일 때 질문이 나타난다. 또한 질문은 학습자의 응답칸과 함께 텍스트 블록 아래 부분에 나타난다.

주석 문제는 학습자가 텍스트의 특정 블록에 대한 질문에 답하도록 한다. 문제는 학습자가 읽은 질문에 대해 생각할 수 있도록 강조 표시된 텍스트 위에 마우스 커서를 이동할 때 텍스트 위에 나타난다.

.. image:: ../../../shared/building_and_running_chapters/Images/AnnotationExample.png
  :alt: Annotation problem

****************************
주석 문제 만들기
****************************

주석 문제를 만들려면 주석 고급 구성 요소를 강좌에 추가하고, **문제의 지침** 및 **토의 안내** 부분을 추가한 다음, 문제의 **주석 문제** 부분을 추가해야 한다.

#. 주석 고급 구성 요소를 추가하려면,

    #. **설정** 메뉴에서 **고급 설정** 을 선택한다.

    #. **고급 모듈 목록** 입력 필드에서, 괄호 사이에 커서를 놓는다.

    #. 다음 값을 입력한다. 인용 부호(")를 포함해야 한다.

       ``"annotatable"``

    4. 페이지의 하단에 **변경 내용 저장** 을 클릭한다.

       페이지를 자동으로 새로 고친다. 페이지의 상단에서, 변경 내용이 저장되었다는 알림을 볼 수 있다.

    5. 특수 문제를 추가하려는 학습활동으로 돌아간다. 가능한 구성 요소 목록에 이제 고급 구성 요소가 포함되어 있다.

       .. image:: ../../../shared/building_and_running_chapters/Images/AdvancedComponent.png
          :alt: Image of the Add a New Component panel with the Advanced component option

2. **문제의 지침 및 토의 안내** 부분을 추가하려면,

    #. 문제를 만들려고 하는 학습활동에서 **새 구성 요소 추가하기** 아래에 **고급** 을 클릭한다.
    #. 문제 유형 목록에서 **주석** 을 클릭한다. 
    #. 표시되는 구성 요소에서 **편집** 을 클릭한다.
    #. 구성 요소 편집기에서, 예제 코드를 본인의 코드로 바꾼다.
    #. **저장** 을 클릭한다.

3. 문제의 **주석 문제** 부분을 추가한다.

    #. 주석 구성 요소에서, 새로운 빈 고급 문제 구성 요소를 만든다.
       
    #. 고급 문제 구성 요소에서 다음 코드를 붙여 넣고 자리 표시자를 본인의 정보로 대체한다.

        .. code-block:: xml

          <problem>
              <annotationresponse>
                  <annotationinput>
                    <text>PLACEHOLDER: Text of annotation</text>
                      <comment>PLACEHOLDER: Text of question</comment>
                      <comment_prompt>PLACEHOLDER: Type your response below:</comment_prompt>
                      <tag_prompt>PLACEHOLDER: In your response to this question, which tag below 
                      do you choose?</tag_prompt>
                    <options>
                      <option choice="incorrect">PLACEHOLDER: Incorrect answer (to make this 
                      option a correct or partially correct answer, change choice="incorrect" 
                      to choice="correct" or choice="partially-correct")</option>
                      <option choice="correct">PLACEHOLDER: Correct answer (to make this option 
                      an incorrect or partially correct answer, change choice="correct" to 
                      choice="incorrect" or choice="partially-correct")</option>
                      <option choice="partially-correct">PLACEHOLDER: Partially correct answer 
                      (to make this option a correct or partially correct answer, 
                      change choice="partially-correct" to choice="correct" or choice="incorrect")
                      </option>
                    </options>
                  </annotationinput>
              </annotationresponse>
              <solution>
                <p>PLACEHOLDER: Detailed explanation of solution</p>
              </solution>
            </problem>

#. **저장**  을 클릭한다.


