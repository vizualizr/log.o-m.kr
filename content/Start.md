---
publish: true
aliases:
  - index
created: 2026-08-08T03:56:19.459Z
modified: 2026-09-08T02:57:24.153Z
---

<a href="https://wakatime.com"><img src="https://wakatime.com/share/@2c977ef5-79a6-45cc-94ed-1ba3005f66dd/256047fa-271f-43f9-b70f-705b6972140f.png" /></a>

[studio.o-m.kr](http://studio.o-m.kr)  documents the process of developing an independent data storytelling blog from scratch.

## Updates

- [[Untitled.md|Untitled]]
- [[backoffice/draft/logseq.md|logseq]]
- [[Journal/2026-09-08.md|2026-09-08]]
- [[Design system/icon.md|icon]]
- [[Journal/2026-09-07.md|2026-09-07]]
- [[Design system/logo/logo.md|logo]]
- [[backoffice/GeminiHelper/chat_1788411429294_qbe3jl2.md|chat_1788411429294_qbe3jl2]]
- [[Journal/2026-09-01.md|2026-09-01]]
- [[Journal/2026-08-29.md|2026-08-29]]
- [[Quartz/quartz/plugins.md|plugins]]

## To-dos

- 추가 작업이 필요하다. [[journal/2026-08-20]]
  - `content` 폴더 이동
  - freefilesync에서 작성한 배치 파일 설정 변경 후 bib 파일 동기화 위치 확인.
  - 이것도 심볼릭 링크로 해야 하나?
- 폴더 클릭했을 때 하위 문서 및 폴더 자동 리스팅. [[Journal/2026-08-19|2026-08-19]]에 추가함
  - 폴더 이름이 `.`을 포함하면 해당 폴더를 클릭했을 때 404 페이지를 반환한다.
- Footer를 변경하고 싶은데 이걸 하려면 꼭 새 컴포넌트를 만들어야 하는 건지 확신이 없다. 꽤 복잡하고 번거로운데 굳이 그럴 필요가 있을까? [컴포넌트 만드는 법](https://quartz.jzhao.xyz/advanced/making-plugins#installing-your-plugin)이 솔직히 너무 복잡하다. 이건 AI한테 물어서 처리하는 게 더 나을 것 같다. [[Journal/2026-08-19|2026-08-19]]에 추가함
- 커스텀 색상인데 지금은 적용이 안 됨. 어떻게 하는 건지 모르겠음. `yaml light: "#edece8" lightgray: "#dfded7" gray: "#c2c5b9" darkgray: "#555555" dark: "#000002" secondary: "#004b73" tertiary: "#434f63" highlight: "rgba(0, 75, 115, 0.15)" textHighlight: "#9ed6ed88" `
- 프리텐다드, IBM Plex Sans KR 등으로 긴 글을 읽을 때 피로도가 걱정된다면 다음과 같이 조정하라. - 기본적으로 두 글꼴은 가독성에 초점을 둔 폰트이다. 또한 장평 조절을 위한 글자너비 축(`wdth`)를 지원하지 않는다. 단 글자 굵기 축(`wght`)만 지원한다. - 따라서 장평을 조정하기 보다는 줄간격과 자간으로 가독성을 올리는 편이 더 낫다. - 단 아래 적용 후 반드시 테스트를 거쳐 확정하라.  `css /* 줄간격 넉넉히 주기:** 본문 폰트 크기의 1.6~1.75배로 설정 */ line-height: 1.65;  /* **미세한 자간 줄임:** 한글 웹폰트는 자간을 아주 살짝 줄여주면 눈이 글자 뭉치를 더 쉽게 인지합니다. */ letter-spacing: -0.01em; /* 또는 -0.02em */ `
