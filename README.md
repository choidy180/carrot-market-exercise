<!-- BANNER -->
<p align="center">
  <img src="./public/coin.jpg" alt="coin Banner" width="200px" />
</p>

<h1 align="center">🪙 COIN TRACKER</h1>
<p align="center">
  <b>암호화폐의 시세와 그래프를 확인할 수 있는 리액트 + 타입스크립트 프로젝트</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=React&logoColor=white"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=TypeScript&logoColor=white"/>
  <img src="https://img.shields.io/badge/ReactQuery-FF4154?style=flat-square&logo=ReactQuery&logoColor=white"/>
  <img src="https://img.shields.io/badge/ReactRouter-CA4245?style=flat-square&logo=ReactRouter&logoColor=white"/>
  <img src="https://img.shields.io/badge/ApexCharts-0F7BFF?style=flat-square&logo=apachespark&logoColor=white"/>
  <img src="https://img.shields.io/badge/Recoil-3578E5?style=flat-square&logo=recoil&logoColor=white"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=JavaScript&logoColor=000"/>
</p>

---

##  기능
- 📈 실시간 시세 확인 (React Query)
- 📊 코인 차트 (ApexCharts)
- 🧭 중첩 라우팅 (React Router)
- 🌓 다크/라이트 테마 (Recoil)
- 🧩 타입 세이프티 (TypeScript 인터페이스)
- 🧠 SEO 최적화 (React Helmet)
---

##  기술 스택
<p align="center">
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=React&logoColor=white"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=TypeScript&logoColor=white"/>
  <img src="https://img.shields.io/badge/ReactQuery-FF4154?style=flat-square&logo=ReactQuery&logoColor=white"/>
  <img src="https://img.shields.io/badge/ReactRouter-CA4245?style=flat-square&logo=ReactRouter&logoColor=white"/>
  <img src="https://img.shields.io/badge/ApexCharts-0F7BFF?style=flat-square&logo=apachespark&logoColor=white"/>
  <img src="https://img.shields.io/badge/Recoil-3578E5?style=flat-square&logo=recoil&logoColor=white"/>
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=JavaScript&logoColor=000"/>
</p>

---

##  라이브 데모
-  URL: 현재 미배포

---

##  프로젝트 요약
#### 1. 코인의 정보와 시세표 제공
#### 2. 코인 검색 및 화폐단위별, 국가별 시세 그래프 제공
#### 3. 테마와 그래프 선택하여 사용자가 원하는 정보로 볼 수 있는 기능 제공



##  Install
```bash
# 1) 레포지토리 복제
git clone https://github.com/choidy180/React_coin_tracking_application
cd poke-next

# 2) 의존성 설치
npm install

# 3) 개발 서버 실행
npm run dev
# 브라우저에서 http://localhost:3000, http://127.0.0.1:3000 열기
```

## 📡 Example Code (Coin Api)
```bash

const BASE_URL = `https://api.coinpaprika.com/v1`

export function fetchCoins() {
  return fetch(`${BASE_URL}/coins`).then((response) => 
    response.json()
  );
}

export function fetchCoinInfo(coinId:string){
  return fetch(`${BASE_URL}/coins/${coinId}`).then((response) => 
    response.json()
  );
}

export function fetchCoinTickers(coinId:string){
  return fetch(`${BASE_URL}/tickers/${coinId}`).then((response) => 
    response.json()
  );
}

export function fetchCoinHistory(coinId:string){
  // 종료
  const endDate = Math.floor(Date.now() / 1000);
  // 시작
  const startDate = endDate - 60 * 60 * 24 * 7; 
  return fetch(
    `${BASE_URL}/coins/${coinId}/ohlcv/historical?start=${startDate}&end=${endDate}`
  ).then((response) => response.json());
}
});
```

