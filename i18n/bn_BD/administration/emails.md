# ইমেইল

> গুরুবপূর্ণ। [Cron](https://github.com/espocrm/documentation/blob/master/administration/server-configuration.md#setup-a-crontab) ইমেইলে আনলিমিটেড কাজের জন্য আপনার সিস্টেমে কনফিগার করা উচিত। আপনি আপনার EspoCRM এ তথ্য পেতে পারেন Administration > Scheduled Jobs এ।

## সংক্ষিপ্ত বিবরণ

EspoCRM এর IMAP মেইলবক্সগুলি নিরীক্ষণ করার একটি ক্ষমতা রয়েছে। ইমেল দুটি উপায়ে সংরক্ষণ করা যায়: গোষ্ঠী ইমেইল অ্যাকাউন্টগুলি এবং ব্যক্তিগত ইমেইল অ্যাকাউন্টগুলি। গোষ্ঠী ইনবাউন্ড অ্যাকাউন্টগুলি গোষ্ঠী মেলবক্সের জন্য নির্ধারিত: সর্বাধিক সাধারণ ক্ষেত্রে একটি সমর্থন বাক্স। ব্যক্তিগত ইমেইল অ্যাকাউন্টগুলি ব্যবহারকারীদের ব্যক্তিগত মেইলবক্সগুলির জন্য নির্ধারিত।

একটি ইমেল আসছে যখন সিস্টেমটি যথাযথ রেকর্ডের সাথে লিঙ্ক করার চেষ্টা করে (অ্যাকাউন্ট, লিড, সুযোগ, কেস)। ব্যবহারকারীরা যে রেকর্ড অনুসরণ করে তারা সিস্টেমে একটি নতুন ইমেইল সম্পর্কে বিজ্ঞপ্তি পাবেন, এমনকি যদি তারা TO বা CC তে না থাকে

## গ্রুপ ইমেইল অ্যাকাউন্টসমুহ

শুধুমাত্র অ্যাডমিনিস্ট্রেটর গ্রুপ ইমেল অ্যাকাউন্ট স্থাপন করতে পারেন। গোষ্ঠী ইমেল অ্যাকাউন্টগুলি ইমেল গ্রহণ ও প্রেরণের জন্য উভয়ই ব্যবহার করা যেতে পারে। গ্রুপ অ্যাকাউন্ট থেকে ইমেল পাঠানো 4.9.0 সংস্করণ থেকে উপলব্ধ করা হয়েছে।

টিমের ক্ষেত্র নির্ধারণ করে যে কোন দলগুলিকে ই-মেইল হিসেবে নিয়োগ করা হবে।

যদি গ্রুপের ইমেইল একাউন্টে SMTP থাকে এবং এটি ভাগ করে নেওয়া হিসাবে পরীক্ষা করা হয় তাহলে একটি অ্যাক্সেস গ্রুপ ইমেল অ্যাকাউন্টের অনুমতির মাধ্যমে ভূমিকা দ্বারা নিয়ন্ত্রিত হবে। টিম ক্ষেত্র ব্যবহার করা হবে যদি অনুমতি স্তর 'Team' হিসাবে সেট করা হয়

সিস্টেমে ইনকামিং ইমেলগুলি জন্য একটি স্বয়ংক্রিয় উত্তর পাঠাতে একটি ক্ষমতা আছে।

## Email-to-Case

সিস্টেমটি আগত গোষ্ঠী ইমেলগুলি থেকে কেস তৈরি করার একটি বিকল্প আছে।
এই বৈশিষ্ট্য সমর্থন দল জন্য উদ্দেশ্যে করা হয়
এই পদ্ধতি অনুযায়ী নির্দিষ্ট দল থেকে ব্যবহারকারীদের ক্ষেত্রে বিতরণ করা যায়:
`direct assignment`, `round-robin` এবং `less-busy`. 
থ্রেডে শুধুমাত্র প্রথম ইমেল একটি নতুন কেস তৈরি করে।
প্রতি পরবর্তী একটি বিদ্যমান ক্ষেত্রে রেকর্ডের সাথে সংযুক্ত হবে এবং তার স্ট্রিম প্যানেলে প্রদর্শিত হবে।

যখন ব্যবহারকারীরা গ্রাহকের কাছে একটি উত্তর পাঠাতে চান তখন তাদের নিশ্চিত করতে হবে যে এই মামলাটিকে ইমেলের একটি পিতা বা মাতা হিসেবে নির্বাচিত করা হয়েছে যা পাঠানো হচ্ছে। এটি ব্যবহারকারীর নিজের পরিবর্তে গ্রাহকের ইমেইল অ্যাড্রেস এর ঠিকানা সরবরাহ করবে।

## ব্যক্তিগত ইমেল অ্যাকাউন্টসমুহ

ব্যবহারকারীরা তাদের নিজস্ব ইমেল অ্যাকাউন্টগুলি সেট আপ করতে পারেন যা নিরীক্ষণ করা প্রয়োজন। Emails > Top Right Dropdown Menu > Personal Email Accounts. অ্যাডমিনিস্ট্রেটর ব্যবহারকারীদের ইমেল অ্যাকাউন্টগুলি পরিচালনা করতে পারেন।

## ইমেল ফিল্টারসমুহ

এই নির্দিষ্ট মানদণ্ড অনুযায়ী আগত ইমেলগুলির ফিল্টারের অনুমতি দেয়। উদাহরণস্বরূপ যদি আপনি EspoCRM এ আমদানি করার জন্য কিছু অ্যাপ্লিকেশন দ্বারা পাঠানো বিজ্ঞপ্তি বার্তাগুলি না চান তবে EspoCRM তাদের তৈরি করতে ফিল্টার তৈরি করতে পারেন।

অ্যাডমিন সমস্ত ইমেইল অ্যাকাউন্টে প্রয়োগ করা গ্লোবাল ফিল্টার তৈরি করতে পারে। ব্যবহারকারীরা নিজের ব্যক্তিগত ইমেইল একাউন্ট এবং সমগ্র ইনবক্সের জন্য ফিল্টারগুলি তৈরি করতে পারে।