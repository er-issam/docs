---

copyright:
  years: 2017
lastupdated: "2017-04-13"

---


{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}

# API 관리
{: #manage_apis}

API Management 시스템에서 관리하고 모니터하도록 API를 통합한 후 API 설정을 보고 수정할 수 있습니다. API를 통합하지 않은 경우 [{{site.data.keyword.openwhisk_short}} 조치에서 API 작성](manage_openwhisk_apis.html)의 프로시저를 완료하여 통합해야 합니다. 

API의 설정을 관리하려면 다음 단계를 완료하십시오.

새 API를 작성했고 이 API가 인터페이스에서 이미 열려 있는 경우 처음 세 단계를 건너뛸 수 있습니다.

1. API의 정보가 아직 표시되지 않은 경우 {{site.data.keyword.openwhisk_short}} 서비스 대시보드에서 조치를 선택하여 관리할 API를 선택하십시오.
2. 필요한 경우 **API** 탭을 선택하십시오.
3. 필요한 경우 관리할 API를 선택하십시오. 연결이 설정되면 다음 선택사항을 보고 업데이트할 수 있습니다.
    * 요약
    * 정의
    * 공유
    * API 탐색기
4. 관리 API 표시 슬라이더를 선택하여 활성화하고 API를 표시하십시오. 참고: API가 표시되지 않으면 일부 설정을 설정할 수 없습니다.  

## API 설정 요약
{: #overview_api}

요약 탭은 API를 선택한 경우 기본적으로 선택되어 있으며 두 섹션으로 분할되어 있습니다.
* 특성 - 특성 섹션에서 다음 정보를 볼 수 있습니다.
    * API에 대한 기본 정보
	* 보안 정책
	* 비율 한계 정보
    * 공유 세부사항
* 분석 및 로깅 섹션 - 분석 및 로깅 섹션에서 다음 통계를 볼 수 있습니다.
	* 지정된 마지막 시간 간격 동안의 응답 수와 평균 응답 시간
    * 그래프 형식의 분당 API 호출 수
    * 응답 로그 테이블의 마지막 100개의 응답
	
*응답* 그래프는 API가 수신한 응답 수와 응답 상태 분류를 간단하게 표시합니다. 이렇게 하면 대부분의 오류 응답을 수신하는지 여부를 판별할 수 있습니다. 대부분의 오류 응답은 비율 설정에서 허용한 트래픽보다 많은 트래픽이 있음을 표시합니다. 정보 아이콘 위에 마우스를 올려 응답 코드별로 응답의 숫자 분류를 볼 수 있습니다. 다음 응답 코드가 일반적입니다.
* 200  OK
* 201 Created

* 302  Found
* 304  Not Modified
* 400  Bad Request
* 401  Unauthorized
* 403  Forbidden
* 500  Internal Server Error
* 503  Service Unavailable

응답 로그 테이블에는 마지막 100개의 응답에 대한 개별 세부사항이 있습니다. 열 표제를 선택하여 열의 항목에 따라 정보를 정렬할 수 있습니다. *응답 검색* 표시줄을 사용하여 응답 로그 테이블에서 특정 항목을 검색할 수 있습니다. 이벤트를 선택하거나 항목 옆의 옵션 메뉴(세 개의 세로 점) 목록에서 **세부사항 보기**를 선택하여 이벤트에 대한 추가 정보를 사용할 수 있습니다.


## API 설정 편집
{: #settings_api}

**정의** 탭에서 API에 대한 기본 정보를 업데이트할 수 있습니다. 이 정보에는 문서, 이름 및 기본 URL이 포함됩니다. 보안 및 비율 제한 섹션을 사용하여 초, 분 또는 시간당 특정 양의 호출만 이루어지도록 호출 및 간격 한계를 지정하십시오. 또한 데이터의 불필요한 사용을 방지하거나 API에 대한 통계를 수집하기 위해 인증 시 API 호출을 작성해야 합니다.

API 설정을 변경하려면 다음 단계를 완료하십시오.

1. API Management 대시보드에서 **정의** 탭을 클릭하십시오.
2. API의 이름을 지정하거나 업데이트할 수 있고 API 정보 섹션에 API 정의를 가져올 수 있습니다.
3. 보안 및 비율 제한 섹션에서 다음 정책을 업데이트할 수 있습니다.
    * API 키 필요 - 올바른 API 키가 제공되는 경우에만 API 호출을 처리할지 여부를 지정합니다. 기본 설정에는 추가 키가 필요하지 않습니다.
    * 보안 방법 - API 키 옵션을 선택한 경우 API 처리에 API 키만 필요한지 아니면 API 키와 API 시크릿이 둘 다 필요한지를 지정합니다.
    * API 키와 시크릿의 위치 - 방법 설정에 따라 API 보안 정보를 호출에 포함하는 방법을 지정합니다. 호출 이름은 보안 정보 식별 방법을 지정합니다.
    * API 호출 비율 제한 - 각 키에 설정하는 옵션을 사용하여 지정된 시간 간격 동안 허용되는 API 호출 수를 설정합니다. 비율 제한 방법의 버스트 유형이 사용됩니다. API 호출의 평균 비율은 비율에 지정한 총 시간 간격에서 계산됩니다. 간격 동안의 API 호출 비율이 평균 API 호출 비율을 초과하면 비율에 지정한 시간 한계까지가 거부된 호출의 기간이 될 수 있습니다.   
    * OAuth 제공자 - 올바른 보안 매개변수를 가진 사용자가 Google, Facebook, IBM 및 GitHub와 같은 제공자의 소셜 로그인 신임 정보를 통해 OAuth를 적용하여 API에 액세스할 수 있도록 합니다.
4. CORS 사용 - CORS(Cross-origin requests)는 다른 도메인에서 제한된 일부 요청을 사용합니다.
5. **저장**을 클릭하십시오.

## API 공유
{: #share_api}

{{site.data.keyword.Bluemix_notm}} 조직의 내부 또는 외부에서 다른 사용자와 API를 공유할 수 있습니다.

{{site.data.keyword.Bluemix_notm}} 조직의 내부 또는 외부에서 다른 사용자와 API를 공유하는 경우 API의 키를 작성할 수 있습니다. 각 관리 API는 작성할 수 있고 API에 지정할 수 있는 5개의 키를 지원합니다. 개인 또는 회사로 고유 키를 보내 API 사용 방법에 대한 몇 가지 통계를 추적할 수 있습니다. 예를 들어, 해당 사용자 또는 회사에서 API에 대한 호출 또는 수를 추적할 수 있습니다.

키를 사용 안함으로 설정하거나 키로부터의 호출을 제한할 수 있습니다. 이는 테스트, 워크로드 밸런싱, 수익화 또는 일부 보안 상황 해결에 유용합니다.  

1. API Management 대시보드에서 **공유** 탭을 클릭하십시오.
2. "{{site.data.keyword.Bluemix_notm}} 조직 내 공유" 영역 내에서 {{site.data.keyword.Bluemix_notm}} 조직에 대한 액세스 권한을 가진 다른 사용자가 API를 사용할 수 있게 하려면 **내 Bluemix 조직의 모든 사용자와 API 공유**를 선택하십시오. 선택해야 키를 생성할 수 있습니다.
3. **API 키 작성**을 클릭하여 API의 고유 키를 작성하십시오. API 키 작성 대화 상자가 표시됩니다. API 키는 자동으로 생성됩니다.
4. API 키를 사용하여 사용자에게 고유 키를 보내 API에 액세스하는 사용자를 판별하십시오. 게이트웨이는 호출을 생성하는 키(및 고객)를 판별할 수 있습니다.
5. 키 옆의 **메뉴** 아이콘(세 개의 세로 점)을 클릭하여 API 키를 편집하거나 삭제하십시오.

{{site.data.keyword.Bluemix_notm}} 조직 외부에서 공유 섹션에서 {{site.data.keyword.Bluemix_notm}} 계정이 없는 사용자와 API를 공유할 수 있습니다. 이 공유 방법은 API 탐색기에서 API에 대한 정보를 보기 위한 직접 링크를 제공합니다. API에는 API 탐색기 보기에서 API를 실행하기 위한 단추가 있습니다. API에 대한 링크를 요청하려면 다음 단계를 완료하십시오.

1. "{{site.data.keyword.Bluemix_notm}} 조직 외부에서 공유" 섹션 내에서 **API 키 작성**을 클릭하십시오. API 키 작성 대화 상자가 표시됩니다.
사용자에게 제어할 수 없는 시크릿이 있습니다.
2. API 키의 공유 이름을 제공하십시오.
3. **키 작성**을 선택하십시오. 
4. {{site.data.keyword.Bluemix_notm}} 계정이 없는 고객에게 API 포털 링크를 보내십시오. API 키 및 시크릿(사용되는 경우)이 링크에 포함되어 있으므로 링크를 생성한 키를 판별할 수 있습니다.
  
API 문서 링크는 **API 탐색기** 탭에서 API를 엽니다.

## API 탐색기를 사용한 보기 및 테스트
{: #explore_api}

Swagger 문서에서 생성된 html을 보려면 API 탐색기 탭을 선택하십시오. 

API 탐색기는 API에 적용되는 모든 API 조치 및 문서를 표시합니다. 오퍼레이션 및 조치, 해당 설명을 보고 UI에서 API를 테스트할 수 있습니다. 또한 Swagger 문서를 다운로드하여 해당 컨텐츠를 재사용할 수 있습니다.

API를 테스트하려면 다음 단계를 완료하십시오.
1. *예제*가 기본적으로 선택되어 있습니다. 이는 선택된 API의 코드 예를 표시합니다.
2. 필요한 경우 지정된 언어 옆에 있는 메뉴에서 언어를 선택하여 예제 형식을 변경하십시오. 
3. **시도**를 선택하십시오.
4. **오퍼레이션 호출**을 선택하십시오. 

요청에 대한 응답이 표시됩니다.   