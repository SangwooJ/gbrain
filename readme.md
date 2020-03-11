## BrainData Analysis with Matplotlib

### 뇌파분석소프트웨어를 개발 하기 전 matplotlib을 사용하여 몇 가지 기능을 구현 해보았습니다

Multi Channel MicroChip은 쥐 뇌표면에 삽입되어 여러 뇌의 위치로 부터 뇌파를 읽어들입니다. 쥐의 발바닥을 자극하면 특정 채널에서 뇌파 시그널에 유의미한 변화를 관찰 할 수 있습니다. 본 프로젝트의 목적은 이러한 원리를 이용하여 쥐로부터 뇌파를 실시간으로 읽어들여 쥐의 질병 및 이상행동을 감지 하고자 함에 있습니다.



Data 형식은 csv 이며 구조는 다음과 같습니다. 실제데이터는 회사보안정책상 공개하지 않습니다

_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _

time | ch1 | ch2 | ch3 | ch4 ... | ch 128

0.002  732. 843.2 392.5 . . . 

0.004. 989.3  . . .. . 

.

.

13.982

_ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _


#### 1. plot_stimulus_detection.ipynb

   자극을 detection 하기 위한 process를 연구하기 위해 작성된 코드 입니다. process 는 다음과 같습니다. 

   - peak detection : 데이터에서 peak를 찾아냅니다. ![find_peak](/images/find_peak.png)

   - peak 사이의 차이를 살펴 봅니다. ![peak_difference](/images/peak_difference.png)

   - peak 사이의 차이가 일정 수준 이상일 경우 자극으로 판단합니다.![find_stimulus](/images/find_stimulus.png)

     

#### 2. liveplot.ipynb

   여러가지 채널의 정보를 한번에 띄우기위해 matplotlib animation을 사용하여 4개의 채널에 대한 liveplot을 구현 해보았습니다.![4liveplot](/images/4liveplot.png)

#### 3. liveplot_with_detection.ipynb

   자극을 실시간으로 감지하여 live plot을 그려줍니다. heatmap을 통해 자극의 횟수 또한 실시간으로 시각화 합니다. heatmap을 통해 어떤 위치에서 자극이 발생하였는지 한눈에 시각화 할 수 있습니다.  ![live_stimulus](/images/live_stimulus.png)

#### 4. simulate.ipynb

   실시간으로 데이터가 들어오는 가상의 상황을 만들어주기 위한 코드 입니다.

   realdata.csv 로 부터 실시간으로 일정 데이터를 live.csv로 보내 줍니다
