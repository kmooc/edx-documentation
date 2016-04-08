.. _Working with HTML Components:


#############################
HTML 구성요소
#############################

***********************
개관
***********************

HTML 또는 HyperText Markup Language는 웹 페이지를 만드는데 이용되는 표준 마크업 언어이다. 웹 브라우저는 HTML 코드를 보다 읽기 좋게 표시한다.

학습자는 강좌에서 텍스트나 이미지를 볼 때 브라우저에서 형식화되고 표현된 HTML 코드를 보게 된다. HTML에 대한 더 많은 정보는 `Wikipedia <http://en.wikipedia.org/wiki/HTML>`_ 에 있다. 

HTML 구성요소는 강좌 콘텐츠를 만드는 기초 재료이며, 텍스트, 링크, 이미지 등을 추가하고 형식화 하는데 사용된다. 콘텐츠를 제작할 때 HTML 코드를 이용하여 직접 HTML 구성요소를 만들어낼 수도 있고, 다음에서 설명될 내용과 같이 비주얼 에디터를 사용할 수도 있다.

자세한 정보는 아래 링크에 안내되어 있다. 

* :ref:`Options for Editing HTML Components`
* :ref:`The Visual Editor`
* :ref:`The Raw HTML Editor`
* :ref:`HTML Component Templates`
* :ref:`Create an HTML Component`
* :ref:`Add a Link in an HTML Component`
* :ref:`Add an Image to an HTML Component`
* :ref:`Import LaTeX Code`

.. note:: HTML 구성요소로 작업을 시작하기 전에 :ref:`Developing Your Course Index` 와 :ref:`Best Practices for HTML
 Markup` 를 먼저 살펴보는 것을 권한다.

 HTML 구성요소에 instant hangout을 추가하는 것과 관련해서는 :ref:`Google Instant Hangout` 에 자세히 안내되어 있다. 


.. _Options for Editing HTML Components:

********************************************
HTML 구성요소 편집 옵션
********************************************

HTML 작업은 다음 두 가지 방법으로 수행할 수 있다.

* :ref:`The Visual Editor`

  비쥬얼 편집기를 이용하면, HTML 코드를 직접 사용하지 않고 워드프로세싱 프로그램처럼 
  콘텐츠를 만들거나, 편집하고, 포맷을 맞출 수 있다. 
  이에 쉽게 강좌 콘텐츠의 서식을 지정할 수 있고, 링크 및 이미지를 추가할 수 있다. 
  그러나, 비쥬얼 편집기에서 HTML 보기는 Raw HTML 편집기에서 할 수 있는 세부 제어를 제공하지 않으며, 
  사용자 서식 및 스크립트를 지원하지 않는다.

* :ref:`The Raw HTML Editor`

  Raw HTML 편집기를 이용하면, HTML 코드를 직접 작업할 수 있다. 
  강좌 콘텐츠 안에 사용자 서식이나 스크립트를 사용해야 한다면 Raw HTML 편집기를 사용해야 한다.

.. _Set the Editor for an HTML Component:

************************************ 
HTML 구성요소 에디터 설정하기
************************************

**설정** 에서 HTML 구성요소에 대한 편집기를 설정한다.

.. image:: ../../../shared/building_and_running_chapters/Images/set_html_editor.png
 :alt: The Editor selection drop-down list in the HTML Component Settings tab

**Visual** 또는 **Raw** 를 선택 후 반드시 **저장** 을 클릭한다. 그리고 새로운 편집기를 사용하기 위해 구성요소를 다시 연다.

.. warning:: Raw HTML 편집기로 강좌 콘텐츠 작업을 한 후 비주얼 편집기로 변경하게 되면, 
 앞서 만들었던 HTML이 삭제될 수 있다. 그래서 우선 비주얼 편집기로 편집을 시작하고, 사용자 HTML을 만들 필요가 있을 때 
 Raw HTML 편집기로 전환하여 이용할 것을 권장한다.
 
.. _The Visual Editor:

*****************************************
비쥬얼 편집기
*****************************************

비쥬얼 편집기는 편집기 상단의 서식 버튼들을 클릭하여 서식을 지정할 수 있는 “what you see is what you get” (WYSIWYG) 인터페이스를 제공한다. 

.. image:: ../../../shared/building_and_running_chapters/Images/HTMLEditor.png
 :alt: Image of the HTML component editor

.. note:: 
  :ref:`Adding Course Updates and Handouts` 에서는 비쥬얼 편집기가 지원되지 않는다.

다음 이미지는 편집 옵션에 대한 설명이다. 

.. image:: ../../../shared/building_and_running_chapters/Images/HTML_VisualView_Toolbar.png
  :alt: Image of the HTML editor, with call-outs for formatting buttons

#. 머리글 1, 머리글 2, 또는 단락 등 선택한 단락에 대한 서식 스타일을 선택한다. 
   
#. Arial, Courier New, 또는 Times New Roman 같은 글꼴을 선택한다.
   
#. 선택한 텍스트를 굵게 한다.
#. 선택한 텍스트를 기울게 한다.
#. 선택한 텍스트에 밑줄 긋는다.
#. 선택한 텍스트에 색상을 적용한다.
#. 선택한 텍스트를 코드로 표시한다.
#. 글머리 기호 목록을 만든다.
#. 번호 매기기 목록을 만든다.
#. 선택한 단락의 들여쓰기를 감소시키고 증가시킨다.
#. 선택한 단락을 인용구로 만든다.
#. 선택한 텍스트에서 링크를 만든다. :ref:`Add a Link in an HTML Component` 에 자세한 안내가 있다.
#. 현재 링크를 삭제한다. 
#. 마우스 커서 위치에 이미지를 삽입한다. :ref:`Add an Image to an HTML Component` 에 자세한 안내가 있다.
#. HTML 소스 코드 작업을 한다.


.. _Work with HTML code:


비쥬얼 편집기에서 HTML 코드 작업하기
*****************************************

비쥬얼 편집기에서 만든 강좌 콘텐츠에 대해 HTML 소스 코드 작업을 하려면, 편집기 도구 모음에서 
**HTML** 을 클릭한다. 그러면 HTML 소스 코드 편집기가 열린다.

.. image:: ../../../shared/building_and_running_chapters/Images/HTML_source_code.png
 :alt: Image of the HTML source code editor

필요한 대로 HTML 코드를 편집한다. 

비쥬얼 편집기에 있는 HTML 소스 코드에서는 사용자 스타일 및 스크립트를 추가할 수 없고, Raw HTML 편집기를 사용해야 한다.

소스 코드 편집기를 닫고 변경 내용을 적용하려면 **확인** 을 클릭한다. 그러면 비쥬얼 편집기는 HTML 코드가 유효한지 확인한다. 예를 들어, 단락 태그를 닫지 않는 경우, 편집기가 자동으로 추가할 것이다.

.. note:: 소스 코드 편집기에서 **확인** 을 클릭하더라도 HTML 구성요소의 변경 내용은 저장되지 않는다.
 그래서, 비쥬얼 편집기에서 변경 내용을 저장하기 위해 **저장** 을 클릭한 후 구성 요소를 닫아야 한다. 
 **취소** 를 클릭하면 HTML 소스 코드에서 수행한 변경 내용이 사라진다.

.. _The Raw HTML Editor:

*****************************
Raw HTML 편집기
*****************************

HTML 구성요소를 위해 Raw 편집기를 선택하면, 텍스트 편집기에서 콘텐츠를 편집할 수 있다. 

.. image:: ../../../shared/building_and_running_chapters/Images/raw_html_editor.png
 :alt: The raw HTML editor

편집할 때 유효한 HTML을 입력해야 한다. Raw HTML 편집기가 HTML 코드를 검사 하지 않기 때문에, 강좌의 HTML 콘텐츠를 꼼꼼하게 테스트해볼 필요가 있다.


.. _HTML Component Templates:

*****************************
HTML 구성요소 템플릿
*****************************

새로운 HTML 구성요소를 만들 때 템플릿의 목록에서 선택할 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/html_templates.png
 :alt: The list of HTML Component templates

Raw HTML 템플릿은 Raw HTML 편집기를 사용하도록 설정되어 있다. 그외 모든 템플릿은 비쥬얼 편집기를 사용한다. 

HTML 구성요소는 템플릿으로 만든다고 해도 에디터로 변경할 수 있다. :ref:`Set the Editor for an HTML Component` 에 안내되어 있다.


.. _Create an HTML Component:

*****************************
HTML 구성요소 만들기
*****************************

HTML 구성요소를 만들려면,

1. **신규 구성요소 추가** 에서 **HTML** 을 클릭한다.

  .. image:: ../../../shared/building_and_running_chapters/Images/NewComponent_HTML.png
   :alt: Image of adding a new HTML component

2. 템플릿을 선택한다. 

   **Text** 를 선택했다고 가정하면,
   
   학습활동 아래쪽에 빈 구성요소가 나타난다.

  .. image:: ../../../shared/building_and_running_chapters/Images/HTMLComponent_Edit.png
   :alt: Image of an empty HTML component

3. 해당 구성요소에서, **편집** 을 클릭한다. 

   비쥬얼 편집기에서 HTML 구성요소가 열린다.

  .. image:: ../../../shared/building_and_running_chapters/Images/HTMLEditor_empty.png
   :alt: Image of the HTML component editor

4. 강좌 콘텐츠를 입력하고 서식을 지정한다. 이에 대해 더 자세한 정보는 :ref:`Work with HTML code` 에 있다.

5. 구성요소 편집기의 오른쪽 상단에서 **설정** 을 클릭한 후, **메뉴명** 에 텍스트를 입력한다.

   편집기로 돌아가려면, 오른쪽 상단에서 **편집기** 를 클릭한다.

6. HTML 구성요소를 저장하려면, **저장** 을 클릭한다. 

비쥬얼 편집기에서, 다음과 같은 작업도 할 수 있다.

* :ref:`Add a Link in an HTML Component`
* :ref:`Add an Image to an HTML Component`
* :ref:`Import LaTeX Code`

.. _Add a Link in an HTML Component:

***********************************
HTML 구성요소에 링크 추가하기
***********************************

비쥬얼 편집기를 사용하여 웹 사이트, 강좌 학습활동, HTML 구성요소에 있는 파일을 추가하려고 할 때는 **링크 삽입** 대화상자로 작업할 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/HTML_Insert-EditLink_DBox.png
 :alt: Image of the Insert link dialog box

이와 관련해 다음과 같은 작업을 할 수 있다:

* :ref:`Add a Link to a Website`
* :ref:`Add a Link to a Course Unit`
* :ref:`Add a Link to a File`

.. _Add a Link to a Website:

웹 사이트 링크 추가하기
***********************************

웹 사이트 링크를 추가하려면

#. 링크를 추가할 텍스트를 선택한다. 

#. 상단 도구모음에서 링크 아이콘 (링크 편집/삽입)을 클릭한다.

#. **링크 삽입** 대화상자에서, URL 입력 필드에 원하는 웹사이트의 URL을 입력한다.

   .. image:: ../../../shared/building_and_running_chapters/Images/HTML_Insert-EditLink_Website.png
    :alt: Image of the Insert link dialog box

#. 새 창에서 링크를 열려면, **Target** 에 있는 드롭다운 화살표를 클릭하고 난 다음, 
   **새 창** 을 선택한다. 그렇지 않은 경우에 기본값(없음)으로 두면 된다. 
   
   
#. **확인** 을 클릭한다.

#. HTML 구성요소를 저장하고 링크를 시험해 본다.


.. _Add a Link to a Course Unit:


강좌 학습활동 링크 추가하기
***********************************

HTML 구성요소에서 강좌 학습활동 링크를 추가할 수 있다. 

#. 추가하려고 하는 학습활동의 고유 식별자를 가져온다. 
   Studio에서 학습활동 페이지를 열고, 오른쪽 하단에 있는 
   **학습 활동 위치** 에서, **위치 ID** 를 복사한다.
   
   .. image:: ../../../shared/building_and_running_chapters/Images/UnitIdentifier.png
    :alt: Image of the unit page with the unit identifier circled

#. 링크를 추가하려는 곳에 HTML 구성요소를 연다.

#. 링크로 만들려는 텍스트를 선택한다. 

#. 도구모음에서 링크 아이콘을 클릭한다.

#. **링크 삽입** 대화 상자에서, **URL** 입력 필드에 다음을 입력한다.

   ``/jump_to_id/<unit identifier>``

    <unit identifier> 대신에 1단계에서 복사했던 학습활동 위치ID로 대체한다. 
   
   .. image:: ../../../shared/building_and_running_chapters/Images/HTML_Insert-EditLink_CourseUnit.png
    :alt: Image of the Insert link dialog box with a link to a unit identifier

#. 새 창에서 링크를 열려면 **Target** 의  드롭다운 화살표를 클릭한 후 **새 창** 을 선택한다. 
   그렇지 않은 경우에 기본값이 적용된다.

#. **확인** 을 클릭한다.

#. HTML 구성요소를 저장하고 링크를 시험해본다.


.. _Add a Link to a File:

파일에 링크 추가하기
***********************************

강좌를 위해 업로드한 모든 파일을 HTML 구성요소에서 링크로 추가할 수 있다. 파일 업로드에 대한 자세한 정보는 :ref:`Add Files to a Course` 에 있다.


#. **파일 업로드** 페이지에서 파일의 **URL** 을 복사한다.

  .. image:: ../../../shared/building_and_running_chapters/Images/HTML_Link_File.png
   :alt: Image of Files and Uploads page with the URL field circled 
  
  .. note:: 
   파일 링크로는 **Web URL** 이 아닌 **Studio URL** 을 사용해야 한다.

2. 링크로 만들 텍스트를 선택한다.

#. 도구모음에서 링크 아이콘을 클릭한다.

#. **링크 삽입** 대화 상자에서, **URL** 입력 필드에 다음을 입력한다.

   ``/static/FileName.type``

   슬래시를 위 예문처럼 포함하도록 한다 (/).

   .. image:: ../../../shared/building_and_running_chapters/Images/HTML_Insert-EditLink_File.png
    :alt: Image of the Insert link dialog box with a link to a file

#. 새 창에서 링크를 열려면 **Target** 의  드롭다운 화살표를 클릭한 후 **새 창** 을 선택한다. 
   그렇지 않은 경우에 기본값이 적용된다.

#. **확인** 을 클릭한다.

#. HTML 구성요소를 저장하고 링크가 잘 되는지 확인한다.


.. _Add an Image to an HTML Component:

***********************************
 HTML 구성요소에 이미지 추가하기
***********************************

비쥬얼 편집기를 사용하면 강좌를 위해 업로드 한 어떤 이미지라도 HTML 구성 요소에 추가할 수 있다. 이미지 업로드하기에 대한 자세한 내용은 :ref:`Add Files to a Course` 에 있다.

.. note:: HTML 구성요소에 이미지를 추가하기 전에 :ref:`Best Practices for Describing Images` 를 확인한다. 이미지를 추가하기 위해, 강좌에 업로드한 이미지 파일의 URL이 필요하다. 

#. **파일 업로드** 페이지에서 원하는 이미지의 **Studio URL** 을 복사한다.

  .. image:: ../../../shared/building_and_running_chapters/Images/image_link.png
   :alt: Image of the Files & Upload page with the Embed URL for the image
       circled

  .. note:: 
    이미지를 추가하기 위해 **Web URL** 이 아닌 **Studio URL** 을 사용해야 한다.

2. 도구모음에서 이미지 아이콘을 클릭한다.

#. **이미지 삽입/편집** 대화 상자에서, **소스** 입력칸에 **Studio URL** 을 붙여넣기한다.

   .. image:: ../../../shared/building_and_running_chapters/Images/HTML_Insert-Edit_Image.png
    :alt: Image of the Insert image dialog box with a reference to a file

4. **이미지 설명** 입력 필드에 이미지를 설명하는 텍스트를 입력한다. 이 텍스트는 HTML에서 ``alt`` 속성 값이 되고, 강좌가 높은 접근성을 갖도록 하기 위해서 필요하다. 자세한 내용은 :ref:`Best Practices for Describing Images` 를 참조한다. 

#. **이미지 크기** 를 사용자가 지정할 수 있다. 이미지가 너비와 높이를 동일한 비율로 유지되도록 하기 위해서는 **비율 제한** 을 선택한다. 

#. 이미지의 간격 및 테두리를 변경 하려면 **고급** 탭을 클릭한다. 

   .. image:: ../../../shared/building_and_running_chapters/Images/HTML_Insert-Edit_Image_Advanced.png
    :alt: Image of the Insert image dialog box Advanced tab

#. **수직 공간, 수평 공간, 및 테두리** 를 입력한다. 입력한 값은 **스타일** 입력칸에 자동으로 변환되어 나타난다.

#. HTML 구성요소에 이미지를 삽입하려면 **확인** 을 클릭한다.

#. HTML 구성요소를 저장하고 이미지가 나오는지 확인한다.


