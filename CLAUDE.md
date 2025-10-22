# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 프로젝트 개요

Dave Lee의 개인 소개 웹사이트입니다. 단일 `index.html` 파일로 구성되어 있으며, mycareer.md 파일의 정보를 기반으로 제작되었습니다.

## 아키텍처

**단일 파일 구조:**
- HTML 구조는 프로필 헤더, 커리어, 학력, 전문 분야, 연락처 섹션으로 구성됩니다
- CSS는 `<style>` 태그에 포함되어 있으며 Apple 디자인 스타일을 따릅니다
- JavaScript는 `<script>` 태그에 포함되어 있으며 애니메이션과 인터랙션을 관리합니다

**주요 섹션:**
- `.profile-header`: 이름과 직책을 표시하는 헤더 (index.html:254-258)
- `.section`: 커리어, 학력, 전문 분야, 연락처 등의 정보 섹션 (index.html:260-297)
- 각 섹션은 순차적인 fade-in 애니메이션을 가집니다

**인터랙션:**
- `IntersectionObserver`: 스크롤 시 섹션이 보일 때 애니메이션 트리거
- 스킬 태그 클릭 시 펄스 효과
- 호버 시 카드 상승 효과

## 데이터 소스

개인 정보는 `mycareer.md` 파일을 참조합니다:
- 이름: Dave Lee
- 주요 커리어: 개발 20년, 기획 5년
- 출신학교: ㅇㅇ대학교

## 실행 방법

`index.html` 파일을 웹 브라우저에서 직접 열면 됩니다. 빌드 프로세스나 서버가 필요하지 않습니다.

## 수정 시 주의사항

개인 정보 수정 시:
- `mycareer.md` 파일을 먼저 업데이트한 후 `index.html`에 반영합니다
- 커리어 정보는 `.career-item` 섹션에서 수정합니다 (index.html:262-269)
- 학력 정보는 학력 섹션에서 수정합니다 (index.html:272-278)

디자인 수정 시:
- Apple 디자인 가이드라인을 따릅니다
- 주요 색상: 배경(#f5f5f7), 강조색(#667eea, #764ba2), 텍스트(#1d1d1f), 보조텍스트(#86868b)
- San Francisco 폰트 스타일을 위해 `-apple-system` 폰트 스택 사용
- 모바일 반응형 브레이크포인트는 600px입니다
- 모든 스타일은 단일 HTML 파일 내에서 관리됩니다
