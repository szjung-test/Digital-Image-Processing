# DIP Terminology

- 모든 좌표 유한 0-255
- 모든 단위 픽셀(pixel)

### 디지털 영상 처리 범위
- Low-level Processing : 입력=출력=영상 영상 내 노이즈 감쇠, 대비증가, 영상 샤프닝
- Mid-level Processing : 입력=영상, 출력 = 특징(Feature;edge, contour, identity of objects)
- High-level Processing : 객체에 대한 "인지(recongnition)" 가능한 처리 과정

### 1. 디지털 영상의 공식화
- Image plane = 그대로 X -> "양자화(quantization)" 통해 영상 이산적 get
- DIP = (x,y) 대해서 0 ≤ (f(x,y)) < ∞
- f(x,y) 반사된 광원과 오리지널 광원 동시에 영향 받음
- γ(x,y), i(x,y) 정의
- f(x,y) = γ(x,y) * i(x,y)
- 0 ≤ i(x,y) < ∞ , 0 ≤ γ(x,y) ≤ 1 
- if γ(x,y) = 0 이면 물체가 완전히 광원을 흡수하여 반사하는 빛이 없다.
- γ(x,y) = 1 이면 물체가 완전히 광원반사

### 2. 영상샘플링과 양자화
- 영상 디지털 형태 변환 과정 2가지
 1. 샘플링(Sampling)
 2. 양자화(quantization)
 3. 픽셀간 관계성  
    - 가장 간단한 관계 = 임의의 (x,y) 좌표 대응되는 값
    - 대각선 이웃들만 고려하는 방법도 있음 

- 1) 인접성(adjacency)
    - 집합 v 밝기값의 집합 정리 
    - 바이너리 영상이라고 가정하면 가능한 밝기값 0 or 1
    - 4-인접성
    - 8-인접성
    - m-인접성

- 2) 디지털경로(Digital path)
    - 시작 픽셀(x, y) = (x,y), 목적픽셀 (s,t) = (xn, yn)

- 3) 연결성(Connectiveness)
    - 집합 S 영상 픽셀의 부분 집합이라고 정의, S안의 픽셀 p,q 사이에 경로 존재한다면 두 픽셀에는 연결성(connected) 존재 정의
    집합T 묶어서 집합T 연결 집합(connected set) 정의

- 4) 영역(region)
    - 집합 R 영상의 부분 집합
- 5) 거리 측정
    - 두 개의 픽셀 사이의 거리(distance) 측정하는 방법
    - "거리"라고 부르기 위해선 3가지 조건 만족해야함
    