<html lang="ko">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>5x5 디자인 포트폴리오</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: 'Pretendard', -apple-system, BlinkMacSystemFont, system-ui, sans-serif;
      background-color: #0d0d0e;
      color: #ffffff;
      padding: 40px 20px;
    }

    header {
      text-align: center;
      margin-bottom: 30px;
    }

h1 {
      font-color:#ffffff
    }
    header h1 {
      font-size: 2rem;
      font-weight: 700;
      letter-spacing: -0.5px;
    }

    /* 5x5 그리드 핵심 설정 */
    .portfolio-grid {
      display: grid;
      /* 가로 5칸 */
      grid-template-columns: repeat(5, 1fr);
      /* 세로 5칸 */
      grid-template-rows: repeat(5, 1fr);
      gap: 12px;
      max-width: 1200px;
      margin: 0 auto;
    }

    /* 썸네일 아이템 */
    .portfolio-item {
      position: relative;
      aspect-ratio: 1 / 1; /* 정사각형 유지 */
      overflow: hidden;
      border-radius: 6px;
      cursor: pointer;
      background-color: #1a1a1e;
    }

    .portfolio-item img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.3s ease;
    }

    .portfolio-item:hover img {
      transform: scale(1.08);
    }

    /* 마우스 올렸을 때 어두워지는 호버 효과 */
    .overlay {
      position: absolute;
      inset: 0;
      background: rgba(0, 0, 0, 0.5);
      opacity: 0;
      transition: opacity 0.3s ease;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .portfolio-item:hover .overlay {
      opacity: 1;
    }

    .overlay p {
      font-size: 0.85rem;
      font-weight: 600;
    }

    /* 원본 보기 모달 (팝업) */
    .modal {
      display: none;
      position: fixed;
      inset: 0;
      z-index: 1000;
      background-color: rgba(0, 0, 0, 0.9);
      backdrop-filter: blur(5px);
      align-items: center;
      justify-content: center;
      padding: 20px;
    }

    .modal.active {
      display: flex;
    }

    .modal-content {
      max-width: 90vw;
      max-height: 90vh;
      object-fit: contain;
      border-radius: 4px;
    }

    .close-btn {
      position: absolute;
      top: 20px;
      right: 30px;
      font-size: 32px;
      color: #fff;
      cursor: pointer;
    }

    /* 화면 폭이 좁은 모바일 대응 */
    @media (max-width: 768px) {
      .portfolio-grid {
        grid-template-columns: repeat(3, 1fr); /* 모바일에서는 3열로 자동 조절 */
      }
    }
  </style>
</head>
<body>

  <header>
    <h1>PORTFOLIO</h1>
  </header>

  <!-- 5가로 x 5세로 (총 25개) 그리드 -->
  <main class="portfolio-grid">
    <!-- 1행 -->
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/10867cff-2955-4a77-bdb8-8ccb5f5409aa"><img src="https://github.com/user-attachments/assets/7486cf3a-938c-4ff7-8410-ad3fc59f0e14" alt="작업 1"><div class="overlay"><p>01</p></div></div>
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/0892cfc7-21ba-4307-8e7d-e9611f85e185"><img src="https://github.com/user-attachments/assets/43ac315f-a48c-43e5-be1d-a41ece1792ac" alt="작업 2"><div class="overlay"><p>02</p></div></div>
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/1ab8f8af-2ff9-4ed7-b1cc-4267488fea50"><img src="https://github.com/user-attachments/assets/f2dd1abc-c4d4-4852-8b4b-c517e32f9f05" alt="작업 3"><div class="overlay"><p>03</p></div></div>
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/c8cd698f-8a82-41dd-9c6a-a9bf7ac74829"><img src="https://github.com/user-attachments/assets/553e84d7-5647-410e-8761-7aa8368a38b8" alt="작업 4"><div class="overlay"><p>04</p></div></div>
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/244be195-faf9-4340-83f4-5c98b29fa59f"><img src="https://github.com/user-attachments/assets/d6f4bcdd-c0c6-4207-9c1f-700b90e3a1a1" alt="작업 5"><div class="overlay"><p>05</p></div></div>

    <!-- 2행 -->
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/bef591c0-57a0-45a0-92a1-9257b8996c39"><img src="https://github.com/user-attachments/assets/a5dd6ba6-aaf9-4b31-bdc0-6997986491a6" alt="작업 6"><div class="overlay"><p>06</p></div></div>
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/dd12fe19-0acd-4c4d-b1b2-9aaa88c386bc"><img src="https://github.com/user-attachments/assets/fa186cd9-1a65-4d78-a288-4ea5b530d81b" alt="작업 7"><div class="overlay"><p>07</p></div></div>
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/4a4ab21d-d761-411e-b6e2-aaa90065acc0"><img src="https://github.com/user-attachments/assets/57d947d6-f4a4-4446-b977-f7624998424a" alt="작업 8"><div class="overlay"><p>08</p></div></div>
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/86e83d1d-378d-47c6-bc54-8c81914d436c"><img src="https://github.com/user-attachments/assets/74e51dad-4ec5-4c4a-b9a2-ef4d8a5511ad" alt="작업 9"><div class="overlay"><p>09</p></div></div>
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/03f94d29-4c49-4efb-8a90-eec3a8959e32"><img src="https://github.com/user-attachments/assets/2d0d807f-5ab2-4036-8c2e-27812679d0a3" alt="작업 10"><div class="overlay"><p>10</p></div></div>

    <!-- 3행 -->
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/28959035-82ee-45fd-ad26-dd15cbaf780a"><img src="https://github.com/user-attachments/assets/f7d74748-9e6e-4850-bf10-872d0d998f18" alt="작업 11"><div class="overlay"><p>11</p></div></div>
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/c5900e07-8f26-4c31-9726-35f7ad49912b"><img src="https://github.com/user-attachments/assets/7cd30817-b683-4b67-9cbf-a9cdb60da639" alt="작업 12"><div class="overlay"><p>12</p></div></div>
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/582014fd-2c11-4b0f-8b8a-e3b10d326913"><img src="https://github.com/user-attachments/assets/5bb4a569-395a-498c-930e-752889ad5d0a" alt="작업 13"><div class="overlay"><p>13</p></div></div>
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/88ea4487-884a-4cad-9fa4-4f6524d6a6cd"><img src="https://github.com/user-attachments/assets/c0211468-6db1-4b7a-b556-84cfea8aeedb" alt="작업 14"><div class="overlay"><p>14</p></div></div>
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/09eb8359-b73f-4639-85d3-893ad4113665"><img src="https://github.com/user-attachments/assets/ee070c58-f4e9-49ce-86d8-7684f5ab82ff" alt="작업 15"><div class="overlay"><p>15</p></div></div>

    <!-- 4행 -->
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/c315e3c2-089c-44cd-aa29-9fec19c2c028"><img src="https://github.com/user-attachments/assets/855590fa-f829-4192-b0bb-de4034c92b17" alt="작업 16"><div class="overlay"><p>16</p></div></div>
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/7d4cf953-5e36-4e41-968a-8d0e158e5270"><img src="https://github.com/user-attachments/assets/16cdeb54-098e-40e0-8e8b-265ad64904a4" alt="작업 17"><div class="overlay"><p>17</p></div></div>
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/cd12fa69-be42-4218-a12b-0800ddc32c73"><img src="https://github.com/user-attachments/assets/b51c9961-3595-40dc-a780-e6955c7fdd61" alt="작업 18"><div class="overlay"><p>18</p></div></div>
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/bd81b83a-38bc-4bb7-bdf9-8651f3a9a4d1"><img src="https://github.com/user-attachments/assets/f84bcedb-af7a-4dfb-9570-7a753f49a007" alt="작업 19"><div class="overlay"><p>19</p></div></div>
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/2a99417e-8f6a-4e55-99d9-74e7cde32c53"><img src="https://github.com/user-attachments/assets/a40d78a5-5883-480e-884b-6ad555b42cf8
" alt="작업 20"><div class="overlay"><p>20</p></div></div>

    <!-- 5행 -->
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/912f9344-fa3d-45cc-b05b-f0b9bd79bb72"><img src="https://github.com/user-attachments/assets/912f9344-fa3d-45cc-b05b-f0b9bd79bb72" alt="작업 21"><div class="overlay"><p>21</p></div></div>
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/bf4f94c3-7ea1-489c-8445-ba4d558df3f5"><img src="https://github.com/user-attachments/assets/2047c9a2-9641-43ef-8e29-6bd41605301e" alt="작업 22"><div class="overlay"><p>22</p></div></div>
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/657a5e9b-2e67-44bb-bdc0-aeec0393c863"><img src="https://github.com/user-attachments/assets/eac89ed4-d804-4fbe-a6ae-b15d5e98b6de" alt="작업 23"><div class="overlay"><p>23</p></div></div>
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/9319472f-cfad-4ecb-a9e2-de3760f5a29e"><img src="https://github.com/user-attachments/assets/796da1de-9269-48ca-b199-89c9cdabc89f" alt="작업 24"><div class="overlay"><p>24</p></div></div>
    <div class="portfolio-item" data-full="https://github.com/user-attachments/assets/a0d28586-23bf-4dfb-97e4-410e8256b8a8"><img src="https://github.com/user-attachments/assets/f726db39-664a-4a08-8d5e-9db43e3d31f9" alt="작업 25"><div class="overlay"><p>25</p></div></div>
  </main>

  <!-- 원본 모달 -->
  <div class="modal" id="imageModal">
    <span class="close-btn" id="closeBtn">&times;</span>
    <img class="modal-content" id="modalImg" alt="원본 이미지">
  </div>

  <script>
    const items = document.querySelectorAll('.portfolio-item');
    const modal = document.getElementById('imageModal');
    const modalImg = document.getElementById('modalImg');
    const closeBtn = document.getElementById('closeBtn');

    items.forEach(item => {
      item.addEventListener('click', () => {
        const fullImgUrl = item.getAttribute('data-full');
        modalImg.src = fullImgUrl;
        modal.classList.add('active');
      });
    });

    closeBtn.addEventListener('click', () => modal.classList.remove('active'));
    modal.addEventListener('click', (e) => {
      if (e.target === modal) modal.classList.remove('active');
    });
    document.addEventListener('keydown', (e) => {
      if (e.key === 'Escape') modal.classList.remove('active');
    });
  </script>
</body>
</html>
