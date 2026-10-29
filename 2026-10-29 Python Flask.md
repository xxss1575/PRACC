# Python SQL 공부

# 오늘 배운 내용


# Flask 백엔드 기본코드

'''Python
from flask import Flask

# 1. 괄호 안에 언더바(_) 2개씩 꼭 붙여야 합니다!
app = Flask(__name__)

# 2. 골뱅이 주소 밑으로 엔터를 쳐서 내려야 합니다!
@app.route('/') 
def hello_world():
    return 'Hello, World!'

if __name__ == '__main__':
    app.run(debug=True)
'''
