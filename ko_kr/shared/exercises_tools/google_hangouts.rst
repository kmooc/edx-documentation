.. _Google Instant Hangout:

###########################################
구글 Instant Hangout 도구
###########################################

이 장에서는 강좌에 Instant Hangout을 사용하는 방법을 설명한다. 

* :ref:`Hangouts_Overview`
* :ref:`Instant Hangouts in Your Course`
* :ref:`The Student Experience`
* :ref:`Limitations`
* :ref:`Create the Instant Hangout`

.. _Hangouts_Overview:

*****************
개관
*****************

학습자가 강좌에서 직접 Instant Hangout에 참여할 수 있는 권한을 추가할 수 있다.

Instant Hangout으로, 학습자는 다음을 수행할 수 있다

* 라이브 비디오와 목소리를 통해 상호 작용한다.
* 화면을 공유하고 함께 비디오를 시청한다.
* 문서를 공동 작업한다.

Instant Hangout 특징의 전체 목록에 대하여, `Google Hangouts <http://www.google.com/+/learnmore/hangouts/>`_ (구글 행아웃 페이지)를 참조하도록 한다.

.. note:: Instant Hangout에 참여하고 싶은 학습자는 구글 계정이 있어야 한다. 강좌 운영팀은 이를 학습자에게 공지해야 한다.

.. _Instant Hangouts in Your Course:

**********************************
Instant Hangout
**********************************

하나 이상의 Instant Hangout을 강좌에 추가할 수 있다. 예를 들어, 

* 한 페이지에서, 전체 강좌 진행 중, 학습자에게 Hangout을 제공하기 위해서 Instant Hangout을 추가할 수 있다. 더 많은 정보는 :ref:`Adding Pages to a Course`  를 참조하도록 한다.

* HTML 구성요소에서, 특정 강좌 학습활동에서 작업하는 학습자에게 행아웃을 제공하기 위해서 Instant Hangout을 추가할 수 있다. HTML 구성요소 만들기에 대한 더 자세한 내용은 :ref:`Working with HTML Components` 를 참조하도록 한다.

 Instant Hangout은 Hangout으로부터 열리는 페이지에만 적용된다. 예를 들어, 한 강좌의 학습활동에서 Hangout에 참여한 학습자는 그 Hangout에 참여한 학습자들끼리만 상호 작용하고, 다른 학습활동에서 Hangout에 참여하는 학습자는 다른 Hangout 내에서 상호 작용한다.

.. _The Student Experience:

*************************
학습자 경험
*************************

강좌에 Instant Hangout을 추가할 때, Hangout에 대한 제어는 해당 페이지에 나타난다. 다음 예제는 강좌 학습활동에 있는 제어를 보여준다. 그 제어는 학습자가 Hangout을 시작할 수 있고 첫 번째 참가자가 될 수 있음을 보여준다.

.. image:: ../../../shared/building_and_running_chapters/Images/hangout_unit.png
 :alt: Image of the instant hangout control on a unit

Hangout을 시작하려면, 학습자는 **Hangout 시작** 을 클릭한다. (첫 번째 학습자가 **Hangout 시작** 을 클릭하면, 다른 학습자는 **Hangout에 참여하기** 버튼을 보게 된다.)

다음 예제에서는 Hangout이 이미 시작 되었을 때 페이지에 있는 제어를 보여준다. 제어는 **Hangout에 참여하기** 버튼이 있으며, 한 다른 학습자가 이미 Hangout에 있음을 보여준다. 

.. image:: ../../../shared/building_and_running_chapters/Images/hangout_static_page.png
 :alt: Image of the instant hangout control on a page

Hangout에 참여하려면, 학습자는 **Hangout에 참여하기** 를 클릭한다. 

이미 로그인한 경우, 구글에 로그인하라는 메시지가 표시된다.

.. image:: ../../../shared/building_and_running_chapters/Images/google_login.png
 :alt: Image of the Google login page

구글 계정이 없는 학습자는 로그인 페이지에서 만들 수 있다. 학습자가 구글에 로그인 한 후, Hangout은 별도 브라우저 창에서 열린다.


.. image:: ../../../shared/building_and_running_chapters/Images/GoogleHangout_WithPeople.png
 :alt: Image of the instant hangout

.. _Limitations:

****************
제한점
****************

현재, 단지 10명의 학습자만 단일 Instant Hangout에 참여할 수 있다. 강좌 교재에 이것을 알려야 한다.

강좌에서 다른 페이지에서 시작된 Hangout에 있는 학습자는 별도로 계산된다. 그래서 한 학습활동에서 시작된 Hangout에 10명의 학습자가 참여할 수 있고, 다른 학습활동에서 시작된 Hangout에도 다른 10명의 학습자가 참여할 수 있다.  

.. _Create the Instant Hangout:

**************************************************
Instant Hangout 만들기
**************************************************

강좌에 Instant Hangout을 만들려면:

#.  `instant hangout JavaScript file from GitHub <https://raw.github.com/google/instant-hangouts/master/instanthangouts-0.1.0.js>`_

#. 컴퓨터에서 이 파일의 텍스트를 텍스트 편집기로 복사하고, JavaScript 파일로 해당 파일을 저장한다 (즉, 파일을 저장할 때, 확장자명을.txt에서.js 로 변경한다).

   .. note::  서식을 포함하지 않는 원본 GitHub 파일을 복사하는지 확인한다. 서식이 지정된 파일을 복사하지 않도록 한다. 모든 서식지정은 JavaScript가 올바르게 작동하지 않게 되는 원인이 된다.

#. 강좌에서 **파일 업로드** 페이지로 JavaScript 파일을 업로드한다. 더 자세한 내용은 :ref:`Add Files to a Course` 를 참조하도록 한다. 

#. 페이지 또는 HTML구성 요소에서 HTML 편집기를 연다.

#. 첫 번째 줄에, <script>태그에서 업로드 한 JavaScript 파일을 추가한다. 이때 완전한 열기 및 닫기 태그를 사용해야 한다.
   
   예를 들어, JavaScript 파일 이름이 **instanthangouts-0.1.0.js** 이면, 다음과 같이 입력한다.
  
    <script src='/static/instanthangouts-0.1.0.js'></script>

#. <script> 태그 뒤에, 다음을 추가한다.
  
    <div class='instanthangouts'/>

#. 원하는 모든 텍스트와 태그를 추가한다.

   예를 들어, 완전한 HTML은 다음과 같이 될 수 있다.

    <p>Join an instant hangout by clicking the button below. 
    You can use the hangout to have live video discussions with other students.</p>
    <script src='/static/instanthangouts-0.1.0.js'></script>
    <div class='instanthangouts'/>

#. 예를 들어, 완전한 HTML은 다음과 같이 될 수 있다.

=============================
JavaScript 파일 업데이트하기
=============================

구글은 정기적으로 Instant Hangout JavaScript파일을 업데이트한다. 업데이트 알림을 수신하려면, `instant hangouts repository <https://github.com/google/instant-hangouts/>`_  로 이동한 다음, 페이지의 오른쪽 위 영역에서 **보기** 를 클릭한다.

강좌에서 업데이트 된 JavaScript 파일을 사용하려면, 저장소로부터 JavaScript를 강좌에 업로드 한 파일과 같은 이름을 가지는 파일로 복사한다. 새로운 파일을 업로드 하는 경우, 새 파일은 이전 파일을 대체한다.

.. warning:: 업로드 된 파일의 파일 이름에 버전 번호를 포함하는 경우, JavaScript 파일을 업데이트할 때마다 Instant Hangout 제어를 포함하는 페이지 또는 모든 HTML 구성 요소를 편집해야 한다.
