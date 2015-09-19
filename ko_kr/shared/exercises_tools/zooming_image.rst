.. _Zooming Image:

##################
이미지 확대/축소 도구
##################

이미지로 된 정보를 학습자에게 제시하는 경우가 있다. 이미지가 크거나 매우 세밀할 경우 학습자는 해당 이미지에 담긴 정보를 확인하지 못할 수 있다. 이 경우 이미지 확대/축소 도구를 이용하여 학습자가 이미지 위에서 마우스를 움직여 이미지 일부를 확대하게 할 수 있다. 아래에 한 예를 제시한다.

.. image:: ../../../shared/building_and_running_chapters/Images/Zooming_Image.png
  :alt: Example zooming image tool showing a chemistry exercise

***********************************
이미지 확대/축소 도구의 구성요소
***********************************

이미지 확대/축소 도구를 생성하려면 다음 파일이 필요하다.

* 학습 활동 수행 중 학습자에게 제시할 이미지
* 학습자가 일반 이미지를 클릭할 경우 확대 영역에 표시될 이미지. 이 이미지는 해당 일반 이미지보다 클 수 있다.
*  **jquery.loupeAndLightbox.js** 자바스크립트 파일. 이미지 확대/축소 도구는 모두 이 자바스크립트 파일을 사용한다. 이 파일을 변경하지 않는 것이 좋다. `이 파일을 내려 받으려면 여기를 클릭한다. <http://files.edx.org/jquery.loupeAndLightbox.js>`_ . 내려 받은 파일을 컴퓨터에 저장하려면 **다른 이름으로 링크 저장하기** 를 클릭한다.  

****************************
이미지 확대/축소 도구 생성하기
****************************

#. 준비한 일반 크기 이미지 파일과 **jquery.loupeAndLightbox.js** 를  **파일 업로드** 페이지에 업로드한다. 이와 관련한 보다 구체적인 정보를 강좌에 :ref:`Add Files to a Course` 에서 확인할 수 있다.  

#. **신규 구성요소 추가** 에서 **HTML** 을 클릭한 후 **이미지 확대/축소(Zooming Image)** 를 클릭한다. 

#. 신규 구성요소가 표시되면 **편집** 을 클릭한다.

#. 구성요소 편집기에서 초기 문제 텍스트를 원하는 텍스트로 바꾼다.

#. **HTML** 탭으로 전환한다. 

#. 다음 플레이스홀더를 원하는 콘텐츠로 교체한다.

   1. 다음 파일명과 경로를, 사용자가 보통 이미지 위에서 마우스를 움직일 때 확대되어 나타나는 이미지의 파일명과 경로로 바꾼다.
     **https://studio.edx.org/c4x/edX/DemoX/asset/pathways_detail_01.png**
     이를테면 파일명 및 경로는 **/static/Image1.jpg** 일 수 있다. 

   2.  다음 파일명과 경로를, 페이지가 열릴 때 표시되는 이미지의 파일명과 경로로 바꾼다.
     **https://studio.edx.org/c4x/edX/DemoX/asset/pathways_overview_01.png**
     이를테면 파일명과 경로는 **/static/Image2.jpg** 일 수 있다. 
     
   3. 다음 파일명과 경로를, 강좌에 해당하는 자바스크립트 파일의 파일명과 경로로 바꾼다.
     **https://studio.edx.org/c4x/edX/DemoX/asset/jquery.loupeAndLightbox.js**
     이미 **jquery.loupeAndLightbox.js** 를 파일 및 업로드 페이지에 업로드했기 때문에 파일명과 경로는 **/static/jquery
     .loupeAndLightbox.js**. 가 된다.  

   4. (선택) 확대 영역을 보다 확대하거나 축소하려면 350을 기준으로 **width** 및 **height** 값을 높이거나 낮추십시오. 가령, 두      수치를 450으로 증가시킬 수 있다. 또, 가로 방향으로 넓게 퍼진 타원형 확대 이미지를 원한다면 **width** 값을 500, **height** 값을 150으로 할 수 있다. 파일 확대/축소 도구에 포함된 HTML은 다음 그림과 유사한 형태를 취하고 있다.
  
   .. image:: ../../../shared/building_and_running_chapters/Images/ZoomingImage_Modified.png
     :alt: Example HTML for a zooming image tool

#.  **저장** 을 클릭하여 HTML 구성요소를 저장한다. 


