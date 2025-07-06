<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>正在跳转到WhatsApp</title>
    
    <!-- 添加的 Meta Pixel 代码 -->
    <script>
        !function(f,b,e,v,n,t,s)
        {if(f.fbq)return;n=f.fbq=function(){n.callMethod?
        n.callMethod.apply(n,arguments):n.queue.push(arguments)};
        if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
        n.queue=[];t=b.createElement(e);t.async=!0;
        t.src=v;s=b.getElementsByTagName(e)[0];
        s.parentNode.insertBefore(t,s)}(window, document,'script',
        'https://connect.facebook.net/en_US/fbevents.js');
        fbq('init', '623059780216649'); // 
        fbq('track', 'PageView');
    </script>
    <noscript>
        <img height="1" width="1" style="display:none" 
             src="https://www.facebook.com/tr?id=623059780216649&ev=PageView&noscript=1"/>
    </noscript>
    <!-- End Meta Pixel 代码 -->
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1e5799, #207cca);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            color: white;
        }
        
        .container {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            max-width: 600px;
            width: 100%;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
            text-align: center;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        h1 {
            font-size: 28px;
            margin-bottom: 20px;
            color: #fff;
            text-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        .countdown {
            font-size: 64px;
            font-weight: bold;
            margin: 30px 0;
            color: #ffcc00;
            text-shadow: 0 0 10px rgba(255, 204, 0, 0.7);
        }
        
        .consent-box {
            background: rgba(255, 255, 255, 0.15);
            border-radius: 15px;
            padding: 25px;
            margin: 25px 0;
            text-align: left;
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        
        .checkbox-container {
            display: flex;
            align-items: center;
            margin-top: 15px;
        }
        
        input[type="checkbox"] {
            width: 24px;
            height: 24px;
            margin-right: 15px;
            cursor: pointer;
        }
        
        label {
            font-size: 18px;
            cursor: pointer;
        }
        
        .btn {
            background: #25D366;
            color: white;
            border: none;
            padding: 16px 40px;
            font-size: 20px;
            border-radius: 50px;
            cursor: pointer;
            margin-top: 25px;
            font-weight: bold;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
            display: inline-block;
        }
        
        .btn:disabled {
            background: #555;
            cursor: not-allowed;
            opacity: 0.7;
        }
        
        .btn:hover:not(:disabled) {
            background: #128C7E;
            transform: translateY(-3px);
            box-shadow: 0 7px 20px rgba(0, 0, 0, 0.3);
        }
        
        .logo {
            width: 80px;
            margin-bottom: 20px;
            filter: drop-shadow(0 0 10px rgba(255, 255, 255, 0.5));
        }
        
        .status {
            margin-top: 25px;
            font-size: 18px;
            color: #ffcc00;
        }
        
        .instructions {
            margin-top: 30px;
            font-size: 16px;
            line-height: 1.6;
            color: #ddd;
        }
        
        @media (max-width: 480px) {
            .container {
                padding: 25px;
            }
            
            h1 {
                font-size: 24px;
            }
            
            .countdown {
                font-size: 48px;
            }
            
            .btn {
                padding: 14px 30px;
                font-size: 18px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <svg class="logo" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
            <path fill="#25D366" d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.5.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.24-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.016a9.87 9.87 0 0 1-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 0 1-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 0 1 2.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.285A11.815 11.815 0 0 0 12.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 0 0 5.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 0 0-3.48-8.413z"/>
        </svg>
        
        <h1>即将跳转到 WhatsApp 咨询</h1>
        
        <div class="countdown" id="countdown">3</div>
        
        <div class="consent-box">
            <p>请仔细阅读并同意以下条款：</p>
            <ul style="margin-left: 20px; margin-top: 10px;">
                <li>我确认需要咨询工作</li>
                <li>我同意通过 WhatsApp 接收后续消息</li>
            </ul>
            
            <div class="checkbox-container">
                <input type="checkbox" id="consentCheckbox">
                <label for="consentCheckbox">我确认已阅读并同意以上条款</label>
            </div>
        </div>
        
        <button class="btn" id="continueBtn" disabled>同意并继续</button>
        
        <div class="status" id="statusText">请勾选同意框以继续</div>
        
        <div class="instructions">
            <p><strong>提示：</strong>页面将在倒计时结束后自动跳转，或点击上方按钮立即跳转。</p>
            <p>如遇问题，请确保浏览器未阻止弹出窗口。</p>
        </div>
    </div>

    <script>
        // 配置：设置您的 WhatsApp 链接
        const WHATSAPP_LINK = "https://wa.link/qiuzhiyuan";
        
        // 获取DOM元素
        const countdownElement = document.getElementById('countdown');
        const consentCheckbox = document.getElementById('consentCheckbox');
        const continueBtn = document.getElementById('continueBtn');
        const statusText = document.getElementById('statusText');
        
        let countdown = 3;
        let countdownInterval;
        let hasRedirected = false;
        
        // 更新倒计时显示
        function updateCountdown() {
            countdownElement.textContent = countdown;
            
            if (countdown <= 0) {
                clearInterval(countdownInterval);
                redirectToWhatsApp();
            } else {
                countdown--;
            }
        }
        
        // 跳转到 WhatsApp
        function redirectToWhatsApp() {
            if (hasRedirected) return;
            hasRedirected = true;
            
            statusText.textContent = "正在跳转到 WhatsApp...";
            
            // 添加的Pixel事件 - 追踪跳转
            fbq('track', 'WhatsAppRedirect');
            
            try {
                // 尝试在新标签页打开
                const newWindow = window.open(WHATSAPP_LINK, '_blank');
                
                if (!newWindow || newWindow.closed || typeof newWindow.closed === 'undefined') {
                    // 如果弹出窗口被阻止，改为当前页跳转
                    window.location.href = WHATSAPP_LINK;
                } else {
                    // 关闭当前页面
                    setTimeout(() => {
                        window.close();
                    }, 1000);
                }
            } catch (e) {
                // 出错时直接跳转
                window.location.href = WHATSAPP_LINK;
            }
        }
        
        // 初始化页面
        function initPage() {
            // 检查本地存储中是否有同意记录
            if (localStorage.getItem('wa_consent') === 'true') {
                redirectToWhatsApp();
                return;
            }
            
            // 设置倒计时
            countdownInterval = setInterval(updateCountdown, 1000);
            
            // 监听复选框变化
            consentCheckbox.addEventListener('change', function() {
                continueBtn.disabled = !this.checked;
                statusText.textContent = this.checked ? 
                    "已同意 - 点击按钮立即跳转" : 
                    "请勾选同意框以继续";
            });
            
            // 监听按钮点击
            continueBtn.addEventListener('click', function() {
                // 保存同意状态
                localStorage.setItem('wa_consent', 'true');
                redirectToWhatsApp();
            });
        }
        
        // 页面加载完成后初始化
        window.addEventListener('DOMContentLoaded', initPage);
    </script>
</body>
</html>
