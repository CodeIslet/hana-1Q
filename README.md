## 하나은행 1Q 프로 거래 데이터 수집 프로그램
<hr/>

이 프로그램은 하나은행 1Q 프로 HTS API 특성상 윈도우즈 OS에서만 구동 가능하며 하나 1Q API와 증권 계정을 필수로 합니다.

### 설치

1. 하나 1Q API 설치
   
   다운로드: <a href="https://www.hanaw.com/main/customer/customer/CS_050600_T1.cmd">Hana 1Q API</a>

2. 1Q open API 에이전트 등록
   ```
   > CD 1QApiAgent
   1QApiAgent> regHFCommAgent.bat
   1QApiAgent> regsvr32 /S HFCommAgent.dll
   ```
   
3. 파이썬 설치 (x86, 32비트)


4. requirements.txt 의존성 설치


### 실행
```
python main.py -e local -l WARN
```
실행 옵션
- e : 실행 모드로 resource 에 environment-{mode}.json 파일에 해당 됩니다.
- l : 로그 레벨
