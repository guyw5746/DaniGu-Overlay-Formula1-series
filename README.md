# F1-25-2026DLC-Custom-board-Release
F1 25 Game (2026 DLC) UDP Telemetry based custom widget
F1 25(2026 DLC)버전의 UDP telemetry data를 사용하여 실제 F1 2026시즌 중계화면과 유사한 테마의 리더보드, 알림창, 피트스탑 타이머등의 위젯을 만들기위한 프로젝트입니다.

udpclient 스레드에서 20780 포트로 전달받는 텔레메트리 데이터를 서버에 저장하며, 프론트엔드에서 웹소켓을 통해 필요한 주기별로 데이터를 요청하며 payload에 싣어 보내게 됩니다.

Current Version: 1.0.0

----------------------------------------------------
📜 Revision History
----------------------------------------------------
Ver.     Date        Description
0.9.1    2026.08.24  최초버전 - parser, server, leaderboard포함. (unlap 구현x)
0.9.2    2026.08.26  FEAT: 백엔드 / 프론트엔드 독립 구성. (ui 개별 payload사용)
1.0.0    2026.09.02  Release: 1st release: Server, Leaderboard

----------------------------------------------------
✨ 기능 및 추가 예정
----------------------------------------------------
In-Race:
- 구현: 순위, 타이어 컴파운드, Interval, In-pit, Safety Car, Fastest Lap, Gap to Leader, Tyre age, Current Tyre, Pit stops, Gain / Lost, Penalty, Warnings,
- 예정: 

----------------------------------------------------
🐛 버그 (Bugs to Fix)
----------------------------------------------------
- Interval 추월시 표기내용 오류  

----------------------------------------------------
🚀 사용 방법
----------------------------------------------------

1. 심허브나 기타 텔레메트리 사용 프로그램이 있다면 UDP 포워딩 기능을 사용하여 UDP포트 20780으로 맞춰주십시오.
    - F1 25 2026DLC 설정창 기준 
    UDP Telemery : ON
    UDP Broadcast Mode : Off
    UDP IP Address : 127.0.0.1
    UDP Port : 20780 
    UDP Send Rate : 60Hz
    UDP Format 2026 (중요!)

2. 폴더내의  f1-overlay-server.exe파일을 실행합니다.

3. 심허브 오버레이 툴이나 OBS 웹페이지 등을 활용하여 리더보드 소스를 켭니다
    사용할 url: http://localhost:8181

4. 게임 내에서 세션이 시작되어야 리더보드가 표시되며 세션이 끝나면 투명해집니다.

----------------------------------------------------
⚙️ Configuration (Port Settings)
----------------------------------------------------
만약 udp 포트, 웹소켓 포트를 수정해야할 경우, 서버를 처음 실행한 후 만들어지는 config.json 파일 내부의 변수를 수정하여 사용하십시오.

config.json
{
  "udpPort": 20780,     // 사용하고자 하는 udp 포트 번호
  "wsPort": 8181        // 사용하고자 하는 웹소켓 포트 번호
}


# F1-25-2026DLC-Custom-board-Release

A custom widget overlay project for the F1 25 game (2026 DLC) powered by UDP telemetry data. It is designed to render broadcast-style overlays—including leaderboards, notification popups, and pit stop timers—modeled after the official F1 2026 TV graphics.

The backend receives UDP telemetry data on port 20780, updates the server state, and streams telemetry/leaderboard payloads to the frontend via WebSocket at user-defined update rates.

Current Version: 1.0.0

----------------------------------------------------
📜 Revision History
----------------------------------------------------
Ver.     Date        Description
0.9.1    2026.08.24  Initial version - includes parser, server, and leaderboard (unlap logic not implemented).
0.9.2    2026.08.26  FEAT: Decoupled backend/frontend architecture (UI uses individual payloads).
1.0.0    2026.09.02  Release: 1st official release (Server & Leaderboard).

----------------------------------------------------
✨ Features
----------------------------------------------------
In-Race:
- Implemented: Position, Tyre Compound, Interval, In-Pit Status, Safety Car, Fastest Lap, Gap to Leader, Tyre Age, Current Tyre, Pit Stops, Gain / Lost, Penalties, Warnings
- Planned: (To be updated)

----------------------------------------------------
🐛 Known Issues (Bugs to Fix)
----------------------------------------------------
- Incorrect interval display/calculation during overtakes.

----------------------------------------------------
🚀 How to Use
----------------------------------------------------
1. Game & Telemetry Setup:
   If you are using SimHub or other telemetry routing software, enable UDP forwarding to port 20780.

   In-Game Settings (F1 25 - 2026 DLC):
   - UDP Telemetry: ON
   - UDP Broadcast Mode: OFF
   - UDP IP Address: 127.0.0.1
   - UDP Port: 20780
   - UDP Send Rate: 60Hz
   - UDP Format: 2026 (Crucial!)

2. Run the Server:
   Launch f1-overlay-server.exe located in the root folder.

3. Load the Overlay:
   Add a Browser Source in OBS, SimHub Overlay tool, or your preferred web browser:
   - URL: http://localhost:8181

4. In-Game Behavior:
   The leaderboard automatically appears once an active in-game session starts and turns transparent/hidden when the session ends.

----------------------------------------------------
⚙️ Configuration (Port Settings)
----------------------------------------------------
If you need to modify the UDP or WebSocket ports, run f1-overlay-server.exe once to generate a config.json file in the root folder, then edit the values as needed:

{
  "udpPort": 20780,
  "wsPort": 8181
}


