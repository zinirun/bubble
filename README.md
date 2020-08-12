# bubble
영작 시험지 제작 프로그램 (Python)

## Bubble의 시작
영어학원 4개에서 아르바이트를 하다가 느낀 것은 매주 원생들을 대상으로 <b>영어 작문 시험</b>을 실시한다는 것이었다. 보통 알바생(거의 대학생)이 제작을 도맡게 되는데 영어 문장만 주어지는 경우가 많아 직접 번역을 하던지, 파파고를 돌리던지 해서 시험지 형태로 제작을 해야 했다. 학원을 오가다가 프로그램 제작을 계획하고, 2019년 여름 제작에 돌입했다.

## 제작 과정
### 프로그램 알고리즘
```
1. 영어 문장을 입력받는다.
2. 파파고 api를 이용해서 한글로 번역한 데이터를 저장한다.
3. 데이터를 시험지 형식으로 바꾼다. (문제 형식으로)
```
### PyQt5와 library
파이썬 gui 프로그램은 처음 제작해봐서 pyqt5에 대한 공부를 많이 했다. api는 네이버 파파고측에서 개발자 이용 신청을 하면 key를 발급해주고 필요한 메소드들을 제공하기 때문에 큰 고민이 없었다.


GUI는 pyqt5 라이브러리 기반으로 코드를 직접 작성해도 되지만 QT Designer라는 좋은 툴이 있어서 편하게 작업했다. GUI 개체들과 파파고의 api를 연결하는 부분, 파파고에서 번역된 결과를 한글 문장에 맞게 리턴하는 부분에 각별히 신경썼다.


필요한 라이브러리들은 다음과 같다.
```python
import urllib.request
from PyQt5.QtWidgets import QMainWindow, QApplication
from PyQt5 import QtCore, QtGui, QtWidgets
from PyQt5.QtGui import QTextCursor
```
