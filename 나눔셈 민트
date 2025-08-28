<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>나눔셈 - 비영리단체 맞춤 종합관리 솔루션</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }

        :root {
            /* New Palette */
            --primary-color: #1DD1A1;         /* 메인 민트(터콰이즈) */
            --accent-color: #55efc4;          /* 포인트 민트 */
            --light-mint: #a7f3d0;            /* 라이트 민트 */
            --bg-mint: #ecfdf5;               /* 배경 민트 */
            --lime-accent: #84cc16;           /* 라임 포인트 */

            --text-dark: #1f2937;             /* 가독성 개선 다크 텍스트 */
            --text-gray: #64748b;             /* 중간 톤 회색 */
            --white: #ffffff;

            /* Gradients (민트 계열) */
            --primary-gradient: linear-gradient(135deg, #1DD1A1, #55efc4);
            --accent-gradient: linear-gradient(135deg, #55efc4, #a7f3d0);
        }

        body { font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; line-height: 1.6; color: var(--text-dark); background: var(--white); }
        .container { max-width: 1200px; margin: 0 auto; padding: 0 20px; }

        /* 프로모션 배너 */
        .promo-banner {
            background: var(--accent-gradient);
            color: var(--white);
            text-align: center;
            padding: 15px 0;
            font-weight: 700;
            font-size: 1.1rem;
            animation: slideDown 0.5s ease-out;
            box-shadow: 0 4px 20px rgba(85, 239, 196, 0.35);
        }
        .promo-banner .btn-promo {
            background: var(--white);
            color: var(--primary-color);
            padding: 8px 20px;
            border-radius: 25px;
            text-decoration: none;
            font-weight: bold;
            margin-left: 15px;
            display: inline-block;
            transition: all 0.3s;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
            border: 2px solid transparent;
        }
        .promo-banner .btn-promo:hover {
            transform: scale(1.05);
            box-shadow: 0 6px 20px rgba(0,0,0,0.16);
            border: 2px solid var(--white);
            background: transparent;
            color: var(--white);
        }

        /* 헤더 */
        .header {
            background: var(--white);
            box-shadow: 0 4px 30px rgba(85, 239, 196, 0.12);
            position: sticky; top: 0; z-index: 100;
            border-bottom: 3px solid var(--accent-color);
            transition: transform .25s ease;
        }
        .navbar { display: flex; justify-content: space-between; align-items: center; padding: 15px 0; }

        .logo {
            display: flex; align-items: center;
            font-size: 24px; font-weight: bold; color: var(--primary-color);
        }
        .logo-icon {
            width: 45px; height: 45px; margin-right: 12px;
            background: var(--primary-gradient);  /* 민트/터콰이즈 */
            border-radius: 50%;
            display: flex; align-items: center; justify-content: center;
            position: relative; overflow: hidden;
            box-shadow: 0 4px 15px rgba(29, 209, 161, 0.35);
        }
        .logo-dots { position: absolute; width: 100%; height: 100%; }
        .dot { position: absolute; background: rgba(255,255,255,0.85); border-radius: 50%; }
        .dot:nth-child(1) { width: 8px; height: 8px; top: 8px; left: 16px; }
        .dot:nth-child(2) { width: 12px; height: 12px; top: 18px; left: 8px; }
        .dot:nth-child(3) { width: 6px; height: 6px; top: 20px; right: 8px; }
        .dot:nth-child(4) { width: 10px; height: 10px; bottom: 8px; left: 12px; }

        .nav-menu { display: flex; list-style: none; align-items: center; gap: 30px; }
        .nav-menu a {
            text-decoration: none; color: var(--text-dark); font-weight: 500; transition: color 0.25s, transform 0.25s;
        }
        .nav-menu a:hover { color: var(--primary-color); transform: translateY(-2px); }

        .nav-buttons { display: flex; gap: 10px; }
        .btn {
            padding: 10px 20px; border-radius: 25px; text-decoration: none; font-weight: 600;
            transition: all 0.25s; border: none; cursor: pointer; display: inline-block;
        }
        .btn-primary {
            background: var(--primary-gradient); color: var(--white);
            box-shadow: 0 8px 25px rgba(29, 209, 161, 0.28);
        }
        .btn-primary:hover {
            background: linear-gradient(135deg, #1DD1A1, #a7f3d0);
            transform: translateY(-3px);
            box-shadow: 0 12px 35px rgba(29, 209, 161, 0.38);
        }
        .btn-outline {
            background: transparent; color: var(--primary-color);
            border: 2px solid var(--primary-color);
            box-shadow: 0 4px 15px rgba(29, 209, 161, 0.18);
        }
        .btn-outline:hover {
            background: var(--primary-color); color: var(--white);
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(29, 209, 161, 0.32);
        }

        /* 메인 섹션 */
        .hero {
            background:
                linear-gradient(135deg, rgba(29, 209, 161, 0.10), rgba(236, 253, 245, 0.85)),
                /* 내장 SVG 색상도 민트/터콰이즈로 교체 (%23 = #) */
                url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="grain" width="100" height="100" patternUnits="userSpaceOnUse"><circle cx="20" cy="20" r="1" fill="%2355efc4" opacity="0.12"/><circle cx="80" cy="40" r="1.5" fill="%231DD1A1" opacity="0.12"/><circle cx="40" cy="70" r="1" fill="%2355efc4" opacity="0.12"/><circle cx="90" cy="90" r="1" fill="%231DD1A1" opacity="0.12"/></pattern></defs><rect width="100" height="100" fill="url(%23grain)"/></svg>');
            padding: 100px 0; text-align: center; position: relative; overflow: hidden;
        }
        .hero::before {
            content: ''; position: absolute; top: -50%; left: -50%; width: 200%; height: 200%;
            background: radial-gradient(circle, rgba(29, 209, 161, 0.12) 0%, transparent 70%);
            animation: float 6s ease-in-out infinite;
        }
        .hero h1 { font-size: 3.5rem; margin-bottom: 20px; color: var(--text-dark); animation: fadeInUp 1s ease-out; position: relative; z-index: 2; text-shadow: 0 2px 10px rgba(0,0,0,0.06); }
        .hero .subtitle { font-size: 1.4rem; color: var(--text-gray); margin-bottom: 50px; animation: fadeInUp 1s ease-out 0.2s both; position: relative; z-index: 2; }

        .core-features { display: flex; justify-content: center; gap: 40px; margin: 40px 0; animation: fadeInUp 1s ease-out 0.4s both; }
        .feature-item {
            background: var(--white); padding: 40px; border-radius: 20px;
            box-shadow: 0 15px 40px rgba(29, 209, 161, 0.12);
            transition: all 0.3s ease; border: 2px solid rgba(29, 209, 161, 0.18);
            position: relative; overflow: hidden;
        }
        .feature-item::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 4px; background: var(--accent-gradient); }
        .feature-item:hover {
            transform: translateY(-15px) scale(1.02);
            border: 2px solid var(--accent-color);
            box-shadow: 0 25px 50px rgba(29, 209, 161, 0.22);
        }
        .feature-icon { font-size: 3rem; margin-bottom: 20px; filter: drop-shadow(0 4px 8px rgba(29, 209, 161, 0.25)); color: var(--lime-accent); }

        .hero-buttons { margin-top: 40px; animation: fadeInUp 1s ease-out 0.6s both; }
        .hero-buttons .btn { margin: 0 10px; padding: 15px 30px; font-size: 1.1rem; }

        /* 이벤트 섹션 */
        .events { padding: 100px 0; background: var(--primary-color); position: relative; }
        .events::before {
            content: ''; position: absolute; inset: 0;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100"><defs><pattern id="dots" width="20" height="20" patternUnits="userSpaceOnUse"><circle cx="10" cy="10" r="1" fill="white" opacity="0.12"/></pattern></defs><rect width="100" height="100" fill="url(%23dots)"/></svg>');
        }
        .events h2 { text-align: center; font-size: 3rem; margin-bottom: 60px; color: var(--white); position: relative; z-index: 2; text-shadow: 0 2px 10px rgba(0,0,0,0.2); }
        .events-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 30px; }
        .event-card {
            background: var(--white); padding: 50px; border-radius: 25px; text-align: center;
            box-shadow: 0 20px 50px rgba(0,0,0,0.15);
            transition: all 0.4s ease; position: relative; z-index: 2;
            border: 3px solid rgba(255,255,255,0.0);
        }
        .event-card:hover {
            transform: translateY(-15px) scale(1.03);
            border: 3px solid rgba(255,255,255,0.85);
            box-shadow: 0 30px 60px rgba(0,0,0,0.2);
        }
        .event-icon {
            font-size: 4rem; margin-bottom: 25px;
            color: var(--lime-accent);  /* 라임 포인트 */
            filter: drop-shadow(0 4px 15px rgba(132, 204, 22, 0.35));
        }

        /* 선택 이유 섹션 */
        .reasons { padding: 80px 0; background: var(--white); }
        .reasons h2 { text-align: center; font-size: 2.5rem; margin-bottom: 50px; color: var(--text-dark); }
        .reasons-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 30px; }
        .reason-card {
            padding: 40px; border-radius: 20px;
            background: linear-gradient(135deg, rgba(85, 239, 196, 0.12), rgba(255,255,255,0.95));
            transition: all 0.4s ease; border: 2px solid rgba(85, 239, 196, 0.25);
            position: relative; overflow: hidden;
        }
        .reason-card::before {
            content: ''; position: absolute; top: -50%; left: -50%; width: 200%; height: 200%;
            background: radial-gradient(circle, rgba(29, 209, 161, 0.12) 0%, transparent 70%);
            transition: all 0.4s ease; opacity: 0;
        }
        .reason-card:hover { transform: translateY(-10px) scale(1.02); border: 2px solid var(--accent-color); box-shadow: 0 20px 40px rgba(29, 209, 161, 0.2); }
        .reason-card:hover::before { opacity: 1; }
        .reason-card h3 { color: var(--primary-color); margin-bottom: 20px; font-size: 1.4rem; font-weight: 700; position: relative; z-index: 2; }

        /* 기능 소개 섹션 */
        .features { padding: 80px 0; background: var(--bg-mint); } /* 부드러운 민트 배경 */
        .features h2 { text-align: center; font-size: 2.5rem; margin-bottom: 50px; color: var(--text-dark); }
        .features-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(350px, 1fr)); gap: 30px; }
        .feature-card {
            background: var(--white); padding: 40px; border-radius: 20px;
            box-shadow: 0 15px 40px rgba(29, 209, 161, 0.10);
            border: 2px solid rgba(85, 239, 196, 0.20);
            transition: all 0.4s ease; position: relative; overflow: hidden;
        }
        .feature-card::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 5px; background: var(--primary-gradient); }
        .feature-card:hover { transform: translateY(-10px); border: 2px solid var(--accent-color); box-shadow: 0 25px 50px rgba(29, 209, 161, 0.20); }
        .feature-card h3 { color: var(--primary-color); margin-bottom: 20px; font-size: 1.4rem; font-weight: 700; }
        .feature-list { list-style: none; padding: 0; }
        .feature-list li { padding: 5px 0; padding-left: 22px; position: relative; }
        .feature-list li:before { content: "✓"; color: var(--lime-accent); font-weight: 900; position: absolute; left: 0; }

        /* 고정 버튼 */
        .fixed-buttons {
            position: fixed; right: 20px; top: 50%; transform: translateY(-50%);
            display: flex; flex-direction: column; gap: 10px; z-index: 50;
        }
        .fixed-btn {
            background: var(--primary-gradient); color: var(--white);
            padding: 18px 25px; border-radius: 30px; text-decoration: none; font-weight: 700;
            box-shadow: 0 8px 25px rgba(29, 209, 161, 0.35);
            transition: all 0.3s; text-align: center; border: 2px solid transparent;
        }
        .fixed-btn:hover {
            background: linear-gradient(135deg, #55efc4, #a7f3d0);
            transform: scale(1.08);
            box-shadow: 0 12px 35px rgba(29, 209, 161, 0.45);
            border: 2px solid rgba(255,255,255,0.35);
        }

        /* 푸터 */
        .footer { background: #0f172a; color: var(--white); padding: 50px 0; text-align: center; }
        .footer-content { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 30px; margin-bottom: 30px; }
        .footer-section h3 { color: var(--light-mint); margin-bottom: 15px; font-size: 1.2rem; font-weight: 700; }
        .footer-section a { color: #cbd5e1; text-decoration: none; display: block; margin: 5px 0; transition: color 0.25s, transform 0.25s; }
        .footer-section a:hover { color: var(--accent-color); transform: translateX(5px); }

        /* 애니메이션 */
        @keyframes fadeInUp { from { opacity: 0; transform: translateY(30px);} to { opacity: 1; transform: translateY(0);} }
        @keyframes slideDown { from { transform: translateY(-100%);} to { transform: translateY(0);} }
        @keyframes float { 0%,100% { transform: translateY(0) rotate(0deg);} 50% { transform: translateY(-20px) rotate(180deg);} }
        @keyframes pulse { 0%,100% { transform: scale(1);} 50% { transform: scale(1.05);} }

        .fade-in { opacity: 0; transform: translateY(30px); transition: all 0.6s ease-out; }
        .fade-in.visible { opacity: 1; transform: translateY(0); }

        /* 반응형 */
        @media (max-width: 768px) {
            .nav-menu { display: none; }
            .hero h1 { font-size: 2rem; }
            .core-features { flex-direction: column; align-items: center; }
            .fixed-buttons { position: static; transform: none; flex-direction: row; justify-content: center; margin: 20px 0; }
        }
    </style>
</head>
<body>
    <!-- 프로모션 배너 -->
    <div class="promo-banner">
        신규 가입 단체 첫 3개월 30% 할인! 지금 바로 시작하세요!
        <a href="#contact" class="btn-promo">할인 혜택 받기</a>
    </div>

    <!-- 헤더 -->
    <header class="header">
        <div class="container">
            <nav class="navbar">
                <div class="logo">
                    <div class="logo-icon">
                        <div class="logo-dots">
                            <div class="dot"></div>
                            <div class="dot"></div>
                            <div class="dot"></div>
                            <div class="dot"></div>
                        </div>
                    </div>
                    나눔셈
                </div>
                <ul class="nav-menu">
                    <li><a href="#about">나눔셈소개</a></li>
                    <li><a href="#features">기능소개</a></li>
                    <li><a href="#guide">이용안내</a></li>
                    <li><a href="#support">교육·지원</a></li>
                    <li><a href="#mypage">마이페이지</a></li>
                </ul>
                <div class="nav-buttons">
                    <a href="#login" class="btn btn-outline">로그인</a>
                    <a href="#apply" class="btn btn-primary">이용신청</a>
                </div>
            </nav>
        </div>
    </header>

    <!-- 메인 섹션 -->
    <section class="hero">
        <div class="container">
            <h1>비영리단체 맞춤 종합관리 솔루션, 나눔셈</h1>
            <p class="subtitle">투명한 회계, 통합관리, 합리적 비용으로 단체 운영을 더욱 체계적이고 효율적으로</p>

            <div class="core-features">
                <div class="feature-item">
                    <div class="feature-icon">💰</div>
                    <h3>투명한 회계</h3>
                    <p>공익법인회계기준 준수</p>
                </div>
                <div class="feature-item">
                    <div class="feature-icon">⚙️</div>
                    <h3>통합관리</h3>
                    <p>모든 업무를 한 곳에서</p>
                </div>
                <div class="feature-item">
                    <div class="feature-icon">💡</div>
                    <h3>합리적 비용</h3>
                    <p>착한 가격의 전문 솔루션</p>
                </div>
            </div>

            <div class="hero-buttons">
                <a href="#start" class="btn btn-primary">나눔셈 이용하기</a>
                <a href="#guide" class="btn btn-outline">신규 단체 도입안내</a>
                <a href="#support" class="btn btn-outline">고객지원</a>
            </div>
        </div>
    </section>

    <!-- 이벤트 & 프로모션 -->
    <section class="events">
        <div class="container">
            <h2>특별 이벤트 & 프로모션</h2>
            <div class="events-grid">
                <div class="event-card fade-in">
                    <div class="event-icon">🎯</div>
                    <h3>신규 고객 30% 할인</h3>
                    <p>처음 이용하는 단체를 위한 특별 혜택! 첫 3개월 동안 30% 할인된 가격으로 모든 기능을 이용하실 수 있습니다.</p>
                </div>
                <div class="event-card fade-in">
                    <div class="event-icon">📚</div>
                    <h3>무료 활용 교육 프로그램</h3>
                    <p>나눔셈UP-DAY: 매월 진행되는 무료 교육으로 시스템 활용도를 높이고 업무 효율성을 극대화하세요.</p>
                </div>
                <div class="event-card fade-in">
                    <div class="event-icon">🔄</div>
                    <h3>기존 시스템 데이터 무료 이전</h3>
                    <p>기존에 사용하던 시스템의 데이터를 나눔셈으로 무료로 이전해드립니다. 걱정 없이 시작하세요.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 선택 이유 -->
    <section class="reasons" id="about">
        <div class="container">
            <h2>나눔셈을 선택해야 하는 이유</h2>
            <div class="reasons-grid">
                <div class="reason-card fade-in">
                    <h3>비영리 회계 특화 프로그램</h3>
                    <p>결산공시, 후원금 관리, 기부금영수증, 출연재산보고 등 비영리단체에 필요한 기능을 한 곳에서 관리할 수 있습니다.</p>
                </div>
                <div class="reason-card fade-in">
                    <h3>철저한 보안체계</h3>
                    <p>금융권 수준의 보안 체계와 전문가 검토를 바탕으로 투명하고 안전한 회계관리를 지원합니다.</p>
                </div>
                <div class="reason-card fade-in">
                    <h3>전문기관 제휴</h3>
                    <p>전문기관과의 제휴를 통해 신뢰할 수 있는 서비스를 제공합니다.</p>
                </div>
                <div class="reason-card fade-in">
                    <h3>검증된 성장 지원</h3>
                    <p>여러 단체가 선택한 솔루션으로 체계적이고 지속가능한 성장을 돕습니다.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- 기능 소개 -->
    <section class="features" id="features">
        <div class="container">
            <h2>핵심 기능 소개</h2>
            <div class="features-grid">
                <div class="feature-card fade-in">
                    <h3>💰 회계 관리</h3>
                    <ul class="feature-list">
                        <li>공익법인회계기준에 따른 결산서양식</li>
                        <li>수입·지출전표로 자산부채관리(복식부기 결산)</li>
                        <li>회계단위별 구분회계(기금회계)</li>
                        <li>구분결산서, 기능별 배분전표</li>
                    </ul>
                </div>
                <div class="feature-card fade-in">
                    <h3>📋 세무 관리</h3>
                    <ul class="feature-list">
                        <li>소득 지급 관리</li>
                        <li>원천세 계산 및 신고</li>
                        <li>법인세 관리</li>
                    </ul>
                </div>
                <div class="feature-card fade-in">
                    <h3>💳 수납 관리</h3>
                    <ul class="feature-list">
                        <li>CMS 회원 관리</li>
                        <li>자동 출금 시스템</li>
                        <li>수납 현황 집계</li>
                    </ul>
                </div>
                <div class="feature-card fade-in">
                    <h3>📞 주소록 관리</h3>
                    <ul class="feature-list">
                        <li>후원자 정보 관리</li>
                        <li>자원봉사자 데이터베이스</li>
                        <li>수혜자 관리</li>
                        <li>거래처 정보</li>
                    </ul>
                </div>
                <div class="feature-card fade-in">
                    <h3>🤝 활동 관리</h3>
                    <ul class="feature-list">
                        <li>후원약정 관리</li>
                        <li>후원금 관리</li>
                        <li>기부금영수증 발급</li>
                        <li>출연재산보고</li>
                    </ul>
                </div>
                <div class="feature-card fade-in">
                    <h3>🎉 행사 관리</h3>
                    <ul class="feature-list">
                        <li>행사 등록 시스템</li>
                        <li>진행 상황 관리</li>
                        <li>참가자 관리</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- 고정 버튼 -->
    <div class="fixed-buttons">
        <a href="#login" class="fixed-btn">로그인</a>
        <a href="tel:02-565-5886" class="fixed-btn">상담하기<br>02-565-5886</a>
    </div>

    <!-- 푸터 -->
    <footer class="footer">
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>나눔셈 채널</h3>
                    <a href="#">나눔셈 블로그</a>
                    <a href="#">YouTube 채널</a>
                    <a href="#">네이버 카페</a>
                    <a href="#">인스타그램</a>
                </div>
                <div class="footer-section">
                    <h3>교육·지원</h3>
                    <a href="#">나눔셈UP-DAY</a>
                    <a href="#">온라인 매뉴얼</a>
                    <a href="#">영상 강의</a>
                    <a href="#">1:1 원격지원</a>
                </div>
                <div class="footer-section">
                    <h3>이용안내</h3>
                    <a href="#">이용 신청 절차</a>
                    <a href="#">요금 안내</a>
                    <a href="#">FAQ</a>
                    <a href="#">자료실</a>
                </div>
                <div class="footer-section">
                    <h3>고객지원</h3>
                    <a href="tel:02-565-5886">전화: 02-565-5886</a>
                    <a href="#">이메일 문의</a>
                    <a href="#">채팅 상담</a>
                </div>
            </div>
            <p>&copy; 2025 나눔셈. All rights reserved. 비영리단체를 위한 전문 솔루션</p>
        </div>
    </footer>

    <script>
        // 스크롤 애니메이션
        const observerOptions = { threshold: 0.1, rootMargin: '0px 0px -50px 0px' };
        const observer = new IntersectionObserver(function(entries) {
            entries.forEach(entry => { if (entry.isIntersecting) { entry.target.classList.add('visible'); }});
        }, observerOptions);
        document.querySelectorAll('.fade-in').forEach(el => observer.observe(el));

        // 부드러운 스크롤
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) target.scrollIntoView({ behavior: 'smooth', block: 'start' });
            });
        });

        // 헤더 스크롤 효과
        let lastScrollY = window.scrollY;
        window.addEventListener('scroll', () => {
            const header = document.querySelector('.header');
            if (window.scrollY > lastScrollY && window.scrollY > 100) header.style.transform = 'translateY(-100%)';
            else header.style.transform = 'translateY(0)';
            lastScrollY = window.scrollY;
        });

        // 로고 점 애니메이션
        const logoDots = document.querySelectorAll('.dot');
        function animateDots() {
            logoDots.forEach((dot, idx) => {
                setTimeout(() => {
                    dot.style.transform = 'scale(1.5)';
                    dot.style.boxShadow = '0 0 15px rgba(255,255,255,0.85)';
                    setTimeout(() => { dot.style.transform = 'scale(1)'; dot.style.boxShadow = 'none'; }, 300);
                }, idx * 150);
            });
        }
        setInterval(animateDots, 4000);

        // 프로모션 배너 펄스 효과
        const promoBanner = document.querySelector('.promo-banner');
        setInterval(() => {
            promoBanner.style.animation = 'none';
            setTimeout(() => { promoBanner.style.animation = 'pulse 0.6s ease-in-out'; }, 10);
        }, 8000);

        // 버튼 클릭 리플
        document.querySelectorAll('.btn').forEach(btn => {
            btn.addEventListener('click', function(e) {
                const ripple = document.createElement('span');
                ripple.style.cssText = `
                    position: absolute; border-radius: 50%;
                    background: rgba(255,255,255,0.6);
                    transform: scale(0); animation: ripple 0.6s linear; pointer-events: none;
                `;
                const rect = this.getBoundingClientRect();
                const size = Math.max(rect.width, rect.height);
                ripple.style.width = ripple.style.height = size + 'px';
                ripple.style.left = (e.clientX - rect.left - size / 2) + 'px';
                ripple.style.top = (e.clientY - rect.top - size / 2) + 'px';
                this.style.position = 'relative'; this.style.overflow = 'hidden';
                this.appendChild(ripple);
                setTimeout(() => ripple.remove(), 600);
            });
        });

        // CSS 애니메이션 추가
        const style = document.createElement('style');
        style.textContent = `
            @keyframes ripple { to { transform: scale(4); opacity: 0; } }
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>
