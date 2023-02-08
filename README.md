# 📋 프로젝트매니저 📋

## 🗒︎ 목차

1. [소개](#-소개)
2. [개발환경 및 라이브러리](#-개발환경-및-라이브러리)
3. [팀원](#-팀원)
4. [타임라인](#-타임라인)
5. [파일구조](#-파일구조)
6. [실행화면](#-실행-화면)
7. [트러블 슈팅 및 고민](#-트러블-슈팅-및-고민)
8. [참고링크](#-참고-링크)

<br>

## 👋 소개

**PAD환경에서 사용 가능한 프로젝트 정보 관리 어플입니다.**

- 프로젝트 기간 : 22.01.09 ~ 23.01.27 (3주)

**[다뤄본 기술]**

- UI를 코드만으로 구성
  - AutoLayout
  - Naviation Controller
  - TableView
- SwiftLint 적용
- MVC 패턴 적용
- Create/Edit/Read 모드별 동작 구현
- Todo/Doing/Done의 데이터 관리 구현
- Realm & FireBase 적용 예정 (현재 미적용)

## 💻 개발환경 및 라이브러리

[![swift](https://img.shields.io/badge/swift-5.6-orange)]()
[![macOS](https://img.shields.io/badge/macOS_Deployment_Target-14.0-blue)]()

<br>

## 🧑 팀원

| Dragon                                                       |
| :----------------------------------------------------------- |
| <img src = "https://i.imgur.com/LI25l3O.png" width=200 height=200> |

<br>

## 🕖 타임라인

| 날짜     | 구현 내용                                                    |
| -------- | ------------------------------------------------------------ |
| 23.01.10 | SwiftLint & Realm & FireBase 적용                            |
| 23.01.12 | TODO & DOING & DONE - 각 테이블뷰 구현                       |
| 23.01.14 | plus(+)버튼의 Action 구현 (프로젝트 정보 작성 페이지 이동)   |
| 23.01.16 | 프로젝트 정보 작성하는 View 구현 및 메인 View의 UI Component 조정 |
| 23.01.17 | TODO & DOING & DONE - 각 테이블뷰 셀 구현<br />사용자가 입력한 프로젝트 정보를 TODO에 저장하는 기능 구현 |
| 23.01.18 | Create & Edit & Read 모드별 동작 구분하는 기능 구현<br />DatePicker를 통해 사용자가 선택한 날짜가 저장되는 기능 구현 <br />프로젝트 정보의 날짜가 지난경우 빨간색으로 표시해주는 기능 구현 <br />TableView Cell을 LongPress하여 TODO -> DOING & DONE 로 데이터 이동 구현 |
| 23.01.19 | Create & Edit & Read 모드별 동작 구분하는 기능 에러 개선<br />NameSpace 정리 & Mark 구분 & 불필요한 코드 정리 |
| 23.01.20 | FireBase 사용으로 인해 필요한 GoogleService-Info.plist를 Git에 업로드되도록 설정 변경 |
| 23.01.25 | MVC 패턴에 맞는 폴더 재구성<br />한 파일에서만 사용되는 NameSpace은 한 파일안에서만 Private로 사용하도록 변경 <br />TableView Cell을 LongPress하여 TODO - DOING - DONE 간 데이터 이동 구현 |
| 23.01.26 | Create & Edit & Read 모드별 동작 구분하는 기능 및 에러 개선<br />Read -> Edit 모드로 변경하기전에 사용자에게 Alert을 통해 확인받도록 기능 구현 |

<br>

## 💾 파일구조

### tree

```bash
[ProjectManager]
│   ├── Resource
│   │   ├── AppDelegate.swift
│   │   ├── Assets.xcassets
│   │   ├── Base.lproj
│   │   │   └── LaunchScreen.storyboard
│   │   └── SceneDelegate.swift
│   └── Source
│       ├── Model
│       │   ├── MainNameSpace.swift
│       │   ├── ProjectData.swift
│       │   └── Protocol
│       │       ├── AlertPresentable.swift
│       │       └── DataSendable.swift
│       └── Scene
│           ├── Add
│           │   ├── AddViewController.swift
│           │   └── View
│           │       └── CustomPopUpView.swift
│           └── Main
│               ├── MainViewController.swift
│               └── View
│                   ├── MainProjectManagerView.swift
│                   ├── MainTableViewCell.swift
│                   └── MainTitleView.swift
└── README.md

```

<br>

## 💻 실행 화면

| ![Simulator Screen Recording - iPad Pro (11-inch) (4th generation) - 2023-01-27 at 15 46 00](https://user-images.githubusercontent.com/102534252/215029196-86be32b0-88ab-40ab-8e3f-bdb92d330934.gif) | ![Simulator Screen Recording - iPad Pro (11-inch) (4th generation) - 2023-01-27 at 15 47 31](https://user-images.githubusercontent.com/102534252/215029271-46ba5102-fde3-4b42-bf0e-e4d9b04e1eef.gif) | ![Simulator Screen Recording - iPad Pro (11-inch) (4th generation) - 2023-01-27 at 15 48 01](https://user-images.githubusercontent.com/102534252/215029281-acdf957c-fdf8-4c9f-b6ba-0c417c1c3d40.gif) |
| :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
|                      TODO에 데이터 저장                      |              TODO-DOING-DONE <br />데이터 이동               |                         데이터 삭제                          |

| ![Simulator Screen Recording - iPad Pro (11-inch) (4th generation) - 2023-01-27 at 15 49 18](https://user-images.githubusercontent.com/102534252/215029289-24ae5ea6-53f6-43fa-946e-940b6f732cb6.gif) | ![Simulator Screen Recording - iPad Pro (11-inch) (4th generation) - 2023-01-27 at 16 14 43](https://user-images.githubusercontent.com/102534252/215029632-4b14cab2-74a1-4291-924e-c73e53410a7f.gif) | ![Simulator Screen Recording - iPad Pro (11-inch) (4th generation) - 2023-01-27 at 15 51 14](https://user-images.githubusercontent.com/102534252/215029497-a870762d-0896-43a9-8b6d-a097edbe5a0a.gif) |
| :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
|                     Read모드 (편집불가)                      |                     Edit모드 (편집가능)                      |                    Create모드 (모드전환)                     |

## 🎯 트러블 슈팅 및 고민

- **MVC 패턴을 기반으로 코드를 작성**
  - 여러 기능들이 올라가면서 점점 Controller에 Code가 쌓이기 시작
    - 이를 해결하기 위해 View와 Model에 역할을 어떻게 분배할지 고민했었습니다.
      - AlertPresent를 통해 Alert 생성하는 모델 생성
      - View에 있는 Component의 설정을 변경하는 메서드는 대부분 View에서 갖고 있도록 변경
- **한 View안에 3개의 TableView를 구현**
  - StackView에 3개의 TableView를 담아 View에 띄우는 방식을 사용
    - 이를 통해 한 View에서도 여러 개의 TableView를 사용할 수 있다는 것을 알게 됨
  - `ContainerViewController` 를 통해서도 구현 가능할 것 같음 (추후 확인 예정)
- **여러 개의 TableView와 여러 개의 Mode를 관리**
  - MainViewController에서는 TableView에 맞는 데이터 관리
  - AddViewController에서는 Mode에 맞는 동작 구현
    - 위 두가지 Enum에 생성된 현재 데이터 위치와 모드를 주고 받으며 동작을 수행하도록 구현
- **Button의 Action 설정은 ViewController에서만 가능한지**
  - 현재 코드에서는 ViewController내에서 Action을 설정해주었음
  - Delegate 패턴을 통해 AddTarget의 메서드를 적용해보는 방법도 가능할 것 같음 (추후 확인 예정)

- **Pod을 사용하여 Install된 파일들을 Git 업로드되지 않도록 관리**
  - .gitignore 파일을 통해 Pod파일 제외하도록 설정 변경

- **FireBase 사용시 `GoogleService-Info.plist`파일 관리도 필요**
  - `GoogleService-Info.plist` 가 없을 경우 Build가 되지 않는 것을 확인
    - Git 에 파일을 업로드할 경우 `GoogleService-Info.plist` 또한 관리를 해줄 것 (공개 or 비공개)


## 📚 참고 링크

**[공식 문서]**

- [List](https://developer.apple.com/documentation/swiftui/list) 
  - [Displaying Data in Lists](https://developer.apple.com/documentation/swiftui/displaying-data-in-lists)
- [Pickers](https://developer.apple.com/design/human-interface-guidelines/ios/controls/pickers/)
  - [DatePicker](https://developer.apple.com/documentation/swiftui/datepicker)
- [popover(isPresented:attachmentAnchor:arrowEdge:content:)](https://developer.apple.com/documentation/swiftui/view/popover(ispresented:attachmentanchor:arrowedge:content:))
- [DateFormatter](https://developer.apple.com/documentation/foundation/dateformatter)
- [Handling Notifications and Notification-Related Actions](https://developer.apple.com/documentation/usernotifications/handling_notifications_and_notification-related_actions)
- [UndoManager](https://developer.apple.com/documentation/foundation/undomanager)
- [Scheduling a Notification Locally from Your App](https://developer.apple.com/documentation/usernotifications/scheduling_a_notification_locally_from_your_app)
- [Localizations](https://developer.apple.com/kr/localization/)
- [ContainerViewController](https://developer.apple.com/documentation/uikit/view_controllers/creating_a_custom_container_view_controller)
