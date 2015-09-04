.. _External Grader:

###########################
외부 채점자
###########################


.. _External Grader Overview:

*******************
개관
*******************

외부 채점자는 문제에 대한 학습자의 응답을 받고, 그 응답을 처리하고, edX 플랫폼으로 피드백과 문제 점수를 반환하는 서비스이다. edX 플랫폼과는 별도로 외부 채점자를 만들고 배포할 수 있다. 

더 자세한 내용은 다음 주제를 참조하도록 한다.

* :ref:`External Grader Example`
* :ref:`External Graders and XQueue`
* :ref:`The XQueue Interface`
* :ref:`Building an External Grader`
* :ref:`Create a Code Response Problem`

.. _External Grader Example:

***************************
외부 채점자 예시
***************************

외부 채점자는 학습자가 복잡한 코드를 제출해야 하는 소프트웨어 프로그래밍 강좌에 특히 유용하다. 외부 채점자는 강좌 운영팀이 코드에 정의한 테스트를 실행할 수 있고, 결과를 학습자에게 반환할 수 있다. 

예를 들어, 학습자가 파이썬 코드를 제출해야 하는 문제를 정의하고, 외부 채점자가 제출을 확인하기 위해 실행할 수 있는 일련의 테스트를 만든다. 학습자가 문제에 대한 파이썬 코드를 입력하고 **확인** 을 클릭하면, 테스트를 위해 코드는 외부 채점자에 전송된다. 코드가 모든 테스트를 통과하는 경우, 외부 채점자는 점수 및 그 결과가 올바른지를 나타내는 문자열을 반환한다.

.. image:: ../../../shared/building_and_running_chapters/Images/external-grader-correct.png
 :alt: Image of a students view of a programming problem that uses an external grader, with a correct result 


외부 채점자는 학습자가 **전체 결과 보기** 를 클릭하여 볼 수 있도록 결과와 함께 문자열을 반환할 수 있다. 결과가 올바르지 않고 실패한 테스트에 대한 정보를 반환하려고 할 경우, 특히 유용할 수 있다. 예를 들어:

.. image:: ../../../shared/building_and_running_chapters/Images/external-grader-incorrect.png
 :alt: Image of a students view of a programming problem that uses an external grader, with a correct result 

.. _External Graders and XQueue:

**************************************
외부 채점자 및 XQueue
**************************************

edX 플랫폼은 XQueue를 통해 외부 채점자와 소통한다. XQueue는 외부 채점자에 대한 학습자의 입력을 제공한다; 그것은 외부 채점자로부터 결과를 받아 학습자에게 반환한다.  

학습자 제출은 XQueue에 수집되어 외부 채점자가 적극적으로 검색하거나 또는 성적을 위해 큐에서 다음 제출을 가져올 때까지 XQueue에 남아있게 된다. 

외부 채점자는 정기적인 간격으로 RESTful 인터페이스를 통해 XQueue에 대해 여론 조사(poll)한다. 외부 채점자가 제출한 것을 가져올 경우, 외부 채점자는 그 제출에 대한 테스트를 실행한 다음, RESTful 인터페이스를 통해 XQueue로 다시 응답을 보낸다. 그런 다음 XQueue는 edX 학습 관리 시스템(Learning Management System)으로 응답을 전달한다.

가져오기(Pull) 모드를 사용하는 외부 채점자의 코드에 대한 예는, `Stanford-Online repository xqueue_pull_ref <https://github.com/Stanford-Online/xqueue_pull_ref>`_ 를 참조하도록 한다.


============================
외부 채점자 작업 흐름
============================

다음 단계는 전체 과정을 보여준다:

#. 학습자는 코드를 입력하거나 아니면 문제에 대한 파일 첨부한 다음, 확인을 클릭한다. 
#. 외부 채점자는 XQueue에서 코드를 가져온다.
#. 외부 채점자 코드에서 만든 테스트를 실행한다.
#. 외부 채점자는 문자열로 된 결과뿐만 아니라 제출한 것에 대한 성적을 XQueue로 반환한다. 
#. XQueue는 edX 학습 관리 시스템으로 결과를 전달한다.
#. 학습자는 문제 결과 및 성적을 본다.


==================
XQueue 이름
==================

강좌는 특정 XQueue 이름을 사용한다. 이 이름은 edX 스튜디오에서 문제를 만들 때 사용된다. edX 프로그램 관리자로부터 이 이름을 얻을 수 있다. EdX가 다른 강좌에 대한 많은 XQueues를 호스트함으로, 문제에서 정확한 XQueue 이름을 사용하는 것은 :ref:`Create a Code Response Problem`  주제에서 설명된 바와 같이 매우 중요하다.


.. _The XQueue Interface:

**************************************
XQueue 인터페이스
**************************************

XQueue에서 채점자에게 보낸 학습자 제출 및 채점자로부터 XQueue로 보낸 응답은 아래에 설명 된 바와 같이 JSON 개체이다.

.. 참고:: XQueue는 외부 채점자에게 학습자 ID를 전송하지 않는다. 채점자는 학습자 ID에 접근할 수 없거나 또는 학습자 ID를 제출과 연관 지을 수 없다.

XQueue 인터페이스에 대한 코드에 대하여, `urls.py in the edX XQueue repository <https://github.com/edx/xqueue/blob/master/queue/urls.py>`_ 파일을 참조하도록 한다.

======================================================
외부 채점자에 대한 입력
======================================================

외부 채점자는 두 개의 열쇠를 가지는 JSON 개체로써 학습자 제출을 받는다.

* **student_response**: 학습자의 코드 제출을 포함하는 문자열. 이 문자열은 edX 학습 관리 시스템에서 학습자가 입력한 입력에서 유래하거나 또는 학습자가 첨부하는 파일로부터 유래한다.

* **grader_payload**: 문제를 만들 때 지정할 수 있는 선택적인 문자열. 더 자세한 내용은, :ref:`Create a Code Response Problem` 주제를 참조하도록 한다.

예를 들어

 {
   "xqueue_body":
   "{
     "student_response": "def double(x):\n return 2*x\n", 
     "grader_payload": "problem_2"
    }"
 }

======================================================
외부 채점자 답안
======================================================

제출한 것에 대한 결과를 기록하고 테스트를 실행 한 후, 외부 채점자는 JSON 응답을 게시하 여 정보를 반환해야 한다. JSON 문자열은 제출이 올바른지에 대한 표시, 점수, 및 테스트가 만드는 모든 메시지를 포함한다

다음 예제에서, 외부 채점자는 제출이 올바르다는 것을 나타내는 JSON 문자열과, 점수는 1이라는 것과, 하나의 메시지를 반환하고 있다.

 { 
  "correct": true, 
  "score": 1, 
  "msg": "<p>The code passed all tests.</p>" 
 }

.. _Building an External Grader:

****************************
외부 채점자 만들기 
****************************

edX가 아니라 강좌 운영팀이 외부 채점자에 대한 구축 및 배포에 대한 책임을 지게 된다. 

강좌에서 사용하는 문제에 관련된 테스트를 만들 뿐만 아니라, 외부 채점자를 구축할 때 계획해야 할4개의 영역이 있다: 

* :ref:`Scale`
* :ref:`Security`
* :ref:`Reliability and Recovery`
* :ref:`Testing`


.. _Scale:

==================
규모
==================

외부 채점자는 강좌에서 수많은 학습자를 지원하도록 확장할 수 있어야 한다. 

학습자 제출이 균등한 흐름이 아닌, 스파이크처럼 폭주하여 올 가능성이 있음을 명심해야 한다. 예를 들어, 시험 날짜 전의 시간에서 평균보다 훨씬 더 큰 부하를 기대해야 한다. 따라서, 외부 채점자가 짧은 기간 내에 대다수 학습자의 제출을 처리할 수 있음을 확인 해야 한다. 

.. _Security:

==================
보안
==================

학습자는 교수자 또는 강좌 운영팀이 담당하는 서버에서 직접 실행되는 코드를 제출한다. 학습자가 악성 코드를 제출할 가능성이 있다. 이것에 대항하여 시스템을 보호해야 하고, 외부 채점자가 강좌 문제와 관련된 코드만 실행하도록 해야 한다. 이러한 보호를 구현하는 방법은 사용 중인 프로그래밍 언어와 배포 아키텍처(deployment architecture)에 따라 달라진다. 악성 코드가 서버를 손상하지 않도록 확인해야 한다.

.. _Reliability and Recovery:

==============================
안정성 및 복구
==============================

일단 강좌를 시작하면, 많은 학습자는 가능한 시간에 언제든지 코드를 제출할 것이며, 신속하게 결과를 보기를 기대할 것이다. 외부 채점자가 오류를 내거나 또는 예기치 않게 지연할 경향이 있는 경우, 학습자의 경험은 질적으로 좋지 않을 것이다.

따라서, 외부 채점자가 이용 가용성이 높고 오류를 복구할 수 있는지 확인해야 한다. 강좌를 시작하기에 앞서, 채점자가 실패할 때, edX 운영팀 뿐만 아니라, 채점자의 운영에 책임이 있는 강좌 운영팀에게 즉시 알리기 위한 계획이 있어야 한다. EdX와 협력하여 채점자 또는 edX의 XQueue가 원인이 될 수 있는 실패의 원인을 신속하게 찾기 위한 절차를 개발해야 한다.

더 자세한 내용은 edX 프로그램 관리자에게 문의한다.

유지 관리를 위해 특정 시간에 채점자를 이용할 수 없는 경우, :ref:`Add a Course Update` (강좌 업데이트를 추가)해야 한다. 

.. _Testing:

==================
테스트
==================

강좌를 시작하기 전에 채점자를 철저하게 테스트 해야 한다. 채점자가 적절한 점수 및 메시지로 응답하는 것을 확인하기 위해 올바른 코드 뿐만 아니라 잘못된 코드도 테스트 해야 한다.

.. _Create a Code Response Problem:

********************************
코드 응답 문제 만들기
********************************

edX 스튜디오에서 일반적인 빈 문제를 추가하여 코드 응답 문제를 만든 다음, :ref:`Advanced Editor`  (고급 편집기)에서 XML 문제 정의를 편집한다.

더 자세한 내용은 :ref:`Working with Problem Components`  (문제 구성 요소로 작업하기)를 참조하도록 한다.

다음은 외부 채점자를 사용하는 문제의 XML 정의에 대한 기본 예제이다:

 <problem display_name="Problem 6">
    <text>
        <p>Write a program that prints "hello world".</p>
    </text>
    <coderesponse queuename="my_course_queue">
        <textbox rows="10" cols="80" mode="python" tabsize="4"/>
        <codeparam>
            <initial_display>
              # students please write your program here
              print ""
            </initial_display>
            <answer_display>
              print "hello world"
            </answer_display>
            <grader_payload>
            {"output": "hello world", "max_length": 2}
            </grader_payload>
        </codeparam>
    </coderesponse>
 </problem>

다음은 XML 정의에 관한 주석이다:

* **queuename**: <coderesponse> 요소의 queuename 값은 edX가 강좌를 위해 설정한 XQueue로 연결된다. edX 프로그램 관리자로부터 이 이름을 얻을 수 있다. 올바른 XQueue와 통신하기 위해 문제에 대한 순서대로 정확한 이름을  사용해야 한다. 

* **Input Type**: 이 예제에서, 입력 유형은 **<textbox>** 요소에 의해 지정된다. <textbox>를 사용하면, 학습자는 강좌 학습활동(course unit)을 볼 때 브라우저 필드에서 코드를 입력한다. 입력 유형을 지정하기 위해 사용할 수 있는 다른 요소는 학습자가 학습활동(unit)에서 코드 파일을 첨부하여 제출할 수 있도록 하는 <filesubmission>이다. 

* **<grader_payload>**: 외부 채점자에게 JSON 개체 형태로  정보를 보내기 위해 <grader_payload>요소를 사용할 수 있다. 예를 들어, 채점자에게 해당 문제에 대해 어느 테스트를  실행해야 하는지 이야기 하기 위해 <grader_payload>를 사용할 수 있다.  
