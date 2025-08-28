# furmunity
회사 소개
<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Furmunity | 확장된 브랜드 스토리</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Noto+Sans+KR:wght@300;400;500;700;900&display=swap" rel="stylesheet">
    <!-- Chosen Palette: Warm Neutrals & Soft Coral -->
    <!-- Application Structure Plan: This expanded version maintains the narrative-driven, single-page scrolling structure, but breaks the content into more detailed, distinct sections to deepen the storytelling. The flow now progresses from a detailed 'Problem Statement' to a comprehensive 'Solution' section that elaborates on the core slogan, then to a multi-layered 'Vision' section that visualizes the transition from a hardware product to a global data platform. This enriched structure allows for a more immersive user experience, providing a complete and cohesive brand story. Key interactions are enhanced with a more complex flow diagram and a dynamic chart that visualizes the expanded service ecosystem. -->
    <!-- Visualization & Content Choices: 1. Problem Statement: Report Info -> Pain points of pet owners. Goal -> Explain & empathize. Viz -> Detailed text blocks with subtle fade-in animation. Justification -> Emotional connection is crucial for the brand's 'Why.' 2. Slogan Breakdown: Report Info -> 'Capture, Connect, Cherish.' Goal -> Inform & detail. Viz -> Three interactive, card-like sections with expanded text content. Interaction -> Clicking or hovering reveals more descriptive text for each concept. Justification -> Breaks down the abstract slogan into tangible actions and values. 3. Vision Flow: Report Info -> Business model evolution (PetBooth -> Data -> Services). Goal -> Organize & visualize complex expansion. Viz -> A multi-stage HTML/CSS flow diagram. Interaction -> The user can click on each service category (e.g., Healthcare) to see a detailed, dynamic Chart.js doughnut chart and description. Justification -> Translates the abstract concept of data-driven expansion into a clear, explorable visual journey. This approach, instead of a static image, empowers the user to actively understand the brand's future. -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <style>
        body {
            font-family: 'Noto Sans KR', sans-serif;
            background-color: #FDFBF8;
            color: #4A4A4A;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 450px;
            margin-left: auto;
            margin-right: auto;
            height: 350px;
            max-height: 450px;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 400px;
            }
        }
        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.6s ease-out, transform 0.6s ease-out;
        }
        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
        .card-expandable-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.5s ease-out, padding 0.5s ease-out;
        }
        .card-expandable-content.visible {
            max-height: 200px;
            padding-top: 1rem;
        }
        .ring-interactive:focus {
            outline: none;
            ring-2 ring-offset-2 ring-[#FD7E53];
        }
    </style>
</head>
<body class="antialiased">

    <header class="bg-[#FDFBF8]/80 backdrop-blur-sm sticky top-0 z-50 shadow-sm">
        <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
            <h1 class="text-2xl font-bold text-[#FD7E53]">Furmunity</h1>
            <ul class="hidden md:flex space-x-8 text-gray-600">
                <li><a href="#intro" class="hover:text-[#FD7E53] transition-colors">브랜드 스토리</a></li>
                <li><a href="#why" class="hover:text-[#FD7E53] transition-colors">우리의 시작</a></li>
                <li><a href="#how" class="hover:text-[#FD7E53] transition-colors">PetBooth</a></li>
                <li><a href="#vision" class="hover:text-[#FD7E53] transition-colors">우리의 비전</a></li>
                <li><a href="#values" class="hover:text-[#FD7E53] transition-colors">핵심 가치</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="intro" class="h-[60vh] md:h-[80vh] flex items-center justify-center text-center bg-gradient-to-b from-[#FDFBF8] to-[#FFF5F1]">
            <div class="container mx-auto px-6">
                <h2 class="text-4xl md:text-6xl font-extrabold text-gray-800 leading-tight mb-4 fade-in">
                    모든 발걸음이<br>존중받는 세상
                </h2>
                <p class="text-lg md:text-xl text-gray-600 fade-in" style="transition-delay: 200ms;">Where Every Paw Belongs</p>
                <div class="mt-8 fade-in" style="transition-delay: 400ms;">
                    <a href="#why" class="bg-[#FD7E53] text-white py-3 px-8 rounded-full font-semibold hover:bg-[#F2643A] transition-colors inline-block">스토리 시작하기 👇</a>
                </div>
            </div>
        </section>

        <section id="why" class="py-20 md:py-32">
            <div class="container mx-auto px-6 text-center">
                <h3 class="text-3xl md:text-4xl font-bold text-gray-800 mb-6 fade-in">우리는 왜 이 일을 시작했을까요?</h3>
                <p class="max-w-3xl mx-auto text-lg text-gray-600 leading-relaxed fade-in" style="transition-delay: 200ms;">
                    Furmunity는 반려동물을 단순한 '애완동물'이 아닌, 삶을 함께하는 소중한 가족으로 바라보는 마음에서 출발합니다. 우리의 삶은 그들과 함께하는 수많은 순간들로 채워지지만, 그 소중한 기억을 간직하고 기록하는 방법은 여전히 부족했습니다.
                </p>
                <p class="max-w-3xl mx-auto mt-4 text-gray-600 leading-relaxed fade-in" style="transition-delay: 400ms;">
                    전문 스튜디오 촬영은 시간적, 금전적 부담이 컸고, 일상의 기록은 종종 흐릿한 스마트폰 사진 한 장으로 끝나는 경우가 많았습니다. 우리는 이 문제를 해결하고 싶었습니다. 누구나, 언제든, 부담 없이 가족의 가장 아름다운 순간을 고화질로 남길 수 있는 방법은 없을까? 이 고민이 Furmunity의 첫걸음이었습니다.
                </p>
            </div>
        </section>

        <section id="how" class="py-20 md:py-32 bg-[#FFF5F1]">
            <div class="container mx-auto px-6">
                <div class="text-center mb-16">
                    <h3 class="text-3xl md:text-4xl font-bold text-gray-800 mb-4 fade-in">솔루션: PetBooth의 탄생</h3>
                    <p class="max-w-3xl mx-auto text-lg text-gray-600 leading-relaxed fade-in" style="transition-delay: 200ms;">
                        우리는 이 문제를 해결하기 위해 'PetBooth'를 만들었습니다. PetBooth는 단순히 사진을 찍는 것을 넘어, 반려동물과의 관계를 강화하는 새로운 경험을 제공합니다. 아래 세 가지 핵심 가치를 클릭하여 자세히 알아보세요.
                    </p>
                </div>
                <div class="grid md:grid-cols-3 gap-10 text-center">
                    <div class="card p-8 rounded-xl shadow-lg bg-white transform hover:scale-105 transition-transform duration-300 cursor-pointer fade-in" data-section="capture" tabindex="0">
                        <div class="text-5xl mb-4 text-[#FD7E53]">📷</div>
                        <h4 class="text-xl font-bold mb-2">Capture</h4>
                        <p class="text-gray-600">소중한 순간을 손쉽게 촬영하고<br>기억으로 간직하는 경험</p>
                        <div class="card-expandable-content">
                            <p class="text-sm mt-2 text-gray-500">
                                특별한 장비나 기술 없이도 스튜디오급 고화질 사진을 얻을 수 있습니다. PetBooth는 반려동물의 시선과 감정까지 담아내는 최적의 환경을 제공합니다.
                            </p>
                        </div>
                    </div>
                    <div class="card p-8 rounded-xl shadow-lg bg-white transform hover:scale-105 transition-transform duration-300 cursor-pointer fade-in" style="transition-delay: 200ms;" data-section="connect" tabindex="0">
                        <div class="text-5xl mb-4 text-[#FD7E53]">🔗</div>
                        <h4 class="text-xl font-bold mb-2">Connect</h4>
                        <p class="text-gray-600">사진을 넘어, 추억을 연결하고<br>공유하는 경험</p>
                        <div class="card-expandable-content">
                            <p class="text-sm mt-2 text-gray-500">
                                촬영한 사진은 즉시 모바일과 연동됩니다. 굿즈로 제작하거나, 친구들과 공유하며 행복을 확장하는 새로운 방식의 소통을 가능하게 합니다.
                            </p>
                        </div>
                    </div>
                    <div class="card p-8 rounded-xl shadow-lg bg-white transform hover:scale-105 transition-transform duration-300 cursor-pointer fade-in" style="transition-delay: 400ms;" data-section="cherish" tabindex="0">
                        <div class="text-5xl mb-4 text-[#FD7E53]">💖</div>
                        <h4 class="text-xl font-bold mb-2">Cherish</h4>
                        <p class="text-gray-600">일상 속에서 행복을<br>오래도록 소장하는 경험</p>
                        <div class="card-expandable-content">
                            <p class="text-sm mt-2 text-gray-500">
                                단순한 파일이 아닌, 반려동물의 발자취를 추억으로 쌓아가는 여정입니다. PetBooth는 모든 순간이 의미 있는 가치가 되도록 돕습니다.
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <section id="vision" class="py-20 md:py-32">
            <div class="container mx-auto px-6">
                <div class="text-center mb-16">
                    <h3 class="text-3xl md:text-4xl font-bold text-gray-800 mb-4 fade-in">PetBooth, 그 이상의 가치</h3>
                    <p class="max-w-3xl mx-auto text-lg text-gray-600 leading-relaxed fade-in" style="transition-delay: 200ms;">
                        PetBooth는 단순한 하드웨어가 아닙니다. 그것은 데이터와 서비스가 연결되는 관문이며, Furmunity가 그리는 미래의 시작점입니다. 아래 다이어그램의 각 항목을 클릭하여 데이터가 어떻게 따뜻한 서비스로 확장되는지 확인해보세요.
                    </p>
                </div>

                <div class="flex flex-col lg:flex-row items-center justify-center gap-12 lg:gap-20">
                    <div class="w-full max-w-lg space-y-8 fade-in">
                        <div class="flex items-center space-x-4">
                            <div class="bg-[#FD7E53] text-white w-24 h-24 rounded-full flex items-center justify-center text-center p-2 font-bold shadow-md">PetBooth</div>
                            <div class="flex-grow h-1 bg-[#FFD1C1] rounded-full"></div>
                            <div class="bg-gray-700 text-white w-24 h-24 rounded-full flex items-center justify-center text-center p-2 font-bold shadow-md">데이터</div>
                        </div>
                        <div class="flex justify-end">
                            <div class="w-1 h-16 bg-[#FFD1C1]"></div>
                        </div>
                        <div class="grid grid-cols-2 gap-x-8 gap-y-6 relative">
                            <div class="service-item cursor-pointer p-4 bg-white rounded-lg shadow-md hover:shadow-xl hover:bg-orange-50 transition-all text-center ring-interactive" data-service="healthcare" tabindex="0">
                                <h5 class="font-bold">헬스케어</h5>
                                <p class="text-xs text-gray-500 mt-1">예방, 정기 검진, 영양</p>
                            </div>
                            <div class="service-item cursor-pointer p-4 bg-white rounded-lg shadow-md hover:shadow-xl hover:bg-orange-50 transition-all text-center ring-interactive" data-service="community" tabindex="0">
                                <h5 class="font-bold">커뮤니티</h5>
                                <p class="text-xs text-gray-500 mt-1">정보 공유, 교류, 전문가 상담</p>
                            </div>
                            <div class="service-item cursor-pointer p-4 bg-white rounded-lg shadow-md hover:shadow-xl hover:bg-orange-50 transition-all text-center ring-interactive" data-service="insurance" tabindex="0">
                                <h5 class="font-bold">보험</h5>
                                <p class="text-xs text-gray-500 mt-1">합리적 보험료, 간편 청구</p>
                            </div>
                            <div class="service-item cursor-pointer p-4 bg-white rounded-lg shadow-md hover:shadow-xl hover:bg-orange-50 transition-all text-center ring-interactive" data-service="lifestyle" tabindex="0">
                                <h5 class="font-bold">라이프스타일</h5>
                                <p class="text-xs text-gray-500 mt-1">맞춤 상품, 여행, 교육</p>
                            </div>
                        </div>
                    </div>
                    <div class="w-full lg:w-1/3 fade-in" style="transition-delay: 400ms;">
                        <div class="chart-container">
                            <canvas id="visionChart"></canvas>
                        </div>
                        <p id="chart-description" class="text-center mt-4 text-gray-600">위 서비스 항목을 클릭해 보세요.</p>
                    </div>
                </div>
            </div>
        </section>

        <section id="values" class="py-20 md:py-32 bg-[#FFF5F1]">
            <div class="container mx-auto px-6 text-center">
                <h3 class="text-3xl md:text-4xl font-bold text-gray-800 mb-12 fade-in">우리가 믿는 핵심 가치</h3>
                <div class="grid md:grid-cols-3 gap-10">
                    <div class="fade-in">
                        <div class="p-8 bg-white rounded-xl shadow-lg">
                            <h4 class="text-2xl font-bold mb-4 text-[#FD7E53]">반려동물은 가족이다</h4>
                            <p class="text-gray-600 leading-relaxed">
                                우리는 반려동물을 단순히 키우는 존재가 아니라, 삶의 기쁨과 슬픔을 함께 나누는 소중한 가족으로 존중합니다. 이 믿음이 Furmunity의 모든 활동의 기본이 됩니다.
                            </p>
                        </div>
                    </div>
                    <div class="fade-in" style="transition-delay: 200ms;">
                        <div class="p-8 bg-white rounded-xl shadow-lg">
                            <h4 class="text-2xl font-bold mb-4 text-[#FD7E53]">기술은 사람과 동물을 더 가깝게 만든다</h4>
                            <p class="text-gray-600 leading-relaxed">
                                혁신적인 기술은 관계를 멀어지게 하는 것이 아니라, 더욱 깊고 풍부하게 만들어야 합니다. 우리는 기술을 통해 반려동물과 보호자의 교감을 돕고, 더 나은 삶을 가능하게 합니다.
                            </p>
                        </div>
                    </div>
                    <div class="fade-in" style="transition-delay: 400ms;">
                        <div class="p-8 bg-white rounded-xl shadow-lg">
                            <h4 class="text-2xl font-bold mb-4 text-[#FD7E53]">우리의 혁신은 따뜻함으로 이어진다</h4>
                            <p class="text-600 leading-relaxed">
                                Furmunity의 모든 혁신과 성장은 결국 세상에 따뜻함을 전하는 방향으로 나아가야 합니다. 우리는 사랑과 배려가 담긴 기술을 통해 긍정적인 변화를 만들어 갑니다.
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </section>

    </main>

    <footer class="bg-gray-800 text-white py-12">
        <div class="container mx-auto px-6 text-center">
            <p class="text-2xl font-bold mb-4">Furmunity</p>
            <p class="mb-2">Capture, Connect, Cherish</p>
            <p class="text-gray-400">Where Every Paw Belongs</p>
            <p class="text-gray-400 mt-4">© 2025 Furmunity. All Rights Reserved.</p>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const faders = document.querySelectorAll('.fade-in');
            const observer = new IntersectionObserver(entries => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('visible');
                        observer.unobserve(entry.target);
                    }
                });
            }, { threshold: 0.1 });

            faders.forEach(fader => {
                observer.observe(fader);
            });

            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    document.querySelector(this.getAttribute('href')).scrollIntoView({
                        behavior: 'smooth'
                    });
                });
            });

            const expandableCards = document.querySelectorAll('.card');
            expandableCards.forEach(card => {
                card.addEventListener('click', () => {
                    const content = card.querySelector('.card-expandable-content');
                    content.classList.toggle('visible');
                });
            });

            const chartData = {
                healthcare: {
                    labels: ['정밀 건강 분석', 'AI 기반 질병 예측', '맞춤형 영양 솔루션'],
                    data: [50, 30, 20],
                    description: "사진 데이터와 행동 패턴 분석을 통해 반려동물의 미묘한 건강 변화를 감지하고, 데이터 기반 맞춤형 헬스케어 솔루션을 제공합니다."
                },
                community: {
                    labels: ['펫 정보 공유', '지역별 교류 모임', '전문가 Q&A'],
                    data: [45, 35, 20],
                    description: "보호자들이 소중한 추억과 유용한 정보를 나누고, 오프라인으로 만나 교류하며 강력한 펫 커뮤니티를 형성합니다."
                },
                insurance: {
                    labels: ['데이터 기반 보험료', '사진 청구 시스템', '맞춤 보장 상품'],
                    data: [60, 25, 15],
                    description: "촬영 데이터를 활용한 합리적인 보험료 산정, 간편한 청구 시스템으로 반려동물 보험의 접근성과 편의성을 혁신합니다."
                },
                lifestyle: {
                    labels: ['맞춤형 상품 추천', '펫 동반 여행/숙소 정보', '교육 및 훈련 콘텐츠'],
                    data: [40, 30, 30],
                    description: "반려동물의 특성과 취향을 분석하여 최적의 상품을 추천하고, 함께 즐길 수 있는 다양한 라이프스타일 경험을 제안합니다."
                }
            };

            const ctx = document.getElementById('visionChart').getContext('2d');
            let visionChart = new Chart(ctx, {
                // Change the chart type to a horizontal bar chart for better quantitative comparison
                type: 'bar',
                data: {
                    labels: ['서비스 영역', '세부 항목', '가치 제안'],
                    datasets: [{
                        label: '서비스 비중 (%)',
                        data: [40, 30, 30],
                        backgroundColor: [
                            '#FD7E53',
                            '#FFB49A',
                            '#FFD1C1',
                        ],
                        borderColor: '#FDFBF8',
                        borderWidth: 4
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    // Configure the chart to be a horizontal bar chart
                    indexAxis: 'y',
                    plugins: {
                        legend: {
                            position: 'bottom',
                            labels: {
                                color: '#4A4A4A'
                            }
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    let label = context.dataset.label || '';
                                    if (label) {
                                        label += ': ';
                                    }
                                    if (context.parsed.x !== null) {
                                        label += context.parsed.x + '%';
                                    }
                                    return label;
                                }
                            }
                        }
                    },
                    scales: {
                        x: {
                            beginAtZero: true,
                            max: 100,
                            ticks: {
                                callback: function(value) {
                                    return value + '%';
                                },
                                color: '#4A4A4A'
                            },
                            grid: {
                                color: '#E5E7EB'
                            }
                        },
                        y: {
                            ticks: {
                                color: '#4A4A4A'
                            },
                            grid: {
                                display: false
                            }
                        }
                    }
                }
            });

            const chartDescription = document.getElementById('chart-description');
            const serviceItems = document.querySelectorAll('.service-item');

            serviceItems.forEach(item => {
                item.addEventListener('click', () => {
                    const serviceKey = item.dataset.service;
                    const newData = chartData[serviceKey];
                    if (newData) {
                        visionChart.data.labels = newData.labels;
                        visionChart.data.datasets[0].data = newData.data;
                        visionChart.update();
                        chartDescription.textContent = newData.description;

                        serviceItems.forEach(el => el.classList.remove('ring-2', 'ring-offset-2', 'ring-[#FD7E53]'));
                        item.classList.add('ring-2', 'ring-offset-2', 'ring-[#FD7E53]');
                    }
                });
            });
        });
    </script>
</body>
</html>
