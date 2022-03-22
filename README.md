# 1. Windows10 환경에서 OS 올리기 - Coral  

### 1-1) 준비물  
- 호스트 컴퓨터(Linux, Mac, Windows10)  
  - Python3 installed  
- 최소 8기가 이상 SD 카드  
- USB-C 파워 케이블  
- USB-C to USB-A 케이블  
- Wifi (or 이더넷 케이블)  
(주의 : 보드는 키보드와 모니터를 연결할 수 있지만, 권장하지 않음. 데스크탑 환경이 가능한 성능으로 설계되지 않음)  

### 1-2) Git Bash 설치  
- 윈도우 환경에서는 git bash 터미널이 필요  
- 물론, python3로 깔려있어야하는데, 여기서 문제는 git bash 터미널에서 파이썬으로 연결을 시켜줘야함  

```$ echo "alias python3='winpty python3.exe'" >> ~/.bash_profile```  
```$ source ~/.bash_profile```  

### 1-2) Flash the board  
- 코랄에는 Mendel Linux 밖에 설치할 수 없음  
- SD카드는 내장메모리에 OS 설치 후 제거할 예정(가즈베리파이처럼 작동하는데 SD카드가 꼭 필요하지 않음)  
- SD카드가 없으면 USB로도 가능 -> [manually flash the board over USB](https://coral.ai/docs/dev-board/reflash/#flash-a-new-board)  
- 설치 단계는 다음과 같음
 #### 1. 이미지 설치 후 압축 해제  
  ```flashcard_arm64.img``` 압축폴더 안에는 이미지 한 파일 들어있음  
 #### 2. balenaEtcher 같은 프로그램을 사용하여 ```flashcard_arm64.img```이미지 파일을 SD카드에 올려줌  
 #### 3. 이미지 파일을 SD카드에 올리는 동안 코랄 보드에 선 연결을 모두 해제한 상태로 스위치를 올려 boot mode로 바꿔줌  
![image](https://user-images.githubusercontent.com/35215836/135013583-89492e0c-2c30-4599-af67-e4c6f94e8cbc.png)  
   #### 4. 보드에 SD 카드 삽입(주의 : 아직 전원 연결을 안 한 상태)  
![image](https://user-images.githubusercontent.com/35215836/135022309-96bfcd98-2b32-4254-b63e-7fa10302aea4.png)  
   #### 5. 옵션 : OS 올리는 중 부트로더 로그를 보고싶다면, HDMI로 모니터를 연결하거나 시리얼 콘솔을 연결하면 됨  
   - 보드에 OS를 올리는 단계에서 아무것도 안 보이니 원한다면 선택  
   #### 6. 보드에 파워 케이블 연결(red LED on)  
   - SD 카드에 있는 이미지가 보드의 eMMC 메모리에 설치가 5~10분 정도 소요됨  
   - red LED가 꺼지면 완료  
 ![image](https://user-images.githubusercontent.com/35215836/135023176-bc9a0e85-39dc-42e6-85cc-68ff9e4134dd.png)  
   #### 7. LED 꺼진 후, 파워 케이블과 SD카드를 보드에서 연결 해제  
   #### 8. 부트 모드를 eMMC 모드로 전환(그림 4 참조)  
 ![image](https://user-images.githubusercontent.com/35215836/135023375-a1a12488-595c-445a-94e9-c0b8802d3a63.png)
   #### 9. 보드에 파워를 연결하면 Mendel Linux 실행됨  
   - OS설치 후 첫 실행시 3분 소요, 그 이후엔 더 빠르게 실행됨  


# 2. Reference

#### Getting Started : https://coral.ai/docs/dev-board/get-started/
