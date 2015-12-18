.. _Adding Pages to a Course:

###########################
강좌 메뉴 추가하기
###########################


*******************
개관
*******************

기본적으로 강좌에는 다음과 같은 메뉴가 있다.

* 강좌 내용
* 공지사항
* 게시판
* 위키
* 진도

기본 메뉴는 강좌 운영팀이 이름을 변경하거나 삭제할 수 없다. 

대신 메뉴를 추가할 수 있다. 추가 메뉴는 기본 메뉴 옆에 위치할 것이다.

예를 들어, 다음 그림과 같이 **강좌 일정** 및 **교수자 블로그** 를 포함할 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/page_bar_lms.png
 :alt: Image of the page bar in the LMS

강좌 운영팀은 성적 규정, 강좌 슬라이드, 또는 그 밖의 다른 목적으로 다른 메뉴를 만들 수 있다.

* Google calendar: Google calendar의 코드를 입력하면 사용 가능하다. 

* HTML calendar: :ref:`Code for Dynamic HTML Schedule` 에 있는 템플릿을 활용할 수 있다.

* Hangout:  :ref:`Google Instant Hangout` 에 자세한 정보가 나와있다.

필요한 정보가 있다면 아래 도움말을 살펴보길 바란다. 

* :ref:`Add a Page`
* :ref:`Show or Hide the Course Wiki Page`
* :ref:`Reorder Pages`
* :ref:`Delete a Page`
* :ref:`Code for Dynamic HTML Schedule`


.. _`Add a Page`:

****************
강좌 메뉴 추가하기
****************

#. Studio의 **콘텐츠** 에서 **강좌 메뉴** 를 선택한다. 

  .. image:: ../../../shared/building_and_running_chapters/Images/pages_page.png
   :alt: Image of the Pages screen


2. **신규 메뉴 추가** 를 클릭한다. **Empty** 제목을 가지는 페이지가 목록에 추가된다.

  .. image:: ../../../shared/building_and_running_chapters/Images/pages_empty.png
   :alt: Image of the Pages screen with a new Empty page

3. **편집** 을 클릭하면 HTML 에디터가 열린다.

  .. image:: ../../../shared/building_and_running_chapters/Images/pages_editor.png
   :alt: Image of the Page editor

4. 텍스트를 입력한다. 에디터 사용에 관해선 :ref:`Options for Editing HTML Components` 에 자세히 나와있다.
#. **설정** 을 클릭해서 **메뉴명** 을 수정한다. 이 메뉴명이 강좌에서 학습자에게 보이게 된다.
#. **저장** 을 클릭한다. 

강좌가 시작되면 학습자는 즉시 새 메뉴를 이용할 수 있다.

.. _Show or Hide the Course Wiki Page:

************************************************
위키 공개 설정하기
************************************************

기본적으로 강좌는 위키 페이지를 포함한다. 학습자와 강좌 운영팀은 콘텐츠와 다른 사람의 콘텐츠에 관한 의견을 게시하기 위해 위키를 사용할 수 있다.

담당자가 강좌에서 위키를 사용하지 않으려면, 위키 페이지를 숨길 수 있다.

위키에서 눈 아이콘은 강좌에서 위키 페이지를 볼 수 있음을 나타낸다.

.. image:: ../../../shared/building_and_running_chapters/Images/pages_wiki_on.png
 :alt: Image of the Pages page with the Wiki made visible

위키 페이지를 숨기기 위해 눈 아이콘을 클릭한다. 아이콘이 변할 것이다.

.. image:: ../../../shared/building_and_running_chapters/Images/pages_wiki_off.png
 :alt: Image of the Pages page with the Wiki made visible

위키 페이지가 보이도록 하기 위해 눈 아이콘을 다시 클릭한다.

.. note:: 강좌 운영팀이 페이지를 숨기더라도 콘텐츠는 위키에 남아 있다. 예를 들어 학습자가 위키 항목을 북마크했는데, 강좌 운영팀이 위키 페이지를 숨긴 경우, 학습자는 해당 위키 항목에 접근하기 위해 그 북마크를 여전히 사용할 수 있다. 이전에 위키 페이지에 게시된 모든 콘텐츠는 위키 페이지를 숨긴 후에도 이용 가능하며, K-MOOC에 로그인하는 모든 학습자는 URL을 알고 있을 경우 해당 콘텐츠에 접근할 수 있다. 

.. _Reorder Pages:

****************
메뉴 순서 바꾸기
****************

메뉴를 끌어서 다른 위치에 메뉴를 위치시켜 강좌에 있는 메뉴들을 재정렬할 수 있다.

메뉴를 이동하려면 마우스 포인터가 십자형 화살표로 바뀔 때까지 메뉴 행의 오른쪽에 있는 아이콘 위에 올려놓는다. 그 다음, 원하는 위치로 페이지를 클릭하여 끌어 옮긴다.

.. note:: 기본적으로 강좌에 포함된 강좌 내용, 강좌 정보, 게시판, 위키, 진도는 재배열할 수 없다. 

.. _Delete a Page:

****************
메뉴 삭제하기
****************

이전에 추가한 메뉴를 삭제하려면 페이지 목록에서 휴지통 아이콘을 클릭한다. 삭제를 확인하라는 메시지가 표시된다.

.. _Code for Dynamic HTML Schedule:

********************************
HTML Schedule 코드
********************************

강좌에서 HTML schedule을 제공하기 위해 페이지에 있는 다음의 코드를 사용할 수 있다.

.. code-block:: html


	<div class= "syllabus">

	<table style="width: 100%">
 		<col width="10%">
 		<col width="15%">
  		<col width="10%">
  		<col width="30%">
  		<col width="10%">
  		<col width="15%">
  		<col width="10%">
  
	<!-- Headings -->
 		 <thead>
    			<td class="day"> Wk of </td>
   			<td class="topic"> Topic </td>
   			<td class="reading"> Read </td>
    			<td class="video"> Lecture Sequence </td>	
    			<td class="slides"> Slides </td>
    			<td class="assignment"> HW/Q </td>
			<td class="due"> Due </td>
  		</thead>
  
	<!-- Week 1 Row 1 -->
 		 <tr class="first">
   			<td class="day">10/22</td>
			<td class="topic">Topic 1</td>
			<td class="reading">Ch. 1</td>
    			<td class="video"><a href="#">L1: Title</a></td>
    			<td class="slides"><a href="#">L1</a></td>
    			<td class="assignment"><a href="#">HW 1</a></td>
    			<td class="due">11/04</td>
  		</tr>
  
	<!-- Week 1 Row 2 -->
    		<tr>
    			<td class="day"> </td>
    			<td class="topic"></td>
    			<td class="reading"></td>
    			<td class="video"><a href="#">L2: Title</a></td>
    			<td class="slides"><a href="#">L2</a></td>
    			<td class="assignment">     </td>
   			 <td class="due">      </td>
  		</tr>

   		 <tr> <td class="week_separator" colspan=7> <hr/> </td> </tr>
  
	<!-- Week 2 Row 1 -->
 		 <tr>
    			<td class="day">10/29</td>
    			<td class="topic">Topic 2</td>
    			<td class="reading">Ch. 2</td>
    			<td class="video"> <a href="#">L3: Title<a></td>
   			 <td class="slides"><a href="#">L3</a></td>
    			<td class="assignment"><a href="#">Quiz 1</a></td>
    			<td class="due">11/11</td>
 		 </tr>
  
	<!-- Week 2 Row 2 -->
 		<tr>
  			<td class="day"></td>
    			<td class="topic"></td>
    			<td class="reading"></td>
    			<td class="video"><a href="#">L4: Title</a></td>
    			<td class="slides"><a href="#">L4</a> </td>
    			<td class="assignment"></td>
    			<td class="due"></td>
  		</tr>
  		<tr> <td class="week_separator" colspan=7> <hr/> </td> </tr>
  
	<!-- Week 3 Row 1 -->
  		<tr>
    			<td class="day">11/05</td>
    			<td class="topic">Topic 3</td>
    			<td class="reading">Ch. 3</td>
    			<td class="video"><a href="#">L5: Title</a></td>
    			<td class="slides"><a href="#">L5 </a></td>
    			<td class="assignment"><a href="#">HW 2</a></td>
    			<td class="due">11/18 </td>
  		</tr>
  
	<!-- Week 3 Row 2 -->
		<tr>
    			<td class="day"> </td>
    			<td class="topic"> </td>
    			<td class="reading"></td>
    			<td class="video"><a href="#">L6: Title</a></td>
    			<td class="slides"><a href="#">L6 </a></td>
    			<td class="video"></td>
    			<td class="assignment"></td>
    			<td class="due"></td>
  		</tr>
  		<tr> <td class="week_separator" colspan=7> <hr/> </td> </tr>
  
	<!-- Week 4 Row 1 -->
  		<tr>
    			<td class="day">11/12</td>
    			<td class="topic">Topic 4</td>
    			<td class="reading">Ch. 4</td>
    			<td class="video"><!--<a href="#">L7: Title</a>-->
    			L7: Title</td>
    			<td class="slides"><!--<a href="#">L7</a>-->L7</td>
    			<td class="assignment"><!--<a href="#">Quiz 2</a>-->
    			Quiz 2</td>
    			<td class="due"> 11/25 </td>
  		</tr>
  
	<!-- Week 4 Row 2 -->
    		<tr>
    			<td class="day"></td>
    			<td class="topic"></td>
    			<td class="reading"></td>
    			<td class="video"><!--<a href="#">L8: Title</a>-->
    			L8: Title</td>
    			<td class="slides"><!--<a href="#">L8</a>-->L8</td>
    			<td class="assignment"></td>
    			<td class="due"></td>
  		</tr>
  		<tr> <td class="week_separator" colspan=7> <hr/> </td> </tr>
  
	<!-- Week 5 Row 1 -->
  		<tr>
    			<td class="day">11/19</td>
    			<td class="topic">Topic 5</td>
    			<td class="reading">Ch. 5</td>
    			<td class="video"><!--<a href="#">L9: Title</a>-->
    			L9: Title</td>
    			<td class="slides"><!--<a href="#">L9</a>-->L9</td>
                        <td class="assignment"><!--<a href="#">HW 3</a>-->
                        HW 3</td>
    			<td class="due"> 12/02 </td>
  		</tr>
  
	<!-- Week 5 Row 2 -->
   		<tr>
    			<td class="day"></td>
    			<td class="topic"></td>
    			<td class="reading"></td>
    			<td class="video"><!--<a href="#">L10: Title</a>-->
    			L10: Title</td>
    			<td class="slides"><!--<a href="#">L10</a>-->L10 </td>
    			<td class="assignment"></td>
    			<td class="due"></td>
  		</tr>
  		<tr> <td class="week_separator" colspan=7> <hr/> </td> </tr>
  
	<!-- Week 6 Row 1 -->
  		<tr>
    			<td class="day">11/26</td>
    			<td class="topic">Topic 6</td>
    			<td class="reading">Ch. 6</td>
    			<td class="video"><!--<a href="#"><L11: Title</a>-->
    			L11: Title </td>
    			<td class="slides"><!--<a href="#">L11</a>-->L11</td>
    			<td class="assignment"><!--<a href="#">HW 4</a>-->
    			HW 4</td>
    			<td class="due">12/09</td>
  		</tr>
  
	<!-- Week 6 Row 2 -->
    		<tr>
			<td class="day"> </td>
    			<td class="topic"> </td>
    			<td class="reading"></td>
    			<td class="video"><!--<a href="#">L12: Title</a>-->
    			L12: Title</td>
    			<td class="slides"><!--<a href="#">L12</a>-->L12</td>
    			<td class="assignment"></td>
    			<td class="due">      </td>
		</tr>

	</table>
	</div>

