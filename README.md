<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>الكفايات اللغوية</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(to bottom right, #eef2f3, #8e9eab);
            color: #333;
            margin: 0;
            padding: 0;
            text-align: center;
        }
        header {
            background-color: #4caf50;
            color: white;
            padding: 20px;
            box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);
        }
        h1 {
            margin: 0;
        }
        .content {
            margin: 20px;
        }
        button {
            display: block;
            margin: 10px auto;
            padding: 10px 20px;
            font-size: 18px;
            color: white;
            background-color: #007bff;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: 0.3s;
        }
        button:hover {
            background-color: #0056b3;
        }
        .rule, .sub-rule {
            display: none;
            margin-top: 20px;
            font-size: 18px;
            color: #333;
            background-color: #fff;
            padding: 15px;
            border-radius: 8px;
            border: 1px solid #ddd;
            box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.1);
        }
        .sub-rule {
            background-color: #f9f9f9;
            margin-top: 10px;
        }
        .back-btn {
            margin-top: 15px;
            background-color: #ff5722;
        }
    </style>
</head>
<body>

    <header>
        <h1>الكفايات اللغوية</h1>
    </header>

    <div class="content">
        <p>أهلاً بك في موقعنا التعليمي المميز! 😊</p>
        <p>اختر القاعدة لتتعلم المزيد عنها بطريقة ممتعة.</p>

        <!-- الأزرار الرئيسية -->
        <button onclick="showRule('rule1')">قاعدة المنادى</button>
        <button onclick="showRule('rule2')">قاعدة الاستثناء</button>
        <button onclick="showRule('rule3')">قاعدة التعجب</button>
        <button onclick="showRule('rule4')">قاعدة العدد</button>

        <!-- القواعد -->
        <div id="rule1" class="rule">
            <h3>قاعدة المنادى</h3>
            <button onclick="showSubRule('rule1-examples')">الأمثلة</button>
            <button onclick="showSubRule('rule1-elements')">العناصر</button>
            <button onclick="showSubRule('rule1-summary')">التلخيص</button>
            <button onclick="showSubRule('rule1-grammar')">طريقة الإعراب</button>
            <button class="back-btn" onclick="hideAll()">رجوع</button>
        </div>

        <!-- القاعدة 1 -->
        <div id="rule1-examples" class="sub-rule">
            <h4>أمثلة:</h4>
            <p>1. يا طالبَ العلمِ، اجتهد!</p>
            <p>2. يا أستاذي، شكراً لك!</p>
        </div>
        <div id="rule1-elements" class="sub-rule">
            <h4>العناصر:</h4>
            <p>- أداة النداء: "يا".</p>
            <p>- المنادى: اسم يُطلب إقباله.</p>
            <p>- المضاف إليه أو المفرد.</p>
        </div>
        <div id="rule1-summary" class="sub-rule">
            <h4>التلخيص:</h4>
            <p>المنادى يُستخدم لجذب الانتباه باستخدام أدوات مثل "يا".</p>
        </div>
        <div id="rule1-grammar" class="sub-rule">
            <h4>طريقة الإعراب:</h4>
            <p>يا: أداة نداء لا محل لها من الإعراب.</p>
            <p>طالبَ: منادى منصوب وعلامة نصبه الفتحة.</p>
            <p>العلمِ: مضاف إليه مجرور وعلامة جره الكسرة.</p>
        </div>

        <!-- القاعدة 2 (مثال فقط، انسخ البنية للقاعدة 3 و 4) -->
        <div id="rule2" class="rule">
            <h3>قاعدة الاستثناء</h3>
            <button onclick="showSubRule('rule2-examples')">الأمثلة</button>
            <button onclick="showSubRule('rule2-elements')">العناصر</button>
            <button onclick="showSubRule('rule2-summary')">التلخيص</button>
            <button onclick="showSubRule('rule2-grammar')">طريقة الإعراب</button>
            <button class="back-btn" onclick="hideAll()">رجوع</button>
        </div>
        <div id="rule2-examples" class="sub-rule">
            <h4>أمثلة:</h4>
            <p>1. حضر الطلاب إلا أحمدَ.</p>
            <p>2. ما نجح إلا المجتهد.</p>
        </div>
        <div id="rule2-elements" class="sub-rule">
            <h4>العناصر:</h4>
            <p>- أداة الاستثناء: "إلا".</p>
            <p>- الجملة المثبتة أو المنفية.</p>
            <p>- المستثنى.</p>
        </div>
        <div id="rule2-summary" class="sub-rule">
            <h4>التلخيص:</h4>
            <p>الاستثناء يُخرج شيئًا من حكم ما باستخدام أدوات مثل "إلا".</p>
        </div>
        <div id="rule2-grammar" class="sub-rule">
            <h4>طريقة الإعراب:</h4>
            <p>حضر: فعل ماضٍ مبني.</p>
            <p>الطلابُ: فاعل مرفوع بالضمة.</p>
            <p>إلا: أداة استثناء.</p>
            <p>أحمدَ: مستثنى منصوب بالفتحة.</p>
        </div>
    </div>

    <script>
        function showRule(ruleId) {
            hideAll();
            document.getElementById(ruleId).style.display = 'block';
        }

        function showSubRule(subRuleId) {
            hideSubRules();
            document.getElementById(subRuleId).style.display = 'block';
        }

        function hideAll() {
            const rules = document.querySelectorAll('.rule');
            const subRules = document.querySelectorAll('.sub-rule');
            rules.forEach(rule => rule.style.display = 'none');
            subRules.forEach(subRule => subRule.style.display = 'none');
        }

        function hideSubRules() {
            const subRules = document.querySelectorAll('.sub-rule');
            subRules.forEach(subRule => subRule.style.display = 'none');
        }
    </script>

</body>
</html>
