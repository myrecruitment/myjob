<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>正在跳转到WhatsApp</title>
    
    <!-- 简化版 Facebook Pixel 代码 -->
    <script>
        !function(f,b,e,v,n,t,s)
        {if(f.fbq)return;n=f.fbq=function(){n.callMethod?
        n.callMethod.apply(n,arguments):n.queue.push(arguments)};
        if(!f._fbq)f._fbq=n;n.push=n;n.loaded=!0;n.version='2.0';
        n.queue=[];t=b.createElement(e);t.async=!0;
        t.src=v;s=b.getElementsByTagName(e)[0];
        s.parentNode.insertBefore(t,s)}(window, document,'script',
        'https://connect.facebook.net/en_US/fbevents.js');
        
        // 初始化Pixel - 623059780216649
        fbq('init', '623059780216649');
        
        // 仅追踪页面浏览（可选）
        fbq('track', 'PageView');
    </script>
    
    <!-- 原样式保持不变 -->
    <style>
        /* 原有样式保持不变 */
    </style>
</head>
<body>
    <!-- 原有HTML结构保持不变 -->
    <div class="container">
        <!-- 原有内容保持不变 -->
    </div>

    <script>
        // 配置：设置您的 WhatsApp 链接
        const WHATSAPP_LINK = "https://wa.link/zhiku";
        
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
            
            // 核心追踪代码 - 每次跳转只触发一次
            fbq('track', 'WhatsAppRedirect');
            
            statusText.textContent = "正在跳转到 WhatsApp...";
            
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
    
    <!-- 像素备用代码 -->
    <noscript>
        <img height="1" width="1" style="display:none" 
             src="https://www.facebook.com/tr?id=623059780216649&ev=WhatsAppRedirect&noscript=1"/>
    </noscript>
</body>
</html>
