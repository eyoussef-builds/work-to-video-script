<div dir="rtl">

# التثبيت وأول استخدام

[English](installation.md) · [الرئيسية](../README.ar.md)

انسخ **مجلد `skills/work-to-video-script` كاملًا**، مش `SKILL.md` لوحده. المهارة تستخدم مرجعين داخل المجلد. تحتاج مساعدًا ونموذجًا، والوصول للشغل المكتمل، ومكانًا خاصًا ومسموحًا لحفظ النتائج. الصور الجديدة تحتاج أداة تصوير متصفح أو تطبيق؛ لو مش موجودة، المهارة تحدد اللقطات الناقصة.

## الطريقة الأولى: اطلب من مساعد يقدر يثبّت ملفات

</div>

```text
ثبّت work-to-video-script من
https://github.com/eyoussef-builds/work-to-video-script/tree/main/skills/work-to-video-script
في مكان المهارات الشخصي الموثق للبرنامج، مع الحفاظ على المراجع ومجلد agents.
لو فيه نسخة موجودة، راجعها واحفظ التخصيصات المحلية قبل التحديث.
اقرأ SKILL.md واتأكد إن المرجعين موجودين.
```

<div dir="rtl">

لو المساعد ما يقدرش يحمّل ملفات، استخدم النسخ اليدوي. التثبيت مش إذن لفتح حسابات خاصة أو قراءة بيانات غير متعلقة بالمشروع.

## الطريقة الثانية: تحميل ونسخ يدوي

حمّل [المصدر ZIP](https://github.com/eyoussef-builds/work-to-video-script/archive/refs/heads/main.zip). في macOS افتحه بالنقر مرتين؛ في Windows استخدم Extract All. انسخ `skills/work-to-video-script` للمكان المناسب في الجدول. مجلدات النظام المخفية ممكن تحتاج إنشاء يدوي.

### macOS وLinux — مثال Codex

</div>

```sh
git clone https://github.com/eyoussef-builds/work-to-video-script.git
skill_destination="$HOME/.agents/skills/work-to-video-script"
if [ -e "$skill_destination" ]; then
  printf '%s\n' 'Already installed; review local changes before updating.'
  exit 1
fi
mkdir -p "$HOME/.agents/skills"
cp -R work-to-video-script/skills/work-to-video-script "$skill_destination"
```

<div dir="rtl">

### Windows PowerShell — مثال Codex

بعد فك الضغط، افتح PowerShell داخل مجلد المستودع:

</div>

```powershell
$skillDestination = Join-Path $HOME '.agents/skills/work-to-video-script'
if (Test-Path $skillDestination) { throw 'Already installed; review local changes before updating.' }
New-Item -ItemType Directory -Force (Split-Path $skillDestination) | Out-Null
Copy-Item -Recurse './skills/work-to-video-script' $skillDestination
```

<div dir="rtl">

غيّر مجلد الوجهة حسب المساعد. الرمز `~` يعني مجلد المستخدم؛ في Windows استخدم `$HOME` أو مستعرض الملفات. أوامر shell مش بتتنفذ في PowerShell من غير تعديل.

## طرق التثبيت حسب المساعد

اتراجعت الوثائق الرسمية يوم **2026-10-25**. المسارات الموثقة مش معناها إن المهارة اتجربت بالكامل في كل برنامج. التصوير والوصول للمحادثات حسب الأدوات المتاحة. كل مسار في الجدول هو المجلد الأب؛ ضع تحته `work-to-video-script/`.

| المساعد | المكان الشخصي | مكان المشروع أو البديل | التشغيل وفحص الظهور | المصدر الرسمي |
| --- | --- | --- | --- | --- |
| Codex | `~/.agents/skills/` | `.agents/skills/` | اطلب `$work-to-video-script` وافحص قائمة المهارات أو مصدر الملف | [Skills](https://learn.chatgpt.com/docs/build-skills) |
| Claude Code | `~/.claude/skills/` | `.claude/skills/` | `/work-to-video-script` وقائمة الأوامر | [Skills](https://code.claude.com/docs/en/skills) |
| OpenClaw | `~/.openclaw/skills/` | `skills/` داخل مساحة العمل | اطلب المهارة وافحص `openclaw skills list` | [Skills](https://docs.openclaw.ai/tools/skills) |
| Hermes Agent | `~/.hermes/skills/` | اضبط مجلد مهارات خارجي لو محتاج نطاق مشروع | اطلب تحميل المهارة وتحديد مصدرها | [Skills](https://hermes-agent.nousresearch.com/docs/user-guide/features/skills) |
| Cursor | `~/.cursor/skills/` أو `~/.agents/skills/` | `.cursor/skills/` أو `.agents/skills/` | اطلب من Agent استخدام الاسم وتحديد مصدره | [Skills](https://cursor.com/docs/skills) |
| Grok Bot | قراءة تعليمات صريحة في هذا الدليل | أتح المجلد والمرجعين داخل مساحة Bot | اطلب قراءة الملفات الثلاثة للمهمة؛ لا ندّعي تثبيتًا أصليًا أو مراقبة كلمات | [سياق Bot](https://cursor.com/docs/grok-bot) |
| OpenCode | `~/.config/opencode/skills/` | `.opencode/skills/` أو `.agents/skills/` | اطلب التحميل بأداة skill ومعرفة المصدر | [Skills](https://opencode.ai/docs/skills/) |
| GitHub Copilot | `~/.copilot/skills/` أو `~/.agents/skills/` | `.github/skills/` أو `.agents/skills/` | اطلب من وضع Agent تحميل المهارة؛ الإتاحة حسب البرنامج وإصداره | [Skills](https://docs.github.com/en/copilot/concepts/customizations/agent-skills) |
| Gemini CLI | `~/.gemini/skills/` أو `~/.agents/skills/` | `.gemini/skills/` أو `.agents/skills/` | `gemini skills list --all` ثم اطلب استخدامها | [Skills](https://geminicli.com/docs/cli/skills/) |
| Windsurf / Cascade / Devin Desktop | `~/.codeium/windsurf/skills/` أو `~/.config/devin/skills/` | `.devin/skills/` والمسار القديم `.windsurf/skills/` | اخترها من Cascade Skills أو @mention وافحص المصدر | [Cascade skills](https://docs.devin.ai/desktop/cascade/skills) |
| Cline | `~/.cline/skills/` | `.cline/skills/` | قائمة Skills ثم `/work-to-video-script` | [Skills](https://docs.cline.bot/customization/skills) |
| Roo Code | `~/.roo/skills/` | `.roo/skills/` | اطلب من Roo تحميل المهارة وتحديد الملف | [Skills](https://roocodeinc.github.io/Roo-Code/features/skills/) |
| Aider | قراءة التعليمات كسياق للقراءة فقط | أتح SKILL.md والمرجعين للمهمة | اطلب الخطوات صراحة، ورتب التصوير خارج Aider لو محتاج | [تعليمات القراءة فقط](https://aider.chat/docs/usage/conventions.html) |
| Amp | `~/.config/agents/skills/` أو `~/.agents/skills/` | `.agents/skills/` | `amp skills list` ثم اطلب إعادة تحميل المهارات في المحادثة | [Skills](https://ampcode.com/docs/customize/skills) |
| Goose | `~/.agents/skills/` | `.agents/skills/` | `goose skills list` أو `/skills work-to-video-script` | [دليل المهارات](https://github.com/aaif-goose/goose/blob/main/documentation/docs/guides/context-engineering/using-skills.md) |

في بديلَي قراءة التعليمات، اطلب:

</div>

```text
اقرأ SKILL.md وreferences/evidence-guide.md وreferences/deliverable-template.md
من مجلد work-to-video-script المرفق كتعليمات للمهمة دي.
الشغل المكتمل معتمد. اكتب حكايته، واجمع الصور الحقيقية، وخطط للديمو.
وضح حدود الوصول والتصوير، وقف قبل إنتاج الفيديو.
```

<div dir="rtl">

ما تضيفش المهارة للتعليمات العامة لمجرد تقليد الاختيار التلقائي. ممكن البرنامج يدعم طرقًا أصلية أخرى؛ الدليل مش بيؤكد عدم وجودها.

## أول استخدام وفحص الظهور

اطلب من المساعد تحديد المجلد وقراءة المهارة وتسمية المرجعين. لو مش موجودة، راجع تداخل المجلدات، وتفعيل المهارة، ومساحة العمل المختارة، وجدّد قائمة المهارات أو الجلسة حسب البرنامج. البيئة السحابية تحتاج الحزمة والأدلة داخل ملفاتها المتاحة؛ المهارات الشخصية المحلية مش بتنتقل تلقائيًا.

</div>

```text
تمام، الشغل خلص. استخدم work-to-video-script للمشروع الحالي.
احكي بلسان الشخصية واللغة اللي اعتمدتهم، ومع الكلام صور حقيقية وخطة ديمو واضحة.
حدد اللقطات الناقصة. ما تولدش صوت أو فيديو وما تنفذش الديمو الفعلي.
```

<div dir="rtl">

تقدر تضيف تفضيلات الشخصية واللغة والهوية البصرية في ملف محلي `references/local-profile.md`. الملف خاص وخارج النسخة العامة. اختيارك الحالي يتقدم على التفضيلات المحفوظة. ما تحطش فيه مفاتيح أو ربط حسابات أو بيانات عملاء.

## التحديث والإزالة

حمّل التحديث في مجلد منفصل، وقارن الملفات والمراجع، واحفظ نسخة من التخصيصات والملف المحلي، واستبدل الملفات المطلوبة فقط. راجع التعليمات الجديدة قبل اعتمادها. للإزالة احذف مجلد المهارة المثبت فقط وحدّث قائمة المهارات. حزم الأدلة منفصلة وتتحذف بقرار منك حسب سياسة الاحتفاظ.

## حدود التحقق

المراجعة تشمل بيانات المهارة، وروابط المراجع، ومحتوى الحزمة العامة، والوثائق، وحالات السلوك. اتكتبت التعليمات داخل Codex؛ مافيش ادعاء باختبار تشغيل في 15 برنامجًا أو ضمان إن «تمام» هتشغلها تلقائيًا في كل مرة. مافيش مثبّت تنفيذي أو برنامج جمع بيانات أو خدمة خلفية أو ربط حسابات جديد.

</div>
