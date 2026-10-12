# English Tutor in Claude

[Русский](README_RU.md) · [Українська](README_UA.md)

A prompt that turns Claude into a personal English tutor with voice lessons, a level diagnostic, a study program, homework and calendar reminders. Setup takes about fifteen minutes and needs no technical skills. It works the same on iPhone and Android.

Author: Kostiantyn Petrenko, mobile developer working on AI-first workflows with Claude.

## What you get

The tutor first asks about your goal and schedule. Then it checks your level in five areas: grammar, sentence building, vocabulary, listening and pronunciation. After that it works out how much time you need to reach your goal and builds a program. Lessons are held by voice. It gives homework and checks it, puts lessons and homework time into your calendar, and remembers everything you have covered.

At first the tutor speaks your native language and mixes in simple English phrases. The share of English grows as you understand more.

## What you need

- A Claude account. Sign up at claude.ai.
- The Claude app on your phone, iPhone or Android. Voice lessons work best there.
- A calendar: your phone's calendar or Google Calendar.
- Google Drive. Strongly recommended: the tutor keeps your homework, student card and lesson log there by itself, and you can open them from any device. Without Drive you have to update the files by hand after every lesson.
- The prompt file english-tutor-prompt-en.md from this repository. The tutor still talks to you in your own language.

If a feature described here is missing for you, check the [Claude help center](https://support.claude.com) to see whether it is available on your plan.

## Step 1. Sign up

Open claude.ai in a browser and create an account. Then install the Claude app on your phone and sign in with the same account.

## Step 2. Create a project

A project is a folder that holds the tutor's settings. Every chat inside it follows the same rules.

1. On claude.ai, open Projects in the left sidebar.
2. Click New Project.
3. Name it, for example, English. The description can stay empty.

## Step 3. Paste the prompt into the project instructions

1. Open english-tutor-prompt-en.md and copy the whole text.
2. On the project page, click Set project instructions.
3. Paste the text and save.

The prompt has to go into the instructions. If you upload it as a file to the project knowledge, Claude treats it as reference material and may not follow it.

## Step 4. Connect Google Drive

The tutor keeps two records about you. The student card holds your questionnaire, level, program and weak points. The lesson log holds lesson notes and your vocabulary. After every lesson it also saves a homework file.

With Google Drive, all of this sits in one folder named English Tutor. The tutor creates it, updates the files and gives you a link to each homework. You do nothing by hand.

Connect Drive in Claude settings, in the connectors section. Connect Google Docs there as well, so the tutor can edit the files in place instead of recreating them. Doing it once on claude.ai is enough; it then works in the phone app too.

The tutor keeps records only in files you can open and read, never hidden in its memory. After every save it reads the file back, checks that the entry is there and gives you a link.

Without Drive, the tutor asks you to upload english-student-card.md and english-lesson-log.md from this repository to the project. It cannot write to project files, so after each lesson it gives you an updated file to upload in place of the old one.

## Step 5. Calendar

In the questionnaire the tutor asks when you want to have lessons and when you will do homework. Once you approve the program, it adds both to your calendar. The homework event contains the task list and a link to the homework file.

Either option works.

- Your phone's calendar: Apple Calendar on iPhone, the built-in calendar on Android. The Claude app will ask for calendar access; allow it. If you declined earlier, turn access on for the Claude app in your phone's settings.
- Google Calendar, connected in Claude settings under connectors, like Drive. If your Google account is added to your iPhone, these events also show up in Apple Calendar.

If the tutor cannot reach any calendar, it says so and gives you a schedule file to import manually.

## Step 6. First conversation

Open the project and start a new chat. Write something like:

Hi, I want to start learning English.

The tutor asks about your goal, timeline, schedule and the kind of English you need. Text is easiest for this part.

## Step 7. Diagnostic and voice lessons

The first lesson is always a diagnostic, about thirty to forty minutes. During it the tutor explains nothing and gives no correct answers; it only records. The review comes at the end.

Grammar is checked on screen: a task with four options appears as text, and you say the letter out loud.

Hold the diagnostic and all lessons by voice on your phone.

1. Open your project in the Claude app.
2. Start a new chat and turn on voice mode.
3. Say it's time to start the lesson.

Start a new chat in the same project for every lesson. The tutor reads your card and log at the start, so you never begin from scratch.

## Good to know

- The tutor cannot call you or start a lesson on its own. You open the chat at the scheduled time; the calendar event reminds you.
- It hears your pronunciation only through the speech transcript, not the audio itself. So it works on pronunciation through exercises and comparison with native recordings, and it cannot judge your accent precisely.
- The tutor cannot feel time passing. At the start of the lesson it sets a timer on your phone for the lesson length, and it ends the lesson only when you say so. When the timer rings or you want to finish, say end of lesson or that's all for today. It then sums up, gives homework and saves the records. A bare stop means stop the current task, not the lesson.
- In voice mode, downloadable files may not appear. That is why homework comes as a Google Drive link or as text in the chat.
- After the first two or three lessons, ask the tutor what it remembers about you and the last lesson. If it remembers nothing, open the English Tutor folder in Drive and check that the card and the log are there.
- You can change anything along the way: more lessons, shorter lessons, more English, a different topic. The tutor rebuilds the plan.
- If the tutor does something that bothers you, such as reading answer options aloud or praising you, tell it directly. It should stop for the rest of the chat.

## Troubleshooting

- The tutor behaves like regular Claude and does not ask the questionnaire. Check that the chat is inside the project and the prompt is in the project instructions.
- Lessons did not appear in the calendar. Check that the Claude app has access to your phone's calendar or that Google Calendar is connected, then ask the tutor to add the schedule again.
- No homework link. Check that Google Drive is connected and ask the tutor to save the homework again, or ask for it as text in the chat.
- Too much English to follow. Say so, and it switches back to your native language.

## License

[CC BY 4.0](LICENSE). You can use, change and share the prompt, including commercially, as long as you credit the author.
