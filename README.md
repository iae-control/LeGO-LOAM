# LeGO-LOAM

이 저장소는 LOAM의 계산시간을 감소 시키고 수직법선 벡터를 Levenberg-Marquadt 알고리즘을 이용하여 맵핑하였다.
사용을 위해 사전에 GTSM 패키지를 설치하여야 한다.

## 의존성

  wget -O ~/Downloads/gtsam.zip https://github.com/borglab/gtsam/archive/4.0.0-alpha2.zip
  cd ~/Downloads/ && unzip gtsam.zip -d ~/Downloads/
  cd ~/Downloads/gtsam-4.0.0-alpha2/
  mkdir build && cd build
  cmake ..
  sudo make install
  ```

## 컴파일

아래 과정을 통해 다운로드 및 컴파일을 수행한다.

```
cd ~/catkin_ws/src
git clone https://github.com/RobustFieldAutonomyLab/LeGO-LOAM.git
cd ..
catkin_make -j1
```
초기 컴파일시 -j1 옵션을 사용한다. 추후 변경시 필요없다.
