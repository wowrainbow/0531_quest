# AIFFEL Campus Data Scientist Peer Review Templete
- 코더 : 남태욱
- 리뷰어 : 김학준


# PRT(Peer Review Template)
[ ]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
- 문제에서 요구하는 기능이 정상적으로 작동하는지?
    - 메인 코드 및 클래스를 완성하지 못하여서 실행까지는 하지 못했습니다.
    - 함수들은 self. 부분이 빠진 부분이 몇 있어서 아마 실행을 해도 정상적으로 작동은 하지 않을 것 같습니다.
    
[ ]  **2. 핵심적이거나 복잡하고 이해하기 어려운 부분에 작성된 설명을 보고 해당 코드가 잘 이해되었나요?**
- 해당 코드 블럭에 doc string/annotation/markdown이 달려 있는지 확인
- 해당 코드가 무슨 기능을 하는지, 왜 그렇게 짜여진건지, 작동 메커니즘이 뭔지 기술.
- 주석을 보고 코드 이해가 잘 되었는지 확인
    - 넵 해당 메서드들이 어떠한 기능을 구현을 하려는 지는 바로 알았습니다.
        
[ ]  **3. 에러가 난 부분을 디버깅하여 “문제를 해결한 기록”을 남겼나요? 또는 “새로운 시도 및 추가 실험”을 해봤나요?**
- 문제 원인 및 해결 과정을 잘 기록하였는지 확인
- 문제에서 요구하는 조건에 더해 추가적으로 수행한 나만의 시도, 실험이 기록되어 있는지 확인
    - 메인 코드 및 클래스를 완성하지 못하여서 추가적은 부분은 없었습니다.

        
[ ]  **4. 회고를 잘 작성했나요?**
- 프로젝트 결과물에 대해 배운점과 아쉬운점, 느낀점 등이 상세히 기록 되어 있나요?
	- np 와 random을 같이 이용하여 계좌번호를 만드는 것을 새로 배웠습니다.
 	- 클래스가 많이 어려워서 고전하는 모습이 많이 보였습니다. 그러나 열심히 하려는 모습이 좋습니다!
	- 시간만 많이 있었으면 그래도 완성을 됐을 것 같습니다 파이팅입니다!   


# 참고 링크 및 코드 개선
```
def __init__(self, name, balance):
        self.name = name # 예금주
        self.balance = 0 # 잔액
        self.deposit_count = 0
        self.bankname = "SC은행"
        self.d_history_list = []
        self.w_history_list = []

에서 bankname 은 클래스 변수로 선언해도 괜찮을 것 같아요!

def withdraw(self, wd): #wd는 출금 금액
    #잔고 이상으로 출금 불가능
        wd = int(input("출금금액: "))
        if wd <= balance:
            amount = self.balance - wd
            print(f"출금완료: {wd}원")
            print(f"현재 잔액: {amount}원")
        else:
            print("잔액부족")

        self.w_history_list.append((datetime.datime.now(), wd))

에서 매개변수로 wd를 받고 있는데 wd = int(input("") 으로 변수를 다시 선언했습니다.
이렇게 하면 매개변수 wd가 아무런 의미가 없어지기 때문에 함수에서 wd = int(input("")을 빼거나 매개변수 wd를 빼는 것을 추천드립니다.

중간중간에 self. 넣는 것 꼭 잊지마세요!

```
