# TM Info — বাংলা সেটআপ গাইড

এটি responsive static website; কোনো build command বা Netlify AI credit লাগে না।

## প্রকাশ করার নিয়ম
1. ZIP extract করুন।
2. GitHub-এ নতুন repository তৈরি করুন।
3. extract করা ফোল্ডারের **ভেতরের সব ফাইল ও ফোল্ডার** repository-র root-এ upload করুন। `index.html` সরাসরি root-এ থাকবে; তার ভেতরে আরেকটি folder যেন না থাকে।
4. Commit changes করুন।
5. Netlify → Add new site / Import an existing project → GitHub repository নির্বাচন করুন।
6. Build command ফাঁকা রাখুন; Publish directory `.` বা repository root দিন। Deploy করুন।

## Admin panel
Admin URL: `https://YOUR-SITE.netlify.app/admin/`

Admin login/publish-এর জন্য Netlify Identity ও Git Gateway চালু করতে হবে:
1. Netlify dashboard → আপনার site → Identity (কিছু account/UI-তে Site configuration বা Integrations-এ থাকতে পারে) → Enable Identity।
2. Registration-এ Invite only দিন।
3. Identity → Invite users থেকে নিজের email invite করুন, invitation গ্রহণ করে password সেট করুন।
4. Identity / Services → Git Gateway → Enable Git Gateway।
5. `admin/config.yml`-এ branch `main`; আপনার GitHub default branch অন্য হলে সেটি বদলান।
6. deploy শেষ হলে `/admin/` খুলে login করুন। Website Articles থেকে লেখা যোগ/edit/delete করে Publish করুন।

গুরুত্বপূর্ণ: শুধু admin ফাইল থাকলেই login/publishing চালু হয় না। Netlify Identity ও Git Gateway feature আপনার account/site-এ available থাকতে হবে। না থাকলে GitHub-এ `content/articles.json` edit করে Commit changes করুন।

## ছবি
Admin Media upload-এ ছবি আপলোড করুন। Cover image path দিন `/assets/uploads/filename.jpg`। ফাইলের নাম ও বড়/ছোট হাতের অক্ষর মিলতে হবে।

## আর্টিকেল
`id` unique English slug (যেমন `my-first-post`) হবে। `title/titleBn`, `summary/summaryBn`, `body` পূরণ করুন। Body-তে Markdown headings (`## Heading`), paragraph ও bullet list ব্যবহার করা যায়।

যোগাযোগের `hello@tminfo.example` placeholder—নিজের email দিয়ে বদলাবেন।
