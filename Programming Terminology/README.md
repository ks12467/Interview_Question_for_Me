# 프로그래밍 용어 정리

## CTRL + F를 사용해서 찾는걸 권장드립니다.


* [프로세스](#프로세스)
* [스레드](#스레드)
* [PCB(Process Control Block)](#pcb)
* [TCB(Thread Control Block)](#tcb)
* [TLB(Translation Lookaside Buffer)](#tlb)
* [I/O(Input/Output)](#io)
* [IPC 기법](#ipc-기법)
* [인터럽트](#인터럽트)
* [Race Condition](#race-condition)

---
## 프로세스
실행 중인 프로그램의 독립적인 실행 단위

독립된 메모리 공간을 보유함.<br>
다른 프로세스와 메모리 공유 안함 <br>
생성. 전환이 느리지만 안정성이 높음 <br>
OS가 [PCB](#pcb)로 상태 관리

---
## 스레드
프로세스 내부에서 실행되는 흐름 단위

같은 프로세스의 Code, Data, Heap 공유 / Stack은 개별적<br>
생성과 전환이 빠르고 통신이 쉬움<br>
동기화 필요 (Race Condition 가능성이 있음)<br>
OS가 [TCB](#tcb)로 상태 관리

---
## PCB
PCB = Process Control Block의 약자로 프로세스의 모든 상태 정보를 담고 있는 자료 구조


포함 내용
* PID (Process ID, 고유 식별자)
* 프로세스 상태
* 프로그램 카운터
* CPU 레지스터 값
* 메모리 정보 (Code/Data/Stack 세그먼트)
* 입출력 상태, 열린 파일 정보 등

프로세스 하나당 PCB 하나 존재

---
## TCB
TCB = Thread Control Block의 약자로 스레드의 실행 상태를 담고 있는 자료구조

포함 내용
* TID (Thread ID, 고유 식별자)
* 스레드 상태
* 프로그램 카운터
* CPU 레지스터 값
* 스레드 스택 정보
* 스레드 우선순위

스레드는 프로세스 자원을 공유하므로, TCB는 스레드 고유 정보만 따로 가짐

스레드 하나당 TCB 하나 존재

---
## TLB
TLB = Translation Lookaside Buffer의 약자로 CPU 안에 있는 아주 빠른 캐시로, 가상 메모리 주소를 실제 물리 메모리 주소로 바꿀 때 속도를 높여주는 장치.

자주 쓰는 일부를 미리 저장해두는 초고속 메모리

---
## I/O
Input/Output의 줄임말

---
## IPC 기법
Inter-Process Communication 즉 프로세스 간 통신을 말한다.

운영 체제에서 독립된 프로세스들이 데이터를 주고받거나 작업을 동기화하기 위해 사용하는 방법.

---
## 인터럽트
Interrupt란? CPU가 하던 일을 잠시 멈추고, 다른 중요한 일을 먼저 처리하게 하는 신호

즉, 예외 상황이나 이벤트가 발생했음을 CPU에 알리는 메커니즘

---
## Race Condition
Race Condition 경쟁 상태란 둘 이상의 프로세스나 스레드가 동시에 같은 자원에 접근해서, 실행 순서에 따라 결과가 달라지는 상황을 말합니다.

---
## 프로세스 동기화
여러 프로세스 또는 스레드가 공유 자원에 접근할 때, 데이터의 일관성과 정확성을 보장하도록 실행 순서를 제어하는 것