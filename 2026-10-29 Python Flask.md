# Python, SQL 공부

# 오늘 배운 내용
- 가상환경 생성, 진입하는법
- Flask 데코레이터 작동원리
- 가상환경에서 pip 핍 설치법

# Flask 백엔드 기본 예제코드

'''
from flask import Flask - import로 Flask를 사용하겠다고 선언

app = Flask(__name__) # 서버가 열리면 이름을 app로 부르자

@app.route('/') -중요한부분 플라스크에서 @가 붙는걸 데코레이터라고 한다 아래 함수에 기능을 덧붙이는 문법이다 이 코드의 의미는 /주소로 요청이 오면 아래 함수를 실행시켜라같은 뜻이다
def hello_world():
    return 'Hello, World!'

if __name__ == '__main__':
    app.run(debug=True)
'''
- 코드들의 의미는 아래 내용과 같다

- 브라우저: "/ 보여줘" 
  → Flask가 요청을 받음
  → @app.route 로 등록된 규칙에서 '/'에 맞는 함수를 찾음
  → hello_world() 실행
  → 반환값을 HTTP 응답으로 만들어 브라우저에 전송
  → 화면에 Hello, World! 표시-

# 가상환경 진입, 생성하는법

# 가상환경 디렉터리 생성
- 윈도우에서 명령 프롬프트를 실행하고 다음 명령어를 입력해 C:\venvs라는 디렉터리를 생성 하나씩 친다

cd \
mkdir venvs
cd venvs


# 가상환경 생성
python -m venv Projekt


- 명령에서 python -m venv는 파이썬 모듈 중 venv라는 모듈을 사용한다는 의미다
- myproject 부분은 내 맘대로 이름을 바꿔도 된다

# 가상환경 진입
.\Projekt\Scripts\activate

-가상환경에 진입하려면 Projekt 가상 환경에 있는 scripts 디렉터리의 activate라는 명령을 수행해야 가상환경에 진입이 가능해진다

-가상환경에 진입한지 확인하고싶다면 왼쪽에 C:\ Projekt라는 또는 본인이 지정한 이름의 프롬포트를 확인할수있다

# 가상환경에서 나가는법

-진입한 가상환경에서 나가고싶다면 deactivate라는 명령을 실행해야하고 어느 위치에서 실행하든 상관이 없다

deactivate

-가상환경에서 벗어났다면 프롬포트가 사라졌을것이다

# 가상환경에서 플라스크 설치하기

- 1번 방법

가장 일반적인 방법은 pip install flask을 사용해 설치하는것이지만 만약에 

WARNING: You are using pip version 20.1.1; however, version 20.2.2 is available.
You should consider upgrading via the ‘c:\venvs\myproject\scripts\python.exe -m pip
install --upgrade pip’ command.
이와 같은 에러가 난다면

python -m pip install --upgrade pip을 사용해서 pip을 최신버전으로 설치해야한다
또 가상환경 진입이 안된다면 보안설정에 문제가 있는것이다 그럴땐
Set-ExecutionPolicy RemoteSigned -Force를 사용해서 영구적으로 변경해주면된다

# 주의 할것은 .\Projekt\Scripts\activate 라는 코드가 있다고 치면 앞에 있는 Projekt 부분을 본인이 현재 들어와있는 폴더명으로 바꿔줘야한다

- 가상환경에서 나갔는지 제대로 확인하고싶으면 pip list을 사용해서 깔린 프로그램이 여러가지 뜬다면 정상적으로 나온것이다










