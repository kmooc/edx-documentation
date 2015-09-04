.. _Create Exercises:

############################
연습 및 도구 만들기
############################

************************************
연습 및 도구 소개
************************************

스튜디오는 강좌에 대해 다양한 연습 및 도구를 만들 수 있도록 허용한다. 쉽게 만들 수 있도록 스튜디오에 대부분의 연습 및 도구에 대한 템플릿이 있다. 또한, 개별 강좌 운영팀은 자주 스튜디오에 템플릿이 없는 연습을 만들기도 한다. Edx는 모든 강좌 운영팀이 이러한 도구를 이용할 수 있도록 노력하고 있으며, 본 주제에서 연습 및 도구 중 일부를 만들기 위한 지침을 제시한다

연습 또는 도구에 따라, HTML, 문제, 또는 고급 구성 요소를 사용하게 될 것이다. 각 개별 연습 또는 도구에 대한 페이지는 모든 파일, 코드 및 연습이나 도구를 만드는데 필요한 단계별 지침과 함께 각 연습 또는 도구에 대한 예제를 포함하고 있다.

.. 참고:: 
  문제는 접근성에 대한 라벨을 포함해야 한다. 라벨은 일반적으로 문제에 있는 주요 질문의 텍스트를 포함한다. 라벨 추가 지침은 각 개별 문제에 대한 페이지에 표시된다.

****************************
일반적 연습 및 도구
****************************

.. list-table::
   :widths: 25 25 50

   * - .. image:: ../../../shared/building_and_running_chapters/Images/AnnotationExample.png
          :width: 100
          :alt: Example 주석 문제
     - :ref:`Annotation`
     - 주석 문제는 학습자에게 텍스트의 특정 블록에 대한 질문에 응답하도록 요청한다. 문제는 학습자가 읽으면서 질문에 대해 생각할 수 있도록, 학습자가 강조 표시된 텍스트 위로 마우스를 이동할 때 텍스트 위에 나타난다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/PollExample.png
          :width: 100
          :alt: Example poll
     - :ref:`Conditional Module`
     -  학습자 그룹이 참조하는 콘텐츠의 버전을 제어하기 위해 조건부 모듈을 만들 수 있다. 예를 들어, 설문 조사 질문에  "예"라고 대답한 학습자는 그 질문에  "아니오" 라고 대답하는 학습자와 다른 텍스트의 블록을 참조하게 된다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/JavaScriptInputExample.png
          :width: 100
          :alt: Example JavaScript problem
     - :ref:`Custom JavaScript`
     - 사용자 지정 JavaScript 표시 및 채점 문제(사용자 지정 JavaScript 문제 또는 JS 입력 문제 라고도 함)는 JavaScript를 사용하는 사용자 지정 문제 또는 도구를 만들고, 스튜디오에 직접 문제 또는 도구를 추가할 수 있도록 허용한다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/external-grader-correct.png
          :width: 100
          :alt: Example external grader
     - :ref:`External Grader`
     - 외부 채점자(external grader)는 문제에 대한 학습자의 응답을 받고, 그 응답을 처리하고 edX 플랫폼으로 피드백과 문제 점수를 반환하는 서비스이다. edX 플랫폼과는 별도로 외부 채점자를 만들고 배포할 수 있다. 외부 채점자는 학습자가 복잡한 코드를 제출해야 하는 소프트웨어 프로그래밍 강좌에 특히 유용하다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/google-calendar.png   
          :width: 100
          :alt: Google Calendar
     - :ref:`Google Calendar Tool`
     - 학습자가 강좌 내용에서 볼 수 있도록 강좌에 구글 캘린더를 포함할 수 있다. 퀴즈 날짜, 근무 시간, 또는 학습자에게 관심이 될만한 다른 일정을 공유하기 위해 구글 캘린더를 사용할 수 있다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/google-spreadsheet.png   
          :width: 100
          :alt: Google Drive Files Tool
     - :ref:`Google Drive Files Tool`
     - 학습자가 강좌 내용(courseware)에서 볼 수 있도록 강좌에 문서, 스프레드시트, 또는 이미지 등의 구글 드라이브 파일을 포함할 수 있다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/GoogleHangout_WithPeople.png   
          :width: 100
          :alt: Google Hangout
     - :ref:`Google Instant Hangout`
     - 강좌에서 직접 인스턴트 행아웃(instant hangouts)에 참여할 수 있도록 학습자에게 능력을 부여할 수 있다. 인스턴트 행아웃(instant hangouts)을 통해, 학습자는 실시간 동영상 및 음성을 통해 상호작용하고, 화면을 공유하며 동영상을 함께 보고, 문서에 관해 공동 작업 할 수 있다. 
   * - .. image:: ../../../shared/building_and_running_chapters/Images/IFrame_1.png
          :width: 100
          :alt: Example IFrame tool
     - :ref:`IFrame`
     - 강좌에서 모든 인터넷 사이트에 있는 채점되지 않은 연습 및 도구를 HTML 구성 요소로 통합할 수 있도록 허용한다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/LTIExample.png
          :width: 100
          :alt: Example LTI component
     - :ref:`LTI Component`
     - LTI 구성 요소는 외부 학습 응용 프로그램 또는 비 PDF 교재를 스튜디오에 추가할 수 있도록 허용한다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/PA_QandRField.png
          :width: 100
          :alt: Example open response assessment
     - :ref:`Open Response Assessments 2`
     - 공개 응답 평가(open response assessments)에서, 학습자는 학습자가 업로드하는 이미지 파일 뿐만 아니라 다양한 길이의 서면 응답에 대한 피드백을 받는다. 공개 응답 평가는 자기 평가 및 동료 평가를 포함한다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/PollExample.png
          :width: 100
          :alt: Example poll
     - :ref:`Poll`
     - 강좌에서 학습자가 다른 질문에 대한 의견을 공유할 수 있도록 여론 조사를 실행할 수 있다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/ProblemWithAdaptiveHintExample.png
          :width: 100
          :alt: Example problem with adaptive hint
     - :ref:`Problem with Adaptive Hint`
     - 적응형 힌트 문제는 학습자의 응답을 평가한 후, 답안에 따라 학습자에게 피드백 또는 힌트를 준다. 그러면 학습자는 다음 시도에 올바르게 대답을 할 가능성이 많아진다. 이 문제는 텍스트 입력 또는 다중 선택 문제가 될 수 있다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/ProblemWrittenInLaTeX.png
          :width: 100
          :alt: Example problem written in LaTeX
     - :ref:`Problem Written in LaTeX`
     - 이미 라텍스에서 문제를 작성한 경우, 코드를 XML로 쉽게 변환하기 위해 이 문제 유형을 사용할 수 있다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/SFD_SN_bodyexample.png
          :width: 100
          :alt: Image of student notes in a course
     - :ref:`Student Notes Tool`
     - 학습자 주석(student notes)을 통해, 학습자는 강좌 콘텐츠에서 읽은 것과 강조한 글에 대한 주석을 만들 수 있다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/TextInputExample.png
          :width: 100
          :alt: Example text input problem
     - :ref:`Text Input`
     - 텍스트 입력 문제에서, 학습자는 응답 입력 필드에 텍스트를 입력한다. 응답은 숫자, 문자와 문장 부호와 같은 특수 문자를 포함할 수 있다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/WordCloudExample.png
          :width: 100
          :alt: Example word cloud
     - :ref:`Word Cloud`
     - 워드 클라우드는 예를 들어 질문에 대한 응답처럼 학습자가 입력한 텍스트를 학습자가 볼 수 있는 화려한 그래픽으로 정렬한다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/CustomPythonExample.png  
          :width: 100
          :alt: Example write-your-own-grader problem
     - :ref:`Write Your Own Grader`
     - 사용자 지정 파이썬 평가 입력 문제 (또한 “스스로 채점을 작성하는 문제")에서, 채점자 (grader)는 학습자의 응답을 평가하거나 힌트를 제공하기 위해 만들고 문제에 포함시킨 파이썬 스크립트를 사용한다. 이 문제는 모든 종류가 될 수 있다.


********************************
이미지 기반 연습 및 도구
********************************

.. list-table::
   :widths: 30 25 80

   * - .. image:: ../../../shared/building_and_running_chapters/Images/DragAndDropProblem.png
          :width: 100
          :alt: Example drag and drop problem
     - :ref:`Drag and Drop`
     - 끌어서 놓기 문제(drag and drop problems)에서, 학습자는 이미지에 특정 위치에 텍스트 또는 개체를 드래그하여 질문에 답한다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/image-modal.png
          :width: 100
          :alt: Example full screen image tool
     - :ref:`Full Screen Image`
     - The Full Screen Image tool allows a student to enlarge an image in the
       whole browser window. This is useful when the image contains a large
       amount of detail and text that is easier to view in context when
       enlarged.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/ImageMappedInputExample.png
          :width: 100
          :alt: Example image mapped input problem
     - :ref:`Image Mapped Input`
     - In an image mapped input problem, students click inside a defined area
       in an image. You define this area by including coordinates in the body
       of the problem.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/Zooming_Image.png
          :width: 100
          :alt: Example zooming image tool
     - :ref:`Zooming Image`
     - Zooming images allow you to enlarge sections of an image so that
       students can see the section in detail.

************************************
Multiple Choice Exercises and Tools
************************************

.. list-table::
   :widths: 30 25 80

   * - .. image:: ../../../shared/building_and_running_chapters/Images/CheckboxExample.png
          :width: 100
          :alt: Example checkbox problem
     - :ref:`Checkbox`
     - In checkbox problems, the student selects one or more options from a
       list of possible answers. The student must select all the options that
       apply to answer the problem correctly.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/DropdownExample.png
          :width: 100
          :alt: Example dropdown problem
     - :ref:`Dropdown`
     - Dropdown problems allow the student to choose from a collection of
       answer options, presented as a dropdown list. Unlike multiple choice
       problems, whose answers are always visible directly below the question,
       dropdown problems don't show answer choices until the student clicks the
       dropdown arrow.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/MultipleChoiceExample.png
          :width: 100
          :alt: Example multiple choice problem
     - :ref:`Multiple Choice`
     - In multiple choice problems, students select one option from a list of
       answer options. Unlike with dropdown problems, whose answer choices
       don't appear until the student clicks the drop-down arrow, answer
       choices for multiple choice problems are always visible directly below
       the question.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/MultipleChoice_NumericalInput.png
          :width: 100
          :alt: Example multiple choice and numerical input problem
     - :ref:`Multiple Choice and Numerical Input`
     - You can create a problem that combines a multiple choice and numerical
       input problems. Students not only select a response from options that
       you provide, but also provide more specific information, if necessary.

********************************
STEM Exercises and Tools
********************************

.. list-table::
   :widths: 30 25 80

   * - .. image:: ../../../shared/building_and_running_chapters/Images/ChemicalEquationExample.png
          :width: 100
          :alt: Example chemical equation problem
     - :ref:`Chemical Equation`
     - Chemical equation problems allow the student to enter text that
       represents a chemical equation into a text box. The grader evaluates the
       student's response by using a Python script that you create and embed in
       the problem.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/CircuitSchematicExample_short.png
          :width: 100
          :alt: Example circuit schematic builder problem
     - :ref:`Circuit Schematic Builder`
     - In circuit schematic builder problems, students can arrange circuit
       elements such as voltage sources, capacitors, resistors, and MOSFETs on
       an interactive grid. They then submit a DC, AC, or transient analysis of
       their circuit to the system for grading.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/GeneExplorer.png
          :width: 100
          :alt: Example gene explorer problem
     - :ref:`Gene Explorer`
     - The Gene Explorer (GeneX) simulates the transcription, splicing,
       processing, and translation of a small hypothetical eukaryotic gene.
       GeneX allows students to make specific mutations in a gene sequence, and
       it then calculates and displays the effects of the mutations on the mRNA
       and protein.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/MathExpressionInputExample.png
          :width: 100
          :alt: Example math expression input problem
     - :ref:`Math Expression Input`
     - The more complex of Studio's two types of math problems. In math
       expression input problems, students enter mathematical expressions to
       answer a question. These problems can include unknown variables and more
       complex symbolic expressions. You can specify a correct answer either
       explicitly or by using a Python script.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/Molecule_Editor.png
          :width: 100
          :alt: Example molecule editor problem
     - :ref:`Molecule Editor`
     - The molecule editor allows students to draw molecules that follow the
       rules for covalent bond formation and formal charge, even if the
       molecules are chemically impossible, are unstable, or do not exist in
       living systems.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/MoleculeViewer.png
          :width: 100
          :alt: Example molecule viewer tool
     - :ref:`Molecule Viewer`
     - The molecule viewer allows you to create three-dimensional representations of molecules for students to view.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/image292.png
          :width: 100
          :alt: Example numerical input problem
     - :ref:`Numerical Input`
     - The simpler of Studio's two types of math problems. In numerical input
       problems, students enter numbers or specific and relatively simple
       mathematical expressions to answer a question. These problems only allow
       integers and a few select constants. You can specify a margin of error,
       and you can specify a correct answer either explicitly or by using a
       Python script.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/Periodic_Table.png
          :width: 100
          :alt: Example periodic table problem
     - :ref:`Periodic Table`
     - An interactive periodic table of the elements shows detailed information
       about each element as the student moves the mouse over the element.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/ProteinBuilder.png
          :width: 100
          :alt: Example protein builder problem
     - :ref:`Protein Builder`
     - The Protex protein builder asks students to create specified protein
       shapes by stringing together amino acids.
