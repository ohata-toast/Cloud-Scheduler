# Cloud Scheduler 개요

**Application Service > Cloud Scheduler > 개요**

Cloud Scheduler는 다양한 작업을 원하는 일정에 따라 실행하도록 설정할 수 있는 서비스입니다. 특정 작업을 정해진 일정에 일회성으로 실행하거나 크론(cron) 표현식 또는 간격을 설정하여 반복 실행하도록 할 수 있습니다. 작업은 API 엔드포인트를 통해 설정할 수 있습니다. API 엔드포인트는 사전 설정된 NHN Cloud 서비스뿐만 아니라 다양한 서비스들의 API를 자유롭게 입력할 수 있습니다. NHN Cloud Object Storage의 오브젝트를 복사하는 것과 같은 작업이 Cloud Scheduler를 이용한 작업의 대표적인 예입니다.

Cloud Scheduler에서 설정한 일정은 시작 및 종료 일시를 지정하여 원하는 기간에만 실행할 수 있으며, 실행을 원하지 않을 경우 비활성화하여 손쉽게 실행을 멈출 수 있습니다. 또한 API 호출 실패 등으로 인해 작업이 성공적으로 완료되지 않을 경우 작업을 다시 실행하도록 재시도 정책을 설정할 수도 있습니다.

Cloud Scheduler는 NHN Cloud의 모든 리전에서 사용할 수 있습니다.


![Cloud Scheduler 개요 이미지](https://static.toastoven.net/prod_cloud_scheduler/CloudScheduler_overview_ko_800.png)


<br>
이 문서에서는 NHN Cloud의 Cloud Scheduler 서비스의 주요 기능, 사용하는 방법과 용어를 안내합니다.

## Cloud Scheduler의 주요 기능

* **다양한 실행 유형**
    * 지정한 시점에 한 번만 실행하는 일회성 실행을 지원합니다.
    * Cron 표현식과 Rate 기반의 반복 실행을 지원합니다.
* **편리한 일정 관리**
    * 일정을 활성화/비활성화할 수 있습니다.
    * 일정 실행 이력을 통해 성공 여부, 요청 및 응답 데이터 등의 상세 정보를 파악할 수 있습니다.
    * 일정에 따른 작업 실패 시 재시도 설정을 할 수 있습니다.
* (추후 제공 예정) **NHN Cloud 서비스 연동 지원**
    * NHN Cloud의 다양한 서비스의 기능들을 대상 템플릿으로 제공하여 손쉬운 일정 등록이 가능합니다.
* (추후 제공 예정) **API에 대한 대상 템플릿 작성 가능**
    * NHN Cloud 서비스뿐만 아니라 다양한 API를 직접 입력을 통해 대상 템플릿 작성이 가능합니다.

## Cloud Scheduler 시작하기

* [일정 생성](create-schedule)
* [일정 관리](manage-schedule)

## 용어 정리


| 용어 | 설명 |
| --- | --- |
| 일정 | Cloud Scheduler를 사용하여 만든 리소스로 실행 유형, 대상, 재시도 정책과 같은 추가 설정을 모두 포함한 개념 |
| Cron | 일정한 시간 간격이나 특정 시각에 실행할 수 있도록 하는 유닉스 기반의 잡 스케줄러. Cron 고유의 표현식을 통해 작성함 |