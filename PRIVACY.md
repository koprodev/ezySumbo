# ezy SumBo 개인정보처리방침 / Privacy Policy

시행일 / Effective date: 2026-09-28

개발자 / Developer: **koprodev**

[한국어](#한국어) · [English](#english)

## 한국어

이 방침은 Windows용 **ezy SumBo**가 처리하는 정보와 사용자가 선택할 수 있는 사항을 설명합니다. ezy SumBo는 사용자가 선택한 다른 프로그램의 창 또는 창의 일부를 작은 미러 창으로 표시하는 앱입니다.

### 1. 화면과 실행 중인 창 정보

- 대상 선택과 미러링을 위해 실행 중인 창의 제목, 프로세스 이름·ID, 창 클래스, 실행 파일 경로 및 창 핸들을 기기 안에서 읽습니다. 창 제목에는 웹페이지나 문서 이름 등 개인적인 내용이 포함될 수 있습니다.
- 사용자가 선택한 대상 창의 화면을 Windows의 화면 합성·캡처 기능으로 처리하고 로컬 미러 창에 표시합니다. 선택한 영역만 표시하더라도 캡처 기능은 대상 창 전체의 프레임을 메모리에서 처리할 수 있습니다.
- 앱은 미러링하는 화면을 서버로 전송하거나 영상·스크린샷 파일로 저장하지 않습니다. 캡처 프레임은 미러링을 위한 메모리에서 교체·해제됩니다.
- 마우스 전달 기능을 켜면 미러 창에 대한 마우스 입력을 선택한 대상 창으로 전달합니다. 전역 단축키는 앱 기능을 제어하기 위해 사용하며 입력 내용을 기록하는 기능은 제공하지 않습니다.
- 앱은 마이크·카메라·연락처·위치 정보에 접근하지 않으며, 브라우저의 방문 기록·쿠키·비밀번호 파일을 읽지 않습니다. 다만 선택한 창의 화면에 표시된 내용은 미러 화면에도 나타날 수 있습니다.

### 2. 기기에 저장되는 정보

다음 정보는 기능과 설정을 유지하기 위해 기기에 저장됩니다. 앱은 이 파일을 개발자에게 자동으로 전송하지 않습니다.

| 정보 | 목적과 기본 저장 위치 |
|---|---|
| 언어, 표시·입력 설정, Windows 시작 옵션, 업데이트 확인 설정, 브라우저 연동 설정과 원래 정책값의 백업 | `%AppData%\ezySumbo\settings.json` |
| 사용자가 저장한 영역 이름과 좌표 | `%AppData%\ezySumbo\regions.json` |
| 프로필 이름, 대상 창 제목·프로세스 이름·창 클래스, 표시 영역·위치·크기·투명도 등 | `%AppData%\ezySumbo\profiles.json` |
| 사용자 지정 언어 파일과 기존 Sumbo 데이터 이전 기록 | `%AppData%\ezySumbo\lang` 및 같은 앱 데이터 폴더의 이전 완료 기록 |
| 프로모션 배너 정보·이미지와 가져온 시각 또는 불러오기 실패 결과 | `%LocalAppData%\ezySumbo\cache\sponsor-banner.json` |

설치 방식에 따라 Windows가 앱 데이터를 앱별 저장 위치로 관리할 수 있습니다. 프로필·영역·설정 파일은 별도로 암호화하지 않는 JSON 파일입니다.

기존 Sumbo 데이터가 있으면 설정·영역·프로필·언어 파일을 새 ezy SumBo 데이터 폴더로 한 번 복사할 수 있습니다. 이 과정은 기존 원본을 삭제하지 않으며, 이전 기록에 원본 폴더 경로와 완료 시각이 남습니다.

Microsoft Store의 MSIX 설치본에서는 브라우저 정책을 변경하는 연동 옵션이 비활성화됩니다. 일반 설치본에서 제공하는 선택적 브라우저 연동 기능은 가려진 브라우저 창의 표시를 유지하도록 Windows의 브라우저 정책값을 변경합니다. 일반 설치본에서 관리자 승인이 필요한 경우 원래 사용자의 Windows 보안 식별자(SID), 정책 백업 및 작업 결과를 로컬 임시 파일로 전달하고 작업 후 삭제를 시도합니다. 이 정보는 네트워크로 전송하지 않습니다. 앱은 Windows 시작 옵션을 위해 로컬 시작 프로그램 설정도 관리합니다.

### 3. 인터넷 연결과 프로모션 배너

설정 창을 열면 앱은 `app.ezy.kr`에서 프로모션 배너 정보와 이미지를 HTTPS로 가져올 수 있습니다. 배너 설정에 지정된 이미지 주소는 `ezy.kr` 또는 그 하위 도메인으로 제한됩니다. 배너는 화면 내용·창 제목·프로필에 따라 선택하지 않습니다.

이 요청을 처리하는 서버와 네트워크 제공자는 IP 주소, 요청 시각·주소, HTTP 요청 헤더 등 통신에 필요한 정보를 받을 수 있습니다. 앱은 요청의 User-Agent에 `ezySumbo`를 사용하며, 캡처한 화면, 대상 창 정보, 저장한 설정·프로필, Windows SID 또는 별도로 생성한 사용자 식별자를 요청에 넣지 않습니다. 서버 설정에 따라 접속기록이 남을 수 있으며, 이러한 서버 기록은 아래의 로컬 캐시 보관 방식과 별개입니다.

배너 캐시는 6시간 동안 재사용할 수 있습니다. 6시간은 자동 삭제 기한이 아니며, 캐시 파일은 나중에 갱신하거나 사용자가 삭제할 때까지 기기에 남을 수 있습니다. 배너를 불러오지 못해도 미러링을 사용할 수 있습니다.

현재 배포 구성에서 앱 자체의 GitHub 업데이트 확인 주소는 비활성화되어 있습니다. Microsoft Store를 통한 설치·업데이트 및 Windows의 자체 진단 기능은 Microsoft가 별도로 처리합니다.

### 4. 외부 링크, 계정 및 문의

앱 자체는 회원가입·클라우드 동기화·사용자 행동 분석 또는 자동 오류 보고 기능을 제공하지 않습니다. 후원 링크나 프로모션 배너를 선택하면 기본 브라우저 등 Windows에 등록된 앱에서 GitHub Sponsors, Microsoft Store 또는 `ezy.kr` 웹페이지를 열 수 있습니다. 후원 링크에는 앱 내 선택 위치와 후원 단계에 해당하는 고정 URL 매개변수가 포함될 수 있습니다. 이 매개변수에 사용자의 창 정보나 개인 식별자를 넣지 않습니다.

외부 사이트에서 로그인·후원·결제·문의 등을 진행하면 해당 서비스가 그 정보를 처리합니다. 해당 웹사이트와 브라우저의 개인정보처리방침 및 설정이 적용되며, 앱은 결제 정보를 직접 받지 않습니다.

문의는 [ezy SumBo GitHub Issues](https://github.com/koprodev/ezySumbo/issues)를 이용해 주세요. GitHub에 직접 제출한 계정 이름, 문의 내용과 첨부물은 공개될 수 있으므로 비밀번호, 개인 문서, 개인 식별정보 또는 민감한 화면을 올리지 마세요. 개발자는 사용자가 제출한 내용을 읽고 문의에 답변할 수 있습니다.

### 5. 보관, 삭제 및 사용자 선택

- 저장된 프로필과 영역은 앱에서 삭제할 수 있습니다. 설정과 기타 로컬 파일은 변경·삭제하기 전까지 남을 수 있습니다.
- 로컬 데이터를 모두 지우려면 먼저 앱의 Windows 시작 옵션을 끄고, 일반 설치본에서 브라우저 연동을 사용했다면 해당 설치본에서 연동을 해제하세요. Store MSIX 설치본에서는 이 정책을 변경하거나 해제하지 않습니다. 브라우저 연동 해제에는 원래 정책값의 백업이 필요하므로 설정 파일을 먼저 지우지 마세요. 이후 앱을 종료한 뒤 위의 ezySumBo 데이터·캐시 폴더를 삭제하면 저장한 설정·프로필·영역이 초기화됩니다.
- 기존 Sumbo에서 복사한 원본은 별도로 남을 수 있습니다. 필요하지 않은 원본과 사용자가 만든 백업은 별도로 관리·삭제해야 합니다.
- 임시 정책 파일은 정상적인 정리 과정에서 삭제를 시도하지만, 앱·시스템의 비정상 종료나 파일 접근 실패 시 남을 수 있습니다.
- 앱의 네트워크 연결을 차단해도 로컬 미러링은 사용할 수 있습니다. 원격 배너는 불러올 수 없으며, 외부 링크의 연결은 링크를 여는 브라우저 등 해당 앱의 네트워크 설정을 따릅니다.
- 외부 서비스에 직접 제공한 정보와 서버의 접속기록에 관한 문의는 아래 연락처 또는 해당 서비스의 개인정보 문의 경로를 이용해 주세요. 앱의 로컬 파일 삭제가 외부 서비스의 기록을 삭제하지는 않습니다.

### 6. 변경 및 연락처

이 방침이 변경되면 이 페이지의 내용과 시행일을 갱신합니다.

개인정보 관련 문의: [koprodev / ezy SumBo Issues](https://github.com/koprodev/ezySumbo/issues)

## English

This policy explains the information processed by **ezy SumBo** for Windows and the choices available to you. ezy SumBo displays a window, or a selected portion of a window, from another application in a small local mirror window.

### 1. Screen content and running windows

- To list and mirror target windows, the app reads window titles, process names and IDs, window classes, executable paths, and window handles on your device. Window titles may include personal information, such as webpage or document names.
- The app uses Windows composition and capture features to display your selected target window locally. Even when only a selected region is displayed, the capture feature may process frames of the entire target window in memory.
- The app does not upload mirrored screen content or save it as video or screenshot files. Capture frames are replaced and released in memory as part of mirroring.
- When mouse forwarding is enabled, the app forwards mouse input from the mirror window to the selected target window. Global keyboard shortcuts control app features; the app does not provide a keystroke recording feature.
- The app does not access your microphone, camera, contacts, or location, and does not read browser history, cookie, or password files. Content visible in your selected window may nevertheless appear in the mirror.

### 2. Information stored on your device

The following information is stored to retain app features and preferences. The app does not automatically send these files to the developer.

| Information | Purpose and default location |
|---|---|
| Language, display and input preferences, Windows startup and update-check settings, browser integration preferences, and backups of original policy values | `%AppData%\ezySumbo\settings.json` |
| Names and coordinates of saved regions | `%AppData%\ezySumbo\regions.json` |
| Profile names, target window titles, process names, window classes, display regions, position, size, opacity, and related preferences | `%AppData%\ezySumbo\profiles.json` |
| Custom language files and a record of migration from the earlier Sumbo app | `%AppData%\ezySumbo\lang` and a migration completion record in the same app data folder |
| Promotion banner metadata, image, and retrieval time, or a failed retrieval result | `%LocalAppData%\ezySumbo\cache\sponsor-banner.json` |

Windows may manage app data in an app-specific location depending on how the app is installed. Profile, region, and settings files use JSON without additional app-level encryption.

If data from the earlier Sumbo app exists, settings, regions, profiles, and language files may be copied once into the new ezy SumBo data folder. The original files are not deleted. The migration record contains the original folder path and completion time.

The Microsoft Store MSIX edition disables the browser integration option that changes browser policies. In the regular installer edition, optional browser integration changes Windows browser policy values to keep an obscured browser window rendering. When that edition requires administrator approval, the app passes the original user's Windows security identifier (SID), policy backups, and operation results through local temporary files and attempts to delete them after the operation. This information is not sent over the network. The app also manages local startup settings for its Windows startup option.

### 3. Internet connections and promotion banners

When you open the settings window, the app may download promotion banner information and images from `app.ezy.kr` over HTTPS. Image addresses specified in the banner configuration are limited to `ezy.kr` and its subdomains. Banners are not selected using your screen content, window titles, or profiles.

The server and network providers handling these requests may receive information required for communication, including your IP address, request time and address, and HTTP request headers. The app uses `ezySumbo` as its User-Agent. It does not include captured screen content, target window information, saved settings or profiles, your Windows SID, or an app-generated user identifier in these requests. Access logs may be kept according to server configuration; these server records are separate from the local cache described below.

The banner cache can be reused for six hours. This is not an automatic deletion deadline: the cache file may remain on your device until it is later replaced or you delete it. Mirroring remains available if a banner cannot be loaded.

The app's own GitHub update-check endpoint is disabled in the current distribution configuration. Installation and updates through Microsoft Store, and Windows' own diagnostic features, are handled separately by Microsoft.

### 4. External links, accounts, and support

The app itself does not provide account registration, cloud synchronization, user behavior analytics, or automatic error reporting. Selecting a sponsorship link or promotion banner may open GitHub Sponsors, Microsoft Store, or an `ezy.kr` page in your default browser or another Windows-registered app. Sponsorship links may include fixed URL parameters identifying the in-app link location and sponsorship tier. These parameters do not include your window information or a personal identifier.

If you sign in, sponsor, pay, or request support on an external site, that service handles the information you provide. The external website's privacy policy and your browser's settings apply. The app does not directly receive payment details.

For support, use [ezy SumBo GitHub Issues](https://github.com/koprodev/ezySumbo/issues). Your GitHub account name, issue text, and attachments may be public. Do not post passwords, private documents, personal identifiers, or sensitive screenshots. The developer can read the information you choose to submit and respond to your inquiry.

### 5. Retention, deletion, and choices

- You can delete saved profiles and regions in the app. Settings and other local files may remain until you change or delete them.
- To remove local app data, first turn off the app's Windows startup option. If you used browser integration in the regular installer edition, turn it off in that edition. The Store MSIX edition does not change or restore these policies. Turning off browser integration requires the original policy backups, so do not delete the settings file first. Then close the app and delete the ezySumBo data and cache folders listed above to reset your saved settings, profiles, and regions.
- Original files copied from the earlier Sumbo app may remain separately. Manage or delete those originals and any backups you created separately if you no longer need them.
- The app attempts to delete temporary policy files during normal cleanup, but files may remain after an app or system crash or a file access failure.
- Local mirroring can be used with the app's network access blocked. Remote banners cannot be downloaded. External links follow the network settings of the browser or other app that opens them.
- For questions about information you submit to external services or server access logs, use the contact below or the relevant service's privacy contact. Deleting the app's local files does not delete external service records.

### 6. Changes and contact

If this policy changes, this page and its effective date will be updated.

Privacy contact: [koprodev / ezy SumBo Issues](https://github.com/koprodev/ezySumbo/issues)
