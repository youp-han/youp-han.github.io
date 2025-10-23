# UniRent - 임대관리솔루션

<p align="center">
  <strong>부동산 임대 관리를 위한 종합 솔루션</strong>
</p>

**UniRent**는 Flutter로 제작된 종합 임대 관리 솔루션입니다. 자산, 임차인, 임대 계약 및 청구 관리를 간소화하여 임대 관리를 효율적으로 만듭니다.

## 📝 프로젝트 현황 (Project Status)

현재 **Phase 4** 개발이 완료되었으며, 핵심 기능 대부분이 구현되었습니다. 코드 품질 향상을 위한 리팩토링과 테스트 코드 작성이 꾸준히 진행 중입니다.

### **Version 0.5.0 (최신)**
*   **신규 기능**:
    *   **생체 인증**: 지문/Face ID를 이용한 빠르고 안전한 로그인 (iOS & Android).
    *   **데이터베이스 백업/복원**: 자동 백업 시스템 및 수동 데이터 복원 기능.
    *   **비밀번호 찾기**: 이메일 인증을 통한 비밀번호 재설정 기능.
    *   **보안 강화**: `flutter_secure_storage` (Keychain/Keystore)를 사용한 민감 정보 보안 저장.

### **Version 0.4.x**
*   **주요 구현 사항**:
    *   **핵심 기능 CRUD**: 임차인(Tenant), 임대 계약(Lease), 청구(Billing) 기능의 전체 CRUD 구현.
    *   **데이터 영속성**: 로컬 SQLite 데이터베이스(`Drift`)를 통한 모든 데이터 영속성 확보.
    *   **UI/UX 개선**: 반응형 UI, 전역 내비게이션 시스템(`NavigationRail`/`Drawer`) 적용 및 전반적인 사용자 경험 개선.

## ✨ 주요 기능 (Features)

*   **인증**: 이메일/비밀번호, 생체 인증, 비밀번호 재설정.
*   **대시보드**: KPI 시각화 (월별 수입, 미납액 등), 최근 활동 로그.
*   **자산 관리**: 건물 및 개별 호실 정보 등록, 수정, 삭제 (CRUD).
*   **임차인 관리**: 임차인 정보 및 계약 이력 관리 (CRUD).
*   **계약 관리**: 임대차 계약 정보, 기간, 보증금/월세 관리 (CRUD).
*   **청구 및 수납**: 월세 자동 청구, 수납 내역 등록 및 자동 배분, PDF 영수증 발행.
*   **데이터 관리**: DB 자동/수동 백업 및 복원, CSV/Excel 데이터 연동.
*   **사용자 설정**: 프로필, 비밀번호 변경, 통화 설정.

## 🏗️ 아키텍처

이 프로젝트는 **Clean Architecture**와 **MVVM(Model-View-ViewModel)** 패턴을 결합하여 확장 가능하고 유지보수가 용이한 구조로 설계되었습니다.

- **Presentation Layer (View)**: Screens & Widgets
- **Application Layer (ViewModel)**: Riverpod Controllers & Business Logic
- **Data Layer (Model)**: Repositories & Data Sources
- **Domain Layer**: Entities (Freezed Models)

> 현재 코드베이스는 빠른 프로토타이핑 과정에서 일부 기술 부채가 발생했으며, 아키텍처 개선을 위한 리팩토링이 계획되어 있습니다. 자세한 내용은 **[코드베이스 아키텍처 분석 보고서](./docs/codebase_analysis.md)**를 참고해 주십시오.

## 🚀 핵심 기술 스택

- **Framework**: Flutter `^3.9.2`
- **State Management**: Riverpod `^2.5.1`
- **Routing**: go_router `^14.2.0`
- **Database**: Drift `^2.17.0` (SQLite ORM)
- **Data Modeling**: Freezed `^2.5.2`
- **Networking**: Dio `^5.5.0`
- **Security**: `local_auth` `^2.2.0`, `flutter_secure_storage` `^9.2.2`
- **UI/UX**: Material 3
- **Document Handling**: `pdf`, `printing`, `excel`, `csv`
- **Asynchronous**: `riverpod_generator`, `build_runner`

## 🛠️ 개발 시작하기

### 사전 요구사항
- Flutter SDK `^3.9.2`
- Dart SDK `^3.9.2`

### 설치 및 실행

```bash
# 프로젝트 디렉토리로 이동
cd renthouse

# 의존성 설치
flutter pub get

# 코드 생성 (필수)
dart run build_runner build --delete-conflicting-outputs

# 앱 실행 (예: Windows 데스크톱)
flutter run -d windows

# 코드 분석
flutter analyze

# 테스트 실행
flutter test
```

## 📝 라이선스

이 프로젝트는 MIT 라이선스 프로젝트입니다.

## 📧 문의

프로젝트 관련 문의사항이 있으시면 youp.han@gmail.com 으로 연락주세요.

---

**UniRent** - 스마트한 임대 관리의 시작
