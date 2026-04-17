## Node.js 다운로드 및 설치 가이드 (2026년 최신판)

Node.js는 Chrome V8 JavaScript 엔진으로 빌드된 **JavaScript 런타임(Runtime, 실행 환경)**입니다. 2026년 현재, Node.js는 서버 사이드 애플리케이션 개발뿐만 아니라 AI 모델 연동, 실시간 데이터 스트리밍 등 다양한 분야에서 핵심적인 역할을 하고 있습니다.

---

## 1. 설치 전 확인 사항: 버전 선택 (LTS vs Current)

Node.js 공식 홈페이지([nodejs.org](https://nodejs.org/))에 접속하면 두 가지 버전 중 하나를 선택해야 합니다.

* **LTS (Long Term Support, 장기 지원 버전):** 기업용 애플리케이션이나 실제 서비스 운영에 권장되는 가장 **안정적인(Stable)** 버전입니다. 2026년 4월 현재 최신 LTS 버전은 **v24.x (Krypton)** 및 **v22.x (Jod)**입니다.
* **Current (최신 기능 버전):** 최신 자바스크립트 문법과 Node.js의 실험적인 기능을 포함하는 버전입니다. 현재 **v25.x**가 배포 중입니다.

> **전문 용어 해설**
> * **Runtime (런타임):** 프로그래밍 언어가 구동되는 환경을 의미합니다.
> * **LTS (Long Term Support):** 출시 후 일정 기간(보통 3년) 동안 보안 업데이트 및 버그 수정을 보장하는 버전 관리 정책입니다.

---

## 2. 운영체제별 설치 방법

### 2.1. Windows (윈도우) 설치
가장 일반적인 방법은 MSI 설치 파일을 사용하는 것입니다.

1.  **공식 사이트 접속:** [Node.js 다운로드 페이지](https://nodejs.org/en/download/)로 이동합니다.
2.  **Installer 다운로드:** `Windows Installer (.msi)` 64-bit 버전을 클릭하여 다운로드합니다.
3.  **설치 마법사 실행:** 다운로드한 파일을 실행하고 `Next`를 눌러 진행합니다.
    * **Custom Setup:** 기본 경로를 유지하는 것이 좋습니다.
    * **Tools for Native Modules:** "Automatically install the necessary tools" 체크박스를 선택하면 Python이나 Visual Studio Build Tools 등 컴파일에 필요한 도구들을 자동으로 설치해 줍니다. (권장)
4.  **완료:** 설치가 끝나면 마침 버튼을 누릅니다.



### 2.2. macOS (맥OS) 설치
macOS 사용자는 공식 패키지(.pkg)를 이용하거나 패키지 관리자인 Homebrew를 사용할 수 있습니다.

* **PKG 파일 방식:** 공식 사이트에서 `macOS Installer (.pkg)`를 내려받아 실행합니다. Intel 칩과 Apple Silicon(M1, M2, M3, M4)을 모두 지원하는 유니버설 바이너리가 제공됩니다.
* **Homebrew 방식:** 터미널에서 다음 명령어를 입력합니다.
    ```bash
    brew install node
    ```

### 2.3. Linux (리눅스) 설치
데비안(Debian)이나 우분투(Ubuntu) 계열에서는 NodeSource 바이너리 배포판을 사용하는 것이 가장 최신 LTS 버전을 유지하기에 좋습니다.

```bash
# 2026년 기준 v24 LTS 설치 예시
curl -fsSL https://deb.nodesource.com/setup_24.x | sudo -E bash -
sudo apt-get install -y nodejs
```

---

## 3. 설치 확인 및 환경 변수 체크

설치가 완료되었다면 터미널(CMD, PowerShell 또는 Terminal)을 열고 다음 명령어를 입력하여 정상 설치 여부를 확인합니다.

```bash
# Node.js 버전 확인
node -v

# npm(Node Package Manager) 버전 확인
npm -v
```

정상적으로 설치되었다면 `v24.14.1`이나 `v22.22.2`와 같은 버전 숫자가 출력됩니다.

> **전문 용어 해설**
> * **NPM (Node Package Manager, 노드 패키지 매니저):** Node.js에서 사용하는 라이브러리들을 관리하고 설치하는 도구입니다. Node.js 설치 시 자동으로 함께 설치됩니다.

---

## 4. [실전 팁] NVM(Node Version Manager) 사용 권장

프로젝트마다 요구하는 Node.js 버전이 다를 수 있습니다. 이때 시스템에 직접 설치하는 대신 **NVM(Node Version Manager, 노드 버전 관리자)**을 사용하면 여러 버전을 자유롭게 전환할 수 있어 전문가들이 가장 선호하는 방식입니다.

* **Windows:** [nvm-windows](https://github.com/coreybutler/nvm-windows) 사용
* **macOS/Linux:** [nvm 공식 저장소](https://github.com/nvm-sh/nvm) 참조

**NVM 주요 명령어:**
```bash
nvm install 24.14.1  # 특정 버전 설치
nvm use 24.14.1      # 해당 버전 사용
nvm list             # 설치된 버전 목록 확인
```

---

## 5. 최신 공식 문서 및 리소스

설치 과정에서 문제가 발생하거나 최신 릴리스 노트를 확인하려면 아래 공식 링크를 참조하십시오.

* **Node.js 공식 다운로드:** [https://nodejs.org/en/download/](https://nodejs.org/en/download/)
* **Node.js 최신 릴리스 정보 (GitHub):** [https://github.com/nodejs/node/releases](https://github.com/nodejs/node/releases)
* **API 공식 문서:** [https://nodejs.org/docs/latest/api/](https://nodejs.org/docs/latest/api/)

---
**주의사항 (과금 관련):**
Node.js 자체는 오픈 소스 무료 소프트웨어입니다. 하지만 이를 AWS Lambda(람다)나 EC2(클라우드 가상 서버)에 배포하여 운영할 경우, 해당 클라우드 서비스 이용 요금이 발생할 수 있으니 주의하시기 바랍니다. 특히 AWS 프리티어 기간이 종료된 계정은 리소스 사용량에 따라 비용이 청구됩니다.

Next Step: Node.js의 기본 구조 및 REPL 사용법
