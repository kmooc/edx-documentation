.. _IFrame:

##################
IFrame 도구
##################

IFrame은 모든 인터넷 사이트에 있는 채점되지 않은 연습 및 도구를 강좌의 본문에 통합할 수 있도록 허용한다. IFrame은 HTML 구성 요소 내에서 나타나고, 연습 및 도구는 IFrame 내에 나타난다. IFrame 은 직접 만든 도구 또는 제 3자 도구를 포함할 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/IFrame_1.png
  :alt: IFrame tool showing a Euler line exercise
  :width: 500

IFrame은 개념을 설명하는데 적절한 도구이지만 채점되지 않으며 학습자 데이터를 저장하는데 적절하다.  채점되는 도구 및 연습을 추가하려면, :ref:`custom JavaScript problem<Custom JavaScript>`  (사용자 지정 JavaScript 문제) 또는 :ref:`LTI component<LTI Component>`  (LTI 구성 요소)와 같은 도구를 추가하도록 한다. 

IFrame에 대한 자세한 내용은 `IFrame specification <http://www.w3.org/wiki/HTML/Elements/iframe>`_  (IFrame 사양)을 참조하도록 한다.

****************************
IFrame 도구 만들기
****************************

IFrame에서 연습 또는 도구를 추가하려면, IFrame HTML 구성 요소를 만들고, 연습 또는 도구를 포함하는 페이지의 URL을 구성 요소에 추가해야 할 것이다.  또한 IFrame 전과 후에 텍스트와 이미지를 모두 추가할 수 있다.

.. note:: IFrame에서 연습 또는 도구를 추가하려면, IFrame HTML 구성 요소를 만들고, 연습 또는 도구를 포함하는 페이지의 URL을 구성 요소에 추가해야 할 것이다. 또한 IFrame 전과 후에 텍스트와 이미지를 모두 추가할 수 있다.

#. **신규 구성요소 추가** 에서, **html** 을 클릭한 다음, **IFrame** 을 클릭한다. 

#. 표시되는 신규 구성요소에서, **편집** 을 클릭한다.

#. 구성요소 편집기의 도구 모음에서, **HTML** 을 클릭한다.

#. HTML 소스 코드 편집기에서, 다음의 HTML (7번째 줄)을 찾는다. 이 HTML은 ``<IFrame>`` 요소를 포함한다:

   .. code-block:: html

      <p><iframe src="https://studio.edx.org/c4x/edX/DemoX/asset/eulerLineDemo.html" width="402" height="402" marginwidth="0" marginheight="0" frameborder="0" scrolling="no">You need an iFrame capable browser to view this.</iframe></p>

5. **src** 속성에 있는 기본 URL( **https://studio.edx.org/c4x/edX/DemoX/asset/eulerLineDemo.html** ) 을 연습문제 및 도구를 포함하는 페이지의 URL로 바꾼다. **이 URL는 https로 시작 해야 한다**. URL을 둘러싼 인용 부호를 삭제하지 않아야 한다.

#. 원하는 다른 설정을 지정 하려면 IFrame 요소에 있는 속성을 변경한다. 이러한 설정에 대한 더 자세한 내용은, :ref:`IFrame Settings` (IFrame 설정)을 참조하도록 한다. 열기 및 닫기 ``<IFrame>`` 태그 사이에 텍스트를 변경할 수 있다. 학습자가 IFrame을 지원하지 않는 브라우저를 사용하는 경우에만 이 텍스트를 보게 된다.

7. HTML 소스 코드 편집기를 닫고 영상 편집기로 돌아가기 위해 **확인** 을 클릭한다.

#. 비주얼 편집기에서, 기본 텍스트를 자신의 텍스트로 바꾼다.

#. **저장** 을 클릭한다.

.. _IFrame Settings:

======================
IFrame 설정
======================

IFrame에 대한 설정을 지정 하려면, 열기 ``<IFrame>`` 태그 내부에 해당 속성을 추가, 제거 또는 변경해야 할 것이다. ``<IFrame>`` 태그는 원하는 웹 페이지의 URL을 지정하는 **src** 속성을 **반드시** 포함해야 한다. 다른 속성은 선택 사항이다.

원하는 순서대로 이러한 속성을 추가할 수 있다.

.. list-table::
   :widths: 20 80
   :header-rows: 1
 
   * - 속성
     - 설명
   * - **src** (필수)
     - 연습 및 도구를 포함하는 페이지의 URL을 지정한다.
   * - **width** 및 **height** (선택)
     - 픽셀 또는 백분율로 IFrame의 너비 및 높이를 지정한다. 픽셀 단위로 값을 지정 하려면 숫자를 입력한다. 백분율로 값을 지정 하려면 숫자 뒤에 백분율 기호를 입력한다.

       너비 및 높이를 지정하지 않으면, IFrame은 연결된 페이지가 설정한 수치를 사용한다. 이 수치는 웹사이트에 따라 다르다. IFrame의 너비 및 높이를 변경하려면, 연결된 페이지의 콘텐츠에서 크기를 조정할 수 있다. 그렇지 않으면 콘텐츠 중 일부만 표시 될 수 있다.

   * - **marginwidth** 및 **marginheight** (선택)
     - IFrame의 가장자리와 픽셀 단위의 연습문제 및 도구 사이의 공간 크기를 지정한다. 
   * - **frameborder** (선택) 
     - 주위에 테두리 표시 여부를 지정한다. 값이 0 이면 아무 테두리가 나타나지 않는다. 값이 임의의 양수이면, 테두리가 나타난다.
   * - **scrolling** (선택 사항)
     - IFrame이 포함하고 있는 연습문제 및 도구보다 더 작으면, 이용자가 IFrame의 콘텐츠 전부를 볼 수 있도록 스크롤 막대가 표시 되는지 여부를 지정한다. 예를 들어, IFrame에 있는 콘텐츠가 매우 긴 경우, IFrame의 높이를 더 작은 숫자로 설정하고 첫 번째 이미지 아래와 같이 이용자를 위해 세로 스크롤 막대를 추가 수 있다.

예를 들어, 아래 ``<IFrame>`` 요소 각각에서 서로 다른 설정들이 IFrame에 어떻게 영향을 미치는지 비교한다. 

.. code-block:: html

      <p><iframe src="https://studio.edx.org/c4x/edX/DemoX/asset/eulerLineDemo.html" width="442" height="200" marginwidth="20" marginheight="20" frameborder="1" scrolling="yes">You need an iFrame capable browser to view this.</iframe></p>

.. image:: ../../../shared/building_and_running_chapters/Images/IFrame_3.png
   :alt: IFrame with only top half showing and vertical scroll bar on the side
   :width: 500

.. code-block:: html

      <p><iframe src="https://studio.edx.org/c4x/edX/DemoX/asset/eulerLineDemo.html" width="550" height="250" marginwidth="30" marginheight="60" frameborder="1" scrolling="no">You need an iFrame capable browser to view this.</iframe></p>

.. image:: ../../../shared/building_and_running_chapters/Images/IFrame_4.png
   :alt: 
   :width: 500

IFrame 속성에 대한 더 자세한 내용은 `IFrame specification <http://www.w3.org/wiki/HTML/Elements/iframe>`_ 를 참조하도록 한다.
