# 0629_aiffel

'''
#운영체제란?

운영 체제는 컴퓨터가 처리해야 하는 복잡하면서도 공통적인 기능들을 알아서 처리해주어 사용자가 신경쓰지 않아도 되도록 만들어주는 프로그램
그리고 컴퓨터 자원(HW,SW 자원 등을 알아서 효율적으로 관리 해주는것)

#이식성이란? https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=knix008&logNo=220098970726
어떠한 SW가 있을 때 특정 HW플랫폼 뿐만이 아닌 다른 HW플랫폼에 올려도 잘 동작하는 SW를 말하는것.

#라이브러리와 패키지? https://thinkreen.github.io/python/py-FunctionModuleClass/
라이브러리와 패키지는 둘다 다른 프로그램에서 포함하여 사용할 수 있는 일종의 코드 모음이라고 생각하면 쉽다
여러 모듈과 패키지를 묶어서 라이브러리라고 한다
특정 기능을 위한 여러 함수 또는 클래스를 담고 있는 보따리
파이썬을 설치할 때 기본적으로 설치되는 라이브러리를 표준라이브러리라고 한다 (예: time, sys, os, math, random, urllib 등)
python.org가 아닌 외부 3rd party에서 개발한 라이브러리를 외부라이브러리라고 한다(예: requests, scrapy, webbrowser 등)
간혹 표준라이브러리보다 써드파티 라이브러리 성능이 더 뛰어난 경우도 있다. (예: Numpy, Scipy, requests)

패키지는 일반적으로 패키지와 라이브러리 사이의 경계가 조금 모호한데, 사용중인 프로그래밍 언어마다 그 정의가 조금씩 달라질 수 있다. 
파이썬에서는 패키지는 패키지 관리자를 사용하여 설치하기 위한 준비된 라이브러리다. 가끔은 라이브러리를 배포하는 메커니즘을 말하기도 한다.
특정 기능과 관련된 여러 모듈들을 하나의 상위 폴더에 넣어 놓은 것을 패키지라고 합니다.
패키지(Package) 란, 간단히 말해서 특정 기능을 하는 작은 프로그램 단위입니다. 위에서 설명한 라이브러리와도 일맥상통하는 개념이죠. 
패키지가 조금 더 큰 범위를 포괄한다고 볼 수도 있지만, 두 용어를 같은 의미로 쓰기도 합니다.
개발을 하다보면 다양한 패키지들이 필요합니다. 패키지는 우리가 다운 받아 사용할 수 있는 다양한 툴을 제공하기 때문에, 
효율적인 개발 작업을 위해서는 많은 패키지들을 설치하거나 삭제하는 등 자유자재로 관리할 수 있어야 합니다.

우분투에서 패키지를 관리하기 위해 주로 쓰이는 명령어는 apt-get 입니다. 다음 글을 통해 명령어를 확인해보시죠.
패키지 안에 여러가지 하위폴더 가 더 존재할 수 있습니다.
파이썬 3.3이후 부터는 __init__.py가 없어도 패키지로 인식하지만, 하위 버전 호환을 위해 __init__.py 파일을 생성하여 패키지를 표현해주는 것이 안전하다.
.을 이용하여 파이썬 모듈을 계층적으로 관리할 수 있도록 하는 것을 말합니다.
A.B라고 하면 A는 패키지, B는 모듈이 됩니다. (예: sound.echo –> sound 패키지에 있는 echo모듈)

마지막으로 모듈은 파이썬에서는 모듈의 기능을 활용하여 코드를 분리하고 공유합니다. 이때 여러 기능들(함수, 변수, 클래스 등)을 따로 구현하여 파이썬 파일(.py)을 모듈(module)이라고 합니다. 
가끔 script라고도 부릅니다.
파이썬 코드 가장 위에 import로 불러오는 것이 모듈입니다. (예: import math)


#텐서플로우란?
바로 머신러닝/딥러닝에 특화된 라이브러리
텐서플로우는 머신러닝/딥러닝을 위해서 공통적으로 많이 쓰이는 함수 또는 클래스들을 한 곳에 모아놓은 보따리라고 볼 수 있다.

#API란? https://aws.amazon.com/ko/what-is/api/
API는 정의 및 프로토콜 집합을 사용하여 두 소프트웨어 구성 요소가 서로 통신할 수 있게 하는 메커니즘입니다. 예를 들어, 기상청의 소프트웨어 시스템에는 일일 기상 데이터가 들어 있습니다. 
휴대폰의 날씨 앱은 API를 통해 이 시스템과 "대화"하고 휴대폰에 매일 최신 날씨 정보를 표시합니다.

API는 Application Programming Interface(애플리케이션 프로그램 인터페이스)의 줄임말입니다. API의 맥락에서 애플리케이션이라는 단어는 고유한 기능을 가진 모든 소프트웨어를 나타냅니다. 
인터페이스는 두 애플리케이션 간의 서비스 계약이라고 할 수 있습니다. 
이 계약은 요청과 응답을 사용하여 두 애플리케이션이 서로 통신하는 방법을 정의합니다. API 문서에는 개발자가 이러한 요청과 응답을 구성하는 방법에 대한 정보가 들어 있습니다.

간단한 CLI 명령어 정리 https://tutorial.djangogirls.org/ko/intro_to_command_line/

터미널과 쉘의 차이 https://blog.naver.com/asianchairshot/221383363419
간단히 비유하면 터미널은 기반 즉 티비이고 쉘은 실행되는 것 즉 방송이라고 볼 수 있다!

- 콘솔
서버의 로컬 장치에서 직접 명령어를 작성할 수 있는 입출력 장치. 콘솔이 물리적인 장치라면 터미널은 원격제어 환경까지 포함하는 더 넓은 의미라고 할 수 있다.

- 터미널
서버의 로컬 또는 원격으로 접속할 수 있는 콘솔을 구현한 소프트웨어

- 쉘
실제로 명령어를 전달하고 결과를 전달받는 프로그램

#CLI 명령어

-뒤에 붙는 a는 숨김파일까지 전부 나타내라!를 뜻하고, l은 long format 자세하게 표현해달라는 명령어!
ls -al을 실행시키면 나오는 항목은 총 8개라고 한다!

각 항목의 의미는? https://securityspecialist.tistory.com/40
먼저 맨 앞의 '-'는 파일 유형이다. 해당 파일이 어떤 종류의 파일인지를 알 수 있다. '-'는 일반 파일, 'd'는 디렉터리, 'b'는 블록 디바이스, 'c'는 문자 디바이스, 'l'은 링크를 뜻한다.

두번째로 오는 'rw-r--r--'는 파일 허가권을 뜻한다.
여기서 r은 read w는 쓰기 x는 실행권한을 뜻하며 -면 권한을 주지 않고 알파벳이 적혀있으면 그 권한을 부여한다 앞에서부터 알파벳3개씩 끊어 처음오는 것은 유저권한 두 번째는 그룹권한 마지막은 파일에 대한 모든 유저의 권한을 나타낸다. 

세번째 '1' 은 링크의 수이다. https://ndb796.tistory.com/506
링크의 수가 무엇일까

네번째 'root'는 해당 파일에 대한 소유권을 가진 소유 사용자의 이름이다.

다섯번째 'root'는 파일을 소유한 그룹의 이름이다.

여섯번째 '0'은 파일 크기이다(바이트 단위). test.txt파일은 touch 명령어로 만든 빈 파일이기 때문에 크기가 0이다. https://godtaehee.tistory.com/9

일곱번째 '3월 27 01:22'는 파일의 최종 수정 일시이다.

마지막 여덟번째 'test.txt'는 해당 파일의 이름이다.

rm -r 디렉토리 명령은 그냥 rm은 그 파일만 지우지만 -r을 붙이게 되면 그 파일의 하위 디렉토리까지 전부 지울 수 있게 됩니다.
조금 더 설명을 덧 붙이자면
-r 옵션은 Recursive라는 의미로, 디렉토리 내부의 모든 파일 및 폴더에 대해 재귀적(반복적)으로 명령을 수행하라는 의미를 가집니다. 
그렇기 때문에 디렉토리에게는 -r 옵션이 필요하고, 개별 파일에게는 -r 옵션이 필요 없는 것이죠!


#CLI 환경에서 파일 옮기기!(GUI는 드래그 앤 드롭이 있지만...)

$ cd ~
$ mkdir new_folder
$ mv new_folder aiffel

mv 명령어는 영어 단어 Move를 줄여서 만든 것임을 어렵지 않게 추측할 수 있죠. 
파일이나 디렉토리를 옮기고 싶을 때에는 mv 명령어 뒤에 이동하고 싶은 파일, 이동할 목적지 디렉토리를 순서대로 입력해주면 됩니다.

$ cd aiffel
$ ls

new_folder
ls 를 입력해서 new_folder 가 목록에 나온다면 성공한 겁니다. 어때요, 간단하죠? 같은 원리로 파일 또는 디렉토리를 복사하는 것도 매우 간단합니다.

#cp 명령어!
다만, 여기서 한 가지 주의할 점은 cp 명령어는 rm(삭제) 명령어와 같이 디렉토리를 복사할 때 -r 옵션을 추가해주어야 복사하려는 디렉토리의 하위디렉토리까지 함께 복사한다는 점입니다.
개별 파일을 복사하고 싶을 때에는 -r 이 필요없죠.

첫번째 명령어에서 우리는 new_folder 를 .. 의 위치, 즉 상위 폴더에 복사했습니다. 물론 cp 는 Copy의 줄임말이죠.

$ cp -r new_folder ..
$ cd ..
ls
aiffel  data  new_folder


#파이썬 설치된 패키지 확인
pip list 이용! (apt list --installed, dpkg -l 등)
sudo apt list --installed 명령어를 입력하면 설치된 패키지의 목록이 차례로 출력됩니다 (이게 더 자세하게 나옴!)
sudo apt list --installed 명령어 뒤에 | grep (패키지명) 을 입력해주면 검색하는 단어를 포함하는 패키지만 출력됩니다. 
보통 아주 많은 패키지가 설치되어 있기 때문에 원하는 패키지의 설치 여부를 확인하려면 눈이 빠지게 리스트를 조사해야 하죠. 
이럴 때 grep 옵션을 사용하면 편리하게 원하는 패키지만 검색해 볼 수 있답니다!
$ sudo apt list --installed | grep acl

컴퓨터에 설치된 패키지 인덱스 정보를 업데이트 하려면 다음 명령어를 실행합니다. 아래 명령어는 주기적으로 실행시키는 습관을 가지는 것이 좋습니다.
$ sudo apt-get update

다음 명령은 모든 패키지에 대해, 새롭게 업데이트 된 버전이 있다면 전부 업그레이드를 하는 명령어입니다. 
하지만 패키지를 최신 버전으로 업그레이드 하는 것은 언제나 기존에 함께 사용되던 패키지들과의 충돌을 야기할 수 있기 때문에, 주의해야 합니다.
$ sudo apt-get upgrade

-참고-
sudo apt-get install -y cmatrix
cmatrix
sudo apt-get remove cmatrix

#가상환경이란?
프로젝트 별로 독립된 공간을 만들어주는 기능

#가상환경이 필요한 이유?
각각의 환경에서 요구하는 패키지 버전이 다르기 때문에
또는
예를 들어 프로젝트 A에서는 어떤 패키지의 1.5 버전을 사용해야 하고, 프로젝트 B에서는 그 패키지의 2.0 버전을 사용해야 하는 경우가 생깁니다. 
이 때 1.5버전과 2.0버전이 호환 되지 않는다면 개발하기가 상당히 불편해집니다. 이런 문제를 해결하기 위해 파이썬에서는 가상 환경을 사용합니다.

가상환경은 프로젝트마다 특정 패키지의 서로 다른 버전이 필요하거나 패키지 간 충돌이 생길 위험이 있을 때, 
각 프로젝트를 독립된 공간에서 사용할 수 있도록 하기 위한 기능입니다. 충돌이 생기기 전에, 애초에 프로젝트 간 공간을 나누어 놓겠다는 의도를 담고 있죠.

-용어정리-
패키지(package) 특정 기능을 위한 여러 함수 또는 클래스를 담고 있는 보따리로서, 라이브러리(library), 모듈(module)과 비슷한 개념 (다만 모듈은 조금 더 작은 개념으로 쓰이기도 함)

가상환경(virtual environment) 컴퓨터에 설치된 패키지 간의 충돌 또는 패키지 버전에 의한 이슈 등을 방지하기 위해 가상으로 나누어서 사용하는 환경 즉, 
특정 프로그램을 돌리기 위해 필요한 패키지들을 모아 만든 각각의 독립된 방과 같은 개념

which conda /opt/conda/bin/conda
여기서 which 명령어는 프로그램 설치 경로를 확인하는 것입니다. 윈도우즈에서는 where를 사용합니다. 프로그램 설치 여부와 경로를 확인하는데 유용합니다.

conda create -n my_env_name python=3.9.7 (가상환경 만들기)
-n 뒤에 my_env_name 과 같이 원하는 가상환경의 이름을 입력하면 됩니다. python=3.9.7 은 
이 가상환경에서는 3.9.7 버전의 python을 사용하겠다는 의미입니다. 가상환경이 잘 만들어졌는지 가상환경 리스트를 확인해봅시다.

conda env list (가상환경 리스트 확인)

conda activate my_env_name(가상환경 실헹)

conda deactivate (가상환경 나오기)

conda env remove -n my_env_name (가상환경 삭제)

base                  *  /opt/conda
my_env_name              /opt/conda/envs/my_env_name
* 는 현재 가상환경으로 어떤 환경을 사용하고 있는지 나타냅니다.

텐서플로우를 원하는 버전으로 설치하고 싶다면 다음과 같이 버전을 지정해 입력해주면 됩니다.
pip install tensorflow==2.6.0

아나콘다 관련 치트시트 https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf

https://dasima.xyz/linux-cd-%EC%A0%88%EB%8C%80%EA%B2%BD%EB%A1%9C-%EC%83%81%EB%8C%80%EA%B2%BD%EB%A1%9C/
절대경로 상대경로란?

'''
