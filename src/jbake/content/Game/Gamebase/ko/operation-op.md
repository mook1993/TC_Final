title=About
date=2013-09-24
type=page
status=published
big=TCGame
summary=TCGamebaseOpOp
nation=ko
~~~~~~
## Game > Gamebase > Operator Guide > Operation

앱 운영시 필요한 기능들을 제공하는 메뉴입니다.

*   점검(Maintenance) : 앱 점검을 관리
*   공지(Notice) : 사용자에게 팝업형태로 제공하는 긴급공지를 관리

## Maintenance

![image alt](http://static.toastoven.net/prod_gamebase/Operators_Guide/Console_Maintenance1_1.1.png)

게임 점검이 필요한 경우 Console화면을 통하여 손쉽게 등록이 가능합니다.
등록한 앱 점검 내역 조회와 점검 등록 내용 및 진행상태 등을 한 눈에 확인할 수 있으며 등록된 점검사유로 점검 검색이 가능합니다.
점검 상태는 아래와 같이 다섯 가지로 구분되어 관리됩니다.

(1) 예약중 : 점검이 진행될 예정
(2) 점검중 : 현재 점검 진행중
Gamebase에서 기본으로 제공하는 점검팝업 ![image alt](http://static.toastoven.net/prod_gamebase/Operators_Guide/Console_Maintenance_popup_1.0.png) Gamebase에서 기본으로 제공하는 점검페이지(점검사유와 점검시간 표시) ![image alt](http://static.toastoven.net/prod_gamebase/Operators_Guide/Console_Maintenance_webview_1.1.png) (3) 종료 : 점검시간 종료
(4) 점검해제 : 점검이 진행중인 상태에서 운영자가 '점검해제'를 한 경우
(5) 점검 해제(기한만료) : '점검해제' 상태에서 점검시간이 종료되는 경우

### Register Maintenance

점검 메인화면에서 '등록'버튼을 클릭하면 점검을 등록하는 화면으로 이동합니다.

![image alt](http://static.toastoven.net/prod_gamebase/Operators_Guide/Console_Maintenance2_1.3.png)

> <font color="red">[WARNING]</font> **업데이트 필수와 점검이 동시에 설정**되어 있을 경우 서비스 상태는 '업데이트 필수'로 Client에 내려가게 됩니다.
> 점검 진행 도중 사용자에게 업데이트 필수 팝업 노출을 원하지 않는 경우에는 점검 완료 이후에 서비스 상태를 '업데이트 필수'로 변경해야 합니다.

#### (1) 대상

점검을 진행할 대상을 선택합니다.

*   전체 게임 : 모든 클라이언트 버전에 점검이 필요한 경우 선택합니다.
*   일부 클라이언트 : 특정 클라이언트 버전에만 점검이 필요한 경우 선택합니다. '버전 선택'버튼을 클릭하면 클라이언트 메뉴에서 등록한 클라이언트 버전리스트가 출력됩니다.
    **[일부 클라이언트 선택 화면 예시]**
    클라이언트 상태 및 스토어별 전체 선택이 가능하며, 점검을 원하는 클라이언트 버전을 선택 후 확인 버튼을 누르면 됩니다.
    ![image alt](http://static.toastoven.net/prod_gamebase/Operators_Guide/Console_Maintenance4_1.3.png)

#### (2) 점검 시간

점검이 진행될 시간을 설정합니다.
Timezone의 경우 기본적으로 'UTC+09:00'이 선택되어 있으며, 서비스하는 국가의 시간대를 선택하여 점검을 등록하는 것도 가능합니다.

#### (3) 점검 사유

점검 진행중에 사용자에게 노출할 메시지를 설정합니다.
다국어 지원을 위해 여러개의 언어로 등록 가능하며, 입력한 언어 이외의 언어를 사용하는 사용자에게는 기본 언어로 선택된 언어가 노출됩니다. 오른쪽의 **'+'**버튼을 클릭하면 언어 추가가 가능하며 원하는 언어가 없는 경우 담당자에게 연락을 주시면 새로운 언어 추가가 가능합니다.

#### (4) 점검 페이지 URL

유저에게 노출할 점검 페이지를 설정합니다.

*   사용하지 않음 : Gamebase에서 제공하는 기본 점검페이지를 사용합니다.

*   사용 : 게임에서 만든 점검페이지 URL을 입력합니다.

### Modify Maintenance

![image alt](http://static.toastoven.net/prod_gamebase/Operators_Guide/Console_Maintenance3_1.1.png)

등록한 점검의 상세내용을 확인하고 수정, 삭제가 가능합니다.
기본적으로 입력 항목은 등록 화면과 동일하며, 점검을 잘못 등록하였을 때 삭제버튼을 통하여 점검 삭제도 가능합니다.
유사한 내용으로 점검을 다시 등록하고자 하는 경우 복사기능을 통하여 점검을 쉽게 등록 하실 수 있습니다.

## Notice

![image alt](http://static.toastoven.net/prod_gamebase/Operators_Guide/Console_Notice1_1.2.png)

앱 실행시 팝업 형태로 노출되는 공지를 제공합니다. 로그인 이전에 노출되는 팝업이므로 외부 인증 장애나 게임 서버 장애가 발생한 경우 등록하여 사용하면 됩니다.
등록된 공지리스트와 진행상태 등을 한눈에 확인 가능하며 공지메시지로 검색도 가능합니다.
공지 상태는 아래와 같이 세 가지로 구분되어 관리됩니다.

(1) 예정 : 공지가 노출될 예정
(2) 노출중 : 공지 노출중
(3) 완료 : 공지 노출시간 종료

### Register Notice

공지 메인화면에서 '등록'버튼을 클릭하면 공지를 등록하는 화면으로 이동합니다.

![image alt](http://static.toastoven.net/prod_gamebase/Operators_Guide/Console_Notice2_1.0.png)

#### (1) 대상

공지를 노출할 대상을 선택합니다.

*   전체 게임 : 모든 클라이언트 버전에 점검이 필요한 경우 선택합니다.
*   일부 클라이언트 : 특정 클라이언트 버전에만 점검이 필요한 경우 선택합니다. '버전 선택'버튼을 클릭하면 클라이언트 메뉴에서 등록한 클라이언트 버전리스트가 출력됩니다.
    **일부 클라이언트 선택 화면 예시**
    클라이언트 상태 및 스토어별 전체 선택이 가능하며, 점검을 원하는 클라이언트 버전을 선택 후 확인 버튼을 누르면 됩니다.
    ![image alt](http://static.toastoven.net/prod_gamebase/Operators_Guide/Console_Maintenance4_1.3.png)

#### (2) 대상 국가

공지를 노출할 국가를 선택합니다.

*   전체 국가 : 모든 사용자에게 노출
*   일부 국가 : 선택한 국가의 사용자에게만 공지 노출.
    추가하고자 하는 국가코드를 입력하면 자동으로 완성되어 입력됩니다. 입력하고자 하는 국가코드가 없는 경우 관리자에게 문의바랍니다.

> [INFO]
> 국가 판단 기준
> 사용자의 **USIM 국가코드** 기준으로 판단하며 USIM이 없을 경우 **Device**에 설정되어 있는 국가를 기준으로 공지가 노출됩니다.

#### (3) 노출 횟수

공지가 사용자에게 노출되는 회수를 선택합니다.

*   기간 중 1회 노출 : 노출기간 중 1회 노출
*   앱 시작할때마다 항상 노출 : 노출기간 중 사용자가 앱을 실행할 때마다 공지를 노출

#### (4) 노출 시간

공지가 노출될 시간을 설정합니다.
Timezone의 경우 기본적으로 'UTC+09:00'이 선택되어 있으며, 서비스하는 국가의 시간대를 선택하여 점검을 등록하는 것도 가능합니다.

#### (5) 노출 메시지

사용자에게 노출할 공지메시지를 입력합니다.
다국어 지원을 위해 여러개의 언어로 등록 가능하며, 입력한 언어 이외의 언어를 사용하는 사용자에게는 기본 언어로 선택된 언어가 노출됩니다. 오른쪽의 **'+'**버튼을 클릭하면 언어 추가가 가능하며 원하는 언어가 없는 경우 담당자에게 연락을 주시면 새로운 언어 추가가 가능합니다.

#### (6) 하단 버튼 타입

공지 팝업 하단에 노출될 버튼의 타입을 지정합니다.

*   닫기 : 닫기 버튼만 노출.
    '닫기'버튼 클릭하면 팝업을 닫고 게임을 진행합니다.

*   닫기+자세히 보기 : '닫기'와 '자세히보기' 버튼을 노출.
    사용자가 '자세히보기' 버튼을 클릭하면 Console에서 입력한 링크를 웹뷰로 오픈합니다.

#### 긴급공지 팝업 예시

(1) 닫기버튼 ![image alt](http://static.toastoven.net/prod_gamebase/Operators_Guide/Console_Notice_popup_close_1.1.png) (2) 닫기+자세히보기 ![image alt](http://static.toastoven.net/prod_gamebase/Operators_Guide/Console_Notice_popup_close_detail_1.0.png)

### Modify Notice

![image alt](http://static.toastoven.net/prod_gamebase/Operators_Guide/Console_Notice3_1.1.png)

등록한 공지의 상세내용을 확인하고 수정, 삭제가 가능합니다.
기본적으로 입력 항목은 등록 화면과 동일하며, 공지를 잘못 등록하였을 때 삭제버튼을 통하여 공지 삭제도 가능합니다.
유사한 내용으로 점검을 다시 등록하고자 하는 경우 복사기능을 통하여 공지를 쉽게 등록 하실 수 있습니다.