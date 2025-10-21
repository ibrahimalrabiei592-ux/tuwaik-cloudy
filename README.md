[index.html.html](https://github.com/user-attachments/files/23015787/index.html.html)
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>دليل حجز قاعات المكتبة</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #1e5f5f 0%, #2d8b8b 100%);
            min-height: 100vh;
            padding: 20px;
            direction: rtl;
        }

        .container {
            max-width: 900px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, #1e5f5f 0%, #2d8b8b 100%);
            color: white;
            padding: 40px;
            text-align: center;
        }

        .header h1 {
            font-size: 2.2em;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        }

        .header p {
            font-size: 1.1em;
            opacity: 0.95;
        }

        .content {
            padding: 40px;
        }

        .step {
            margin-bottom: 20px;
            padding: 25px;
            background: #f8f9fa;
            border-radius: 15px;
            border-right: 5px solid #2d8b8b;
            display: none;
        }

        .step.active {
            display: block;
            animation: fadeIn 0.5s ease;
        }

        @keyframes fadeIn {
            from {
                opacity: 0;
                transform: translateY(10px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .step-number {
            display: inline-block;
            width: 45px;
            height: 45px;
            background: linear-gradient(135deg, #1e5f5f 0%, #2d8b8b 100%);
            color: white;
            border-radius: 50%;
            text-align: center;
            line-height: 45px;
            font-size: 1.3em;
            font-weight: bold;
            margin-left: 15px;
            box-shadow: 0 4px 10px rgba(45, 139, 139, 0.3);
        }

        .step-title {
            font-size: 1.5em;
            color: #1e5f5f;
            margin-bottom: 15px;
            font-weight: bold;
        }

        .step-content {
            color: #555;
            font-size: 1.1em;
            line-height: 1.8;
            margin-right: 60px;
        }

        .link-box {
            background: #e8f4f4;
            padding: 15px 20px;
            border-radius: 10px;
            margin: 15px 0;
            border: 2px solid #2d8b8b;
        }

        .link-box a {
            color: #1e5f5f;
            text-decoration: none;
            font-weight: bold;
            word-break: break-all;
        }

        .link-box a:hover {
            color: #2d8b8b;
            text-decoration: underline;
        }

        .image-container {
            margin: 15px 0;
            text-align: center;
            padding: 10px;
            background: white;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        .image-container img {
            max-width: 100%;
            height: auto;
            border-radius: 8px;
            border: 3px solid #2d8b8b;
            max-height: 500px;
            object-fit: contain;
        }

        .navigation {
            display: flex;
            justify-content: space-between;
            margin-top: 30px;
            gap: 15px;
        }

        .btn {
            padding: 15px 35px;
            background: linear-gradient(135deg, #1e5f5f 0%, #2d8b8b 100%);
            color: white;
            border: none;
            border-radius: 10px;
            cursor: pointer;
            font-size: 1.1em;
            font-weight: bold;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(45, 139, 139, 0.3);
        }

        .btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(45, 139, 139, 0.4);
        }

        .btn:disabled {
            background: #ccc;
            cursor: not-allowed;
            box-shadow: none;
        }

        .progress-bar {
            width: 100%;
            height: 8px;
            background: #e0e0e0;
            border-radius: 10px;
            margin-bottom: 30px;
            overflow: hidden;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, #1e5f5f 0%, #2d8b8b 100%);
            transition: width 0.5s ease;
            border-radius: 10px;
        }

        .highlight {
            background: #fff3cd;
            padding: 3px 8px;
            border-radius: 5px;
            font-weight: bold;
            color: #856404;
        }

        .info-box {
            background: #d1ecf1;
            border: 2px solid #0c5460;
            border-radius: 10px;
            padding: 15px;
            margin: 15px 0;
            color: #0c5460;
        }

        .info-box strong {
            display: block;
            margin-bottom: 8px;
            font-size: 1.1em;
        }

        .warning-box {
            background: #fff3cd;
            border: 2px solid #856404;
            border-radius: 10px;
            padding: 15px;
            margin: 15px 0;
            color: #856404;
        }

        .success-box {
            background: #d4edda;
            border: 2px solid #155724;
            border-radius: 10px;
            padding: 15px;
            margin: 15px 0;
            color: #155724;
        }

        .important-box {
            background: #f8d7da;
            border: 2px solid #721c24;
            border-radius: 10px;
            padding: 15px;
            margin: 15px 0;
            color: #721c24;
        }

        @media (max-width: 768px) {
            .header h1 {
                font-size: 1.5em;
            }

            .content {
                padding: 20px;
            }

            .step {
                padding: 20px;
            }

            .step-content {
                margin-right: 0;
                margin-top: 15px;
            }

            .navigation {
                flex-direction: column;
            }

            .btn {
                width: 100%;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🏛️ دليل حجز قاعات المكتبة</h1>
            <p>كلية العلوم الشرعية - سلطنة عُمان</p>
        </div>

        <div class="content">
            <div class="progress-bar">
                <div class="progress-fill" id="progressFill"></div>
            </div>

            <div id="stepsContainer"></div>

            <div class="navigation">
                <button class="btn" id="prevBtn" onclick="changeStep(-1)" disabled>⮜ السابق</button>
                <button class="btn" id="nextBtn" onclick="changeStep(1)">التالي ⮞</button>
            </div>
        </div>
    </div>

    <script>
        const steps = [
            {
                title: "الدخول إلى موقع المكتبة",
                content: `
                    <p>ابدأ بالدخول إلى رابط مكتبة كلية العلوم الشرعية من خلال الرابط التالي:</p>
                    <div class="link-box">
                        <a href="https://library.css.edu.om" target="_blank">🔗 https://library.css.edu.om</a>
                    </div>
                    <p>سيتم نقلك إلى الصفحة الرئيسية للمكتبة حيث ستجد مجموعة من الخدمات والموارد المتاحة.</p>
                    <div class="image-container">
                        <img src="https://i.imgur.com/0OX6c4G.png" alt="الصفحة الرئيسية للمكتبة" />
                        <p style="margin-top: 10px; color: #666; font-size: 0.9em;">الصفحة الرئيسية لمكتبة كلية العلوم الشرعية</p>
                    </div>
                `
            },
            {
                title: "تسجيل الدخول إلى حسابك",
                content: `
                    <p>للوصول إلى خدمة حجز القاعات، يجب عليك تسجيل الدخول باستخدام بيانات حسابك الجامعي:</p>
                    <div class="info-box">
                        <strong>📝 معلومات مطلوبة:</strong>
                        <ul style="margin-right: 20px; margin-top: 10px;">
                            <li><span class="highlight">اسم المستخدم:</span> عنوان بريدك الإلكتروني الجامعي (مثال: username@css.edu.om)</li>
                            <li><span class="highlight">كلمة المرور:</span> كلمة المرور الخاصة بحسابك</li>
                        </ul>
                    </div>
                    <p>اضغط على زر "دخول" في أعلى الصفحة، ثم أدخل بياناتك في النافذة المنبثقة.</p>
                    <div class="image-container">
                        <img src="https://i.imgur.com/vasMfv1.png" alt="نافذة تسجيل الدخول" />
                        <p style="margin-top: 10px; color: #666; font-size: 0.9em;">نافذة تسجيل الدخول إلى المكتبة</p>
                    </div>
                `
            },
            {
                title: "الانتقال إلى صفحة حجوزات القاعات",
                content: `
                    <p>بعد تسجيل الدخول بنجاح، ابحث عن قسم <span class="highlight">"حجوزات القاعات"</span> في القائمة الجانبية.</p>
                    <div class="image-container">
                        <img src="https://i.imgur.com/0yAbUF1.png" alt="القائمة الجانبية" />
                        <p style="margin-top: 10px; color: #666; font-size: 0.9em;">القائمة الجانبية تحتوي على خيار "حجوزات القاعات"</p>
                    </div>
                    <div class="info-box" style="margin-top: 15px;">
                        <strong>💡 نصيحة:</strong>
                        ستجد خيار "حجوزات القاعات" في القائمة الجانبية بعد تسجيل الدخول مباشرة.
                    </div>
                    <p>اضغط على الرابط للانتقال إلى صفحة الحجز.</p>
                `
            },
            {
                title: "عرض التقويم واختيار التاريخ",
                content: `
                    <p>بعد الدخول لصفحة حجوزات القاعات، سيظهر لك تقويم شهري يعرض الأيام المتاحة:</p>
                    <div class="image-container">
                        <img src="https://i.imgur.com/Ew6hZvA.png" alt="التقويم الشهري" />
                        <p style="margin-top: 10px; color: #666; font-size: 0.9em;">التقويم الشهري لحجز القاعات - عرض اليوم</p>
                    </div>
                    <p style="margin-top: 15px;">يمكنك أيضاً التبديل إلى العرض الأسبوعي للحصول على تفاصيل أكثر:</p>
                    <div class="image-container">
                        <img src="https://i.imgur.com/r3AcOE5.png" alt="العرض الأسبوعي" />
                        <p style="margin-top: 10px; color: #666; font-size: 0.9em;">العرض الأسبوعي مع الأوقات المفصلة</p>
                    </div>
                    <p style="margin-top: 15px;">أو استخدم قائمة القاعات المتاحة لمعرفة القاعات وأوقاتها:</p>
                    <div class="image-container">
                        <img src="https://i.imgur.com/1lymNSs.png" alt="قائمة القاعات" />
                        <p style="margin-top: 10px; color: #666; font-size: 0.9em;">قائمة القاعات المتاحة ومواعيدها</p>
                    </div>
                    <div class="info-box">
                        <strong>📅 خطوات اختيار التاريخ:</strong>
                        <ul style="margin-right: 20px; margin-top: 10px; line-height: 2;">
                            <li>اختر الشهر المناسب من أعلى التقويم</li>
                            <li>يمكنك التبديل بين العرض اليومي والأسبوعي والشهري</li>
                            <li>اضغط على اليوم أو الوقت الذي ترغب في الحجز فيه</li>
                            <li>راجع القاعات المتاحة والأوقات الفارغة</li>
                        </ul>
                    </div>
                `
            },
            {
                title: "تحديد تفاصيل الحجز",
                content: `
                    <p>بعد اختيار اليوم والوقت، ستظهر لك نافذة منبثقة لإدخال تفاصيل الحجز:</p>
                    <div class="image-container">
                        <img src="https://i.imgur.com/XA1UClx.png" alt="نموذج الحجز" />
                        <p style="margin-top: 10px; color: #666; font-size: 0.9em;">نموذج إضافة حجز جديد للقاعة</p>
                    </div>
                    <div class="info-box">
                        <strong>📝 المعلومات المطلوبة:</strong>
                        <ul style="margin-right: 20px; margin-top: 10px; line-height: 2;">
                            <li><span class="highlight">اسم القاعة:</span> اختر القاعة المناسبة من القائمة المنسدلة</li>
                            <li><span class="highlight">اسم التصنيف:</span> حدد نوع الحجز أو الفئة</li>
                            <li><span class="highlight">تاريخ الحجز:</span> سيكون محدداً تلقائياً حسب اختيارك</li>
                            <li><span class="highlight">ساعة البداية:</span> حدد وقت بداية الحجز (مثال: 10:00)</li>
                            <li><span class="highlight">ساعة النهاية:</span> حدد وقت انتهاء الحجز (مثال: 11:00)</li>
                            <li><span class="highlight">عدد الحضور:</span> أدخل عدد الأشخاص المتوقع حضورهم</li>
                            <li><span class="highlight">موضوع الحجز:</span> اكتب سبب أو هدف الحجز بشكل واضح</li>
                            <li><span class="highlight">الأهداف:</span> يمكنك إضافة أهداف تفصيلية (اختياري)</li>
                            <li><span class="highlight">التفاصيل:</span> أي معلومات إضافية تود إضافتها</li>
                        </ul>
                    </div>
                    <p style="margin-top: 15px; background: #e8f4f4; padding: 15px; border-radius: 8px; border-right: 4px solid #2d8b8b;">
                        <strong>📌 تنبيه:</strong> تأكد من ملء جميع الحقول الإلزامية (المشار إليها بـ <span style="color: red;">*</span>) قبل الحفظ.
                    </p>
                `
            },
            {
                title: "تأكيد الحجز والمراجعة",
                content: `
                    <p>بعد إدخال جميع التفاصيل المطلوبة:</p>
                    <div class="info-box">
                        <strong>✅ خطوات التأكيد:</strong>
                        <ol style="margin-right: 20px; margin-top: 8px; line-height: 1.8;">
                            <li>راجع جميع المعلومات المدخلة للتأكد من صحتها</li>
                            <li>اضغط على زر <span class="highlight">"حفظ"</span> في أسفل النموذج</li>
                            <li>ستظهر لك رسالة تأكيد إرسال الطلب بنجاح</li>
                            <li>سيظهر حجزك في التقويم بحالة "قيد الانتظار"</li>
                        </ol>
                    </div>
                    
                    <div class="success-box">
                        <strong>📧 عملية الاعتماد:</strong>
                        <ul style="margin-right: 20px; margin-top: 8px; line-height: 1.8;">
                            <li>سيصل إشعار بطلب حجزك إلى <span class="highlight">مشرفي المكتبة</span></li>
                            <li>سيقوم المشرفون بمراجعة طلبك واعتماده</li>
                            <li>عند الاعتماد، ستصلك رسالة تأكيد على <span class="highlight">بريدك الإلكتروني الجامعي</span></li>
                            <li>يمكنك متابعة حالة حجزك من خلال التقويم</li>
                        </ul>
                    </div>

                    <div class="warning-box">
                        <strong>⚠️ ملاحظات هامة:</strong>
                        <ul style="margin-right: 20px; margin-top: 8px; line-height: 1.8;">
                            <li>احتفظ برقم الحجز والتفاصيل</li>
                            <li>تأكد من الحضور في الوقت المحدد</li>
                            <li>في حالة التأخير أو الإلغاء، يرجى إبلاغ إدارة المكتبة مسبقاً</li>
                            <li>يمكنك التعديل على حجزك قبل الاعتماد من خلال التقويم</li>
                        </ul>
                    </div>

                    <div class="important-box">
                        <strong>🚫 تنبيه مهم - النظام الجديد:</strong>
                        <p style="margin-top: 8px; line-height: 1.8;">
                            تم <strong>التوقف عن العمل بالنظام السابق</strong> لحجز القاعات الذي كان متاحاً عبر الرابط المباشر. 
                            جميع الحجوزات الآن يجب أن تتم من خلال هذا <strong>النظام الجديد فقط</strong> عبر موقع المكتبة الإلكتروني.
                        </p>
                    </div>

                    <div style="text-align: center; margin-top: 20px; padding: 20px; background: linear-gradient(135deg, #1e5f5f 0%, #2d8b8b 100%); border-radius: 10px; color: white;">
                        <h3 style="margin-bottom: 10px;">🎉 تهانينا!</h3>
                        <p style="font-size: 1.1em;">لقد أكملت جميع خطوات حجز قاعات المكتبة بنجاح</p>
                        <p style="margin-top: 8px; opacity: 0.9;">نتمنى لك تجربة مثمرة في استخدام قاعات المكتبة 📚</p>
                    </div>
                `
            }
        ];

        let currentStep = 0;

        function renderSteps() {
            const container = document.getElementById('stepsContainer');
            container.innerHTML = '';
            
            const stepDiv = document.createElement('div');
            stepDiv.className = 'step active';
            stepDiv.innerHTML = `
                <div class="step-title">
                    <span class="step-number">${currentStep + 1}</span>
                    ${steps[currentStep].title}
                </div>
                <div class="step-content">
                    ${steps[currentStep].content}
                </div>
            `;
            
            container.appendChild(stepDiv);
            
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function updateProgress() {
            const progress = ((currentStep + 1) / steps.length) * 100;
            document.getElementById('progressFill').style.width = progress + '%';
        }

        function changeStep(direction) {
            const newStep = currentStep + direction;
            
            if (newStep >= 0 && newStep < steps.length) {
                currentStep = newStep;
                renderSteps();
                updateProgress();
                updateButtons();
            }
        }

        function updateButtons() {
            const prevBtn = document.getElementById('prevBtn');
            const nextBtn = document.getElementById('nextBtn');
            
            prevBtn.disabled = currentStep === 0;
            
            if (currentStep === steps.length - 1) {
                nextBtn.textContent = '✓ إنهاء';
                nextBtn.onclick = () => {
                    alert('🎉 تهانينا! لقد أكملت دليل حجز قاعات المكتبة بنجاح!\n\nيمكنك الآن البدء في حجز القاعات من خلال موقع المكتبة.');
                    currentStep = 0;
                    renderSteps();
                    updateProgress();
                    updateButtons();
                };
            } else {
                nextBtn.textContent = 'التالي ⮞';
                nextBtn.onclick = () => changeStep(1);
            }
        }

        renderSteps();
        updateProgress();
        updateButtons();
    </script>
</body>
</html>
