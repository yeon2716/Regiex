# 정규표현식
# /regiex/  ==> Regular expression의 약자

# 언제 사용하는가?
 - 텍스트에서 우리가 원하는 특정한 패턴을 찾을때 (전화번호형태의 패턴, 웹사이트주소형태의 패턴,이메일형식의 패턴을 찾을때 등등)
 - 사용자가 입력한 텍스트가 이메일이나 패스워드와 같이 특정한 패턴에 부합하는지 유효성검사흘 할때도 사용할수 있다
 - 정규식은 문자를 검사하고자할때 사용하는 식이다.

# 정규식은 /로 시작하여 "나는 정규표현식"임을 나타낸다
- /우리가 찾고자하는 패턴/

- /regex/i
- i는 어떤 옵션에 따라 검색할건지 플래그를 활용할수 있다.

# 문법
 1) Groups anf ranges
   - |   : 또는
   - ()  : 그룹
   - []  : 문자셋, 괄호안의 어떤 문자든
   - [^] : 부정 문자셋, 괄호안의 어떤 문자가 아닐때
   - (?:) : 찾지만 기억하지는 않음 
2) 제한하기위해 사용하는
  - ? :없거나 있거나(zero or one)
  - * : 없거나 있거나 많거나(zero or more)
  - + : 하나 또는 많거나(one or more)
  - {n} : n번 반복
  - {min,} : 최소
  - {min,max} : 최소 그리고 최대

3) 경계에 대한
   - \b  : 단어경계      
   - \B  : 단어경계가 아님
   - ^   : 문장의 시작
   - $   : 문장의 끝

  4) 특징을 이용하는 방법
     - \ : 특수문자가 아닌 문자
     - . : 어떤 글자(줄바꿈 문자 제외)
     - \d: 숫자
     - \D: 숫자 아님
     - \w : 문자
     - \W : 문자 아님
     - \s  : 공백
     - \S  : 공백 아님

![image](https://github.com/understanding963852/604_regiex/assets/60366769/2efc7d18-872e-4750-9f08-0f52552bba49)

![image](https://github.com/understanding963852/604_regiex/assets/60366769/aff12b22-5705-4be9-ba39-592336feca70)

# gr로 시작하고 중간글자가  e 또는 a 가 되고  y로 끝나는것을 찾음
![image](https://github.com/understanding963852/604_regiex/assets/60366769/9d54dcca-ffcd-4356-89f1-c43fc5a24122)

# 찾아는 지지만 그룹으로 만들고 싶지 않다면 사용   
![image](https://github.com/understanding963852/604_regiex/assets/60366769/b0330007-df73-4950-b376-e16bb13e9f91)


# gr로 시작하고 a또는 e 또는 d 가 있고 y로 끝남
# [aed]  --> 대괄호안에 있는 글자중 하나라도 만족하는것을 찾아라는 의미 
![image](https://github.com/understanding963852/604_regiex/assets/60366769/f9f241d8-8285-435f-a584-8692f7ff50f4)

![image](https://github.com/understanding963852/604_regiex/assets/60366769/2d28193c-416a-4f1b-a96f-8fc57b7e49d4)


# 아래 두 이미지는 gr로 시작하고 a~g사이의 글자중 하나라도 포함되고 y로 끝나는 것을 찾음
![image](https://github.com/understanding963852/604_regiex/assets/60366769/81b911a6-9879-4a3a-ae04-ed042aba73a9)

![image](https://github.com/understanding963852/604_regiex/assets/60366769/79687923-4c92-4c7d-b7ab-01f7ca06c3ab)

# a 부터 z까지, A 부터 Z까지 0부터 9까지 하나라도 만족하면 모두 찾는다
![image](https://github.com/understanding963852/604_regiex/assets/60366769/ae66b905-31e8-4e99-92f7-fed568a7c623)

![image](https://github.com/understanding963852/604_regiex/assets/60366769/7a6b0e0f-2e4e-4bb4-8693-1d5f94b356fa)

# ? :있거나 없거나 (많거나X)
![image](https://github.com/understanding963852/604_regiex/assets/60366769/f1f5fe3f-fec7-4aff-b53a-0c6ab1dcc129)

# * :있거나 없거나 많거나
![image](https://github.com/understanding963852/604_regiex/assets/60366769/b3313be5-ab40-4287-9136-b3f7e2227e32)

# + : 하나 또는 많거나(one or more)
![image](https://github.com/understanding963852/604_regiex/assets/60366769/26fa9597-3e6c-49c7-94e7-89b89c01470a)


# {n} : n번 반복

![image](https://github.com/understanding963852/604_regiex/assets/60366769/ee8b5521-2c00-4756-b3fd-fd71754b85b6)

# {min,} : 최소
![image](https://github.com/understanding963852/604_regiex/assets/60366769/2520e054-bd40-49cb-bc6e-9ace1325ead7)


# {min,max} : 최소 그리고 최대
![image](https://github.com/understanding963852/604_regiex/assets/60366769/b3ae102f-4b85-4f70-bddf-ed8282e0ce99)




   - \b  : 단어경계      
   - \B  : 단어경계가 아님
   - ^   : 문장의 시작
   - $   : 문장의 끝
