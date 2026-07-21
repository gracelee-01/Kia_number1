# 더그아웃 (Dugout)

KIA 타이거즈 팬들을 위한 직관(직접 관람) 인증 및 투표 웹 애플리케이션입니다.

## 프로젝트 소개

야구장을 직접 찾는 KIA 타이거즈 팬들이 자신의 직관 여부를 인증하고, 경기와 관련된 투표에 참여할 수 있는 서비스입니다.

## 기술 스택

- **Backend / DB**: Firebase, Firestore
- **인증**: Kakao OAuth, Firebase Anonymous Auth

## 주요 해결 과제

프로젝트 진행 중 발생한 기술적 이슈들을 직접 진단하고 해결했습니다.

- **크로스 디바이스 인증 버그 수정**: 인증 코드(auth code)가 uid로 잘못 사용되던 문제를 발견하고 수정
- **XSS 취약점 대응**: `innerHTML` 사용 부분을 `textContent`로 교체하여 보안 취약점 해소
- **투표 동시성 문제 해결**: 동시 투표 시 데이터가 덮어써지던 문제를 배열(array) 구조에서 맵(map) 구조로 변경하여 해결
- **Firebase Anonymous Auth 오류 해결**

## 배포 로드맵

Firebase Hosting → PWA → Google Play TWA → App Store (Capacitor) 순으로 단계적 배포를 계획

## 진행 중 기능

- UTIC 공공 API를 활용한 경기장 CCTV 날씨 정보 기능 (구현 중)
