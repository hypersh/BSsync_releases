# BS Sync

실행 전에 변경 내용을 확인할 수 있는 Windows 폴더 동기화 앱입니다. **개인과 기업 모두 무료로 사용할 수 있습니다.**

## 다운로드

**[BS Sync 3.1.0 다운로드 — Windows x64](https://github.com/hypersh/BSsync_releases/releases/download/v3.1.0/BS_Sync310.exe)**

[SHA-256 체크섬](https://github.com/hypersh/BSsync_releases/releases/download/v3.1.0/BS_Sync310.exe.sha256) · [최신 릴리스](https://github.com/hypersh/BSsync_releases/releases/latest) · [공식 웹사이트](https://tools.bsbiotec.com/ko/bs-sync.php)

설치파일: `BS_Sync310.exe` · 17,066,108바이트 · Windows 11 x64에서 검증 · 한국어·영어 지원

[English](README.md) · 한국어

## 세 단계로 시작하기

1. **설치하고 언어를 선택합니다.** **BS Sync 3**를 열고 오른쪽 위에서 **한국어** 또는 **English**를 선택합니다.
2. **A/B 폴더와 모드를 정합니다.** 양쪽 변경을 반영하려면 **동기화**, 한쪽을 기준으로 맞추려면 **복사**와 방향을 선택합니다.
3. **분석하고 확인한 뒤 실행합니다.** 필요한 항목에서 **A 사용**, **B 사용**, **양쪽 삭제**, **보류**를 선택합니다. 삭제 예정 항목을 확인한 뒤 **동기화 실행** 또는 **복사 실행**을 누릅니다.

처음에는 작은 시험 폴더로 사용해 보세요. 선택의 의미, 복구 위치, 다운로드 확인 방법은 [시작 안내](docs/QUICK_START.ko.md)에 있습니다.

## 모드 선택

| 앱의 모드 | 동작 |
|---|---|
| **동기화** | 확인된 변경과 삭제 이력을 양쪽에 반영합니다. 독립적인 양쪽 변경이 충돌하면 사용자 선택을 기다리며, 수정시각만으로 최신 파일을 고르지 않습니다. |
| **복사 (Mirror)** | A → B 또는 B → A의 기준 폴더와 같게 맞춥니다. **대상에만 있는 파일·폴더는 삭제합니다.** 제외 항목은 보호합니다. |

복사 내용을 검증하고 미완료 작업의 복구 기록을 남깁니다. 동기화는 이전본을 보관하며, 복사는 보관 여부를 선택할 수 있습니다. 3.1.0에는 한국어·영어 전환, 선택·복구 오류 수정, 반복 분석과 작은 파일 복사 개선이 포함되어 있습니다.

## 설치파일 서명 안내

현재 설치파일에는 **디지털 서명이 없습니다.** Windows에서는 `NotSigned`로 표시되며 경고가 나타날 수 있습니다. 위 공식 경로에서 내려받고 [SHA-256을 확인](docs/QUICK_START.ko.md#다운로드-확인)하세요. 체크섬 일치는 다운로드한 파일을 확인하는 수단이며 게시자 서명을 대신하지 않습니다. 조직의 보안 정책을 따르고, 설치를 위해 Windows 보호 기능을 끄지 마세요.

## 도움말과 프로젝트 정보

- [시작 안내·FAQ](docs/QUICK_START.ko.md) · [English Quick Start](docs/QUICK_START.md)
- [오류 제보](https://github.com/hypersh/BSsync_releases/issues/new?template=bug_report.yml) — 한국어·영어 모두 가능하며 첨부파일은 선택 사항입니다.
- [한국어 웹사이트](https://tools.bsbiotec.com/ko/bs-sync.php) · [English website](https://tools.bsbiotec.com/bs-sync.php)

이 저장소는 설치파일과 사용자 문서를 제공합니다. BS Sync는 오픈소스가 아니며 앱 소스는 비공개입니다. 개인·기업 모두 무료로 사용할 수 있습니다.
