.. _Add Files to a Course:

###########################
강좌에 파일 추가하기
###########################

강좌 콘텐츠에 이미지를 사용하거나 강좌 계획서와 같이 다른 소프트웨어로 작성한 문서를 사용하려면, 강좌 운영팀은 **파일 업로드**  페이지에 해당 파일을 업로드 한 다음 강좌에 있는 구성 요소에서 업로드 된 파일을 링크해야 한다.

*******************
개관
*******************

스튜디오에서 **콘텐츠** 메뉴 아래에 있는**파일 업로드** 에 업로드 된 강좌 파일을 관리할 수 있다.

* :ref:`Upload a File`
* :ref:`File URLs`
* :ref:`Sort Files`
* :ref:`Filter Files`
* :ref:`Find Files`
* :ref:`Lock a File`
* :ref:`Delete a File`


.. _Upload a File:

*******************
파일올리기
*******************
 
강좌에 학습자가 접근하기 원하는 파일을 업로드할 수 있다. 파일을 업로드 한 후, **파일 업로드** 페이지에서 생성된 URL을 사용하여 강좌 구성요소, 강좌 업데이트 또는 학습 자료 페이지에 파일을 연결할 수 있다. 학습자는 강좌 운영팀이 파일에 대한 링크를 만들 경우에만 파일을 볼 수 있다. 

.. 참고:: 업로드된 파일에 대한 URL이 생성되면 파일 이름은 URL의 일부가 되고 학습자가 파일에 접근할 때 볼 수 있게 된다. 
주의할 점은 예를 들어 Answerkey.pdf와 같이, 공유해서는 안 되는 콘텐츠에 관한 정보를 포함하는 파일 이름 사용을 피해야 한다는 것이다. 

.. 주의::
   PDF, 이미지 등 학습 자료가 많을 경우 파일 크기를 줄이기 위해 압축을 권장한다.

   If you have files that are larger than 50 MB after compression and need them
   for your course, contact your edX program manager.

   Furthermore, do not add video or audio files, or large data sets that are to
   be used by students. You should use YouTube or another hosting service to
   host multimedia files for your course. For information about storing large
   data sets for student use, contact your edX program manager.

To upload files:
 
#. From the **Content** menu, select **Files & Uploads**.
#. Click **Upload New File**.
#. In the **Upload New File** dialog box, click **Choose File**.
   
#. In the **Open** dialog box, select one or more files to upload, then click
   **Open**.

   .. note::
      If you upload a file that has the same name as an existing course file, the
      original file is overwritten without warning.

5. To upload additional files, click **Load Another File** and repeat the
   previous step.

6. To close the dialog box, click the **X** in the top right corner.

You see the new files on the **Files & Uploads** page.


.. _File URLs:

********************************************
Use File URLs to Reference Uploaded Files
********************************************


After you upload a file, you can link to it from a component, from a course
update, or in the course handouts, using the generated URLs on the **Files and
Uploads** page. On the **Files & Uploads** page, the **URL** column lists the
Studio URL and web URL for each file.

* To link to the file or image from within a course (that is, from a component,
  a course update, or a course handout), use the Studio URL. You cannot use
  the web URL to link to a file or image from within your course.

* To provide a link to the file or image from outside the course, use the
  web URL. 


.. note:: If you lock a file, the web URL no longer works for external access
   to the file, unless the person accessing the URL is enrolled in and logged in to
   the course.

To copy a URL from the file list, double click the URL in the **URL** column so
that the value is selected, then copy it.


.. _Sort Files:

*********************
Sort Files
*********************

On the **Files & Uploads** page, by default, files are sorted by the **Date
Added** column, with the most recently added files at the top.

You can sort your files by any column that has a blue column header. For
example, to sort the list by name, click the **Name** column header.

Change the sort order by clicking a sortable column header. The direction of the
arrow in the column header indicates whether the order is ascending or
descending. Each time you click the column header, the sort order reverses.

The current sort order is shown at the top of the file list, and the active sort
column header is underlined.


.. _Filter Files:

*********************
Filter Files
*********************

You can filter the list of files by type so that only a selected type of file is
visible. The list remains in the current sort order.


.. list-table::
   :widths: 10 20

   * - **Type**
     - **File Types Include**
   * - Images
     - .gif, .ico, .jpg, .jpeg, .png, .tif, or .tiff
   * - Documents 
     - .pdf, .txt, Microsoft Office and Open Office documents, presentations, or
       spreadsheets
   * - Other
     - Files not included in the other types, such as .html, .js, or .sjson


To filter the list of files by type:
 
#. On the **Files & Uploads** page, click the **Type** column header.

#. In the dropdown list, select the type of file that you want to view. 

The list refreshes to show only the type of file you selected, and the column
header changes to reflect the type of file that you have filtered by.

To reset the list and view files of all types, click **Show All** in the **Type**
dropdown list.


.. _Find Files:

*******************
Find Files
*******************

The **Files & Uploads** page lists up to 50 files.  If your course has more than
50 files, additional files are listed on other pages.

The range of the files listed on the page, and the total number of files, are
shown at the top of the page.

You can navigate through the pages in these ways:

* Use the **<** and **>** buttons at the top and bottom of the list to navigate
  to the previous and next pages.

* At the bottom of the page, you can edit the first number in the page range.
  Click the number to place your cursor in the field, then enter the page number
  you want to jump to.

  .. image:: ../../../shared/building_and_running_chapters/Images/file_pagination.png
   :alt: Image showing the pair of page numbers at the bottom of the Files and
         Uploads pages with the first number in editable mode and circled


.. _Lock a File:
 
*******************
Lock a File
*******************

By default, anyone can access a file you upload if they know the URL, even
people not enrolled in your class.

To ensure that those not in your class cannot view the file, click the lock
icon.

.. note:: If you lock a file, the web URL no longer works for external access
   to the file, unless the person accessing the URL is enrolled in and logged in to
   the course.
 

.. _Delete a File:

*******************
Delete a File
*******************

To delete a file, click the **x** icon next to the file.  You are prompted to
confirm the deletion.

.. warning:: If you delete a file that has been linked from a course component,
   those links will be broken. Before deleting files that are used in a course,
   make sure you update the links to those files in the course.
 
