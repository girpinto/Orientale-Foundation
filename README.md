# Foundation
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
- **var** : It's the keyword to identify a variable in Swift and obviously SwiftUI. Its value can change and you can set it as you want.
- **let** : It's similar to **var** keyword but its value is constant and can't change. 
- **class** : In the real world, you'll often find many individual objects all of the same kind. There may be thousands of other cars in existence, all of the same make and model. Each car was built from the same set of blueprints and therefore contains the same components. In object-oriented terms, we say that your car is an instance of the class of objects known as cars. A class is the blueprint from which individual objects are created. Inside a class you can define its properties and methods (functions that helps class to do something).
- **struct** : In simple terms, a struct is like a custom data type which provides storage of data using properties with extended functionality using methods.
- **enum** : An *enumeration* defines a common type for a group of related values and enables you to work with those values in a type-safe way within your code. If you are familiar with C, you will know that C enumerations assign related names to a set of integer values. Enumerations in Swift/SwiftUI are much more flexible, and don’t have to provide a value for each case of the enumeration. If a value (known as a raw value) is provided for each enumeration case, the value can be a string, a character, or a value of any integer or floating-point type.
- **Framework** : In computer science and specifically in software development, it is a supporting logical architecture (often a logical implementation of a particular design pattern) on which a software can be designed and built, often facilitating its development by the programmer.
- **Design Pattern** : Design pattern (architectural scheme), in computer science and especially in software engineering, is a concept that can be defined as "a general design solution to a recurring problem". It is a description or logical model to be applied for solving a problem that can arise in different situations during the software design and development phases, even before the definition of the solution algorithm.

## Doubts? 
Many of you talked about their doubts during coding office hours. One doubt that hit me was the difference between a class and a struct. Well first read at Apple Developer Documentation : 

> Classes and structures are general-purpose, flexible constructs that become the building blocks of your program’s code. You define properties and methods to add functionality to your classes and structures by using exactly the same syntax as for constants, variables, and functions.
>
> — Apple Documentation

Got it? No? Well while classes are used to define a blueprint for an object that we want to abstract from the reality, structures are used to store some data that we need. We can define variables and methods in both constructs. So why in SwiftUI we use structures and not classes? I would answer because Mom Apple decided in this way, but there's a deeper reason.

## Because....
First, there is an element of performance: structs are simpler and faster than classes. I say an element of performance because lots of people think this is the primary reason SwiftUI uses structs, when really it’s just one part of the bigger picture.

In UIKit, every view descended from a class called UIView that had many properties and methods – a background color, constraints that determined how it was positioned, a layer for rendering its contents into, and more. There were lots of these, and every UIView and UIView subclass had to have them, because that’s how inheritance works.

Often this wasn’t a problem, but there was a particular subclass called UIStackView, which is analogous to VStack and HStack in SwiftUI. In UIKit, UIStackView was a non-rendering view type designed to make layout easier, but it meant that even though it had a background color thanks to inheritance, that background color never actually got used.

In SwiftUI, all our views are trivial structs and are almost free to create. Think about it: if you make a struct that holds a single integer, the entire size of your struct is… that one integer. Nothing else. No surprise extra values inherited from parent classes, or grandparent classes, or great-grandparent classes, etc – they contain exactly what you can see and nothing more.

## How it will be? 
Now, the best part: how it will work this repository? Well this repository was my personal repository to store all my shitty code I made during my free time. I wanna ensure you that now it was clenaned up and it was improved just for you guys. I deserve an applause. 👏 

Jokes besides, this repository will be open for you guys as well as you need it. In here you'll find some projects that you can use and don't worry they are free of charge, fuck to copyright. But remember guys these projects are not apps and they can't compose an app, they are just some tips on how to show some UI on your apps. So as I said before don't copy/paste these chuncks of code, they're useless alone and they work bad together. I'll try to comment as much as possible, even if swift developers hate this part because they say that Swift is in natural language and it can be understood also by a child. Well coders, fuck you I need explanations. 

So Foundation' students I just have to wish you good luck for all your projects and I can't wait to see your work in action. Cheers 🍻 !!

## Some "keywords" to keep in mind
- **self** : In Swift/SwiftUI *self* is a special property of an instance that holds the instance itself. Most of the times *self* appears in an initializer or method of a class, structure or enumeration.
- **@State** : A *State* instance isn’t the value itself; it’s a means of reading and writing the value. To access a state’s underlying value, use its variable name, which returns the *wrappedValue* property value. You should only access a state property from inside the view’s body, or from methods called by it. For this reason, declare your state properties as private, to prevent clients of your view from accessing them. It is safe to mutate state properties from any thread.
To pass a state property to another view in the view hierarchy, use the variable name with the **$** prefix operator. This retrieves a binding of the state property from its projectedValue property. For example, in the following code example **PlayerView** passes its state property **isPlaying** to **PlayButton** using **$isPlaying**:
```swift
struct PlayerView: View {
    var episode: Episode
    @State private var isPlaying: Bool = false

    var body: some View {
        VStack {
            Text(episode.title)
            Text(episode.showTitle)
            PlayButton(isPlaying: $isPlaying)
        }
    }
}
```
- **$** : The *$* is used in conjunction with property delegates. It's not an **operator**, but a **prefix**.
- **Binding** : Use a binding to create a two-way connection between a property that stores data, and a view that displays and changes the data. A binding connects a property to a source of truth stored elsewhere, instead of storing data directly. For example, a button that toggles between play and pause can create a binding to a property of its parent view using the Binding property wrapper.
```swift
struct PlayButton: View {
    @Binding var isPlaying: Bool

    var body: some View {
        Button(action: {
            self.isPlaying.toggle()
        }) {
            Image(systemName: isPlaying ? "pause.circle" : "play.circle")
        }
    }
}

```
The parent view declares a property to hold the playing state, using the **State** property wrapper to indicate that this property is the value’s source of truth.
```swift
struct PlayerView: View {
    var episode: Episode
    @State private var isPlaying: Bool = false

    var body: some View {
        VStack {
            Text(episode.title)
            Text(episode.showTitle)
            PlayButton(isPlaying: $isPlaying)
        }
    }
}
```
When PlayerView initializes PlayButton, it passes a binding of its state property into the button’s binding property. Applying the *$* prefix to a property wrapped value returns its **projectedValue**, which for a state property wrapper returns a binding to the value.
Whenever the user taps the *PlayButton*, the *PlayerView* updates its *isPlaying* state.
- **@ObservableObject** : When using observed objects there are three key things we need to work with: the **ObservableObject** protocol is used with some sort of class that can store data, the **@ObservedObject** property wrapper is used inside a view to store an observable object instance, and the **@Published** property wrapper is added to any properties inside an observed object that should cause views to update when they change.

Tip: It is really important that you use **@ObservedObject** only with views that were passed in from elsewhere. You should not use this property wrapper to create the initial instance of an observable object – that’s what **@StateObject** is for.

As an example, here’s a UserProgress class that conforms to ObservableObject:
```swift
class UserProgress: ObservableObject {
    @Published var score = 0
}
```
I know that doesn’t look like much code, but that’s because SwiftUI is doing a remarkable amount on our behalf! There are two things that matter in there:

1. The **ObservableObject** conformance allows instances of this class to be used inside views, so that when important changes happen the view will reload.
2. The **@Published** property wrapper tells SwiftUI that changes to score should trigger view reloads.
    
We can use that UserProgress class with code like this:
```swift
class UserProgress: ObservableObject {
    @Published var score = 0
}

struct InnerView: View {
    @ObservedObject var progress: UserProgress

    var body: some View {
        Button("Increase Score") {
            progress.score += 1
        }
    }
}

struct ContentView: View {
    @StateObject var progress = UserProgress()

    var body: some View {
        VStack {
            Text("Your score is \(progress.score)")
            InnerView(progress: progress)
        }
    }
}
```
As you can see, other than using the **@ObservedObject** property wrapper with progress, everything else more or less looks the same – SwiftUI takes care of all the implementation details for us.

There is one important difference, though: the progress property isn’t declared as private. This is because bound objects can be used by more than one view, so it’s common to share it openly.

Remember, please do not use **@ObservedObject** to create instances of your object. If that’s what you want to do, use **@StateObject** instead.

## @EnvironmentObject
SwiftUI’s **@EnvironmentObject** property wrapper lets us create views that rely on shared data, often across an entire SwiftUI app. For example, if you create a user that will be shared across many parts of your app, you should use **@EnvironmentObject**.

For example, we might have an **Order** class like this one:
```swift
class Order: ObservableObject {
    @Published var items = [String]()
}
```
That conforms to **ObservableObject**, which means we can use it with either **@ObservedObject** or **@EnvironmentObject**. In this instance, we might create a view that uses it with **@EnvironmentObject**, like this:
```swift
struct ContentView: View {
    @EnvironmentObject var order: Order

    var body: some View {
        // your code here
    }
}
```
Notice how the order property isn’t given a default value – by using **@EnvironmentObject** we’re saying that value will be provided by the SwiftUI environment rather than explicitly created by this view.

**@EnvironmentObject** has a lot in common with @ObservedObject: both must refer to a class that conforms to **ObservableObject**, both can be shared across many views, and both will update any views that are watching when significant changes happen. However, **@EnvironmentObject** specifically means “this object will be provided from some outside entity, rather than being created by the current view or specifically passed in.

In practical terms, imagine if you had view A, and view A had some data that view E wanted. Using **@ObservedObject** view A would need to hand the object to view B, which would hand it to view C, then view D, and finally view E – all the intermediate views would need to be sent the object even though they didn’t actually need it.

When using **@EnvironmentObject**, view A can create an object and place it into the environment. Any views inside it can then gain access to that environment object whenever they want just by asking for it, rather than having to pass it around explicitly – it makes our code much simpler.

### Warning
When a view using **@EnvironmentObject** is shown, SwiftUI will immediately search the environment for an object of the correct type. If such an object can’t be found – i.e., if you forgot to place it in the environment – then your app will immediately crash. When you use @EnvironmentObject you are effectively promising that object will exist in the environment by the time it is needed, a bit like using implicitly unwrapped optionals.

# License
[MIT](https://choosealicense.com/licenses/mit/)

# Bibliography 
1. [Apple Documentation](https://developer.apple.com/documentation/swiftui)
2. [Hacking With Swift](https://www.hackingwithswift.com)

###### Author 
Girolamo Pinto
