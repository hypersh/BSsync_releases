# BS Sync Releases

BS Sync의 Windows 설치파일을 제공하는 공개 다운로드 저장소이다. 애플리케이션 소스는 비공개 저장소에서 관리하며, 이 저장소에는 포함하지 않는다.

## BS Sync 2.0.5 다운로드

- [최신 Release](https://github.com/hypersh/BSsync_releases/releases/latest)
- [2.0.5 설치파일 — BS_Sync_v205.exe](https://github.com/hypersh/BSsync_releases/releases/download/v2.0.5/BS_Sync_v205.exe)
- [SHA-256 체크섬](https://github.com/hypersh/BSsync_releases/releases/download/v2.0.5/BS_Sync_v205.exe.sha256)

설치파일은 기존 설치를 업데이트하거나 새로 설치한다. 설치된 앱 이름은 `BS_Sync.exe`로 유지한다. 작업 목록·동기화 기록·복구 파일을 지울 필요가 없다.

## 주요 기능과 이번 업데이트

- 폴더 A/B의 동기화, 방향을 지정하는 미러, 백업 모드.
- 현재 파일 상태를 우선하는 A/B 수동 선택과 폴더 하위 항목 반영.
- 분석 제외 항목 보존, 실행 전 확인, 진행 표시, 중지 및 완료/부분완료/오류 기록.
- 검은 배경과 밝은 글씨, 테두리 없는 사각형 버튼, 검은 Windows 제목줄.

같은 작업 폴더를 여러 PC에서 사용하면 모든 PC를 2.0.5로 맞춘다. 미러와 A/B 상태 반영은 선택한 기준에 따라 반대편 파일을 삭제할 수 있으므로 비교 결과와 방향을 확인한 뒤 실행한다.

## 검증 범위

기능 자동 시험 154개(Linux)와 Windows UI 시험 10개를 통과하였다. Windows 설치파일을 빌드하고, 앱을 임시 DB로 열고 정상 종료하였다. Windows 11에서 제목줄 표시와 재표시도 확인하였다. 설치 프로그램 자체의 실제 설치/업데이트, 실제 외부 저장장치와 클라우드 동작은 이번 최종 점검 범위에 포함하지 않았다.

---

## English

This public repository contains Windows installers and checksums for BS Sync. Application source code is maintained privately.

Download [BS Sync 2.0.5](https://github.com/hypersh/BSsync_releases/releases/tag/v2.0.5), then run `BS_Sync_v205.exe` to install or update the app. Existing task settings and recovery data are retained by the installer configuration.

Version 2.0.5 supports Sync, Mirror and Backup modes, manual A/B choices based on current files, exclusion preservation and operation history. The final UI update adds dark surfaces, borderless rectangular buttons and black Windows title bars without changing the 2.0.5 synchronization engine.

Update every PC sharing the same workspace to 2.0.5. Review planned changes and deletion directions before execution. The installer was built and the app launch was checked; installation on the target system remains a separate check.
