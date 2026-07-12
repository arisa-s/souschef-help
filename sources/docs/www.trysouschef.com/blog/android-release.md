# Source: https://www.trysouschef.com/blog/android-release

# Android (devlog)

Souschef is now available for Android user on Google Play Store!

![author](https://www.trysouschef.com/_next/image?url=%2Farisashiraishi.png&w=96&q=75)

Arisa Shiraishi

published: 2/7/2025

![Android (devlog)](https://www.trysouschef.com/_next/image?url=https%3A%2F%2Fcdn.sanity.io%2Fimages%2F10y6s55e%2Fproduction%2Feceaa808ee03fd0f49be6bb11fda6ad06bef7b5b-370x439.jpg%3Fw%3D370%26h%3D439&w=750&q=75)

I’m super excited to announce that **Souschef is now available for Android users on the [Google Play Store](https://play.google.com/store/apps/details?id=com.souschef.app)!** Every feature from the iOS version has finally made its way to Android, making Souschef officially available across Web, iOS, and now Android!

This marks a huge milestone for me, and in today’s blog, I want to do something a little different. Instead of just announcing the release, I’ll share my thoughts on the **tech stack (aka React Native)** I chose and the **challenges** I faced in bringing Souschef to Android. Hope you enjoy it!

## From Web to Mobile App

Souschef originally started as a **portfolio project** called [**Recipe Thief**](https://www.recipe-thief.com/)—a web-based recipe organizer I built right after college to showcase my skills. The idea was simple: cut straight to the chase—no ads, no long backstories, just ingredients and instructions.

But here’s the twist: I built it to avoid endlessly scrolling through cluttered recipe websites, only to create a new kind of inconvenience—copy-pasting recipe URLs into my own web app felt like extra work. That’s when it hit me that I needed a mobile app—one where I could import recipes with a simple tap.

Luckily, in 2024, I had the chance to learn React Native on the job while developing an iOS-focused mobile app for my former employer. That experience gave me the confidence to take Souschef from a simple web tool to a true cross-platform app—one that runs on Web, iOS, and Android.

### React Native

I know some engineers are still skeptical about React Native, and I get it. But as a sole developer who wants to build and ship as fast as I can, —**build once, ship everywhere**—sounded perfect.

If you're considering React Native for your next mobile app project, start by listing your must-have features and checking the latest documentation to ensure they're supported.

For example, my top priority was **share intent**—a mechanism that allows other apps to send data to yours. Since my app needed a seamless way for users to import recipes, this feature was essential.

But what if React Native doesn’t support what you need? That was my situation in 2022 when share intent wasn’t officially supported (and still isn’t). I kept monitoring [discussions in the community](https://expo.canny.io/feature-requests/p/share-extension-ios-share-intent-android), and eventually, someone (👼) shared a custom solution—at that point, I had no excuse not to go with React Native!

Honestly, it still amazes me that without knowing native mobile languages, I was able to release an app on both iOS and Android. So far, I have no complaints! (Of course, if I run into unforeseen issues, like scaling problems, I’ll be sure to write another blog post. 😉)

## Why the Delay?

If React Native lets me share code between platforms, why did it take me a whole year to launch Souschef on Android after iOS?

**It's the Google’s “20 testers for 14 days” rule.**

To release an app on Google Play, you have to recruit **20 Android users** to test your app for **14 consecutive days**—which, frankly, felt impossible. Like who has 20 android friends? I procrastinated, and as a result, Souschef’s Android release got stuck on the back burner.

Eventually, I stumbled upon [**Testers Community**](https://www.testerscommunity.com/)—a community where developer test each other's app and give feedbacks. And It was perfect - they gave me the feedback I needed without the headache of finding 20 willing participants on my own.

## Key takeaway

![](https://cdn.sanity.io/images/10y6s55e/production/1608b97f2123a3134b902c81f46e6693b432985f-500x500.png)

We often think our challenges are unique, but if you’re struggling with something, chances are others are too—and sometimes, all it takes is reaching out and asking for help. I know this sounds like something a college student might say after a six-month internship, but ever since I started building on my own, I’ve lost touch with that mindset. This experience was a much-needed reminder for me, and if you’ve made it this far, I hope it serves as a reminder for you too.

## A Look Ahead

Now that Souschef is finally available on both iOS and Android, I’m excited to gather more feedback and continue improving the app to help home chefs have more fun and less frustration in the kitchen.

#### **Ready to give it a try?**

Download **Souschef** from the [Google Play Store](https://play.google.com/store/apps/details?id=com.souschef.app) today and let me know what you think!

Thank you for reading, happy cooking! (or coding!)

Follow us for updates!