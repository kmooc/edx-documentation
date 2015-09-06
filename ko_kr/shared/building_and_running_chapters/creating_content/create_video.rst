.. _Working with Video Components:

#############################
동영상 구성요소
#############################

**********************
동영상 소개
**********************

적극적으로 학습이 이루어지도록 하기 위해 강좌 동영상을 만들 수 있으며 토의 및 문제 등과 같은 구성요소를 강좌에 추가할 수 있다. 강좌에 동영상는 몇 가지 단계가 있다.

#. :ref:`Create the Video`.
#. :ref:`Create Transcript`.
#. :ref:`Post the Video Online`.
#. :ref:`Create a Video Component`.

또한 다음을 참조하도록 한다:

* :ref:`Video TOC`
* :ref:`Additional Transcripts`
* :ref:`Steps for sjson files`

.. 참고:: 강좌에 동영상을 추가하기 전에 :ref:`Best Practices for Accessible Media` 를 검토하도록 한다.

강좌 운영팀은 동영상을 보호하도록, edX 동영상 플레이어는 기본적으로 학습자에게 동영상 URL을 숨긴다. 이 기능은 YouTube 동영상 및 다른곳에 게시한 동영상을 포함하여 모든 동영상 파일에 대해 적용된다.  
동영상 구성요소에 대해 **동영상 다운로드 허용** 옵션을 선택하는 경우, 학습자는 동영상을 다운로드 할 수 있다. YouTube가 아닌 동영상을 온라인에 게시하는 것에 대한 자세한 내용은 :ref:`Post the Video Online` 를 참조하도록 한다. 동영상 구성 요소를 만들 때 설정할 수 있는 옵션에 대한 자세한 내용은 :ref:`Video Advanced Options` 아래에 있는 :ref:`Create a Video Component` 을 참조하도록 한다. 
 
.. _Create the Video:

************************
1단계. 동영상 만들기
************************

동영상은 강좌에 넣고 싶은 어떤 콘텐츠라도 포함할 수 있다. 'Creating Videos'_ 의 `edX101 Overview of Creating an edX Course`_  주제는 좋은 동영상 콘텐츠를 만들기 위한 유용한 정보를 담고 있다. 

.. _Compression Specifications:

====================================
압축 사양
====================================

동영상을 만들 때 edX는 다음 압축 사양을 권장한다. (참고로 사양은 권장사항이며 필수적 것은 아니다.)

.. list-table::
   :widths: 10 20 20
   :stub-columns: 1

   * - Output
     - **Publish to YouTube**
     - **Publish downloadable file to AWS S3**
   * - Codec
     - H.264 .mp4
     - H.264 .mp4
   * - Resolution & Frame Rate (see note)
     - 1920x1080, progressive, 29.97 fps 
     - 1280x720, progressive, 29.97 fps
   * - Aspect
     - 1.0
     - 1.0
   * - Bit Rate
     - VBR, 2 pass 
     - VBR, 2 pass  
   * - Target VBR
     - 5 mbps
     - 1 mbps
   * - Max VBR
     - 7.5 mbps
     - 1.5 mbps
   * - Audio
     - AAC 44.1 / 192 kbps
     - AAC 44.1 / 192 kbps

.. note:: 일반적으로 미디어 파일을 만들 때 사용된 동일한 프레임 속도로 동영상을 내보낼 수 있다. 예를 들어 PAL 시스템을 사용하는 국가에서 동영상 파일을 만들 경우 29.97의 NTSC 표준 대신 25 fps에서 내보낸다.

.. _Video Formats:

==================
동영상 포맷
==================

edX 동영상 플레이어는 .mp4,.webm,.mpeg, .ogg 형식의 동영상을 지원한다. 그러나, 모든 표준 브라우저에서 동영상을 재생할 수 있는지 확인하기 위해, **.mp4 또는.webm 형식 사용** 을 적극 권장한다.

.. _Create Transcript:

*********************************************
2단계. 동영상 자막 만들기 및 찾기 
*********************************************

동영상 자막은 필수적이다. 자막은 모국어 이외의 언어로 동영상을 보거나, 동영상을 볼 수 없거나, 또는 동영상 콘텐츠를 검토하기 원하는 학습자에게 유용하다. 학습자가 오프라인으로 자막을 볼 수 있도록 자막 다운로드를 허용할 수 있다. 동영상 구성요소를 만들 때 동영상과 함께 자막을 연결하도록 한다. 

재생시간이 포함된 SubRip 텍스트 (.srt) 형식의 자막은 권장된다. .srt 형식의 자막은 동영상 옆에서 동영상이 재생되면 자동으로 스크롤된다. 학습자는 자막에서 단어를 클릭하여 동영상 내에서 그 단어가 말해진 지점으로 이동할 수 있다.

.srt 형식의 자막을 만들거나 찾기 위해, 캡션 서비스를 제공하는 회사와 함께 작업할 수 있다. EdX는 `3Play Media <http://www.3playmedia.com>`_ 와 협력하고 있으며, `YouTube <http://www.youtube.com/>`_ 또한 캡션 서비스를 제공한다.


.srt 파일을 업로드 할 때 .txt 파일이 자동으로 만들어진다. 학습자가 자막 파일을 다운로드 하도록 허용할 수 있다. 학습자가 자막을 다운로드 하는 것을 허용하는 경우, 동영상 아래에 **자막 다운로드** 버튼이 나타난다. 학습자는 .srt 또는 .txt  자막을 다운로드 하기 위해 **SubRip (.srt) 파일** 또는 **텍스트 (.txt) 파일** 을 선택할 수 있다. 

.. image:: ../../../shared/building_and_running_chapters/Images/Video_DownTrans_srt-txt.png
   :width: 500
   :alt: Video status bar showing srt and txt transcript download options

또한 다른 형식 (예: .pdf 등)으로 자막을 제공할 수 있고, 다른 언어 자막도 제공할 수도 있다. 자세한 정보를 위해 :ref:`Additional Transcripts` 를 참조한다.

.. note:: 일부 강좌는 동영상 자막으로 .sjson 파일을 사용했다. .sjson 파일은 더 이상 권장되지 않는다; 그러나 강좌에서 이 형식의 자막을 사용하는 경우 :ref:`Steps for sjson files` 를 참조하도록 한다.

.. _Post the Video Online:

*****************************
3단계. 온라인 동영상 게시하기
*****************************

모든 강좌 동영상은 YouTube에 게시되어야 한다. 기본적으로 edX 동영상 플레이어는 YouTube 동영상에 접근할 수 있다.

그러나 YouTube를 사용할 수 없는 곳이 있기 때문에, `Amazon S3<http://aws.amazon.com/s3/>`_ 와 같은 제3사이트에 강좌 동영상의 자막을 게시할 것을 권장한다. 학습자가 강좌에서 동영상을 볼 때, 학습자의 위치에서 YouTube를 사용할 수 없는 경우 또는 YouTube 동영상이 재생되지 않는 경우, 백업 사이트에 있는 동영상이 자동으로 재생되기 시작한다. 또한 학습자가 백업 사이트에서 동영상을 다운로드 하도록 허용할 수 있다.

동영상을 온라인에 게시한 후, 동영상에 대한 URL이 있는지 반드시 확인한다. 하나 이상의 장소에서 동영상의 복자막을 호스트 하는 경우, 각 동영상 위치에 대한 URL을가지고 있는지 확인해야 한다.

==================
YouTube
==================

동영상을 만든 후 `YouTube<http://www.youtube.com/>`_ 에 동영상을 업로드 하도록 한다.

.. note:: YouTube는 15분 분량의 동영상만을 올릴 수 있다. 0.75-속도 옵션을 만들려고 할 경우, YouTube가 모든 속도로 호스팅할 수 있도록 1.0-속도로 11.25분 걸리는지 확인해야 한다. YouTube는 이 제한으로부터 자유로운 유료 계정도 제공하고 있다.

==================
다른 사이트
==================

모든 동영상 백업사이트를 사용할 수 있다. 그러나, 동영상을 게시하는 사이트는 심각한 트래픽을 겪을 수 있음을 유념해야 한다.

.. note:: 제3의 사이트에 게시하는 동영상에 대한 URL은 .mp4,.webm,.mpeg, .ogg 로 끝나야 한다. (모든 표준 브라우저가 동영상을 재생할 수 있는지 확인하기 위해, .mp4 또는.webm 형식을 사용하도록 **적극** 권장한다.) EdX는 Vimeo와 같은 사이트에 게시하는 동영상을 지원하지 않는다.

.. _Create a Video Component:

********************************
동영상 구성요소 만들기
********************************

#. **신규 구성요소 추가** 아래에, **동영상** 을 클릭한다.

#. 새로운 동영상 구성요소가 보이면 **편집** 을 클릭한다. 동영상 편집기는 **기본** 탭이 열린다.

   .. image:: ../../../shared/building_and_running_chapters/Images/VideoComponentEditor.png
    :alt: Image of the video component editor
    :width: 500

   기본 값을 바꿀 있다.
   
3. **표시될 구성요소 이름** 입력칸에서, 학습자가 강좌 리본에 있는 학습활동 위에 마우스 포인트를 갖다댈 때 나타나는 텍스트를 입력한다. 이 텍스트는 동영상에 대한 상단 제목으로 나타난다.

#. **동영상 URL 기본값** 입력칸에서 동영상 URL을 입력한다. 예를 들어 URL은 다음과 같을 것이다.

   ::
   
      http://youtu.be/OEoXaMPEzfM
      http://www.youtube.com/watch?v=OEoXaMPEzfM
      https://s3.amazonaws.com/edx-course-videos/edx-edx101/EDXSPCPJSP13-G030300.mp4
      https://s3.amazonaws.com/edx-videos/edx101/video4.webm	

.. note:: 모든 학습자가 동영상에 접근하도록 하기 위해서 .mp4 및 .webm 동영상을 모두 제공할 것을 권장한다. 이렇게 하려면 동영상의 추가 버전을 인터넷에 올리고, 기본 동영상 URL 아래에 추가 동영상의 URL을 더할 수 있다. **이러한 URL은 YouTube URL이 될 수 없다.** 다른 버전에 대한 URL을 추가 하려면 **다른 버전 URL 추가하기** 를 클릭한다. 학습자의 컴퓨터와 호환되는 첫 번째로 나열된 동영상이 재생될 것이다.

5. **기본 자막** 의 옵션을 선택한다. 

   * 예를 들어 기존의 강좌에 있는 동영상을 이용하는 경우와 같이 EdX에 이미 동영상에 대한 자막이 있는 경우 Studio는 자동으로 동영상을 찾아서 자막을 연결한다.
     
     자막을 수정할 경우 **편집을 위해 자막 다운로드** 를 클릭한다. 변경 내용을 확인하고 **신규 자막 업로드하기** 를 클릭하여 새 파일을 업로드 수 있다.

   * EdX에는 동영상에 대한 자막이 없지만 YouTube는 자막이 있는 경우, Studio는 자동으로 YouTube 자막을 찾아서 가져올 것인지 묻는다. YouTube 자막을 사용하려면 **YouTube 자막 가져오기** 를 클릭한다. (YouTube 자막을 수정하려는 경우 YouTube 자막을 스튜디오로 가져온 다음 **편집을 위해 자막 다운로드** 를 클릭한다. 변경 후 **신규 자막 업로드하기** 를 클릭하여 새로운 파일을 업로드 할 수 있다.) 

   * EdX와 YouTube 모두 동영상 자막을 가지고 있지만 edX의 자막이 최신 버전이 아니라면, edX에 있는 자막을 YouTube 자막과 교체할 것인지를 묻는 메시지를 보게된다. YouTube 자막을 사용하려면 **예, edX 자막을 YouTube 자막으로 교체하세요** 를 클릭한다.

   * EdX와 YouTube 모두 동영상에 대한 자막이 없고, 운영팀에서 올리는 자막이 .srt 파일일 경우, 컴퓨터에서 자막 파일을 업로드 하려면 **신규 자막 업로드하기** 를 클릭한다. 

     .. note:: 

        * 운영팀에서 올리는 자막이 .sjson 형식을 사용하려고 하는 경우, 이 설정을 이용하지 않는다. 자세한 내용은 :ref:`Steps for sjson files` 을 참조한다.
        * PDF 등과 같은 형식으로 자막을 제공하려는 경우, 자막을 업로드하기 위해 이 설정을 이용하지 않도록 한다. 자세한 내용은 :ref:`Additional Transcripts` 를 참조 한다.

6. 동영상에 대한 다양한 옵션을 설정하려면 **고급** 을 클릭한다. 각 옵션의 설명은 :ref:`Video Advanced Options` 를 참조한다.

#. **저장** 을 클릭한다.
  
.. _Video Advanced Options:

==================
고급 옵션
==================

동영상 구성요소에서 **고급** 탭에 다음 옵션이 나타난다.

.. _Video Advanced Options:

==================
Advanced Options
==================

The following options appear on the **Advanced** tab in the video component.

.. list-table::
    :widths: 30 70

    * - **구성요소 표시 이름**
      - 학습자가 보게 될 이름이다. 이것은 **기본** 탭에 있는 
        **표시 이름** 입력 필드와 동일하다.
    * - **기본 자막**
      -  **기본** 탭의 **기본 자막** 입력 필드에 사용되는 자막 파일의 이름이다. 
         이 입력 필드는 자동으로 채워진다. 이 설정을 변경할 필요가 없다.
         
    * - **자막 다운로드 허용**
      - 학습자가 정기 자막을 다운로드 하도록 허용하는지 지정한다.
        이 값을 True로 설정하면 자막 파일을 다운로드 하는 링크가 
        동영상 아래에 나타난다.

        기본적으로 스튜디오는 .srt 자막을 업로드하면 .txt 자막을 만든다.
        **자막 다운로드 허용** 을 **True** 로 설정하면 
        학습자는 .srt 또는.txt 버전의 자막을 다운로드 할 수 있다. 
        .pdf 등 다른 형식으로 자막 다운로드를 제공하려는 경우 
        **강좌 자료 업로드하기** 입력 필드를 사용 하여 스튜디오에 
        파일을 업로드 한다.

    * - **다운로드 할 수 있는 자막 URL**
      - **파일 및 업로드** 페이지 또는 인터넷에 게시된 자막 파일의 
        비.srt 버전에 대한 URL이다. 학습자는 동영상 아래 비.srt 
        자막을 다운로드 하는 링크를 보게 된다.

        이 입력 필드에 자막을 추가하면 추가한 자막만이 다운로드 가능하다. 
        .Srt 및.txt 자막은 이용할  수 없게 된다. .Srt 이외의 형태로 다운로드
        가능한 자막을 제공하려는 경우에, **강좌 자료 업로드하기** 입력 필드를 
        사용하여 학습자를 위한 자료를 업로드 할 것을 권장한다. 
        자세한 내용은 :ref:`Additional Transcripts` 를 참조하도록 한다.
         

    * - **동영상 ID**
      - 동영상 파일을 프로세스 및 호스트 하기 위해 EdX와 함께 작업하는 강좌 운영팀에 
        의해서만 사용되는 선택적인 입력 필드이다.
    * - **자막 보여주기**
      - 기본적으로 자막을 동영상과 함께 재생할 것인지 여부를 지정한다
    * - **자막 언어**
      - 모든 추가 언어에 대한 자막 파일이다. 더 자세한 
        내용은 :ref:`Transcripts in Additional Languages` 를 참조 하도록 한다.
    * - **강좌 자료 업로드하기**
      - 동영상이 동반하는 강좌 자료를 업로드 할 수 있다. 강좌 자료는 
        어떤 형식도 될 수 있다. 학습자는 동영상 아래 **강좌 자료 다운로드하기**를
        클릭하여 강좌 자료를 다운로드 할 수 있다.
    * - **동영상 다운로드 허용**
      - 학습자가 EdX 동영상 플레이어를 사용할 수 없거나, YouTube에 접근할 수 없는 경우 
        다른 형식으로 동영상 버전을 다운로드할 수 있는지 여부를 지정한다. 
        이 값을 **True** 로 설정하면 **Video File URLs** 입력 필드에
        최소 한 개 이상의 비-YouTube URL을 추가 해야 한다.
    * - **동영상 파일 URLs**
      - 비-YouTube 버전으로 게시된 동영에 대한 URL 또는 URLs 이다. 모든 URL은 
        .mpeg,.webm,.mp4, 또는.ogg 형식으로 끝나야 하고 YouTube URL이 될 수 없다. 
        각 학습자는 학습자의 컴퓨터와 호환되는 첫 번째 나열된 동영상을 볼 수 있을 
        것이다. 학습자가 이러한 동영상을 다운로드 할 수 있도록, 
        **동영상 다운로드 허용**를 **True** 로 설정해야 한다.
        


.. _Video TOC:

***************************
동영상 목차
***************************

K-MOOC 담당자는 동영상의 다른 부분을 클릭할 수 있는 링크를 포함하는.srt 자막 파일을 추가함으로써 동영상에 대한 목차를 추가할 수 있다. 학습자가 동영상을 볼 때, 동영상에 대한 주요 자막과 목차 사이를 전환하기 위해 동영상 플레이어의 하단에 있는 **CC** 버튼을 클릭 할 수 있다.

목차를 추가하려면 K-MOOC 담당자는 .srt 자막 파일을 만들기 위해 제 3 자 서비스 업체와 함께 작업한다. 그런 다음, K-MOOC 담당자는 .srt 파일을 동영상과 연관시키기 위해 동영상 구성 요소에 있는 **자막 언어** 설정을 사용한다.

.. image:: ../../../shared/building_and_running_chapters/Images/VideoTOC.png
   :alt: Image of a video with a transcript that has links to different parts
    of the video
   :width: 500

#. 목차로써 기능할 .srt 자막 파일을 구한 후, 동영상에 대한 동영상 구성 요소를 연다.

#. **고급** 탭에서 **자막 언어** 아래로 스크롤 한 다음, **추가하기** 를 클릭한다. 

#. 나타나는 드롭-다운 목록에서, **목차** 를 선택한다. **업로드하기** 버튼이 나타난다.

#. **업로드하기** 를 클릭하고, 자막에 대한 .srt 파일로 이동한 다음 **열기** 를 클릭한다.

#. **자막 업로드하기** 대화 상자에서, **업로드하기** 를 클릭한다.

.. _Additional Transcripts:

**********************
추가 자막
**********************

기본적으로.srt 파일을 업로드하는 경우 .txt 파일이 만들어지고, 학습자는 K-MOOC 담당자가 **자막 허용** 을 **True**로 설정한 경우 .srt 또는.txt 자막을 모두 다운로드 할 수 있다. **자막 다운로드** 버튼이 동영상 아래쪽에 나타나고, 학습자는 버튼 위로 마우스를 가져가면 .srt 및.txt 옵션을 보게 된다.

.. image:: ../../../shared/building_and_running_chapters/Images/Video_DownTrans_srt-txt.png
   :width: 500
   :alt: Video status bar showing srt and txt transcript download options

.Srt 및.txt  자막과 함께 .pdf 같은 형태로도 다운로드 가능한 자막을 제공하려는 경우에 **강좌 자료 업로드하기** 입력 필드를 사용할 것을 권장한다. 이 작업을 수행 하는 경우 **강좌 자료 다운로드하기** 버튼은 **자막 다운로드하기** 버튼의 오른쪽에 나타나고 학습자는 .srt,.txt, 또는 강좌자료 버전의 자막을 다운로드 할 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/Video_DownTrans_srt-handout.png
   :width: 500
   :alt: Video status bar showing srt, txt, and handout transcript download
    options

**강좌 자료 업로드하기** 입력 필드를 사용하여 다운로드 가능한 자막을 추가 하려면,

#. pdf 또는 다른 형식으로 된 자막을 만들거나 구한다.
#. 동영상 구성 요소에서 **고급** 탭을 클릭
#. **강좌 자료 업로드하기** 를 찾아서 **업로드하기** 를 클릭한다.
#. **파일 업로드하기** 대화 상자에서, **파일 선택하기**를 클릭한다.
#. 대화 상자에서, 컴퓨터에 파일을 선택하고, **열기** 를 클릭한다.
#. **파일 업로드하기** 대화 상자에서, **업로드하기** 를 클릭한다.

스튜디오가 **강좌 자료 업로드하기** 기능을 추가하기 전에, 일부 강좌는 **파일 및 업로드** 페이지 또는 인터넷에서 자막 파일을 게시하였고 그런 다음 동영상 구성 요소에서 해당 파일들의 링크를 추가하였다. **Edx는 더 이상 이 방법을 권장하지 않는다.** 이 방법을 사용할 경우 **자막 다운로드하기** 버튼이 표시 되지만 오직 K-MOOC 담당자가 추가한 자막만 다운로드 할 수 있다. .Srt 및.txt 자막은 이용할 수 없게 된다.

.. image:: ../../../shared/building_and_running_chapters/Images/Video_DownTrans_other.png
   :width: 500
   :alt: Video status bar showing Download Transcript button without srt and
    txt options

이 방법을 사용 하려는 경우, 자막을 온라인에 게시하고 난 다음 **Downloadable Transcript URL** 입력 필드에서 자막에 대한 URL을 추가 할 수 있다. 그러나, 학습자는 .srt 또는.txt 자막을 다운로드 할 수 없다는 것을 염두에 두어야 한다.

.. _Transcripts in Additional Languages:

====================================
추가 언어 자막
====================================

 K-MOOC 담당자는 다른 언어로 동영상에 대한 자막을 제공할 수 있다. 이렇게 하려면, K-MOOC 담당자는 각 언어에 대한 .srt 자막 파일을 얻기 위해 제 3 자 서비스 업제와 작업해야 하고, 그런 다음에 스튜디오에서 .srt 파일을 동영상과 연결할 수 있다.

#. 추가 언어에 대한.srt 파일을 구한 후 동영상에 대한 동영상 구성 요소를 연다.

#. **고급** 탭에서 **자막 언어** 아래로 스크롤 한 다음 **추가하기** 를 클릭한다.

#. **고급** 탭에서 **자막 언어** 아래로 스크롤 한 다음 **추가하기** 를 클릭한다.

   **업로드하기** 버튼이 언어 아래쪽에 나타난다.

#. **업로드하기** 를 클릭하고, 원하는 언어에 대한 .srt파일을 찾은 다음 **열기** 를 클릭한다. 

#. **자막 업로드하기** 대화 상자에서 **업로드하기** 를 클릭한다.

#. 모든 추가 언어에 대해 2-5 단계를 반복한다. 

.. 참고:: 모든 자막 파일 이름이 각 동영상 및 언어에 대해 고유한지를 확인하도록 한다. 하나 이상의 동영상 구성 요소에서 동일한 자막 이름을 사용하는 경우, 동일한 자막이 각 동영상에 대해 재생된다. 이 문제를 방지하려면, K-MOOC 담당자는 동영상의 파일 이름 및 자막 언어에 따라 외국어 자막 파일을 이름 지을 수 있다.

 예를 들어, video1.mp4 및 video2.mp4 라는 두 개의 동영상을 가지고 있는 경우, 각 동영상은 러시아 자막 및 스페인어 자막을 가진다. K-MOOC 담당자는 첫 번째 동영상에 대해 video1_RU.srt 및 video1_ES.srt라고 이름을 짓고, 두 번째 동영상에 대해서는 video2_RU.srt 및 video2_ES.srt라고 자막의 이름을 지을 수 있다.

학습자가 동영상을 볼 때, 그들은 언어를 선택 하기 위해 동영상 플레이어의 하단에 있는 **CC** 버튼을 클릭 할 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/Video_LanguageTranscripts_LMS.png
   :alt: Video playing with language options visible

.. _Steps for sjson files:

**********************
sjson파일을 위한 단계
**********************

K-MOOC 담당자의 강좌가 .sjson 파일을 사용하는 경우, **파일 업로드** 페이지에서 동영상에 대한.sjson 파일을 업로드하고, 동영상 구성 요소에서.sjson 파일의 이름을 지정하도록 한다.

.. 참고:: 과거에.sjson 파일을 사용한 오래된 강좌는 .sjson 파일을 사용해야 한다. 모든 새로운 강좌도 .srt 파일을 사용해야 한다.

#. 3Play 같은 미디어 회사에서.sjson 파일을 가져온다.
#. 다음 형식을 사용하여.sjson 파일의 이름을 변경한다.
   
   ``subs_{video filename}.srt.sjson``
   
   예를 들어 동영상의 이름이 **Lecture1a** 인 경우, .sjson 파일의 이름은 **subs_Lecture1a.srt.sjson** 가 되어야 한다.
   
#. **파일 업로드** 페이지에서 동영상에 대한.sjson 파일을 업로드 한다.
#. 새로운 동영상 구성 요소를 만든다.
#. **기본** 탭에서 학습자가 **구성 요소 표시 이름** 입력 필드에서 보기 원하는 이름을 입력한다.
#. **동영상 URL** 입력 필드에서, 동영상의 URL을 입력한다. 예를 들어, URL은 다음 중 하나를 닮을 수 있다.

   ::
   
      http://youtu.be/OEoXaMPEzfM
      http://www.youtube.com/watch?v=OEoXaMPEzfM
      https://s3.amazonaws.com/edx-course-videos/edx-edx101/EDXSPCPJSP13-G030300.mp4

#. **고급** 탭을 클릭한다.
#. **기본 정기 자막** 입력 필드에서, 동영상의 파일 이름을 입력한다. subs_ 또는 .sjson를 포함하지 않도록 한다. 예를 들어, 2 단계에서 K-MOOC 담당자는 **Lecture1a** 만 입력한다.
#. 원하는 다른 옵션을 설정한다.
#. **Save** 를 클릭한다.

.. _Creating Videos: https://courses.edx.org/courses/edX/edX101/2014/courseware/c2a1714627a945afaceabdfb651088cf/9dd6e5fdf64b49a89feac208ab544760/

.. _edX101 Overview of Creating an edX Course: https://www.edx.org/node/5496#.VH8p51fF_FA
