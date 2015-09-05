.. Section is shared in CA and OLX guides

.. _Set Up Group Configuration for OLX Courses:

************************************************
OLX 강좌의 집단 설정을 설정하기
************************************************

OLX 강좌의 ``policies`` 디렉토리에서 ``policy.json`` 파일에서 집단 설정을 정의한다. 

집단 설정을 하기 위해, ``user_partitions`` 의 정책키 값을 수정한다. 

.. note::  
  ``user_partitions`` 은 집단 설정을 위한 내부의 edX 플랫폼명이다. 

``user_partitions`` 값은 집단 설정의 JSON 컬랙션며, 각 학습자의 실험집단을 정의한다. 

.. note:: 
  의미 있는 집단 설정명을 이용한다. 콘텐츠 실험을 추가할 때 집단 설정명의 목록에서 선택한다. 

추가 정보를 위한 다음 예시를 살펴 본다. 

=============================================
예: 1개의 집단 설정
=============================================

다음 코드는 2개의 학습자 세그먼트로 집단 설정을 정의하는 JSON 오브젝트 예를 보여준다. 

.. code-block:: json

    "user_partitions": [{"id": 0,
                       "name": "Name of the group configuration",
                       "description": "Description of the group configuration.",
                       "version": 1,
                       "groups": [{"id": 0,
                                   "name": "Group 1",
                                   "version": 1},
                                  {"id": 1,
                                   "name": "Group 2",
                                   "version": 1}]
                                }
                       ]

위의 예에서:

* ``"id": 0`` 은 집단 설정을 의미한다. XML 강좌들에서, 이 값은 ``<split_test>`` element에서 ``user_partition`` 속성에서 참조된다. 
* ``groups`` 배열은 무작위로 배정된 학습자의 실험집단을 의미한다. XML 강좌들에서, 각 집단의 ``id`` 값은 ``<split_test>`` 엘리먼트에서 ``group_id_to_child`` 속성에 참조된다. 

==========================================================
예: 복수개의 집단 설정
==========================================================

다음 코드는 2개의 집단 설정을 정의한 JSON 오브젝트 예를 보여준다. 첫번째 그룹 설정은 2개의 실험 집단으로 학습자를 나누고, 두번째는 학생들을 3개의 실험 집단으로 나눈다. 

.. code-block:: json

    "user_partitions": [{"id": 0,
                         "name": "Name of Group Configuration 1",
                         "description": "Description of Group Configuration 1.",
                         "version": 1,
                         "groups": [{"id": 0,
                                     "name": "Group 1",
                                     "version": 1},
                                    {"id": 1,
                                     "name": "Group 2",
                                     "version": 1}]}
                        {"id": 1,
                         "name": "Name of Group Configuration 2",
                         "description": "Description of Group Configuration 2.",
                         "version": 1,
                         "groups": [{"id": 0,
                                     "name": "Group 1",
                                     "version": 1},
                                    {"id": 1,
                                     "name": "Group 2",
                                     "version": 1}
                                     {"id": 2,
                                     "name": "Group 3",
                                     "version": 1}
                                     ]}
                       ]

.. note:: 
  이 예가 보여주는 것 처럼. 각 집단 설정은 독립적이다. 집단 IDs 와 명칭은 집단 설정내에서 유일한 것이라야 하지만 강좌에서 모든 집단 설정에서는 아니다. 
