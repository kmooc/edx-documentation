.. _Conditional Module:

####################
조건 모듈
####################

********************
양식 설명
********************

조건 모듈 입력의 주요 태그는

.. code-block:: xml

    <conditional> ... </conditional>

``conditional`` 은 모든 xmodule 태그 ( ``html`` , ``poll`` , ``video`` 등) 또는 ``show`` 태그를 포함할 수 있다.

================
conditional 태그
================

conditional 태그는 조건 모듈의 단일 인스턴스(instance)를 위한 컨테이너(container)이다. 이 태그는 다음의 속성을 지정할 수 있다

.. code-block:: xml

    sources - 필수 모듈의 id 위치로 ';' 로 분리
    [message | ""] - 하나 혹은 그 이상 통과하지 못한 경우 메세지. 필수 모듈에 링크를 만들 수 있는 {link} 변수를 이용할 수 있다. 
    [submitted] - `is_submitted` 모듈 메서드에 매핑
    (RESET 버튼 누그리는 이 함수에서 False를 리턴하게 한다.)
    [correct] - `is_correct` 모듈 메서드에 매핑
    [attempted] - `is_attempted` 모듈 메서드에 매핑
    [poll_answer] - `poll_answer` 모델 속성에 매핑
    [voted] - `voted` 모델 속성에 매핑

========
show 태그
========

Xmodules의 몇 가지 세트에 대한 Symlink이다. 이 태그에 대하여 다음과 같은 속성을 지정할 수 있다

.. code-block:: xml

    sources - 모듈의 id 위치로 ';'로 분리된다. 

*********
예
*********

========================================
설문 조사에 의존하는 조건의 예
========================================

.. code-block:: xml

    <conditional sources="i4x://MITx/0.000x/poll_question/first_real_poll_seq_with_reset" poll_answer="man"
    message="{link} must be answered for this to become visible.">
        <html>
            <h2>You see this because your vote value for "First question" was "man"</h2>
        </html>
    </conditional>

========================================================
설문 조사에 의존하는 조건의 예 (<show> 태그 사용하기) 
========================================================

.. code-block:: xml

    <conditional sources="i4x://MITx/0.000x/poll_question/first_real_poll_seq_with_reset" poll_answer="man"
    message="{link} must be answered for this to become visible.">
        <html>
            <show sources="i4x://MITx/0.000x/problem/test_1; i4x://MITx/0.000x/Video/Avi_resources; i4x://MITx/0.000x/problem/test_1"/>
        </html>
    </conditional>

================================================
문제에 의존하는 조건의 예
================================================

.. code-block:: xml

    <conditional sources="i4x://MITx/0.000x/problem/Conditional:lec27_Q1" attempted="True">
        <html display_name="HTML for attempted problem">You see this, cause "lec27_Q1" is attempted.</html>
    </conditional>
    <conditional sources="i4x://MITx/0.000x/problem/Conditional:lec27_Q1" attempted="False">
        <html display_name="HTML for not attempted problem">You see this because "lec27_Q1" is not attempted.</html>
    </conditional>
