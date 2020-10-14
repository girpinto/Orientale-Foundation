# Orientale Foundation
This repository is intended to support Orientale Foundation' students. Here you'll find some tips and examples to complete your tasks with the new framework SwiftUI. In this repository you'll find some tips and tricks to go forward on your projects. As I always say to pepople who approach for the very first time to code, don't worry about syntax and grammar in code. Coding it's like to learn a new language and you're Orientale' students, so for you should be easy learning a new language. I just hope to give you a real support in this awesome journey and this is why I created this repository. I should give you just some recommendations : 

1. Don't use this repository as a guide, it's not intended to be that 
2. Don't just copy/paste code that is wrote here, I know that you'll act in this way, but if you can try to understand what's happening
3. I'll try to explain every single line of code, but forgive me if I won't so accurate, theory is boring sometimes (I'm joking....maybe)
4. Don't forget to swear and to say bad words during coding session, it helps a lot

# SwiftUI
Ok, I hate this part, because it's the boring part, but I have to write it. For your challenge you're using the beautiful framework for Xcode **SwiftUI**, it won't be easy, I know, but let's make small steps. First, some history of the framework. 

## History
> SwiftUI is an innovative, exceptionally simple way to build user interfaces across all Apple platforms with the power of Swift. 
>    
> — Apple 

SwiftUI was introduced in 2019, after years of *Objective-C* and *Swift*, Apple came to conclusione that ***less is more***. As may you've noticed, coding it's not easy and you should be very accurate if you want to display something on your devices. Before SwiftUI, frameworks that allowed developers to create User Interfaces in their apps were **UIKit** and **AppKit**. Now thanks to this fresh and new paradigm you'll be able to create User Interfaces in an easier way and with less effort. 

If you think that Swift (languange who developers uses to work with Apple devices) was announced in 2014, you can easily undestand that programming is a constantly evolving discipline. This is why I think that programming, and in particular coding, should be studied from elementary school. Anyway, let's start with funny part.

## Why SwiftUI?
Developer community has been always be divided between using storyboards or using programmatic UI. Now SwiftUI looks easy enough for a beginner to grasp and yet offers the maintainability of a coded UI. So the best of both worlds, right? Obviously we have to say that's up to developers to choose which programming language learn. Since your challenge is about SwiftUI you have no choice. Smile! 😊 

But I can say to you a thing starting with this framework will help you to understand what's behind the application you use everyday (such as Instagram or TikTok) and trust me at the end of this experience you'll be able to create your personal projects on your own.  

## What the hell is that? 
Before you dive into creating your views, there's a little vocabulary you must learn. First, you should know that SwiftUI it's a **declarative** framework: it means that you declare how you want the UI to look, and SwiftUI converts your declarations into efficient code that gets the job done. Apple and me encourage you to create as many views as you need to keep your code easy to read. Reusable parameterized views are especially recommended, in this way you can use multiple times yours algorithms.

## Vocabulary 
- **Canvas and Minimap** : First is intended to preview your app's views and it's alongside the code editor. Second is a real **minimap** of your code, it allows you to see all your code and you can hide it in Xcode by clicking on **Editor -> Hide Minimap**.
- **Container Views** : *Container View* fetches data and passes it to a *Rendering View* or another *Container View*. Container View doesn’t present any User Interface itself. It is just managing data-flow and passes the data to the Rendering View. A Container View should do things only related to data-flow:
    1. Store the state of the Rendering View
    2. Fetch data using ObservableObject
    3. Handle life cycle (onAppear/onDisappear)
    4. Provide action handlers to the Rendering View
- **Rendering View** : Build User Interface using primitive components provided by SwiftUI and compose it by using other Rendering views. Use data as input to render User Interface and don’t store any state. 
- **Stack Views** : **Stacks** in SwiftUI are similar to the stack views in **UIKit**. By combining views in *horizontal* (HStack) and *vertical* (VStack) stacks, you can construct complex user interfaces for your apps.
- **@State variables** : It's the new keyword introduced with SwiftUI. To understand it read at this : *When the state updates, the view invalidates its appearance and updates itself* (Martin Lasek, SwiftUI - Understanding State). It basically means our View which is our body variable will be re-rendered as soon as we are changing a variable that has **@State** as a keyword in front of it.

## How it will be? 
Now, the besta part: how it will work this repository? Well this repository was my personal repository to store all my shitty code I made during my free time. I wanna ensure you that now it was clenaned up and it was improved just for you guys. I deserve an applause. 👏 

Jokes besides, this repository will be open for you guys as well as you need it. In here you'll find some projects that you can use and don't worry they are free of charge, fuck to copyright. But remember guys these projects are not apps and they can't compose an app, they are just some tips on how to show some UI on your apps. So as I said before don't copy/paste these chuncks of code, they're useless alone and they work bad together. I'll try to comment as much as possible, even if swift developers hate this part because they say that Swift is in natural language and it can be understood also by a child. Well coders, fuck you I need explanations. 

So Foundation' students I just have to wish you good luck for all your projects and I can't wait to see your work in action. Cheers 🍻 !!

# License
[MIT](https://choosealicense.com/licenses/mit/)

###### Author 
Girolamo Pinto
