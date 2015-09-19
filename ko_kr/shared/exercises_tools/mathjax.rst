.. _MathJax in Studio:

############################################
Studio에서 MathJax 사용하는 방법 간략 소개
############################################

LaTex와 유사한 언어인 `MathJax <http://www.google.com/url?q=http%3A%2F%2Fwww.mathjax.org%2F&sa=D&sntz=1&usg=AFQjCNGef2H-mZCdmCo7-kWHfu9fUGVCfg>`_ 를 이용하여 깔끔하고 전문적으로 보이는 기호와 수식을 입력할 수 있다. MathJax로 작성한 수식은 한 문단에서 텍스트와 함께 표시되거나(내부 수식), 별도의 행으로 표시할수도(display 수식) 있다.
  
- 다음 두 가지 방법 가운데 하나를 이용하여 내부 수식을 생성할 수 있다.

  - MathJax 수식을 백슬래시와 **괄호(parentheses)** 로 묶는다.
    
    ``\( equation \)``

  - [mathjaxinline] 태그로 MathJax 수식을 묶는다. 태그에서 ([]) 를 사용한다

    [mathjaxinline] equation [/mathjaxinline]
    
- 다음 두 가지 방법 가운데 어느 하나를 이용하여 별도 수식을 생성할 수 있다.

  - MathJax 수식을 백슬래시와 **대괄호** 로 묶는다. 

    ``\[ equation \]``

  - [mathjax] 태그로 Mathjax 표현을 묶는다. 태그는 ([]) 를 사용한다. 

    [mathjax] equation [/mathjax]

HTML (텍스트) 구성요소 및 문제 구성요소에서도 MathJax를 사용할 수 있다.

.. note:: `http://www.onemathematicalcat.org/MathJaxDocumentation/TeXSyntax.htm <http://www.google.com/url?q=http%3A%2F%2Fwww.onemathematicalcat.org%2FMathJaxDocumentation%2FTeXSyntax.htm&sa=D&sntz=1&usg=AFQjCNEV8PtCX6Csp0lW7lDKOLIKCOCkHg>`_ 완결성 있는 MathJax 문서와 검정 도구를 확인할 수 있다.

****************************
HTML (텍스트) 구성요소
****************************

HTML 구성요소 편집기의 경우 비주얼(Visual) 보기 및 HTML 보기 모두에서 MathJax를 사용할 수 있다.

.. image:: ../../../shared/building_and_running_chapters/Images/MathJax_HTML.png
 :alt: Image of an HTML component with MathJax in both the Visual and HTML views

*********************
문제 구성요소
*********************

문제 구성요소 편집기의 경우 기본 편집기 및 고급 편집기 모두 MathJax를 사용할 수 있다.
아래의 예시에서, 설명 내부의 아인슈타인 방정식이 백슬래시와 괄호로 묶인 것에 주목한다. 해당 텍스트는 문단 내부(inline)에 표시된다. 나비어-스토크 방정식은 백슬래시와 대괄호로 묶여 있으므로 별도로 표시된다.

.. image:: ../../../shared/building_and_running_chapters/Images/MathJax_Problem.png
 :alt: Image of a problem component with MathJax in both the Visual and HTML views
