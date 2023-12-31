# Image Optimization

## 이미지 최적화 기본

- 반드시 이미지는 최적화 과정을 거쳐야 한다.  
  (로딩 속도 개선이 눈에 띄게 향상된다.)
- 아이콘 이미지 10개보다 아이콘을 모아둔 이미지 1개의 용량이 작다.
- 이미지 용량 뿐만 아니라, 이미지 파일을 주고받는 횟수도 줄여주는 것이 중요하다.  
  ==> 이미지 스프라이트(Image Sprite) 기법
- cf. base64, svg 등

## 이미지 스프라이트 기법

- 이미지 용량도 줄이고 이미지 갯수도 줄여 사이트를 가볍게 한다.
- `background-position`, `background-size` 등을 이용한다.
- 이미지가 수정되면 스프라이트 파일 수정 및 position 계산을 다시 해야 한다.
- tip: [mask](https://developer.mozilla.org/ko/docs/Web/CSS/mask): 이미지 클리핑 마스크

### 이미지 파일 작업

- 이미지 고해상도 대응, 위치 등을 고려해야 하므로 개발자가 직접 스프라이트 이미지 파일을 만드는 것이 좋다.
- 비트맵 기반의 파일만 가능하다.
- 반투명한 이미지는 불투명하게 만들어서 작업한 후 CSS 로 투명 처리한다.
- 이미지의 width 사이즈는 각자 다른 경우가 많으므로 가로보다는 세로로 이미지를 나열하는 것이 좋다.
- 각 이미지는 5px 이상 간격을 둔다.  
  이때 각 이미지 영역의 크기를 똑같이 만들어야 하므로, 가장 큰 이미지를 기준으로 간격을 설정한다.
- 각 이미지는 좌상단 등 특정 위치에 맞추거나, 교차축 기준 중앙 정렬 한다.
- 고해상도 대응 : 4배수까지(아이콘), 이미지는 2배수까지
