.. _Custom JavaScript:

###########################
사용자 정의 JavaScript 문제
###########################

사용자 지정 JavaScript표시 및 채점 문제(사용자 지정 JavaScript 문제 또는 JS 입력 문제 라고도 함)는 JavaScript를 사용하는 사용자 지정 문제 또는 도구를 만들고, 스튜디오에 직접 문제 또는 도구를 추가할 수 있도록 허용한다. JS 입력 문제를 만들 때, 스튜디오는 학습자가 LMS에서 그 문제와 상호 작용할 수 있도록 인라인 프레임 문제(IFrame)를 포함하고 있다. JavaScript와 몇 가지 기본적인 Python을 사용하여 학습자의 작업을 채점하고, 채점 결과는 edX 채점 시스템에 통합된다.

생성한 JS 입력 문제는 HTML, JavaScript 및 연속적인 스타일 시트(CSS)를 사용해야 한다. JS 입력 문제를 만들기 위해 구글 웹 툴킷 (GWT) 등과 같은 모든 응용 프로그램 제작 도구를 사용할 수 있다. 

.. image:: ../../../shared/building_and_running_chapters/Images/JavaScriptInputExample.png
 :alt: Image of a JavaScript Input problem

.. 경고:: 
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

.. NOTE:: SOP를 무시하려는 경우, **jschannel.js** 파일이 또한 필요하고, webGLDemo.html 파일은 약간 다를 것이다. .zip 파일 저장소에서 이러한 모든 파일을 다운로드 하려면 http://files.edx.org/JSInput_BypassSOP.zip로 이동한다.

#. Download and unpackage the files in either the JSInput.zip file or the JSInput_BypassSOP.zip file.
#. On the **Files & Uploads** page, upload all the files from the .zip file.
#. Create a new custom JavaScript display and grading problem component.
#. On the **Settings** tab, set **Maximum Attempts** to a number larger than
   zero.
#. In the problem component editor, replace the example code with the code below.
#. Click **Save.**

================================
JavaScript Input Problem Code
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


.. note::    When you create this problem, keep the following in mind.

 - The webGLDemo.js file defines the three JavaScript functions (**WebGLDemo.getGrade**, **WebGLDemo.getState**, and **WebGLDemo.setState**).

 - The JavaScript input problem code uses **WebGLDemo.getGrade**, **WebGLDemo.getState**, and **WebGLDemo.setState** to grade, save, or restore a problem. These functions must be global in scope.

 - **WebGLDemo.getState** and **WebGLDemo.setState** are optional. You only have to define these functions if you want to conserve the state of the problem.

 - **Width** and **height** represent the dimensions of the IFrame that holds the application.

 - When the problem opens, the cone and the cube are both blue, or "unselected." When you click either shape once, the shape becomes yellow, or "selected." To unselect the shape, click it again. Continue clicking the shape to select and unselect it.

 - The response is graded as correct if the cone is selected (yellow) when the user clicks **Check**.

 - Clicking **Check** or **Save** registers the problem's current state.


.. _JS Input Problem XML:

******************************
JavaScript Input Problem XML 
******************************

JSInput allows problem authors to turn stand-alone HTML files into problems that can be integrated into the edX platform. Since its aim is flexibility, it can be seen as the input and client-side equivalent of **CustomResponse**.

A JSInput exercise creates an IFrame in a static HTML page, and passes the return value of author-specified functions to the enclosing response type (generally **CustomResponse**). JSInput can also store and retrieve state.

========
Template
========

The following is the basic format of a JSInput problem:

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

The accepted attributes are:

==============  ==============  =========  ==========
Attribute Name   Value Type     Required   Default
==============  ==============  =========  ==========
html_file        URL string     Yes        None
gradefn          Function name  Yes        `gradefn`
set_statefn      Function name  No         None
get_statefn      Function name  No         None
height           Integer        No         `500`
width            Integer        No         `400`
==============  ==============  =========  ==========

========================
Required Attributes
========================

* **html_file**

  The **html_file** attribute specifies the HTML file that the IFrame will point to. The HTML file
  must be located in the content directory.

  The IFrame is created using the sandbox attribute. Although pop-ups, scripts, and pointer locks are allowed, the IFrame cannot access its parent's attributes.

  The HTML file must contain a **gradefn** function that the JSInput file can access. To determine whether the **gradefn** function is accessible, in the console, make sure that **gradefn** returns the right thing. When JSInput uses the **gradefn** function, `gradefn` is called with `gradefn`.call(`obj`), where **obj** is the object-part of **gradefn**. For example, if **gradefn** is **myprog.myfn**, JSInput calls **myprog.myfun.call(myprog)**. (This is to ensure "`this`" continues to refer to what `gradefn` expects.)

  Aside from that, more or less anything goes. Note that currently there is no support for inheriting CSS or JavaScript from the parent (aside from the Chrome-only **seamless** attribute, which is set to True by default).

* **gradefn**

  The **gradefn** attribute specifies the name of the function that will be called when a user clicks **Check**, and that returns the student's answer. Unless both the **get_statefn** and **set_statefn** attributes are also used, this answer is passed as a string to the enclosing response type. In the **customresponse** example above, this means **cfn** will be passed this answer as ``ans``.

  If the **gradefn** function throws an exception when a student attempts to submit a problem, the submission is aborted, and the student receives a generic alert. The alert can be customised by making the exception name ``Waitfor Exception``; in that case, the alert message will be the exception message.

  .. important:: To make sure the student's latest answer is passed correctly, make sure that the **gradefn** function is not asynchronous. Additionally, make sure that the function returns promptly. Currently the student has no indication that her answer is being calculated or produced.

========================
Optional Attributes
========================

* **set_statefn**

  Sometimes a problem author will want information about a student's previous answers ("state") to be saved and reloaded. If the attribute **set_statefn** is used, the function given as its value will be passed the state as a string argument whenever there is a state, and the student returns to a problem. The function has the responsibility to then use this state approriately.

  The state that is passed is:

  * The previous output of **gradefn** (i.e., the previous answer) if **get_statefn** is not defined.
  * The previous output of **get_statefn** (see below) otherwise.

  It is the responsibility of the iframe to do proper verification of the argument that it receives via **set_statefn**.

* **get_statefn**

  Sometimes the state and the answer are quite different. For instance, a problem that involves using a javascript program that allows the student to alter a molecule may grade based on the molecule's hydrophobicity, but from the hydrophobicity it might be incapable of restoring the state. In that case, a
  *separate* state may be stored and loaded by **set_statefn**. Note that if **get_statefn** is defined, the answer (i.e., what is passed to the enclosing response type) will be a json string with the following format:

  .. code-block:: xml

      {
          answer: `[answer string]`
          state: `[state string]`
      }


  The enclosing response type must then parse this as json.

* **height** and **width**

  The **height** and **width** attributes are straightforward: they specify the height and width of the IFrame. Both are limited by the enclosing DOM elements, so for instance there is an implicit max-width of around 900. 

  In the future, JSInput may attempt to make these dimensions match the HTML file's dimensions (up to the aforementioned limits), but currently it defaults to `500` and `400` for **height** and **width**, respectively.


