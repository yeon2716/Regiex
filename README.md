# Regiex (정규 표현식)

# /regiex/ ==> Regular expression 의 약자

# 언제 사용하는가?
 - 텍스트에서 우리가 원하는 특정한 패턴을 찾을 때 (전화번호형태의 패턴, 웹사이트 주소형태의 패턴, 이메일형식의 패턴을 찾을때 등등)
 - 사용자가 입력한 텍스트가 이메일이나 패스워드와 같이 특정한 패턴에 부합하는지 유효성검사를 할때도 사용할 수 있다
 - 정규식은 문자를 검사하고자할 때 사용하는 식이다.

# 정규식은 /로 시작하여 "나는 정규표현식"임을 나타낸다
 - ex :  /우리가 찾고자하는 패턴/

 - /regex/i
 - i는 어떤 옵션에 따라 검색할건지 플래그를 활용할 수 있다.

# 문법
 1) Groups anf ranges
 -  | : 또는
 - ![image](https://github.com/yeon2716/Regiex/assets/145514579/69721c2e-7c11-4a73-bdfa-096722236532)

 - () : 그룹
 - ![image](https://github.com/yeon2716/Regiex/assets/145514579/862fc347-1358-47a2-bcff-036f41437e6b)


    Expression은 그룹 첫번째에서, the는 그룹 두번째에서 찾아짐
   
 - [] : 문자셋, 괄호안의 어떤 문자든
 - [^] : 부정 문자셋, 괄호안의 어떤 문자가 아닐때
 - (?:) : 찾지만 기억하지는 않음

 # gr로 시작하고 중간글자가 e 또는 a 가 되고 y로 끝나는 것을 찾음
 #[aed]  --> 대괄호 안의 글자중 하나라도 만족하는 것을 찾아라
 /gr(e|a)y/gm

 # 찾아는 지지만 그룹으로 만들고 싶지 않을때 사용
 /gr(?:e|a)y/gm 

 기능이 있는 특수문자는 \를 넣고  기능이 없는 특수문자는 넣지않음  : ? #    그냥 무조건 넣어봐라



# 괄호 안의 글자 중 하나라도 포함되는 것 찾을때
- ![image](https://github.com/yeon2716/Regiex/assets/145514579/9a631109-a5a3-4078-8535-3f2a2d211e9c)
![image](https://github.com/yeon2716/Regiex/assets/145514579/c9864318-442f-42dd-a4c2-47502a26c967)


a 부터 g 까지 하나라도 포함되는 것
![image](https://github.com/yeon2716/Regiex/assets/145514579/9eb3723d-5218-4b46-8e24-9c014cd47550)
![image](https://github.com/yeon2716/Regiex/assets/145514579/a9aa6a71-4033-4552-b342-566cf39fbc50)


 
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


# - $   : 문장의 끝   --> /Ya$/ 문장의 끝인 ya
![image](https://github.com/yeon2716/Regiex/assets/145514579/7fbe04a9-a75a-4fb4-9700-77d332e77618)


# . : 어떤 글자 (줄바꿈 문자 제외)
# /./ 모든 문자

![image](https://github.com/yeon2716/Regiex/assets/145514579/f74fc44e-fb8c-4296-a4a1-1fbeda953a20)


# /\/  특수문자  --> 특수문자 .를 찾고자할때 
![image](https://github.com/yeon2716/Regiex/assets/145514579/d1274c43-1137-482a-bb72-61b052d28674)



   - \b  : 단어경계      
   - \B  : 단어경계가 아님
   - ^   : 문장의 시작



  
