.. _Gene Explorer:

##################
유전자 탐색기 (Gene Explorer) 도구
##################

`UMB <http://www.umb.edu/>`_ 생물학과에서 만든 유전자 탐색기 (GeneX)는 전사, 접합, 처리, 및 작은 가상 진 핵 유전자의 번역을 시뮬레이션한다. GeneX는 학습자가 유전자 시퀀스에 특정 돌연변이를 만들 수 있도록 허용하며, mRNA와 단백질에 있는 돌연변이 수를 계산하고 이들 돌연변이의 효과를 표시한다.  

특히, 유전자 탐색기는 다음을 수행한다:

#. promoter 및 terminator 찾기
#. pre-mRNA를 생산하기 위해 DNA 시퀀스를 읽기
#. splice 사이트 찾기
#. mRNA splice 하기 및 tail하기
#. 시작 코돈 찾기
#. mRNA 번역하기

.. image:: ../../../shared/building_and_running_chapters/Images/GeneExplorer.png
  :alt: Image of the Gene Explorer

유전자 탐색기에대한 추가 정보를 위해 `The Gene Explorer <http://intro.bio.umb.edu/GX/>`_ 를 살펴본다. 

********************
유전자 탐색기 코드
********************

.. code-block:: xml

  <problem>
  <p>Make a single base pair substitution mutation in the gene below that results in a protein that is longer than the protein produced by the original gene. When you are satisfied with your change and its effect, click the <b>SUBMIT</b> button.</p>
  <p>Note that a "single base pair substitution mutation" is when a single base is changed to another base; for example, changing the A at position 80 to a T. Deletions and insertions are not allowed.</p>
  <script type="loncapa/python">
  def genex_grader(expect,ans):
      if ans=="CORRECT": return True
      import json
      ans=json.loads(ans)
      return ans["genex_answer"]=="CORRECT"
  </script>
  <customresponse cfn="genex_grader">
  <editageneinput width="818" height="1000" dna_sequence="TAAGGCTATAACCGAGATTGATGCCTTGTGCGATAAGGTGTGTCCCCCCCCAAAGTGTCGGATGTCGAGTGCGCGTGCAAAAAAAAACAAAGGCGAGGACCTTAAGAAGGTGTGAGGGGGCGCTCGAT" genex_dna_sequence="TAAGGCTATAACCGAGATTGATGCCTTGTGCGATAAGGTGTGTCCCCCCCCAAAGTGTCGGATGTCGAGTGCGCGTGCAAAAAAAAACAAAGGCGAGGACCTTAAGAAGGTGTGAGGGGGCGCTCGAT" genex_problem_number="2"/>
  </customresponse>
  </problem>

이 코드에서: 

* **width** 및 **height** 는 픽셀 단위로 응용 프로그램의 크기를 지정한다.
* **genex_dna_sequence** 는 문제를 열 때 나타나는 기본 DNA 시퀀스이다.
* **dna_sequence** 는 응용 프로그램의 상태 및 학습자의 답안을 포함한다. 이 값은 **genex_dna_sequence** 와 동일해야 한다. 
* **genex_problem_number** 는 문제의 번호를 지정한다. 이 수는 MITx 7.00 x 강좌에 있는 5 개의 유전자 편집기 문제를 기반으로 한다 - 예를 들어 7.00 x 강좌에서 두 번째 유전자 편집기 문제처럼 문제를 만들 경우, **genex_problem_number** 값은 2가 된다. 이 수는 1, 2, 3, 4, 또는 5 이어야 한다.
