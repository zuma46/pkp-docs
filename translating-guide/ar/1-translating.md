مقدمة
=====

نظام المجلات المفتوحة ونظام المؤتمرات المفتوحة هما نظامان متعددا اللغات، مما يسمح للمجلات والمؤتمرات بإدارة النشر بلغات متعددة. إن مشروع المعرفة العامة يهدف إلى دعم الترجمات باللغات الإنجليزية، الفرنسية، الإسبانية، والبرتغالية لكل من نظام المجلات المفتوحة ونظام المؤتمرات المفتوحة. فضلاً عن ذلك، المزيد من حزم الترجمات ولكلا النظامين قد أضيفت إليهما من قبل مساهمات المجتمع، ونحن نرحب بها في أي وقت.

كل النص الذي تراه في واجهة النظامين في في الواقع مستخلص عبر برامجيات خاصة تسترجع النصوص من ملفات متعددة بصيغة XML متخصصة بكل لغة. هذه الملفات يمكن أن تتواجد في مجلدات مسماة وفقاً لترميزات متوافقة مع التسميات القياسية لمنظمة ISO (حسب [قائمة ترميز اللغات](http://www.loc.gov/standards/iso639-2/php/code_list.php) متبوعة برمز من [قائمة رموز الدول](http://www.iso.org/iso/country_codes/iso_3166_code_lists/english_country_names_and_code_elements.htm))، فعلى سبيل المثال، `ar_IQ` يمثل الإنجليزية الأمريكية، و `pt_BR` يمثل البرتغالية البرازيلية. هذه الوثيقة ستخاطبكم بالعربية `ar_IQ`.

مجلدات اللغة هذه ستضم عادة ملفات بصيغة XML تحتوي قائمة من مفاتيح العبارات المكتوبة فيها: هذه المفاتيح وقيمها المقابلة تتعلق بقوالب ثابتة مستعملة في كتابة النصوص البرمجية للنظام نفسه. المجموعة أدناه من مفاتيح العبارات مستقاة من الملف `locale/ar_IQ/locale.xml`:

```
<message key="navigation.journalHelp">المساعدة</message>
<message key="navigation.home">الصفحة الرئيسية</message>
<message key="navigation.about">عن</message>
<message key="navigation.userHome">الرئيسية للمستخدم</message>
<message key="navigation.login">تسجيل الدخول</message>
<message key="navigation.register">التسجيل</message>
```

عندما يريد النظام عرض نص معين، عليه أولاً تحديد
اللغة التي عليه استعمالها. أول مكان يتحقق منه هو التعرف
اللغة المقرر لها أن تكون لغة الموقع إفتراضياً من قبل
المشرف. إذا كان المستخدم يتعامل حالياً مع مجلة معينة، فإن النظام
بدلاً من ذلك، يتحقق من اللغة التي قررها رئيس تحرير المجلة بمثابة
اللغة الافتراضية. وأخيراً، إذا تم تنصيب لغات متعددة، فإنه
يتحقق فيما لو أن المستخدم نفسه قد اختار لغة أخرى لتكون
بديلاً عن اللغة الإفتراضية. المزيد من المعلومات عن إدارة اللغات
يمكن العثور عليها في مقطع التحقق عن توفرية اللغة.

بمجرد معرفة النظام للغة التي عليه استعمالها للمستخدم، فإنه
يقبض على مفتاح العبارة من الملف العائد للغة المعنية:
أي، إذا تطلب الأمر عرض العبارة المقابلة للمفتاح
`message key="navigation.journalHelp"` من المثال أعلاه، وتبين له أن عليه
إظهارها بالعربية، فإنه سيبحث في الملف
`locale/ar_IQ/locale.xml` عن القيمة المقابلة لهذا المفتاح، والتي
في مثالنا ستكون "المساعدة". لو كان مفتاح العبارة غير موجود (إن كان ملف اللغة
مفتقداً لمفتاح معين، أو غير موجود في النظام من الأساس)،
فإنه سيعرض تسمية المفتاح نفسه محاطاً برموز مربعات مزدوجة:
كما في: `##navigation.journalHelp##`

إذا صادفك يوماً هذا النمط من العبارات في نظام المجلات المفتوحة أو نظام المؤتمرات المفتوحة، فاعلم
بأن الترجمة هنا غير مكتملة. يمكنك أخذ نظرة على المقطع الخاص بالترجمة
لتتعلم كيف يمكنك إكمالها.

التحقق عن توفرية اللغة
======================

يُنصح أولاً بالتحقق من وجود اللغة فعلياً لنسختك من
نظام المؤتمرات المفتوحة أو نظام المجلات المفتوحة. إن كانت اللغة التي تريدها
غير مدرجة، فعليك مراجعة موقعنا للتحقق من توافرها أصلاً.

فحص النظام بشأن اللغات المتاحة فيه
-----------------------------------

أول موضع للتحقق منه بشأن توفرية اللغة، هو
من التنصيب نفسه.

لكل من نظام المجلات المفتوحة ونظام المؤتمرات المفتوحة: إن كانت لديك صلاحيات المشرف،
سجل دخولك ثم اذهب إلى الصفحة الرئيسية للمستخدم، وانقر على رابط
<em>اللغات</em>، حيث سيأخذك هذا إلى صفحة إدارة اللغات على مستوى
الموقع. هذه الصفحة فيها مقطعان رئيسيان:

-   ضمن <em>إعدادات اللغة</em> ستشاهد قائمة منسدلة مخصصة
    للغتك الرئيسية: هذا يحدد اللغة الإفتراضية عبر عموم
    الموقع؛ حيث سيواجه المستخدمون تلك اللغة إفتراضياً،
    حتى يقوموا بتعديل لغتهم المفضلة على الصعيد الشخصي.\
    \
    كما أنك ستشاهد قائمة باللغات المدعومة، مع خانات اختيار
    محاذية لكل منها. اللغات المنتخبة ستكون متاحة للاستعمال من قبل
    كل المجلات المستضافة في الموقع، كما أنها ستظهر في قائمة
    اختيار اللغات على كل صفحة في الموقع (هذا يمكن تخطيه في صفحات
    معينة في النظام). إذا لم يتم تأشير أكثر من لغة ضمن التنصيب،
    فإن قائمة تبديل اللغات لن تظهر، وكذلك الإعدادات الموسعة الخاصة
    بها، هي الأخرى لن تكون متاحة للمجلات أو المؤتمرات.
-   عند صفحة إدارة اللغات، ستشاهد قائمة باللغات المنصبة،
    وكذلك قائمة أخرى باللغات الأخرى التي لم يتم تنصيبها.\
    \
    محاذياً لكل لغة منصبة، ستشاهد: رابطاً <em>إعادة تحميل اللغة</em>،
    وهو مفيد إذا سبق لك إجراء تعديلات على ملفات تلك اللغة،
    كما أن هناك رابط <em>إلغاء تنصيب اللغة</em>، والذي لن يزيلها
    من التنصيب الحالي لنظامك، بل سيرفعها من قائمة اللغات
    المدعومة والمتاحة لمجلاتك أو مؤتمراتك.\
    \
    عند أسفل النافذة، وجوار كل لغة لم يتم تنصيبها بعد،
    ستشاهد خانة اختيار. لتنصيب تلك اللغة، فقط أشر على الخانة
    المحاذية لاسمها، ثم انقر <em>تنصيب</em>. سيتم تنشيط الصفحة
    واللغة المعنية ستظهر ضمن <em>إدارة اللغات</em>.\
    \
    إذا كانت اللغة منصبة من قبل المشرف عبر صفحة
    <em>اللغات</em>، فعليك أيضاً إتاحتها لمجلاتك
    أو مؤتمراتك من أجل أن تكون ظاهرة أمام المستخدمين.
    سجل دخولة بصفة رئيس التحرير أو المشرف على المؤتمر،
    وعبر صفحتك الرئيسية أنقر على <em>اللغات</em> لتذهب
    إلى صفحة إدارتها ضمن المجلة - أو المؤتمر -.
    هنا يمكنك تعيين اللغة الافتراضية لمجلتك
    أو مؤتمرك، وعلى نفس الغرار، تمكين اللغات المدعومة
    لأن تكون متاحة للمجلات - المؤتمرات - في عموم الموقع. إذا قمت بتمكين
    أكثر من لغة واحدة، سيكون بإمكان المستخدمين التنقل بينها عبر قائمة
    منسدلة تظهر في الشريط الجانبي.

التحقق من توافر اللغات في موقع مشروع المعرفة العامة
---------------------------------------------------

إن مشروع المعرفة العامة يحتفظ بقائمة محدثة من اللغات والمساهمين بها
ضمن صفحة خاصة في موقع المشروع.

-   [قائمة لغات نظام المجلات المفتوحة](http://pkp.sfu.ca/ojs-languages)

-   [قائمة لغات نظام المؤتمرات المفتوحة](http://pkp.sfu.ca/ocs-languages)

المعلومات منظمة في جدول، مع رقم نسخة البرنامج في
المحور الأفقي مع قائمة اللغات في المحور الصادي. النقر
على اسم اللغة سيأخذك إلى صفحتها، حيث يعرض أسماء آخر
المساهمين، مع أي معلومات ذات صلة.

جميع اللغات تقع ضمن الأصناف الآتية:

-   **مكتملة:** سواءً مضمنة في تلك النسخة بعينها من نظام المؤتمرات المفتوحة أو
    نظام المجلات المفتوحة، أو بخلاف ذلك، جاهزة للتنزيل من القائمة.

-   **بحاجة إلى تحديث:** هذه الملفات مضمنة في النسخة التي تستعملها
    (الجدول سيشير إلى ذلك) لكنها غير مكتملة لسبب ما
    (قد تكون نسخة متقادمة لكنها لا تزال تعتبر مؤدية لعملها؛ أو
    قد تكون منقوصة عن نسبة 100% في المقام الأول). 
    إذا كانت مدرجة على أنها غير مضمنة في نسخة النظام
    الذي تستعمله، يمكنك مراسلة آخر من يتولى إدامتها
    من المترجمين لمعرفة فيما لو كانت لديهم أي ملفات حديثة.

إذا لم تشاهد اللغة/اللغات التي تتطلع إليها مدرجة في
كلا القائمتين، لطفاً، نتطلع إلى أن تنهض بمهمة الترجمة بنفسك.
إذا كنت مهمتماً بمساهمة من هذا النوع، [راسلنا]
(http://pkp.sfu.ca/contact) للنصيحة، أو استعن بما تجده
في هذه الوثيقة.

تنصيب اللغة
============

حزم اللغات تتوفر بشكل ملفات بصيغة tar.gz، ويمكن تنصيبها
عبر اتباع الخطوات الآتية (ستحتاج إلى برنامج مثل
7-Zip لفك ضغط الحزمة):

-   ضع الأرشيف في منبع ملفات نظام المجلات المفتوحة أو نظام المؤتمرات المفتوحة ضمن الملقم:
    هذا من شأنه وضع ملفات الترجمة لتلك اللغة في المجلدات الصحيحة.
-   أضف إدخالاً جديداً في الملف `registry/locales.xml` مستعملاً الصيغة الآنية:

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE locales SYSTEM "../dbscripts/xml/dtd/locales.dtd">
<locales>
    <locale key="de_DE" name="Deutsch (Deutschland)"/>
    <locale key="ar_IQ" name="English"/>
    <locale key="es_ES" name="Español (España)"/>
    <locale key="fr_CA" name="Français (Canada)"/>
    (... and so on)
</locales>
```

-   سجل دخولك إلى النظام بصلاحيات المشرف، ثم اذهب إلى صفحة اللغات؛
-   ضع تأشرة في خانة التأشير المجاورة للغة المضافة تحت باب
    اللغات المنصبة حديثاً، ثم انقر <em>تنصيب</em>;
-   بعد إعادة تحميل الصفحة، ضع تأشيرة في خانة التأشير المجاورة
    للغة المنصبة تواً ضمن باب اللغات المدعومة، ثم انقر
    <em>حفظ</em>.

عند ذلك، قد يتطلب الأمر أن تستعرض كل مؤتمر أو مجلة لديك صلاحية
إدارتها، لتفعيل اللغة هناك عبر صفحة إدارة اللغات في
المؤتمر/المجلة. يمكنك القيام بهذا عبر تأشير خانة التأشير المحاذية
للغات المدعومة، ومن ثم النقر على <em>حفظ</em>.

**تحذير:** قم بزيارة صفحة معلومات النظام لديك
(http://<your-site>/index.php/index/admin/systemInfo) وقم بمراجعة المتغير
"registry\_dir" للتأكد من كونك تعدل ملف locales.xml الصحيح


مدراء الترجمات
===============

يعتبر المساهمون بتقديم حزم الترجمات الجاهزة إلى مشروع المعرفة العامة
قد أخذوا على عاتقهم مهمة إدامة الترجمات التي قدموها للمشروع
ولذلك فهم المرجع الأول لنا عندما تطرأ تحديثات هامة أو كثيرة
على التطبيقات المعنية. بلا شك، بماأن عملهم قائم على أساس تطوعي،
فقد يصدف أن يعتذر البعض منهم عن إدامة نسخته من الترجمة، مما يضطرنا
إلى قبول مساهمات الآخرين لاحقاً، حرصاً منا على تقديم التطبيقات
إلى أكبر طيف من الجمهور المشتغل بالتعليم أو البحث العلمي.


الترجمات حسب التطبيق
====================

ستجد معلومات إضافية عن الترجمات، بضمنها المساهمين
وملاحظات الترجمة، أدناه. نحث المساهمين على [مراساتنا]
(mailto:pkp.contact@gmail.com) للحصول على حسابات الدخول من أجل
إدامة صفحات الترجمة الخاصة بهم.