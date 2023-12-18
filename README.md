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



# 괄호 안의 글자 중 하나라도 포함되는 것 찾을때
- ![image](https://github.com/yeon2716/Regiex/assets/145514579/9a631109-a5a3-4078-8535-3f2a2d211e9c)
![image](https://github.com/yeon2716/Regiex/assets/145514579/c9864318-442f-42dd-a4c2-47502a26c967)


a 부터 g 까지 하나라도 포함되는 것
![image](https://github.com/yeon2716/Regiex/assets/145514579/9eb3723d-5218-4b46-8e24-9c014cd47550)
![image](https://github.com/yeon2716/Regiex/assets/145514579/a9aa6a71-4033-4552-b342-566cf39fbc50)


 
