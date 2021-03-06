.. _Word Cloud:

##################
Word Cloud 도구
##################


Word Cloud (워드 클라우드) 도구에서 학습자는 질문지 또는 프롬프트에 대한 응답으로 어떤 필드에 단어를 입력한다. 학습자 모두가 입력한 단어들은 형형색색의 그래픽으로 즉시 나타나며 입력 빈도가 가장 큰 응답이 가장 크게 표시된다. 응답하는 학습자가 많아질수록 그래픽도 커진다. 학습자는 동료들이 응답하는 방식을 확인하며 자신의 생각을 동료 집단에 제공할 수도 있다.

다음의 워드 클라우드는 HarvardX 강좌의 질문지에 대한 학습자 응답을 바탕으로 생성한 것이다.

.. image:: ../../../shared/building_and_running_chapters/Images/WordCloudExample.png
  :alt: Image of a word cloud problem

****************************
워드 클라우드 도구 만들기
****************************

워드 클라우드 도구를 만들려면,

#. 워드 클라우드(Word Cloud) 고급 구성요소를 추가한다.

    #. **설정** 메뉴에서 **고급 설정** 을 클릭한다.

    #. **고급 모듈 목록** 규정 키 필드에서 대괄호 사이에 커서를 놓는다.
       
    #. 다음 값을 입력한다. 따옴표도 함께 입력해야 한다.

       ``"word_cloud"``

    4. 페이지 하단에서 **변경사항 저장** 을 클릭한다.

       페이지가 자동으로 새로고침되며, 변경이 저장됐다는 안내 메시지가 페이지 상단에 표시된다.
       

    5. 이 특수 문제를 추가하고자 하는 학습활동으로 복귀한다. 가능한 구성요소 목록에 고급 구성요소가 포함됐다.
       
#. 문제를 만들고자 하는 학습 활동에서 **신규 구성요소 추가** 하단의 **고급** 을 클릭한다.
  
#. **문제** 유형 목록에서 **Word Cloud** 를 클릭한다.
#. 구성요소가 나타나면 **편집** 을 클릭한다.
#. 구성요소 편집기에서 여러분이 원하는 설정을 지정한다. **표시명** 을 제외한 모든 항목의 초기값을 그대로 
   유지할 수도 있다.

   -  **메뉴명** : 강좌 리본 및 문제 상단 제목으로 표시되는 명칭
      
   -  **입력** : 학습자가 단어, 구 또는 문장을 입력하는 텍스트 박스의 갯수
      
   -  **최대 단어 수** : 해당 워드 클라우드가 표시하는 단어의 최대 갯수. 
      학습자가 300개의 단어를 중복 없이 입력하고 
      최대 단어수가 250인 경우 가장 빈번하게 입력된 단어 250개만 워드 클라우드에 나타난다.
      
   -  **퍼센트 보이기** : 학습자들이 주어진 한 단어를 입력한 횟수. 입력한 모든 단어의 퍼센트는 해당 단어 부근에 표시된다.
      

#. **저장** 을 클릭한다.
