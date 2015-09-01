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

#. 새 창에서 링크를 열려면 **Target** 입력 필드 옆에 있는 드롭 다운 화살표를 클릭한 다음 **New Window**을 선택한다. 
   그렇지 않은 경우에 기본값을 남길 수 있다.

#. **Insert** 를 클릭한다.

#. HTML 구성 요소를 저장 하고 링크를 시험해본다.

.. _Add a Link to a File:


Add a Link to a File
***********************************

You can add a link in an HTML component to any file you've uploaded for the
course. For more information about uploading files, see :ref:`Add Files to a
Course`.

#. On the **Files & Uploads** page, copy the **Embed URL** of the file.


  .. image:: ../../../shared/building_and_running_chapters/Images/HTML_Link_File.png
   :alt: Image of Files and Uploads page with the URL field circled 
  
  .. note:: 
   You must use the **Embed URL** to link to the file, not the **External URL**.

2. Select the text that you want to make into the link.

#. Click the link icon in the toolbar.

#. In the **Insert link** dialog box, enter the following in the **URL** field.

   ``/static/FileName.type``

   Make sure to include both forward slashes (/).

   .. image:: ../../../shared/building_and_running_chapters/Images/HTML_Insert-EditLink_File.png
    :alt: Image of the Insert link dialog box with a link to a file

#. If you want the link to open in a new window, click the drop-down arrow next
   to the **Target** field, and then select **New Window**. If not, you can
   leave the default value.

#. Click **Insert**.

#. Save the HTML component and test the link.

.. _Add an Image to an HTML Component:

***********************************
Add an Image to an HTML Component
***********************************

When using the visual editor, you can add any image that you have uploaded for
the course to an HTML component. For more information about uploading images,
see :ref:`Add Files to a Course`.

.. note:: 
 Review :ref:`Best Practices for Describing Images` before you add images to
 HTML components.

To add an image, you'll need the URL of the image that you uploaded to the
course. You'll then create a link to the image in the HTML component.

#. On the **Files & Uploads** page, copy the **Embed URL** of the image that you
   want.

  .. image:: ../../../shared/building_and_running_chapters/Images/image_link.png
   :alt: Image of the Files & Upload page with the Embed URL for the image
       circled

  .. note:: 
   You must use the **Embed URL** to add the image, not the **External URL**.

2. Click the image icon in the toolbar.

#. In the **Insert image** dialog box, enter the following in the **Source**
   field.

   ``/static/FileName.type``

   Make sure to include both forward slashes (/).

   .. image:: ../../../shared/building_and_running_chapters/Images/HTML_Insert-Edit_Image.png
    :alt: Image of the Insert image dialog box with a reference to a file

4. Enter alternative text in the **Image description** field. This text becomes
   the value of the ``alt`` attribute in HTML and is required for your course to
   be fully accessible. See :ref:`Best Practices for Describing Images` for more
   information.

#. As needed, customize the image dimensions. Keep **Constrain proportions**
   checked to ensure the image keeps the same width and height proportions.

#. To change the spacing and border of the image, click the **Advanced** tab. 

   .. image:: ../../../shared/building_and_running_chapters/Images/HTML_Insert-Edit_Image_Advanced.png
    :alt: Image of the Insert image dialog box Advanced tab

#. Enter the **Vertical space**, **Horizontal space**, and **Border** as needed.
   The values you enter are automatically added to the **Style** field.

#. Click **OK** to insert the image in the HTML component.

#. Save the HTML component and test the image.


.. _Import LaTeX Code:

****************************************
Import LaTeX Code into an HTML Component
****************************************

You can import LaTeX code into an HTML component. You might do this, for
example, if you want to create "beautiful math" such as the following.

.. image:: ../../../shared/building_and_running_chapters/Images/HTML_LaTeX_LMS.png
 :alt: Image of math formulas created with LaTeX

.. warning:: 
 The LaTeX processor that Studio uses to convert LaTeX code to XML is a third-
 party tool. We recommend that you use this feature with caution. If you do use
 it, make sure to work with your Program Manager.

This feature is not enabled by default. To enable it, you have to change the
advanced settings in your course.

To create an HTML component that contains LaTeX code:

#. Enable the policy key in your course.

   #. In Studio, click **Settings**, and then click **Advanced Settings**.
   #. In the field for the **Enable LaTeX Compiler** policy key, change
      **false** to **true**.
   #. At the bottom of the page, click **Save Changes**.

#. In the unit where you want to create the component, click **html** under
   **Add New Component**, and then click **E-text Written in LaTeX**. The new
   component is added to the unit.

#. Click **Edit** to open the new component. The component editor opens.

  .. image:: ../../../shared/building_and_running_chapters/Images/latex_component.png
   :alt: Image of the HTML component editor with the LaTeX compiler.

4. In the component editor, click **Launch Latex Source Compiler**. The LaTeX
   editor opens.

   .. image:: ../../../shared/building_and_running_chapters/Images/HTML_LaTeXEditor.png
    :alt: Image of the HTML component editor with the LaTeX compiler

#. Write LaTeX code as needed. You can also upload a LaTeX file into the editor
   from your computer by clicking **Upload** in the bottom right corner.

#. When you have written or uploaded the LaTeX code you need, click **Save &
   Compile to edX XML** in the lower-left corner.

   The component editor closes. You can see the way your LaTeX content looks.

   .. image:: ../../../shared/building_and_running_chapters/Images/HTML_LaTeX_CompEditor.png
    :alt: Image of the LaTeX component

#. On the unit page, click **Preview** to verify that your content looks the way
   you want it to in the LMS.

   If you see errors, go back to the unit page. Click **Edit** to open the
   component again, and then click **Launch Latex Source Compiler** in the
   lower-left corner of the component editor to edit the LaTeX code.
