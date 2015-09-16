.. _Overview of Content Experiments:

#################################
콘텐츠 실험 살펴보기
#################################

콘텐츠 실험은 학습자 집단별로 다른 강좌 내용을 제공하는데 이용된다. “A/B test”나 “split tests”로 알려진 것처럼, 콘텐츠 실험은 강좌 내용의 상대적인 효과를 고려하여 학습자 집단별 성취 결과를 조사 및 비교하는 것이 가능하다.

콘텐츠 실험에서 발생한 이벤트 분석 정보는 `연구자 가이드`_ 에 있다.

.. _연구자 가이드: http://edx.readthedocs.org/projects/devdata/en/latest/internal_data_formats/tracking_logs.html#a-b-testing-events

추가 정보는 다음과 같다:

* :ref:`Configure Your Course for Content Experiments`
* :ref:`Add Content Experiments to Your Course`
* :ref:`Test Content Experiments`

.. _Courses with Multiple Content Experiments:

******************************************
여러 콘텐츠 실험을 포함한 강좌
******************************************

강좌 내 여러 콘텐츠 실험을 운영할 수 있다. 동일한 학습자 집단에서 각 실험 참여하도록 설정하거나, 별개 집단을 만들어 독립적인 실험에 참여하도록 설정한다.


.. important::

  강좌에 여러개의 실험이 있을 때, 동일 집단의 학습자가 실험을 공유할지 혹은 특정 집단에 따라 각 실험을 하게 될 지 미리 결정해야 한다. 즉 두 실험을 동일 집단에서 공유한다면, 첫 번째 실험에서의 집단 A에 속한 학습자가 있고, 두 번째 실험에도 집단 A의 학습자가 포함되어 있을 것이다. 독립적인 실험을 원할 경우, 각 실험은 학습자를 무작위로 배정되는 별개의 집단들이 있어야 한다. 


적용할 학습자 집단을 결정하기 위해, 스튜디오  :ref:`Set up Group Configurations in edX Studio` 및 :ref:`Set Up Group Configuration for OLX Courses` 을 사용하여 집단을 편성한다.

그리고나서, 콘텐츠 실험을 :ref:`Add a Content Experiment in Studio` 혹은
:ref:`Add a Content Experiment in OLX` 로 추가할 때, 학습자 집단을 설정할 것인지 선택한다.  
