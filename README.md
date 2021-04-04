# Anti-Virus-Vaccine-Program
해시값 비교 등 여러 방법을 통한 안티바이러스 백신 프로그램
# 논산대건고등학교 2506 김태경 - 진로맞춤형 심층탐구 보고서
import os

fp = open('mal_ware.txt', 'rb') # 반드시 'Binary'형식으로 읽어 파일객체 생성
fread = fp.read() # 파일객체로부터 내용 읽어들여 버퍼에 저장
fp.close() # 파일 닫기

if fread[0:3] == b'X5O' : #파일의 첫번째 글자부터 세번째 글자가 'X5O'이라면
    print ('Virus') # 인자를 출력
    os.remove('mal_ware.txt') #파일 강제 삭제
else :
    print ('No Virus') #다르다면 다음과 같은 인자 출력
