 **Git** كأنك تستخدمه فقط لنسخ (Clone) المشاريع من الإنترنت بدون أي تعقيدات إضافية.

---

### **ما هو Git (كمستنسخ فقط)؟**
- هو أداة تسمح لك بنسخ مشاريع جاهزة من الإنترنت (عادةً من منصات مثل GitHub) مباشرةً إلى جهازك.
- بمجرد نسخ المشروع، يكون عندك نسخة كاملة من الملفات كما هي على الإنترنت.

---

### **كيف تستخدم Git للاستنساخ فقط؟**

#### 1. **التأكد من وجود Git على جهازك**
- افتح الطرفية (Terminal) وتأكد أن Git مثبت:
  ```
  $ git --version
  ```
  إذا ظهر رقم إصدار مثل `git version 2.x.x`، فكل شيء تمام.  
  إذا لم يكن مثبتًا، يمكنك تثبيته على توزيعات Linux مثل Ubuntu:
  ```
  $ sudo apt-get install git
  ```

---

#### 2. **البحث عن مشروع تريد نسخه**
- اذهب إلى موقع GitHub (أو أي منصة أخرى)، واختر المشروع الذي تريده.
- انسخ رابط المشروع من الزر "Code" (تأكد أن الرابط يبدأ بـ `https://`).

---

#### 3. **نسخ المشروع باستخدام Git**
- في الطرفية، اذهب إلى المكان الذي تريد وضع المشروع فيه:
  ```
  $ cd /path/to/your/folder
  ```
- نفذ أمر الاستنساخ:
  ```
  $ git clone https://github.com/username/repository.git
  ```

#### مثال عملي:
- إذا كان الرابط:
  ```
  https://github.com/torvalds/linux.git
  ```
- الأمر سيكون:
  ```
  $ git clone https://github.com/torvalds/linux.git
  ```

---

#### 4. **النتيجة:**
- بمجرد تنفيذ الأمر، ستظهر مجلدات وملفات المشروع في جهازك.  
- مثال على النتيجة:
  ```
  Cloning into 'linux'...
  remote: Enumerating objects: 123456, done.
  remote: Counting objects: 100% (123456/123456), done.
  remote: Compressing objects: 100% (12345/12345), done.
  Receiving objects: 100% (123456/123456), done.
  Resolving deltas: 100% (67890/67890), done.
  ```

- الآن إذا كتبت:
  ```
  $ ls
  ```
  سترى مجلد المشروع (مثل `linux`).

---

### **أوامر إضافية قد تهمك:**
#### تحديث نسخة المشروع:
- إذا كان المشروع محدثًا وتريد الحصول على آخر التغييرات:
  ```
  $ git pull
  ```

#### حذف المشروع إذا انتهيت منه:
- يمكنك حذف المجلد باستخدام الأمر:
  ```
  $ rm -r project_name
  ```

---

### **أهمية Git كأداة استنساخ:**
- بدلاً من تحميل ملفات المشروع يدويًا، Git يجعل العملية أسرع وأسهل.
- كل ما تحتاجه هو رابط المشروع، وبأمر واحد تحصل على النسخة كاملة.


---

أكيد يا صديقي! الآن خليني أشرح لك **GitHub** ببساطة.

---

### **ما هو GitHub؟**

- **GitHub** هو منصة على الإنترنت تُستخدم لاستضافة المشاريع التي تستخدم Git.
- ببساطة، يمكنك تخزين الكود الذي تكتبه (سواء كنت تعمل بمفردك أو مع فريق) ومشاركته مع الآخرين.
- يتيح لك **GitHub** التعاون مع المطورين الآخرين، وتتبع التغييرات، والعمل على مشاريع برمجية مختلفة.

---

### **كيف يعمل GitHub؟**

- **GitHub** هو خدمة استضافة للمشاريع التي تستخدم Git.
- كل مشروع على GitHub يتم تخزينه في "مستودع" (Repository) يمكن أن يحتوي على ملفات، أكواد، مستندات، وأشياء أخرى.
- **GitHub** يعمل على تسهيل مشاركة وتعديل المشاريع بين فرق العمل المختلفة. كما أنه يسمح لك **بإرسال التعديلات** عبر **Pull Requests**.

---

### **المفاهيم الرئيسية في GitHub:**
1. **المستودع (Repository):**
   - هو المكان الذي يتم فيه تخزين المشروع على GitHub. مثل مجلد يحتوي على جميع ملفات المشروع.
   - كل مستودع يحتوي على تاريخ التغييرات (التعليقات أو الـ commits).
   
2. **Fork (التفريع):**
   - إذا أردت تعديل مشروع شخص آخر على GitHub، يمكنك "تفريع" (أخذ نسخة من) المستودع الخاص به والعمل عليه. يمكنك تعديل الكود كما تريد ثم "إرسال" هذه التعديلات مرة أخرى باستخدام **Pull Requests**.

3. **Pull Request (طلب السحب):**
   - هو طلب لدمج التعديلات التي قمت بها في مستودع شخص آخر. بعد أن تقوم بالتعديلات، تطلب من صاحب المستودع دمج التغييرات.

4. **Commit (التعليق):**
   - عند تعديل الكود، تقوم بحفظ هذه التغييرات على Git باستخدام ما يسمى بـ "Commit". كل Commit يحتوي على رسالة توضح التغييرات التي أجريتها.

5. **Branch (الفرع):**
   - الفرع هو نسخة من المستودع يمكنك العمل عليها بشكل مستقل عن الفرع الرئيسي (عادة يسمى `main` أو `master`). هذه الطريقة تساعدك على تجنب التأثير على الكود الأساسي أثناء التعديلات.

---

### **كيفية استخدام GitHub:**

#### 1. **إنشاء حساب على GitHub:**
   - أول شيء يجب فعله هو التسجيل على GitHub عبر الرابط: [https://github.com](https://github.com)
   - بعد التسجيل، يمكنك إنشاء مستودع جديد.

#### 2. **إنشاء مستودع جديد:**
   - بعد الدخول إلى حسابك في GitHub، اضغط على زر "New Repository" في صفحتك الشخصية.
   - اختر اسم للمستودع وأضف بعض الوصف (اختياري).
   - اختر إذا كنت تريد أن يكون المستودع **عام** (Public) أو **خاص** (Private).

#### 3. **رفع الملفات إلى GitHub (Push):**
   - بعد إنشاء مستودع، يمكنك رفع ملفاتك إليه باستخدام Git من الطرفية.
   - خطوات رفع الملفات:
     1. انتقل إلى المجلد الذي يحتوي على ملفاتك:
        ```
        $ cd /path/to/your/project
        ```
     2. قم بتهيئة المستودع باستخدام Git:
        ```
        $ git init
        ```
     3. قم بإضافة الملفات:
        ```
        $ git add .
        ```
     4. قم بعمل "Commit" للتغييرات:
        ```
        $ git commit -m "First commit"
        ```
     5. اربط المستودع المحلي بمستودع GitHub:
        ```
        $ git remote add origin https://github.com/username/repository.git
        ```
     6. ادفع الملفات إلى GitHub:
        ```
        $ git push -u origin main
        ```

---

### **كيفية التعاون مع الآخرين على GitHub؟**

#### 1. **Fork (التفريع):**
   - إذا أردت تعديل مشروع شخص آخر، قم بـ **Fork** للمستودع. هذا سيمكنك من الحصول على نسخة خاصة بك للعمل عليها.
   
#### 2. **عمل التعديلات (Clone):**
   - يمكنك نسخ المشروع إلى جهازك باستخدام `git clone`:
     ```
     $ git clone https://github.com/username/repository.git
     ```

#### 3. **إرسال التعديلات (Pull Request):**
   - بعد عمل التعديلات على نسخة Fork الخاصة بك، يمكنك **إرسال Pull Request** للمستودع الأصلي ليتم دمج التعديلات.
   - سيقوم صاحب المستودع بمراجعة التعديلات وإذا كانت جيدة، سيقوم بدمجها.

---

### **أهم المميزات التي يقدمها GitHub:**
1. **التحكم في الإصدارات (Version Control):**
   - يمكنك تتبع جميع التغييرات في الكود والرجوع لأي نقطة في الماضي.

2. **التعاون مع الآخرين:**
   - يمكنك العمل مع فرق على نفس المشروع بسهولة من خلال **Pull Requests** و**Forks**.

3. **العمل مع الأوامر (Commands):**
   - يمكنك التحكم الكامل في المشروع باستخدام الأوامر عبر سطر الأوامر (Git Terminal) مع GitHub.

4. **التوثيق والمشاركة:**
   - يتيح لك GitHub نشر مستندات (Documentation) للمشاريع ومشاركتها مع الآخرين، مما يسهل على الآخرين فهم الكود والعمل عليه.

---

### **أمثلة عملية على GitHub:**

#### مثال 1: استنساخ (Clone) مشروع من GitHub:
- إذا كنت ترغب في العمل على مشروع موجود في GitHub، استخدم:
  ```
  $ git clone https://github.com/username/repository.git
  ```

#### مثال 2: رفع التعديلات:
- بعد إجراء التعديلات، يمكنك رفعها باستخدام:
  ```
  $ git push origin main
  ```

---

### **نصائح لاستخدام GitHub:**
1. **تعلم Git أولًا:**
   - GitHub يعتمد بشكل أساسي على Git. إذا تعلمت Git، ستتمكن من استخدام GitHub بسهولة.
   
2. **كن دائمًا حريصًا في كتابة رسائل commit:**
   - رسالة commit يجب أن تكون واضحة وموضحة للتغييرات التي أجريتها.

---
