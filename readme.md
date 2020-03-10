### BrainData Analysis with Matplotlib

##### 뇌파분석소프트웨어를 개발 하기 전 matplotlib을 사용하여 몇 가지 기능을 구현 해보았습니다

1. plot_stimulus_detection.ipynb

   자극을 detection 하기 위한 process를 연구하기 위해 작성된 코드 입니다. process 는 다음과 같습니다. 

   - peak detection : 데이터에서 peak를 찾아냅니다. ![find_peak](/Users/jeonsang-u/gbrain/find_peak.png)

   - peak 사이의 차이를 살펴 봅니다. ![peak_difference](/Users/jeonsang-u/gbrain/peak_difference.png)

   - peak 사이의 차이가 일정 수준 이상일 경우 자극으로 판단합니다.![find_stimulus](/Users/jeonsang-u/gbrain/find_stimulus.png)

     

2. liveplot.ipynb

   matplotlib animation을 사용하여 4개의 liveplot을 구현 해보았습니다.![4liveplot](/Users/jeonsang-u/gbrain/4liveplot.png)

3. liveplot_with_detection.ipynb

   자극을 실시간으로 감지하여 live plot을 그려줍니다. heatmap을 통해 자극의 횟수 또한 실시간으로 시각화 합니다.![live_stimulus](/Users/jeonsang-u/gbrain/live_stimulus.png)

4. simulate.ipynb

   실시간으로 데이터가 들어오는 가상의 상황을 만들어주기 위한 코드 입니다.

   realdata.csv 로 부터 실시간으로 일정 데이터를 live.csv로 보내 줍니다