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
    <div class="portfolio-item" data-full="https://picsum.photos/1200/800?random=6"><img src="https://picsum.photos/300/300?random=6" alt="작업 6"><div class="overlay"><p>06</p></div></div>
    <div class="portfolio-item" data-full="https://picsum.photos/1200/800?random=7"><img src="https://picsum.photos/300/300?random=7" alt="작업 7"><div class="overlay"><p>07</p></div></div>
    <div class="portfolio-item" data-full="https://picsum.photos/1200/800?random=8"><img src="https://picsum.photos/300/300?random=8" alt="작업 8"><div class="overlay"><p>08</p></div></div>
    <div class="portfolio-item" data-full="https://picsum.photos/1200/800?random=9"><img src="https://picsum.photos/300/300?random=9" alt="작업 9"><div class="overlay"><p>09</p></div></div>
    <div class="portfolio-item" data-full="https://picsum.photos/1200/800?random=10"><img src="https://picsum.photos/300/300?random=10" alt="작업 10"><div class="overlay"><p>10</p></div></div>

    <!-- 3행 -->
    <div class="portfolio-item" data-full="https://picsum.photos/1200/800?random=11"><img src="https://picsum.photos/300/300?random=11" alt="작업 11"><div class="overlay"><p>11</p></div></div>
    <div class="portfolio-item" data-full="https://picsum.photos/1200/800?random=12"><img src="https://picsum.photos/300/300?random=12" alt="작업 12"><div class="overlay"><p>12</p></div></div>
    <div class="portfolio-item" data-full="https://picsum.photos/1200/800?random=13"><img src="https://picsum.photos/300/300?random=13" alt="작업 13"><div class="overlay"><p>13</p></div></div>
    <div class="portfolio-item" data-full="https://picsum.photos/1200/800?random=14"><img src="https://picsum.photos/300/300?random=14" alt="작업 14"><div class="overlay"><p>14</p></div></div>
    <div class="portfolio-item" data-full="https://picsum.photos/1200/800?random=15"><img src="https://picsum.photos/300/300?random=15" alt="작업 15"><div class="overlay"><p>15</p></div></div>

    <!-- 4행 -->
    <div class="portfolio-item" data-full="https://picsum.photos/1200/800?random=16"><img src="https://picsum.photos/300/300?random=16" alt="작업 16"><div class="overlay"><p>16</p></div></div>
    <div class="portfolio-item" data-full="https://picsum.photos/1200/800?random=17"><img src="https://picsum.photos/300/300?random=17" alt="작업 17"><div class="overlay"><p>17</p></div></div>
    <div class="portfolio-item" data-full="https://picsum.photos/1200/800?random=18"><img src="https://picsum.photos/300/300?random=18" alt="작업 18"><div class="overlay"><p>18</p></div></div>
    <div class="portfolio-item" data-full="https://picsum.photos/1200/800?random=19"><img src="https://picsum.photos/300/300?random=19" alt="작업 19"><div class="overlay"><p>19</p></div></div>
    <div class="portfolio-item" data-full="https://picsum.photos/1200/800?random=20"><img src="https://picsum.photos/300/300?random=20" alt="작업 20"><div class="overlay"><p>20</p></div></div>

    <!-- 5행 -->
    <div class="portfolio-item" data-full="https://picsum.photos/1200/800?random=21"><img src="https://picsum.photos/300/300?random=21" alt="작업 21"><div class="overlay"><p>21</p></div></div>
    <div class="portfolio-item" data-full="https://picsum.photos/1200/800?random=22"><img src="https://picsum.photos/300/300?random=22" alt="작업 22"><div class="overlay"><p>22</p></div></div>
    <div class="portfolio-item" data-full="https://picsum.photos/1200/800?random=23"><img src="https://picsum.photos/300/300?random=23" alt="작업 23"><div class="overlay"><p>23</p></div></div>
    <div class="portfolio-item" data-full="https://picsum.photos/1200/800?random=24"><img src="https://picsum.photos/300/300?random=24" alt="작업 24"><div class="overlay"><p>24</p></div></div>
    <div class="portfolio-item" data-full="https://picsum.photos/1200/800?random=25"><img src="https://picsum.photos/300/300?random=25" alt="작업 25"><div class="overlay"><p>25</p></div></div>
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
