title=About
date=2013-09-24
type=page
status=published
big=TCNotification
summary=SMSRelease
nation=ko
~~~~~~
## Notification > SMS > Release Notes
### 2017.09.21
#### 기능 추가
* [Console, API] 080수신거부 대상자 조회
    * 080수신거부 한 수신자 조회 기능과 API가 추가되었습니다.
    * 자세한 사항은 [[개발자 가이드](./Developer`s Guide/#080)] 참고하시기 바랍니다.

### 2017.08.24
#### 기능 추가
* [Console] 발신번호 승인/반려 안내 메일 발송
    * 발신번호 승인/반려 시 사용자에게 안내 메일을 발송합니다.
* [Console] 080 수신거부 승인/해지 메일 발송
    * 080 수신거부 승인/해지 시 사용자에게 안내 메일을 발송합니다.
* [API] 지원하지 않는 ContentType에 대한 에러 응답 추가
    * API 요청 헤더에 ContentType이 지원하지 않는 값으로 설정된 경우 시스템 에러가 아닌 명확한 에러 형태로 반환되도록 수정되었습니다.

#### 버그 수정
* [Console] 카테고리/템플릿 등록 시 사용여부가 "사용"으로만 저장되는 현상 수정
    * 카테고리/템플릿 등록 시 사용 여부를 "미사용"으로 체크하더라도 "사용"으로 저장되는 버그가 수정되었습니다.

### 2017.04.20
#### 기능 추가
* [API] 080수신거부 서비스 기능 추가
    * 080수신거부 서비스에 가입하여 광고성 SMS를 발송할 수 있습니다. [[개발자 가이드](./Developer`s Guide/#_27)]
    * 가입 관련 자세한 사항은 [[080 수신거부 서비스](./Getting Started/#080)] 참고하시기 바랍니다.

### 2017.03.23
#### 기능 개선/변경
* [Console] 대량 발신 조회 시, 결과 사유 셀렉트 창 그룹화하였습니다.

#### 버그 수정
* [Console] 예약 발송 후 상세 보기 화면 공백으로 나오는 버그 수정하였습니다.


### 2017.02.23
#### 버그 수정
* [Console] MMS 대량 발송 조회 시 발송 건수 오류로 pagination 비정상 작동 버그 수정되었습니다.

### 2017.01.19
#### 기능 개선/변경
* [API] 다수의 수신자 리스트로 발송 시 인원 수 제한 추가되었습니다.
    * AS-IS : 다수의 수신자 리스트 인원 수에 대한 제한이 없음
    * TO-BE : 한 요청에 대한 수신자 리스트 1000명으로 제한

#### 버그 수정
* [Console] 발송 조회에서 필드 내용 클릭시 ellipsis가 필드 오른쪽에 생기는 버그 수정되었습니다.
    * AS-IS : 제목,내용이 긴 경우 ellipsis가 필드 오른쪽에 생김
    * TO-BE : 제목,내용이 길어져도 ellipsis가 해당 필드 위에 정상적으로 생김

### 2016.12.22
#### 기능 개선/변경
* [Console] 발송 요청 실패 건에 대해서 조회할 수 있는 기능 추가되었습니다.
    * AS-IS : SMS, MMS 발송 시, 실패할 경우 실패 응답은 받지만 Console에서 조회할 수 없음
    * TO-BE : SMS, MMS 발송 시, 실패할 경우 요청 상태를 실패로 변경하여 조회할 수 있도록 변경
* [API] 다수의 수신자리스트에게 발송 시 유효성 검사 정상 건만 발송되도록 로직 변경되었습니다.
    * AS-IS : 다수의 수신자 리스트의 발송 요청이 실패했을 경우, 실패한 수신자 이후 수신자는 미발송
    * TO-BE : 모든 수신자에게 발송하며, response에서 수신자별 발송 결과를 제공. 발송 실패가 있어도 요청 결과는 성공. <br/>
    자세한 사항은 [[개발자 가이드](./Developer`s Guide)] 참고하시기 바랍니다.
* 요금 정산 방식 변경되었습니다.
    * AS-IS : 문자 발송 요청 시간을 기준으로 과금
    * TO-BE : 문자 발송 결과를 응답 받는 시간으로 과금



#### 버그 수정
* [API] MMS 첨부파일 발송 시, 존재하지 않은 첨부파일일 경우 서버에러 발생하는 버그 수정되었습니다.
    * AS-IS : 존재하지 않은 첨부파일 아이디로 발송할 경우 서버에러 실패 응답
    * TO-BE : MMS 첨부파일 발송에서 존재하지 않은 첨부파일이 있는 경우 실패 원인을 에러 메시지로 제공함
* [Console] 대량 발송에서 CSV 템플릿 파일 공백 버그 수정되었습니다.
    * AS-IS : CSV 템플릿 파일에서 필드 사이에 ,기준으로 공백이 있는 경우 파싱 오류
    * TO-BE : CSV 템플릿 파일에서 필드 사이에 ,기준으로 공백이 있는 경우 정상 작동

### 2016.12.08
#### 기능 개선/변경
* [Console] 템플릿 기능 개선되었습니다.
    * AS-IS : 템플릿을 삭제할 경우, 해당 템플릿으로 발송한 내역에 템플릿 정보가 표시되지 않음
    * TO-BE : 템플릿을 삭제해도, 해당 템플릿으로 발송한 내역에 템플릿 정보를 볼 수 있다. 단, 삭제한 템플릿 아이디는 재사용 불가능하고 발신 내역에 조회되는 템플릿 내용은 최근 수정한 템플릿 정보로 표시
* [Console] 발신 조회 시, 결과 사유 셀렉트창 개선되었습니다.
    * AS-IS : 결과 사유를 전체로 선택했을 경우, 상세 결과 사유 셀렉트창이 전체로 표시
    * TO-BE : 결과 사유를 전체로 선택했을 경우, 상세 결과 사유 셀렉트창 보이지 않게 수정
* [Console] 발신번호 등록 시, 유효성 검사 강화하였습니다.
    * AS-IS : 중복 검사만 체크
    * TO-BE : 중복검사 + 발신번호 등록 형식 체크 &nbsp;&nbsp;[[발신번호 등록 형식](./Getting Started/#_12)]


#### 버그 수정
* [Console] MMS 템플릿 등록 시, 제목을 입력하지 않아도 등록되는 버그 수정되었습니다.
    * 현상 : MMS 템플릿 등록 시, 제목을 입력하지 않아도 템플릿이 등록됨
    * 해결 : MMS 템플릿 등록 시, 제목 공란 체크 로직 추가

### 2016.11.24
#### 기능 개선/변경
* [Console] 대량 발송 기능 개선되었습니다.
    * 치환 기능 개선: 치환 발송을 할 경우 기존에는 템플릿을 선택했을 경우에만 치환 기능이 적용되었으나 템플릿을 선택하지 않고 제목이나 본문에 치환 키를 입력할 경우 치환되도록 개선
    * 템플릿 파일 업로드 개선: 엑셀과 같은 일부 편집기에서 편집 이력이 있는 셀의 경우 셀 데이터가 없을 경우에도 빈 문자열 데이터가 포함되어 저장됨. 입력 범위 밖의 빈 문자열의 경우 템플릿 파일 업로드 시 유효성 검사에서 무시하도록 변경
    * 유의 안내 문구 추가: 엑셀과 같은 일부 편집기에서 CSV 템플릿 파일을 작성할 경우 유니코드 정보가 저장되지 않아 문자가 깨지는 이슈가 있음. 해당 이슈에 대한 내용을 템플릿 다운로드와 발송 예약 시 유의 안내 문구 표시

#### 버그 수정
* [Console] 대량 발송 페이지 오류 수정되었습니다.
    * 이벤트 오류 수정: 요청 리스트의 헤더를 클릭할 경우 '발송 요청 건을 선택 후 조회할 수 있습니다.' alert 가 표시되는 오류 수정

### 2016.10.20
#### 기능 개선/변경
* [Console] 대량 업로드 발송 기능 개선되었습니다.
    * 대량 업로드 발송 CSV 포맷 지원 : 기존 대량 업로드 발송시 엑셀 파일 뿐만 아니라 CSV파일을 통해서도 발송 할 수 있도록 확장 (CSV 템플릿 제공)
    * 선택적 대상자 확인 프로세스: 기존 대량 업로드 발송시 대상자 확인 후 발송 할 수 있었던 프로세스에서 선택적으로 대상자를 확인 할 수 있도록 개선
    * 대량 업로드 발송 파일 validation 강화 : 대량 업로드 발송시 파일에 잘못된 포맷의 수신자 번호 입력 또는 누락된 데이터가 있는지 오류를 확인 해주는 기능이 추가
    * 대량SMS발송 탭 추가 : 대량 업로드 발송시 대상자 확인과 발송 진행 상태를 확인 할 수 있는 대량SMS발송 탭이 추가
    * 참고 : Notification > SMS > Getting Started > 대량 업로드 발송
* [Console] SMS 요청별 조회 탭에서 결과 사유 셀렉트 창 그룹화로 변경되었습니다.
    * 참고 : Notification > SMS > Getting Started > SMS 요청별 조회
* [API] SMS 발송 API request body 본문 내용 공란일 경우 발송 실패로 변경되었습니다.
    * AS-IS : 공란일 경우 Response는 성공이지만, 실제로 내용이 없기 때문에 미발송. 조회 시, 메시지 형식 오류로 표시됨
    * TO-BE : 공란일 경우 본문 내용이 없다는 내용과 함께 응답 실패

#### 버그 수정
* [Console] 파이어폭스 브라우저에서 SMS 발송 후 비정상 작동 수정되었습니다.
    * 현상 : 발송 후, 발신번호 셀렉트 창에서 선택이 되지 않거나, 필드 초기화 되지 않는 이슈
    * 해결 : 발송 후, 필드 초기화 및 정상적으로 동작하도록 수정

### 2016.09.29
#### 기능 개선/변경
* [Console] SMS 웹 페이지에서 발송 시, 수신자 번호 입력란에 국가 코드가 포함된 수신자 번호로 발송 가능하도록 수정되었습니다.
    * 참고 : Notification > SMS > Getting Started > 일반 SMS 발송, 일반 LMS 발송, MMS 발송

#### 버그 수정
* [API] SMS 발송 조회 API response 값 중 userId 항목에 항상 null값이 응답하는 버그 수정되었습니다.
    * 현상 : SMS 발송 조회 API response 값 중 userId 항목에 항상 null값이 응답하는 현상.
    * 해결 : SMS 발송 조회 API response 값 중 userId 항목이 정상적인 데이터로 응답.
* [API] 인증용 SMS 단일 발송 조회 API response 값 중 sendType 항목에 비정상 데이터로 응답하는 버그 수정되었습니다.
    * 현상 : 인증용 SMS 단일 발송 조회 API response 값 중 sendType이 SMS 타입인 0인 문제.
    * 해결 : 인증용 SMS 단일 발송 조회 API response 값 중 sendType이 정상적인 데이터 2로 응답. (0:SMS, 1:MMS, 2:Auth)

### 2016.08.18
#### 기능 개선/변경
* [API] 국가 코드가 포함된 수신자 번호 입력 필드 추가되었습니다.
    * 참고 : Notification > SMS > Developer's Guide > [단문 SMS 발송, 장문 MMS 발송, 인증용 SMS 발송] API 명세서 (internationalRecipientNo 필드 추가)

#### 버그 수정
* [Console] SMS 템플릿 사용여부 변경이 정상적으로 안되는 문제 수정되었습니다.
    * 현상 : 사용여부를 사용/미사용 변경하더라도 다시 템플릿 호출 시 정상적으로 반영되지 않는 현상
    * 해결 : 사용여부 필드가 정상적으로 저장 및 노출되도록 수정

### 2016.08.04
#### 버그 수정
* [API] SMS 발신번호가 핸드폰 인증으로 등록된 경우 MMS 발송이 안되는 버그 수정되었습니다.
    * 현상 : 핸드폰 인증으로 저장되는 발신번호가 국제번호 형태(82-1x-xxxx-xxxx)로 저장이 되며, 이로인해 MMS 발송이 안되는 문제가 있음
    * 해결 : 국제번호로 저장되던 방식을 대한민국 핸드폰 번호 형태(01x-xxxx-xxxx)로 변경하여 저장되도록 수정
* [API] countryCode 공백으로 입력 시 문자 발송이 안되는 버그 수정되었습니다.
    * 현상 : countryCode에 빈 값(null, "") 전송 시 응답은 성공으로 노출되나 정상적으로 발송이 안되는 현상
    * 해결 : countryCode에 빈 값이 넘어올 경우 국가 번호 82가 기본적으로 설정되도록 수정
