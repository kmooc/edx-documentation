.. _Working with HTML Components:


#############################
HTML 구성요소를 사용한 작업
#############################

***********************
HTML 구성 요소 개요
***********************

HTML 또는 하이퍼 텍스트 마크업 언어(HyperText Markup Language)는 웹 페이지를 만드는데 사용되는 표준 마크업 언어이다. 웹 브라우저는 HTML 코드를 보다 읽기 쉬운 식으로 표시한다.

학습자가 KMOOC담당자의 강좌에서 텍스트나 이미지를 볼 때 브라우저에서 형식화되고 표현된 HTML 코드를 보게 된다. HTML에 대한 더 많은 정보는 `Wikipedia <http://en.wikipedia.org/wiki/HTML>`_ 에 있다. 

HTML 구성요소는 강좌 콘텐츠를 만드는 기초 재료이다. HTML 구성요소는 텍스트, 링크, 이미지 등을 추가하고 형식화 하는데 사용된다. K-MOOC 담당자는 콘텐츠를 제작할 때 HTML 코드를 이용하여 직접 HTML 구성요소를 만들어낼 수도 있고, 다음에서 설명될 내용과 같이 자세한 HTML 코드가 숨겨져 있는 비주얼 에디터를 사용할 수도 있다.

더 많은 정보는 다음 주제에 안내되어 있다. 

* :ref:`Options for Editing HTML Components`
* :ref:`The Visual Editor`
* :ref:`The Raw HTML Editor`
* :ref:`HTML Component Templates`
* :ref:`Create an HTML Component`
* :ref:`Add a Link in an HTML Component`
* :ref:`Add an Image to an HTML Component`
* :ref:`Import LaTeX Code`

.. 참고:: 
 HTML 구성요소로 작업을 시작하기 전에 :ref:`Developing Your Course Index` 와 :ref:`Best Practices for HTML
 Markup` 를 먼저 살펴보는 것을 권한다.

HTML 구성요소에 instant hangout을 추가하는 것과 관련해서는 :ref:`Google Instant
Hangout` 에 자세히 안내되어 있다. 


.. _Options for Editing HTML Components:

********************************************
HTML 구성요소 편집 옵션
********************************************

다음의 두 가지 방법으로 HTML 작업을 수행할 수 있다.

* :ref:`The Visual Editor`
  비쥬얼 편집기를 통해 워드 프로세싱과 유사한 인터페이스에서 HTML 코드를 직접 사용하지 않고, 
  콘텐츠를 만들고 편집하고 또한 포맷할 수 있다. 
  비쥬얼 편집기와 함께, 보다 쉽게 강좌 콘텐츠의 서식을 지정할 수 있고, 링크 및 이미지를 추가할 수 있다. 
  비쥬얼 편집기는 필요에 따라 서식에 대한 작은 변경사항을 만들 수 있도록 HTML 코드에 대한 접근을 제공한다. 
  그러나, 비쥬얼 편집기에서 HTML 보기는 원본 HTML 편집기에서 얻을 수 있는 세부적인 제어를 제공하지 않으며, 
  또한 사용자 지정 서식 및 스크립트를 지원하지 않는다.

* :ref:`The Raw HTML Editor`

  원본 HTML 편집기를 통해 직접 HTML 코드를 활용하여 작업할 수 있다. 
  강좌 콘텐츠 안에 사용자 지정 포맷이나 스크립트를 사용해야 한다면 원본 HTML 편집기를 사용해야 한다.


HTML 구성요소 에디터 설정하기
************************************

**설정** 탭에서 HTML 구성요소에 대한 편집기를 설정할 수 있다

.. image:: ../../../shared/building_and_running_chapters/Images/set_html_editor.png
 :alt: The Editor selection drop-down list in the HTML Component Settings tab

**비주얼** 또는 **원본** 을 선택한다. 편집기를 변경하려면, 반드시 **저장** 을 클릭하고 새로운 편집기를 사용하기 위해 구성요소를 다시 열어야 한다.

.. 주의:: 
 HTML 원본 편집기로 강좌 콘텐츠 작업을 한 후 비주얼 편집기로 변경하게 되면, 
 앞서 만들었던 사용자 정의 HTML이 삭제될 수 있다. 
 그러므로 비주얼 편집기를 사용하여 시작하고, 사용자 정의 HTML을 만들 필요가 있을 때 
 원본 HTML 편집기로 전환하여 이용할 것을 권장한다.
 
.. _The Visual Editor:

*****************************************
비쥬얼 편집기
*****************************************

비쥬얼 편집기는 편집기 상단에서 서식 버튼을 클릭하여 텍스트를 포맷할 수 있는 “what you see is what you get” (WYSIWYG) 인터페이스를 제공한다. 

.. image:: ../../../shared/building_and_running_chapters/Images/HTMLEditor.png
 :alt: Image of the HTML component editor

.. 참고:: 
  비쥬얼 편집기가 :ref:`course handouts <Adding Course Updates and Handouts>` 에 대해서는 지원되지 않는다.

다음 이미지는 편집 옵션에 대한 결과를 보여준다. 

.. image:: ../../../shared/building_and_running_chapters/Images/HTML_VisualView_Toolbar.png
  :alt: Image of the HTML editor, with call-outs for formatting buttons

#. 머리글 1, 머리글 2, 또는 단락 등 선택한 단락에 대한 서식 스타일을 선택한다. 
   
#. Arial, Courier New, 또는 Times New Roman 같이 글꼴을 선택한다.
   
#. 선택한 텍스트를 굵게 한다.
#. 선택한 텍스트를 기울게 한다.
#. 선택한 텍스트에 밑줄 긋는다.
#. 선택한 텍스트에 색상을 적용한다.
#. 코드로서 선택한 텍스트를 서식한다.
#. 글머리 기호 목록을 만든다.
#. 번호 매기기 목록을 만든다.
#. 선택한 단락의 들여쓰기를 감소시키고 증가시킨다.
#. 선택한 단락을 인용구로 만든다.
#. 선택한 텍스트에서 링크를 만든다. 이에 관해 :ref:`Add a Link in an HTML
   Component` 에 더 자세한 안내가 있다.
#. 현재 링크를 삭제한다. 
#. 마우스 커서 위치에 이미지를 삽입한다. 이에 관해 :ref:`Add an Image to an HTML Component` 에 더 자세한 안내가 있다.
#. 아래에 설명된 방식으로 HTML 소스 코드에 대한 작업을 한다.


.. _Work with HTML code:


비쥬얼 편집기에서 HTML 코드 작업하기
*****************************************

비쥬얼 편집기에서 만드는 강좌 콘텐츠를 위해 HTML 소스 코드에 대한 작업을 하려면, 편집기 도구 모음에서 
**HTML** 을 클릭한다. 그러면 HTML 소스 코드 편집기가 열린다.

.. image:: ../../../shared/building_and_running_chapters/Images/HTML_source_code.png
 :alt: Image of the HTML source code editor

필요에 따라 HTML 코드를 편집한다. 

비쥬얼 편집기에 있는 HTML 코드 보기에서 사용자 지정 스타일 또는 스크립트를 추가하지 않는 대신, 원본 HTML 편집기(raw HTML editor)를 사용해야 한다.

소스 코드 편집기를 닫고 비쥬얼 편집기에서 변경 내용을 적용하려면 **확인** 을 클릭한다. 그러면 비쥬얼 편집기는 HTML 코드가 유효하다는 것을 확인하려고 한다. 예를 들어, 단락 태그를 닫지 않는 경우, 편집기가 그것을 닫을 것이다. 

.. 주의:: 
 소스 코드 편집기에서 **확인** 을 클릭하면 HTML 구성 요소에 대한 변경 내용을 저장하지 않는다.
 그 후 변경 내용을 저장하기 위해 **저장** 을 클릭한 후 구성 요소를 닫아야 한다. 
 **취소** 를 클릭하면 HTML 소스 코드에서 수행한 변경 내용이 사라진다.

.. _The Raw HTML Editor:

*****************************
HTML 에디터
*****************************

HTML 구성 요소를 위해 원본 편집기를 선택하면 텍스트 편집기에서 콘텐츠를 편집할 수 있다. 

.. image:: ../../../shared/building_and_running_chapters/Images/raw_html_editor.png
 :alt: The raw HTML editor

이때 유효한 HTML을 입력해야 한다. 원본 HTML 편집기가 HTML 코드를 검사 하지 않기 때문에, 철저하게 강좌에 있는 HTML 콘텐츠를 시험해볼 필요가 있다.


.. _HTML Component Templates:

*****************************
HTML 구성요소 템플릿
*****************************

새로운 HTML 구성 요소를 만들 때 템플릿의 목록에서 선택할 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/html_templates.png
 :alt: The list of HTML Component templates

원본 HTML 템플릿은 원본 HTML 편집기를 사용하도록 설정되어 있다. 그외 모든 템플릿은 비쥬얼 편집기를 사용한다. 

어떤 HTML 구성 요소에 대해서라도, 구성 요소를 만드는데 사용된 템플릿에 상관없이 편집기를 변경할 수 있다. 
이에 관해 `Set the Editor for an HTML Component`_ 에 안내되어 있다.



.. _Create an HTML Component:

*****************************
HTML 구성요소 만들기
*****************************

To create an HTML component:

1. **Add New Component** 에서 **HTML** 을 클릭한다.

  .. image:: ../../../shared/building_and_running_chapters/Images/NewComponent_HTML.png
   :alt: Image of adding a new HTML component

2. 템플릿을 선택한다. 

   이제부터 **Text** 를 선택하여, 선택된 비쥬얼 편집기를 통해 빈 구성 요소를 만든다고 가정한다.
   
   학습활동(unit) 아래쪽에 빈 구성요소가 나타난다.

  .. image:: ../../../shared/building_and_running_chapters/Images/HTMLComponent_Edit.png
   :alt: Image of an empty HTML component

3. 해당 구성 요소에서, **편집** 을 클릭한다. 

   비쥬얼 편집기에서 HTML 구성 요소가 열린다.

  .. image:: ../../../shared/building_and_running_chapters/Images/HTMLEditor_empty.png
   :alt: Image of the HTML component editor

4. 강좌 콘텐츠를 입력하고 서식을 지정한다. 필요에 따라 :ref:`Work with HTML code` 할 수도 있다. 

5. 구성 요소 편집기의 오른쪽 상단에서 **설정**을 클릭하고 난 다음, 
    **Display Name** 영역에 텍스트를 입력한다.
   

   편집기로 돌아가려면, 오른쪽 상단에서 **편집기** 를 클릭한다.

6. HTML 구성요소를 저장하려면, **저장** 을 클릭한다. 

비쥬얼 편집기 사용 시, 다음과 같은 작업도 할 수 있다.

* :ref:`Add a Link in an HTML Component`
* :ref:`Add an Image to an HTML Component`
* :ref:`Import LaTeX Code`

.. _Add a Link in an HTML Component:

***********************************
HTML 구성요소에 링크 추가하기
***********************************

비쥬얼 편집기를 사용하여 웹 사이트, 강좌 학습활동, 또는 HTML 구성요소에 있는 파일을 추가하려고 할 때는  **Insert link** 대화상자로 작업할 수 있다.

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

#. 링크로 만들 텍스트를 선택한다.

#. 도구 모음에서 링크 아이콘을 클릭한다.

#. **링크 삽입하기** 대화 상자에서, URL 입력 필드에 원하는 웹사이트의 URL을 입력한다.

   .. image:: ../../../shared/building_and_running_chapters/Images/HTML_Insert-EditLink_Website.png
    :alt: Image of the Insert link dialog box

#. 새 창에서 링크를 열려면, **Target** 입력 필드 옆에 있는 드롭 다운 화살표를 클릭하고 난 다음, 
   **New Window** 를 선택 한다. 그렇지 않은 경우에 기본값을 남겨 둘 수 있다. 
   
   
#. **OK** 를 클릭한다.

#. TML 구성 요소를 저장 하고 링크를 시험해본다.


.. _Add a Link to a Course Unit:


강좌 학습활동 링크 추가하기
***********************************

HTML 구성 요소에서 강좌 학습활동 링크를 추가할 수 있다. 

#. 연결하려고 하는 학습활동의 고유 식별자를 가져온다. 
   이렇게 하려면, 스튜디오에서 학습활동 페이지를 열고, 오른쪽 하단에 있는 
   **학습 활동 위치** 에서, **위치 ID** 를 복사한다.
   
   .. image:: ../../../shared/building_and_running_chapters/Images/UnitIdentifier.png
    :alt: Image of the unit page with the unit identifier circled

#. 링크를 추가 하려는 곳에 HTML 구성 요소를 연다.

#. 링크로 만들려는 텍스트를 선택한다. 

#. 도구 모음에서 링크 아이콘을 클릭한다.

#. **링크 삽입하기** 대화 상자에서, **URL** 입력 필드에 다음을 입력한다.

   ``/jump_to_id/<unit identifier>``

    <unit identifier="">(대괄호 포함)에 2단계에서 복사했던 학습활동 식별자로 대체하고 /를 양쪽에 포함해야 한다. 
   
   .. image:: ../../../shared/building_and_running_chapters/Images/HTML_Insert-EditLink_CourseUnit.png
    :alt: Image of the Insert link dialog box with a link to a unit identifier

#. 새 창에서 링크를 열려면 **Target** 입력 필드 옆에 있는 드롭 다운 화살표를 클릭한 다음 **New Window** 을 선택한다. 
   그렇지 않은 경우에 기본값을 남길 수 있다.

#. **Insert** 를 클릭한다.

#. HTML 구성 요소를 저장 하고 링크를 시험해본다.

.. _Add a Link to a File:


파일에 링크 추가하기
***********************************


담당자는 강좌를 위해 업로드 한 어떤 파일에 대해서도 HTML 구성 요소에서 링크를 추가할 수 있다. 파일 업로드 하기에 대한 자세한 내용은 :ref:`Add Files to a
Course` 을 참조한다.


#. **파일 업로드**  페이지에서 파일의 **Embed URL** 을 복사한다


  .. image:: ../../../shared/building_and_running_chapters/Images/HTML_Link_File.png
   :alt: Image of Files and Uploads page with the URL field circled 
  
  .. 참고:: 
   담당자는 파일에 링크를 포함시키기 위해 **External URL** 이 아닌 **Embed URL**  을 사용 해야 한다.

2. 링크로 만들 텍스트를 선택한다.

#. 도구 모음에서 링크 아이콘을 클릭한다.

#. **링크 삽입하기** 대화 상자에서, **URL** 입력 필드에 다음을 입력한다.

   ``/static/FileName.type``

   전방향 슬래시를 양쪽에 포함하도록 한다 (/).

   .. image:: ../../../shared/building_and_running_chapters/Images/HTML_Insert-EditLink_File.png
    :alt: Image of the Insert link dialog box with a link to a file

#.새 창에서 링크를 열려면 **대상** 입력 필드 옆에 있는 드롭 다운 화살표를 클릭한 다음 **새 창** 을 선택한다. 그렇지 않은 경우에 기본값을 남길 수 있다.

#. **삽입** 을 클릭한다.

#. HTML 구성 요소를 저장 하고 링크를 테스트 한다.

.. _Add an Image to an HTML Component:

***********************************
 HTML 구성요소에 이미지 추가하기
***********************************

K-MOOC 담당자가 비쥬얼 편집기를 사용하면 강좌를 위해 업로드 한 어떤 이미지라도 HTML 구성 요소에 추가할 수 있다. 이미지 업로드하기에 대한 자세한 내용은 :ref:`Add Files to a Course` 을 참조하도록 한다.


.. 참고:: 

. K-MOOC 담당자는 HTML 구성 요소에 이미지를 추가하기 이전에 :ref:`Best Practices for Describing Images` 를 검토하도록 한다.



이미지를 추가하기 위해, K-MOOC 담당자는 강좌에 업로드했던 이미지에 대한 URL이 필요하다. 그런 다음 HTML 구성 요소에서 이미지에 대한 링크를 만들 수 있다

#.. **파일 업로드** 페이지에서 원하는 이미지의 **Embed URL** 을 복사한다.

  .. image:: ../../../shared/building_and_running_chapters/Images/image_link.png
   :alt: Image of the Files & Upload page with the Embed URL for the image
       circled

  .. 참고::
   . K-MOOC 담당자는 이미지를 추가하기 위해 **External URL** 이 아닌 **Embed URL** 을 사용 해야 한다.

2. 도구 모음에서 링크 아이콘을 클릭한다.

#. **링크 삽입하기** 대화 상자에서, **Source** 입력 필드에 다음을 입력한다

   ``/static/FileName.type``

  전방향 슬래시를 양쪽에 포함하도록 한다 (/).

   .. image:: ../../../shared/building_and_running_chapters/Images/HTML_Insert-Edit_Image.png
    :alt: Image of the Insert image dialog box with a reference to a file

4. **이미지 설명** 입력 필드에 대안 텍스트를 입력한다. 이 텍스트는 HTML에서 alt 속성 값이 되고, 강좌에서 완벽하게 접근할 수 있는 텍스트가 되어야 한다. 더 자세한 내용은 :ref:`Best Practices for Describing Images` 를 참조한다. 


#. 필요에 따라 이미지 크기를 사용자 지정한다. 이미지가 같은 너비와 높이 비율을 유지하도록 **제한 비율** 이 선택된 상태를 유지한다.

#. 이미지의 간격 및 테두리를 변경 하려면 **고급** 탭을 클릭한다. 

   .. image:: ../../../shared/building_and_running_chapters/Images/HTML_Insert-Edit_Image_Advanced.png
    :alt: Image of the Insert image dialog box Advanced tab

#.필요에 따라 **수직 공간, 수평 공간, 및 테두리** 를 입력한다. 입력한 값은 **스타일** 입력 필드에 자동으로 추가된다.

#. HTML 구성 요소에 이미지를 삽입 하려면 **확인** 을 클릭한다.

#. HTML 구성 요소를 저장하고 이미지를 테스트 한다.


.. _Import LaTeX Code:

****************************************
HTML 구성요소에 LaTeX 코드 넣기
****************************************

. K-MOOC 담당자는 HTML 구성 요소에 LaTeX 코드를 가져올 수 있다. 예를 들어 다음과 같이 “아름다운 수학공식”를 만들려는 경우 LaTeX 코드를 가져올 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/HTML_LaTeX_LMS.png
 :alt: Image of math formulas created with LaTeX

.. 주의:: 
LaTeX 코드를 XML로 변환하기 위해 스튜디오가 사용하는 LaTeX 프로세서는 제 3 공급업체 도구이다. 따라서 이 기능을 주의하여 사용하는 것이 좋다. LaTeX 프로세서를 사용 할 경우 반드시 프로그램 관리자와 함께 작업하도록 한다

. 이 LaTeX 기능은 기본적으로 작동되지 않는다. 그것을 사용 하려면 강좌에서 고급 설정을 변경해야 한다.

LaTeX 코드를 포함하는 HTML 구성 요소를 만들려면:

#. 강좌에서 정책 키를 사용한다

   #. 스튜디오에서 **설정** 을 클릭 한 다음 **고급 설정** 을 클릭한다.
   #. **LaTeX 컴파일러 사용하기** 정책 키에 대한 입력 필드에서, false를 true로 변경한다.
   #.페이지 하단에 있는, **변경 사항 저장하기** 을 클릭한다.

#. 구성 요소를 생성 하고자 하는 학습활동에서, **새 구성 요소 추가하기** 에서 **html** 을 클릭하고 난 다음,  **라텍스에서 전자 텍스트 작성하기** 를 클릭한다. 새 구성 요소가 해당 학습활동에 추가된다.

#.새 구성 요소를 열려면 **편집** 을 클릭한다. 구성 요소 편집기가 열린다.

  .. image:: ../../../shared/building_and_running_chapters/Images/latex_component.png
   :alt: Image of the HTML component editor with the LaTeX compiler.

4. 구성 요소 편집기에서 **라텍스 소스 컴파일러 실행** 을 클릭한다. 라텍스 편집기가 열린다.

   .. image:: ../../../shared/building_and_running_chapters/Images/HTML_LaTeXEditor.png
    :alt: Image of the HTML component editor with the LaTeX compiler

#.필요에 따라 LaTeX 코드를 작성한다. 또한 K-MOOC 담당자는 오른쪽 하단에서 **업로드** 를 클릭하여 컴퓨터에서 LaTeX 파일을 편집기로 업로드 할 수 있다.

#.필요한 LaTeX 코드를 업로드 또는 작성 했을 경우, 왼쪽 모서리에 있는 **edX XML 컴파일 하기 및 저장하기** 를 클릭한다.

   구성 요소 편집기를 닫는다. K-MOOC 담당자는 라텍스 콘텐츠 모양을 볼 수 있다.

   .. image:: ../../../shared/building_and_running_chapters/Images/HTML_LaTeX_CompEditor.png
    :alt: Image of the LaTeX component

#. 학습활동 페이지에서, K-MOOC 담당자의 콘텐츠가 LMS에서 보이듯이 원하는 방식으로 보이는지 확인하기 위해 **미리 보기** 를 클릭한다.

   오류가 나타나는 경우, 해당 학습활동 페이지로 다시 이동한다. 구성 요소를 다시 열기 위해 **편집** 을 클릭하고 난 다음  그리고 LaTeX 코드를 편집하기 위해 구성 요소 편집기의 왼쪽 아래 모서리에 있는 **라텍스 소스 컴파일러 시작하기** 를 클릭한다.
