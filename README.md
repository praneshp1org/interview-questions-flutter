# interview-questions-flutter
Documentation of all questions that I have faced during interviews. Basically the realworld documentations of interview. I might have missed some question so please feel free to create pull request. A start will be appreciated. Best of Luck. Thank You 

<!-- Starting -->
<br />
<br />

### introudction

```
My name is Arjun Dahal.I am currently working on xyzcompany name as full stack mobile app developer. 
I have 2 years of experience in android development, 1 year in flutter and 1 year in go development.

I Specialize in these skills (read their requirement and try to match those sills):

1. Flutter App Development
    . Project Name
        - Description (What problem your app solved)
        - Tech Used 
        - Achivements (What you have learned)

2. Backend Development with Golang
    . Project Name
        - Description (What problem your app solved)
        - Tech Used
        - Achivements (What you have learned)

3. Native Android App Development with Kotlin
    . Project Name
        - Description (What problem your app solved)
        - Tech Used 
        - Achivements (What you have learned)

For more information please feel free to find my CV.

```


### Question Answer

### Dart Specific Questions

1. What is null safety in dart? <br/>
Ans: Generally, a variable holds some kind of value but let's take an example of a variable called favourite color now this varable can be null right? some of us don't have any favourite color so it kind of make sense. now let's imagine a situation that we don't have this beautiful feature of dart i.e null safety. we should always know  that the color variable can be null and check it all the time. now imagine you just forgot that variable favourite color can be null but you have just used it. now in this case you will get an error app will crash. what null safety does is it shows error while writing code so that you don't miss to address null and your app won't crash cuz you already know it can be null.

2. What is static variable or method? <br/>
Ans: The static variable or methods are the same for every instance of the class, so if we declare the data member as static then we can access it without creating an object.

3. What is const? <br/>
Ans: const means compile time constant. The expression value must be known at compile time.

4. What is final? <br/>
Ans: The final keyword is used to hardcode the values of the variable and it cannot be altered in future.  <br/>

5. What is abstract class?  <br/>
Ans: An abstract class is a class that can’t be instantiated, instead they are used for defining interfaces that are used by other classes. Abstract classes can only be extended. Abstract classes are useful for defining blue-prints for other classes to implement.  <br/>

6. What extends keyword is used for?<br/>
Ans: The extends keyword is typically used to alter the behavior of a class using Inheritance. 

7.  What implement keyword is used for? <br/>
Ans: The implement keyword is used to implement an interface by forcing the redefinition of the functions.<br/>

8. What is Mixins?<br/>
Ans: Mixins are a way to abstract and reuse a family of operations and state. It is similar to the reuse you get from extending a class, but is not multiple inheritances. 

9. What with keyowrd is used for? <br/>
Ans: With is used to include Mixins. A mixin is a different type of structure, which can only be used with the keyword with. <br/>

<!-- Reactive  -->

#### Reactive Programming 
10. What is reactive programming? <br/>
Ans: The reactive proramming is a programming paradime where we deal with data streams and act upon changes. <br/>

11. How can we do reactive programming in dart? <br/>
Ans: We can work with asyncronus data with steams. basically a stream emits multiple pieces of data over time. <br/>

12. How can we listen to multiple streams and is it possible to listen to it? <br/>
Ans: By default stream can be only listened by single subscriber but there is something called broadcast streams this can be listened by multiple subscribers. <br/>

13. What is Stream Controller? <br/>
Ans: Steam Controller allows sending data, error and done events on its stream. This can be used to create a simple stream that others can listen on, and to push events to that stream. <br/>

14. What is StreamSink? <br/>
Ans: A StreamSink is a StreamConsumer, which means it can take several streams (added by addStream) and processes the events these streams emit. <br/>

15. What is RxDart? <br/>
Ans: RxDart extends the capabilities of Dart Streams and StreamControllers. so basically this means that RxDart has all the capabilities of stream and additonal features. <br/>

16. How can we Combime Streams in RxDart? <br/>
Ans: We can combine a specific number of Streams together with proper types information for the value of each Stream by sing combine2..9(2 represents combining two streams and so on till 9) <br/>

17. What is BehaviourSubject in RxDart? <br/>
Ans: BehaviorSubject captures only the latest added item. When a new listener starts to listen to the controller, it will receive the stored item. <br/>

18. What is ReplaySubject in RxDart? <br/>
Ans: ReplaySubject captures all items that have been added. When a new listener starts to listen to the controller, it will receive all items. After that, any new event will be sent to all listeners. <br/>

19. What is PublishSubject in RxDart? <br/>
Ans: PublishSubject emits all the items on listen that is added. <br/>



## Flutter Specific Questions

1. What is Stateless Widget? <br/>
Ans: Stateless widgets are those widgets which states or content is not changed with user interaction <br/>

2. What is Stateful Widget? <br/>
Ans: Widgets value can be changed as per users interaction is stateful widget. </br>

3. What is StatelessElement? <br/>
Ans: An Element that uses a StatelessWidget as its configuration.<br/>

4. What is StatefulElement? <br/>
Ans: An Element that uses a StatefulWidget as its configuration.

5. What is InheritedWidget? <br/>
Ans: Base class for widgets that efficiently propagate information down the tree. e.g. Theme.of(context).primaryIconTheme.color <br/>

6. How do we find Screen sizes and resolution?<br/>
Ans: Using MediaQuery

7. How can we implement LazyLoading? <br/>
Ans: 
- You can listen to a ScrollController.
- ScrollController has some useful information, such as the scrolloffset and a list of ScrollPosition.
- ScrollPosition contains informations about it's position inside the scrollable. Such as extentBefore and extentAfter. Or it's size, with extentInside.
- Considering this, you could trigger a server call based on extentAfter which represents the remaining scroll space available.

10. What's the use of Vsync? <br/>
Ans: Vsync/TickerProvider allows animations to be muted, slowed, or fast-forwarded.

11. How can we serialize complex json? <br/>
Ans: We can use json_serializable package and use that to generate code for us. similar to gson on native android development.

12. What is Dio? <br/>
Ans: Dio is a powerful HTTP client for Dart. It has support for interceptors, global configuration, FormData, request cancellation, file downloading, and timeout, among others. Flutter offers an http package that’s nice for performing basic network tasks but is pretty daunting to use when handling some advanced features. By comparison, Dio provides an intuitive API for performing advanced network tasks with ease.




## StateManagement Related Questions

1. What is state management? <br/>
Ans: State-Management is the implementation of a Design Pattern, with the help of  design pattern we can synchronize the state of the application throughout all widgets of the application.  <br/>

2. Why not just use setState?
Ans: Let's suppose we are building an app and we have a screen which have ton of widgets. Now the problem with any ui framework is painting screen. This thing is super duper expensive. Now let's assume a situation where we want to change a text value only depending of button click. Now we can use something called setState to repaint the whole screen but will it be effective? just to change the text is good to paint the whole screen is expensive.

3. Why we need state management? <br/>
Ans: The State of the Whole Application is present at a single place, so we do not need to access the single state or data from different places.  This makes our code clean and seprate business logic from ui logic <br/>

4. When to implement the state management? <br/> 
Ans: If the application contains a large number of widgets and a lot of requests are being sent to the back-end for data retrieval, then it becomes mandatory to implement the state-management, as it will boost the user experience and speed of the application to a great extent.

5. What are the state managemet approaches in flutter? </br>
Ans: 
    Provider
    setState
    InheritedWidget & InheritedModel
    Redux
    Fish-Redux
    BLoC / Rx
    GetIt
    MobX
    Flutter Commands
    Binder
    GetX
    Riverpod
    states_rebuilder


6. What is ChangeNotifierProvider from Provider Package? <br/>
Ans: ChangeNotifierProvider listens for changes in the model object. When there are changes, it will rebuild any widgets under the Consumer. <br/>


7. What is FutureProvider? <br/> 
Ans: The FutureProvider listens for when the Future completes and then notifies the Consumers to rebuild their widgets. <br/>

8. What is StreamProvider? <br/>
Ans:StreamProvider is basically a wrapper around a StreamBuilder. You provide a stream and then then the Consumers get rebuilt when there is an event in the stream. The StreamProvider doesn’t listen for changes in the model itself. It only listens for new events in the stream. </br>



### Design patterns in Dart
[SOLID](https://github.com/ArjunDahal864/SOLID_principle_in_dart)
