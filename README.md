![Remote Input Overlay](assets/banner.jpg)

# Remote Input Overlay

Android 스마트폰에서 원격 화면(Parsec 등) 위에 투명 터치 컨트롤러를 띄워, **Windows PC로 키보드·마우스 입력을 전달**하는 무료 도구입니다.

---

## 🚀 빠른 다운로드 (최신 버전 자동 연결)

[![Windows PC용 EXE 다운로드](https://img.shields.io/badge/Windows_PC용-RemoteInputServer.exe-0078D6?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/rech4210/remote-input-overlay/releases/latest/download/RemoteInputServer.exe)
[![Android 스마트폰용 APK 다운로드](https://img.shields.io/badge/Android_폰용-APK_바로_받기-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://github.com/rech4210/remote-input-overlay/releases/latest/download/RemoteInputOverlay-latest.apk)
[![전체 릴리즈 보기](https://img.shields.io/badge/전체_버전_&_ZIP-Releases-24292F?style=for-the-badge&logo=github&logoColor=white)](https://github.com/rech4210/remote-input-overlay/releases/latest)

<table>
  <tr>
    <td align="center" width="210">
      <img src="assets/qr_apk_download.png" width="160" alt="Android APK 다운로드 QR 코드" /><br/>
      <b>📱 폰 카메라로 찍어 바로 받기</b><br/>
      <sub>PC에서 보고 계실 때 폰으로 옮길 필요 없이<br/>카메라로 찍으면 APK가 바로 내려받아집니다.</sub>
    </td>
    <td>
      <b>✅ 사전 준비: Tailscale 무료 앱 (PC + 폰)</b><br/>
      공유기 포트 설정 없이 내 PC와 스마트폰을 1:1로 안전하게 이어주는 무료 앱입니다.<br/>
      <b>PC와 폰에 각각 설치 → 같은 구글/애플 아이디로 로그인 → 연결 스위치 ON</b>만 하면 끝입니다.<br/><br/>
      👉 <b>PC용 Tailscale</b>: <a href="https://tailscale.com/download/windows">Windows 설치 파일 받기</a><br/>
      👉 <b>폰용 Tailscale</b>: <a href="https://play.google.com/store/apps/details?id=com.tailscale.ipn">Google Play 스토어에서 설치</a><br/><br/>
      <sub><b>지원 환경</b>: Android 8.0 이상 / Windows 10·11 (64비트, Python 설치 불필요)<br/>
      ※ iOS(아이폰/아이패드)는 OS 정책상 다른 앱 위에 오버레이를 띄울 수 없어 미지원</sub>
    </td>
  </tr>
</table>

---

## 🎬 실제 동작 미리보기

[![실제 동작 미리보기 (클릭 시 전체 4분 28초 MP4 영상 보기)](assets/demo_preview.gif)](https://github.com/rech4210/remote-input-overlay/releases/download/v1.4.3/demo.mp4)

> [▶ 전체 고화질 시연 영상 보기 (4분 28초 · MP4)](https://github.com/rech4210/remote-input-overlay/releases/download/v1.4.3/demo.mp4)

---

## ✅ 3분 설치 체크리스트 (처음 한 번만!)

### 1단계 · 연결 다리 놓기 (PC + 폰)
- [ ] **PC**와 **스마트폰** 둘 다 **Tailscale** 설치
- [ ] 두 기기 모두 **같은 계정(구글/애플 등)**으로 로그인 후 **연결 스위치(ON)** 켜기

### 2단계 · Windows PC에서 할 일
- [ ] 위 버튼으로 **`RemoteInputServer.exe`** 다운로드 후 더블클릭 실행
  - *"Windows의 PC 보호"* 파란 창이 뜨면 **`추가 정보` → `실행`** 클릭 *(개인 배포 파일이라 최초 1회만 표시)*
  - 방화벽 알림이 뜨면 **`사설 네트워크 허용`** 선택
- [ ] 검은 창이 열리고 **QR 코드**가 표시되는지 확인 *(같은 폴더에 `.overlay_token` 보안 키가 자동 생성됩니다)*

> [!TIP]
> 조작하려는 PC 프로그램이나 게임이 **관리자 권한**으로 실행 중이라면, `RemoteInputServer.exe`도 **우클릭 → 관리자 권한으로 실행**해야 입력이 정상 전달됩니다.

### 3단계 · 스마트폰에서 할 일
- [ ] 위 **QR 코드 스캔**(또는 APK 버튼 클릭)으로 앱 다운로드 후 설치 *("출처를 알 수 없는 앱 허용" 시 허용)*
- [ ] 앱 실행 → **`GRANT OVERLAY PERMISSION`** 눌러 **"다른 앱 위에 표시"** 허용
- [ ] 앱 상단 **`📷 QR 코드로 1초 연결`** 클릭 → PC 검은 창에 뜬 QR 코드 스캔 *(IP·포트·토큰 자동 입력)*
- [ ] **`START OVERLAY`** 버튼 클릭 → 상단 상태 점이 **초록색(`●`)**이 되면 완료!

이제 **Parsec 등 원격 앱을 켜고 가로모드로 전환**하면 기기 해상도에 맞춰진 기본 배치로 바로 조작할 수 있습니다.

---

## 🎮 조작 및 주요 기능

### 상단 제어 바 아이콘

| 아이콘 | 기능 |
|:---:|:---|
| **`🔓` / `🔒` + `JOY`** | 드래그해 위치 이동 *(가로/세로 위치 각각 자동 저장)* · 탭하여 잠금 전환 |
| **`✎`** | **배치 편집 모드** ON/OFF *(주황색 테두리 표시)* |
| **`⚙`** | 빠른 설정 메뉴 (빠른 프리셋 전환, 추천 갤러리, 조이스틱/D-PAD, 터치패드, 스마트 Tab 등) |
| **`–` / `+`** | 오버레이 접기 / 펼치기 |
| **`●`** | 연결 상태 *(초록=연결됨 · 노랑=재접속 · 빨강=끊김 / 탭하면 즉시 재접속)* |

### 핵심 기능 요약
- **💬 퀵 채팅 바 (`⚙ → 💬 퀵 채팅` 또는 `💬채팅` 키 배치)**: 채팅 시 오버레이 버튼이 자동 숨김되어 키보드를 가리지 않으며, **Windows 한/영 상태와 무관하게 한글·영문 문장을 즉시 전송**하고 자동 복귀합니다.
- **자유 버튼 편집 (`✎`)**: 드래그로 위치 이동(자석 스냅 지원), 버튼 탭으로 **이름 변경 · 크기(`S/M/L/XL`) · 1탭 누름 고정 · 연결키(Nested Key) · 이미지 설정 · 버튼 복제(`⧉`)** 지원
- **태블릿 터치패드**: 드래그로 마우스 이동, **1손가락 탭 = 제자리 좌클릭**, **2손가락 탭 = 우클릭**, 상단 **`정밀`** 버튼으로 미세 이동 전환 *(`⚙ → 태블릿 정밀도`에서 감도 조절)*
- **스마트 `Tab` 스와이프**: `TAB` 버튼을 누른 채 상/하/좌/우로 밀면 설정한 간격마다 1틱씩 탐색
- **프리셋 & 추천 갤러리 (`⚙ → 📋 프리셋`)**: 저장된 슬롯 1~5 빠른 전환 및 이름 변경(`✎`), **☁️ 추천 프리셋 갤러리**에서 검증된 배치 바로 불러오기, 텍스트 복사/붙여넣기 공유 지원
- **자동 업데이트 · 로드맵**: 새 버전이나 공지가 등록되면 Android 앱과 PC 서버 모두에 자동 안내되며, 앱 하단 **`🗺 업데이트 계획`** 에서 예정 기능을 확인할 수 있습니다.

<details>
<summary><b>자주 묻는 질문 / 문제 해결 (클릭해서 펼치기)</b></summary>

- **Windows에서 "PC 보호" 파란 창이 떠요**: 개인 배포 프로그램이라 최초 1회 표시됩니다. `추가 정보 → 실행`을 누르면 정상 실행됩니다.
- **상태 점이 계속 노랑/빨강이에요**: PC와 스마트폰 모두 Tailscale이 **같은 계정으로 연결(ON)** 되어 있는지, PC에서 `RemoteInputServer.exe`가 켜져 있는지 확인해 주세요.
- **초록불인데 PC 프로그램에 키가 안 먹혀요**: 조작할 프로그램이 관리자 권한으로 실행 중일 수 있습니다. `RemoteInputServer.exe`를 **우클릭 → 관리자 권한으로 실행**해 주세요.
- **QR 코드가 잘 안 찍혀요**: PC 콘솔 창을 조금 키우거나, 콘솔에 적힌 `Tailscale IP`와 폴더 안 `.overlay_token` 파일 내용을 앱에 직접 입력하셔도 동일하게 연결됩니다.
- **버튼 위치가 꼬였거나 초기화하고 싶어요**: `⚙ → 프리셋 → ⭐ 기본 추천 배치 불러오기`를 누르면 기기 해상도에 맞춰 깔끔하게 초기화됩니다.

</details>

---

## 💬 피드백 · 버그 제보 · 프리셋 공유

- **💬 피드백 / 버그 제보 (비로그인 가능)**: https://forms.gle/gepva2zctACe9hUK8
- **📤 추천 프리셋 공유 신청 (스팸 방지 Google 로그인 필요)**: https://forms.gle/TFwHwKtfB8uzeE1U8

---

## ⚠️ 유의 사항 및 면책 안내

> [!WARNING]
> 본 프로그램은 개인의 원격 입력 편의를 위해 제공되며, 사용에 따른 모든 책임은 사용자 본인에게 있습니다.

- 본 프로그램은 사용자의 Tailscale 사설망 내에서만 동작하도록 설계되었으나, **Tailscale 계정 보안 및 `.overlay_token` 파일 관리**는 사용자가 직접 주의하여 관리해야 합니다.
- 앱 개선을 위해 버전·해상도·연결 성공 여부·기능 사용 여부 같은 익명 통계만 수집하며(키 입력·채팅·IP·토큰은 수집하지 않음), 원치 않으시면 메인 화면 하단 스위치에서 언제든 끌 수 있습니다.
- 대상 프로그램·게임의 운영 정책, 보안 모듈 또는 업데이트에 따라 일부 입력이 제한되거나 작동하지 않을 수 있으며, 이로 인해 발생하는 불이익이나 손해에 대해 개발자는 책임을 지지 않습니다.
