.. _Circuit Schematic Builder:

##################################
회로도 문제
##################################

회로도 문제에서 학습자는 인터랙티브 그리드(interactive grid)위에 전압 소스, capacitors, 저항, MOSFETs 등 회로 요소를 나열할 수 있다. 그런 다음, 채점을 위해 회로에 대한 DC, AC, 또는 과도기 분석 결과를 시스템에 제출한다.

.. image:: ../../../shared/building_and_running_chapters/Images/CircuitSchematicExample.png
 :alt: Image of a circuit schematic builder

*********************************************
회로도 문제 만들기
*********************************************

#. 문제를 만들려는 학습활동에서 **신규 구성 요소 추가** 에서 **문제** 를 클릭한 다음 **고급** 탭을 클릭한다.
#. **회로도** 를 클릭한다. 
#. 표시되는 구성 요소에서 **편집** 을 클릭한다. 
#. 구성 요소 편집기에서 예제 코드를 본인의 코드로 대체한다.
#. **저장** 을 클릭한다.

**문제 코드**

위의 이미지에서 문제를 만들려면, 다음의 코드를 고급 편집기로 붙여 넣는다.

.. code-block:: xml

 <problem>
    <p>Make a voltage divider that splits the provided voltage evenly.</p>
      <schematicresponse>
      <center>
      <schematic height="500" width="600" parts="g,r" analyses="dc"
      initial_value="[["v",[168,144,0],{"value":"dc(1)","_json_":0},["1","0"]],["r",[296,120,0],{"r":"1","_json_":1},["1","output"]],["L",[296,168,3],{"label":"output","_json_":2},["output"]],["w",[296,216,168,216]],["w",[168,216,168,192]],["w",[168,144,168,120]],["w",[168,120,296,120]],["g",[168,216,0],{"_json_":7},["0"]],["view",-67.49999999999994,-78.49999999999994,1.6000000000000003,"50","10","1G",null,"100","1","1000"]]"
      />
      </center>
        <answer type="loncapa/python">
      dc_value = "dc analysis not found"
      for response in submission[0]:
        if response[0] == 'dc':
            for node in response[1:]:
                dc_value = node['output']
      if dc_value == .5:
        correct = ['correct']
      else:
        correct = ['incorrect']
      </answer>
      </schematicresponse>
    <schematicresponse>
    <p>Make a high pass filter.</p>
    <center>
    <schematic height="500" width="600" parts="g,r,s,c" analyses="ac"
    submit_analyses="{"ac":[["NodeA",1,9]]}"
    initial_value="[["v",[160,152,0],{"name":"v1","value":"sin(0,1,1,0,0)","_json_":0},["1","0"]],["w",[160,200,240,200]],["g",[160,200,0],{"_json_":2},["0"]],["L",[240,152,3],{"label":"NodeA","_json_":3},["NodeA"]],["s",[240,152,0],{"color":"cyan","offset":"0","_json_":4},["NodeA"]],["view",64.55878906250004,54.114697265625054,2.5000000000000004,"50","10","1G",null,"100","1","1000"]]"/>
    </center>
    <answer type="loncapa/python">
    ac_values = None
    for response in submission[0]:
      if response[0] == 'ac':
          for node in response[1:]:
              ac_values = node['NodeA']
    print "the ac analysis value:", ac_values
    if ac_values == None:
      correct = ['incorrect']
    elif ac_values[0][1] < ac_values[1][1]:
      correct = ['correct']
    else:
      correct = ['incorrect']
    </answer>
    </schematicresponse>
        <solution>
            <div class="detailed-solution">
                <p>Explanation</p>
                <p>A voltage divider that evenly divides the input voltage can be formed with two identically valued resistors, with the sampled voltage taken in between the two.</p>
                <p><img src="/c4x/edX/edX101/asset/images_voltage_divider.png"/></p>
                <p>A simple high-pass filter without any further constaints can be formed by simply putting a resister in series with a capacitor. The actual values of the components do not really matter in order to meet the constraints of the problem.</p>
                <p><img src="/c4x/edX/edX101/asset/images_high_pass_filter.png"/></p>
            </div>
        </solution>
 </problem>
