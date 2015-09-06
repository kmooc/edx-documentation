.. _Molecule Editor:

#######################
분자 편집기 도구
#######################

학습자는 분자 편집기(molecular editor)를 이용하여 분자 생성 방법을 학습할 수 있다. 분자 학습기를 통해 공유 결합 형성 및 형식 전하 규칙에 따른 분자를 구성할 수 있다. 분자 편집기를 이용하면 화학적으로 구성 불가하거나 불안정한 분자, 생명계에는 존재하지 않는 분자도 구성할 수 있다. 단, 화학적으로 구성 불가능한 분자 구조를 제출하고자 할 때 분자 편집기가 경고 메시지를 표시한다.

분자 편집기는 두 가지 도구, 즉 Peter Erl과 Bruno Bienfait가 개발한 JSME 분자 편집기 및 Jmol이 제공하는 자바스크립트 기반 분자 뷰어 JSmol를 포함하고 있다. (Studio는 이 두 가지 도구를 자동으로 사용한다. 별도로 내려받을 필요가 없다.) JSME 분자 편집기 및 JSmol에 관한 보다 자세한 정보를 `JSME Molecule Editor <http://peter-ertl.com/jsme/index.html>`_ 및 `JSmol <http://sourceforge.net/projects/jsmol/>`_ 에서 각각 확인할 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/Molecule_Editor.png
  :alt: Image of the molecule editor

.. _Create the Molecule Editor:

******************************
분자 편집기 생성하기
******************************

분자 편집기를 생성하기 위해서는 다음 파일이 필요한다.

* MoleculeAnswer.png
* MoleculeEditor_HTML.png
* dopamine.mol

http://files.edx.org/MoleculeEditorFiles.zip에서 상기 모든 파일을 하나의 .zip 파일로 내려받을 수 있다.

.. 참고:: 편집기 시작 시 표시되는 것은 도파민 분자이다. 다른 분자로 교체하고자 하는 경우 BioTopics 웹 사이트의 분자 목록(`list of molecules <http://www.biotopics.co.uk/jsmol/molecules/>`_ )에서 원하는 분자의 .mol을 내려받아 Studio에서 강좌에 해당하는 **파일 업로드** 페이지에 올린 후 예제 코드의 “dopamine.mol”을 “원하는이름.mol”로 바꾼다.

상기 이미지에 표시된 분자 편집기를 생성하려면 “문제(Problem)” 구성 요소 앞에 HTML 구성 요소 하나가 있어야 한다.

#. 강좌의 **Files & Uploads** 페이지에 상기 파일을 모두 업로드한다.
#. HTML 구성 요소를 생성한다.

  #. 문제를 생성하고자 하는 학습 활동에서 **새 구성 요소 추가** 아래에 있는 **HTML** 을 클릭한 후 다시 **HTML** 을 클릭한다.
  #. 구성 요소가 표시되면 **편집** 을 클릭한다.
  #. 구성 요소 편집기에 아래의 HTML 구성 요소를 복사해 넣는다.
  #. 원하는 대로 변경한 후 **저장** 을 클릭한다.

3. 문제 구성 요소를 생성한다.

  #. HTML 구성 요소에서 **새 구성 요소 추가** 아래의 **문제** 를 클릭한 후 **고급 문제 생성** 을 클릭한다.
  #. 해당 구성 요소가 표시되면 **편집** 을 클릭한다.
  #. 구성 요소 편집기에서 아래의 문제 구성 요소를 복사해 넣는다.
  #. **저장** 을 클릭한다.

.. _EMC Problem Code:

========================
분자 편집기 코드
========================

분자 편집기를 생성하려면 HTML 구성 요소 하나와 문제 구성 요소 하나가 필요한다.

HTML 구성 요소 코드
***************************

.. code-block:: xml

  <h2>Molecule Editor</h2>
  <p>The molecule editor makes creating and visualizing molecules easy. A chemistry professor may have you build and submit a molecule as part of an exercise.</p>
  <div>
  <script type="text/javascript">// <![CDATA[
  function toggle2(showHideDiv, switchTextDiv) {
              var ele = document.getElementById(showHideDiv);
              var text = document.getElementById(switchTextDiv);
              if(ele.style.display == "block") {
                  ele.style.display = "none";
                  text.innerHTML = "+ open";
                  }
              else {
                  ele.style.display = "block";
                  text.innerHTML = "- close";
              }
          }
  // ]]></script>
  </div>
  <div>
  <style type="text/css"></style>
  </div>
  <div id="headerDiv">
  <div id="titleText">Using the Molecule Editor<a id="myHeader" href="javascript:toggle2('myContent','myHeader');">+ open </a></div>
  </div>
  <div id="contentDiv">
  <div id="myContent" style="display: none;">
  <p>In this problem you will edit a molecule using the molecular drawing program shown below:</p>
  <img alt="" src="/static/MoleculeEditor_HTML.png" /></div>
  </div>
  <p>&nbsp;</p>
  <div id="headerDiv">
  <div id="titleText">Are the molecules I've drawn chemically possible?<a id="IntroductionHeader" href="javascript:toggle2('IntroductionContent','IntroductionHeader');">+ open </a></div>
  </div>
  <div id="contentDiv">
  <div id="IntroductionContent" style="display: none;">
  <p>The chemical editor you are using ensures that the structures you draw are correct in one very narrow sense, that they follow the rules for covalent bond formation and formal charge. However, there are many structures that follow these rules that are chemically impossible, unstable, do not exist in living systems, or are beyond the scope of this course. The editor will let you draw them because, in contrast to the rules of formal charge, these properties cannot be easily and reliably predicted from structures.</p>
  <p>If you submit a structure that includes atoms that are not possible or are beyond the scope of this course, the software will warn you specifically about these parts of your structure and you will be allowed to edit your structure and re-submit. Submitting an improper structure will not count as one of your tries. In general, you should try to use only the atoms most commonly cited in this course: C, H, N, O, P, and S. If you want to learn about formal charge, you can play around with other atoms and unusual configurations and look at the structures that result.</p>
  </div>
  </div>
  <div id="ap_listener_added">&nbsp;</div>




문제 구성 요소 코드
***************************

.. code-block:: xml

  <problem>
  <p>The dopamine molecule, as shown, cannot make ionic bonds. Edit the dopamine molecule so it can make ionic bonds.</p>
  <p>When you are ready, click Check. If you need to start over, click Reset.</p>
    <script type="loncapa/python">
  def check1(expect, ans):
      import json
      mol_info = json.loads(ans)["info"]
      return any(res == "Can Make Ionic Bonds" for res in mol_info)
      </script>
    <customresponse cfn="check1">
      <editamoleculeinput file="/static/dopamine.mol">
          </editamoleculeinput>
    </customresponse>
    <solution>
      <img src="/static/MoleculeAnswer.png"/>
    </solution>
  </problem>

**문제 2**

::

  <problem>
  <p>The dopamine molecule, as shown, cannot make strong hydrogen bonds. Edit the dopamine molecule so that it can make strong hydrogen bonds.</p>
  <script type="loncapa/python">
  def grader_1(expect, ans):
      import json
      mol_info = json.loads(ans)["info"]
      return any(res == "Cannot Make Strong Hydrogen Bonds" for res in mol_info)
  </script>
    <customresponse cfn="grader_1">
      <editamoleculeinput file="/static/dopamine.mol">
      </editamoleculeinput>
    </customresponse>
  </problem>

**문제 3**

::

  <problem>
  <p>The dopamine molecule has an intermediate hydrophobicity. Edit the dopamine molecule so that it is more hydrophobic.</p>
  <script type="loncapa/python">
  def grader_2(expect, ans):
      import json
      mol_info = json.loads(ans)["info"]

      hydrophobicity_index_str=mol_info[0]
      hydrophobicity_index=float(hydrophobicity_index_str[23:])
      return hydrophobicity_index &gt; .490
  </script>
    <customresponse cfn="grader_2">
      <editamoleculeinput file="/static/dopamine.mol">
      </editamoleculeinput>
  </customresponse>
  </problem>
