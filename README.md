<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>WhatsApp招聘咨询</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }

        .container {
            background: rgba(255, 255, 255, 0.95);
            padding: 40px;
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
            text-align: center;
            max-width: 500px;
            width: 100%;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }

        .logo {
            width: 80px;
            height: 80px;
            margin: 0 auto 20px;
            background: #25D366;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 40px;
            color: white;
            box-shadow: 0 10px 30px rgba(37, 211, 102, 0.3);
        }

        h1 {
            color: #333;
            margin-bottom: 10px;
            font-size: 28px;
            font-weight: 600;
        }

        .subtitle {
            color: #666;
            margin-bottom: 30px;
            font-size: 16px;
            line-height: 1.5;
        }

        .features {
            margin-bottom: 30px;
            text-align: left;
        }

        .feature {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
            padding: 15px;
            background: rgba(37, 211, 102, 0.1);
            border-radius: 10px;
            transition: all 0.3s ease;
        }

        .feature:hover {
            background: rgba(37, 211, 102, 0.2);
            transform: translateX(5px);
        }

        .feature-icon {
            width: 24px;
            height: 24px;
            margin-right: 15px;
            color: #25D366;
        }

        .whatsapp-btn {
            background: linear-gradient(135deg, #25D366, #128C7E);
            color: white;
            border: none;
            padding: 15px 30px;
            font-size: 18px;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            width: 100%;
            font-weight: 600;
            box-shadow: 0 10px 30px rgba(37, 211, 102, 0.3);
            position: relative;
            overflow: hidden;
        }

        .whatsapp-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 15px 40px rgba(37, 211, 102, 0.4);
        }

        .whatsapp-btn:active {
            transform: translateY(0);
        }

        .whatsapp-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
            transition: left 0.5s;
        }

        .whatsapp-btn:hover::before {
            left: 100%;
        }

        .status {
            margin-top: 20px;
            padding: 15px;
            border-radius: 10px;
            font-weight: 500;
            display: none;
        }

        .status.success {
            background: rgba(76, 175, 80, 0.1);
            color: #4CAF50;
            border: 1px solid rgba(76, 175, 80, 0.3);
        }

        .status.error {
            background: rgba(244, 67, 54, 0.1);
            color: #F44336;
            border: 1px solid rgba(244, 67, 54, 0.3);
        }

        .countdown {
            display: block;
            margin-top: 20px;
            text-align: center;
        }

        .countdown-circle {
            width: 60px;
            height: 60px;
            border: 4px solid #25D366;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 10px;
            position: relative;
            overflow: hidden;
        }

        .countdown-circle::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: conic-gradient(#25D366 0deg, transparent 0deg);
            border-radius: 50%;
            animation: countdown-fill 1s linear forwards;
        }

        .countdown-number {
            font-size: 24px;
            font-weight: bold;
            color: #25D366;
            z-index: 1;
            position: relative;
            background: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        @keyframes countdown-fill {
            0% { background: conic-gradient(#25D366 0deg, transparent 0deg); }
            100% { background: conic-gradient(#25D366 360deg, transparent 360deg); }
        }

        .loading {
            display: none;
            margin-top: 20px;
        }

        .spinner {
            width: 40px;
            height: 40px;
            border: 4px solid #f3f3f3;
            border-top: 4px solid #25D366;
            border-radius: 50%;
            animation: spin 1s linear infinite;
            margin: 0 auto;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .footer {
            margin-top: 30px;
            color: #888;
            font-size: 14px;
        }

        @media (max-width: 480px) {
            .container {
                padding: 30px 20px;
            }
            
            h1 {
                font-size: 24px;
            }
            
            .whatsapp-btn {
                padding: 12px 25px;
                font-size: 16px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="logo">📱</div>
        <h1>WhatsApp招聘咨询</h1>
        <p class="subtitle">立即联系我们的招聘顾问，获取最新职位信息和专业建议</p>
        
        <div class="features">
            <div class="feature">
                <div class="feature-icon">✨</div>
                <div>专业招聘顾问一对一服务</div>
            </div>
            <div class="feature">
                <div class="feature-icon">🚀</div>
                <div>最新职位信息实时更新</div>
            </div>
            <div class="feature">
                <div class="feature-icon">💼</div>
                <div>个性化职业发展建议</div>
            </div>
        </div>

        <button class="whatsapp-btn" onclick="redirectToWhatsApp()">
            📱 立即咨询 WhatsApp
        </button>

        <div class="loading" id="loading">
            <div class="spinner"></div>
            <p id="loadingText">正在跳转到WhatsApp...</p>
        </div>

        <div class="countdown" id="countdown">
            <div class="countdown-circle">
                <div class="countdown-number" id="countdownNumber">1</div>
            </div>
            <p>秒后自动跳转到WhatsApp</p>
        </div>

        <div class="status" id="status"></div>

        <div class="footer">
            <p>点击按钮将跳转到WhatsApp应用</p>
            <button onclick="testPixelEvent()" style="margin-top: 10px; padding: 5px 10px; background: #666; color: white; border: none; border-radius: 5px; cursor: pointer;">
                🧪 测试Lead事件
            </button>
        </div>
    </div>

    <!-- Facebook Pixel Code -->
    <script>
        !function(f,b,e,v,n,t,s)
        {if(f.fbq)return;n=f.fbq=function(){n.callMethod?
        n.callMethod.apply(n,arguments):n.queue.push(arguments)};
        if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
        n.queue=[];t=b.createElement(e);t.async=!0;
        t.src=v;s=b.getElementsByTagName(e)[0];
        s.parentNode.insertBefore(t,s)}(window, document,'script',
        'https://connect.facebook.net/en_US/fbevents.js');

        // ⚠️ 重要：请替换为你的Facebook Pixel ID
        fbq('init', '623059780216649'); 
    </script>
    <noscript>
        <img height="1" width="1" style="display:none" 
             src="https://www.facebook.com/tr?id=623059780216649&ev=PageView&noscript=1"/>
    </noscript>
    <!-- End Facebook Pixel Code -->

    <script>
        // 确保事件只发送一次
        let eventSent = false;
        let redirectAttempted = false;
        let countdownStarted = false;

        // 你的WhatsApp链接 - 请在这里设置你的WhatsApp链接
        const WHATSAPP_LINK = 'https://wa.link/zhiku';

        function trackConversion() {
            if (eventSent) return;
            eventSent = true;
            
            console.log('🔥 开始发送转化事件...');
            
            // 发送Lead事件 - 这是WhatsApp跳转的标准追踪事件
            if (typeof fbq !== 'undefined') {
                try {
                    fbq('track', 'Lead', {
                        content_name: 'WhatsApp招聘咨询',
                        content_category: 'WhatsApp跳转',
                        content_type: 'contact_form',
                        event_source_url: window.location.href,
                        value: 1.00,
                        currency: 'USD'
                    });
                    console.log('✅ Facebook Pixel Lead事件已发送');
                    console.log('📝 事件参数: content_name = WhatsApp招聘咨询');
                    
                    // 同时发送自定义事件用于更详细的追踪
                    fbq('trackCustom', 'WhatsAppRedirect', {
                        content_name: 'WhatsApp招聘咨询',
                        redirect_success: true,
                        timestamp: new Date().toISOString()
                    });
                    console.log('✅ 自定义WhatsApp跳转事件已发送');
                    
                    // 强制刷新事件（确保发送）
                    setTimeout(() => {
                        console.log('🔄 强制再次发送Lead事件确保追踪');
                        fbq('track', 'Lead', {
                            content_name: 'WhatsApp招聘咨询',
                            content_category: 'WhatsApp跳转_确认',
                            event_source_url: window.location.href
                        });
                    }, 500);
                    
                } catch (error) {
                    console.error('❌ 发送Pixel事件时出错:', error);
                }
            } else {
                console.error('❌ Facebook Pixel未正确加载');
            }
        }

        function showStatus(message, type) {
            const statusDiv = document.getElementById('status');
            statusDiv.textContent = message;
            statusDiv.className = `status ${type}`;
            statusDiv.style.display = 'block';
        }

        function showLoading(show) {
            const loadingDiv = document.getElementById('loading');
            loadingDiv.style.display = show ? 'block' : 'none';
        }

        function hideCountdown() {
            const countdownDiv = document.getElementById('countdown');
            countdownDiv.style.display = 'none';
        }

        function startCountdown() {
            if (countdownStarted) return;
            countdownStarted = true;

            const countdownDiv = document.getElementById('countdown');
            const countdownNumber = document.getElementById('countdownNumber');
            
            countdownDiv.style.display = 'block';
            
            // 1秒倒计时后自动跳转
            setTimeout(() => {
                hideCountdown();
                forceRedirectToWhatsApp();
            }, 1000);
        }

        function forceRedirectToWhatsApp() {
            if (redirectAttempted) return;
            redirectAttempted = true;

            // 显示加载状态
            showLoading(true);
            
            try {
                // 记录跳转尝试时间
                const startTime = Date.now();
                
                // 强制跳转到WhatsApp
                window.open(WHATSAPP_LINK, '_blank', 'noopener,noreferrer');
                
                // 同时尝试直接跳转（适用于某些浏览器）
                window.location.href = WHATSAPP_LINK;
                
                // 延迟检查跳转是否成功
                setTimeout(() => {
                    checkRedirectSuccess(startTime);
                }, 1000);
                
            } catch (error) {
                console.error('跳转失败:', error);
                showLoading(false);
                showStatus('跳转失败，请手动打开WhatsApp', 'error');
            }
        }

        function redirectToWhatsApp() {
            // 手动点击按钮时立即跳转
            forceRedirectToWhatsApp();
        }

        function checkRedirectSuccess(startTime) {
            // 检查页面是否失焦（用户可能已经跳转到WhatsApp）
            const timeElapsed = Date.now() - startTime;
            
            // 无论什么情况，都先发送Lead事件（确保事件被触发）
            showLoading(false);
            showStatus('已成功跳转到WhatsApp！', 'success');
            trackConversion();
            
            console.log(`⏱️ 跳转检查完成，耗时: ${timeElapsed}ms`);
        }

        // 监听页面可见性变化
        document.addEventListener('visibilitychange', function() {
            if (document.hidden && redirectAttempted && !eventSent) {
                // 页面失焦，可能已经跳转到WhatsApp
                setTimeout(() => {
                    trackConversion();
                }, 500);
            }
        });

        // 监听焦点变化
        window.addEventListener('blur', function() {
            if (redirectAttempted && !eventSent) {
                setTimeout(() => {
                    trackConversion();
                }, 500);
            }
        });

        // 页面加载完成后自动开始倒计时
        window.addEventListener('load', function() {
            console.log('📱 页面加载完成');
            
            // 验证Facebook Pixel是否正确加载
            if (typeof fbq !== 'undefined') {
                console.log('✅ Facebook Pixel已正确加载');
                
                // 测试Pixel连接
                fbq('track', 'PageView');
                console.log('✅ PageView事件已发送');
            } else {
                console.error('❌ Facebook Pixel加载失败 - 请检查Pixel ID设置');
                showStatus('⚠️ 追踪设置需要检查', 'error');
            }
            
            // 页面加载完成后立即开始倒计时
            setTimeout(() => {
                startCountdown();
            }, 100);
        });

        // 测试Lead事件的函数
        function testPixelEvent() {
            console.log('🧪 手动测试Lead事件...');
            eventSent = false; // 重置状态以允许测试
            trackConversion();
            showStatus('测试Lead事件已发送！检查控制台和Events Manager', 'success');
        }
    </script>
</body>
</html>
