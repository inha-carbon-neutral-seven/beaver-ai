<div align="center">
  <br>
<p align="center" width="100%">
    <img src="docs/images/logo.png" alt="beaver icon" style="width: 140px; height:140px; display: block; margin: auto; border-radius: 80%;">
</p>
  
  <h2>비버.ai, 일반 소매업자를 위한 데이터 분석 서비스</h2></hr>
  <p align="center">
    <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" alt="React badge">
    <img src="https://img.shields.io/badge/Redux-593d88?style=flat-square&logo=redux&logoColor=white" alt="Redux badge">
    <img src="https://img.shields.io/badge/Tailwind CSS-38B2A?style=flat-square&logo=Tailwind CSS&logoColor=white"/>
    <img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=Node.js&logoColor=white"/>
    <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=Docker&logoColor=white"/>
    <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=FastAPI&logoColor=white" alt="FastAPI badge">
    <img src="https://img.shields.io/badge/LangChain-339933?style=flat-square&logo=GitHub&logoColor=white" alt="LangChain badge">
    <img src="https://img.shields.io/badge/pandas-%23150458.svg?style=flat-square&logo=pandas&logoColor=white" alt="Pandas badge">
    <img src="https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=flat-square&logo=scikit-learn&logoColor=white" alt="Scikit-learn badge">
    <img src="https://img.shields.io/badge/FastChat-0467DF?style=flat-square&logo=GitHub&logoColor=white" alt="FastChat badge">
    <img src="https://img.shields.io/badge/Huggingface-FFD21E?style=flat-square&logo=huggingface&logoColor=white" alt="Huggingface badge">
    <img src="https://img.shields.io/badge/chatGPT-74aa9c?style=flat-square&logo=openai&logoColor=white" alt="ChatGPT badge">
  <!-- https://github.com/Ileriayo/markdown-badges for more badge -->
</div>

## 비버.ai 소개

- **비버.ai**는 일반 소매업자가 데이터 분석을 쉽게 할 수 있도록 돕는 서비스입니다.
- **소매업 파일을 첨부**하면 맞춤형 대시보드와 데이터 분석 인사이트를 제공합니다.
- **서비스에 LLM을 결합**하여 정규화되지 않은 다양한 데이터를 이해하고, 사용자에게 자연어 인터페이스를 제공합니다.

## 비버.ai 주요 기능

- 파일 내용을 분석하고, 맞춤형 정보로 가공해 대시보드 형태로 제공합니다.
    <details>
    <summary><b>맞춤형 대시보드</b></summary>

  ![image](docs/images/맞춤형-대시보드.gif)
    </details>

- 소매업자의 요청에 맞추어 데이터 분석을 돕습니다.
    <details>
    <summary><b>데이터 분석 지원</b></summary>
    
    ![image](docs/images/테이블-질의응답.gif)
    </details>
- 첨부한 문서로부터 믿을 수 있는 다양한 인사이트를 제공합니다.
    <details>
    <summary><b>문서로부터 인사이트 제공</b></summary>

  ![image](docs/images/문서-질의응답.gif)
    </details>

## 팀원 구성 및 역할 분담

|                                                                 **서강문**                                                                  |                                                                  **백범성**                                                                  |                                                               **최승혁**                                                                |                                                              **강민우**                                                              |                                                                 **최보근**                                                                  |
| :-----------------------------------------------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------: |
| [<img src="https://avatars.githubusercontent.com/u/100016044?v=4" height=150 width=150> <br/> @KangmoonSeo](https://github.com/KangmoonSeo) | [<img src="https://avatars.githubusercontent.com/u/80192345?v=4" height=150 width=150> <br/> @highcloud100](https://github.com/highcloud100) | [<img src="https://avatars.githubusercontent.com/u/117180508?v=4" height=150 width=150> <br/> @ColdTbrew](https://github.com/ColdTbrew) | [<img src="https://avatars.githubusercontent.com/u/69228100?v=4" height=150 width=150> <br/> @hemaher0](https://github.com/hemaher0) | [<img src="https://avatars.githubusercontent.com/u/136104922?v=4" height=150 width=150> <br/> @ChoiBoKeun1](https://github.com/ChoiBoKeun1) |
|                                  팀장<br/> 백엔드 개발 </br> LLM 결합 로직 개발</br> 모델 서버 관리 </br>                                  |                                       웹 개발 환경 구축</br> 개발 CI/CD 관리 </br> 모델 서버 및 최적화                                       |                                     오픈 소스 모델 평가<br> LLM 로직 개발 지원 </br> 모델 서버 관리                                     |                       프론트엔드 개발 </br> 대시보드 기획 </br> 대시보드 인터페이스 제작</br> 형태소 분석 기획                       |                                  프론트엔드 개발</br> 프론트엔드 프로젝트 관리 </br> 채팅 인터페이스 제작                                   |

## 개발 기간

2023.09.26. ~ 2024.02.27. (6개월)

## 서비스 아키텍처

<img src="https://raw.githubusercontent.com/inha-carbon-neutral-seven/beaver-web-client/38a00bd4a568ac22022d60abc8eee145ee76b663/src/image/Architecture.png"/>

- `React 프론트엔드`, `FastAPI 백엔드`, `GPU 모델 서버`로 구성
- `GPU 모델 서버`는 HuggingFace 오픈 소스 LLM과 OpenAI 교체하며 사용
  - A100, A40 GPU에 오픈 소스 LLM `ldcc-solar-10.7b`, `llama2-13b-dpo-v7` 탑재
  - OpenAI `gpt-3.5-turbo-0125`, `gpt-4-0125-preview`
