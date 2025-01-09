# 🚀 Visual Studio 2022 Community with OpenCV 설치 및 셋팅 가이드

---

## 📌 목차
1. [Visual Studio 2022 설치](#1-visual-studio-2022-설치)
2. [OpenCV 다운로드 및 설치](#2-opencv-다운로드-및-설치)
   - [필수 파일 복사](#22-필수-파일-복사)
3. [Visual Studio 환경 설정](#3-visual-studio-환경-설정)
   - [언어 및 폰트 설정](#31-언어-및-폰트-설정)
4. [프로젝트 속성 설정](#4-프로젝트-속성-설정)
5. [OpenCV 경로 설정](#5-opencv-경로-설정)

---

## 1. Visual Studio 2022 설치
1. **Visual Studio 2022 Community 설치 파일 실행**  
   - 이미 설치되어 있다면:
     - **영어팩**: `Tools > Get Tools and Features`  
     - **한글팩**: `도구 > 도구 및 기능 가져오기`
2. 설치 시 아래 옵션을 선택:
   - ✔ **C++를 사용한 데스크톱 개발**
   - ✔ **Visual Studio 확장 개발**
   - ✔ **언어팩 > 영어**
3. 설치를 시작합니다.

---

## 2. OpenCV 다운로드 및 설치
### 2.1 OpenCV 설치
1. [OpenCV 공식 웹사이트](https://opencv.org/)에서 최신 버전을 다운로드합니다.
2. 압축 해제 후 폴더를 **`Thirdparty`** 폴더에 이동:
   - 예: `C:\YourSolutionFolder\Thirdparty`
3. OpenCV 폴더 이름을 변경:  
   - 예: `opencv_4.10.0`

### 2.2 필수 파일 복사
아래 파일 4개를 **`Build\x64`** 폴더로 복사합니다:
- `opencv_world4100.dll`
- `opencv_world4100.pdb`
- `opencv_world4100d.dll`
- `opencv_world4100d.pdb`

---

## 3. Visual Studio 환경 설정
### 3.1 언어 및 폰트 설정
1. **Tools > Options > Environment > International Settings**  
   - **Language**: `English`로 설정
2. **Tools > Options > Environment > Fonts and Colors**  
   - **Font**: `Consolas`  
   - **Size**: `11`  
   - **Display Items**: 개인 취향대로 설정

---

## 4. 프로젝트 속성 설정
**모든 구성(Debug / Release) 및 모든 플랫폼(Active(64) / Win32 / x64)**에서 아래 설정을 동일하게 적용합니다.

1. **프로젝트 이름**에서 마우스 우클릭 > **속성(Properties)** 선택
2. 아래 설정을 적용합니다:

---

## 5. OpenCV 경로 설정
1. 프로젝트 이름 마우스 우클릭 -> 속성(Properties) 선택
2. OpenCV 관련 경로 추가
```
	../../Thirdparty\opencv_4.10.0\build\include

```

---

#### General
- **Output Directory**:  
  ```plaintext
  $(SolutionDir)Build\$(PlatformTarget)

  ```

---
