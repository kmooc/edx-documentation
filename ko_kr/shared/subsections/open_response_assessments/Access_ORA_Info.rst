.. _Accessing ORA Assignment Information:

##########################################
과제 접근 및 학습자 통계
##########################################

개방형 응답 평가 과제의 각 단계를 수행하는 학습자의 수 또는 각 학습자의 성과에 관한 정보에 접근할 수 있다. 강좌 내용에서 해당 과제를 열어 과제 하단까지 스크롤을 내린 후 검은색으로 된 **강좌 운영팀 정보** 배너를 클릭하면 된다.

.. image:: ../../../../shared/building_and_running_chapters/Images/PA_CourseStaffInfo_Collapsed.png
   :alt: The Course Staff Information banner at the bottom of the peer assessment

.. _PA View Metrics for Individual Steps:

************************************************
단계별 학습자 통계 보기
************************************************

다음 절차를 완료한 학습자 수 또는 현재 수행 중인 학습자 수를 확인할 수 있다.

* 응답 제출
* 상호 평가
* 응답 평가 또는 채점 결과 수령 대기
* 자기 평가
* 과제 전체

해당 정보에 접근하려면 강좌 내용에서 해당 과제를 열어 과제 하단까지 스크롤을 내린 후 **강좌 운영팀 정보** 를 클릭한다.

**강좌 운영팀 정보** 대화 상자가 열리면 해당 문제의 각 단계를 진행 중(완료 이전)인 학습자의 수를 확인할 수 있다.

.. image:: ../../../../shared/building_and_running_chapters/Images/PA_CourseStaffInfo_Expanded.png
   :alt: The Course Staff Information box expanded, showing problem status

.. _Access Information for a Specific Student:

***********************************************
개별 학습자 정보에 접근하기
***********************************************

동료 평가 과제 관련해, 개별 학습자가 수행한 다음 정보에 대해 접근할 수 있다.

* 해당 학습자의 응답 
* 개별 평가 항목 및 응답 전반에 관한 피드백을 포함, 다른 학습자가 해당 학습자의 응답을 대상으로 수행한 상호 평가
* 개별 평가 항목 및 응답 전반에 관한 피드백을 포함, 해당 학습자가 다른 학습자의 응답을 대상으로 수행한 상호 평가
* 해당 학습자의 자기 평가

다음 예를 보면 학습자의 응답을 확인할 수 있다. 이 학습자의 응답은 1개의 상호 평가를 받았으며, 해당 학습자도 다른 학습자의 응답에 대한 상호 평가를 완수했다. 또한 이 학습자가 자기 평가를 완료했다는 사실도 알 수 있다.

.. image:: ../../../../shared/building_and_running_chapters/Images/PA_SpecificStudent.png
   :width: 500
   :alt: Report showing information about a student's response

:ref:`Access Student Information` 에서 보다 많은 평가와 관련한 학습자의 응답 현황을 보여주는 예시를 확인할 수 있다.

개별 학습자에 관한 정보에 접근하려면 다음 두 단계를 거쳐야 한다.

#. 해당 학습자의 강좌별 익명 ID 찾기
#. 해당 학습자 정보에 접근하기

=====================================================
학습자 강좌별 익명 학습자 ID 찾기
=====================================================

어떤 학습자의 강좌별 익명 학습자 ID를 결정하기 위해서는 교수자 대시보드에서 점수 보고서( **<course name>_grade_report_<datetime>.csv** ) 및 강좌별 익명 학습자 ID 목록( **<course name>-anon-ids.csv** ) 등, 두 개의 .csv 스프레드시트를 획득해야 한다.

#. 학습 관리 시스템에서 **교수자** 탭을 클릭한다.
#. 교수자 대시보드에서 **데이터** 를 클릭한다.
#. **데이터** 페이지에서 **익명 학습자 ID CSV** 받기를 클릭한다. **<course name>-anon-ids.csv** 라는 이름을 가진 파일이 자동으로 다운로드된다. 해당 파일을 클릭하여 스프레드시트를 연다.
#. **보고서** 섹션에서 **성적 보고서 생성** 을 클릭한다.

   시스템이 자동으로 성적 보고서를 생성해 보고서 작성이 완료되면, **다운로드 가능한 보고서** 아래의 목록에 점수 보고서 링크가 표시된다.

   .. note:: 대형 강좌의 경우 성적 보고서를 생성하는 데 시간이 다소 걸리기도 한다.

5. **다운로드 가능한 보고서** 목록에 점수 보고서 링크가 표시되면 해당 링크를 클릭하여 스프레드시트를 연다.

#. 두 스프레드시트가 모두 열리면 **<course name>_grade_report_<datetime>.csv** 스프레드시트를 검토한다. ID 또는 이메일 주소를 이용하여 원하는 학습자를 찾는다. ID 열(A열)에 있는 해당 학습자의 번호를 기록한다. 다음 예에서 이메일 주소가 ``amydorrit@example.com`` 인 학습자(ID ``lildorrit``) 번호는 ``18557``이다.

   .. image:: ../../../../shared/building_and_running_chapters/Images/PA_grade_report.png
      :width: 500
      :alt: Spreadsheet listing enrolled students and grades

7. **<course name>-anon-ids.csv** 스프레드시트로 가서 6단계에서 기록한 ID를 찾아 익명 학습자 ID열(C열)에 있는 해당 사용자의 값을 복사한다. **C열** 에 있는 값이 해당 강좌에 대한 해당 학습자의 익명화된 ID이다. 다음 예의 학습자  ``18557`` 의 익명화된 ID는 ``ofouw6265242gedud8w82g16qshsid87`` 이다.

   .. image:: ../../../../shared/building_and_running_chapters/Images/PA_anon_ids.png
      :width: 500
      :alt: Spreadsheet listing students' anonymous user IDs

   .. note:: B열에 있는 값을 복사하지 않도록 주의한다. 필요한 것은 **C열** 에 있는 **강좌별** 익명 학습자 ID이다.

.. _Access Student Information:

=======================================
해당 학습자 정보에 접근하기
=======================================

#. 학습 관리 시스템에서 확인하고자 하는 상호 평가 과제를 찾는다.
#. 문제 하단까지 화면을 스크롤한 후 검은색으로 된 **강좌 운영팀 정보** 배너를 클릭한다.
#. **학습자 정보 받기** 박스가 표시될 때까지 화면을 내린 후 해당 학습자의 강좌별 익명 ID를 박스에 복사해 넣고 **제출** 을 클릭한다.

**학습자 정보 받기** 박스 아래에 학습자 정보가 표시된다.

다음 예시에서 다음 정보가 표시된 것을 확인할 수 있다.

* 학습자 응답
* 해당 응답에 대한 상호 평가 2가지
* 해당 학습자가 완료한 상호 평가 2가지
* 해당 학습자의 자기 평가

이미지를 클릭하면 이미지가 브라우저 창 안에서 열린다. 이렇게 열린 이미지에서 아무 곳이나 클릭하면 보다 큰 화면으로 볼 수 있다.

.. image:: ../../../../shared/building_and_running_chapters/Images/PA_SpecificStudent_long.png
   :width: 250
   :alt: Report showing information about a student's response
