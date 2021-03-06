---
title: "বিশেষ বিজ্ঞপ্তি!"
date: 2021-05-01
author: Muhammad Mominul Huque
---

ওপেনবাংলা কিবোর্ড ২.০.০ সংস্করণ প্রকাশের মধ্য দিয়ে আমরা Bintray এর মাধ্যমে বিভিন্ন লিনাক্স ডিস্ট্রিবিউশনের জন্য প্যাকেজ বিতরণ করা শুরু করি। তবে পহেলা মে থেকে Bintray তাদের পরিষেবা গুটিয়ে নিচ্ছে।

<!--more-->

ফলশ্রুতিতে যেসব ব্যবহারকারীরা [ইন্সটল পেইজে অথবা রিড মি ফাইলে](https://github.com/OpenBangla/OpenBangla-Keyboard/blob/2.0.0/README.adoc#installation) বর্ণিত ধাপগুলো অনুসরণ করে ওপেনবাংলা কিবোর্ড ইন্সটল করেছিলেন তারা এররর এর সম্মুখীন হতে পারেন তাদের প্যাকেজ ম্যনেজারের তথ্য হালনাগাদের সময়। তাই ব্যবহারকারীদের নিম্নের ধাপ অনুসরণ করে তাদের প্যাকেজ ম্যানেজার থেকে ওপেনবাংলা কিবোর্ডের Bintray রেপোটি অপসারণ করতে হবে।

### ডেবিয়ান ও উবুন্টু ভিত্তিক ডিস্ট্রো
নিচের কমান্ডটি দিয়ে রিপজিটরিটি অপসারণ করে নিন:
```bash
$ sudo rm /etc/apt/sources.list.d/openbangla.list
```

### ফেদোরা ভিত্তিক ডিস্ট্রো
নিচের কমান্ডটি দিয়ে রিপজিটরিটি অপসারণ করে নিন:
```bash
$ sudo rm /etc/yum.repos.d/openbangla.repo
```

### আর্চলিনাক্স ভিত্তিক ডিস্ট্রো
নিচের কমান্ডটি দিয়ে রিপজিটরিটি অপসারণ করে নিন:
```bash
sudo sed -i.$(date +%s) -e '/\[openbangla\]/,+2d' /etc/pacman.conf
```
অথবা /etc/pacman.conf ফাইলের [openbangla] সেকশনটা রিমুভ করে নিন।
এ কমান্ডটি একটি `/etc/pacman.conf.$EPOCH_SECONDS` নামে ব্যাকআপ ফাইল তৈরি করে রাখবে যেখানে `$EPOCH_SECONDS` হচ্ছে কমান্ডটা চালানোর সময়কার ইউনিক্স টাইম।

#### নতুন ইন্সটলেশন পদ্ধতি?
আমরা আবার আগের মতোই একটা স্ক্রিপ্টের মাধ্যমে ওপেনবাংলা কিবোর্ড ইন্সটল করার পদ্ধতিতে ফিরে যাচ্ছি:
```bash
bash -c "$(wget -q https://raw.githubusercontent.com/OpenBangla/OpenBangla-Keyboard/master/tools/install.sh -O -)"
```
আর [রিলিজেস পেইজ](https://github.com/OpenBangla/OpenBangla-Keyboard/releases/tag/2.0.0) থেকে ডাউনলোড করে [ইন্সটল করা](https://github.com/OpenBangla/OpenBangla-Keyboard/wiki/Installing-OpenBangla-Keyboard) যাবেই বরাবরের মতোই!

তবে আমরা ডেবিয়ান ও উবুন্টুর অফিশিয়াল প্যাকেজ রিপজিটরিতে ওপেনবাংলা কিবোর্ডকে যুক্ত করার চেষ্টায় আছি। ওপেনবাংলা কিবোর্ড ইন্সটলেশনে ব্যবহারকারীদের স্বাচ্ছন্দ্য বৃদ্ধি করার ব্যপারে আমাদের সবসময় চেষ্টা থাকবে! তবে আমরা এই অসুবিধার জন্য আন্তরিকভাবে দুঃখিত।
