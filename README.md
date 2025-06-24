<!DOCTYPE html>
<html lang="ko">
<head>
  <meta charset="UTF-8">
  <title>일본어 기말 준비하기</title>
  <style>
    body { font-family: sans-serif; text-align: center; margin: 40px; }
    #word-box { font-size: 40px; margin: 30px; font-weight: bold; }
    #answer { font-size: 24px; padding: 10px; width: 300px; }
    #result { margin: 10px; font-size: 18px; color: red; }
    section { display: none; margin-top: 20px; }
    table { margin: 0 auto; border-collapse: collapse; }
    td, th { border: 1px solid #aaa; padding: 10px; font-size: 16px; }
    button { margin: 10px; padding: 10px 20px; font-size: 16px; }
    .nav-button { margin: 10px; }
  </style>
</head>
<body>
  <h1>일본어 기말 준비하기</h1>

  <div>
    <button class="nav-button" onclick="switchSection('quiz')">단어 퀴즈</button>
    <button class="nav-button" onclick="switchSection('sentenceQuiz')">문장 퀴즈</button>
    <button class="nav-button" onclick="switchSection('mistakes')">틀린 단어</button>
    <button class="nav-button" onclick="switchSection('dictionary')">전체 단어</button>
    <button class="nav-button" onclick="switchSection('grammar')">일본어 문법</button>
  </div>

  <section id="quiz">
    <div id="word-box">단어가 여기에 표시됩니다</div>
    <input type="text" id="answer" placeholder="뜻을 적어라">
    <button onclick="checkAnswer()">제출</button>
    <div id="result"></div>
  </section>
  
  <section id="sentenceQuiz">
    <div id="sentence-box" style="font-size: 40px; margin: 20px;"></div>
    <input type="text" id="sentence-answer" placeholder="뜻을 적어라" style="font-size: 20px; padding: 8px; width: 400px;">
    <button onclick="checkSentenceAnswer()">제출</button>
    <div id="sentence-result"></div>
  </section>

  <section id="mistakes">
    <h3>틀린 단어</h3>
    <table><thead><tr><th>일본어</th><th>입력한 뜻</th><th>정답</th></tr></thead><tbody id="mistake-list"></tbody></table>
  </section>

  <section id="dictionary">
    <h3>전체 단어 사전</h3>
    <table><thead><tr><th>일본어</th><th>뜻</th></tr></thead><tbody id="dictionary-list"></tbody></table>
  </section>

    <section id="grammar">
     <h3>일본어 문법</h3>
     <ol style="text-align:left; max-width:800px; margin:0 auto; font-size:16px;">
      <li><strong>탁음:</strong> 부드럽고 느끼하게</li>
      <li><strong>반탁음:</strong> 의성어에 많이 사용</li>
      <li><strong>요음:</strong> や、ゆ、よ를 작게 씀. 앞에는 ‘い’ 발음만 올 수 있음. 두 음절을 합쳐 1박으로 발음</li>
      <li><strong>촉음:</strong> 뒷글자의 자음과 같은 음으로 1박으로 발음.<br>
         - つ+か/き/く/け/こ → [k]<br>
         - つ+さ/し/す/せ/そ → [s]<br>
          - つ+た/ち/つ/て/と → [t]<br>
         - つ+ぱ/ぴ/ぷ/ぺ/ぽ → [p]</li>
     <li><strong>발음:</strong> ん의 뒤 글자에 따라 달라짐 (1박으로 발음)<br>
      - ん+ま/ば/ぱ → [ㅁ]<br>
      - ん+さ/ざ/た/だ/な/ら → [ㄴ]<br>
      - ん+か/が → [ㅇ]<br>
      - ん+あ/は/や/わ/말끝 → [ㄴ/ㅇ]</li>
    <li><strong>장음:</strong> 히라가나의 장음은 あ/い/う/え/お로 표기, 1박으로 발음<br>
      - あ+あ, い+い, う+う, え+え 또는 い, お+お 또는 う</li>
    <li><strong>こんいちは:</strong> 친구끼리는 잘 사용하지 않음. 대신 이름을 부르거나 손을 흔들며 인사</li>
    <li><strong>일본의 구성:</strong><br>
      - 4개의 큰 섬: 훗카이도(ほっかいどう), 혼슈(ほんしゅう), 시코쿠(しこく), 큐슈(きゅうしゅう)<br>
      - 행정 단위: 도도부현(とどうふけん)<br>
      - 수도: 도쿄(とうきょう)<br>
      - 남북으로 길어 지역 간 기후 차 큼, 오키나와는 일 년 내내 따뜻함<br>
      - 소비세 10%<br>
      - 히라가나: 흘림체 46자 / 가타카나: 획이 많고 외래어, 의성어, 의태어, 강조 등에 사용</li>
    <li><strong>4학년 표현:</strong> よねんせい</li>
    <li><strong>존대 표현:</strong><br>
      - 네: はい, ええ > うん (반말)<br>
      - 아니오: いいえ > ううん (반말)</li>
    <li><strong>お/ご의 사용:</strong> 말 앞에 붙어 미화 또는 존경의 의미</li>
    <li><strong>일본인의 방문 예절:</strong> 다른 사람의 집에 방문 시 과자 등 작은 선물 준비. 바닥에 앉을 때는 무릎 꿇고 앉음</li>
    <li><strong>시제:</strong> きます(현재형), きました(과거형)</li>
    <li><strong>일본 주거 문화:</strong><br>
      - 주택 형태: 단독주택(いっこだて), 맨션, 아파트<br>
      - 구조 표기: LDK<br>
      - 도코노마(とこのま): 방바닥보다 약간 높은 장식 공간<br>
      - 다다미(たたみ): 와시쓰(わしつ)에 까는 전통 바닥재<br>
      - 고타쓰(こたつ): 난방용 탁자, 아래에 온열기 설치<br>
      - 욕실과 화장실이 분리된 구조가 많음</li>
    <li><strong>30분 표현:</strong> さんじゅっぷん 또는 はん</li>
    <li><strong>どうぞ의 용법:</strong> 상대에게 권유하거나 물건을 줄 때</li>
    <li><strong>고등학생의 학교생활:</strong><br>
      - 입학: 4월 / 졸업: 다음해 3월<br>
      - 3학기제 운영<br>
      - 방과 후 동아리 활동 (문화부와 운동부)<br>
      - 체육대회 및 문화제(ぶんかさい) 개최. 지역 주민 초청 가능</li>
  </ol>
</section>


  <script>
    const words = [
  { jp: "あかい", kr: "빨갛다" },
  { jp: "おんがく", kr: "음악" },
  { jp: "ちゅうごく", kr: "중국" },
  { jp: "いえ", kr: "집" },
  { jp: "かばん", kr: "가방" },
  { jp: "えき", kr: "역" },
  { jp: "かじ", kr: "화재" },
  { jp: "です", kr: "~입니다" },
  { jp: "かお", kr: "얼굴" },
  { jp: "て", kr: "손" },
  { jp: "ねんせい", kr: "-학년" },
  { jp: "いす", kr: "의자" },
  { jp: "てん", kr: "점" },
  { jp: "すし", kr: "초밥" },
  { jp: "おかあさん", kr: "어머니" },
  { jp: "ちゅうがく", kr: "중학교" },
  { jp: "しち", kr: "7, 칠" },
  { jp: "おにいさん", kr: "형, 오빠" },
  { jp: "だいがく", kr: "대학교" },
  { jp: "ちかてつ", kr: "지하철" },
  { jp: "すうがく", kr: "수학" },
  { jp: "ちち", kr: "아버지" },
  { jp: "つくえ", kr: "책상" },
  { jp: "おねえさん", kr: "누나, 언니" },
  { jp: "はは", kr: "어머니" },
  { jp: "いぬ", kr: "개" },
  { jp: "せんせい", kr: "선생님" },
  { jp: "あね", kr: "누나, 언니" },
  { jp: "ねこ", kr: "고양이" },
  { jp: "おおさか", kr: "오사카" },
  { jp: "あに", kr: "형, 오빠" },
  { jp: "はち", kr: "8, 팔" },
  { jp: "こうこう", kr: "고등학교" },
  { jp: "いもうと", kr: "여동생" },
  { jp: "ひと", kr: "사람" },
  { jp: "おばさん", kr: "아주머니" },
  { jp: "おとうと", kr: "남동생" },
  { jp: "みせ", kr: "가게" },
  { jp: "おばあさん", kr: "할머니" },
  { jp: "そふ", kr: "할아버지" },
  { jp: "なまえ", kr: "이름" },
  { jp: "れい", kr: "0, 영" },
  { jp: "そぼ", kr: "할머니" },
  { jp: "やさい", kr: "채소" },
  { jp: "いち", kr: "1, 일" },
  { jp: "ーさん", kr: "-씨" },
  { jp: "ふゆ", kr: "겨울" },
  { jp: "に", kr: "2, 이" },
  { jp: "これ", kr: "이것" },
  { jp: "ふろ", kr: "목욕, 욕조" },
  { jp: "さん", kr: "3, 삼" },
  { jp: "しゃしん", kr: "사진" },
  { jp: "ろく", kr: "6, 육" },
  { jp: "よん", kr: "4, 사" },
  { jp: "か～", kr: "~? (의문)" },
  { jp: "くすり", kr: "약" },
  { jp: "ご", kr: "5, 오" },
  { jp: "ええ", kr: "네" },
  { jp: "にわ", kr: "정원" },
  { jp: "わたし", kr: "나, 저" },
  { jp: "なな", kr: "7, 칠" },
  { jp: "は～", kr: "~은/는" },
  { jp: "しろい", kr: "하얗다" },
  { jp: "はち", kr: "8, 팔" },
  { jp: "が～", kr: "~이/가" },
  { jp: "はん", kr: "책, 반" },
  { jp: "きゅう", kr: "9, 구" },
  { jp: "うち", kr: "집" },
  { jp: "じゅう", kr: "10, 십" },
  { jp: "いしゃ", kr: "의사" },
  { jp: "おみやげ", kr: "선물" },
  { jp: "じゆう", kr: "자유" },
  { jp: "これから", kr: "앞으로, 이제부터" },
  { jp: "りよう", kr: "이용" },
  { jp: "いちねんかん", kr: "1년간" },
  { jp: "りょうり", kr: "요리" },
  { jp: "どうぞ", kr: "부디, 아무쪼록" },
  { jp: "がっこう", kr: "학교" },
  { jp: "ーちゃん", kr: "~쨩 (친근한 호칭)" },
  { jp: "ーさん", kr: "~씨" },
  { jp: "こちら", kr: "이쪽, 이분" },
  { jp: "けっせき", kr: "결석" },
  { jp: "ほっかいどう", kr: "홋카이도" },
  { jp: "こちらこそ", kr: "저야말로" },
  { jp: "きって", kr: "우표" },
  { jp: "ほんしゅう", kr: "혼슈" },
  { jp: "いっぱい", kr: "가득" },
  { jp: "しこく", kr: "시코쿠" },
  { jp: "きて", kr: "오고, 와서" },
  { jp: "きゅうしゅう", kr: "규슈" },
  { jp: "わしつ", kr: "와시쓰" },
  { jp: "おと", kr: "소리" },
  { jp: "どとうふけん", kr: "도도부현" },
  { jp: "おしいれ", kr: "붙박이장" },
  { jp: "おっと", kr: "남편" },
  { jp: "えん", kr: "엔" },
  { jp: "どこのま", kr: "도코노마" },
  { jp: "さんぽ", kr: "산책" },
  { jp: "にほん", kr: "일본" },
  { jp: "たたみ", kr: "다다미" },
  { jp: "かんじ", kr: "한자" },
  { jp: "かんこく", kr: "한국" },
  { jp: "こたつ", kr: "코타츠" },
  { jp: "～じ", kr: "~시" },
  { jp: "とうきょう", kr: "도쿄" },
  { jp: "ぎゅうどん", kr: "소고기 덮밥" },
  { jp: "まで～", kr: "~까지" },
  { jp: "ふくおか", kr: "후쿠오카" },
  { jp: "じてんしゃ", kr: "자전거" },
  { jp: "えいご", kr: "영어" },
  { jp: "きょうと", kr: "교토" },
  { jp: "ちょっと", kr: "잠시, 조금" },
  { jp: "じゅく", kr: "학원" },
  { jp: "ひめじ", kr: "히메지" },
  { jp: "びょういん", kr: "병원" },
  { jp: "ゆうびんきょく", kr: "우체국" },
  { jp: "おきなわ", kr: "오키나와" },
  { jp: "きみょう", kr: "기묘함" },
  { jp: "ぎんこう", kr: "은행" },
  { jp: "ふじさん", kr: "후지산" },
  { jp: "さっぽろ", kr: "삿포로" },
  { jp: "ゆきまつり", kr: "유키 마츠리 (눈 축제)" },
  { jp: "すいえい", kr: "수영" },
  { jp: "しゅり", kr: "슈리성" },
  { jp: "きょうしつ", kr: "교실" },
  { jp: "なは", kr: "나하" },
  { jp: "さんじゅっぷん", kr: "30분" },
  { jp: "まつやま", kr: "마쓰야마" },
  { jp: "はん", kr: "반" },
  { jp: "きんかくじ", kr: "긴카쿠지 (금각사)" },
  { jp: "しゅみ", kr: "취미" },
  { jp: "どうご", kr: "도고 온천" },
  { jp: "りょこう", kr: "여행" },
  { jp: "いっこだて", kr: "단독주택" },
  { jp: "えいが", kr: "영화" },
  { jp: "おふろ", kr: "욕실" },
  { jp: "やきゅう", kr: "야구" },
  { jp: "ともだち", kr: "친구" },
  { jp: "ーくん", kr: "-군" },
  { jp: "じゃま", kr: "방해" },
  { jp: "まだ", kr: "아직" },
  { jp: "どうも", kr: "정말" },
  { jp: "つぎだよ", kr: "다음이야" },
  { jp: "から", kr: "~에서부터" },
  { jp: "ばくたち", kr: "우리들" },
  { jp: "ね", kr: "알겠지~?" },
  { jp: "れんしゅう", kr: "연습" },
  { jp: "よ", kr: "강조 (~!)" },
  { jp: "げつようび", kr: "월요일" },
  { jp: "かぞく", kr: "가족" },
  { jp: "すいようび", kr: "수요일" },
  { jp: "ぶかつ", kr: "동아리 활동" },
  { jp: "じかん", kr: "시간" },
  { jp: "ここ", kr: "여기" },
  { jp: "ばしょ", kr: "장소" },
  { jp: "ごご", kr: "오후" },
  { jp: "おんがくしつ", kr: "음악실" },
  { jp: "あし", kr: "다리" },
  { jp: "きょねん", kr: "작년" },
  { jp: "あじ", kr: "맛" },
  { jp: "まいとし", kr: "매년" },
  { jp: "あんない", kr: "안내" },
  { jp: "ぶんがさい", kr: "문화제" },
  { jp: "にゅうがく", kr: "입학" },
  { jp: "にんき", kr: "인기" },
  { jp: "おめでとう", kr: "축하해" },
  { jp: "みなさん", kr: "여러분" },
  { jp: "へ～", kr: "~에 (~으로)" },
  { jp: "ぜひ", kr: "꼭" },
  { jp: "かようび", kr: "화요일" },
  { jp: "どようび", kr: "토요일" },
  { jp: "にちようび", kr: "일요일" },
  { jp: "としょかん", kr: "도서관" },
  { jp: "やすみ", kr: "휴일" },
  { jp: "もくようび", kr: "목요일" },
  { jp: "きんようび", kr: "금요일" },
  { jp: "たんじょうび", kr: "생일" }
    ];

    const sentences = [
      { jp: "よろしくおねがいします", kr: "잘 부탁드립니다" },
      { jp: "はじめまして", kr: "처음 뵙겠습니다" },
      { jp: "いってらっしゃい", kr: "다녀오세요" },
      { jp: "いってきます", kr: "다녀오겠습니다" },
      { jp: "こんばんは", kr: "안녕하세요 (저녁)" },
      { jp: "ただいま", kr: "다녀왔습니다" },
      { jp: "そうです", kr: "그렇습니다" },
      { jp: "おはようございます", kr: "안녕하세요 (아침)" },
      { jp: "おかえり", kr: "어서 와" },
      { jp: "こんにちは", kr: "안녕하세요 (낮)" },
      { jp: "さようなら", kr: "안녕히 가세요" },
      { jp: "どうもありがとう", kr: "정말 고마워요" },
      { jp: "じゃまたね", kr: "그럼 안녕" },
      { jp: "またあした", kr: "또 내일 봐요" },
      { jp: "はじめまして。イ・ジスです。", kr: "처음 뵙겠습니다. 이지수입니다." },
      { jp: "ジスさん、わたしのちちとははです。", kr: "지수씨, 저의 아빠와 엄마입니다." },
      { jp: "こんにちは。", kr: "안녕하세요." },
      { jp: "おじゃまします", kr: "실례하겠습니다" },
      { jp: "ここはわたしのうちです。", kr: "여기는 나의 집입니다." },
      { jp: "ただいま。", kr: "다녀왔습니다." },
      { jp: "おかえり。", kr: "어서 와." },
      { jp: "こんにちは。ユイのあねです。", kr: "안녕하세요. 유이의 언니입니다." },
      { jp: "これ、かんこくのおみやげです。", kr: "이거 한국의 선물이에요." },
      { jp: "どうもありがとう。", kr: "정말 고마워요." },
      { jp: "これからいちねんかん、どうぞよろしくおねがいします。", kr: "이제부터 1년간 잘 부탁드립니다." }
    ];

    let currentWord;
    let currentSentence;
    let mistakes = [];

    function shuffleWord() {
      currentWord = words[Math.floor(Math.random() * words.length)];
      document.getElementById("word-box").innerText = currentWord.jp;
      document.getElementById("answer").value = "";
      document.getElementById("result").innerText = "";
    }

    function checkAnswer() {
      const userAnswer = document.getElementById("answer").value.trim();
      if (userAnswer === currentWord.kr) {
        document.getElementById("result").style.color = "green";
        document.getElementById("result").innerText = "정답입니다!";
        setTimeout(shuffleWord, 1000);
      } else {
        document.getElementById("result").style.color = "red";
        document.getElementById("result").innerText = `땡이지롱~ 정답은 '${currentWord.kr}'이였음~`;
        mistakes.push({ ...currentWord, user: userAnswer });
        setTimeout(shuffleWord, 2000);
      }
    }

    function checkSentenceAnswer() {
      const userAnswer = document.getElementById("sentence-answer").value.trim();
      const resultDiv = document.getElementById("sentence-result");
      if (userAnswer === currentSentence.kr) {
        resultDiv.style.color = "green";
        resultDiv.innerText = "정답입니다!";
        setTimeout(shuffleSentence, 1000);
      } else {
        resultDiv.style.color = "red";
        resultDiv.innerText = `이걸 틀리네ㅋ 정답은 '${currentSentence.kr}'였다!!`;
        setTimeout(shuffleSentence, 2000);
      }
    }

    function shuffleSentence() {
      currentSentence = sentences[Math.floor(Math.random() * sentences.length)];
      document.getElementById("sentence-box").innerText = currentSentence.jp;
      document.getElementById("sentence-answer").value = "";
      document.getElementById("sentence-result").innerText = "";
    }

    function switchSection(id) {
      const sections = document.querySelectorAll("section");
      sections.forEach(sec => sec.style.display = "none");

      if (id === 'mistakes') {
        showMistakes();
      } else if (id === 'dictionary') {
        showDictionary();
      } else if (id === 'quiz') {
        shuffleWord();
      } else if (id === 'sentenceQuiz') {
        shuffleSentence();
      }

      document.getElementById(id).style.display = "block";
    }

    function showMistakes() {
      const mistakeList = document.getElementById("mistake-list");
      mistakeList.innerHTML = "";
      mistakes.forEach(m => {
        const row = `<tr><td>${m.jp}</td><td>${m.user}</td><td>${m.kr}</td></tr>`;
        mistakeList.innerHTML += row;
      });
    }

    function showDictionary() {
      const dictList = document.getElementById("dictionary-list");
      dictList.innerHTML = "";
      words.forEach(w => {
        const row = `<tr><td>${w.jp}</td><td>${w.kr}</td></tr>`;
        dictList.innerHTML += row;
      });
    }

    window.onload = () => switchSection('quiz');
  </script>
</body>
</html>
