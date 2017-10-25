title=About
date=2013-09-24
type=page
status=published
big=TCUpcoming
summary=SmartDownloaderOverview
nation=ja
~~~~~~
## Upcoming Products > Smart Downloader > Overview

Smart Downloader는 게임 구동시에 게임에 필요한 리소스를 멀티 스레드로 다운로드 해 주는 서비스 입니다.
클라이언트에서 리소스를 다운로드 해주고 여러 통계 데이터를 수집해서 다양한 정보도 제공합니다.

## 주요 기능

### 멀티 스레드 다운로드
- 연결 개수를 네트워크 대역폭을 최대로 활용할 수 있습니다.
- 파일의 개수가 많고 네트워크 환경이 느린 환경(글로벌 환경)에서 유용합니다.

### 갱신된 파일 리스트만 업데이트
- 파일의 사이즈, 체크섬 기반으로 업데이트를 진행합니다.
	- 종종 이미지나 텍스트 파일과 같이 사이즈는 변하지 않고 내용이 변한 파일에 대해서도 (파일의 체크섬은 바뀌기 때문에)업데이트 가능합니다.
- 최초 풀 다운로드 이후에는 증분만 업데이트를 진행합니다.
- 메타파일만 수정해서 코드 수정 없이 게임 리소스 업데이트가 가능합니다. 

### 심플한 메타파일 및 메타파일 생성 툴 지원
- 범용적으로 사용되는 json 형태의 메타파일 기반으로 다운로드를 진행합니다.
- 게임 리소스를 Input / 메타파일을 Output으로 만들어주는 생성 툴을 지원합니다.

### 다운로드 및 업데이트 구현 간소화
- 전체 API가 3개로 API 사용성이 간결합니다.
- 다운로드 진행정보를 상세하게 제공하고 있습니다.
	- 다운로드 결과 정보 제공
	- 각 스레드별 다운로드 정보 제공(파일 이름, 다운로드 받은 용량, 전체 다운로드 받아야 할 용량)
	- 전체 다운로드 진행률
	- 다운로드 속도(bps값으로 제공)
	- 전체 다운로드 받은 용량
	- 전체 다운로드 받아야 할 용량
	- 전체 파일 개수

### 게임 다운로드 통계 데이터 제공
- 다운로드 성공 / 실패 통계를 확인할 수 있습니다.
- 국가별 / 기기별 / OS별 다운로드 통계를 확인할 수 있습니다.
- 검색 기능을 제공 하여 원하는 시간대(게임 배포 전후로)에 다운로드 통계를 확인할 수 있습니다.
- 다음과 같은 Dashboard 화면을 통해서 통계 데이터를 확인 할 수 있습니다.
![a](http://static.toastoven.net/prod_smartdownloader/img_04.png)