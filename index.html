# js251120
js251120

<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>Real-time Moving Particles</title>
    <style>
        /* 화면의 여백을 없애고 꽉 채웁니다 */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            overflow: hidden; /* 스크롤 방지 */
            background-color: #1a1a1a; /* 어두운 배경 */
        }
        canvas {
            display: block; /* 캔버스 위치 잡기 */
        }
    </style>
</head>
<body>

    <canvas id="canvas1"></canvas>

    <script>
        const canvas = document.getElementById('canvas1');
        const ctx = canvas.getContext('2d');

        // 캔버스 크기를 브라우저 창 크기에 맞춤
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;

        let particlesArray;

        // 마우스 위치 저장
        let mouse = {
            x: null,
            y: null,
            radius: 100 // 마우스 주변 반응 반경
        }

        // 마우스 움직임 감지
        window.addEventListener('mousemove', function(event) {
            mouse.x = event.x;
            mouse.y = event.y;
        });

        // 파티클(입자) 클래스 정의
        class Particle {
            constructor(x, y, directionX, directionY, size, color) {
                this.x = x;
                this.y = y;
                this.directionX = directionX; // X축 이동 속도
                this.directionY = directionY; // Y축 이동 속도
                this.size = size;
                this.baseSize = size; // 원래 크기 기억
                this.color = color;
            }

            // 그리기 함수
            draw() {
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2, false);
                ctx.fillStyle = this.color;
                ctx.fill();
            }

            // 위치 업데이트 함수 (핵심 로직)
            update() {
                // 1. 화면 경계에 닿으면 방향 반전 (튕기기 효과)
                if (this.x > canvas.width || this.x < 0) {
                    this.directionX = -this.directionX;
                }
                if (this.y > canvas.height || this.y < 0) {
                    this.directionY = -this.directionY;
                }

                // 2. 마우스와의 충돌(반응) 감지
                let dx = mouse.x - this.x;
                let dy = mouse.y - this.y;
                let distance = Math.sqrt(dx*dx + dy*dy);

                if (distance < mouse.radius) {
                    // 마우스 근처에 있으면 커짐
                    if (this.size < this.baseSize * 5) {
                        this.size += 3;
                    }
                } else {
                    // 멀어지면 원래 크기로 복귀
                    if (this.size > this.baseSize) {
                        this.size -= 3;
                    }
                }

                // 3. 위치 이동
                this.x += this.directionX;
                this.y += this.directionY;

                // 4. 그리기
                this.draw();
            }
        }

        // 파티클 초기화 함수
        function init() {
            particlesArray = [];
            let numberOfParticles = (canvas.height * canvas.width) / 9000; // 화면 크기에 비례해 개수 조절

            for (let i = 0; i < numberOfParticles; i++) {
                let size = (Math.random() * 5) + 1;
                let x = (Math.random() * ((innerWidth - size * 2) - (size * 2)) + size * 2);
                let y = (Math.random() * ((innerHeight - size * 2) - (size * 2)) + size * 2);
                let directionX = (Math.random() * 2) - 1; // -1 ~ 1 사이의 속도
                let directionY = (Math.random() * 2) - 1;
                let color = 'rgba(255, 255, 255, 0.8)'; // 흰색

                particlesArray.push(new Particle(x, y, directionX, directionY, size, color));
            }
        }

        // 애니메이션 루프 (계속 반복 실행)
        function animate() {
            requestAnimationFrame(animate); // 다음 프레임 요청
            ctx.clearRect(0, 0, innerWidth, innerHeight); // 화면 지우기 (잔상 제거)

            for (let i = 0; i < particlesArray.length; i++) {
                particlesArray[i].update();
            }
        }

        // 창 크기 변경 시 대응
        window.addEventListener('resize', function() {
            canvas.width = innerWidth;
            canvas.height = innerHeight;
            init();
        });

        // 실행
        init();
        animate();

    </script>
</body>
</html>
