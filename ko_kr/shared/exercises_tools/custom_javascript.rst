.. _Custom JavaScript:

###########################
사용자 정의 JavaScript 문제
###########################

사용자 지정 JavaScript표시 및 채점 문제(사용자 지정 JavaScript 문제 또는 JS 입력 문제 라고도 함)는 JavaScript를 사용하는 사용자 지정 문제 또는 도구를 만들고, 스튜디오에 직접 문제 또는 도구를 추가할 수 있도록 허용한다. JS 입력 문제를 만들 때, 스튜디오는 학습자가 LMS에서 그 문제와 상호 작용할 수 있도록 인라인 프레임 문제(IFrame)를 포함하고 있다. JavaScript와 몇 가지 기본적인 Python을 사용하여 학습자의 작업을 채점하고, 채점 결과는 K-MOOC 채점 시스템에 통합된다.

생성한 JS 입력 문제는 HTML, JavaScript 및 연속적인 스타일 시트(CSS)를 사용해야 한다. JS 입력 문제를 만들기 위해 구글 웹 툴킷 (GWT) 등과 같은 모든 응용 프로그램 제작 도구를 사용할 수 있다. 

.. image:: ../../../shared/building_and_running_chapters/Images/JavaScriptInputExample.png
 :alt: Image of a JavaScript Input problem

.. warning:: 
  하나 이상의 문제를 포함 하는 구성 요소에는 사용자 지정 JavaScript 문제를 사용할 수 없다. 각 사용자 지정 JavaScript 문제는 그 자신의 구성 요소에 있어야 한다. 더 자세한 정보는 :ref:`Multiple Problems in One Component` 를 참조하도록 한다.

************************************************************
사용자 지정 JavaScript 표시 및 채점 문제 만들기
************************************************************

#. JavaScript 응용 프로그램을 만들고 난 다음, JavaScript 응용 프로그램과 관련된 모든 파일을 **파일 업로드** 페이지로 업로드한다.
#. 문제를 만들려는 학습활동에서, **새 구성 요소 추가하기** 아래 **문제** 를 클릭하고 난 다음, **고급** 탭을 클릭한다.
#. **사용자 지정 JavaScript 표시 및 채점** 을 클릭한다.
#. 표시되는 구성요소에서, **편집** 을 클릭한다.
#. 구성요소 편집기에서, 문제에 따라 예제 코드를 수정한다.

   - 모든 문제는 하나 이상의 요소를 가져야 한다. 대부분의 문제는 동일 출처 정책 (SOP)을 따르고 있으며, 모든 요소들이 동일한 프로토콜, 호스트 및 포트를 가지고 있음을 의미한다. 예를 들어 **http**://**store.company.com**:**81**/subdirectory_1/JSInputElement.html 및 **http**://**store.company.com**:**81**/subdirectory_2/JSInputElement.js  는 동일한 프로토콜 (http), 호스트(store.company.com) 및 포트(81)를 가진다.

     문제의 어떤 요소가 다른 프로토콜, 호스트 또는 포트를 사용하는 경우 SOP를 무시해야 한다. 예를 들어 **https**://**info.company.com**/JSInputElement2.html 는 다른 프로토콜, 호스트 및 포트를 사용한다. SOP를 무시하려면, 예제 코드의 8번째 줄에서 **sop=”false”** 를 **sop=”true”** 로 변경하도록 한다. 더 자세한 내용은 `Mozilla Developer Network <https://developer.mozilla.org/en-US/docs/Web/JavaScript/Same_origin_policy_for_JavaScript>`_ 또는 `Wikipedia <http://en.wikipedia.org/wiki/Same_origin_policy>`_ 에 있는 동일 출처 정책 페이지를 참조하도록 한다.
#. 문제가 **저장** 버튼을 가지기를 원한다면, **설정** 탭을 클릭한 다음 **최대 시도 수** 를 0 보다 큰 수로 지정한다.
#. **저장** 을 클릭한다.

================================
예제 문제 다시 만들기
================================

위의 예제 문제를 다시 만들려면 다음 파일이 필요하다.

   - webGLDemo.html
   - webGLDemo.js
   - webGLDemo.css
   - three.min.js

.zip 파일 저장소에서 이러한 파일을 다운로드 하려면 http://files.edx.org/JSInput.zip로 이동한다.

.. note:: SOP를 무시하려는 경우, **jschannel.js** 파일이 또한 필요하고, webGLDemo.html 파일은 약간 다를 것이다. .zip 파일 저장소에서 이러한 모든 파일을 다운로드 하려면 http://files.edx.org/JSInput_BypassSOP.zip로 이동한다.

#. JSInput.zip 파일 또는 JSInput_BypassSOP.zip 파일을 다운로드하고 파일 압축을 푼다.
#. **파일 업로드** 페이지에서.zip 파일로부터 모든 파일을 업로드 한다.
#. 새로운 사용자 지정 JavaScript 표시 및 채점 문제 구성 요소를 만든다.
#. **설정** 탭에서 **최대 시도 수** 를 0 보다 큰 수로 설정한다.
#. 문제 구성 요소 편집기에서, 예제 코드를 아래 코드로 교체한다.
#. **저장** 을 클릭한다.

================================
JavaScript 입력 문제 코드
================================

.. code-block:: xml

    <problem display_name="webGLDemo">
    In the image below, click the cone.

    <script type="loncapa/python">
    import json
    def vglcfn(e, ans):
        '''
        par is a dictionary containing two keys, "answer" and "state"
        The value of answer is the JSON string returned by getGrade
        The value of state is the JSON string returned by getState
        '''
        par = json.loads(ans)
        # We can use either the value of the answer key to grade
        answer = json.loads(par["answer"])
        return answer["cylinder"]  and not answer["cube"]
        # Or we can use the value of the state key
        '''
        state = json.loads(par["state"])
        selectedObjects = state["selectedObjects"]
        return selectedObjects["cylinder"] and not selectedObjects["cube"]
        '''
    </script>
    <customresponse cfn="vglcfn">
        <jsinput
            gradefn="WebGLDemo.getGrade"
            get_statefn="WebGLDemo.getState"
            set_statefn="WebGLDemo.setState"
            width="400"
            height="400"
            html_file="/static/webGLDemo.html"
        />
    </customresponse>
    </problem>


.. note:: 이 문제를 만들 때 다음 사항을 기억해야 한다.

 - webGLDemo.js 파일은 세 가지 JavaScript 함수를 정의한다 ( **WebGLDemo.getGrade** , **WebGLDemo.getState** , 및 **WebGLDemo.setState** ).

 - JavaScript 입력 문제 코드는 문제 채점, 저장 또는 복원을 위해 **WebGLDemo.getGrade** , **WebGLDemo.getState** , 및 **WebGLDemo.setState** 를 사용한다. 이러한 함수는 범위가 세계적이어야 한다.

 - **WebGLDemo.getState** 와 **WebGLDemo.setState** 는 선택적이다. 문제 상태를 보존하려는 경우에만 이러한 함수를 정의해야 한다.

 - **너비** 와 **높이** 는 응용 프로그램을 보유하는 IFrame의 치수(dimension)를 나타낸다.

 - 문제를 열면, 원뿔 및 큐브는 둘다 파란색이거나 "선택되지 않은" 상태이다. 어느 모양을 한번 클릭하면, 모양이 노란색 또는 "선택된" 상태가 된다. 모양에 대한 선택 취소를 하려면. 모양을 다시 선택한다. 모양을 선택하고 취소하려면 계속 클릭한다.

 - 이용자가 **확인** 을 클릭할 때 콘이 선택되면 (노란색) 응답은 올바른 것으로 채점된다.

 - **확인** 또는 **저장** 을 클릭하면 문제의 현재 상태를 등록한다.


.. _JS Input Problem XML:

******************************
JavaScript 입력 문제 XML 
******************************

JSInput은 문제 저자(author)가 독립형 HTML 파일을 K-MOOC 플랫폼에 통합될 수 있는 문제로 바꿀 수 있도록 허용한다. JSInput 의 목표는 유연성이므로 입력 및 **CustomResponse** 의 클라이언트 쪽과 동등한 것으로 간주될 수 있다.

JSInput 연습은 정적 HTML 페이지에서 IFrame을 만들고, 저자가 지정된 함수의 반환 값을 에워싸인 응답 유형으로 (일반적으로 **CustomResponse** ) 전달한다. 또한 JSInput은 상태를 저장하고 불러 올 수 있다.

========
템플릿
========

다음은 JSInput 문제의 기본 양식이다

.. code-block:: xml

 <problem>
        <script type="loncapa/python">
 def all_true(exp, ans): return ans == "hi"
        </script>
        <customresponse cfn="all_true">
            <jsinput gradefn="gradefn" 
                height="500"
                get_statefn="getstate"
                set_statefn="setstate"
                html_file="/static/jsinput.html"/>
        </customresponse>
 </problem>

허용된 속성은

==============  ==============  =========  ==========
속성명           값 유형         필수       기본
==============  ==============  =========  ==========
html_file        URL string     예          None
gradefn          Function name  예         `gradefn`
set_statefn      Function name  아니오      None
get_statefn      Function name  아니오      None
height           Integer        아니오     `500`
width            Integer        아니오     `400`
==============  ==============  =========  ==========

========================
필수 속성 사항
========================

* **html_file**

  **html_file** 속성은 IFrame이 가리키는 HTML파일을 지정한다. HTML 파일은 콘텐츠 디렉터리에 위치해야 한다.

  IFrame은 샌드박스 속성을 사용하여 만들어진다. 팝업, 스크립트 및 포인터 잠금이 허용될지라도, IFrame은 부모의 속성에 접근할 수 없다.

  HTML 파일은 JSInput 파일이 접근할 수 있는 **gradefn** 함수를 포함해야 한다. **Gradefn** 함수가 콘솔에 접근할 수 있는지 여부를 확인하려면, **gradefn** 함수가 옳은 것을 반환하는지 확인해야 한다. JSInput이 **gradefn** 함수를 사용하는 경우, `gradefn` 는 **obj** 가 **gradefn** 의 개체 부분이 되는`gradefn` .call( `obj` )와 함께 호출된다. 예를 들어, **gradefn** 이 **myprog.myfn** 인 경우, JSInput은 **myprog.myfun.call(myprog)** 를 호출한다. (이는 " `이것` "이 `gradefn` 이 참조할 것으로 기대되는 것을 계속 언급하도록 하기 위함이다.)

  그 외에, 다소 모든 것이 가능하다. 현재는 부모로부터 CSS 또는 JavaScript를 상속 하는 것을 지원하지 않는다. (기본적으로 True로 설정되어 있는, 크롬 전용 **원활한** 속성은 예외다.).

* **gradefn**

  **gradefn** 속성에는 이용자가 **확인** 을 클릭할 때 호출되는 함수의 이름 및 학습자의 답안을 반환하는 함수의 이름을 지정한다. **get_statefn** 및 **set_statefn** 의 속성이 모두 사용되지 않는 한, 이 답안은 문자열로 에워싸인 응답 유형에 전달된다. 위의 **customresponse** 예에서, 이것은 **cfn** 이 이 함수에 대한 답을 ``ans`` 로써 전달할 것임을 의미한다.

  학습자가 문제를 제출하려고 할 때 **gradefn** 함수가 예외를 던지는 경우, 제출은 중단되고, 학습자는 일반적인 경고를 받는다. 경고는 예외 이름을 ``Waitfor Exception`` 로 만들어 사용자 지정될 수 있다; 이 경우 경고 메시지는 예외 메시지가 될 것이다

  .. important:: 학습자의 최신 답안이 제대로 전달된다는 것을 확인하려면 **gradefn** 함수가 동기화 되어 있는지 확인하도록 한다. 또한, 함수가 즉시 반환 하는지도 확인하도록 한다. 현재 학습자는 그의 답안이 계산되거나 만들어지고 있는지 아무런 표시를 가지고 있지 않다. 

========================
선택 속성 사항
========================

* **set_statefn**

  때로는 문제 저자는 학습자의 이전 답변 ("상태")에 관한 정보가 저장되고 다시 로드되기를 바랄 것이다. **set_statefn** 속성을 사용하는 경우 값으로 주어진 함수는 상태가 있을 때마다 문자열 인수로 상태가 전달 될 것이며, 학습자는 문제로 돌아가게 된다. 함수는 이 상태를 적절히 사용할 책임이 있다.

  전달 되는 상태는

  * **get_statefn** 정의 되지 않은 경우 **gradefn** 의 이전 출력 (즉, 이전 답변)이다.
  * 그렇지 않으면 **get_statefn** (아래 참조)의 이전 출력이다.

  **set_statefn** 를 통해 받는 인수의 적절한 검증을 하는 것은 iframe의 책임이다.

* **get_statefn**

  때때로 상태 및 답안은 매우 다르다. 예를 들어, 학습자에게 분자를 변경하도록 허용하는 javascript 프로그램 사용을 포함하는 문제는 분자의 hydrophobicity를 기반으로 채점될 것이지만, hydrophobicity로부터 상태 복원은 불가능할 것이다. 이 경우, *별도 상태* 는 **set_statefn** 에 의해 저장되고 로드(load)될 수 있다. 만일 **get_statefn** 이 정의되면, 답안 (즉, 에워싸인 응답 유형으로 전달되는 것)은 다음과 같은 형식을 지니는 json 문자열이 될 것이다.

  .. code-block:: xml

      {
          answer: `[answer string]`
          state: `[state string]`
      }


  에워싸인 응답 유형은 이것을 json으로 구문 분석 해야 한다.

* **height** 및  **width**

  **height** 및 **width** 속성은 간단하다: IFrame의 너비와 높이를 지정하는 것이다. 둘 다 에워싸인 DOM 요소에 의해 제한 된다. 예를 들어 약 900정도의 암시적 최대 폭이 있다. 

  미래에, JSInput는 이러한 치수가 HTML 파일의 치수와 (앞서 언급한 한도까지) 일치 하도록 시도할 수 있지만, 현재는 **height** 와 **width** 각각에 대해 `500` 및 `400` 으로 기본 설정 되어 있다.


