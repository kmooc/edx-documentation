.. _Rerun a Course:

###################
강좌 재개강하기
###################

Studio 에서 강좌를 만드는 또 다른 방법은 기존 강좌를 재개강하는 것이다. 강좌 재개강하기를 선택하면, 전부는 아니지만, 원래 강좌 콘텐츠의 대부분이 새로운 강좌로 복제된다. 기존 강좌가 변경 될 일은 없다.

.. list-table::
   :widths: 45 45
   :header-rows: 1

   * - 콘텐츠 유형
     - 새로운 강좌로 복제되는가?
   * - 강좌 시작 날짜
     - 아니오. 2030년 1월 1일 자정으로 설정.
   * - 강좌 일정
     - 네. 강좌 시작일과 종료일을 변경해야 한다. 
   * - 강좌 구조 (주제, 소주제, 학습활동) 및 상태 (게시된 상태, 숨겨진 상태)
     - 네.
   * - 개별 문제 및 다른 구성요소
     - 네.
   * - 동영상 및 교재를 포함하여 강좌에 업로드된 파일
     - 네.
   * - 추가된 메뉴
     - 네, 모든 메뉴 콘텐츠 및 정해진 메뉴 순서도 복제.
   * - 공지사항
     - 네.
   * - 고급 설정
     - 네.
   * - 성적 규정
     - 네.
   * - 학습자 수강 데이터
     - 아니오.
   * - 교수자, 토론 운영자, 베타 테스터를 포함한 강좌 운영팀의 특별 권한
     - 아니오. 새로운 강좌를 개설한 자만 접근 가능.
   * - 직접  설정한  학습집단 
     - 아니오.
   * - 학습자 답안, 진도, 및 채점 데이터
     - 아니오.
   * - 수료증
     - 아니오.
   * - 게시글, 답글, 의견 및 다른 데이터
     - 아니오..
   * - 위키
     - 아니오.

See :ref:`Use Re-Run to Create a Course<Use ReRun to Create a Course>` and
:ref:`Update the New Course`.

.. _Use ReRun to Create a Course:

********************************************
Use Re-Run to Create a Course
********************************************

Before you re-run a course:

* For a course that is hosted on the `edge.edx.org`_ site, verify that you have
  permission to create courses in Studio. See :ref:`Use Studio on Edge`.

* For a course that is hosted on the `edx.org`_ site, contact your Program
  Manager. Your Program Manager will create the new course using the re-run
  feature, and then work with you to complete the steps to :ref:`update the new
  course<Update the New Course>`.

To re-run a course, you must have course creation privileges in Studio and you
must be a member of the course team for the course you want to re-run.
  
To re-run a course:

#. Log in to Studio. Your dashboard lists the courses that you have access to
   as a staff member.

#. Move your cursor over each row in the list of courses. The **Re-Run Course**
   and **View Live** options appear for each course.

  .. image:: ../../../shared/building_and_running_chapters/Images/Rerun_link.png
     :alt: A course listed on the dashboard with the Re-run Course and View 
           Live options shown 

3. Locate the course you want to re-run and click **Re-Run Course**. The
   **Create a re-run of a course** page opens with values already supplied in
   the **Course Name**, **Organization**, and **Course Number** fields.

  .. image:: ../../../shared/building_and_running_chapters/Images/rerun_course_info.png
     :alt: The course creation page for a rerun, with the course name, 
           organization, and course number supplied

4. Supply a **Course Run** to indicate when the new course will be offered. 
   
   Together, the course number, the organization, and the course run are used
   to create the URL for the new course. The combination of these three values
   must be unique for the new course. In addition, the total number of
   characters used for the name, organization, number, and run must be 65 or
   fewer.

5. Click **Create Re-Run**. Your **My Courses** dashboard opens with a status
   message about the course creation process.

   Duplication of the course structure and content takes several minutes. You
   can work in other parts of Studio or in the LMS, or on other web sites,
   while the process runs. The new course appears on your **My Courses**
   dashboard in Studio when configuration is complete.

.. _Update the New Course:

********************************************
Update the New Course
********************************************

When you create a course by re-running another course, you should carefully
review the settings and content of the new course. To assure a quality
experience for students, be sure to test the course thoroughly before the
course start date. See :ref:`Testing Your Course Content` and
:ref:`Beta_Testing`.

At a minimum, you will need to make these changes to prepare the new course for
release:

* Add course staff members, including discussion admins, moderators, and
  community TAs. See :ref:`Add Course Team Members` or
  :ref:`Course_Staffing`.
  
* Update course-wide dates, including course and enrollment start and end
  dates. See :ref:`Set Important Dates for Your Course`.

* Change the release dates of course sections, subsections, and units. See
  :ref:`Release Dates`.

* Change the due dates of subsections that are part of your grading policy. See
  :ref:`Set the Assignment Type and Due Date for a Subsection`.

* Delete or edit posts on the **Course Updates** page in Studio. See :ref:`Add
  a Course Update`.

* Review the files on the **Files & Uploads** page. To update a file that
  contains references to course-related dates, you will need to:
  
  #. Locate the source file.
  #. Change course-related dates in the file.
  #. Upload the revised version of the file.
  
  .. note:: If you use the same file name when you upload a revised file, 
   links to that file in course components and course handouts will continue to
   work correctly. If you rename a file and then upload it, you must also
   update all links to the original file name. See :ref:`Add Course Handouts`
   or :ref:`Add a Link to a File`.

* Review the staff biographies and other information on the course summary
  page and make needed updates. See :ref:`Providing a Course Overview`.

* Create initial posts for discussion topics and an "introduce yourself"
  post. See :ref:`Discussions`.

* Add initial wiki articles.
  
You can use the :ref:`course checklists<Use the Course Checklist>` to work
through the course and verify that it is ready for release. You can also refer
to the :ref:`Launch` chapter for tools and ideas that help you prepare the
course for launch.


.. _edge.edx.org: http://edge.edx.org
.. _edx.org: http://edx.org
