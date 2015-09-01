.. _Enrollment:

##########################
수강신청
##########################

강좌 개발팀과 교수자는 강좌에 학습자를 수강 등록하거나 수강 신청한 인원을 확인할 수 있으며, 필요에 따라 교수자 대시보드에서 학습자 수강 신청을 취소할 수 있다.

수강 신청 기간 동안 학습자는 직접 수강 신청 할 수 있다. ``www.edx.org`` 의 강좌는  edX 계정으로 등록한 모든 사람들이 공개적으로 수강신청할 수 있다. ``edge.edx.org`` 와 같은 곳의 강좌를 수강 신청할 경우, 수강신청은 강좌의 URL을 아는 학습자와 등록시킨 학습자만 가능하다. 

* :ref:`registration_enrollment`

* :ref:`enroll_student`

* :ref:`view_enrollment_count`

* :ref:`unenroll_student`

강좌의  수강신청 데이터는  edX Insights에서 이용할 수 있다. 강좌 보기의 교수자 대시보드에서 Insights에 접근할 수 있다: **교수자** 클릭 후, 각 페이지의 상단에 있는 배너의 링크를 클릭한다. 자세한 정보는  `Using edX Insights`_ 에서 확인한다.

.. _registration_enrollment:

*********************************
가입과 수강신청
*********************************

Before a student can enroll in a course, he or she must:

#. Register a user account, which includes supplying a valid email address, on
   ``www.edx.org``, ``edge.edx.org``, or your implementation of the edX
   platform. Each platform requires a separate user account.

#. Activate the registered account by following the emailed instructions.

As long as the course **Enrollment End Date** has not passed, students who
have registered and activated user accounts can enroll themselves in
``www.edx.org`` courses, or can enroll in other courses if they know the URL.
For a more detailed description of this process from a student's point of
view, see :ref:`Sample Student Login Guide`.

Course authors and instructors, however, can enroll students in a course either
before or after the students register their user accounts.

To work on a course, all course staff members must also have registered and
activated user accounts and be enrolled in the course.

.. _enroll_student:

*********************************
학습자 수강 등록 처리하기
*********************************

You enroll students, and other course staff members, in your course by
supplying their email addresses. After the **Enrollment End Date** for a
course students can no longer enroll themselves; however, you can still
explicitly enroll students.

When you enroll people in a course you have these options:

* **Auto Enroll**. When you choose this option, the people who you enroll do
  not need to complete an explicit course enrollment step. Of the list of email
  addresses that you supply, those that correspond to a registered user account
  are immediately enrolled in the course, and your course displays on the
  **Current Courses** dashboard for those users on log in. Email addresses on
  the list that do not match a registered user account are enrolled as soon as
  that account is registered and activated.

  If you do not select **Auto Enroll**, the people who you enroll must also actively locate your course and enroll themselves in it. These students see the course on their dashboards after they have done so.

* **Notify students by email**. When you choose this option, an email message is
  automatically sent to each of the email addresses that you supply. The message
  includes the name of the course and, for students who are not already
  enrolled, a reminder to use that same email address to enroll.

  An example of the email message that a student received when this option was
  selected during enrollment follows. In this example, the student already had a
  registered and activated edx.org account, and both **Auto Enroll** and
  **Notify students by email** were selected.

  .. image:: ../../../shared/building_and_running_chapters/Images/Course_Enrollment_Email.png
        :alt: Email message inviting a student to enroll in an edx.org course

To enroll students or staff members:

#. View the live version of your course.

#. Click **Instructor**, then click **Membership**. 

#. In the **Batch Enrollment** section of the page, enter the username or email
   address of the student, or enter multiple names or addresses separated by
   commas or new lines.

  You can copy and paste data from a CSV file of email addresses. However,
  note that this feature is better suited to courses with smaller enrollments,
  rather than courses with massive enrollments.

4. To streamline the course enrollment process, leave **Auto Enroll** selected.

#. To send students an email message, leave **Notify students by email**
   selected.

#. Click **Enroll**.

.. _view_enrollment_count:

***************************
전체 수강신청자 수 보기
***************************

After you create a course, you can access the total number of people who are
enrolled in it. When you view an enrollment count, note that:

* In addition to students, the enrollment count includes the course author,
  course team members, instructors, and course staff. (To work with a
  course in Studio or the LMS, you must be enrolled in that course.)

* Students can unenroll from courses, and course authors and instructors can
  unenroll students when necessary.

  **Note**: The enrollment count displays the number of currently enrolled
  students and course team staff. It is not a historical count of everyone who
  has ever enrolled in the course.

The total number of current enrollees is shown as the sum of the number of
people who selected each of the certification tracks (verified, audit, or
honor) that are available for your course.

To view the enrollment count for a course:

#. View the live version of your course.

#. Click **Instructor**, then click **Course Info** if necessary. 

  The **Enrollment Information** section of the page that opens shows the
  number of people who are currently enrolled in your course and in each of the
  certification tracks.

You can also view or download a list of the people who are enrolled in the
course. See :ref:`Student Data`.

.. _unenroll_student:

*********************************
학습자 수강 등록 취소하기
*********************************

You can remove students from a course by unenrolling them. To prevent students
from re-enrolling, course enrollment must also be closed. You use Studio to
set the **Enrollment End Date** for the course to a date in the past. See
:ref:`Set Important Dates for Your Course`.

**Note**: Unenrollment does not delete data for a student. An unenrolled
student's state remains in the database and is reinstated if the student does
re-enroll.

To unenroll students, you supply the email addresses of enrolled students. 

#. View the live version of your course.

#. Click **Membership**. 

#. In the **Batch Enrollment** section of the page, enter a username or an email
   address, or multiple names or addresses separated by commas or new lines.

#. To send students an email message, leave **Notify students by email**
   selected.

.. note:: The **Auto Enroll** option has no effect when you click **Unenroll**.

5. Click **Unenroll**. The course is no longer listed on the students'
   **Current Courses** dashboards, and the students can no longer contribute to
   discussions or the wiki or access the courseware.


.. _Using edX Insights: http://edx-insights.readthedocs.org/en/latest/
