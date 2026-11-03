# DaniGu Overlay (Lite) · 1.0.0

[한국어](#한국어) · [English](#english)

> **비공개 검증 빌드 / Private validation build**
> 무료·소스 비공개 앱입니다. 판매·재배포 조건과 일부 자산의 권리 확인이 끝나기 전까지 공개 배포를 보류합니다.
> Free-of-charge, closed-source application. Public release is on hold pending sale/redistribution terms and asset-rights verification.

## 한국어

F1 25(2026 Season Pack) UDP 텔레메트리로 방송용 오버레이와 피트월·휠 대시보드를 표시하는 Windows 앱입니다.
게임 조작을 보내는 프로그램은 아닙니다.

### 주요 기능

| 구분 | 포함 기능 |
|---|---|
| 오버레이 6종 | 리더보드, 차량 텔레메트리, 트랙맵, 섹터 타이머, 알림, 피트박스 타이머 |
| 화면 배치 | 모니터 비율 미리보기, 위젯 켜기/끄기·이동·크기 조절, 해상도·화면 비율 대응 |
| 앱 창 | 투명·항상 위·클릭 통과, 설정 창이 있는 모니터 전체에 표시 |
| 피트월 | LIVE CAR STATUS / LIVE TIMING, 레이스 컨트롤 이벤트 |
| 휠 대시보드 | 대시보드 선택·팀별 자동 선택, 화면 비율 대응 |
| 표시 설정 | Best lap / Previous lap 델타 기준, 폰트 선택, 종류별 알림 토글 |
| 네트워크 | LAN IP·보기 주소·오프라인 QR, 여러 IPv4 대상으로 UDP 원본 포워딩 |
| 트레이 | 설정 열기, 오버레이 표시/숨기기, 앱·서버 함께 종료 |

무전·음성 AI·레이스 전략 기능은 Lite에 포함하지 않습니다.

### 설치와 실행

필요 환경: Windows x64, Microsoft Edge WebView2 Runtime, F1 25 UDP 텔레메트리.
최초 버전은 서명하지 않은 테스트 빌드이며 SmartScreen 경고가 나타날 수 있습니다.

- **설치형:** `DaniGu-Overlay-Lite-1.0.0-windows-x64-setup.exe` 실행. 사용자별 설치이며 관리자 권한을 요구하지 않습니다.
  WebView2가 없으면 공식 설치 파일을 내려받으므로 인터넷이 필요합니다.
- **ZIP:** `DaniGu-Overlay-Lite-1.0.0-windows-x64.zip` 전체를 쓰기 가능한 폴더에 풀고 `DaniGu Overlay (Lite).exe` 실행.
  옆의 `f1-server-lite.exe`도 필요합니다. 앱 exe만 옮기면 실행되지 않습니다.

1. 게임 UDP 대상 IP를 앱 PC의 주소로, 수신 포트를 기본 `20777`로 맞춥니다.
2. 앱 설정에서 위젯·배치·폰트·델타 기준을 선택하고 저장합니다.
3. 표시할 모니터로 설정 창을 옮긴 뒤 **오버레이 시작**을 누릅니다.
4. 설정 창을 닫으면 종료가 아니라 트레이로 숨겨집니다. 완전히 종료하려면 트레이의 **앱과 서버 종료**를 사용합니다.

### 다른 기기에서 보기 / UDP 포워딩

- 같은 네트워크에서 설정 화면의 피트월·휠 대시보드 주소 또는 QR을 엽니다. 다른 기기는 **보기 전용**입니다.
- QR은 앱 내부에서 생성하며 외부 QR 서비스에 주소를 보내지 않습니다.
- 접속이 안 되면 Windows 방화벽의 사설 네트워크 앱 허용 및 PC IP를 확인합니다.
  앱은 방화벽 규칙을 자동으로 추가하거나 게임 설정을 바꾸지 않습니다.
- 포워딩은 기본 꺼짐입니다. 여러 `IPv4:port` 대상으로 수신한 원본 UDP를 전달하며 저장 즉시 적용됩니다.
  다른 프로그램에서 역방향 포워딩을 켜 순환 전달이 생기지 않게 하세요.
- UDP **수신 포트** 변경은 앱 재시작 후 적용됩니다.

### 설정과 사용자 자료

- 서버 exe 옆 `config.json`에 설정을 저장합니다. 쓰지 못하면 `%APPDATA%\F1Lite\config.json`을 사용합니다.
  AppData 설정이 이미 있으면 그것이 우선합니다.
- ZIP도 같은 저장 규칙을 공유합니다. 완전히 독립된 포터블 모드는 아닙니다.
- 제거·업데이트 전에 설정을 백업하세요. 설치 제거는 사용자 설정을 지우지 않습니다.
- 서버 exe 옆 `assets/`로 내장 파일을 덮어쓸 수 있습니다.
  예: `assets/logos/ferrari.svg`, `assets/fonts/MyFont.ttf`.
  사용자가 추가한 파일의 이용 권리는 사용자가 확인해야 합니다.
- 사용자 설정·데이터·녹화·원본 앱 소스는 배포 묶음에 포함하지 않습니다.

### 라이선스와 확인 범위

- 앱: 무료·소스 비공개. 판매·재배포 조건은 별도 확정 예정입니다. [LICENSE.txt](LICENSE.txt)를 확인하세요.
- 트랙맵: **Jules Roy (julesr0y)**, [원본 저장소](https://github.com/julesr0y/f1-circuits-svg),
  [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
  프로젝트의 기존 SVG를 그대로 동봉하며 화면에서 크기·색상을 조정할 수 있습니다.
  라이선스 근거는 프로젝트 소유자가 제공했으며 이번 작업에서 원본 저장소 접근은 확인하지 못했습니다.
- 폰트: Titillium Web, SIL OFL 1.1. 그 외 고지는 [THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt)와 `licenses/`를 확인하세요.
  해당되는 MPL-2.0 구성요소 원본은 `third-party-sources/`에 별도로 포함합니다.
- 카드 배경·체커기·타이어 등의 자산은 기존 포함 결정을 유지하지만 재배포 근거는 추가 확인 대상입니다.
- 게임 실물·트레이 손 조작·다른 실제 기기의 카메라 QR/방화벽 확인은 별도입니다.
  자동 테스트 통과를 실제 게임 검증으로 표현하지 않습니다.
- 자동 업데이트·코드 서명은 포함하지 않습니다.

## English

A Windows application displaying broadcast overlays, pitwall views and wheel dashboards from F1 25
(2026 Season Pack) UDP telemetry. It does **not** send game-control commands.

### Features

| Area | Included |
|---|---|
| Six overlays | Leaderboard, car telemetry, track map, sector timer, notifications, pitbox timer |
| Layout | Monitor-aspect preview, widget visibility/position/scale, resolution-independent placement |
| Overlay window | Transparent, always on top, click-through; fills the settings window's monitor |
| Pitwall | LIVE CAR STATUS / LIVE TIMING and race-control events |
| Wheel display | Dashboard selection, automatic team selection, aspect-ratio scaling |
| Display settings | Best lap / Previous lap delta, font selection, notification toggles |
| Networking | LAN IP/viewing links, locally generated QR, raw UDP forwarding to multiple IPv4 targets |
| System tray | Open settings, show/hide overlay, quit app and server together |

Voice radio, speech AI and race strategy are not included in Lite.

### Install and start

Requirements: Windows x64, Microsoft Edge WebView2 Runtime and F1 25 UDP telemetry.
This initial test build is unsigned and may trigger Windows SmartScreen.

- **Installer:** run `DaniGu-Overlay-Lite-1.0.0-windows-x64-setup.exe`.
  Installs per user without administrator rights. If WebView2 is missing, the official bootstrapper
  is downloaded; internet access is required.
- **ZIP:** extract all of `DaniGu-Overlay-Lite-1.0.0-windows-x64.zip` into a writable folder.
  Run `DaniGu Overlay (Lite).exe`. Keep `f1-server-lite.exe` alongside it; the app is not a single-file executable.

1. Set the game's UDP destination IP to the app PC and its port to `20777` by default.
2. Choose widgets, layout, font and delta reference in settings, then save.
3. Move settings to the desired monitor and press **Start overlay** (오버레이 시작).
4. Closing settings hides it to the tray. Use **Quit app and server** (앱과 서버 종료) to exit completely.
   The current app interface includes Korean labels; this English guide does not imply a fully localized UI.

### LAN viewing and UDP forwarding

- On the same network, open the pitwall/wheel URL or scan its QR from settings. Other devices are **view-only**.
- QR codes are generated locally; viewing URLs are not sent to an external QR service.
- Check Windows Firewall private-network app permissions and the selected PC IP if a device cannot connect.
  The app does not automatically add firewall rules or change game settings.
- Forwarding is off by default. It copies incoming raw UDP packets to multiple `IPv4:port` destinations.
  Changes apply immediately after saving. Avoid reverse forwarding loops between programs.
- Changes to the UDP **receive port** take effect after restarting the app.

### Settings and custom assets

- Settings are saved to `config.json` beside the server exe, falling back to
  `%APPDATA%\F1Lite\config.json` when the exe directory is not writable.
  An existing AppData file takes precedence.
- ZIP uses the same rules; it is **not** a fully isolated portable mode.
- Back up settings before updating/removing. Uninstall preserves user settings.
- Files in `assets/` beside the server exe override built-in assets, e.g.
  `assets/logos/ferrari.svg` or `assets/fonts/MyFont.ttf`. Check rights for your custom files.
- User config, data, recordings and original application source are not included in the distribution.

### Licenses and validation limits

- App: free of charge and closed source. Sale/redistribution terms remain pending; see [LICENSE.txt](LICENSE.txt).
- Track maps: **Jules Roy (julesr0y)**, [original repository](https://github.com/julesr0y/f1-circuits-svg),
  [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).
  Existing project SVGs are included unchanged; display scaling/colouring may apply.
  This license basis was supplied by the project owner; upstream availability could not be independently confirmed.
- Fonts: Titillium Web, SIL OFL 1.1. See [THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt) and `licenses/`.
  Applicable MPL-2.0 component source archives are supplied separately in `third-party-sources/`.
- Card backgrounds, chequered flag and tyre graphics remain included by prior project decision;
  redistribution provenance still needs confirmation.
- Live gameplay, manual tray operation and QR-camera/firewall checks on other physical devices remain separate.
  Automated tests do not establish live-game validation.
- No automatic updater or code signing is included.

## 배포 저장소 / Release repository

배포용 저장소 루트에 이 README와 `LICENSE.txt`, 고지·라이선스 폴더를 같은 상대 경로로 올리면 됩니다.
`RELEASE-NOTES.md`는 GitHub Release 본문으로 사용하고, 설치형·ZIP·`SHA256SUMS.txt`는 릴리즈 첨부물로 올립니다.
원본 소스·개인 설정·녹화는 올리지 않습니다. 현재는 로컬 검증만 하며 저장소 생성·업로드는 하지 않습니다.

Use this same README, `LICENSE.txt` and the notice/license folders at the release repository root.
Use `RELEASE-NOTES.md` as the GitHub Release body and attach the installer, ZIP and `SHA256SUMS.txt`.
Do not upload original source, personal config or recordings. This work only prepares local artifacts; no repository creation/upload is performed.
