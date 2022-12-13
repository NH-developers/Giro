# Giro
지로/공과금 API
## 1 소개  
### 1.1 지로/공과금
전자납부번호로 전기/상하수도 요금을 조회하고 납부하는 서비스입니다.
#### 1.1.1 지로/공과금 NH API 목록
| 전문명 | API |
|:---:|:---:|
| 전기요금 납부 선조회 |	InquireElectricityFarePayment |
| 전기요금 납부	| ElectricityFarePayment |
| 전기요금 납부내역 조회	| InquireElectricityFarePaymentHistory |
| 상하수도요금 납부 선조회	| InquireSewageFarePayment |
| 상하수도요금 납부	| SewageFarePayment |
| 상하수도요금 납부내역 조회 |	InquireSewageFarePaymentHistory |

## 2 resource url
#### 2.1 전기요금 납부 선조회
https://developers.nonghyup.com/InquireElectricityFarePayment.nh
#### 2.2 전기요금 납부
https://developers.nonghyup.com/ElectricityFarePayment.nh
#### 2.3 전기요금 납부내역 조회
https://developers.nonghyup.com/InquireElectricityFarePaymentHistory.nhh
#### 2.4 상하수도 납부 선조회
https://developers.nonghyup.com/InquireSewageFarePayment.nh 
#### 2.5 상하수도 납부 
https://developers.nonghyup.com/SewageFarePayment.nh
#### 2.6 상하수도 납부내역 조회
https://developers.nonghyup.com/InquireSewageFarePaymentHistory.nh


## 3 example
### 3.1.1 전기요금 납부 선조회 Request example
```json
{
    "Header": {
        "ApiNm": "InquireElectricityFarePayment",
        "Tsymd": "20191212",
        "Trtm": "112428",
        "Iscd": "000013",
        "FintechApsno": "001",
        "ApiSvcCd": "13E_001_00",
        "IsTuno": "9832749832",
        "AccessToken": "10b74dd7f5f0f521ecdc7ade82f793bdfc119c3635d2e5303ae6aba0c93d4246"
    },
    "ElecPayNo": "0606628088",
    "Acno": "3020000000071"
}
```
### 3.1.2 전기요금 납부 선조회 Request Element
| Element |	한글명 | Type |	Length |	optional |	Description |  
|:---|:---:|:---:|:---:|:---:|:---|  
| Header || 공통부 |||||	  	
| ElecPayNo |	전자납부번호 |	필드 |	17 |	필수 |	테스트에서는 '0606628088' 고정값으로 입력 |
| Acno |	계좌번호 |	필드 |	20 |	필수 |	테스트에서는 '3020000000071' 고정값으로 입력 |
### 3.1.3 전기요금 납부 선조회 Response example
```json
{
    "Header": {
        "Trtm": "154658",
        "Rsms": "정상처리되었습니다.",
        "ApiNm": "InquireElectricityFarePayment",
        "IsTuno": "20191010155501000008",
        "Tsymd": "20191010",
        "FintechApsno": "001",
        "Iscd": "000013",
        "Rpcd": "00000",
        "ApiSvcCd": "13E_001_00"
    },
    "ElecPayNo": "0606628088",
    "MmbrFlnm": "이희준",
    "PbtxGroNo": "0420007",
    "PbtxBrnNm": "부여지사",
    "CustInqNo": "19014601060662808823",
    "TaxtYm": "201909",
    "Tram": "9230",
    "PbtxPayExdt": "20191031",
    "NtfFrmt": "0",
    "IssShp": "4",
    "ETC": "01",
    "PbtxTmpmDsnc ": "A"
}
```
### 3.1.4 전기요금 납부 선조회 Response Element
| Element |	한글명 | Type |	Length |	optional |	Description |  
|:---|:---:|:---:|:---:|:---:|:---|  
| Header || 공통부 |||||	 
| ElecPayNo |	전자납부번호 |	필드 |	17 |	필수 |	 
| MmbrFlnm |	회원성명 |	필드 |	30 |	필수 |	 
| PbtxGroNo |	공과금 지로번호 |	필드 |	7 |	필수 |	 
| PbtxBrnNm |	공과금 지사명 |	필드 |	16 |	필수 |	 
| CustInqNo |	고객조회번호 |	필드 |	20 |	필수 |	 
| TaxtYm |	과세년월 |	필드 |	6 |	필수 |	 
| Tram |	납부금액 |	필드 | 12 |	필수 |	 
| PbtxPayExdt |	공과금  납부기한 |	필드 |	8 |	필수 |	 
| NtfFrmt |	고지형태 |	필드 |	1 |	필수 |	 
| IssShp |	발행형태 |	필드 |	1 |	필수 |	 
| Etc |	기타 |	필드 |	2 |	필수 |	 
| PbtxTmpmDsnc |	공과금 납기구분 |	필드 |	1 |	필수 |	 

### 3.2.1 전기요금 납부 Request example
```json
{
    "Header": {
        "ApiNm": "ElectricityFarePayment",
        "Tsymd": "20191212",
        "Trtm": "112428",
        "Iscd": "000013",
        "FintechApsno": "001",
        "ApiSvcCd": "13E_001_00",
        "IsTuno": "123324324",
        "AccessToken": "10b74dd7f5f0f521ecdc7ade82f793bdfc119c3635d2e5303ae6aba0c93d4246"
    },
    "PbtxGroNo": "0420007",
    "ElecPayNo": "0606628088",
    "CustInqNo": "19014601060662808823",
    "TaxtYm": "201909",
    "NtfFrmt": "0",
    "IssShp": "4",
    "Etc": "01",
    "Tram": "9230",
    "Acno": "3020000000071",
    "Tlno": "01012345678",
    "MmbrRrno": "9912311234567",
    "PryFlnm": "홍길남",
    "TrSbjcSrchNm": "주택관리공단"
}
```
### 3.2.2 전기요금 납부 Request Element
| Element |	한글명 | Type |	Length |	optional |	Description |  
|:---|:---|:---:|:---:|:---:|:---|  
| Header || 공통부 |||||	  	
| PbtxGroNo |	공과금 지로번호 |	필드 |	7 |	필수 |	납부선조회 응답의 " PbtxGroNo " 값테스트에서는 '0420007' 고정값으로 입력 |
| ElecPayNo |	전자납부번호 |	필드 |	17 |	필수 |	납부선조회 응답의 " ElecPayNo " 값테스트에서는 '0606628088' 고정값으로 입력 |
| CustInqNo |	고객조회번호 |	필드 |	20 |	필수 |	납부선조회 응답의 " CustInqNo " 값테스트에서는 '19014601060662808823' 고정값으로 입력 |
| TaxtYm |	과세년월 |	필드 |	6 |	필수 |	납부선조회 응답의 " TaxtYm " 값테스트에서는 '201909' 고정값으로 입력 |
| NtfFrmt |	고지형태 |	필드 |	1 |	필수 |	납부선조회 응답의 " NtfFrmt " 값테스트에서는 '0' 고정값으로 입력 |
| IssShp |	발행형태 |	필드 |	1 |	필수 |	납부선조회 응답의 " IssShp " 값테스트에서는 '4' 고정값으로 입력 |
| Etc |	기타 |	필드 |	2 |	필수 |	납부선조회 응답의 " Etc " 값테스트에서는 '01' 고정값으로 입력 |
| Tram |	거래금액 |	필드 |	15 |	필수 |	납부선조회 응답의 " Tram " 값테스트에서는 '9230' 고정값으로 입력 |
| Acno |	계좌번호 |	필드 |	20 |	필수 |	테스트에서는 '3020000000071' 고정값으로 입력 | 
| Tlno |	전화번호 |	필드 |	13 |	필수 |	테스트에서는 '01012345678' 고정값으로 입력 |
| MmbrRrno |	회원 주민/사업자번호 |	필드 |	13 |	필수 |	개인계좌이면 '주민등록 번호' , 사업자계좌이면 '사업자번호' 를 입력 ※사업자번호인경우 10자리테스트에서는 '9912311234567' 고정값으로 입력 |
| PryFlnm |	납부자성명 |	필드 |	10 |	필수 |	테스트에서는 '홍길남' 고정값으로 입력 |
| TrSbjcSrchNm |	거래기록사항 |	필드 |	12 |	필수 |	입금 정보 입력(최대 한글 6자) 테스트에서는 '주택관리공단' 고정값으로 입력 |
### 3.2.3 전기요금 납부 Response example
```json
{
    "Header": {
        "Trtm": "154658",
        "Rsms": "정상처리되었습니다.",
        "ApiNm": "ElectricityFarePayment",
        "IsTuno": "20190110155501000018",
        "Tsymd": "20190110",
        "FintechApsno": "001",
        "Iscd": "000013",
        "Rpcd": "00000",
        "ApiSvcCd": "13E_001_00"
    },
    "Rpcd ": "000",
    "InstClasCd ": "72",
    "PbtxGroNo ": "0420007",
    "ElecPayNo ": "0606628088",
    "PmntYmd ": "20190110",
    "PryFlnm ": "홍길남"
}
```
### 3.2.4 전기요금 납부 Response Element
| Element |	한글명 | Type |	Length |	optional |	Description |  
|:---|:---:|:---:|:---:|:---:|:---|  
| Header || 공통부 |||||	 
| Rpcd |	응답코드 |	필드 |	3 |	필수 |	 
| InstClasCd |	기관분류코드 |	필드 |	2 |	필수 |	 
| PbtxGroNo |	공과금 지로번호 |	필드 |	7 |	필수 |	 
| ElecPayNo |	전자납부번호 |	필드 |	17 |	필수 |	 
| PmntYmd |	납부일자 |	필드 |	8 |	필수 |	 
| PryFlnm |	납부자성명 |	필드 |	10 |	필수 |	

### 3.3.1 전기요금 납부내역조회 Request example
```json
{
    "Header": {
        "ApiNm": "InquireElectricityFarePaymentHistory",
        "Tsymd": "20191212",
        "Trtm": "112428",
        "Iscd": "000013",
        "FintechApsno": "001",
        "ApiSvcCd": "13E_001_00",
        "IsTuno": "1232112131233213123",
        "AccessToken": "10b74dd7f5f0f521ecdc7ade82f793bdfc119c3635d2e5303ae6aba0c93d4246"
    },
    "ElecPayNo": "0606628088",
    "PageNo": "1",
    "Insymd": "20191010",
    "Ineymd": "20191010"
}
```
### 3.3.2 전기요금 납부내역조회 Request Element
| Element |	한글명 | Type |	Length |	optional |	Description |  
|:---|:---|:---:|:---:|:---:|:---|  
| Header || 공통부 |||||	  	
| ElecPayNo |	전자납부번호 |	필드 |	17 |	필수 |	미입력 시 기간 내 납부내역 전체 조회테스트에서는 '0606628088' 고정값으로 입력 |
| PageNo |	페이지번호 |	필드 |	4 |	필수 |	Default : 1테스트에서는 '1' 고정값으로 입력 |
| Insymd |	조회시작일자 |	필드 |	8 |	필수 |	YYYYMMDD 테스트에서는 '20191010' 고정값으로 입력 |
| Ineymd |	조회종료일자 |	필드 |	8 |	필수 |	YYYYMMDD 테스트에서는 '20191010' 고정값으로 입력 |
### 3.3.3 전기요금 납부내역조회 Response example
```json
{
    "Header": {
        "Trtm": "104316",
        "Rsms": "정상처리되었습니다.",
        "ApiNm": "InquireElectricityFarePaymentHistory",
        "IsTuno": "20191010104316000020",
        "Tsymd": "20191010",
        "FintechApsno": "001",
        "Iscd": "000013",
        "Rpcd": "00000",
        "ApiSvcCd": "13E_001_00"
    },
    "IqtCnt": "1",
    "CtntDataYn": "N",
    "TotCnt": "1",
    "PageNo": "1",
    "Rec": [
        {
        "ElcrPmntNo ": "0606628088",
        "Drano ": "3020000000071",
        "PmntStcd ": "1",
        "PmntAmt ": "9230",
        "PmntYmd ": "20191010",
        "PmntTm": "154658",
        "PmntPtrn ": "E",
        "Txpr ": "홍길남",
        "TxtnIntt ": "부여지사",
        "PmntDln ": "20190930",
        "RcrdSbjc": "주택관리공단"
        }
    ]
} 
```
### 3.3.4 전기요금 납부내역조회 Response Element
| Element |	한글명 | Type |	Length |	optional |	Description |  
|:---|:---:|:---:|:---:|:---:|:---|  
| Header || 공통부 |||||	 
| TotCnt |	총건수 |	필드 |	10 |	필수 |	전체 건수 |
| IqtCnt |	조회총건수 |	필드 |	10 |	필수 |	페이지 당 조회된 총건수 |
| PageNo |	페이지번호 |	필드 |	4 |	필수 |	 
| CtntDataYn |	연속데이터여부 |	필드 |	1 |	필수 |	Y : 데이터 존재, N : 데이터 미존재 |
| REC |	납부내역목록 |	반복부 || 필수 |	페이지당 20건 |
| ElcrPmntNo |	전자납부번호 |	필드 |	17 |	필수 |	 
| Drano |	출금계좌번호 |	필드 |	20 |	필수 |	 
| PmntStcd |	납부상태코드 |	필드 |	1 |	필수 |	0 : 처리 중, 1 : 정상, 9 : 오류 |
| PmntAmt |	납부금액 |	필드 |	9 |	필수 |	 
| PmntYmd |	납부일자 |	필드 |	8 |	필수 |	YYYYMMDD |
| PmntTm |	납부시각 |	필드 |	6 |	필수 |	HH24MISS |
| PmntPtrn |	납부유형 |	필드 |	1 |	필수 |	E : 전기, S : 상하수도 |
| Txpr |	납세자명 |	필드 |	40 |	필수 |	 
| TxtnIntt |	과세기관 |	필드 |	40 |	필수 |	 
| PmntDln |	납부기한 |	필드 |	8 |	필수 |	 
| RcrdSbjc |	기록사항 |	필드 |	1 |	필수 |	입금 정보 |

### 3.4.1 상하수도요금납부 선조회 Request example
```json
{
    "Header": {
        "ApiNm": "InquireSewageFarePayment",
        "Tsymd": "20191212",
        "Trtm": "112428",
        "Iscd": "000013",
        "FintechApsno": "001",
        "ApiSvcCd": "13E_002_00",
        "IsTuno": "0001232130",
        "AccessToken": "10b74dd7f5f0f521ecdc7ade82f793bdfc119c3635d2e5303ae6aba0c93d4246"
    },
    "ElecCsmrNo": "263201755751004",
    "Acno": "3020000000071",
    "PageNo": "1"
}
```
### 3.4.2 상하수도요금납부 선조회 Request Element
| Element |	한글명 | Type |	Length |	optional |	Description |  
|:---|:---|:---:|:---:|:---:|:---|  
| Header || 공통부 |||||	  	
| ElecCsmrNo |	전자수용가번호 |	필드 |	15 |	필수 |	테스트에서는 '263201755751004' 고정값으로 입력 |
| Acno |	계좌번호 |	필드 |	20 |	필수 |	테스트에서는 '3020000000071' 고정값으로 입력 |
| PageNo |	페이지번호 |	필드 |	4 | |	미입력시 default 1 세팅 테스트에서는 '1' 고정값으로 입력 |
### 3.4.3 상하수도요금납부 선조회 Response example
```json
{
    "Header": {
        "Trtm": "104316",
        "Rsms": "정상처리되었습니다.",
        "ApiNm": "InquireElectricityFarePaymentHistory",
        "IsTuno": "20191010104316000020",
        "Tsymd": "20191010",
        "FintechApsno": "001",
        "Iscd": "000013",
        "Rpcd": "00000",
        "ApiSvcCd": "13E_001_00"
    },
    "IqtCnt": "1",
    "CtntDataYn": "N",
    "TotCnt": "1",
    "PageNo": "1",
    "Rec": [
        {
        "ElcrPmntNo ": "0606628088",
        "Drano ": "3020000000071",
        "PmntStcd ": "1",
        "PmntAmt ": "9230",
        "PmntYmd ": "20191010",
        "PmntTm": "154658",
        "PmntPtrn ": "E",
        "Txpr ": "홍길남",
        "TxtnIntt ": "부여지사",
        "PmntDln ": "20190930",
        "RcrdSbjc": "주택관리공단"
        }
    ]
} 
```
### 3.4.4 상하수도요금납부 선조회 Response Element
| Element |	한글명 | Type |	Length |	optional |	Description |  
|:---|:---:|:---:|:---:|:---:|:---|  
| Header || 공통부 |||||	 
| TotCnt |	총건수 |	필드 |	10 |	필수 |	전체 건수 |
| IqtCnt |	조회총건수 |	필드 |	10 |	필수 |	페이지 당 조회된 총건수 |
| CtntDataYn |	연속데이터여부 |	필드 |	1 |	필수 |	Y : 데이터 존재, N : 데이터 미존재 |
| REC |	상하수도목록 |	반복부 |	 |	필수 |	페이지당 10건 |
| PbtxGroNo |	공과금 | 지로번호 | 필드 |	7 |	필수 |	 
| PbtxInstClasCd |	공과금 기관분류코드 |	필드 |	2 |	필수 |	 
| PbtxPytxno |	공과금 납세번호 |	필드 |	32 |	필수 |	 
| PbtxElcrPmntNo |	공과금 전자납부번호 |	필드 |	19 |	필수 |	 
| Isnm |	기관명 |	필드 |	40 |	필수 |	 
| TxitNm |	세목명 |	필드 |	30 |	필수 |	 
| PbtxNtfFrmt |	공과금 고지형태 |	필드 |	1 |	필수 |	 
| Tram |	거래금액 |	필드 |	15 |	필수 |	 
| PbtxTmpmDsnc |	공과금 납기구분 |	필드 |	1 |	필수 |	 
| TmpmWthnDay |	공과금 납부기한 |	필드 |	8 |	필수 |	 
| PbtxAhstRcvDvCd |	공과금 선결제입금구분코드 |	필드 |	1 |	필수	|
| PbtxAttrRgsnYn |	공과금 자동이체등록여부 |	필드 |	1 |	필수 |	 

### 3.5.1 상하수도요금납부 Request example
```json
{
   "Header": {
     "ApiNm": "SewageFarePayment",
     "Tsymd": "20191212",
     "Trtm": "112428",
     "Iscd": "000013",
     "FintechApsno": "001",
     "ApiSvcCd": "13E_002_00",
     "IsTuno": "23435435443",
     "AccessToken": "10b74dd7f5f0f521ecdc7ade82f793bdfc119c3635d2e5303ae6aba0c93d4246"
   },
   "PbtxGroNo": "1004102",
   "PbtxInstClasCd": "26",
   "PbtxPytxno": "2632017557510042632000017091002",
   "PbtxElcrPmntNo": "2632001709000428753",
   "Acno": "3020000000071",
   "PayRcrdSbjcCntn": "주택관리공단",
   "Tram": "733120",
   "Isnm": "부산광역시",
   "TmpmWthnDay": "20191130",
   "PryNm": "홍길남",
   "TxitNm": "상하수도요금"
}
```
### 3.5.2 상하수도요금납부 Request Element
| Element |	한글명 | Type |	Length |	optional |	Description |  
|:---|:---|:---:|:---:|:---:|:---|  
| Header || 공통부 |||||	  	 	 	 
| PbtxGroNo |	공과금 지로번호 |	필드 |	7 |	필수 |	납부선조회 응답의 " PbtxGroNo " 값 테스트에서는 '1004102' 고정값으로 입력 |
| PbtxInstClasCd |	공과금 기관분류코드 |	필드 |	2 |	필수 |	납부선조회 응답의 " PbtxInstClasCd " 값 테스트에서는 '26' 고정값으로 입력 |
| PbtxPytxno |	공과금 납세번호 |	필드 |	32 |	필수 |	납부선조회 응답의 " PbtxPytxno " 값 테스트에서는 '2632017557510042632000017091002' 고정값으로 입력 |
| PbtxElcrPmntNo |	공과금 전자납부번호 |	필드 |	19 |	필수 |	납부선조회 응답의 " PbtxElcrPmntNo " 값 테스트에서는 '2632001709000428753' 고정값으로 입력 |
| Acno |	계좌번호 |	필드 |	20 |	필수 |	테스트에서는 '3020000000071' 고정값으로 입력 |
| PayRcrdSbjcCntn |	납부기록사항 |	필드 |	12 |	필수 |	테스트에서는 '주택관리공단' 고정값으로 입력 |
| Tram |	거래금액 |	필드 |	15 |	필수 |	납부선조회 응답의 " Tram " 값 테스트에서는 '733120' 고정값으로 입력 |
| Isnm |	기관명 |	필드 |	100 |	필수 |	납부선조회 응답의 " Isnm " 값 테스트에서는 '부산광역시' 고정값으로 입력 |
| TmpmWthnDay |	납기내일자 | 필드 |	8 |	필수 |	납부선조회 응답의 " TmpmWthnDay " 값 테스트에서는 '20191130' 고정값으로 입력 |
| PryNm |	납부자명 |	필드 |	40 |	필수 |	테스트에서는 '홍길남' 고정값으로 입력 |
| TxitNm |	세목명 |	필드 |	50 |	필수 |	납부선조회 응답의 " TxitNm " 값 테스트에서는 '상하수도요금' 고정값으로 입력 |
### 3.5.3 상하수도요금납부 Response example
```json{
{
  "Header": {
    "Trtm": "104316",
    "Rsms": "정상처리되었습니다.",
    "ApiNm": "SewageFarePayment",
    "IsTuno": "20191108104316000076",
    "Tsymd": "20191108",
    "FintechApsno": "001",
    "Iscd": "000013",
    "Rpcd": "00000",
    "ApiSvcCd": "13E_002_00"
  },
  "PbtxGroNo": "1004102",
  "PbtxInstClasCd": "26",
  "PbtxPytxno": "2632017557510042632000017091002",
  "PbtxElcrPmntNo": "2632001709000428753",
  "PayRcrdSbjcCntn": "주택관리공단",
  "PryAmt": "733120",
  "Isnm": "부산광역시",
  "TmpmWthnDay": "20191130",
  "PryNm": "홍길남"
}
```
### 3.5.4 상하수도요금납부 Response Element
| Element |	한글명 | Type |	Length |	optional |	Description |  
|:---|:---:|:---:|:---:|:---:|:---|  
| Header || 공통부 |||||	 
| PbtxGroNo |	공과금 지로번호 |	필드 |	7 |	필수 |	 
| PbtxInstClasCd |	공과금 기관분류코드 |	필드 |	2 |	필수 |	 
| PbtxPytxno |	공과금 납세번호 |	필드 |	32 |	필수 |	 
| PbtxElcrPmntNo |	공과금 전자납부번호 |	필드 |	19 |	필수 |	 
| PayRcrdSbjcCntn |	납부기록사항 |	필드 |	12 |	필수 |	 
| PryAmt |	납부금액 |	필드 |	15 |	필수 |	 
| Isnm |	기관명 |	필드 |	100 |	필수 |	 
| TmpmWthnDay |	납기내일자 |	필드 |	8 |	필수 |	 
| PryNm |	납부자명 |	필드 |	40 |	필수 |	 

### 3.6.1 상하수도요금 납부내역조회 Request example
```json
{
    "Header": {
        "ApiNm": "InquireSewageFarePaymentHistory",
        "Tsymd": "20191212",
        "Trtm": "112428",
        "Iscd": "000013",
        "FintechApsno": "001",
        "ApiSvcCd": "13E_002_00",
        "IsTuno": "09832749",
        "AccessToken": "10b74dd7f5f0f521ecdc7ade82f793bdfc119c3635d2e5303ae6aba0c93d4246"
    },
    "ElecPayNo": "2632001709000428753",
    "PageNo": "1",
    "Insymd": "20191108",
    "Ineymd": "20191108"
}
```
### 3.6.2 상하수도요금 납부내역조회 Request Element
| Element |	한글명 | Type |	Length |	optional |	Description |  
|:---|:---|:---:|:---:|:---:|:---|  
| Header || 공통부 |||||	  	 	 	 
| ElecPayNo |	전자납부번호 |	필드 |	19 |	선택 |	미입력 시 기간 내 납부내역 전체 조회 테스트에서는 '2632001709000428753' 고정값으로 입력 |
| PageNo |	페이지번호 |	필드 |	4 |	선택 |	Default : 1 테스트에서는 '1' 고정값으로 입력 |
| Insymd |	조회시작일자 |	필드 |	8 |	필수 |	YYYYMMDD 테스트에서는 '20191108' 고정값으로 입력 |
| Ineymd |	조회종료일자 |	필드 |	8 |	필수 |	YYYYMMDD 테스트에서는 '20191108' 고정값으로 입력 |
### 3.6.3 상하수도요금 납부내역조회 Response example
```json{{
    "Header": {
        "Trtm": "145651",
        "Rsms": "정상처리되었습니다.",
        "ApiNm": "InquireSewageFarePaymentHistory",
        "IsTuno": "20180731145659000024",
        "Tsymd": "20180731",
        "FintechApsno": "001",
        "Iscd": "000013",
        "Rpcd": "00000",
        "ApiSvcCd": "13E_002_00"
    },
    "TotCnt": "3",
    "PageNo": "1",
    "IqtCnt": "3",
    "CtntDataYn": "N",
    "Rec": [
        {
        "PmntPtrn": "S",
        "RcrdSbjc": "주택관리공단",
        "PmntStcd": "1",
        "Txpr": "테스트",
        "TxtnIntt": "부산광역시",
        "PmntAmt": "2400",
        "PmntDln": "20180731",
        "ElcrPmntNo": "2632001709000879493",
        "Drano": "11017002365",
        "PmntTm": "104918",
        "PmntYmd": "20180727"
        },
        {
        "PmntPtrn": "S",
        "RcrdSbjc": "주택관리공단",
        "PmntStcd": "1",
        "Txpr": "테스트",
        "TxtnIntt": "부산광역시",
        "PmntAmt": "69440",
        "PmntDln": "20180731",
        "ElcrPmntNo": "2632001709000879659",
        "Drano": "11017002365",
        "PmntTm": "140540",
        "PmntYmd": "20180731"
        },
        {
        "PmntPtrn": "S",
        "RcrdSbjc": "주택관리공단",
        "PmntStcd": "1",
        "Txpr": "테스트",
        "TxtnIntt": "부산광역시",
        "PmntAmt": "576300",
        "PmntDln": "20180731",
        "ElcrPmntNo": "2632001709000882884",
        "Drano": "11017002365",
        "PmntTm": "142616",
        "PmntYmd": "20180731"
        }
    ]
}
```
### 3.6.4 상하수도요금 납부내역조회 Response Element
| Element |	한글명 | Type |	Length |	optional |	Description |  
|:---|:---:|:---:|:---:|:---:|:---|  
| Header || 공통부 |||||	 
| TotCnt |	총건수 |	필드 |	10 |	필수 |	전체 건수 |
| IqtCnt |	조회총건수 |	필드 |	10 |	필수 |	페이지 당 조회된 총건수 |
| PageNo |	페이지번호 |	필드 |	4 |	필수 |	 
| CtntDataYn |	연속데이터여부 |	필드 |	1 |	필수 |	Y : 데이터 존재, N : 데이터 미존재 |
| REC |	납부내역목록 | |	반복부 | 필수 |	페이지당 20건 | 
| ElcrPmntNo |	전자납부번호 |	필드 |	19 |	필수 |	 
| Drano |	출금계좌번호 |	필드 |	20 |	필수 |	 
| PmntStcd |	납부상태코드 |	필드 |	1 |	필수 |	0 : 처리 중, 1 : 정상, 9 : 오류 |
| PmntAmt |	납부금액 |	필드 |	9 |	필수 |	 
| PmntYmd |	납부일자 |	필드 |	8 |	필수 |	YYYYMMDD |
| PmntTm |	납부시각 |	필드 |	6 |	필수 |	HH24MISS |
| PmntPtrn |	납부유형 |	필드 |	1 |	필수 |	E : 전기, S : 상하수도 |
| Txpr |	납세자명 |	필드 |	40 |	필수 |	 
| TxtnIntt |	과세기관 |	필드 |	40 |	필수 |	 
| PmntDln |	납부기한 |	필드 |	8 |	필수 |	 
| RcrdSbjc |	기록사항 |	필드 |	40 |	필수 |	입금 정보 |
