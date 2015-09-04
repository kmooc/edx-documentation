.. _Conditional Module:

####################
조건부 모듈
####################

********************
양식 설명
********************

조건부 모듈 입력의 주요 태그는

.. code-block:: xml

    <conditional> ... </conditional>

``조건부`` 는 모든 수의 모든 xmodule 태그 ( ``html`` , ``설문 조사`` , ``비디오`` 등) 또는 ``표시`` 태그를 포함할 수 있다.

================
조건부 태그
================

조건부 모듈의 단일 예시에 대한 주요한 컨테이너(container)이다. 이 태크에 대하여 다음과 같은 속성을 지정할 수 있다

.. code-block:: xml

    sources - location id of required modules, separated by ';'
    [message | ""] - message for case, where one or more are not passed. Here you can use variable {link}, which generate link to required module.

    [submitted] - map to `is_submitted` module method.
    (pressing RESET button makes this function to return False.)

    [correct] - map to `is_correct` module method
    [attempted] - map to `is_attempted` module method
    [poll_answer] - map to `poll_answer` module attribute
    [voted] - map to `voted` module attribute

========
표시 태그
========

Xmodules의 몇 가지 세트에 대한 Symlink이다. 이 태크에 대하여 다음과 같은 속성을 지정할 수 있다

.. code-block:: xml

    sources - location id of modules, separated by ';'

*********
예
*********

========================================
설문 조사에 의존하는 조건부의 예
========================================

.. code-block:: xml

    <conditional sources="i4x://MITx/0.000x/poll_question/first_real_poll_seq_with_reset" poll_answer="man"
    message="{link} must be answered for this to become visible.">
        <html>
            <h2>You see this because your vote value for "First question" was "man"</h2>
        </html>
    </conditional>

========================================================
설문 조사에 의존하는 조건부의 예 (<표시> 태그 사용하기) 
========================================================

.. code-block:: xml

    <conditional sources="i4x://MITx/0.000x/poll_question/first_real_poll_seq_with_reset" poll_answer="man"
    message="{link} must be answered for this to become visible.">
        <html>
            <show sources="i4x://MITx/0.000x/problem/test_1; i4x://MITx/0.000x/Video/Avi_resources; i4x://MITx/0.000x/problem/test_1"/>
        </html>
    </conditional>

================================================
문제에 의존하는 조건부의 예
================================================

.. code-block:: xml

    <conditional sources="i4x://MITx/0.000x/problem/Conditional:lec27_Q1" attempted="True">
        <html display_name="HTML for attempted problem">You see this, cause "lec27_Q1" is attempted.</html>
    </conditional>
    <conditional sources="i4x://MITx/0.000x/problem/Conditional:lec27_Q1" attempted="False">
        <html display_name="HTML for not attempted problem">You see this because "lec27_Q1" is not attempted.</html>
    </conditional>
