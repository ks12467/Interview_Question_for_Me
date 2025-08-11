# 프로그래밍 용어 정리

* [PCB(Process Control Block)](#pcb)
* [TCB(Thread Control Block)](#tcb)
* [TLB(Translation Lookaside Buffer)](#tlb)
* [I/O(Input/Output)](#io)
* [IPC 기법](#ipc-기법)
* [인터럽트](#인터럽트)



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