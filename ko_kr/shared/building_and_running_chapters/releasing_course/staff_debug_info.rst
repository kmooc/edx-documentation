.. _Staff Debug Info:

############################
오류 제거 도움말
############################

edX 시스템은 학습자의 강좌 학습 진도를 계속 추적하며, 학습자가 동영상을 시청할때, 문제를 풀때 기록한다. 강좌의 운영팀이라면, 디버깅을 위해서 몇가지 데이터가 나타날 것이다. 모든 문제 아래에 **Staff Debug Info** 버튼이 있다.: 버튼을 클릭하면, 문제와 관련된 메타데이터가 팝업창으로 뜬다. 

아래 정보는 edx를 매일 사용하는데 필요한 것은아니지만 명확히 하기 위해 몇가지를 설명한다.:

``is_released``
  문제가 학습자에게 보이는지 여부를 나타낸다. 
``location``
  An internal unique identifier that corresponds to this problem. If you
  are having trouble with a problem, and need assistance from the edX support
  team, including this value will make it easier for them to track down the
  issue you're having with the problem.
``markdown``
  The text of the problem, in Markdown format. This is often written using Studio.
``display_name``
  문제의 명칭으로 학습자에게 나타난다. 
``max_attempts``
  The maximum number of times that a student can attempt to answer the problem
  correctly.
``attempts``
  The number of times that the currently logged in student has attempted to
  answer the problem correctly, so far. Every time this student attempts to answer
  this question, this number will go up, until it reaches ``max_attempts``.


