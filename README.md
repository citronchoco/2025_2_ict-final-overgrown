# light-shadow-garden
정문기입 기말 프로젝트 git 저장소

### 개발 환경 및 협업 규칙

각자 코드를 짜서 하나로 합쳐야 하기 때문에, 아래 내용은 반드시 통일해주세요.

**1. 코드 편집기 (IDE) 통일** - 설치와 초기 설정 방법은 정문기입 수업 초반 자료에 있습니다.

- VS Code (Visual Studio Code)
- 필수 확장프로그램: Live Server (Ritwick Dey 제작)

**2. 폴더 구조**

각자 컴퓨터의 폴더 구조가 다르면 이미지를 못 불러옵니다. 아래 구조를 똑같이 맞춰주세요.

```
ProjectName/
├── index.html
├── style.css
├── sketch.js      (메인 코드)
├── classes/       (클래스를 모아 둔 폴더 - 나중에 합칠 때 편함)
│   ├── Plant.js
│   ├── Moss.js
│   └── Light.js
└── assets/        (이미지 리소스 폴더)
    ├── plant/     (식물 관련 이미지)
    │   ├── stem_01.png
    │   └── flower_01.png
    └── moss/      (이끼 관련 이미지)
        └── moss_texture.png
```
- **프로젝트 폴더명(-> ProjectName/)**: 2024_2_ICT_Final_Overgrown
- 프로젝트 폴더명 로컬 환경에서도 통일해주세요
- 파일은 알아서 추가되니 
- index.html, style.css, sketch.js는 vscode에서 create p5.js project 하면 자동으로 생성됩니다.
- **주의:** 파일명은 모두 **소문자 영문**으로 통일합니다. (띄어쓰기 금지, `stem_01.png` O, `Stem 1.png` X)

**3. 캔버스 크기 및 p5.js 버전**

- HTML 라이브러리: `index.html`에 넣을 p5.js 스크립트 링크 통일 - 수업시간에 클래스 생성 시 넣는 코드 배운 대로
- Canvas Size: 1024 x 768

**4. 변수명 명명 규칙 (Naming Convention)**

- **변수/함수:** camelCase (첫 글자 소문자, 단어 바뀔 때 대문자)
- **클래스:** PascalCase (첫 글자 대문자)
    - 예: `class Plant {}`, `class Moss {}`

**5. 이미지 로딩 방식 약속**

- 이미지가 없어도 코드는 돌아가야 하므로, 각자 더미 이미지를 넣고 테스트하되 **코드는 아래와 같이 작성**해 주세요.
- 다만 이미지 변수명은 각자 구현하고자 하는 것에 맞게 변경
```
let img;
function preload() {
   // 경로는 무조건 'assets/폴더명/파일명' 기준
   img = loadImage('assets/plant/stem_01.png'); 
}
```

### 변수명 정리

