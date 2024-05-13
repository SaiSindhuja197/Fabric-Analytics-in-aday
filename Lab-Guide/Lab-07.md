![](../Images/Lab-07/lab-7.png)

## 목차
- 소개

- Power BI

    - 작업 1: 보고서 자동 생성

    - 작업 2: 새 보고서의 배경 구성

    - 작업 3: 보고서에 헤더 추가

    - 작업 4: 보고서에 KPI 추가

    - 작업 5: 보고서에 꺾은선형 차트 추가

    - 작업 6: 보고서 저장

    - 작업 7: Date 테이블의 Year 열 구성

    - 작업 8: Date 테이블의 Short_Month_Name 열 구성
    
    - 작업 9: 꺾은선형 차트 형식 지정
    
    - 작업 10: Direct Lake 모드를 시뮬레이션하기 위해 새 데이터 추가	

- 랩 환경 정리

- 참조

## 소개
우리는 다양한 데이터 원본의 데이터를 Lakehouse로 수집하고, Lakehouse에 도입하고, 데이터 모델을 만들고, 데이터 원본에 대한 새로 고침 일정을 설정했습니다. 이제 보고서를 작성해 보겠습니다.
이 랩을 마치면 다음 사항을 알게 됩니다.

- 보고서를 자동 생성하는 방법

- 빈 캔버스에서 시작해서 보고서를 빌드하는 방법

- Direct Lake 모드에서 데이터의 자동 새로 고침을 경험하는 방법

## Power BI
### 작업 1: 보고서 자동 생성
보고서 자동 생성 옵션을 사용해 시작해 보겠습니다. 그리고 본 랩의 후반에서 Power BI에 있는 보고서를 다시 작성해 보겠습니다.

1. 이전 랩에서 만든 **Fabric 작업 영역**으로 되돌아가 보겠습니다.
2. 왼쪽 패널의 아래쪽에서 **Fabric 환경 선택기** 아이콘을 선택합니다.
3. Fabric 환경 대화 상자가 열립니다. **Power BI**를 선택합니다. **Power BI 홈 페이지**로 이동합니다.
 
 ![](../Images/Lab-07/image006.png)
 
4. 상단 메뉴에서 **새 보고서**를 선택합니다.

![](../Images/Lab-07/image009.png)

5. **첫 번째 보고서 화면 만들기**로 이동됩니다. 데이터를 수동으로 입력하고 보고서를 작성하거나 게시된 의미 체계 모델을 선택하는 옵션이 있습니다. 이전 랩에서 의미 체계 모델을 만들♘습니다. 그 모델을 사용해보겠습니다. **게시된 의미 체계 모델 선택** 옵션을 선택합니다.

![](../Images/Lab-07/image012.jpg)

6. 보고서 페이지에서 사용할 데이터 세트를 선택합니다. 네 가지 옵션이 있습니다. **lh_FAIAD를 선택합니다**.

    a. **lh_FAIAD:** 이것은 우리가 생성하고 보고서에 사용하려는 데이터 세트가 있는 레이크하우스입니다.

    b. **Units by Supplier:** 이것은 T-SQL을 사용하여 생성한 데이터 세트입니다.

    c. **DataflowsStagingWarehouse:** 기본적으로 생성되는 준비 Warehouse입니다.
    데이터를 준비하지 않았기 때문에 사용하지 않았습니다.

    d. **DataflowsStagingLakehouse:** 기본적으로 생성되는 준비 Lakehouse입니다. 데이터를 준비하지 않았기 때문에 사용하지 않았습니다.

7.	**보고서 자동 만들기 버튼** 옆에 있는 화살표를 클릭합니다. 보고서 자동 만들기와 빈 보고서 만들기라는 두 가지 옵션이 있습니다. 자동 만들기를 해보겠습니다. **보고서 자동 만들기**를 선택합니다.

![](../Images/Lab-07/image015.jpg) 

8.	Power BI가 보고서 자동 만들기를 시작합니다. 원할 경우 데이터를 사전 선택하는 옵션도 있습니다. 보고서가 준비되면 화면 오른쪽 상단에 대화 상자가 나타납니다. **View report now**를 선택합니다.

![](../Images/Lab-07/image018.jpg) 

**체크포인트:** 아래 스크린샷과 같은 보고서가 생성됩니다. 몇 가지 KPI와 몇 가지 추세 시각적 개체가 있습니다. 새 모델을 분석하고 빠른 시작이 필요한 경우 이것이 좋은 방법입니다.

**참고:** 상단 메뉴에는 보고서를 편집하거나 일부 데이터를 표로 볼 수 있는 옵션이 있습니다. 이들 옵션을 자유롭게 탐색해보십시오.

9.	이 보고서를 저장해 보겠습니다. 상단 메뉴에서 **저장**을 선택합니다.

10.	보고서 저장 대화 상자가 열립니다. 보고서 이름을 **rpt_Sales_Auto_Report**로 지정합니다.

**참고:** 보고서 이름 앞에는 보고서의 약자인 rpt가 붙습니다.
 
11.	보고서가 작업 영역, **FAIAD_<username>**에 저장되어 있는지 확인합니다.

12.	**저장**을 선택합니다.

![](../Images/Lab-07/image021.jpg) 

**참고:** 자동 생성된 보고서는 "자동 생성"되므로 다르게 보일 수 있습니다. 또한 이전 랩(랩
6)에서 생성한 관계 및 측정값에 따라 달라집니다.

위 스크린샷은 선택적 관계(랩 6)를 포함하여 모든 관계와 측정값을 생성한 경우 자동 생성된 보고서가 **어떻게** 표시되는지 보여줍니다.

아래 스크린샷은 선택적 관계(랩 6)와 측정값 생성을 건너뛴 경우 자동 생성된 보고서가
**어떻게** 표시되는지 보여줍니다.

 
### 작업 2: 새 보고서의 배경 구성

빈 캔버스를 사용하여 새 보고서를 생성해 보겠습니다.

1. **왼쪽 패널**에서 작업 영역 이름 **FAIAD_<username>**을 선택하여 작업 영역으로 다시 이동합니다.

2.	상단 메뉴에서 **새로 만들기 -> 보고서**를 선택합니다. 첫 번째 보고서 페이지 만들기로 이동됩니다.

![](../Images/Lab-07/image027.png) 

3.	**게시된 의미 체계 모델 선택**을 선택하면 우리가 만든 모델을 선택할 수 있습니다.

![](../Images/Lab-07/image030.jpg) 

4.	보고서에서 사용할 의미 체계 모델을 선택하면 대화 상자가 열립니다. **lh_FAIAD**를 선택합니다.

5.	**보고서 자동 만들기 버튼** 옆에 있는 화살표를 클릭합니다. **빈 보고서 만들기를**을 선택합니다.


 ![](../Images/Lab-07/image033.jpg) 

 

6.	아직 열지 않았다면 랩 환경의 **C:\FAIAD\Reports** 폴더에 있는 **FAIAD.pbix**를 엽니다.
이 보고서를 기준으로 사용하겠습니다. 캔버스 배경을 추가하는 것부터 시작하겠습니다. 보고서 머리글을 만들고, 몇 가지 KPI를 추가하고, 시간별 매출 선 차트를 만듭니다. 시간 관계상 Power BI Desktop에서 시각적 개체를 구축한 경험이 있다고 가정하고 모든 시각적 개체를 생성하지는 않을 것입니다.

![](../Images/Lab-07/image036.jpg) 


7.	브라우저에서 **Power BI 캔버스**로 되돌아갑니다.

8.	시각화 창에서 **페이지 형식 지정 아이콘**을 선택합니다.
 
9.	**캔버스 배경 섹션**을 확장합니다.

10.	**이미지** 옵션에서 **찾아보기**를 선택합니다. 파일 탐색기 대화 상자가 열립니다.

11.	랩 환경의 **C:\FAIAD\Reports**폴더로 이동합니다.

12.	**Summary Background.png**를 선택합니다.

13.	**이미지 맞춤** 드롭다운을 **맞춤**으로 설정합니다.

14.	투명도를 **0%**로 설정합니다.

![](../Images/Lab-07/image039.jpg) 


### 작업 3: 보고서에 헤더 추가

1.	상단 여백에 헤더를 추가해 보겠습니다. **메뉴**에서 **텍스트 상자**를 선택합니다.

2.	텍스트 상자의 첫 번째 줄에 **Fabrikam Company**를 입력합니다.

3.	텍스트 상자의 두 번째 줄에 **Sales Report**를 입력합니다.

4.	**Fabrikam Company**를 강조 표시하고 **글꼴**을 **Segoe UI**로 **글꼴 크기**를 **18, 굵게**로 설정합니다.

5.	**Sales Report**를 강조 표시하고 **글꼴**을 **Segoe UI**로 **글꼴 크기**를 **14**로 설정합니다.

6.	**텍스트 상자를 선택**하고 오른쪽 서식 텍스트 **상자 창**에서 효과를 확장합니다.

7.	**배경** 슬라이더를 사용하여 **끄기**로 설정합니다.

8.	**텍스트 상자의 크기를 상단 여백에 맞게 조정합니다**.

![](../Images/Lab-07/image042.jpg) 
 
### 작업 4: 보고서에 KPI 추가

1.	매출 KPI를 추가해 보겠습니다. 텍스트 상자에서 벗어나려면 캔버스에서 **공백**을 선택합니다.

2.	**시각화 섹션**에서 **다중행 카드 시각적 개체**를 선택합니다.

3.	**데이터 섹션**에서 **Sales 테이**블을 확장합니다.

4.	**Sales 측정값**을 선택합니다.

![](../Images/Lab-07/image045.jpg) 

5.	**다중행 카드 시각적 개체가 선택된** 상태에서 시각화 섹션에서 **시각적 개체 서식 지정 아이**콘을 선택합니다.

6.	**범주 레이블** 섹션을 확장합니다.

7.	**글꼴 크기**를 **14**로 높입니다.

8.	**색상 드롭다운**을 선택합니다. 색상 팔레트 대화 상자가 열립니다.

9.	헥스 값을 **#004753**으로 설정합니다.
 
 ![](../Images/Lab-07/image048.jpg) 

10.	**카드** 섹션을 확장합니다.

11.	**악센트 바** 슬라이더를 **끄기**로 설정합니다.

![](../Images/Lab-07/image051.png) 
 

12.	시각화 창에서 **일반**을 선택합니다.

13.	**효과 섹션**을 확장합니다.

14.	**배경** 슬라이더를 사용하여 **끄기**로 설정합니다.

15.	**시각적 개체**의 크기를 조정하고 **스크린샷과 같이 왼쪽 상자**로 옮깁니다.

![](../Images/Lab-07/image054.png) 

16.	또 다른 KPI를 추가해 보겠습니다. 방금 만든 **Sales 다중 행 카드**를 선택합니다. 키보드에서
**Ctrl+C**를 선택하여 시각적 개체를 **복사**합니다.

17.	키보드에서 **Ctrl+V**를 선택하여 시각적 개체를 **붙여넣기**합니다. 시각적 개체가 캔버스에 붙여넣기 됐습니다.
 
18.	**새 시각적 개체가 강조표시된** 상태에서 **시각화 창 -> 시각적 개체 빌드 -> 필드** 섹션에서
**Sales** 측정값을 제거합니다.

19.	**데이터** 섹션에서 **Sales** 테이블을 확장하고 **Units** 측정값을 선택합니다.

20.	**시각적 개체**의 크기를 조정하고 **Sales 시각적 개체 아래의 상자에** 넣습니다.

![](../Images/Lab-07/image057.jpg) 


### 작업 5: 보고서에 꺾은선형 차트 추가

재판매사별로 시간에 따른 매출을 시각화하는 꺾은선형 차트를 만들어 보겠습니다.

1.	다중 행 카드 시각 개체에서 벗어나려면 캔버스에서 **공백**을 선택합니다.

2.	**시각화 섹션**에서 **꺾은선형 차트**를 선택합니다.

3.	**데이터 섹션**에서 **Date** 테이블을 확장합니다.

4.	**Year** 필드를 선택합니다. Year가 기본 설정으로 합산되어 Y축에 추가되어 있습니다. 이 문제를 해결해보겠습니다.

![](../Images/Lab-07/image060.jpg) 

 
### 작업 6: 보고서 저장

모델을 변경하기 위해 보고서에서 벗어나기 전에 보고서를 저장해 보겠습니다.

1.	상단 메뉴에서 **파일 -> 저장**을 선택합니다.

2.	보고서 저장 대화 상자가 열립니다. 보고서 이름을 **rpt_Sales_Report**로 지정합니다.

**참고:** 보고서 이름 앞에는 보고서의 약자인 rpt가 붙습니다.

3.	보고서가 **FAIAD_<username** 작업 영역에 저장되어 있는지 확인합니다.

4.	**저장**을 선택합니다.

![](../Images/Lab-07/image063.jpg) 



### 작업 7: Date 테이블의 Year 열 구성

1.	**왼쪽 메뉴 모음**에서 **lh_FAIAD**를 선택하여 Lakehouse로 이동합니다.

2.	왼쪽 탐색기 창에서 **lhFAIAD -> Schemas -> dbo -> Tables -> Date**로 확장합니다.

3.	**Year** 열을 선택합니다.

4.	오른쪽 **속성** 창에서 **고급** 섹션을 확장합니다.

5.	**요약 기준** 드롭다운에서 **없음**을 선택합니다.

![](../Images/Lab-07/image066.jpg) 
 
 

6.	왼쪽 메뉴 모음에서 **rpt_Sales_Report**를 선택하여 보고서로 다시 이동합니다.

7.	상단 메뉴에서 **편집**을 선택합니다.

8.	상단 메뉴에서 **새로 고침**을 선택합니다. 데이터 패널에서 Year는 합계 필드가 아닙니다.

9.	**꺾은선형 차트 시각적 개체를 선택한** 상태에서 Y축에서 Year 합계를 제거합니다.

10.	**Year** 필드를 선택하면 **X축**에 추가됩니다.

11.	**Sales** 테이블을 확장하고 **Sales 측정**값을 선택합니다.

![](../Images/Lab-07/image069.jpg) 
 
### 작업 8: Date 테이블의 Short_Month_Name 열 구성

1.	이 차트에 월을 추가해 보겠습니다. Date 테이블에서 **X축의 Year**아래로 **Short_Month_Name**
필드를 드래그합니다. 시각적 개체가 Sales를 기준으로 정렬되어 있습니다. 이를
Short_Month_Name으로 정렬해 보겠습니다.

2.	시각적 개체의 오른쪽 상단에서 **줄임표**(...)를 선택합니다.

3.	**축 정렬 -> Year Short_Month_Name**을 선택합니다.

4.	시각적 개체의 오른쪽 상단에서 **줄임표(...)**를 선택합니다.

5.	**축 정렬 -> 오름차순 정렬**을 선택합니다.

![](../Images/Lab-07/image072.jpg) 

**참고:** 월이 알파벳순으로 정렬되어 있습니다. 이를 수정해 보겠습니다.

![](../Images/Lab-07/image075.png) 

6.	**왼쪽 메뉴 모음**에서 **lh_FAIAD**를 선택하여 Lakehouse로 이동합니다.

7.	**저장되지 않은 변경 사항** 대화 상자가 열립니다. **저장**을 선택하여 변경 사항을 보고서에 저장합니다.

![](../Images/Lab-07/image078.png) 

 
8.	lh_FAIAD Lakehouse로 이동합니다. 왼쪽 탐색기 창에서 **lhFAIAD -> Schemas -> dbo -> Tables -> Date**로 확장합니다.

9.	**Short_Month_Name** 열을 선택합니다.

10.	오른쪽 **속성** 창에서 **고급** 섹션을 확장합니다.

11.	**열 기준 정렬** 드롭다운에서 **Month**를 선택합니다.

![](../Images/Lab-07/image081.jpg) 

12.	왼쪽 메뉴 모음에서 **rpt_Sales_Report**를 선택하여 보고서로 다시 이동합니다.

13.	상단 메뉴에서 **편집**을 선택합니다.

14.	상단 메뉴에서 **새로 고침**을 선택합니다. 이제 월이 올바르게 정렬되어 있습니다.

![](../Images/Lab-07/image084.png) 

 
### 작업 9: 꺾은선형 차트 형식 지정

보고서를 작성하는 동안 의미 체계 모델을 업데이트하는 것이 얼마나 쉬운지 확인하십시오. 이는 Power BI Desktop과 같은 원활한 상호 작용을 제공합니다.

1.	**꺾은선형 차트 시각적 개체를 선택한** 상태에서 **데이터 섹션**에서 **Reseller** 테이블을 확장합니다.

2.	**Reseller -> Reseller Company** 필드를 **범례** 섹션으로 드래그합니다.

![](../Images/Lab-07/image087.jpg) 

3.	**꺾은선형 차트 시각적 개체를 선택한** 상태에서 시각화 섹션에서 **시각적 개체 서식 지정 아이콘 -> 일반**을 선택합니다.

4.	**제목** 섹션을 확장합니다.

5.	**제목** 텍스트를 **시간 경과에 따른 매출**로 설정합니다.

6.	**효과 섹션**을 확장합니다.

7.	**배경** 슬라이더를 사용하여 **끄기**로 설정합니다.

![](../Images/Lab-07/image090.png) 
 
8.	**시각화** 섹션에서 **시각적 개체 서식 지정 아이콘 - > 시각적 개체**를 선택합니다.

9.	**줄** 섹션을 확장합니다.

10.	**색** 섹션을 펼칩니다.

11.	**Wingtip Toys** 색상을 **#004753**으로 설정합니다.

12.	**Tailspin Toys** 색상을 **#F17925**으로 설정합니다.

13.	**시각적 개체**의 크기를 조정하고 **스크린샷과 같이 우측 상단 상자**로 옮깁니다.

14.	시각적 개체에서 오른쪽으로 스크롤하면 **2023년 4월까지의 데이터를 확인할 수 있습니다.**

![](../Images/Lab-07/image093.png) 

15.	보고서를 저장하겠습니다. 메뉴에서 **파일 -> 저장**을 선택합니다.
앞서 언급했듯이 본 랩에서는 모든 시각적 개체를 빌드하지는 않습니다. 시간이 있다면 자유롭게 더 많은 시각적 요소를 빌드해보십시오.
 
### 작업 10: Direct Lake 모드를 시뮬레이션하기 위해 새 데이터 추가
일반적으로 Import 모드에서는 원본의 데이터가 새로 고침되면 Power BI 모델을 새로 고침해야 하고 그런 후에 보고서의 데이터가 업데이트됩니다. Direct query 모드를 사용할 경우 원본에서 데이터를 새로 고침되면 Power BI 보고서에서 사용할 수 있습니다. 그러나 Direct query 모드는 일반적으로 느립니다. 이 문제를 해결하기 위해 Microsoft Fabric은 Direct Lake 모드를 도입했습니다. Direct Lake는 레이크의 데이터를 Power BI 엔진으로 직접 로드하여 분석 준비를 하는 빠른 경로입니다. 이에 대해서 알아보겠습니다.
실제 시나리오에서는 데이터가 원본에서 업데이트됩니다. 지금은 교육 환경에 있는 만큼, 2023년 5월 데이터가 포함된 Parquet 파일에 연결하여 이를 시뮬레이션하겠습니다.

1.	왼쪽 메뉴 모음에서 **FAIAD_<username**을 선택하여 작업 영역 홈으로 이동합니다.

2.	**df_Sales_ADFS**를 선택하면 새 Parquet 파일을 추가하여 데이터 흐름을 편집할 수 있습니다.

![](../Images/Lab-07/image096.jpg) 

3.	리본 메뉴에서 **홈 -> 데이터 가져오기 -> 빈 쿼리...**를 선택합니다.

4.	데이터 원본에 연결 대화 상자가 열립니다. **편집기에서 모든 행을 선택하고 삭제**합니다.

5.	아래 코드를 복사하여 편집기에 붙여넣습니다.
 
let 

Source = #"ADLS Base Folder",
#"Filtered Rows" = Table.SelectRows(Source, each Text.Contains([Folder Path], "Sales.Invoices_May")),

#"https://stvnextblobstorage dfs core windows net/fabrikam-sales/Delta-Parquet-Format/Sales Invoices_May/_0- 0ee085a3-716f-4833-a792-c3162c1de300-0 parquet" = #"Filtered Rows"{[#"Folder
Path"="https://stvnextblobstorage.dfs.core.windows.net/fabrikam-sales/Delta-Parquet-
Format/Sales.Invoices_May/",Name="0-0ee085a3-716f-4833-a792-c3162c1de300-0.parquet"]}[Content],

#"Imported Parquet" = Parquet.Document(#"https://stvnextblobstorage dfs core windows net/fabrikam-sales/Delta- Parquet-Format/Sales Invoices_May/_0-0ee085a3-716f-4833-a792-c3162c1de300-0 parquet")

in

#"Imported Parquet"

6.	**다음**을 선택합니다.

![](../Images/Lab-07/image100.jpg) 

7.	새 쿼리가 다시 생성됩니다. **이름 바꾸기**를 해보겠습니다. **쿼리 설정 -> 속성 -> 이름**의 오른쪽 패널에서 쿼리의 이름을 **MayInvoice**로 변경합니다.

8.	새 쿼리에 대한 준비를 비활성화하겠습니다. MayInvoice 쿼리를 **마우스 오른쪽 버튼으로 클릭**하고 **준비 활성화를 선택 취소**합니다.

![](../Images/Lab-07/image103.jpg) 

 
9.	이제 5월 Invoice 데이터를 Invoice 테이블에 추가해 보겠습니다. 쿼리 섹션에서 **Invoice**
쿼리를 선택합니다.

10.	리본 메뉴에서 **홈 -> 쿼리 추가**를 선택합니다.

11.	쿼리 추가 대화 상자가 나타납니다. **추가할 테이블** 드롭다운에서 **MayInvoice**를 선택합니다.

12.	**확인**을 선택합니다.

![](../Images/Lab-07/image106.jpg) 

13.	우측 하단에서 게시를 선택하여 업데이트를 저장 및 게시합니다.

![](../Images/Lab-07/image109.jpg)

**참고:** 게시되면 데이터 흐름이 새로 고침됩니다. 이 작업은 몇 분 정도 걸릴 수 있습니다.

14.	왼쪽 메뉴 모음에서 **rpt_Sales_Report**를 선택하여 보고서로 다시 이동합니다.

15.	상단 메뉴에서 **새로 고침**을 선택합니다. 이제 꺾은선형 차트에 2023년 5월의 데이터가 있습니다. 또한 판매 금액과 판매 단위가 증가한 것을 확인할 수 있습니다.

![](../Images/Lab-07/image112.jpg)
 
 

이전 랩에서 만든 데이터 흐름이 일정에 따라 새로 고침되고 데이터가 Lakehouse로 수집됩니다. Lakehouse의 데이터 모델이 업데이트되고 보고서가 새로 고침됩니다. 각 데이터 흐름이 새로 고침될 때 데이터 모델과 보고를 새로 고침할 필요가 없습니다. 이것이 바로 Direct Lake의 장점입니다.

문제 설명에 나열된 과제를 다시 살펴보겠습니다.

- **서로 다른 데이터 원본에 대한 서로 다른 업데이트 시간을 설정하려면 데이터 세트를 적어도 하루에 세 번 이상 새로 고쳐야 합니다.**

Direct Lake를 사용하여 이 문제를 해결했습니다. 각 개별 데이터 흐름은 해당 일정에 따라 새로 고침됩니다. 데이터 세트와 보고서를 새로 고침할 필요가 없습니다.

- **소스 시스템에 발생한 업데이트를 캡처하기 위해 매번 전체 새로 고침을 수행해야 하므로 새로 고치는 데 시간이 오래 걸립니다**.

    다시 한번 Direct Lake를 사용하여 이 문제를 해결했습니다. 각 개별 데이터 흐름은 해당 일정에 따라 새로 고침됩니다. 데이터 세트와 보고서는 새로 고침할 필요가 없으므로 전체 새로 고침에 대해 걱정할 필요가 없습니다.

- **가져오는 데이터 원본에 오류가 있으면 데이터 세트 새로 고침이 중단됩니다. 직원 파일이 제 시간에 업로드되지 않아 데이터 세트 새로 고침이 중단되는 경우가 많습니다.**

 데이터 파이프라인은 실패 시 다양한 간격으로 새로 고침을 재시도하는 기능을 제공하여 이 문제를 해결하는 데 도움이 됩니다.

- **데이터 크기가 크고 변환이 복잡한 것을 감안하면, Power Query가 미리 보기를 새로 고치는 데 오랜 시간이 걸리는 만큼 데이터 모델을 변경하는 데 매우 오랜 시간이 소요됩니다.**

    우리는 데이터 흐름이 효율적이고 변경하기 쉽다는 것을 알았습니다. 일반적으로 데이터 흐름의 미리 보기는 로드하는 데 시간이 오래 걸리지 않습니다.

- **회사 표준은 Mac이지만 Power BI Desktop을 사용하려면 Windows PC가 필요합니다.** 

    Microsoft Fabric은 SaaS 제품입니다. 필요한 것은 서비스에 액세스하기 위한 브라우저뿐입니다. 데스크톱에 소프트웨어를 설치할 필요가 없습니다.
 
## 랩 환경 정리

랩 환경을 정리할 준비가 되면 아래 단계를 따릅니다.

1.	왼쪽 패널에서 **FAIAD_<username** 작업 영역을 선택하여 작업 영역 홈으로 이동합니다.

2.	상단 메뉴에서 관리 액세스 옆에 있는 **줄임표(…)**를 선택하고 **작업 영역 설정**을 선택합니다.

![](../Images/Lab-07/image115.jpg)

3.	작업 영역 설정 대화 상자가 열립니다. 왼쪽 메뉴에서 **기타**를 선택합니다.

4.	**이 작업 영역 제거**를 선택합니다.

5.	작업 영역 삭제 대화 상자가 열립니다. **삭제**를 클릭합니다.

이렇게 하면 작업 영역과 작업 영역에 포함된 모든 항목이 삭제됩니다.

![](../Images/Lab-07/image118.jpg)

## 참조

Fabric Analyst in a Day(FAIAD)는 Microsoft Fabric에서 사용할 수 있는 몇 가지 주요 기능을 소개합니다. 서비스의 메뉴에 있는 도움말(?) 섹션에는 유용한 리소스로 연결되는 링크가 있습니다.

아래는 Microsoft Fabric의 다음 단계에 도움이 되는 몇 가지 추가 자료입니다.

![](../Images/Lab-07/image121.png)

아래는 Microsoft Fabric의 다음 단계에 도움이 되는 몇 가지 추가 자료입니다.

- [Microsoft Fabric GA 발표](https://www.microsoft.com/en-us/microsoft-fabric/blog/2023/11/15/prepare-your-data-for-ai-innovation-with-microsoft-fabric-now-generally-available/) 발표 전문을 블로그 포스트로 읽기  
-	 [가이드 투어](https://guidedtour.microsoft.com/en-us/guidedtour/microsoft-fabric/microsoft-fabric/1/1)로 Fabric 탐색 
-	 [Microsof t Fabric 무료 평가판](https://www.microsoft.com/en-us/microsoft-fabric/getting-started)신청   
-	[Microsof t Fabric 웹사이트](https://www.microsoft.com/en-in/microsoft-fabric) 방문  
-	[Fabric 학습 모듈](https://learn.microsoft.com/en-us/training/browse/?products=fabric&resource_type=module)을 탐색해서 새로운 기술 익히기 
-	[Fabric 기술 문서 ](https://learn.microsoft.com/en-us/fabric/)검토
-	[Fabric 시작하기 무료 e북](https://info.microsoft.com/ww-landing-unlocking-transformative-data-value-with-microsoft-fabric.html)읽기
-	[Fabric 커뮤니티](https://community.fabric.microsoft.com/)에 가입하여 질문을 게시하고 피드백을 공유하며 다른 사람들로부터 배우기 
 
더 많은 심층 Fabric 환경 발표 블로그 포스트 읽기:

-	[Fabric 블로그의 Data Factory 환경](https://blog.fabric.microsoft.com/en-us/blog/introducing-data-factory-in-microsoft-fabric/)
-	[Fabric 블로그의 Synapse Data Engineering 환경](https://blog.fabric.microsoft.com/en-us/blog/introducing-synapse-data-engineering-in-microsoft-fabric/)
-	[Fabric 블로그의 Synapse Data Science 환경](https://blog.fabric.microsoft.com/en-us/blog/introducing-synapse-data-science-in-microsoft-fabric/)
-	[Fabric 블로그의 Synapse Data Warehousing 환경](https://blog.fabric.microsoft.com/en-us/blog/introducing-synapse-data-warehouse-in-microsoft-fabric/)
-	[Fabric 블로그의 Synapse Real-Time Analytics 환경](https://blog.fabric.microsoft.com/en-us/blog/sense-analyze-and-generate-insights-with-synapse-real-time-analytics-in-microsoft-fabric/)
-	[Power BI 발표 블로그](https://powerbi.microsoft.com/en-us/blog/empower-power-bi-users-with-microsoft-fabric-and-copilot/)
-	[Fabric 블로그의 Data Activator 환경](https://blog.fabric.microsoft.com/en-us/blog/driving-actions-from-your-data-with-data-activator/)
-	[Fabric 블로그의 관리 및 거버넌스](https://blog.fabric.microsoft.com/en-us/blog/administration-security-and-governance-in-microsoft-fabric/)
-	[Fabric 블로그의 OneLake](https://blog.fabric.microsoft.com/en-us/blog/microsoft-onelake-in-fabric-the-onedrive-for-data/)
-	[Dataverse 및 Microsof t Fabric 통합 블로그](https://cloudblogs.microsoft.com/dynamics365/it/2023/05/24/new-dataverse-enhancements-and-ai-powered-productivity-with-microsoft-365-copilot/)


© 2023 Microsoft Corporation. All rights reserved.
이 데모/랩을 사용하면 다음 조건에 동의하게 됩니다.
이 데모/랩에 설명된 기술/기능은 학습 환경을 제공하고 사용자 의견을 얻기 위해 Microsoft Corporation에서 제공합니다. 데모/랩을 통해서만 이러한 기술적 특성과 기능을 평가하고 사용자 의견을 Microsoft에 제시할 수 있습니다. 다른 용도로는 사용할 수 없습니다. 이 데모/랩 또는 그 일부에 대해 수정, 복사, 배포, 전송, 표시, 수행, 재현, 게시, 라이선스 허여, 파생 작업 생성, 양도 또는 판매할 수 없습니다.
추가 복제 또는 재배포를 위한 다른 서버 또는 위치에 대한 데모/랩(또는 그 일부)의 복사 또는 재현은 명시적으로 금지됩니다.
이 데모/랩은 위에서 명시한 목적을 위해 복잡한 설정 또는 설치가 없는 시뮬레이션된 환경에서 잠재적인 새로운 기능과 개념을 포함하여 특정 소프트웨어 기술/제품의 특성 및 기능을 제공합니다. 이 데모/랩에서 서술된 기술/개념은 전체 기능을 나타내지 않을 수 있으며, 최종 버전이 작동하지 않을 수도 있습니다. 또한 해당 기능 또는 개념의 최종
버전을 릴리스하지 않을 수도 있습니다. 또한 실제 환경에서 이러한 특성과 기능을 사용한 경험이 다를 수도 있습니다.
 
**피드백.** 이 데모/랩에서 서술된 기술적 특성, 기능 및/또는 개념에 대한 사용자 의견을
Microsoft에 제시하면 Microsoft는 이 사용자 의견을 어떤 방식과 목적으로든 무료로 사용, 공유 및 상용화할 수 있습니다. 또한 제품, 기술 및 서비스에서 사용자 의견이 포함된
Microsoft 소프트웨어 또는 서비스의 특정 부분을 사용하거나 인터페이스하는 데 필요한 모든 특허권을 제3자에게 무료로 제공합니다. Microsoft에서 사용자 의견을 포함하기 때문에 Microsoft에서 해당 소프트웨어 또는 설명서의 사용을 인가해야 하는 라이선스에 종속된 사용자 의견은 제공할 수 없습니다. 이러한 권리는 본 계약에 의거하여 유효합니다.
Microsoft Corporation은 이에 따라 명시적, 묵시적 또는 법적 특정 목적에의 적합성, 권리 및 비침해 여부에 관계없이 모든 보증과 조건을 포함하여 데모/랩과 관련된 모든 보증 및 조건을 부인합니다. Microsoft는 어떤 목적으로든 결과의 정확성, 데모/랩의 사용으로 파생된 출력 또는 데모/랩에 포함된 정보의 적합성과 관련하여 어떠한 보증이나 진술도 하지 않습니다.

**고지 사항**
이 데모/랩에는 Microsoft Power BI의 새로운 기능 및 향상된 기능 중 일부만 포함되어 있습니다. 일부 기능은 제품의 향후 릴리스에서 변경될 수 있습니다. 이 데모/랩에서는 새로운 기능 모두가 아닌 일부에 대해 학습하게 됩니다.

