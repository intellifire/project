# Library Discussion Notes

## The Vision (My Current Thinking)

### Bandwidth
The current trend in development seems to be following the ubiquity of big bore bandwidth. I have always felt the pain of this folly as I live in an area that is rife with inconsistent and inferior bandwidth. When Applications are developed on the assumption that big pipes are available all the time, or that cellular networks mean accessibility everywhere, Our decision support systems fail and then we try to mitigate becuase we cannot address the root cause, a poorly architected Solution, ill equipped to handle the real world situations of minimal, or no connectivity.

### Dependencies
Dependencies and the software development lifecycle interference we see caused by changes to dependencies and another big factor here. Until Software I build is supported by more than a one-man-army, I need the sofware maintenance to be sustwainable, and upstream changes

My Recent choices have been driven by the desire to solve the following problems:

* Work intelligently online with lots of bandwidth, minimal bandwidth & offline.
* Less painful Upgrades
* less bugs introduced when dependencies change.
* Make codebase more accessible to Non-engineers
* lessen dependency on my knowledge to support systems.


### Frameworkless = Web Standards Instead of bloated Frameworks and Libraries
#### Why?
Frameworks come and go, while web standards tend to stick around and evolve in a backwards  compatible way. Frameworks cost bandwidth & overall application footprint real estate, while they save development time. They also increase depandancy madness and increase the possiblity of introducing bugs with any dependency upgrade/changes and frameworks can affect the ‘health’ and lifespan of a codebase.

web standards and web componets themselves wont fundamentally change as often as a framework or a library, and when standards change they are usually backwards compatible or deprecation and migration is usually well documented at MDN

#### How?
Going frameworkless looks attractive to me for many reasons, but mostly becuase it is eminently doable. The Modern Browser is now capabale of doing so much more since the addition of the following to basic browser ecosystems.

* Fetch API
* ES6 Features

with vast improvements under the hood of the browsers addressing:

* DOM manipulation works
* front-end application state management with different patterns

Documentation fo web standards has been dramatically improved by the multi coprpate collaboration to keep the MDN sites updated.

### Web components
#### Why?
web compontest represent a leap forward in basing development on standards. A web componet is an application built inside of a custom HTML tag.

```<my-custom-element myProperty='someValue'></my-custom-element>```

A web component has the capacity to be like a stand alone application with its own built in DOM and facilities, and can be 100% agnostic of your application look and feel (Styles), or the opposite, it can 100% conform to your application style depending on how you build them.
#### How?
I have gone through the experience of learning how to build web componets from pure HTML, CSS and Javascript, and the first thing I learned is, Its hard, and takes time and would be easier if there was something that was not a bloated framework to get it done. Hello litElement.

**litElement**
This very lightweight javascript library provides a simple base class for creating fast, lightweight web components. From the website:
> LitElement makes it easy to define Web Components – ideal for sharing elements across your organization or building a UI design system.

> Use your components anywhere you use HTML: in your main document, a CMS, Markdown, or a framework like React or Vue.

> ### Delightfully declarative
> LitElement’s simple, familiar development model makes it easier than ever to build Web Components.

> Express your UI declaratively, as a function of state. No need to learn a custom templating language – you can use the full power of JavaScript in your templates. Elements update automatically when their properties change.

> ### Fast and light
> Whether your end users are in emerging markets or Silicon Valley, they’ll appreciate that LitElement is extremely fast.

> LitElement uses lit-html to define and render HTML templates. DOM updates are lightning-fast, because lit-html only re-renders the dynamic parts of your UI – no diffing required.

> ### Seamlessly interoperable
> LitElement follows the Web Components standards, so your components will work with any framework.

> LitElement uses Custom Elements for easy inclusion in web pages, and Shadow DOM for encapsulation. There’s no new abstraction on top of the web platform.




### Service Oriented Architechture
#### Why?

SOA, or service-oriented architecture, defines a way to make software components reusable via service interfaces. These interfaces utilize common communication standards in such a way that they can be rapidly incorporated into new applications without having to perform deep integration each time.

#### How?

By developing specific micro-services with dedicated APIs on the back end, we are facilitating the use of abstracted micro-front ends that communicate via standardized APIs

## Progresive Web Apps

> As Wikipedia defines them, [PWAs](https://en.wikipedia.org/wiki/Progressive_web_application) are “web applications that are regular web pages or websites, but can appear to the user like traditional applications or native mobile applications.”

#### Why?
From the 2020 State of PWA report:
![From the 2020 State of PWA report](https://simplabs.com/assets/images/posts/2020-06-10-the-state-of-pwa-support-on-mobile-and-desktop-in-2020/infographic@1800-86adeafe83d6d8f7cac59be98a208ff6.png)


recent research shows that PWAs can provide many benefits:

* 68% increase of mobile traffic
* 15-fold improvement of load and installation speed
* 25-times reduced use of device storage
* 52% average conversion increase
* 78% average session increase
* 137% engagement increase
* 42.86% lower bounce rate when compared to that of mobile websites
* 133.67% increase in page views

1. Low Development Costs
- do not require different versions for various devices;
- reduces the amount of dev effort, costs go down.
- cost is three or four times lower than a native mobile app.

2. App-Like Look and Feel
- Apps are more user-friendly, work offline and are more attractive.
- Offer advanced user experience combining look/feel of mobile apps and website performance.  - Regardless of technologies, tools and frameworks, PWAs provide the same user experience as native mobile apps, and it is considered to be superior to that of websites.
- same speed, responsiveness and capabilities of websites with database access and automatic data.
- Search engines can index PWAs well compared to mobile apps

3. Fast Installation
- PWA Install experience is faster, smoother and improves user experience.
- no App Store or Google Play.
- After installation of PWAs, access it via a desktop(destop/laptop/tablet) or homescreen(mobile) icon.


``` beforeinstallprompt ``` Chrome & Edge.


- Some browsers offer call-to-action-like teasers that prompt users to download these apps
eg using
 This functionality comes built into browsers and allows the apps to enhance their credibility and reliability. As this software does not require installation on devices, users can easily access the PWA via a URL, which significantly contributes to the high shareability.

Read also: The Guide to Developing a Mobile Banking App
4. Better Performance
PWAs cache and serve text, images and other content in a specific, efficient manner, which enables them to operate like websites and significantly improves the running speed. Along with quick operation, impeccable performance is another attribute that has an impact on user experience and conversion rates.

Retailers and content providers should adopt this type of software as it enables a more positive user experience than mobile apps by improving retention and customer loyalty.

5. Platform- and Device-Agnosticism
Unlike regular applications that are very demanding on operating systems and the technical capabilities of various devices, PWAs work everywhere. A single app can satisfy the needs of various consumers and provide a uniform user experience on different endpoints. At the same time, this type of application enables cross-support to users that switch between their devices by providing them with a continuous experience. Users can access an app that has the same settings and data as that on another device.

This fact also significantly contributes to business automation, as companies that rely on PWAs know that the software their employees use performs seamlessly regardless of the platform or app version. Also, PWAs are highly responsive to various form factors, as they adapt properly to various screen sizes.

6. No Updating Issues
PWAs have a specific functionality that allows them to update automatically, without notifying users and bothering them with permission requests. These apps update themselves every time when users visit them, thus eliminating the need to download batch changes and install them. They just provide a renewed look with no human participation.

However, some of the producers of progressive apps send push notifications to users to inform them about the arrival of a new update. All the same, producers have full control of the information and content, to which users have access.

7. Seamless Offline Operation
The capability to operate offline or in compromised networks makes PWAs much more convenient than websites, which require a proper internet connection. Built-in service workers cache important progressive web apps’ features and information automatically, which eliminates the necessity to download it and allows users to access it without an internet connection.

It is based on the saving of information that users previously accessed, for example, pages. If they try to open those that they have not visited online, an app can show a custom offline page. This capability is crucial for retailers, as it allows them to prevent users from abandoning their catalogs and enhances customer retention.

Read also: A Mobile App for a Smart Home Solution: Takeaways and Guidelines
8. No Dependence on App Distribution Services
Usually, app distribution services, such as the App Store, Google Play or Microsoft Store, set high requirements to software that is included in their databases. Meeting their requirements may become quite a time- and effort-consuming process. Also, in some cases, services remove applications from databases without notice if a company fails to meet some of the requirements. So, PWAs allow producers to avoid complex reconciliation procedures as they do not need to be stored in similar services.

9. Push Notification Functionality
Like native mobile applications, PWAs have access to device-specific functionality, such as push notifications. This capability can be performed in various ways and allows companies to make the best use of content advertising.

Why are push notifications especially efficient when it comes to PWAs? According to some statistical data, almost 60% of users allow their progressive applications to send them notifications, which significantly increases opportunities to promote products or services. Moreover, these notifications are displayed on the screens of mobile devices, which is why there is a high probability that they attract users’ attention, especially when compared to email newsletters, blog entries or posts in social networks.

In such a way, a company can better access its target audience, and chances are, the audience will respond. Another valuable outcome is that these bouncing notifications, along with app icons on device desktops, considerably add to brand recognition, as they allow a business to draw attention to itself. However, users that have numerous applications installed on their mobile devices and that allow a great number of them to send notifications risk making their digital experiences cluttered.

10. Enhanced Security
PWAs rely on HTTPS to provide data safety and minimize the risk of security issues, as this protocol allows to preclude snooping and content tampering. Also, the applications take advantage of Web Bluetooth technology that includes certain security capabilities.


	above summarised from: https://www.sam-solutions.com/blog/the-benefits-of-progressive-web-apps-pwa-for-business/  [^1]








#### How?

### Mobile First - #### Why?
#### How?

## Typescript

- [ ] Should we or shouldnt we.

## Frameworks/Libraries I am avoiding (most popular first)

### React
#### Why?

### Vue.js
#### Why?

### Svelte
#### Why?

### Angular
#### Why?

### Jquery & Jquery UI
#### Why?

## Librarys/technologies I am leaning towards.

### NodeJS & NPM
#### Why?

### litEleent (and LitHTML)
#### Why?

### Web Components (HTML/JS vs React/Vue)
#### Why?

### OpenAPI 3.0 aka Swagger
#### Why?
__Code Generation__
By defining the API Requirements in a very specific format (YAML or JSON), the definitions is then used by code generation tools to produce a backend API server (Written in Node JS) and a front end client library (Written in Pure Javascript) to include in your app/component to ensure perfect communication between front end and back end.

__Documentation__
Further, OpenAPI 3 also provides immediate robust and accessible API documentation with built in teaching and demo tools to help a user understand exactly how to use the API and to implement it in your favorite language.

__Demos and Sample Request and Response Structures__
Finally, the resultant documentation provides not only great information on how to use the API but also examples of what the API input need to look like, but also what the returned results look like.


### Open Web Components
#### Why?
__Code Generation__
with a simple line of code and 4 easy to answer questions, the OWC code generator can scaffold out a basic standatrds-based web component in seconds. and the code is perfect.




[^1]:  [summarised from: https://www.sam-solutions.com/blog/the-benefits-of-progressive-web-apps-pwa-for-business/](https://www.sam-solutions.com/blog/the-benefits-of-progressive-web-apps-pwa-for-business/)