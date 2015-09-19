.. _Molecule Viewer:

#######################
분자 뷰어 도구
#######################

Studio는 분자를 다루기위한 두 가지 도구를 제공한다.

* **분자 뷰어 도구** 를 이용하여 학습자가 볼 수 있는 3차원 분자 모형을 생성할 수 있다.
* **분자 편집기** 문제 유형을 이용하여 학습자 스스로가 원하는 대로 분자 구조를 구성할 수 있다. :ref:`Molecule Editor` 에서 이 도구에 관한 보다 자세한 정보를 확인할 수 있다.

두 도구 모두 **Jmol** 이 개발한 자바스크립트 기반 분자 뷰어 JSmol을 사용한다. (Studio는 이 두 가지 도구를 자동으로 사용한다. 별도로 내려받을 필요가 없다.) JSmol에 관한 보다 자세한 정보를 `JSmol <http://sourceforge.net/projects/jsmol/>`_ 에서 확인할 수 있다.

다음 이미지는 강좌에서 사용할 수 있는 분자 뷰어 도구를 나타낸다.

.. image:: ../../../shared/building_and_running_chapters/Images/MoleculeViewer.png
   :width: 500
   :alt: Image of molecule viewer showing a molecule of Ciprofloxacin

.. note:: 분자 뷰어 도구를 생성하려면 아마존 웹 서비스 심플 스토리지 서비스(Amazon Web Services Simple Storage Service, AWS S3)와 같은 서드파티 파일 호스팅 사이트에 파일을 업로드할 권한 반드시 있어야 한다. 분자 뷰어를 생성하는 경우 대단히 많은 파일을 포함하는 폴더 1개를 해당 호스팅 사이트에 업로드하게 된다. 

.. _Create the Molecule Viewer:

*******************************
분자 뷰어 도구 생성하기
*******************************

분자 뷰어 도구를 생성하려면 다음과 같은 몇 가지 단계를 거쳐야 한다.

#. `BioTopics website <http://www.biotopics.co.uk/jsmol/molecules>`_ 및 edX에서 파일을 내려받다.
#. 내려받은 파일 중 일부의 저장 장소를 변경하거나 편집한다.
#. 내려받아 편집한 모든 파일을 하나의 폴더에 넣고 이 폴더를 이용하는 파일 호스팅 사이트에 올린다.
#. IFrame을 포함하는 HTML 구성 요소를 Studio에 생성한다. 이 IFrame은 파일 호스팅 사이트에 올린 파일들을 참조하게 된다.

================================================
BioTopics 및 edX에서 파일 내려받기
================================================

#. 구성하고자 하는 분자에 해당하는 .mol 파일을 생성하거나 내려받는다. `BioTopics website <http://www.biotopics.co.uk/jsmol/molecules>`_ 에서 다양한 .mol 파일을 내려받을 수 있다. 쉽게 찾을 수 있는 장소에 해당 파일을 저장한다.
#. edX에서  `MoleculeViewerFiles.zip <http://files.edx.org/MoleculeViewerFiles.zip>`_ 를 내려받다.
#. 내려받은 `MoleculeViewerFiles.zip <http://files.edx.org/MoleculeViewerFiles.zip>`_ 의 압축을 푼다.

   압축을 풀면 **MoleculeViewerFiles** 라는 폴더가 생성된다. 이 안에는 다음과 같은 폴더 및 파일이 들어있다.

    * data (폴더)
    * j2s (폴더)
    * js (폴더)
    * MoleculeViewer.html (파일)

================================================================
.mol 저장 위치 변경하고 MoleculeViewer.html 편집하기
================================================================

#. BioTopics에서 내려받은 .mol 파일을 edX에서 내려받은 **데이터** 폴더로 옮긴다.
#. 다음과 같이 MoleculeViewer.html 파일을 편집한다.


   #. 텍스트 편집기에서 MoleculeViewer.html 파일을 연다.
   #. MoleculeViewer.html 파일의 19행에서 **Example.mol** 을 “원하는 파일명.mol” 으로 바꾼다. 가령 Glucose.mol이라는 파일을 다운로드 했다면 해당 파일의 19번째 행은 다음과 같다.

   		``script: "set antialiasDisplay; background black; load data/Glucose.mol;"``

3. MoleculeViewer.html을 저장한다.

================================
호스팅 사이트에 파일 올리기
================================

#. **MoleculeViewerFiles** 폴더에 다음과 같은 폴더 및 파일이 포함돼 있는지 확인한다.

   * data (폴더): 위에서 .mol을 추가한 폴더이다
   * j2s (폴더)
   * js (폴더)
   * MoleculeViewer.html (파일): 위에서 19번째 행의 내용을 수정한 파일이다.

2. **MoleculeViewerFiles** 폴더 전체를 파일 호스팅 사이트에 업로드한다.

   .. note:: 이 폴더에는 많은 파일이 들어 있다. 네트워크 속도가 빠르더라도 업로드 완료까지 몇 분이 걸릴 수도 있다.

===============================
Studio에서 구성 요소 생성하기
===============================

#. Studio에 들어가 분자 뷰어를 추가하고자 하는 학습 활동을 연다.
#. **신규 구성요소 추가** 에서 **HTML** 을 클릭한 후 **IFrame** 을 클릭한다.
#. 구성요소 편집기가 열리면 기존 내용을 없애고 원하는 문자열을 입력한다.
#. 툴바에서 **HTML** 을 클릭한다.
#. **HTML 소스 코드 박스** 에서 분자 뷰어를 나타내고자 하는 장소에 다음 행을 입력한다.

   ``<p><iframe name="moleculeiframe" src="https://path_to_folder/MoleculeViewerFiles/MoleculeViewer.html" width="500" height="500"></iframe></p>``

6. ``path_to_file`` 을 이용하는 파일 호스팅 사이트로 바꾼다. 이를테면 해당 행은 다음과 같은 형태가 될 수 있다.

   ``<p><iframe name="moleculeiframe" src="https://myfiles.example.com/MoleculeViewerFiles/MoleculeViewer.html" width="500" height="500"></iframe></p>``

7. **OK** 를 클릭하여 **HTML 소스 코드** 박스를 닫은 후 **저장** 을 클릭하여 해당 구성 요소를 저장한다.
#. **미리보기** 를 클릭하여 생성한 구성 요소를 학습자가 볼 수 있도록 한다.
