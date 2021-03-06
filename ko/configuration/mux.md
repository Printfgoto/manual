---
refcn: chapter_02/mux
refen: configuration/mux
---
# 멀티플렉싱

멀티플렉싱 또는 멀티플렉싱은 다중 가상 TCP 연결에 하나의 물리적 TCP 연결을 사용하는 것입니다.

Mux는 TCP 핸드 셰이크 대기 시간을 줄 이도록 설계되었습니다. 그것은 높은 처리량을위한 것이 아닙니다. 대용량 파일을 다운로드하거나 속도 측정에 사용할 때 Mux는 일반적으로 일반 TCP 연결보다 느립니다.

## MuxObject

```javascript
{
  "enabled": false,
  "concurrency": 8
}
```

> `활성화 됨`: true | 그릇된

아웃 바운드에서 Mux를 사용할지 여부.

> `동시성`: 숫자

한 번에 하나의 물리적 연결이 처리 할 수있는 다중화 된 연결의 최대 수입니다. 최대 값 `1024`, 최소값 `1`, 기본값 `8`.