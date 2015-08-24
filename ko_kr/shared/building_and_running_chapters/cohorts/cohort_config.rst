.. _Enabling and Configuring Cohorts:

############################################
학습 집단 기능 활성화 및 설정하기
############################################

강좌의 학습 집단 구성을 위해서, 자동 배치, 직접 배치, 혼합적 배치 방법을 통해 학습자를 학습 집단에 배치할 수 있는데
이에 대한 사항은 학습 집단에 학습자 배치하기에서 확인할 수 있다. 학습 집단 혹은  전체 학습자에게 동일하게 강좌 전반이나 학습 내용별로 토의 주제를 나눌 수 있다. :ref:`학습 집단에 학습자 배치하기`. 

학습 집단 활용 방법을 선택한 후, (해당하는 경우) 다음의 구성 단계에 따라 학습 집단 기능을 활성화 할 수 있다.:

#. :ref:`학습 집단 활성화하기<Enable cohorts>`.

#. 학습자를 학습 집단에 배치하는 방법 결정하기:
   
  * :ref:`자동 학습 집단 정의<Define Auto Cohorts>`

  * :ref:`Define manual cohorts<Define Manual Cohorts>` 와
    :ref:`manually assign students<Assign Students to Cohorts Manually>` 
    
  * :ref:`Use a combination of automated and manual assignment<Hybrid Assignment>` 

3. 선택적으로, 학습 집단에 따라 나누길 원하는 토의 주제를 확인한다.
   
  * :ref:`course-wide discussion topics to be divided by cohort<Identifying Private CourseWide Discussion Topics>` 를 원한다면
    일부 설정작업을 완료해야 한다.

  * 반면, 학습 내용별 토의 주제를 학습 집단별로 나누기를 원한다면,
    더 이상의 구성 절차를 완료할 필요가 없다. 대신 :ref:`content-specific discussion topics to be unified<Make ContentSpecific Discussion Topics Unified>` 를 원한다면, 약간의 구성 단계를 완료해야 한다.

이러한 구성 절차는 스튜디오와 교수자 대시보드에서 완료할 수 있다. 최상의 학습자 경험을 위해 강좌 시작일 이전에 학습 집단 기능을 활성화하는 것이 좋다. 

강좌가 진행되는 중에 활성화된 학습 집단 기능을 변경하고자 한다면, 
:ref:`Altering Cohort Configuration` 를 참고하라. 


.. _Enable cohorts:

***************************
학습 집단 기능 활성화하기
***************************

#. 스튜디오에서 강좌를 연다. 

#. **설정** 을 선택하고, **고급 설정** 을 선택한다. 

#. **학습 집단 설정** 칸에서, 중괄호 사이에 커서를 위치시킨다.

#. ``"cohorted": true``를 입력한다. 

#. **변경사항 저장** 을 클릭하면. 변경사항 저장을 클릭하면, 스튜디오는 재배열을하고, 입력된 값은 새로운 줄에 들여쓰기가 된다.
   
 .. image:: ../../../shared/building_and_running_chapters/Images/Enable_cohorts.png
  :alt: Cohort Configuration dictionary field with the cohorted key defined 
        as true

다음으로 :ref:`implement the automated assignment strategy<Implementing the Automated Assignment Strategy>`, :ref:`implement the manual assignment strategy<Implementing the Manual Assignment Strategy>` 를 할 수 있으며, 두 방법 모두를 설정할 수 있다. 

강좌의 학습자 프로필 정보에서 강좌에 등록된 모든 학습자의 학습 집단 배치 결과를 포함하는 보고서를 볼 수 있다. 자세한 내용은 :ref:`View and download student data` 에서 확인할 수 있다
 

.. _Implementing the Automated Assignment Strategy:

***************************************************
학습자 자동 배치
***************************************************

학습자를 학습 집단에 자동 배치하기 위해서, 고급 설정의 **학습 집단 설정** 에서 자동 학습 집단을 정의해야 한다

강좌에서 학습자 자동 배치나 혼합 배치를 사용하고자 한다면, 이 절차를 완료해야 한다.
관련 정보는 :ref:``All Automated Assignment`` 또는 :ref:`Hybrid Assignment` 에서 확인할 수 있다. 

.. _Define Auto Cohorts:

=======================
자동 학습 집단 정의
=======================

자동 학습 집단을 정의하기 전에, 학습자는 자신이 속해 있는 학습 집단의 이름을 볼 수 있다.
학습 집단에 따라 나뉘어진 토의 주제 게시판에 게시된 각각의 게시물에는 “이 게시물은 {cohort name}만 볼 수 있습니다.” 라는 메세지가 나타난다. 관련해서 :ref:`Read the Cohort Indicator in Posts` 에서 확인할 수 있다.

.. note:: 학습 집단을 제거하거나  집단명을 바꿀 수 없다.
  강좌 운영 중에 설정한 학습 집단 기능을 변경하고자 한다면, 
  진행 중인 강좌에서 :ref:`Altering Cohort Configuration` 를 참조할 수 있다. .

#. 스튜디오에서 강좌를 연다. 

#. **설정** 을 선택한 후, **고급 설정** 을 클릭한다.

#. **학습 집단 설정** 칸에서, 중괄호(``{``)문자 뒤에 커서를 위치한 후, 엔터키를 누른다. 

#. 새로운 행에서 ``"auto_cohort_groups":`` policy key 를 정의하고, 대괄호 (``[ ]``) 안에 학습 집단명을 입력하면 된다. 이 방법으로 자동 학습 집단을 정의하거나 학습 집단을 한 개만 정의할 수 있다. 
   
   여러개의 학습 집단을 정의하기 위해서, 각 학습 집단명을 새로운 행에서 큰 따옴표 (``" "``)안에 입력하고, 
   큰 따옴표 안에 입력된 학습 집단은 쉼표로 구분한다.
   다음은 자동 학습 집단을 정의한 예이다.:
   
   .. code-block:: xml 

      "auto_cohort_groups": [
          "Example Cohort Name A",
          "Example Cohort Name B",
          "Example Cohort Name C"
      ]
   

.. comment is here only to allow indented formatting of next line

  You can also define only a single auto cohort. Type ``"auto_cohort_groups":
  ["Example Cohort Name"]`` and then press Enter again.

5. 닫는 중괄호 다음에는 쉼표를 입력한다 (``],``). 설정한 각각의 policy keys는 반드시 쉼표로 구분해야 한다
   
#. **변경사항 저장** 을 클릭하면, 스튜디오는 재설정된다. 입력 내용이 잘 저장되었는지 확인하기 위해서 다시 **학습 집단 설정**으로 이동한다.
     저장할 때 필요한 쉽표가 없는 경우에는 입력 이전으로 돌아가고, 경고창은 뜨지 않는다.

 .. image:: ../../../shared/building_and_running_chapters/Images/Multiple_auto_cohort_groups.png
  :alt: Cohort Configuration dictionary field with the auto_cohort_groups key 
        with three values

.. spacer line

 .. image:: ../../../shared/building_and_running_chapters/Images/Single_auto_cohort_group.png
  :alt: Cohort Configuration dictionary field with the auto_cohort_groups key 
        with one value

학습 집단에 배치되지 않은 학습자는, 토의 주제 게시판을 방문했을 때 자동 학습 집단 중 하나에 임의로 배치된다.


.. _Implementing the Manual Assignment Strategy:

***************************************************
학습자 직접 배치
***************************************************

학습자를 학습 집단에 직접 배치하기 위해, 우선 직접 배치를 정의하고 나서 학습자를 학습 집단에 배치하게 된다.

직접 배치나 혼합 배치 방식을 사용하기 위해서는 다음의 절차 따라야 한다.
이와 관련해서는 :ref:`All Manual Assignment`  혹은 :ref:`Hybrid Assignment`.

학습자 직접 배치 절차를 완료하기 전에, 반드시 :ref:`학습 집단 기능 활성화<Enable Cohorts>` 를 설정해야 한다.


.. _Define Manual Cohorts:

======================
직접 학습 집단 정의
======================

직접 학습 집단을 정의하기 전에, 학습자는 자신이 속한 학습 집단명을 볼 수 있다.학습 집단에 따라 나뉘어진 토의 주제 게시판에 게시된 각각의 게시물에는 “이 게시물은 {cohort name}만 볼 수 있습니다.” 라는 메세지가 나타난다. 이와 관련해서는 :ref:`Read the Cohort Indicator in Posts` 에서 확인할 수 있다. 

.. note:: 학습 집단을 제거하거나 명칭을 바꿀 수 없다.강좌 운영 중에 학습 집단 기능을 변경하고자 한다면, :ref:`Altering Cohort Configuration` 를 참조할 수 있다. .

#. 스튜디오에서 강좌를 열고, **적용 결과 보기** 를 클릭한다. 

#. **교수자** 를 클릭한 후, **회원** 을 클릭한다. (참고: 현재 학습 집단 선택) 

#. 하단의 **학습 집단 관리** 영역을 찾는다.

#. **학습 집단 추가하기** 를 클릭한다.

#. **새로운 학습 집단명** 칸에 학습 집단명을 입력하고, 저장하기를 클릭한다.


.. _Assign Students to Cohorts Manually:

====================================
학습자를 학습 집단에 직접 배치하기
====================================

.. note:: 강좌가 시작되기 전에 직접 배치를 완료하는 것이 좋다.
 만일 강좌가 시작한 후에도 학습자가 계속 등록한다면, 새로 등록한 학습자를 계속해서 학습 집단에 배치해야 한다.

#. 스튜디오에서 강좌를 열고, **적용 결과 보기** 를 클릭한다.

#. **교수자** 를 클릭한 후, **회원** 을 클릭한다. (참고: 현재 학습 집단 선택) 

#. 하단의 **학습 집단 관리** 영역을 찾는다. 

#. 드롭 다운 목록에서 학습 집단을 선택한다.

#. **학습자 추가** 칸에서 학습자의 사용자 이름이나 이메일 주소를 입력하거나, 다수 학습자의 사용자 이름이나 이메일 주소를 쉼표 또는 새로운 행으로 구분하여 입력한다. 또한 이메일 주소가 저장된 CSV 파일 데이터를 복사한 후 이 칸에 붙여 넣기 할 수도 있다.

#. **학습자 추가** 버튼을 클릭한다. 학습자는 선택된 학습 집단에 배치된다. 해당 학습 집단에 몇 명의 학습자가 추가 되었는지 메시지가 나타난다. 학습자는 하나의 학습 집단에만 속할 수 있으므로, 이 메시지는 이 절차에 의해 다른 학습 집단으로 배치된 학습자의 수를 나타낸다.

모든 등록 학습자의 학습 집단 배치 결과를 포함하는 보고서는 학습자 프로필 정보에서 확인할 수 있다. 관련해서는 ref:`View
and download student data` 에서 살펴볼 수 있다. 

.. _Assign Students to Cohort Groups by uploading CSV:

========================================================
Assign Students to Cohorts by Uploading a CSV File
========================================================

In addition to assigning students to cohorts by entering usernames or email
addresses directly on the Membership page in the Instructor Dashboard, you can
also upload a .csv file containing a list of students and the cohorts that you
want to assign them to.

Any assignments to cohorts that you specify in the .csv files you upload
will overwrite or change existing cohort assignments. The configuration of
your cohorts should be complete and stable before your course begins. You
should also complete manual cohort assignments as soon as possible after any
student enrolls, including any enrollments that occur while your course is
running. To understand the effects of changing cohort assignments after your
course has started, see :ref:`Altering Cohort Configuration`.

.. note:: Be aware that the contents of the .csv file are processed row by row,
  from top to bottom, and each row is treated independently. 

  For example, if your .csv file contains conflicting information such as
  Student A being first assigned to Cohort 1, then later in the spreadsheet
  being assigned to Cohort 2, the end result of your .csv upload is that Student
  A is assigned to Cohort 2. However, the upload results file will count Student
  A twice in the "Students Added" count: once when they are added to Cohort 1,
  and again when they are added to Cohort 2. Before submitting a file for
  upload, check it carefully for errors.

The requirements for the .csv file are summarized in this table.

.. list-table::
    :widths: 15 30

    * - **Requirement**
      - **Notes**
    * - Valid .csv file

      - The file must be a properly formatted comma-separated values file: 

        * The file extension is .csv.
        * Every row must have the same number of commas, whether or not there
          are values in each cell. 
    * - File size
      - The file size of .csv files for upload is limited to a maximum of 2MB.               
    * - UTF-8 encoded
      
      - You must save the file with UTF-8 encoding so that Unicode characters
        display correctly. 

        See :ref:`Creating a Unicode Encoded CSV File`.

    * - Header row
      - You must include a header row, with column names that exactly match those 
        specified in "Columns" below.
    * - One or two columns identifying students      
      - You must include at least one column identifying students: 
        either "email" or "username", or both. 

        If both the username and an email address are provided for a student,
        the email address has precedence. 
        
        In other words, if an email address is present, an incorrect or non-
        matching username is ignored.

    * - One column identifying the cohort
            
      - You must include one column named "cohort" to identify the cohort
        to which you are assigning each student.

        The specified cohorts must already exist in Studio.

    * -                        
      - Columns with headings other than "email", "username" and "cohort" are
        ignored.

Follow these steps to assign students to cohorts by uploading a .csv file.
      
#. View the live version of your course. For example, in Studio, click **View
   Live**.

#. Click **Instructor**, then click **Membership**. 

#. Scroll to the **Cohort Management** section at the bottom.

#. Under **Assign students to cohorts by uploading a CSV file**, click
   **Browse** to navigate to the .csv file you want to upload. 

#. Click **Upload File and Assign Students**. A status message displays
   above the **Browse** button.

#. Verify your upload results on the **Data Download** page. 

   Under **Reports Available for Download**, locate the link to a .csv file with
   "cohort_results" and the date and time of your upload in the filename. The
   list of available reports is sorted chronologically, with the most recently
   generated files at the top.

The results file provides the following information:  

.. list-table::
    :widths: 15 30

    * - **Column**
      - **Description**
    * - Cohort
      - The name of the cohort to which you are assigning students.
    * - Exists
      - Whether the cohort was found in the system. TRUE/FALSE. 
      
        If the cohort was not found (value is FALSE), no action is taken for students you assigned to that cohort in the .csv file.

    * - Students Added
      - The number of students added to the cohort during the row by row
        processing of the .csv file.             
    * - Students Not Found
      - A list of email addresses or usernames (if email addresses were not
        supplied) of students who could not be matched by either email address
        or username and who were therefore not added to the cohort.
             
For a report that includes the cohort assignment for every enrolled student,
review the student profile information for your course. See :ref:`View and
download student data`.


.. _Creating a Unicode Encoded CSV File:

====================================
Creating a Unicode-encoded CSV File
====================================

Make sure the .csv files that you upload are encoded as UTF-8, so that any
Unicode characters are correctly saved and displayed.

.. note:: Some spreadsheet applications (for example, MS Excel) do not allow you
   to specify encoding when you save a spreadsheet as a .csv file. To ensure that
   you are able to create a .csv file that is UTF-8 encoded, use a spreadsheet
   application such as Google Sheets, LibreOffice, or Apache OpenOffice.


.. _Altering Cohort Configuration:

*************************************************
Altering Cohort Configuration in a Running Course
*************************************************

The configuration of the cohort feature should be complete and stable before
your course begins. Manual cohort assignments should be completed as soon as
possible after any student enrolls, including any enrollments that occur while
your course is running. 

If you decide that you must alter cohort configuration after your course starts
and activity in the course discussion begins, be sure that you understand the
consequences of these actions:

* :ref:`Changing Student Cohort Assignments`
* :ref:`Renaming a Cohort`
* :ref:`Deleting a Cohort`
* :ref:`Disabling the Cohort Feature`


.. _Changing Student Cohort Assignments:

=================================
Change Student Cohort Assignments
=================================

After your course starts and students begin to contribute to the course
discussion, each post that they add is visible either to everyone or to the
members of a single cohort. When you change the cohort that a student is
assigned to, there are three results:

* The student continues to see the posts that are visible to everyone.

* The student sees the posts that are visible to his new cohort.

* The student no longer sees the posts that are visible only to his original
  cohort.

The visibility of a post and its responses and comments does not change, even if
the cohort assignment of its author changes. To a student, it can seem that
posts have "disappeared".

To verify the cohort assignments for your students, download the  :ref:`student
profile report<View and download student data>` for your course. If changes are
needed, you can :ref:`assign students<Assign Students to Cohorts Manually>` to
different cohorts manually on the **Membership** page of the Instructor
Dashboard.


.. _Renaming a Cohort:

===============
Rename a Cohort
===============

Name changes for cohorts are not supported. The **Membership** page of the
Instructor Dashboard does not offer an option to rename your manual cohorts.

It is possible to change the value for the ``auto_cohort_groups`` policy key on
the **Advanced Settings** page in Studio. However, changing the names in the
listed name:value pairs **does not** result in any renamed auto cohorts.
Instead, changing the value for the ``auto_cohort_groups`` policy key has these
results.

* The system uses the new value that you saved for the ``auto_cohort_groups``
  policy key to create one or more additional auto cohorts.

* The system begins to assign students who do not have a cohort assignment to
  the newly defined cohort or cohorts. Students also continue to be assigned to
  any auto cohorts that were not affected by your changes.

  The system uniformly distributes students among all of the auto cohorts that
  exist when an assignment is needed. The size of each cohort is not considered.

* The original cohort or cohorts remain in the system. Any students who were
  assigned to the original cohorts remain assigned to them.

  For the results of assigning any students who remain in the original cohorts
  to other cohorts, see :ref:`Changing Student Cohort Assignments`.

* The system converts the original auto cohorts, which are no longer listed as
  values for ``auto_cohort_groups``, into manual cohorts. The system no longer
  assigns students to those cohorts automatically. These cohorts are listed as
  manual cohorts on the **Membership** page of the Instructor Dashboard.


.. _Deleting a Cohort:

================
Delete a Cohort
================

Deletion of cohorts is not supported. The **Membership** page of the Instructor
Dashboard does not offer an option to delete your manual cohorts.

It is possible to change the value for the ``auto_cohort_groups`` policy key on
the **Advanced Settings** page in Studio. However, removing any of the listed
name:value pairs **does not** result in the deletion of any cohorts. Instead,
changing the value for the ``auto_cohort_groups`` policy key has these results.

* The cohorts that you removed from the policy key remain in the system.

* Any students who were assigned to those cohorts remain assigned to them. 
  
  For the results of assigning any students to other cohorts, see :ref:`Changing
  Student Cohort Assignments`.

* The system no longer assigns students to the cohorts automatically. 

* The cohorts are listed as manual cohorts on the **Membership** page of the
  Instructor Dashboard, and you can continue to assign students to them
  manually.


.. _Disabling the Cohort Feature:

==========================
Disable the Cohort Feature
==========================

You can disable the cohort feature for your course. Follow the instructions for
:ref:`enabling the cohort feature<Enable Cohorts>`, but set ``"cohorted":
false``. All discussion posts immediately become visible to all students.

If you do re-enable the cohort feature by setting ``"cohorted": true``, all
previous student cohort assignments are reenabled, and all visibility settings
for posts are reapplied. However, any posts created while the cohort feature
was disabled will remain visible to all users.
