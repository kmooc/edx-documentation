.. This section is shared in course authors and OLX guides.

.. _Add a Content Experiment in OLX:

****************************************
OLX에 콘텐츠 실험 추가하기
****************************************

콘텐츠 실험을 설정하기 위하여 여러개의 XML 파일을 다루게 된다. 여기서는 두 개의 다른 학습자 집단에 다른 콘텐츠를 보여주는 콘텐츠 실험에 포함된 XML 파일들을 살펴 본다.

=====================================================
순차적인 파일에서 콘텐츠 실험 정의하기
=====================================================

``sequential`` 디렉토리에서, 소주제와 관련된 xml 파일에서 콘텐츠 실험을 참조할 수 있다. 예를 들면:

.. code-block:: xml

    ...
    <vertical url_name="name for the unit that contains the A/B test" display_name="A/B Test Unit">
        <split_test url_name="name of A/B test file in the split_test folder"/>
    </vertical>
    .....

``<split_test>`` 요소의  ``url_name`` 값은 ``split_test`` 디렉토리의 콘텐츠 실험명을 참조한다.  

.. caution::
  1개의 학습활동에 1종의 콘텐츠 실험만 정의할 수 있으며, 다른 구성요소의 모음은 다른 실험 집단과 관련된 것이다.  소주제 혹은 주제 레벨에서 1종의 콘텐츠 실험을 정의할 수 없고, 다른 집단과 관련된 다른 학습 활동들 혹은 소주제들을 둘 수 없다. 


.. _Define the Experiment Content in the Split Test File:

=====================================================
분할 테스트 파일에서 실험 콘텐츠 정의하기
=====================================================

순차적인 파일에서 콘텐츠 실험을 정의한 후에, ``split_test`` 디렉토리에 있는 파일을 테스트할 수 있도록 강좌 내용을 정의한다. 아래에 나타난 것 처럼 순차적 파일 내에서 ``<split_test>`` 요소를 참고한 파일이다. 

콘텐츠 실험 파일 안에, 실험 콘텐츠를 위한 요소들을 추가한다. 예를 들어 2 개의 서로 다른 콘텐츠를 비교하기 위하여 2개의  ``<vertical>`` 요소들을 추가한다. 

.. code-block:: xml

    <split_test url_name="AB_Test.xml" display_name="A/B Test" user_partition_id="0" 
                group_id_to_child='{"0": "i4x://path-to-course/vertical/group_a", 
                                    "1": "i4x://path-to-course/vertical/group_b"}'>
        <vertical url_name="group_a" display_name="Group A">
           <html>Welcome to group A.</html>
           <video url_name="group_a_video"/>
        </vertical>
        <vertical url_name="group_b" display_name="Group B">
            <html>Welcome to group B.</html>
            <problem display_name="Checkboxes">
                <p>A checkboxes problem presents checkbox buttons for student input. 
                   Students can select more than one option presented.</p>
                <choiceresponse>
                    <checkboxgroup direction="vertical" label="Select the answer that matches">
                        <choice correct="true">correct</choice>
                        <choice correct="false">incorrect</choice>
                        <choice correct="true">correct</choice>
                    </checkboxgroup>
                </choiceresponse>
            </problem>
        </vertical>
    </split_test>


위의 예문에서:

* ``user_partition_id`` 값은 ``policy.json`` 파일에 정의한 실험 ID를 참조한다.  

* ``group_id_to_child`` 값은 ``policy.json`` 파일에 정의한 집단 ID과 특정 콘텐츠의 집단 ID를 참조한다.  

  예를 들어, 집단 ``0`` 에서의 값``i4x://path-to-course/vertical/group_a``은 ``url_name`` 과 ``group_a`` 을 같게 하는 <vertical>요소를 일치시켜야 하다. 따라서, 집단 0 에서의 학습자는 ``<vertical>`` 로 콘텐츠를 보게 된다.

``policy.json`` 파일에 대해 더 정보를 원하면, :ref:`Set Up Group Configuration for OLX Courses` 를 확인한다.
