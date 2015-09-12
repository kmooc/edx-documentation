.. _Google Drive Files Tool:

########################
구글 드라이브 파일 도구
########################

이 장에서는 강좌에 문서, 스프레드시트 및 이미지 등의 구글 드라이브 파일을 포함하는 방법을 설명한다. 더 자세한 내용은 다음 항목 중 하나를 참조하도록 한다.

* `개관`_
* `강좌에 구글 드라이브 포함하기`_

  * `강좌에 구글 드라이브 포함하기`_

    * `스튜디오에서 구글 드라이브 파일 활용하기`_
    * `OLX에서 구글 드라이브 파일 활용하기`_

  * `소스 코드가 포함된 구글 드라이브 파일 얻기`_
  * `구글 드라이브 파일을 강좌에 추가하기`_

    * `스튜디오에서 구글 드라이브 파일 구성 요소를 추가하기`_
    * `OLX에서 구글 드라이브 파일 XBlock를 추가하기`_

* `구글 드라이브 파일 변경하기`_

또한 강좌 내용에 :ref:`Google Calendar Tool` 를 사용할 수 있다. 더 자세한 내용은 :ref:`Google Calendar Tool` 를 참조하도록 한다.

*********
개관
*********

학습자 강좌 내용에서 파일을 볼 수 있도록 강좌에 구글 드라이브 파일을 포함할 수 있다. 예를 들어, 학습자와 구글 스프레드시트를 공유할 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/google-spreadsheet.png
  :width: 600
  :alt: A Google spreadsheet in courseware

다음과 같은 유형의 구글 드라이브 파일을 포함할 수 있다. 

* 구글 문서 도구 (텍스트 문서)
* 구글 그림 (이미지)
* 구글 양식 (양식 또는 설문 조사)
* 구글 슬라이드 (프레젠테이션)
* 구글 시트 (스프레드시트)
  
********************************************
강좌에 구글 드라이브 파일 포함하기
********************************************

강좌에 구글 드라이브 파일을 포함하려면 다음 3 단계가 있다: 구글 드라이브 가져올 파일 소스 코드.

#. :ref:`Studio<Enable Google Drive Files in edX Studio>` 또는 :ref:`OLX<Enable Google Drive Files in OLX>` 를 사용하여 :ref:`Enable Google Drive Files in Your Course` .


#. `코드가 포함된 구글 드라이브 파일 열기`_.

#. :ref:`Studio<Add a Google Drive File Component in edX Studio>` 또는 :ref:`OLX<Add a Google Drive File XBlock in OLX>` 를 사용하여 :ref:`Add a Google Drive File to Your Course` 하기.



.. _Enable Google Drive Files in Your Course:

========================================
강좌에 구글 드라이브 파일 활용하기
========================================

스튜디오 또는 OLX를 사용하여 강좌에서 구글 드라이브 파일을 사용할 수 있다.

.. _Enable Google Drive Files in edX Studio:

스튜디오에서 구글 드라이브 파일 활용하기
***************************************

강좌에서 구글 드라이브 파일을 활용 하려면: 

#. **설정**  메뉴에서 **고급 설정** 을 선택한다.

#. **고급 모듈 목록** 입력 필드에서 중괄호 사이 커서를 놓고 ``"google-document"`` 를 입력한다. 이 입력 필드에 다른 값을 보려면, 마지막 값에 대한 닫는 따옴표 후 쉼표를 추가한 다음, ``"google-document"`` 를 입력한다. 예를 들면:
   
   .. image:: ../../../shared/building_and_running_chapters/Images/google-advanced-setting.png
    :alt: Advanced modules setting for Google documents

#. 페이지 하단에 **변경 사항 저장** 을 선택한다.


.. _Enable Google Drive Files in OLX:

OLX에서 구글 드라이브 파일 활용하기
********************************

강좌에서 구글 드라이브 파일을 활용하려면, 강좌 구조를 정의하는 XML 파일을 편집할 수 있다. 당신은 ``course`` (강좌) 요소의 ``advanced-modules`` (고급 모듈) 속성을 찾아서, 그곳에 문자열 ``google-document`` 를 추가한다. 

예를 들어, 다음 XML 코드는 강좌에서 구글 드라이브 파일을 활용할 수 있게 한다. 또한 구글 캘린더를 활용할 수 있게 한다.

.. code-block:: xml

  <course advanced_modules="[&quot;google-document&quot;, 
      &quot;google-calendar&quot;]" display_name="Sample Course" 
      start="2014-01-01T00:00:00Z">
      ...
  </course>

더 자세한 내용은 :ref:`The Courseware Structure` 를 참조하도록 한다.

.. _Obtain the Google Drive File Embed Code:

=======================================================
구글 드라이브 파일 게시하기 및 포함된 소스 코드 얻기
=======================================================

구글 드라이브 파일을 강좌에 추가하기 전에, 웹에 그 파일을 먼저 게시해야 하고 파일에 대한 소스 코드를 얻어야 한다. 

.. important:: 
 이 주제에 설명된 작업은 제 3 자 소프트웨어의 사용에 의존한다. 이 소프트웨어는 소유자에 의해 변경될 수 있기 때문에, 여기에 제공된 단계들은 지침이며, 정확한 절차를 위한 것이 아니다.

#. 구글 드라이브 파일을 연다.
#. **파일** 메뉴에서 **웹에 게시하기** 를 선택한다.
   
   .. image:: ../../../shared/building_and_running_chapters/Images/google-publish-to-web.png
    :alt: The Google Drive file Publish to the web dialog box

#. **게시** 를 클릭한 다음, 동작을 확인하려면 **확인** 을 선택한다. 
#. **소스** 탭을 클릭한다.
      
   .. image:: ../../../shared/building_and_running_chapters/Images/google-embed.png
    :alt: The Google Drive file Publish to web Embed tab

#. **소스** 입력 필드에 ``<iframe>`` 태그를 포함한 전체 문자열을 복사한다. 

   .. note::  
    구글 이미지는 ``<iframe>`` 태그가 없다. 이미지를 포함하려면, 완전한 ``img`` 태그를 복사하도록 한다. 

   이 문자열을 사용하여 구글 드라이브 파일 구성 요소를 설정할 수 있다.

.. _Add a Google Drive File to Your Course:

========================================
구글 드라이브 파일을 강좌에 추가하기
========================================

강좌 내용에 구글 드라이브 파일을 추가 하려면, 스튜디오에서 고급 구성 요소를 만들거나 또는 OLX에서 Google 문서 Xblock를 만든다.

.. _Add a Google Drive File Component in edX Studio:

스튜디오에서 구글 드라이브 파일 구성 요소 추가하기
******************************************************

구성 요소를 추가하기 전에, :ref:`Enable Google Drive Files in edX Studio`  하는지 확인한다.

구글 드라이브 파일 구성 요소를 추가 하려면: 

#. 강좌 개요 페이지에서, 추가 하려는 구글 드라이브 구성 요소가 있는 학습활동을 연다. 

#. **새 구성 요소 추가** 에서, **고급** 을 클릭하고 **구글 문서** 를 선택한다.
   
   새 구성 요소는 포함된 기본 구글 프레젠테이션 과 함께 학습활동에 추가된다.

   .. image:: ../../../shared/building_and_running_chapters/Images/google-document-studio.png
    :alt: The Google Drive file component in a unit page

#. 새 구성 요소에서 **편집** 을 선택한다.
   
   .. image:: ../../../shared/building_and_running_chapters/Images/google-document-edit-studio.png
    :alt: The Google Drive file editor

#. **표시 이름** 입력 필드에, 구성 요소에 대한 이름을 입력한다.

#. **소스 코드** 입력 필드에, `코드가 포함된 구글 드라이브 파일 얻기`_ 작업에서 복사한 소스 코드를 붙여 넣는다.

#. **저장** 을 클릭한다.

그런 다음 구글 드라이브 파일이 있는 학습활동이 학습자에게 어떻게 표시되는지 보기 위해 :ref:`Preview Course Content` 를 할 수 있다.

.. _Add a Google Drive File XBlock in OLX:

OLX에서 구글 드라이브 파일 XBlock 추가하기
*******************************************

OLX에서 구글 드라이브 파일 XBlock을 추가하려면, ``google-document`` (구글 문서) 요소를 만든다. vertical (수직) 요소에 google-document (구글 문서) 요소를 포함시킬 수 있거나 또는 ``수직`` 에서 참조하는 독립 실행형 파일로써 ``google-document`` (구글 문서) 요소를 만들 수 있다.

더 자세한 내용은 `강좌 내용 구조`_  를 참조하도록 한다. 

예를 들면:

.. code-block:: xml

  <google-document url_name="c5804436419148f68e2ee44abd396b12"
    embed_code="&lt;iframe 
    frameborder=&quot;0&quot; src=&quot;https://docs.google.com/spreadsheet/pub
    ?key=0AuZ_5O2JZpH5dGVUVDNGUE05aTFNcEl2Z0ZuTUNmWUE&amp;output=html&amp;widge
    t=true&quot;&gt;&lt;/iframe&gt;" display_name="Google Document"/>

``embed_code`` 속성의 값은 `코드가 포함된 구글 드라이브 파일 얻기` _ 작업에서 복사한 소스 코드이다. 

.. note:: 
  edX 학습 관리 시스템은 구글 드라이브 파일에 대한 높이 및 너비 값을 설정한다. 이러한 속성을 추가하면, LMS는 변경 내용을 무시한다.

**************************
구글 드라이브 파일 변경하기
**************************

강좌에 포함된 구글 드라이브 파일을 변경하고 저장하는 경우, 학습자는 즉시 업데이트를 볼 수 있게 된다. 구글 사용자 인터페이스를 가지고 파일을 변경한다. 구글 문서 구성 요소를 편집할 필요는 없다.


.. _The Courseware Structure: http://edx.readthedocs.org/projects/edx-open-learning-xml/en/latest/organizing-course/course-xml-file.html
