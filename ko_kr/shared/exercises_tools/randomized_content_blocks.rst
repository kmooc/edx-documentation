.. _Randomized Content Blocks:

#########################
무작위 콘텐츠 블록
#########################

:ref:`Content Libraries` 이 활성화되어 있고 사용하고자 하는 콘텐츠가 포함된 보관함에 접근할 수 있는 경우 해당 보관함을 통해 학습자를 위한 무작위 과제를 만들 수 있다.

무작위 과제를 만들려면, 강좌 학습활동 1개에 무작위 콘텐츠 블록을 1개 이상 추가해야 한다. 무작위 콘텐츠 블록 각각에 대해 해당 콘텐츠를 가져올 1개 이상의 보관함을 지정하고 그 갯수를 명시한다. 또한, 각 학습자에게 무작위로 배정할 **문제** 의 유형을 지정할 수 있는데 이는 선택사항이다. 무작위 과제를 위한 구성요소를 무작위로 가져올 보관함을 2개 이상 지정한 경우 모든 지정 보관함에서 가져온 콘텐츠는 무작위 선택에 앞서 조합한다.

강좌 운영팀이 만들고 접근하는 보관함의 목록은 Studio의 **콘텐츠 보관함** 탭에 있다. 
콘텐츠 보관함에 대한 더 자세한 안내는 :ref:`Content Libraries` 에 있다. 


강좌에서 콘텐츠 보관함 구성요소를 사용하는 자세한 방법에 관해서는 다음 주제를 참조한다.

* :ref:`Use Components from Libraries in a Course`
* :ref:`Add a Randomized Content Block to Your Course`
* :ref:`View the Matching Components in a Randomized Content Block`
* :ref:`Edit Components in Randomized Content Blocks`
* :ref:`Get the Latest Version of Library Content`


.. _Use Components from Libraries in a Course:

*****************************************
강좌 내 보관함에서 구성요소 사용하기
*****************************************

콘텐츠 보관함의 구성요소를 사용하는 무작위 과제를 생성하려면 사용하고자 하는 보관함에 대해, 최소한 사용자 수준의 접근 권한을 반드시 보유해야 한다. 보관함 접근 권한이 없는 경우 강좌 운영진 중 해당 보관함에 대한 **교수자** 접근 권한을 보유한 자가 여러분에게 접근 권한을 부여할 수 있다.

강좌 운영팀이 생성하거나 접근하는 보관함의 목록은 Studio Home의 **콘텐츠 보관함** 탭에 있다. 콘텐츠 보관함에 대한 더 자세한 안내는 :ref:`Content Libraries` 에 있다.

콘텐츠 보관함에서 구성요소를 사용하는 방법은 크게 아래 두 가지다.

#. :ref:`Enable Content Libraries`
#. :ref:`Add a Randomized Content Block to Your Course`
   
.. 참고:: 무작위 콘텐츠 블록을 강좌에 추가한 후, 1개 혹은 복수의 보관함 구성요소에 변경사항이 발생한 경우 
   해당 구성요소를 보관함 버전과 동기화한 상태를 유지하고자 한다면, 
   강좌 개요 내부 구성요소를 반드시 수동 업데이트 해야 한다는 점에 주의한다.
   

강좌에서 무작위 콘텐츠 블록을 취급하는 자세한 방법에 관해서는 다음 주제를 참조한다

* :ref:`View the Matching Components in a Randomized Content Block`
* :ref:`Edit Components in Randomized Content Blocks`
* :ref:`Get the Latest Version of Library Content`


.. _Enable Content Libraries:

========================
콘텐츠 보관함 활성화하기
========================

강좌 내 콘텐츠 보관함의 무작위 구성요소를 사용하기에 앞서 :ref:`Content Libraries` 을 반드시 활성화 해야 한다. 

#. Studio에서, 보관함 콘텐츠를 제공하고자 하는 강좌를 연다.

#. **설정** 을 선택한 후 **고급 설정** 을 선택한다.

#. **고급 모듈 목록(Advanced Module List)** 필드에서 한 쌍의 대괄호 사이에 커서를 놓는다.

#. ``"library_content"`` 를 입력한다.

#. **변경사항 저장** 을 클릭한다.
   
   Studio는 강좌 운영팀이 입력한 규정 키를 다시 포맷하여 해당 키의 위치를 새로운 행에서 들여쓰기 한다.

  .. image:: ../../../shared/building_and_running_chapters/Images/ContentLibraries_AdvancedSetting.png
     :alt: Advanced Module policy key "library_content"


.. _Add a Randomized Content Block to Your Course:

=============================================
강좌에 무작위 콘텐츠 블록 추가하기
=============================================

:ref:`Enable Content Libraries`  이후 무작위 콘텐츠 블록 고급 구성요소를 이용하여 보관함 콘텐츠를 강좌에 추가할 수 있다.

.. note:: 이 단계를 시작하기에 앞서 무작위 콘텐츠 블록에서 참조하고자 하는 보관함 각각의 
   보관함 ID를 획득한다. 보관함 ID는 각 보관함 페이지의 사이드바에 있다. 
   :ref:`Create a New Library` 에 더 자세한 안내가 있다. 

#. Studio에서, 1개 이상의 콘텐츠 보관함의 무작위 **문제** 를 추가하고자 하는 강좌를 연다.
   

#. **콘텐츠** 를 클릭한 후 **강좌 개요** 를 클릭한다.

#. 일련의 무작위 **문제** 를 추가하고자 하는 학습 활동에서 **신규 구성요소 추가** 를 클릭한다.
   
#. **고급** , **무작위 콘텐츠 블록** 을 차례로 클릭한다. 그러면 무작위 콘텐츠 블록이 학습 활동에 추가된다.
   
#. **편집** 아이콘을 클릭한다.
   
#. 무작위 콘텐츠 블록 설정에서 이 블록에 추가하고자 하는 콘텐츠의 세부 조건을 지정한다.
   
  - **문제 수** 에는 각 학습자에게 제시할 문제의 갯수를 입력한다.

  - **표시명** 에는 학습자가 보게 될 이 블록의 명칭을 입력한다.
    

  - **보관함** 에는 Studio 내 보관함 페이지의 사이드바에서 확인한 보관함 ID를 입력한다.
    2개 이상의 콘텐츠 보관함에서 문제를 선택하려면
    **추가** 를 클릭하여 각 추가 보관함 ID를 입력한다.

  - **문제 유형** 의 드롭다운 목록에서는 1개 또는 복수의 보관함에서 가져 올 문제의 특정 유형을 선택한다. 
    유형을 특정하고자 하지 않는 경우 어떠한 유형을 선택해도 무관하다.
    

    .. image:: ../../../shared/building_and_running_chapters/Images/ContentLibraries_SelectProblemType.png
     :alt: The Edit icon to the right of the Library Name    

  - **채점 여부** 의 드롭다운 메뉴에서는 **True** 혹은 **False** 를 선택하여 해당 과제의 채점 여부를 규정한다.
    

.. note:: 채점은 이 학습 활동의 소주제 또는 주제의 설정 항목이다. 소주제 또는 주제를 채점하지 않는 경우 
   이 학습 활동에서 **True** 를 선택하면 아무런 영향도 미치지 않는다. 
   **False** 를 선택하는 경우 소주제 또는 주제를 채점하는 경우라도 과제는 채점하지 않는다는 의미이다.
   
7. 무작위 콘텐츠 블록 관련 세부 조건 지정을 완료하면 저장을 클릭한다.


필터 설정과 일치하는 소스 보관함의 구성요소 목록에 대해 
:ref:`View the Matching Components in a Randomized Content Block` 에 안내되어 있다. 

Studio에서 보관함 콘텐츠 전체를 확인하려면, :ref:`View the Contents of a Library` 을 참조한다.
   

.. _View the Matching Components in a Randomized Content Block:

***********************************************************
무작위 콘텐츠 블록에서 일치하는 구성요소 보기
***********************************************************

무작위 콘텐츠 블록을 사용하는 학습 활동에서 해당 블록에 지정된 필터와 일치하는 모든 구성요소의 목록을 볼 수 있다.

이를 테면, 무작위 콘텐츠 블록을 지정하여 각 학습자에게 선다형 문제 3개를 제공하고자 하는 경우 이렇게 참조된 1개 혹은 복수의 보관함에 존재하는 모든 선다형 문제를 볼 수 있다. 다시 말해, 학습자에게 제공될 수 있는 보관함 내부의 모든 문제를 볼 수 있다.


#. Studio 에서, 보관함을 참조하는 무작위 콘텐츠 블록을 포함하는 학습 활동을 탐색한다.
#. 해당 무작위 콘텐츠 블록에서 **보기** 아이콘을 클릭한다.
   
   .. image:: ../../../shared/building_and_running_chapters/Images/ContentLibraries_ViewMatching.png
      :alt: The View button for a randomized content block

   무작위 콘텐츠 블록 내 규격과 일치하는 모든 구성요소를 볼 수 있다. 
   구성요소 목록 상단의 텍스트는 이들 구성요소 가운데 몇 가지를 선택하여 
   각 학습자에게 제공하는지를 나타낸다.


Studio에서 보관함의 콘텐츠를 보려면 
 :ref:`View the Contents of a Library` 를 참조한다.


.. _View the Randomized Content as a Student:

****************************************
학습자 방식으로 무작위 콘텐츠 보기
****************************************

무작위 콘텐츠 블록 내 구성요소의 갯수와 유형을 학습자가 보는 방식으로 보려면, :ref:`Preview a Unit` 를 참조한다.

보관함 내부의 일치하는 구성요소 목록을 보려면, :ref:`View the Matching Components in a Randomized Content Block` 을 참조한다. 

Studio에서 보관함의 콘텐츠 전체를 보려면, :ref:`View the Contents of a Library` 을 참조한다.


.. _Edit Components in Randomized Content Blocks:

******************************************************
무작위 콘텐츠 블록 내 구성요소 편집하기
******************************************************

무작위 콘텐츠 블록을 사용하는 강좌 학습 활동의 무작위 콘텐츠 블록 내 각 구성요소를, 강좌의 기타 어떠한 구성요소를 편집하는 방식과도 동일한 방식으로 Studio에서 편집할 수 있다.

.. note:: 어떤 구성요소의 **편집기** 탭을 변경한 경우, 해당 무작위 콘텐츠 블록을 
   보관함 구성요소의 최신 버전으로 업데이트한다면 이들 변경은 덮어쓰기 된다는 점에 주의한다. 
   무작위 콘텐츠 블록 내 보관함 콘텐츠의 최신 버전을 획득하는 구체적인 방법에 대해서는 
   :ref:`Get the Latest Version of Library Content` 을 참조한다.


무작위 콘텐츠 블록 내에 제공되는 구성요소의 설정은 해당 구성요소를 가져오는 콘텐츠 보관함의 구성요소의 설정에서 유래한 것이다. 무작위 콘텐츠 블록에서 구성요소 설정을 변경, 보관함 내 “소스” 구성요소와 다르게 할 수 있다.

어떤 구성요소의 설정값을 초기화할 수도 있다. 어떤 구성요소의 설정값이 보관함 내 초기 설정값에서 변경된 경우 해당 설정 필드 옆에 **지우기(Clear)** 아이콘이 표시된다.

 .. image:: ../../../shared/building_and_running_chapters/Images/ContentLibraries_ResetComponentField.png
    :alt: Clear button in the course component field reverts value to library value.

설정 필드에 대한 보관함 초기 설정을 복구하려면 **지우기** 아이콘을 클릭한다.



.. _Get the Latest Version of Library Content:

*********************************************
보관함 콘텐츠 최신 버전 획득하기
*********************************************

하나 또는 복수의 강좌에서 무작위 콘텐츠 블록이 참조하는 보관함의 콘텐츠를 변경하는 경우 이들 강좌가 업데이트된 콘텐츠를 자동으로 이용하지는 않다. 해당 무작위 콘텐츠 블록을 보관함 내 버전으로 업데이트한다.

.. 주의:: 이미 공개된 문제를 변경할 때 주의해야 한다. 게시된 문제에 변경을 가하는 경우 
   해당 강좌를 수강하는 학습자 경험과 강좌 자료 분석에 영향을 미칠 수 있다.
   

.. 참고:: 무작위 콘텐츠 블록 내 구성요소의 설정에 대한 변경사항을 유지할 수 있다. 
   그러나 해당 구성요소를 최신 보관함 버전으로 업데이트 하는 경우, 구성요소의 **편집기** 의 변경사항에 덮어씌워진다. 
   무작위 콘텐츠 블록 내 구성요소를 보관함 내 최신 버전으로
   업데이트하기를 원하지 않을 경우 아무런 조치도 취할 필요가 없다.
  
* 강좌 개요에서 무작위 콘텐츠 블록의 구성요소를 편집하지 않은 경우, 
  강좌 개요의 해당 무작위 콘텐츠 블록을 다음 번에 열 때 
  해당 구성요소가 보관함에 비해 최신판이 아니라는 메시지가 표시된다.
 

  .. image:: ../../../shared/building_and_running_chapters/Images/ContentLibraries_ComponentUpdateNow.png
     :alt: Error message shown when the source library has changed, with the
      Update Now link circled.

 무작위 콘텐츠 블록 구성요소를 콘텐츠 보관함 최신 버전으로 업데이트 하려면 **지금 업데이트** 를 클릭한다.

  그러면 무작위 콘텐츠 블록은 해당 무작위 콘텐츠 블록이 참조하는 1개 혹은 복수의 보관함의 
  최신 콘텐츠로 업데이트될 것이다.

* 강좌 내 무작위 콘텐츠 블록 구성요소의 설정만을 변경하여 
  이들 설정이 보관함의 최초 버전과 달라진 경우에도 
  **지금 업데이트** 를 클릭하면 변경은 사라지지 않는다. 
  이 경우, 강좌 개요 내 무작위 콘텐츠 블록에 발생한 변경사항이 저장된다. 
  단, 해당 구성요소의 변경된 필드 옆에 **지우기** 버튼이 사용가능한 상태로 된다. 
  그러나 최신 보관함 버전을 획득하기 위하여 **지금 업데이트** 를 클릭한 경우 
  어떠한 유형이든 무작위 콘텐츠 블록 내 구성요소의 편집기 탭의 변경사항은 손실될 것이다.
  
  .. image:: ../../../shared/building_and_running_chapters/Images/ContentLibraries_ResetComponentField.png
     :alt: Clear icon in the course component field reverts value to library value.

  
  강좌 개요에 취한 모든 종류의 편집을 지우고 편집된 구성요소를 보관함 버전으로 업데이트 하려면 **지우기** 를 클릭한다.
  
  해당 구성요소 필드의 값이 보관함의 현재 값으로 재설정될 것이다.


