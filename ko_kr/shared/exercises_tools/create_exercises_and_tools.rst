.. _Create Exercises:

############################
연습문제 및 도구 만들기
############################

************************************
연습문제 및 도구 소개
************************************

Studio에서 강좌에 활용할 다양한 연습문제 및 도구를 만들 수 있다. 쉽게 만들 수 있도록 Studio에 대부분의 연습문제 및 도구에 대한 템플릿이 있다. 이 장에서는 연습문제 및 도구를 만드는 방법을 다룬다.

연습문제 또는 도구에 따라 적절한 HTML, 문제, 또는 고급 구성 요소 중 하나를 사용하게 될 것이다. 각 연습문제 또는 도구에 대한 페이지는 모든 파일, 코드 및 연습이나 도구를 만드는데 필요한 단계별 지침과 함께 각 연습문제 또는 도구에 대한 예제를 포함하고 있다.

.. 참고:: 
  문제는 접근성 라벨을 포함해야 한다. 라벨은 일반적으로 문제에 있는 주요 질문의 텍스트를 포함한다. 라벨 추가 지침은 각 개별 문제에 대한 페이지에 표시된다.

****************************
일반적 연습문제 및 도구
****************************

.. list-table::
   :widths: 25 25 50

   * - .. image:: ../../../shared/building_and_running_chapters/Images/AnnotationExample.png
          :width: 100
          :alt: Example Annotation problem
     - :ref:`Annotation`
     - 주석 문제는 학습자에게 텍스트의 특정 블록에 대한 질문에 대해 답변하도록 요청한다. 학습자가 읽으면서 질문에 대해 생각할 수 있도록, 학습자가 강조 표시된 텍스트 위로 마우스를 이동할 때 문제가 텍스트 위에 나타난다.
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
     - 외부 채점자는 문제에 대한 학습자의 응답을 받아 처리한 후, K-MOOOC 플랫폼으로 피드백과 문제 점수를 전달하는 서비스이다. K-MOOC 플랫폼과는 별도로 외부 채점자를 만들고 배포할 수 있다. 외부 채점자는 학습자가 복잡한 코드를 제출해야 하는 소프트웨어 프로그래밍 강좌에 특히 유용하다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/google-calendar.png   
          :width: 100
          :alt: Google Calendar
     - :ref:`Google Calendar Tool`
     - 학습자가 강좌 내용에서 볼 수 있도록 강좌에 구글 캘린더를 포함할 수 있다. 퀴즈 날짜, 근무 시간, 또는 학습자에게 관심이 될만한 다른 일정을 공유하기 위해 구글 캘린더를 사용할 수 있다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/google-spreadsheet.png   
          :width: 100
          :alt: Google Drive Files Tool
     - :ref:`Google Drive Files Tool`
     - 학습자가 강좌 내용에서 볼 수 있도록 강좌에 문서, 스프레드시트, 또는 이미지 등의 구글 드라이브 파일을 포함할 수 있다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/GoogleHangout_WithPeople.png   
          :width: 100
          :alt: Google Hangout
     - :ref:`Google Instant Hangout`
     - 강좌에서 직접 인스턴트 행아웃(instant hangouts)에 참여할 수 있도록 학습자에게 능력을 부여할 수 있다. 인스턴트 행아웃을 통해, 학습자는 실시간 동영상 및 음성을 통해 상호작용하고, 화면을 공유하며 동영상을 함께 보고, 문서에 관해 공동 작업 할 수 있다. 
   * - .. image:: ../../../shared/building_and_running_chapters/Images/IFrame_1.png
          :width: 100
          :alt: Example IFrame tool
     - :ref:`IFrame`
     - 강좌에서 모든 인터넷 사이트에 있는 채점되지 않은 연습 및 도구를 HTML 구성 요소로 통합할 수 있도록 허용한다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/LTIExample.png
          :width: 100
          :alt: Example LTI component
     - :ref:`LTI Component`
     - LTI 구성 요소는 외부 학습 응용 프로그램 또는 비 PDF 교재를 Stuio에 추가할 수 있도록 허용한다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/PA_QandRField.png
          :width: 100
          :alt: Example open response assessment
     - :ref:`Open Response Assessments 2`
     - 개방형 평가(open response assessments)에서, 학습자는 학습자가 업로드하는 이미지 파일 뿐만 아니라 다양한 길이의 서면 응답에 대한 피드백을 받는다. 개방형 평가는 자기 평가 및 상호 평가를 포함한다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/PollExample.png
          :width: 100
          :alt: Example poll
     - :ref:`Poll`
     - 강좌에서 학습자가 다른 질문에 대한 의견을 공유할 수 있도록 설문조사를 시행할 수 있다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/ProblemWithAdaptiveHintExample.png
          :width: 100
          :alt: Example problem with adaptive hint
     - :ref:`Problem with Adaptive Hint`
     - 응답 맞춤형 힌트 문제는 학습자의 응답을 평가한 후, 답안에 따라 학습자에게 피드백 또는 힌트를 준다. 그러면 학습자는 다음 시도에 올바르게 대답을 할 가능성이 많아진다. 이 문제는 텍스트 입력 또는 다중 선택 문제가 될 수 있다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/ProblemWrittenInLaTeX.png
          :width: 100
          :alt: Example problem written in LaTeX
     - :ref:`Problem Written in LaTeX`
     - 이미 LaTex에서 문제를 작성한 경우, 코드를 XML로 쉽게 변환하기 위해 이 문제 유형을 사용할 수 있다.
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
     - 사용자 지정 Python 평가 입력 문제 (또한 “스스로 채점을 작성하는 문제")에서, 채점자는 학습자의 응답을 평가하거나 힌트를 제공하기 위해 만들고 문제에 포함시킨 Python 스크립트를 사용한다. 


********************************
이미지 기반 연습문제 및 도구
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
     - 전체 화면 이미지 도구는 학습자가 전체 브라우저 창에 이미지를 확대할 수 있도록 허용한다. 확대했을 때 더 보기 쉬운 많은 양의 세부 사항 및 텍스트를 포함하는 이미지를 볼 때 유용하다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/ImageMappedInputExample.png
          :width: 100
          :alt: Example image mapped input problem
     - :ref:`Image Mapped Input`
     - 이미지가 그려진 입력 문제에서, 학습자는 이미지에서 정의된 영역의 내부를 클릭한다. 문제의 본문에서 좌표를 포함함으로써 이 영역을 정의할 수 있다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/Zooming_Image.png
          :width: 100
          :alt: Example zooming image tool
     - :ref:`Zooming Image`
     - . 이미지 확대는 학습자가 해당 부분을 자세히 볼 수 있도록 이미지의 부분을 확대할 수 있도록 허용한다. 

************************************
다양한 유형의 연습문제 및 도구
************************************

.. list-table::
   :widths: 30 25 80

   * - .. image:: ../../../shared/building_and_running_chapters/Images/CheckboxExample.png
          :width: 100
          :alt: Example checkbox problem
     - :ref:`Checkbox`
     - 체크박스 문제에서, 학습자는 가능한 답안 목록에서 하나 이상의 옵션을 선택한다. 학습자는 문제에 대해 올바르게 대답하기 위해 적용되는 모든 옵션을 선택해야 한다
   * - .. image:: ../../../shared/building_and_running_chapters/Images/DropdownExample.png
          :width: 100
          :alt: Example dropdown problem
     - :ref:`Dropdown`
     - 드롭다운 문제는 학습자가 드롭다운 목록으로 제공된 답안 옵션 모음에서 선택할 수 있도록 허용한다. 답안이 항상 질문 바로 아래 표시되는 다중 선택 문제와는 달리, 드롭다운 문제는 학습자가 드롭다운 화살표를 클릭할 때까지 답안 선택을 표시하지 않는다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/MultipleChoiceExample.png
          :width: 100
          :alt: Example multiple choice problem
     - :ref:`Multiple Choice`
     - 선다형 문제에서, 학습자는 답안 옵션 목록에서 하나의 옵션을 선택한다. 학습자가 드롭다운 화살표를 클릭할 때까지 답안 선택이 표시되지 않는 드롭다운 문제와는 달리, 선다형 문제에 대한 답안 선택은 항상 질문 바로 아래 표시된다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/MultipleChoice_NumericalInput.png
          :width: 100
          :alt: Example multiple choice and numerical input problem
     - :ref:`Multiple Choice and Numerical Input`
     - 선다형 및 숫자 입력 문제를 결합한 문제를 만들 수 있다. 학습자는 제공하는 옵션에서 응답을 선택할 수 있을 뿐만 아니라, 필요한 경우 더 자세한 정보를 제공할 수 있다. 

********************************
STEM 연습 및 도구
********************************

.. list-table::
   :widths: 30 25 80

   * - .. image:: ../../../shared/building_and_running_chapters/Images/ChemicalEquationExample.png
          :width: 100
          :alt: Example chemical equation problem
     - :ref:`Chemical Equation`
     - 화학 공식 문제는 학습자가 화학 공식을 나타내는 텍스트를 텍스트 상자에 입력할 수 있도록 허용한다. 채점자는 만들고 문제에 포함시킨 Python 스크립트를 사용하여 학습자의 응답을 평가한다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/CircuitSchematicExample_short.png
          :width: 100
          :alt: Example circuit schematic builder problem
     - :ref:`Circuit Schematic Builder`
     - 회로도 문제에서 학습자는 인터랙티브 그리드(interactive grid)위에 전압 소스, 커패시터, 저항, MOSFETs 등 회로 요소를 나열할 수 있다. 그런 다음, 채점을 위해 회로에 대한 DC, AC, 또는 과도기 분석 결과를 시스템에 제출한다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/GeneExplorer.png
          :width: 100
          :alt: Example gene explorer problem
     - :ref:`Gene Explorer`
     - GeneX는 전사, 접합, 처리, 및 작은 가상 진핵 유전자의 번역을 시뮬레이션 한다. GeneX는 학습자가 유전자 시퀀스에 특정 돌연변이 만들 수 있도록 허용하며, mRNA와 단백질에 미치는 돌연변이의 효과를 계산하고 표시한다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/MathExpressionInputExample.png
          :width: 100
          :alt: Example math expression input problem
     - :ref:`Math Expression Input`
     - 스튜디오에 있는 두 가지 유형의 수학 문제 중에 더 복잡한 유형이다. 수학 공식 입력 문제에서, 학습자는 질문에 답하기 위해 수학 공식을 입력한다. 이 문제는 알 수 없는 변수와 더 복잡한 기호식을 포함할 수 있다. 명시적으로 또는 Python 스크립트를 사용하여 정답을 지정할 수 있다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/Molecule_Editor.png
          :width: 100
          :alt: Example molecule editor problem
     - :ref:`Molecule Editor`
     - 분자 편집기는 분자가 화학적으로 불가능하거나, 불안정하거나, 또는 살아있는 시스템에 존재하지 않는 경우라 할지라도, 학습자가 공유 결합 형성 및 형식 전하에 대한 규칙에 따라 분자를 그릴 수 있도록 허용한다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/MoleculeViewer.png
          :width: 100
          :alt: Example molecule viewer tool
     - :ref:`Molecule Viewer`
     - 분자 보기(molecule viewer)를 사용하면 학습자가 분자의 3차원 묘사를 볼 수 있도록 만들 수 있다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/image292.png
          :width: 100
          :alt: Example numerical input problem
     - :ref:`Numerical Input`
     - Studio에 있는 두 가지 유형의 수학 문제 중에 더 간단한 유형이다. 숫자 입력 문제에서, 학습자는 질문에 답하기 위해 숫자 또는 구체적이고 비교적 간단한 수학 공식을 입력한다. 이러한 문제는 정수만을 허용하며, 몇 가지 문제는 상수만 허용한다. 허용 오차를 지정하고 명시적으로 또는 Python 스크립트를 사용하여 정답을 지정할 수 있다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/Periodic_Table.png
          :width: 100
          :alt: Example periodic table problem
     - :ref:`Periodic Table`
     - 요소에 관한 인터랙티브 주기율표는 학습자가 마우스를 요소 위로 이동하면각 요소에 대한 자세한 정보를 표시한다.
   * - .. image:: ../../../shared/building_and_running_chapters/Images/ProteinBuilder.png
          :width: 100
          :alt: Example protein builder problem
     - :ref:`Protein Builder`
     - Protex 단백질 작성기는 학습자가 아미노산을 함께 모아 특정 단백질 모양을 만들 수 있도록 한다.
