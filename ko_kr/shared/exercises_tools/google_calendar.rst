.. _Google Calendar Tool:

#####################
구글 캘린더 도구 
#####################

이 장에서는 강좌에 구글 캘린더를 포함하는 방법을 설명한다. 더 자세한 내용은 다음 항목 중 하나를 참조하도록 한다.

* `개관`_

* `구글 캘린더 활용하기`_

  * `강좌에서 구글 캘린더 활용하기`_

    * `스튜디오에서 구글 캘린더 활용하기`_
    * `OLX 에서 구글 캘린더 활용하기`_

  * `구글 캘린더 공개하기 및 ID 얻기`_
  * `강좌 내용에 구글 캘린더 추가하기`_

    * `스튜디오에서 구글 캘린더 구성 요소 추가하기`_
    * `OLX에서 구글 캘린더 XBlock 추가하기`_

* `구글 캘린더 변경하기`_

또한 강좌에서 문서, 스프레드시트, 및 이미지 등과 같은 구글 드라이브 파일을 사용할 수 있다. 더 자세한 내용은 :ref:`Google Drive Files Tool`  를 참조하도록 한다.


*********
개관 
*********

학습자가 강좌내용에서 볼 수 있도록 강좌에 구글 캘린더를 포함시킬 수 있다. 퀴즈 날짜, 근무 시간, 또는 학습자에게 관심이 될만한 다른 일정들을 공유하기 위해 구글 캘린더를 사용할 수 있다. 예를 들면:

.. image:: ../../../shared/building_and_running_chapters/Images/google-calendar.png
  :alt: A Google calendar in courseware

*******************************************
구글 캘린더 활용하기 
*******************************************

강좌에 구글 캘린더를 포함하려면 세 단계가 있다.

#. :ref:`Enable Google Calendars in the Course` by using :ref:`Enable Google Calendars in edX Studio` or
   :ref:`OLX<Enable Google Calendars in OLX>` .

#. :ref:`Make the Google Calendar Public and Obtain Its ID` .

#. :ref:`Add a Google Calendar in the
   Courseware` by using :ref:`Add a Google Calendar Component in edX
   Studio` or :ref:`OLX<Add a Google Calendar XBlock in OLX>`.


.. _Enable Google Calendars in the Course:

======================================
강좌에서 구글 캘린더 활용하기
======================================

스튜디오 또는 OLX를 사용하여 강좌에서 구글 캘린더를 사용할 수 있다.

.. _Enable Google Calendars in edX Studio:

스튜디오에서 구글 캘린더 활용하기
**********************************************

강좌에서 구글 캘린더를 사용하려면:

#. **설정** 메뉴에서, **고급 설정** 을 선택한다.
#. **고급 모듈 목록** 입력 필드에서 중괄호 사이 커서를 놓은 다음  ``"google-calendar"`` 를 입력한다. 이 입력 필드에 다른 값을 보려면, 마지막 값에 대한 닫는 따옴표 후 쉼표를 추가하고 ``"google-calendar"`` 를 입력한다. 예를 들면:
   
   .. image:: ../../../shared/building_and_running_chapters/Images/google-advanced-setting.png
    :alt: Advanced modules setting for Google Calendars

#. 페이지의 하단에서 **변경사항 저장** 을 선택한다.

.. _Enable Google Calendars in OLX:

OLX에서 구글 캘린더 활용하기
**********************************************

강좌에서 구글 캘린더를 사용하려면, 강좌 구조를 정의 하는 XML 파일을 편집할 수 있다. 당신은 ``강좌`` 요소의 ``고급 모듈`` 속성을 찾아서, 그것에 문자열 ``google-calendar`` 를 추가한다. 

예를 들어, 다음 XML 코드는 강좌에서 구글 캘린더를 사용할 수 있게 만든다. 그것은 또한 구글 드라이브 파일을 활용할 수 있게 만든다.

.. code-block:: xml

  <course advanced_modules="[&quot;google-document&quot;, 
      &quot;google-calendar&quot;]" display_name="Sample Course" 
      start="2014-01-01T00:00:00Z">
      ...
  </course>

더 자세한 내용은 `The Courseware Structure`_ 를 참조하도록 한다.

.. _Make the Google Calendar Public and Obtain Its ID:

===================================================
구글 캘린더 공개하기 및 ID 얻기
===================================================

강좌에 구글 캘린더를 추가할 수 있기 전에, 먼저 구글 캘린더를 공개하고 ID를 얻어야 한다. 

.. important:: 
 이 주제에서 설명하는 작업은 제3 소프트웨어의 사용에 의존한다. 소프트웨어가 소유자에 의해 변경 될 수 있기 때문에 여기에 제공된 단계는 지침을 위한 것이지, 정확한 절차를 위한 것이 아니다.

구글 캘린더 공개하기
**********************************************


#. 구글 캘린더를 연다.
#. **설정** 메뉴에서 **설정** 을 선택한다.
#. **캘린더**  탭을 선택한다.
   
   **캘린더** 탭에 여러 개의 캘린더를 가질 수 있다. 강좌내용에서 공유하려는 캘린더를 찾는다.

#. **공유** 열에 있는, 캘린더를 공유하기 위한 열에서, **설정 편집하기** 을 선택한다.
#. **이 캘린더 공유하기** 탭을 클릭한 **이 캘린더 공개하기** 를 선택한다.
   
  .. image:: ../../../shared/building_and_running_chapters/Images/google-calendar-settings.png
   :alt: Google calendar settings

7. **저장** 을 선택한다. 
   
   **캘린더 설정** 페이지를 닫고, **캘린더** 탭으로 돌아간다. 다음에서 :ref:`obtaining the Google calendar's ID<Obtain the
   Google Calendar ID>` 에 대해 계속 알아보도록 한다.


.. _Obtain the Google Calendar ID:

구글 캘린더 ID 얻기
**********************************************

#. **캘린더** 탭에서 캘린더의 이름을 클릭한다.
#. **캘린더 세부 정보** 탭을 선택한다.
#. **캘린더 주소** 라벨 옆의 3 가지 색 **XML** , **ICAL** , **HTML** 버튼의 오른쪽을 본다. 괄호에서 캘린더 ID를 볼 수 있다.

   .. image:: ../../../shared/building_and_running_chapters/Images/google-calendar-address.png
     :width: 600
     :alt: Image of Calendar Address label with the calendar ID to the right

   캘린터 ID는 다음 텍스트와 유사하다.

   ``abcdefghijklmnop1234567890@group.calendar.google.com``

   캘린더 ID를 선택 및 복사한다. 강좌에서 구글 캘린더 구성 요소를 설정하기 위해 이 값을 사용한다.

.. _Add a Google Calendar in the Courseware:

========================================
강좌 내용에 구글 캘린더 추가하기
========================================

강좌내용에 구글 캘린더를 추가 하려면, 스튜디오에서 고급 구성 요소를 만들거나 또는 OLX에서 구글 캘린더 XBlock을 만든다.

.. _Add a Google Calendar Component in edX Studio:

스튜디오에서 구글 캘린더 구성 요소 추가하기
**********************************************

구글 캘린더 구성 요소를 추가하기 전에, 강좌에서 구글 캘린더를 활용할 수 있다 :ref:`enable Google Calendars in your course<Enable Google
Calendars in edX Studio>` 는 것을 확인한다.


구글 캘린더 구성 요소를 추가 하려면:

#. **강좌 개요** 페이지에서, 구글 캘린더 구성 요소를 추가하고 싶은 학습활동을 연다. 

#. **새 구성 요소 추가** 에서 **고급** 을 클릭한 후, **구글 캘린더** 를 선택한다.
   
    **새 구성 요소** 는 포함된 기본 구글 캘린더와 함께 학습활동에 추가된다.

   .. image:: ../../../shared/building_and_running_chapters/Images/google-calendar-studio.png
    :width: 600
    :alt: The Google calendar component in a unit page

#. **편집** 을 선택한다.
   
   .. image:: ../../../shared/building_and_running_chapters/Images/google-calendar-edit.png
    :width: 600
    :alt: The Google calendar editor

#. **표시 이름** 입력 필드에는 구성 요소에 대한 이름을 입력한다. 

#. **공개 캘린더 ID** 입력 필드에는  `Obtain the Google Calendar ID`_  (구글 캘린더 ID 얻기) 작업에서 복사한 캘린더 ID를 붙여 넣는다.

#. **기본 보기** 입력 필드에 대하여, **월** , **주** 또는 **안건** 을 선택한다. 이것은 학습자가 볼 캘린더에 대한 초기 보기이다. 각 학습자는 그 혹은 그녀의 보기를 변경할 수 있다.

#. **저장** 을 선택한다.

학습자에게 구글 캘린더를 포함한 학습활동이 어떻게 보이는지  :ref:`Preview Course Content`  (강좌 콘텐츠 미리보기) 할 수 있다.


.. _Add a Google Calendar XBlock in OLX:

OLX에서 구글 캘린더 XBlock 추가하기
**********************************************

OLX에 구글 캘린더 XBlock를 추가 하려면, ``google-calendar`` 요소를 만든다. ``vertical`` 요소에 이 요소를 포함시킬 수 있거나 또는 ``vertical`` 요소 내에서 참조되는 해당 파일에 이 요소를 포함시킬 수 있다. 더 자세한 내용은 `The Courseware Structure`_ (강좌내용 구조)를 참조하도록 한다. 

예를 들면:

.. code-block:: xml

  <google-calendar url_name="4115e717366045eaae7764b2e1f25e4c" 
    calendar_id="abcdefghijklmnop1234567890@group.calendar.google.com" 
    default_view="1" display_name="Class Schedule"/>

``calendar_id``  속성의 값은 `Obtain the Google Calendar ID`_ (구글 캘린더 ID 얻기) 작업에서 복사한 캘린더 ID이다.

.. note:: 
  K-MOOC 학습 관리 시스템은 구글 캘린더에 대한 height 및 width 값을 설정한다. 이러한 속성을 추가 하면, LMS는 변경 내용을 무시한다.

**************************
구글 캘린더 변경하기
**************************

강좌에 포함되어 있는 구글 캘린더를 변경할 때, 학습자는 즉시 업데이트를 보게 된다. 구글 사용자 인터페이스를 통해 캘린더를 변경한다. 구글 캘린더의 구성 요소는 변경할 필요가 없다.


.. _The Courseware Structure: http://edx.readthedocs.org/projects/edx-open-learning-xml/en/latest/organizing-course/course-xml-file.html
