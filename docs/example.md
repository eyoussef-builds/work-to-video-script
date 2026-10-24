# A fictional first-use example / مثال خيالي

This example is invented to explain the output. **It is not a real build report, screenshot or test result.**

المثال ده خيالي لشرح طريقة التسليم، وليس تقرير بناء حقيقيًا أو صورة لمنتج فعلي.

## Input situation

A developer finishes a fictional “Task Garden” task-list feature. The available material consists of a local test log and one current screenshot. There is no deployment receipt or historical screen recording.

The user says: “All good. Write the story in my assistant's voice with real screenshots and a demo plan. Do not make the video.”

## Appropriate story treatment

| Scene | Example narration | Visual / evidence treatment |
| --- | --- | --- |
| Problem | “Finding the next task meant opening three different lists.” | Paraphrase the supplied motivation; do not invent a quote |
| Build | “We put the next action in one place.” | Use the genuine available current screenshot, identified as current |
| Verification | “The local checks passed.” | Link the supplied test log privately; do not say it was deployed |
| Demo | “Add a task, mark it complete, then reload.” | Plan the steps and visible checkpoints; record later only when authorized |

A screenshot of the pre-build state is missing. The skill lists that gap rather than generating a fake “before” interface. A diagram may explain the difference if it is clearly labeled illustrative.

## Example private output layout

```text
private-story-output/
├── script.md
├── evidence.md
├── demo-plan.md
└── screenshots/
    ├── index.md
    └── S01-current-tasks-safe.png
```

The image filename above describes an example output, not an image shipped in this repository. Actual image files must come from the user's genuine project captures.

## Example planned demo

| Step | Action | Visible checkpoint | Side effect |
| --- | --- | --- | --- |
| 1 | Open the fictional local test instance | Empty task list | Read-only navigation |
| 2 | Add “Prepare the demo” | Task appears | Local test write; pending execution |
| 3 | Mark it complete and reload | Completed state remains | Local test write; pending execution |
| 4 | Remove the disposable test item | Initial state restored | Owned test cleanup; pending execution |

The draft stops here. It does not claim the planned demo was recorded, run or published.

<div dir="rtl">

## الفكرة بالعربي

المساعد يكتب حكاية الميزة، ويستخدم الصورة الفعلية المتاحة باعتبارها لقطة حالية، ويربط نجاح الاختبارات بسجلها. ما يقولش إن التطبيق اتنشر من غير دليل نشر، وما يختلقش صورة «قبل» أو تسجيلًا قديمًا. خطة الديمو توضح الإضافة والإكمال وإعادة التحميل والتنظيف، وتفضل خطة لحد التنفيذ المصرح به.

</div>
