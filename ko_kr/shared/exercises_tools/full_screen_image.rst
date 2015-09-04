.. _Full Screen Image:

######################
전체 화면 이미지 도구
######################

일부 큰 이미지는 강좌 내용에서 학습자가 보기에 어려울 수 있다. 전체 화면 이미지 도구는 학습자가 문맥에서 모든 세부 정보를 볼 수 있도록 이미지를 확대할 수 있도록 허용한다. 

****************************************
학습자 화면에서 전체 화면 이미지 보기
****************************************

학습자 학습활동 페이지에서 전체 화면 이미지를 본다. 학습자 이미지 위에 마우스 포인터를 가져가면 **전체 화면** 버튼이 나타난다.

.. image:: ../../../shared/building_and_running_chapters/Images/image-modal.png
 :alt: Image of the full screen image tool with the Full Screen button.

학습자가 **전체 화면** 을 클릭하면, 이미지가 열리고 전체 브라우저 창에 표시된다. **닫기** , **확대** 및 **축소**  버튼들이 표시된다:

.. image:: ../../../shared/building_and_running_chapters/Images/image-modal-window.png
 :alt: Image of the Image Modal tool with the Full Screen button.

그러면 학습자는 이미지 위에서 확대 할 수 있고, 이미지의 원하는 부분을 보기 위해 이미지를 drag (드래그) 할 수 있다:

.. image:: ../../../shared/building_and_running_chapters/Images/image-modeal-zoomed.png
 :alt: Image of the Image Modal tool with the Full Screen button.

******************************
전체 화면 이미지 만들기
******************************

#. **파일 업로드** 페이지에 이미지 파일을 업로드한다. 이 작업을 수행하는 방법에 대한 더 자세한 내용은 :ref:`Add Files to a Course` (강좌에 파일 추가하기)를 참조하도록 한다.

#. **새 구성 요소 추가** 에서, **html** 을 클릭한 다음, **전체 화면 이미지** 를 클릭한다.

#. 표시되는 새 구성 요소에서, **편집** 을 클릭한다.

#. 구성 요소 편집기에서, 기본값으로 설정되어 있는 제목을 바꾸고, 지침 단락을 제거하고, 필요에 따라 텍스트를 추가할 수 있다.

#. **HTML** 탭으로 바꾼다.

#. 다음의 자리 표시자를 자신의 콘텐츠로 대체한다.

   * <a>요소의 href 속성의 값을 이미지에 대한 경로로 대체한다. 클래스 속성의 값은 변경하지 않는다. 예를 들면:

     **<a href="/static/Image1.jpg" class="modal-content">**

   * 2.	<img> 요소의 src 속성의 값을 이미지에 대한 경로로 대체한다. 예를 들면:
     
     **<img alt="Full screen image" src="/static/Image1.jpg"/>**

   * Src 및 href 속성의 값은 동일해야 하며, 클래스 속성은 변경하지 않도록 한다. 샘플 코드는 다음과 같이 표시된다.

   .. code-block:: xml

     <h2>Sample Image Modal</h2>
     <a href="/static/Image1.jpg" class="modal-content">
     <img alt="Full screen image" src="/static/Image1.jpg"/>
     </a>

   .. 참고:: 전체 화면 이미지로 만든 구성 요소 뿐만 아니라, HTML 구성 요소에서 이와 동일한 HTML 코드를 사용할 수 있다.

#. HTML 구성 요소를 저장 하기 위해 **저장** 을 클릭한다.
