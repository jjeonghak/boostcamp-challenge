# Day 04

## Allocation of Physical Memory  
* 메모리는 OS 상주영역과 사용자 프로세스 영역으로 나누어 사용  

* 사용자 프로세스 영역 할당 방법  

1. Contiguous allocation(연속 할당)  
2. Noncontiguous allocation(불연속 할당)  

<br>

## Contiguous Allocation
* 각각의 프로세스가 메모리의 `연속적인 공간`에 적재  

* `External fragmentation`(외부조각)  
  * 프로그램 크기보다 분할 크기가 작은 경우  
  * 아무 프로그램에도 배정되지 않은 빈 곳이지만 프로그램이 올라갈 수 없는 작은 분할  

* `Internal fragmentation`(내부조각)  
  * 프로그램 크기보다 분할의 크기가 큰 경우  
  * 하나의 분할 내부에서 발생하는 사용되지 않는 메모리 조각  
  * 특정 프로그램에 배정되었지만 사용되지 않는 공간  

* `Hole`  
  * 가용 메모리 공간  
  * 프로세스가 도착하면 수용가능한 hole을 할당  
  * 다양한 크기의 hole들이 메모리 여러 곳에 흩어져 존재  

<br>

## 메모리 분할

1. Fixed partition allocation(고정분할)  
    * 물리적 메모리를 영구적 분할로 나눔  
    * 분할당 하나의 프로그램 적재  
    * 융통성 없음  
    * 외부조각, 내부조각 발생  

2. Variable partition allocation(가변분할)  
    * 프로그램 크기를 고려해서 할당  
    * 분할 크기, 개수가 동적으로 변경  
    * 외부조각 발생  

<br>
