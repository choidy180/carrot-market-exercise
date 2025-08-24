<!-- BANNER -->
<p align="center">
  <img src="./public/carrot.jpg" alt="coin Banner" width="200px" />
</p>

<h1 align="center">🪙 COIN TRACKER</h1>
<p align="center">
  <b>Next.js와 Tailwinds CSS를 이용한 당근마켓 클론코딩</b>
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
- 🌈 게시물 등록 및 확인
- 📃 등록자와 채팅으로 대화나누기
- ✏️ 게시물 정렬 기능 리스트업
---

##  기술 스택
<p align="center">
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=React&logoColor=white"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=TypeScript&logoColor=white"/>
  <img src="https://img.shields.io/badge/ReactRouter-CA4245?style=flat-square&logo=ReactRouter&logoColor=white"/>
  <img src="https://img.shields.io/badge/Recoil-3578E5?style=flat-square&logo=recoil&logoColor=white"/>
  <img src="https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white"/>
  <img s현



##  Install
```bash
# 1) 레포지토리 복제
git clone https://github.com/choidy180/carrot-market-exercise
cd poke-next

# 2) 의존성 설치
npm install

# 3) 개발 서버 실행
npm run dev
# 브라우저에서 http://localhost:3000, http://127.0.0.1:3000 열기
```

## 📡 Example Code (input component)
```bash

interface InputProps {
  label: string;
  name: string;
  kind?: "text" | "phone" | "price";
  [key: string]: any;
}

export default function Input({
  label,
  name,
  kind = "text",
  ...rest
}: InputProps) {
  return (
    <div>
      <label
        className="mb-1 block text-sm font-medium text-gray-700"
        htmlFor={name}
      >
        {label}
      </label>
      {kind === "text" ? (
        <div className="rounded-md relative flex  items-center shadow-sm">
          <input
            id={name}
            {...rest}
            className="appearance-none w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm placeholder-gray-400 focus:outline-none focus:ring-orange-500 focus:border-orange-500"
          />
        </div>
      ) : null}
      {kind === "price" ? (
        <div className="rounded-md relative flex  items-center shadow-sm">
          <div className="absolute left-0 pointer-events-none pl-3 flex items-center justify-center">
            <span className="text-gray-500 text-sm">$</span>
          </div>
          <input
            id={name}
            {...rest}
            className="appearance-none pl-7 w-full px-3 py-2 border border-gray-300 rounded-md shadow-sm placeholder-gray-400 focus:outline-none focus:ring-orange-500 focus:border-orange-500"
          />
          <div className="absolute right-0 pointer-events-none pr-3 flex items-center">
            <span className="text-gray-500">KRW</span>
          </div>
        </div>
      ) : null}
      {kind === "phone" ? (
        <div className="flex rounded-md shadow-sm">
          <span className="flex items-center justify-center px-3 rounded-l-md border border-r-0 border-gray-300 bg-gray-50 text-gray-500 select-none text-sm">
            +82
          </span>
          <input
            id={name}
            {...rest}
            className="appearance-none w-full px-3 py-2 border border-gray-300 rounded-md rounded-l-none shadow-sm placeholder-gray-400 focus:outline-none focus:ring-orange-500 focus:border-orange-500"
          />
        </div>
      ) : null}
    </div>
  );
}
```

