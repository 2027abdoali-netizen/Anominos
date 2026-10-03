# Anominos<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>منصة الهكر العربي - التقييم والاختبارات السيبرانية</title>
    <!-- Google Fonts & FontAwesome Icons -->
    <link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;500;700;900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        :root {
            --bg-color: #0d1117;
            --card-bg: #161b22;
            --accent-green: #00ff66;
            --accent-blue: #58a6ff;
            --text-primary: #c9d1d9;
            --text-heading: #ffffff;
            --border-color: #30363d;
            --shadow-glow: 0 0 15px rgba(0, 255, 102, 0.2);
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Tajawal', sans-serif;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-primary);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            background-image: radial-gradient(circle at 50% 10%, rgba(0, 255, 102, 0.05), transparent 40%);
        }

        .container {
            width: 100%;
            max-width: 480px;
            background: var(--card-bg);
            border: 1px solid var(--border-color);
            border-radius: 16px;
            padding: 28px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
            position: relative;
            overflow: hidden;
        }

        .container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 4px;
            background: linear-gradient(90deg, var(--accent-green), var(--accent-blue));
        }

        /* Top Bar Header */
        .top-nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 24px;
        }

        .admin-btn {
            background: #21262d;
            color: var(--accent-green);
            border: 1px solid var(--border-color);
            padding: 8px 14px;
            border-radius: 8px;
            font-size: 0.85rem;
            cursor: pointer;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: all 0.3s ease;
        }

        .admin-btn:hover {
            border-color: var(--accent-green);
            box-shadow: var(--shadow-glow);
        }

        .status-badge {
            font-size: 0.75rem;
            color: var(--accent-green);
            background: rgba(0, 255, 102, 0.1);
            padding: 4px 10px;
            border-radius: 20px;
            border: 1px solid rgba(0, 255, 102, 0.2);
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .status-dot {
            width: 6px;
            height: 6px;
            background-color: var(--accent-green);
            border-radius: 50%;
            box-shadow: 0 0 8px var(--accent-green);
        }

        /* Main Logo & Title */
        .header {
            text-align: center;
            margin-bottom: 24px;
        }

        .logo-icon {
            width: 70px;
            height: 70px;
            background: rgba(0, 255, 102, 0.1);
            border: 2px solid var(--accent-green);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0 auto 12px;
            color: var(--accent-green);
            font-size: 1.8rem;
            box-shadow: var(--shadow-glow);
        }

        .header h1 {
            color: var(--text-heading);
            font-size: 1.5rem;
            font-weight: 700;
            margin-bottom: 4px;
        }

        .header p {
            color: #8b949e;
            font-size: 0.85rem;
        }

        /* Form Fields */
        .form-group {
            margin-bottom: 16px;
        }

        .form-group label {
            display: block;
            font-size: 0.85rem;
            margin-bottom: 6px;
            color: var(--text-heading);
        }

        .input-wrapper {
            position: relative;
        }

        .input-wrapper i {
            position: absolute;
            right: 14px;
            top: 50%;
            transform: translateY(-50%);
            color: #8b949e;
        }

        .custom-input, select.custom-input {
            width: 100%;
            padding: 12px 42px 12px 14px;
            background-color: #0d1117;
            border: 1px solid var(--border-color);
            border-radius: 8px;
            color: var(--text-heading);
            font-size: 0.9rem;
            outline: none;
            transition: border-color 0.3s;
        }

        .custom-input:focus {
            border-color: var(--accent-green);
            box-shadow: var(--shadow-glow);
        }

        select.custom-input option {
            background-color: var(--card-bg);
            color: var(--text-heading);
        }

        /* Buttons */
        .btn-primary {
            width: 100%;
            padding: 12px;
            background: linear-gradient(135deg, #238636, #2ea043);
            color: #fff;
            border: none;
            border-radius: 8px;
            font-size: 1rem;
            font-weight: 700;
            cursor: pointer;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 8px;
            transition: all 0.3s ease;
        }

        .btn-primary:hover {
            opacity: 0.9;
            box-shadow: 0 0 15px rgba(46, 160, 67, 0.4);
        }

        .divider {
            display: flex;
            align-items: center;
            text-align: center;
            margin: 20px 0;
            color: #8b949e;
            font-size: 0.8rem;
        }

        .divider::before, .divider::after {
            content: '';
            flex: 1;
            border-bottom: 1px solid var(--border-color);
        }

        .divider span {
            padding: 0 10px;
        }

        .btn-gold {
            width: 100%;
            padding: 12px;
            background: transparent;
            color: #d29922;
            border: 1px solid #d29922;
            border-radius: 8px;
            font-size: 0.95rem;
            font-weight: 700;
            cursor: pointer;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 8px;
            transition: all 0.3s ease;
        }

        .btn-gold:hover {
            background: rgba(210, 153, 34, 0.1);
            box-shadow: 0 0 12px rgba(210, 153, 34, 0.3);
        }

        .card-secondary {
            background-color: #0d1117;
            border: 1px solid var(--border-color);
            border-radius: 12px;
            padding: 16px;
            margin-top: 10px;
        }

        .card-title {
            font-size: 0.85rem;
            color: var(--accent-blue);
            margin-bottom: 12px;
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .btn-secondary {
            width: 100%;
            padding: 10px;
            background-color: #21262d;
            color: var(--accent-blue);
            border: 1px solid var(--border-color);
            border-radius: 8px;
            font-size: 0.9rem;
            font-weight: 500;
            cursor: pointer;
            margin-top: 10px;
            transition: border-color 0.3s;
        }

        .btn-secondary:hover {
            border-color: var(--accent-blue);
        }

        .footer {
            margin-top: 24px;
            text-align: center;
            font-size: 0.75rem;
            color: #8b949e;
            border-top: 1px solid var(--border-color);
            padding-top: 16px;
        }

        .footer p span {
            color: var(--accent-green);
        }
    </style>
</head>
<body>

<div class="container">
    <!-- Top Nav -->
    <div class="top-nav">
        <button class="admin-btn">
            <i class="fa-solid fa-user-shield"></i>
            لوحة التحكم
        </button>
        <div class="status-badge">
            <div class="status-dot"></div>
            النظام متصل
        </div>
    </div>

    <!-- Header -->
    <div class="header">
        <div class="logo-icon">
            <i class="fa-solid fa-terminal"></i>
        </div>
        <h1>منصة الهكر العربي</h1>
        <p>اختبارات وتقييم المهارات في الأمن السيبراني</p>
    </div>

    <!-- Main Registration Form -->
    <form onsubmit="return false;">
        <div class="form-group">
            <label for="track">المسار التعليمي / التخصص</label>
            <div class="input-wrapper">
                <i class="fa-solid fa-layer-group"></i>
                <select id="track" class="custom-input">
                    <option value="web">اختراق التطبيقات والويب (Web Pentesting)</option>
                    <option value="network">أمن الشبكات والإنترنت (Network Security)</option>
                    <option value="reverse">الهندسة العكسية والبرمجيات الخبيثة (Reverse Engineering)</option>
                    <option value="soc">تحليل الحوادث ومراقبة SOC (Blue Teaming)</option>
                </select>
            </div>
        </div>

        <div class="form-group">
            <label for="username">الاسم بالكامل / المقب المتخصص</label>
            <div class="input-wrapper">
                <i class="fa-solid fa-user-ninja"></i>
                <input type="text" id="username" class="custom-input" placeholder="أدخل اسمك أو الكود الخاص بك">
            </div>
        </div>

        <div class="form-group">
            <label for="phone">رقم الهاتف أو المعرّف</label>
            <div class="input-wrapper">
                <i class="fa-solid fa-mobile-screen-button"></i>
                <input type="tel" id="phone" class="custom-input" placeholder="01XXXXXXXXX">
            </div>
        </div>

        <button type="submit" class="btn-primary">
            <i class="fa-solid fa-code"></i>
            بدء الاختبار السيبراني
        </button>
    </form>

    <div class="divider">
        <span>أو</span>
    </div>

    <!-- Leaderboard Button -->
    <button class="btn-gold">
        <i class="fa-solid fa-trophy"></i>
        قائمة المتصدرين والجوائز
    </button>

    <!-- Result Verification Box -->
    <div class="card-secondary" style="margin-top: 16px;">
        <div class="card-title">
            <i class="fa-solid fa-key"></i>
            التحقق من النتيجة أو الشهادة
        </div>
        <div class="input-wrapper">
            <i class="fa-solid fa-lock"></i>
            <input type="text" class="custom-input" placeholder="أدخل الكود السري للاختبار">
        </div>
        <button class="btn-secondary">
            <i class="fa-solid fa-magnifying-glass"></i>
            عرض النتيجة
        </button>
    </div>

    <!-- Footer Credit -->
    <div class="footer">
        <p>تطوير وتصميم: <span>فريق الهكر العربي</span></p>
        <p style="margin-top: 4px;">جميع الحقوق محفوظة &copy; 2026</p>
    </div>
</div>

</body>
</html>
