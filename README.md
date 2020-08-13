# Lalaca
[홍익대학교 컴퓨터 공학과 졸업 프로젝트] 인생샷 도우미, 라라카입니다.
라라카는 'Life is Like A Camera' 에서 따온 이름입니다.






## 프로젝트 기기

프로젝트 기기의 대략적인 사용도는 다음 그림과 같습니다.

[그림1 : 라라카 기기 구성도]

삼각대에는 아두이노를 통해 상하, 좌우 움직임용 서버 모터가 달려있으며 현재 카메라의 바닥까지의 높이를 측정하기 위한 초음파 센서또한 부착되어있습니다.
아두이노는 부착될 삼각대와 블루투스 통신 이용해 조작됩니다.

또 하나의 아두이노 기기를 사용해 리모컨을 만들고, 사진을 찍을 수 있는지 여부를 알려줍니다.






## 프로젝트 기능 설명

프로젝트의 기능은 크게 두가지로 나뉩니다.


[그림2 : 프로젝트 기능 (라라카 첫 화면)]




------------
### 1. 사진 구도 설정하기

[그림3 : 사진 구도 설정 첫 화면]

사진 구도 설정하기를 통해 [그림 3]과 같이 현재 카메라에 찍히고 있는 화면에서 본인이 위치하고 싶은 구간을 정한뒤, 카메라 고정 완료를 누릅니다.
본인이 찍히고 싶은 곳에 대략적인 위치를 하게 되면, 라라카는 자동으로 본인이 설정한 구도에 맞춰 모터를 조정, 준비가 완료되면 리모컨을 통해 신호를 보냅니다.

[그림 4 : 사진 구도 설정 뒤 사진 찍는 과정]


리모컨을 통해 사진 찍기 입력을 주면 라라카는 사진을 저장하게 되며,
현재 삼각대의 높이 , 서보모터의 구도, 그리고 사용자 정보와 위치, 별점 등을 json형식으로 서버에 보내게 됩니다.





------------
### 2. 근처에서 찍은 다른 사람의 사진 보기

[그림 5 : 근처에서 찍은 다른 사람들 사진 리스트를 보여줌]

이 기능으로 들어오게 되면 라라카는 자체 추천 시스템을 통해 근처에서 찍은 사진들을 정렬해서 보여주게 됩니다.
사진을 선택하게 되면 다음과 같이 [사진 찍은 장소로 안내하기] 기능을 사용할 수 있습니다.
사진 찍은 장소에 도착하게 되면 라라카는 [이 구도로 사진 찍기] 기능을 사용할 수 있게 됩니다.

[그림 6 : 이 구도로 사진 찍기 버튼]


이 구도로 사진 찍기 버튼을 누르게 되었을 경우, 앞에서 설정된 사진 구도 설정하기 기능이 사진을 기반으로 자동으로 완성된 화면이 나오게 됩니다.
이후에는 [사진 구도 설정하기] 기능과 같은 기능을 수행하게 되지만, 차이점이 존재합니다.
추천 받은 사진과 삼각대의 높이, 그리고 카메라의 방향이 크게 다르면 어느정도 다른지 사용자에게 알려주고, 물리적인 수정을 요구하게 됩니다.


[그림 7 : 물리적인 수정 요청]

물리적인 수정이 완료 된 뒤에는 [사진 구도 설정하기] 기능과 같은 진행 순서로 사진을 찍고, 서버에 정보를 저장하게 됩니다.


## 프로젝트에 사용된 HW, SW

------------
### HW

스마트폰 
아두이노 * 2
삼각대
블루투스 센서
서보모터 * 2
초음파 거리 센서


------------
### SW

Tenserflow Lite
AWS EC2
Android
Python
Node.js
등
