
.. _Poll:

##########
설문 조사 도구
##########

강좌에서 설문 조사를 시행하여 학습자가 질문들에 대한 의견을 교환할 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/PollExample.png

.. note:: 설문 조사 도구를 생성하려면 강좌를 내보내고(export), 해당 강좌의 XML 파일 일부를 텍스트 편집기로 편집한 후, 해당 강좌에 다시 가져와야 (re-import) 한다. 설문 조사를 생성하기 전에 강좌 백업 사본을 만들것을 권한다. XML 편집에 익숙하다면, 설문 조사를 포함한 파일만을 텍스트 편집기에서 편집할 것을 권한다.

**************
용어
**************

강좌 개요 보기에 규정된 주제, 소주제, 학습활동, 구성요소는 강좌를 내보내고 .xml 파일을 열어 편집한 후 보게 될 파일 목록에서는 다른 이름으로 명시된다. 강좌 개요 보기 및 파일 목록에 등장하는 요소의 명칭을 다음 표로 정리한다.

.. list-table::

   :widths: 15 15
   :header-rows: 0

   * - 강좌 개요 보기
     - File List
   * - 주제
     - Chapter
   * - 소주제
     - Sequential
   * - 학습활동 
     - Vertical
   * - 구성요소
     - Discussion, HTML, problem, or video
     
 

즉, 어떤 강좌의 특정 주제를 해당 강좌가 포함하고 있는 파일 목록에서 찾고자 한다면 **Chapter** 폴더를 조사해야 한다는 뜻이다. 마찬가지로 강좌에서의 학습 활동은 **Vertical** 폴더에서 찾아야 한다.

.. _Create a Poll:

**************
설문 조사 생성하기
**************

#. 설문 조사를 생성하고자 하는 학습 활동에서, 해당 설문 조사를 제외하고 원하는 모든 콘텐츠를 포함하는 구성요소를 생성한다. **학습 활동 위치** 의 **학습 활동 식별자** 필드에 표시되는 32자리 숫자의 학습활동 ID를 기록하는 것이 좋다.

#. 강좌를 내보내기 한다. 내보내는 방법을 확인하려면 :ref:`Exporting and Importing a Course` 를 참조한다. 강좌를 포함하고 있는 .tar.gz 파일을 기억하기 쉬운 장소에 저장하여 쉽게 찾을 수 있도록 한다.

#. 강좌를 포함하고 있는 .tar.gz 파일을 찾은 후 압축을 푼다. 폴더 및 파일 목록에서 압축 해제된 내용을 확인한다

   - 윈도우즈를 OS로 사용하는 컴퓨터에서 이 작업을 시행하려면 별도의 프로그램이 필요한다. 자세한 정보가 필요할 경우 윈도우즈에서 tar 파일 압축 푸는 방법(How to Unpack a tar File in Windows), Gz파일 압축 푸는 방법(How to Extract a Gz File), gzip 홈페이지, .tar.gz 파일 여는 방법 페이지(How to Open .tar.gz Files) 중 윈도우즈 섹션을 참고한다.

   - Mac에서 이를 시행하려면 tar.gz 파일 여는 방법 페이지 중 Mac OS X 섹션을 참조바란다.

#. 폴더 및 파일 목록에서 **Vertical** 폴더를 연다.

   .. note:: 학습활동이 게시되지 않았다면, **Drafts** 폴더를 열고, **Vertical** 를 연다.

#. **Vertical** 폴더 내부에서, 위의 단계1에서 기록해 둔 학습활동 ID와 동일한 이름을 가진 .xml 파일을 찾아 Sublime 2와 같은 텍스트 편집기에서 연다. 가령, 학습활동 ID가 e461de7fe2b84ebeabe1a97683360d31인 경우 e461de7fe2b84ebeabe1a97683360d31.xml 파일을 연다.

  이 파일은 해당 학습 활동의 모든 구성요소와 그 구성요소의 URL 목록을 포함하고 있다. 가령 다음 파일은 하나의 게시판 구성요소 앞에 HTML 구성요소를 포함한다.

   .. code-block:: xml
     
       <vertical display_name="Test Unit">
        <html url_name="b59c54e2f6fc4cf69ba3a43c49097d0b"/>
        <discussion url_name="8320c3d511484f3b96bdedfd4a44ac8b"/>
       </vertical>

6. 설문 조사를 만들려고 하는 위치에 다음 설문 조사 코드를 추가한다. 프롬프트 텍스트를 원하는 텍스트로 바꾼다.

   .. code-block:: xml
      
    <poll_question display_name="Poll Question">
      <p>Text of the prompt</p>
      <answer id="yes">Yes</answer>
      <answer id="no">No</answer>
    </poll_question>

   상기 예시에서 설문 조사를 해당 학습활동의 HTML 구성요소와 게시판 구성요소 사이에 게시하고자 하는 경우 코드는 다음과 유사한 형태가 된다.

   .. code-block:: xml

     <vertical display_name="Test Unit">
      <html url_name="b59c54e2f6fc4cf69ba3a43c49097d0b"/>
      <poll_question display_name="Poll Question">
        <p>Text of the prompt</p>
        <answer id="yes">Yes</answer>
        <answer id="no">No</answer>
      </poll_question>
      <discussion url_name="8320c3d511484f3b96bdedfd4a44ac8b"/>
     </vertical>

#. 설문 조사 코드를 추가한 후 .xml 파일을 저장하고 닫는다.

#. 강좌를 .tar.gz 파일로 다시 압축한다.

   * Mac에서 압축하는 방법은  `How to Create a Tar GZip File from the Command Line <http://osxdaily.com/2012/04/05/create-tar-gzip/>`_ 에서 확인한다.

   * 윈도우즈 환경에서 압축하는 방법은, `How to Make a .tar.gz on Windows <http://stackoverflow.com/questions/12774707/how-to-make-a-tar-gz-on-windows>`_ 에서 확인한다.

#. Studio에서 강좌를 가져오기(re-import) 한다. 이제 설문 조사 문항과 선택지를 Studio에서 검토할 수 있다.

.. note::

  * Studio에서 설문 조사를 적절히 실행할 수는 있으나 편집할 수는 없다. 설문 조사 도구를 편집할 경우 상기한 내보내기/가져오기절차를 따른다.
  
  * 현재는 문제에 대한 학습자 응답을 포함하는 .csv 파일은 설문 조사에서 사용할 수 없다. 단, 데이터를 해당 문제에서 직접 획득할 수 있다.

*********************
포맷 설명
*********************

설문 조사 모듈 입력의 메인 태그는 다음과 같다.

.. code-block:: xml

    <poll_question> ... </poll_question>

``poll_question`` 에는 다음 태그를 포함할 수 있다: xml 및 ``answer`` 태그. 모든 내부 xml, 단 "question"으로 부르는 ``answer`` 태그 제외

==================
poll_question 태그
==================

Xmodule은 설문 조사 기능, 즉 투표 시스템을 생성하기 위한 것이다. 이 태그에는 다음 속성을 지정할 수 있다.::

    name - Name of xmodule.
    [display_name| AUTOGENERATE] - Display name of xmodule. When this attribute is 
    not defined - display name autogenerate with some hash.
    [reset | False] - Can reset/revote many time (value = True/False)

============
answer 태그
============

설문 조사 모듈에 가능한 답변 가운데 하나를 정의한다. 이 태그에는 다음 속성을 지정할 수 있다.::

    id - unique identifier (using to identify the different answers)

내부 텍스트 – 선택지에 대한 표시 텍스트

***********
예시
***********

==================
설문 조사 예시
==================

.. code-block:: xml

    <poll_question name="second_question" display_name="Second question">
        <h3>Age</h3>
        <p>How old are you?</p>
        <answer id="less18">&lt; 18</answer>
        <answer id="10_25">from 10 to 25</answer>
        <answer id="more25">&gt; 25</answer>
    </poll_question>

================================================
초기화 기능이 없는 설문 조사 예시
================================================

.. code-block:: xml

    <poll_question name="first_question_with_reset" display_name="First question with reset"
        reset="True">
        <h3>Your gender</h3>
        <p>You are man or woman?</p>
        <answer id="man">Man</answer>
        <answer id="woman">Woman</answer>
    </poll_question>
