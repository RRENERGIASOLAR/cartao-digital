<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RR Energia Solar - Instalação, Limpeza e Manutenção</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            min-height: 100vh;
            background: linear-gradient(135deg, #001f3f 0%, #0074D9 50%, #39CCCC 100%);
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .business-card {
            width: 100%;
            max-width: 900px;
            height: auto;
            min-height: 600px;
            background-image: 
                linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.6)),
                url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 800"><defs><linearGradient id="sky" x1="0%" y1="0%" x2="0%" y2="100%"><stop offset="0%" style="stop-color:%2387ceeb"/><stop offset="100%" style="stop-color:%23ffffff"/></linearGradient></defs><rect width="1200" height="800" fill="url(%23sky)"/><rect x="0" y="600" width="1200" height="200" fill="%23333"/><rect x="100" y="400" width="200" height="200" fill="%23666"/><rect x="350" y="350" width="150" height="250" fill="%23555"/><rect x="550" y="300" width="180" height="300" fill="%23777"/><rect x="780" y="320" width="160" height="280" fill="%23666"/><rect x="980" y="380" width="140" height="220" fill="%23555"/><rect x="120" y="380" width="160" height="15" fill="%230061ff" opacity="0.8"/><rect x="125" y="385" width="150" height="10" fill="%230061ff" opacity="0.9"/><rect x="370" y="330" width="110" height="15" fill="%230061ff" opacity="0.8"/><rect x="375" y="335" width="100" height="10" fill="%230061ff" opacity="0.9"/><rect x="570" y="280" width="140" height="15" fill="%230061ff" opacity="0.8"/><rect x="575" y="285" width="130" height="10" fill="%230061ff" opacity="0.9"/><rect x="800" y="300" width="120" height="15" fill="%230061ff" opacity="0.8"/><rect x="805" y="305" width="110" height="10" fill="%230061ff" opacity="0.9"/><circle cx="200" cy="150" r="60" fill="%23ffcc00" opacity="0.9"/><path d="M170 150 L190 130 L190 140 L210 140 L210 160 L190 160 L190 170 Z" fill="%23ff6600"/></svg>');
            background-size: cover;
            background-position: center;
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
            position: relative;
            overflow: hidden;
            display: flex;
            flex-direction: column;
            animation: slideIn 1s ease-out;
        }

        @keyframes slideIn {
            from { 
                opacity: 0;
                transform: translateY(50px) scale(0.9);
            }
            to { 
                opacity: 1;
                transform: translateY(0) scale(1);
            }
        }

        .header-section {
            background: linear-gradient(135deg, rgba(0, 97, 255, 0.95), rgba(0, 59, 181, 0.95));
            padding: 30px;
            text-align: center;
            border-radius: 20px 20px 0 0;
            position: relative;
            overflow: hidden;
        }

        .header-section::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: conic-gradient(from 0deg, transparent, rgba(255, 204, 0, 0.1), transparent);
            animation: rotate 15s linear infinite;
        }

        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        .logo-section {
            position: relative;
            z-index: 2;
            margin-bottom: 20px;
        }

        .logo-container {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            background: linear-gradient(135deg, #ffcc00, #ff9900);
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0 auto 20px;
            box-shadow: 0 10px 20px rgba(255, 204, 0, 0.3);
            animation: pulse 3s ease-in-out infinite;
            border: 4px solid rgba(255, 255, 255, 0.3);
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        .logo-container::after {
            content: '☀️';
            font-size: 40px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }

        .company-name {
            font-size: 3.2em;
            font-weight: bold;
            color: white;
            margin-bottom: 10px;
            text-shadow: 3px 3px 6px rgba(0, 0, 0, 0.5);
            letter-spacing: 3px;
            position: relative;
            z-index: 2;
        }

        .company-service {
            font-size: 1.4em;
            color: rgba(255, 255, 255, 0.9);
            margin-bottom: 20px;
            font-weight: 600;
            position: relative;
            z-index: 2;
        }

        .main-content {
            background: rgba(255, 255, 255, 0.95);
            padding: 40px;
            flex-grow: 1;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            backdrop-filter: blur(10px);
        }

        .info-section {
            margin-bottom: 30px;
        }

        .impact-phrase {
            font-size: 1.3em;
            color: #0061ff;
            font-weight: bold;
            margin-bottom: 25px;
            padding: 20px;
            background: linear-gradient(135deg, rgba(0, 97, 255, 0.1), rgba(255, 204, 0, 0.1));
            border-radius: 15px;
            border-left: 5px solid #ffcc00;
            line-height: 1.5;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 30px;
        }

        .service-card {
            background: linear-gradient(135deg, #0061ff, #003bb5);
            color: white;
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 8px 16px rgba(0, 97, 255, 0.3);
            transition: transform 0.3s ease;
        }

        .service-card:hover {
            transform: translateY(-5px);
        }

        .service-icon {
            font-size: 2.5em;
            margin-bottom: 10px;
        }

        .service-title {
            font-size: 1.2em;
            font-weight: bold;
            margin-bottom: 8px;
        }

        .service-desc {
            font-size: 0.9em;
            opacity: 0.9;
        }

        .differentials {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }

        .differential-item {
            background: linear-gradient(135deg, #ffcc00, #ff9900);
            color: #333;
            padding: 12px 20px;
            border-radius: 25px;
            font-size: 1em;
            font-weight: bold;
            box-shadow: 0 5px 10px rgba(255, 204, 0, 0.3);
            transition: transform 0.3s ease;
        }

        .differential-item:hover {
            transform: translateY(-3px);
        }

        .contact-section {
            background: linear-gradient(135deg, #f8f9fa, #e9ecef);
            padding: 25px;
            border-radius: 15px;
            margin-bottom: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }

        .contact-title {
            font-size: 1.5em;
            color: #0061ff;
            font-weight: bold;
            margin-bottom: 15px;
            text-align: center;
        }

        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 15px;
            text-align: center;
        }

        .contact-item {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            font-size: 1.1em;
            color: #2c3e50;
        }

        .contact-icon {
            font-size: 1.5em;
        }

        .phone-number {
            color: #0061ff;
            font-weight: bold;
            font-size: 1.2em;
        }

        .location-text {
            color: #666;
            font-weight: 600;
        }

        .social-buttons {
            display: flex;
            gap: 25px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .social-btn {
            width: 70px;
            height: 70px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            text-decoration: none;
            color: white;
            font-size: 28px;
            transition: all 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
            position: relative;
            overflow: hidden;
        }

        .social-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            transition: left 0.6s;
        }

        .social-btn:hover::before {
            left: 100%;
        }

        .social-btn:hover {
            transform: translateY(-8px) scale(1.1);
            box-shadow: 0 20px 30px rgba(0, 0, 0, 0.3);
        }

        .whatsapp {
            background: linear-gradient(135deg, #25D366, #128C7E);
        }

        .instagram {
            background: linear-gradient(135deg, #E4405F, #C13584, #833AB4);
        }

        .facebook {
            background: linear-gradient(135deg, #1877F2, #42A5F5);
        }

        .email-btn {
            background: linear-gradient(135deg, #EA4335, #FBBC05);
        }

        @media (max-width: 768px) {
            .business-card {
                margin: 10px;
            }

            .header-section {
                padding: 25px 20px;
            }

            .company-name {
                font-size: 2.5em;
                letter-spacing: 2px;
            }

            .company-service {
                font-size: 1.2em;
            }

            .main-content {
                padding: 30px 20px;
            }

            .impact-phrase {
                font-size: 1.1em;
                padding: 15px;
            }

            .services-grid {
                grid-template-columns: 1fr;
                gap: 15px;
            }

            .contact-info {
                grid-template-columns: 1fr;
                gap: 10px;
            }

            .differentials {
                gap: 10px;
            }

            .differential-item {
                font-size: 0.9em;
                padding: 10px 15px;
            }

            .social-buttons {
                gap: 20px;
            }

            .social-btn {
                width: 60px;
                height: 60px;
                font-size: 24px;
            }
        }

        @media (max-width: 480px) {
            .company-name {
                font-size: 2em;
                letter-spacing: 1px;
            }

            .main-content {
                padding: 25px 15px;
            }

            .impact-phrase {
                font-size: 1em;
            }

            .differentials {
                flex-direction: column;
                align-items: center;
            }
        }
    </style>
</head>
<body>
    <div class="business-card">
        <div class="header-section">
            <div class="logo-section">
                <div class="logo-container"></div>
                <h1 class="company-name">RR ENERGIA SOLAR</h1>
                <p class="company-service">INSTALAÇÃO • LIMPEZA • MANUTENÇÃO</p>
            </div>
        </div>

        <div class="main-content">
            <div class="info-section">
                <div class="impact-phrase">
                    💡 "Limpeza técnica especializada que recupera até +25% da eficiência do seu sistema solar"
                </div>

                <div class="services-grid">
                    <div class="service-card">
                        <div class="service-icon">🔧</div>
                        <div class="service-title">INSTALAÇÃO</div>
                        <div class="service-desc">Sistemas completos com garantia</div>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">✨</div>
                        <div class="service-title">LIMPEZA TÉCNICA</div>
                        <div class="service-desc">Sem produtos abrasivos</div>
                    </div>
                    <div class="service-card">
                        <div class="service-icon">⚙️</div>
                        <div class="service-title">MANUTENÇÃO</div>
                        <div class="service-desc">Preventiva e corretiva</div>
                    </div>
                </div>

                <div class="differentials">
                    <span class="differential-item">✅ Equipe Certificada</span>
                    <span class="differential-item">⚡ Atendimento Rápido</span>
                    <span class="differential-item">🛡️ Produtos Seguros</span>
                </div>
            </div>

            <div class="contact-section">
                <h3 class="contact-title">📞 ENTRE EM CONTATO</h3>
                <div class="contact-info">
                    <div class="contact-item">
                        <span class="contact-icon">📱</span>
                        <span class="phone-number">(21) 99280-6330</span>
                    </div>
                    <div class="contact-item">
                        <span class="contact-icon">✉️</span>
                        <span>comercialrrsolar@gmail.com</span>
                    </div>
                    <div class="contact-item">
                        <span class="contact-icon">📍</span>
                        <span class="location-text">Itaipuaçu • Maricá • Niterói</span>
                    </div>
                </div>
            </div>

            <div class="social-buttons">
                <a href="https://wa.me/5521992806330?text=Olá! Vi seu cartão digital e gostaria de um orçamento para energia solar. Tenho interesse em:" class="social-btn whatsapp" title="WhatsApp - Orçamento Grátis">
                    <svg fill="currentColor" viewBox="0 0 24 24" width="32" height="32">
                        <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893A11.821 11.821 0 0020.525 3.685"/>
                    </svg>
                </a>

                <a href="https://www.instagram.com/rrsolar.energy/" class="social-btn instagram" title="Instagram @rrsolar.energy" target="_blank">
                    <svg fill="currentColor" viewBox="0 0 24 24" width="30" height="30">
                        <path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/>
                    </svg>
                </a>

                <a href="https://www.facebook.com/profile.php?id=61576155369309" class="social-btn facebook" title="Facebook RR Solar Energy" target="_blank">
                    <svg fill="currentColor" viewBox="0 0 24 24" width="30" height="30">
                        <path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/>
                    </svg>
                </a>

                <a href="mailto:comercialrrsolar@gmail.com?subject=Orçamento Energia Solar&body=Olá! Gostaria de receber um orçamento para:" class="social-btn email-btn" title="Email Comercial">
                    <svg fill="currentColor" viewBox="0 0 24 24" width="30" height="30">
                        <path d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/>
                    </svg>
                </a>
            </div>
        </div>
    </div>

    <script>
        // Efeitos interativos aprimorados
        document.querySelectorAll('.social-btn').forEach(btn => {
            btn.addEventListener('mouseenter', () => {
                btn.style.transform = 'translateY(-8px) scale(1.1)';
            });
            
            btn.addEventListener('mouseleave', () => {
                btn.style.transform = 'translateY(0) scale(1)';
            });
        });

        // Animação de entrada suave
        window.addEventListener('load', () => {
            const elements = document.querySelectorAll('.service-card, .differential-item');
            elements.forEach((el, index) => {
                el.style.opacity = '0';
                el.style.transform = 'translateY(30px)';
                
                setTimeout(() => {
                    el.style.transition = 'all 0.6s ease';
                    el.style.opacity = '1';
                    el.style.transform = 'translateY(0)';
                }, index * 100);
            });
        });

        // Efeito de clique com feedback visual aprimorado
        document.querySelectorAll('.social-btn').forEach(btn => {
            btn.addEventListener('click', function(e) {
                const ripple = document.createElement('div');
                ripple.style.position = 'absolute';
                ripple.style.borderRadius = '50%';
                ripple.style.background = 'rgba(255, 255, 255, 0.7)';
                ripple.style.transform = 'scale(0)';
                ripple.style.animation = 'ripple 0.8s linear';
                ripple.style.left = '50%';
                ripple.style.top = '50%';
                ripple.style.width = '30px';
                ripple.style.height = '30px';
                ripple.style.marginLeft = '-15px';
                ripple.style.marginTop = '-15px';
                
                this.appendChild(ripple);
                
                setTimeout(() => {
                    ripple.remove();
                }, 800);
            });
        });

        // CSS para animação de ripple
        const style = document.createElement('style');
        style.textContent = `
            @keyframes ripple {
                to {
                    transform: scale(4);
                    opacity: 0;
                }
            }      
        `;
        document.head.appendChild(style);
    </script>
</body>
</html>
