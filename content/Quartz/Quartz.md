---
publish: true
aliases:
  - 쿼츠
  - quartz
created: 2026-08-17T11:47:51.847Z
modified: 2026-09-08T02:57:24.179Z
---

## Summary

### workflow

- 로컬(로그식 그래프 폴더)에서 아래와 같이 작성한다. [[logseq|로그식으로 이미 테스트를 했지만 문제가 있어]] 옵시디언으로 선택했다.
  - ubuntu@oci
    - 우분투가 파일 변경 감지
    - quartz가 자동으로 정적 html 파일로 빌드
    - 빌드 완료하면 git이 자동으로 git commit한 뒤 깃허브로 push
    - 깃허브에서 GitHub Actions가 빌드 후 github page로 배포
  - 트리거
    - 로컬에서 rsync 실행하면
    - 호스트(p1@windows 11)에서 리모트로 로그식 그래프 폴더 전송

### configurations

1. 로컬에서 우선 테스트하고 가능하면 OCI에서는 도커로 설치하자.
   1. 로컬 환경
      1. 윈도우
      2. Quartz 설치 [[Journal/2026-08-18]]
         1. Quartz 기본 플러그인 설치는 자동으로 해 준다. 마찬가지로 완료.
         2. [Quartz syncer](https://saberzero1.github.io/quartz-syncer-docs/setup-guide) 설치 (이건 옵시디안 플러그인이다)
      3. Quartz로 옵시디안 폴더 변환 후 아래를 확인한다.
         1. backlink 게시 여부
         2. 폴더 클릭했을 때 하위 문서 및 폴더 자동 리스팅. [[Journal/2026-08-19|2026-08-19]]에 추가함
            1. 폴더 이름이 `.`을 포함하면 해당 폴더를 클릭했을 때 404 페이지를 반환한다.
         3. Footer를 변경하고 싶은데 이걸 하려면 꼭 새 컴포넌트를 만들어야 하는 건지 확신이 없다. 꽤 복잡하고 번거로운데 굳이 그럴 필요가 있을까? [컴포넌트 만드는 법](https://quartz.jzhao.xyz/advanced/making-plugins#installing-your-plugin)이 솔직히 너무 복잡하다. 이건 AI한테 물어서 처리하는 게 더 나을 것 같다. [[Journal/2026-08-19|2026-08-19]]에 추가함

#### Build Options

아래 명령어로 테스트할 수 있다.

```bash
npx quartz build --serve --watch
```

자세한 문서는 [build options](https://quartz.jzhao.xyz/cli/build)를 참고하라.

##### Explicit publish

- [ExplicitPublish](https://quartz.jzhao.xyz/plugins/explicitpublish)
- `publish:`라는 페이지 속성이 `true`인 문서만 게시하도록 한다. [[Journal/2026-08-21|2026-08-21]]에 수정.

```yaml
- source: "@quartz-community/explicit-publish"
  enabled: true
```

##### citation

1. Zotero citation key 게시 여부 /link 확인
2. \[@shoemakerSystemsProgrammingModel2026]

## Steps

1. Installation
   ```bash
   git clone https://github.com/jackyzha0/quartz.git

   # 2. 다운로드된 quartz 폴더로 이동
   cd quartz

   # 3. 필요한 패키지(의존성) 설치 (시간이 조금 걸릴 수 있습니다)
   npm i

   # 4. Quartz 초기화 스크립트 실행
   npx quartz create
   ```

## Troubleshooting

#### 폴더 및 파일을 숨기고 싶을 때

- 폴더 및 파일을 게시하지 않으려면 다음을 확인하라.
  - [Private Pages](https://quartz.jzhao.xyz/features/private-pages)
- 커스텀 색상인데 지금은 적용이 안 됨. 어떻게 하는 건지 모르겠음.
  ```yaml
  light: "#edece8"
  lightgray: "#dfded7"
  gray: "#c2c5b9"
  darkgray: "#555555"
  dark: "#000002"
  secondary: "#004b73"
  tertiary: "#434f63"
  highlight: "rgba(0, 75, 115, 0.15)"
  textHighlight: "#9ed6ed88"
  ```

폴더를 클릭했을 때 404 페이지가 뜨는 문제
[[Quartz/content 폴더를 옵시디언 저장소로 쓰는 방법]]

### plugins

[[Quartz/quartz/plugins|quartz plugins]]을 보라

## Log

- [[journal/2026-05-30|2026-05-30]] Page created.
- [[Journal/2026-08-18]] 설치 완료함. 로컬에서 테스트 가능

### References

- [Abridged list of Quartz community plughins](https://github.com/quartz-community/awesome-quartz)
