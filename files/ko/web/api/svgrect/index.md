---
title: SVGRect
slug: Web/API/SVGRect
page-type: web-api-interface
tags:
  - API
  - Reference
  - SVG
  - SVG DOM
browser-compat: api.SVGRect
translation_of: Web/API/SVGRect
---
{{APIRef("SVG")}}

**`SVGRect`** 인터페이스는 직사각형을 나타냅니다. 직사각형은 최소 `x` 값과 최소 `y` 값을 가리키는 좌표쌍, 그리고 양수인 `width`와 `height` 값으로 구성됩니다.

**`SVGRect`** 객체는 읽기 전용으로 지정될 수 있습니다. 읽기 전용일 경우 객체를 수정하려고 시도하면 예외가 발생합니다.

## 속성

- {{domxref("SVGRect.x")}}
  - : 이 좌표의 정확한 효과는 요소에 따라 다릅니다. `x` 특성을 지정하지 않은 경우 `0`을 지정한 것과 동일하게 취급합니다.
- {{domxref("SVGRect.y")}}
  - : 이 좌표의 정확한 효과는 요소에 따라 다릅니다. `y` 특성을 지정하지 않은 경우 `0`을 지정한 것과 동일하게 취급합니다.
- {{domxref("SVGRect.width")}}
  - : 직사각형의 너비를 나타냅니다. 음수로 설정하려고 시도하면 오류가 발생합니다. `0`일 경우 요소를 렌더링하지 않습니다.
- {{SVGAttr("SVGRect.height")}}
  - : 직사각형의 높이를 나타냅니다. 음수로 설정하려고 시도하면 오류가 발생합니다. `0`일 경우 요소를 렌더링하지 않습니다.

## 메서드

없음.

## 명세

{{Specifications}}

## 브라우저 호환성

{{Compat}}
