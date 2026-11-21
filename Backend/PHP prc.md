# PHP 설치법 (윈도우 11pro, VS17 x64 Thread Safe 버전기준)

1.  https://www.php.net/downloads.php?os=windows&osvariant=windows-downloads&version=8.5 링크에서 VS17 x64 Thread Safe 파일 다운
2. 압축 해제후 파일 이름 자체를 php 소문자로 변경후 > 잘라내기 > C 드라이브나 본인이 쓰는 디스크로 들어가 빈공간에 끌어다가 놓기
3. 윈도우 검색창 > 시스템 환경 변수 편집 > 환경변수 > 시스템변수 창에서 path를 찾아서 클릭 > 편집 > 새로만들기 > C:\php 경로로 하나 만들기
4. win + R > cmd 들어가서 php -v로 php가 깔렸는지 확인


# 1. PHP 기본 코드쓸때 지켜야하는 규칙, 문법

- 1. PHP는 기본적으로 변수를 만들때는 앞에 $을 만들어서 $Allow = 이런식으로 만들어줘야한다
- 2. 
