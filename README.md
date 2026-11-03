<div align="center">

# DaniGu Overlay (Lite)

**Your race. Your display.**

F1 25 · 2026 Season Pack · Windows x64

게임 텔레메트리를 나만의 오버레이와 대시보드로.

Turn race telemetry into your own overlays and dashboards.

**[시작하기 / Quick start](#quick-start)** · **[English](#english)**

</div>

---

| 🏁 Overlay | 📊 Pitwall | 🎛️ Dashboard |
| :---: | :---: | :---: |
| 리더보드 · 텔레메트리 · 트랙맵 | 차량 상태 · 라이브 타이밍 | 팀별 휠 대시보드 |
| 섹터 · 알림 · 피트 타이머 | 다른 기기에서 보기 | 팀별 대시보드 매칭 |

위젯 위치·크기·폰트·델타 기준을 원하는 대로 설정하세요. 오버레이 표시 창으로 간편하게 사용할 수 있습니다.

<a id="quick-start"></a>
## 🚀 시작하기

1. 이 저장소의 **Releases → 최신 버전 → Assets**에서 `…-setup.exe`를 받아 설치합니다.
2. 게임에서 **UDP 텔레메트리를 켜고**, 대상 IP를 앱 PC로 설정합니다. 게임과 앱의 UDP 포트를 동일하게 맞추세요. 기본값은 **20777**입니다.
3. 앱에서 배치를 저장하고, 원하는 모니터로 설정 창을 옮긴 뒤 **오버레이 시작**을 누릅니다.

> **Node.js 설치는 필요 없습니다.** Windows x64와 WebView2가 필요하며, 설치형은 WebView2가 없으면 인터넷으로 설치합니다.

<details>
<summary>알아둘 점</summary>

- ZIP은 **전체 압축 해제** 후 실행하세요. 앱과 서버 실행 파일을 함께 두어야 합니다.
- 설정 창을 닫으면 트레이로 숨겨집니다. 완전 종료는 **앱과 서버 종료** 메뉴를 사용하세요.
- 수신 포트를 바꾸면 앱을 완전히 종료한 뒤 다시 실행하세요.
- 미서명 빌드이므로 SmartScreen 경고가 나올 수 있습니다. 출처를 확인한 파일만 실행하세요.
- 1.0.0/1.0.1에는 자동 업데이트가 없습니다. 앱 종료 후 새 설치형으로 덮어 설치할 수 있습니다. 설정은 먼저 백업하세요.
- Lite에는 음성 AI·무전·레이스 전략이 포함되지 않습니다. 게임 조작을 보내지 않습니다.
- 자세한 사용법은 다운로드 패키지의 README를 확인하세요.

</details>

## English

Six configurable overlays, two pitwall views and team-aware wheel dashboards for F1 25 (2026 Season Pack).
Customize layout, fonts and delta reference; view dashboards on other devices on your LAN.

**Get started:** download the latest `…-setup.exe` from **Releases → Assets**, enable game UDP telemetry,
set the destination to the app PC and match both UDP ports (**20777** by default).
Save your layout, move settings to the desired monitor and select **오버레이 시작** (Start overlay).

No Node.js required. Windows x64 and WebView2 are required; the installer downloads WebView2 if missing.
Extract ZIP downloads completely. Closing settings hides the app to the tray; use **앱과 서버 종료** to quit.
The current UI includes Korean labels. Builds are unsigned; verify the download source.
Versions 1.0.0/1.0.1 have no automatic updater. Quit the app before installing a newer version; back up settings first.
Voice AI/radio and race strategy are not included.

---

<sub>
Free of charge · Closed source · Unofficial project, not affiliated with Formula 1 or EA.
Free use and official-link sharing permitted; no sale or binary redistribution.
See LICENSE.txt and THIRD-PARTY-NOTICES.txt in the download for terms and credits.
Track maps: <a href="https://github.com/julesr0y/f1-circuits-svg">Jules Roy (julesr0y)</a>,
<a href="https://creativecommons.org/licenses/by/4.0/">CC BY 4.0</a>.
</sub>
