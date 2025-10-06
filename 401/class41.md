# 401-Read_41

📱 React Native & Expo — Beginner Study Sheet
🧩 React Native Basics

1. Name three Core Components of React Native and describe what they do

React Native comes with core components — the basic building blocks of every app.
**View**

- Acts like a <div> in HTML.
- Used to structure and group UI elements.
- Helps control layout and styling.

**Text**

- Displays text content such as labels, titles, and paragraphs.
- Supports styling like bold, color, and font size.

**Image**

- Used to show pictures or icons.
- Can load local or remote images.

💡 **Insight:**
React Native swaps out web elements (like <div>, <p>, <img>) for native components that work on iOS and Android.

2. What problem does React Native solve (why call it native)?

- Developers used to build separate apps for iOS (Swift) and Android (Java/Kotlin).
- React Native allows you to write one set of JavaScript code that works on both.
- *It’s called “native” because your app uses the phone’s actual native components, not a web browser*.

💡 **In short:**
React Native bridges JavaScript with real device features — so your app looks and feels fully native.

3. What are the building blocks of a React Native app? How does that compare to a React app?

- React Native apps use native components (View, Text, Image).
- React (web) apps use HTML elements (div, span, img).

- **Feature**   **React (Web)**	    **React Native (Mobile)**
*UI elements*	HTML tags	        Native components
*Platform*	    Browser	            iOS / Android
*Styling CSS*   JavaScript-based    (StyleSheet API)

💡 Key idea:
React Native uses the same React logic, but renders to mobile UI elements instead of the web.

⚙️ **Expo**
1. What solution does Expo provide?

Expo makes building and testing React Native apps easier.

It includes tools for:
    - Instantly previewing your app on your phone.
    - Using device features (camera, GPS, notifications) without setup.
    - Publishing and sharing prototypes quickly.

💡 *Think of Expo as “training wheels” for React Native* — it handles the hard setup so you can focus on learning and coding.

2. Expo tries to manage as much of the complexity of building apps as possible, which is why we call it the managed workflow.

- The Managed Workflow = Expo manages all the complex native setup.
- You just code in JavaScript, and Expo builds the rest.

3. What is the difference between React Native and Expo?
| Feature               | React Native         | Expo                   |
| --------------------- | -------------------- | ---------------------- |
| Setup                 | Manual               | Easy & automatic       |
| Access to native code | Full access          | Limited (managed)      |
| Use case              | Complex, custom apps | Simple, quick projects |
| Control level         | Full control         | Managed by Expo        |


💡 **Analogy:**
React Native = manual car (more control, more work)
Expo = automatic car (easy to drive, less setup)

💻 **Expo Snack**
1. What does Snack allow you to do?

Expo Snack is an online playground for React Native.
Lets you:
    - Write and test React Native code in your browser.   
    - See live results instantly.
    - Scan a QR code to view the app on your phone.
    - Share your code via a link.

💡 Like CodePen, but for mobile apps.

🧨 **Ejecting**
1. What does “eject” mean within the context of Expo?

- Ejecting means leaving Expo’s managed setup.
- You gain access to the underlying native iOS and Android files.
- You’re now responsible for your own builds and configurations.

💡 *Like taking off the training wheels* — you get full control, but more responsibility.

2. When should you not eject?

Don’t eject if:
- Expo supports everything your app needs.
- You’re still learning or want simplicity.
- You don’t need native code access.

💡 Once you eject, *it’s hard to go back* — only do it when necessary.

3. Why might you choose to eject?

You might eject if you need:
    - Custom native features or libraries not supported by Expo.
    - Full control over the build and release process.
    - To integrate SDKs or advanced hardware features.

💡 Eject when your app grows beyond Expo’s limits.

✅ **Key Takeaways**

* React Native lets you build mobile apps with JavaScript and React logic.
* Expo simplifies the setup and testing process.
* Snack lets you experiment online.
* Ejecting gives you full power — but also full responsibility.