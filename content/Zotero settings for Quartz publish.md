---
publish: true
created: 2026-08-17T07:58:45.203Z
modified: 2026-09-08T02:57:24.083Z
---

## Summary

-

## Steps

1. ZotLit installed.
2. check the pipeline with [[Quartz/Quartz]]
   1. [quartz plugin - Citations](https://quartz.jzhao.xyz/plugins/citations)

## Troubleshooting

- 저널에서 해당 저널을 참조하는 문서들의 백링크를 표시하려면 날짜를 아래와 같이 템플릿에 삽입하면 된다.

  ```text
  아래처럼 쓰면 원하는 저널 폴더에 있는 오늘 날짜 문서를 참조하는 링크를 생성한다.
  [[journal/{{date}} | {{date}}]]
  ```

## Log

- 2026-08-17 Page created.
  - installed [zotlit](https://community.obsidian.md/plugins/zotlit) and link zotero successfull
- [[Journal/2026-08-19|2026-08-19]] citation 플러그인 활성화 완료.
  - 일단 citation 플러인을 활성화시키기는 했는데 설정이 꼬였는지 옵시디안 저장소를 기준으로 하는 상대경로가 아니라 .git 폴더를 기준으로 하는 상대 경로로 `.bib` 파일을 찾는 거 같다.
  - 문제가 확실해지면 [깃허브에 이슈](https://github.com/jackyzha0/quartz/issues) 등록해라.

### References

- [ZotLit homepage](https://zotlit.aidenlx.site/)
- [The definitive guide to academic writing with Obsidian and Pandoc](https://paul-stewens.com/blog/2026/academic-writing-obsidian-pandoc/)
- [Citations](https://quartz.jzhao.xyz/plugins/citations) plugin page and [its github repo](https://github.com/quartz-community/citations)
