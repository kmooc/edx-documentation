.. _Image Mapped Input:

###########################
이미지맵 입력 문제
###########################

이미지맵 입력 문제에서, 학습자는 이미지에 정의된 영역 내부를 클릭한다. 문제의 본문에서 좌표를 포함하여 이 영역을 정의한다.

.. image:: ../../../shared/building_and_running_chapters/Images/ImageMappedInputExample.png
 :alt: Image of an image mapped input problem

****************************************
이미지맵 문제 만들기
****************************************

이미지맵 입력 문제를 만들려면:

#. 문제를 만들려는 학습활동에서, **새 구성 요소 추가** 아래에 *문제** 를 클릭한 다음 **고급** 탭을 클릭한다.
#. **이미지맵 입력** 을 클릭한다.
#. 표시되는 구성요소에서, **편집** 을 클릭한다.
#. 구성 요소 편집기에서, 예제 코드를 자신의 코드로 바꾼다.
#. **저장** 을 클릭한다.

**문제 코드**:

.. code-block:: xml

  <problem>
    <p><b>Example Problem</b></p>
     <startouttext/>
      <p>In the image below, click the triangle.</p>
      <endouttext/>
      <imageresponse>
      <imageinput src="/static/threeshapes.png" width="220" height="150" rectangle="(80,40)-(130,90)" />
      </imageresponse>
  </problem>


.. _Image Mapped Input Problem XML:

******************************
이미지맵 입력 문제 XML
******************************

==========
템플릿
==========

.. code-block:: xml

  <problem>
    <startouttext/>
      <p>In the image below, click the triangle.</p>
    <endouttext/>
        <imageresponse>
         <imageinput src="IMAGE FILE PATH" width="NUMBER" height="NUMBER" rectangle="(X-AXIS,Y-AXIS)-(X-AXIS,Y-AXIS)" />
        </imageresponse>
  </problem>

=====
테그
=====

* ``<imageresponse>``: 문제가 이미지맵 입력 문제임을 나타낸다.
* ``<imageinput>``: 학습자가 클릭해야 하는 파일에서 이미지 파일 및 영역을 지정한다.

**Tag:** ``<imageresponse>``

문제가 이미지맵 입력 문제임을 나타낸다.

  속성

  (none)

  Children

  * ``<imageinput>``

**Tag:** ``<imageinput>``

학습자가 클릭해야 하는 파일에서 이미지 파일 및 영역을 지정한다.

  Attributes

   .. list-table::
      :widths: 20 80

      * - Attribute
        - Description
      * - src (필수 사항)
        - 이미지의 URL
      * - height (필수 사항)
        - 픽셀 단위로 이미지의 높이
      * - width (필수 사항)
        - 픽셀 단위로 이미지의 너비
      * - rectangle (필수 사항)
        - (<start_width>,<start_height>)-(<end_width>,<end-height>)의 형식에 포함된 4개의 값에 대한 속성이다. 모든 좌표는 위 왼쪽 모서리에서 (0,0)으로 시작하고, 오른쪽 하단 모서리를 향해 값이 증가한다. 영어 읽기의 진행과 매우 비슷하다. 정의된 두 개의 좌표는 학습자가 내부를 클릭할 수 있는 박스의 두 반대편 모서리를 형성한다. 

  Children
  
  (none)

