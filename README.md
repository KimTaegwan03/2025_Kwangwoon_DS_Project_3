# 2025_Kwangwoon_DS_Project_3

반드시 제안서에 표기되어 있는 **구현 스펙 및 감점 조건**을 확인하고 구현할 것, 이를 확인하지 않고 이의 신청 시 점수 부여 불가능

제안서에 명시되어 있는 내용에 대한 질문은 답변 없이 Close할 예정입니다. 꼭 제안서를 꼼꼼히 살펴보시기를 바랍니다.

---

## Update Notes  

---

## How to Clone Repository  

```bash
sudo apt-get install git   #1차 프로젝트에서 다운받았다면 입력하지 않아도 무방
git clone https://github.com/KimTaegwan03/2025_Kwangwoon_DS_Project_3.git
```

---

## How to check memory leak 
- make 이후 생성된 run 파일 실행 전에 valgrind 명령어를 입력하면 메모리 누수를 확인 가능
- 반드시 run 파일이 있는 디렉토리 내에서 수행해야 함. cd(change directory)로 변경하기
```bash
sudo apt-get update
sudo apt-get install valgrind  #1차 프로젝트에서 다운받았다면 입력하지 않아도 무방
valgrind ./run
```
- "All heap blocks were freed -- no leaks are possible" 메세지가 출력되어야 누수가 발생하지 않은 것, "LEAK SUMMARY"가 나온다면 누수가 발생
- **3차 프로젝트에서는 메모리 누수를 체크하여 누수가 발생한 경우 -10% 감점할 예정**
---

## 구현 고려사항

1. 제안서에 명시되어 있지 않은 예외 case는 고려하지 않아도 무방함 (너무 애매하다고 생각하면 Github Issue를 통해 질문해주세요.)
2. 모든 명령어에 대해서, 너무 많은 인자 혹은 적은 인자를 받는 경우엔 각 명령어에 맞는 Error Code 출력
3. 주석은 필수로 작성. Line by line 수준으로 디테일할 필요는 없음. 그러나 너무 미흡하다면 **감점 - 10%** (반복문, 조건문이 어떤 역할을 하는지 정도만 입력해도 괜찮습니다.)
4. 출력은 반드시 log.txt 파일을 생성해 출력해야 함. 지키지 않을 시 **감점 - 10%**
5. log.txt, command.txt, graph_L.txt, graph_M.txt 파일 모두 코드와 같은 디렉토리 내에서 존재해야 함. 이를 지키지 않아서 코드 실행이 안될 경우 **점수 부여 불가**
6. 프로그램 종료 시(EXIT 명령어 수행 시) 할당된 메모리를 모두 해제하여 메모리 누수가 발생하지 않도록 할 것. 누수 발생 시 **감점 -10%**
