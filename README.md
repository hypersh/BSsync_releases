# BS Sync Releases

BS Sync의 Windows 설치파일과 체크섬을 제공하는 공개 다운로드 저장소입니다. 애플리케이션 소스는 비공개 저장소에서 관리합니다.

## BS Sync 3.0.1 다운로드

- [최신 Release](https://github.com/hypersh/BSsync_releases/releases/latest)
- [3.0.1 설치파일 — BS_Sync301.exe](https://github.com/hypersh/BSsync_releases/releases/download/v3.0.1/BS_Sync301.exe)
- [SHA-256 체크섬](https://github.com/hypersh/BSsync_releases/releases/download/v3.0.1/BS_Sync301.exe.sha256)
- [변경 사항과 검증 범위](https://github.com/hypersh/BSsync_releases/releases/tag/v3.0.1)

앱과 바로가기 이름은 **BS Sync 301**입니다. 2026-10-22 최종 개선본을 2026-11-10에 검증하여 게시했으며, 원본 설치파일을 유지했습니다.

## 주요 기능

- A/B 방향 복사와 파일별 변경 이력을 사용하는 동기화.
- 독립된 양쪽 변경에 대한 사용자 선택과 실행 전 변경 확인.
- 문제 항목의 상태·이유·권장 조치 표시 및 전체 결과 CSV·JSON 저장.
- 하위 경로와 내용이 정확히 대응하는 폴더의 전체 이름 변경.
- 최초 파일·변경 후보 중심의 기본 분석과 선택 가능한 정밀 검사.

## 설치와 첫 분석

3.0.1은 전용 설치 경로와 `_BS_Sync_Data_v3` 기록을 사용하는 독립 앱입니다. 구버전 기록을 자동 이관하지 않습니다. v3 기록이 없으면 선택한 A/B 폴더의 현재 파일로 새 기록을 만듭니다.

첫 동기화에서는 과거 삭제 여부를 알 수 없으므로 한쪽에만 있는 파일을 다른 쪽에 복사합니다. 복사 모드는 지정한 기준 방향을 따르며 대상에만 있는 파일을 삭제합니다. 실행 전 계획과 삭제 범위를 확인하세요. 기존 v3 기록·미완료 복구 기록을 유지하고, 구버전 기록·이전본은 제외 대상으로 보존합니다.

## 검증

2026-11-10 노트북 전체 unittest에서 299개 중 298개 통과, 1개 건너뜀(심볼릭 링크 생성 권한), 실패·오류 없음. 원본 소스 manifest 75개 파일과 설치파일의 SHA-256을 확인했습니다.

2026-10-22 Windows 빌드와 패키지 자체 실행 성공 기록을 보존합니다. 이번 게시에서는 재빌드·재설치하지 않았습니다. 최종 개선본 실제 설치·재설치 및 실제 SSD·UNC·물리적 연결 단절 시험은 별도입니다.

설치파일 SHA-256:

```text
3bf4f3cbaa269842bf47e164f0e4f24c2c85ffff6fd33de628eb55eeade5f10f
```

이전 배포본은 [전체 릴리스 목록](https://github.com/hypersh/BSsync_releases/releases)에 보존합니다.

## English

Download [BS Sync 3.0.1](https://github.com/hypersh/BSsync_releases/releases/tag/v3.0.1) and run `BS_Sync301.exe`. This version uses its own v3 installation and history. It does not migrate v2 history automatically. A first sync starts from current files; one-sided files are copied because previous deletions are unknown.

The original October 22 installer was verified and published on November 10, 2026. The current source test run passed 298 tests with one permission-related skip. This publication did not rebuild or reinstall the app.

