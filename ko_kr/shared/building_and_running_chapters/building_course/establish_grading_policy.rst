.. _Establish a Grading Policy:

##############################
성적 규정 설정하기
##############################

*******************
개관
*******************

성적 규정을 설정하는 것은 여러 단계를 거친다. 

#. :ref:`Set the Grade Range`
#. :ref:`Set the Grace Period`
#. :ref:`Configure the Assignment Types`
#. :ref:`Graded Subsections`
#. :ref:`The Student View of Grades`

.. 중요:: 강좌를 시작한 후, 강좌 채점 규정, 성적 반영 소주제, 또는 성적 반영 구성요소에 대한 변경은 강좌에서 학습자의 학습 경험과 성적 분석에 영향을 미친다.

.. _Set the Grade Range:

*******************
성적 범위 설정하기
*******************

강좌의 성적 범위를 설정해야 한다. 예를 들어, 가 될 수 있고, 또는 A 부터 F까지 등급을 가질 수 있다.

성적 범위를 설정하려면 **설정** 메뉴에서 **과제 평가**를 선택한다.

페이지 상단의 바를 마우스로 움직이면 성적 범위를 조정할 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/grade_range.png
  :alt: Image of the Grade Range control

위의 예제는 컷오프 50점으로 통과/과락 범위를 보여준다. 50점이 기본값이며, 성적바를 마우스로 움직이면 성적 범위를 조정할 수 있다.

다음 설정을 변경하기 위해 점수 범위 제어를 이용할 수 있다.

* 범위에서 등급을 추가하기 위해 **+** 아이콘을 클릭한다.

  새로운 등급이 기존 등급 사이의 범위에 추가된다. 예를 들어 기본 설정에서 등급을 추가 하는 경우, 점수 범위는 **F** (0 ~ 50), **B** (50 75 ~), 그리고  **A** (75 ~ 100)로 변경된다.

  .. image:: ../../../shared/building_and_running_chapters/Images/grade_range_b.png
    :alt: Image of an altered Grade Range control

* 점수 범위를 변경 하려면 점수 경계선 위로 커서를 이동 후 클릭하고 왼쪽이나 오른쪽으로 움직인다.
선이 원하는 곳에 있을 때 마우스 단추를 놓는다.

* 등급명을 변경하려면, 변경하고 싶은 현재 등급명을 두 번 클릭하고, 새 이름을 입력한다. 예를 들어, 원래 등급명이  "통과"인 경우, "통과"를 두 번 클릭한 다음, "Excellent (우수)"를 입력 할 수 있다. 

**F** 또는 **과락** 은 변경할 수 없다.



* 등급을 삭제하려면 점수 위에 있도록 커서를 이동한다. **remove** 링크가 점수 위에 나타난다. 링크를 클릭한다. F 또는 A는 제거할 수 없다.
  
범위를 변경한 후 페이지 하단에 있는 **변경 사항 저장** 을 클릭해야 한다..

.. _Grade Ranges and Certificates:

==============================
성적 범위와 수료증
==============================

강좌 수료증을 발급할 경우, 학습자가 F나 Fail이상의 성적을 받아야 수료증을 취득할 수 있다. 이는 얼마나 많은 등급이 성적 범위에 추가되는지에 상관없이 적용된다.

.. _Set the Grace Period:

*************************
추가 제출 기간 설정하기
*************************
    
과제 제출 날짜를 연장하는 추가 제출 기간을 설정할 수 있다. 

.. 참고:: 추가 제출 기간은 모든 강좌에 적용된다. 개별 과제에 대해서는 추가 제출 기간을 설정할 수 없다.
  
성적 규정 영역에서, **추가 제출 기간** 입력란에 값을 입력한다. 시간:분 형식으로 값을 입력한다.

.. _Configure the Assignment Types:

******************************
과제 유형 설정하기
******************************

과제의 유형을 설정해야 하고, 각 과제 형식에 대해 학습자의 전체 성적에서의 비중(weight)을 결정해야 한다.

예를 들어, 다음의 과제 유형들을 가질 수 있다.

* 점수의 50%에 해당하는 10가지 과제 할당.
* 점수의 20%에 해당하는 중간 평가
* 점수의 30%에 해당하는 기말 평가

기본적으로, 개설하는 신규 강좌는 4개의 과제 유형을 가진다: 

* 과제
* 실험
* 중간 평가
* 기말 평가

이러한 과제 유형을 이용, 수정 또는 삭제할 수 있고, 새로운 과제 유형을 만들 수 있다. 

새로운 과제 유형을 만들려면 성적 페이지의 하단에서 **과제 추가히기** 를 클릭한 다음, 아래에 설명된 입력 필드를 설정한다.

==========================
과제 유형 입력 필드
==========================
각 과제 유형에 대해 다음의 입력 필드를 설정한다.
    
* **과제명:** 
  
  중간평가, 기말평가 등 과제명을 입력한다. 이 이름은 학습자에게 표시된다.
 
  .. 참고:: 한 과제 유형에 속하는 모든 하위 과제는 그 유형의 비중으로 동일하게 계산된다. 즉, 10개의   문제를 포함하는 과제든, 20개의 문제를 포함하는 과제든, 동일한 비율로 성적에 반영된다.
  
* **성적 기록부 표시용 약자** 
  
  이것은 학습자의 **진도** 탭과 **성적 기록부** 에 사용될 것으로, 공간의 문제상 과제명의 약자가 필요하다. 예를 들어 중간 평가의 경우, ‘중간’으로 입력하면 된다.   

* **점수 가중치** 
  
  해당 유형에 속하는 전체 과제가 합쳐져서 과목 전체 성적에, 점수 가중치에 맞춰 반영된다.
  
  모든 과제 유형의 비중을 합치면 100이 되어야 한다.
  
  .. 참고:: 이 입력 필드에 백분율 기호 (%)를 포함하지 않는다.
  
* **합계**
  
  강좌 전체 과제 유형의 개수이다.
  
* **낙제 횟수**
  
  채점자가 낙제시킬 과제 유형의 수이다. 채점자는 최저 득점 과제를 먼저 낙제시킬 것이다

.. _Graded Subsections:

**********************************************
성적 반영 소주제 지정하기
**********************************************

소주제에 문제를 추가하고 과제 유형을 지정한다. 

채점될 문제를 포함하는 각 소주제는 한 가지 유형의 과제만을 포함할 수 있다.

.. 참고:: 
소주제 수준에서만 과제 유형 및 마감 날짜를 설정할 수 있다. 전체 주제 또는 소주제 내 개별 학습활동에 대한 과제 유형 또는 마감 날짜를 설정할 수는 없다. 또한, 한 과제유형에 대해선 오직 하나의 소주제만 지정할 수 있다. 
  
:ref:`Developing Course Subsections` 에 에 소주제 설정하기에 대한 일반적인 안내가 있다.
:ref:`Set the Assignment Type and Due Date for a Subsection` 에 채점되는 과제로서 소주제를 지정하는 것에 관한 안내가 있다.

채점된 소주제 내에서, 해당 소주제에 대해 지정된 유형의 문제를 만든다. 같은 소주제에서 다른 과제 유형의 문제와 혼합할 수 없다.

예를 들어 특정 주제에 대한 과제와 실험을 만들려는 경우, 두 개의 소주제를 만들도록 한다. 하나의 소주제는 과제 유형으로, 다른 하나의 소주제는 실험 과제 유형으로 설정한다. 두 소주제는 실제 숙제 또는 실험 문제뿐 아니라 다른 콘텐츠를 포함할 수 있다.

.. 참고:: 
 You can create problems in Studio without specifying that the subsection is an
 assignment type. However, such problems do not count toward a student's grade.

See :ref:`Working with Problem Components` for instructions on creating
problems.

.. _The Student View of Grades:

**************************
The Student View of Grades
**************************

After a grading policy is in place, students can view both their problem scores
and the percent completed and current grade in the **Progress** tab for the
course.
  
  .. image:: ../../../shared/building_and_running_chapters/Images/Progress_tab.png
    :alt: Image of the student Progress tab

Each item in the X axis of the chart is for a graded subsection. Graded
problems in units are not broken out in the chart; the score from each problem
in the subsection is added to that vertical bar.

Graded subsections are grouped in the chart by assignment type rather than
listed in chronological order. For example, all homework exercises are grouped
together, followed by labs, then exams.

.. note:: The **x** for an assignment in the Progress tab indicates that the 
 grade for that assignment is currently dropped. You configure how many
 assignments are dropped when you :ref:`Configure the Assignment Types`.
