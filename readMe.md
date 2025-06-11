## 현재 해결하지 못한 오류
ros2가 연결이 완료되었지만 PWM신호를 만들지 못함
단순히 GPIO 포트에서 High 하거나 Low하는 신호는 정상적으로 됨
jetson-io에서 configuration 수정을 하면 된다고 하지만 jetson-io가 켜지지 않고
바로 꺼지는 오류가 발생함

- 이를 해결하기 위해 커뮤니티를 탐색하여 해결방법들을 적용해봤지만 해결되지 않음

- 현재 최종적인 해결법은 NVIDIA SDK Manager를 사용하여 Jetpack 및 관련 소프트웨어 설치 Jetson
   초기화 방법이다.

관련사진은 다음과 같다

![alt text](image-9.png)

# mac os에서 원격 접속 방법
1. jetson xavier 에서 ifconfig로 ip확인
2. 확인된 ip를 이용하여 연결
```bash
username@ip
```
3. vscode에서 ssh연결시 동일한 방법(단 board가 로그오프되면 연결이 종료됨)


# ros 기본 명령어 모음 

## ros2 버전확인 방법

```bash
ros2 doctor
```

- 예상 출력

```bash
kim@kim-desktop:~$ ros2 doctor
/opt/ros/foxy/lib/python3.8/site-packages/ros2doctor/api/platform.py: 82: UserWarning: Distribution foxy is no longer supported or deprecated. To get the latest features, download the new versions at https://index.ros.org/doc/ros2/Installation/

All 4 checks passed
```

## 간단한 설치 확인 방법 혹은 테스트

터미널 2개를 열어서 확인할 수 있음

```bash
ros2 run demo_nodes_cpp talker
``

```bash
ros2 run demo_nodes_cpp listener
```


![alt text](image-8.png)


# ROS를 위한 linux

## 경로 찾기

```bash
cd /home/user/catkin_ws/src/linux_course_files/move_bb8_pkg/src/
```

/home/user/ 는 일반적으로 사용자의 **HOME** 폴더이다. **HOME**폴더는 **~** 로 축약할 수 있다.

```bash
cd ~/catkin_ws/src/linux_course_files/move_bb8_pkg/src/
```

![alt text](image-6.png)

## ls 명령어는 숨겨진 파일을 시각화 하지 못한다.

```bash
ls -la
```

![alt text](image-7.png)

> '.'의 의미는 숨겨져 있다는 의미이다.


# shortcuts
## start terminal

> window + T

## show applications

> window + A

