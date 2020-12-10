# Library Discussion Notes

## The Vision (My Current Thinking) and perhaps a case for doing it all!

### Bandwidth
The current trend in development seems to be following the ubiquity of big bore bandwidth. I have always felt the pain of this folly as I live in an area that is rife with inconsistent and inferior bandwidth. When Applications are developed on the assumption that big pipes are available all the time, or that cellular networks mean accessibility everywhere, Our decision support systems fail and then we try to mitigate because we cannot address the root cause, a poorly architected Solution, ill equipped to handle the real world situations of minimal, or no connectivity.

### Dependencies
Dependencies and the software development lifecycle interference we see caused by changes to dependencies and another big factor here. Until Software I build is supported by more than a one-man-army, I need the software maintenance to be sustainable, and upstream changes

My Recent choices have been driven by the desire to solve the following problems:

* Work intelligently online with lots of bandwidth, minimal bandwidth & offline.
* Less painful Upgrades
* less bugs introduced when dependencies change.
* Make codebase more accessible to Non-engineers
* lessen dependency on my knowledge to support systems.


### Frameworkless = Web Standards Instead of bloated Frameworks and Libraries
#### Why?
Frameworks come and go, while web standards tend to stick around and evolve in a backwards  compatible way. Frameworks cost bandwidth & overall application footprint real estate, while they save development time. They also increase dependency madness and increase the possibility of introducing bugs with any dependency upgrade/changes and frameworks can affect the ‘health’ and lifespan of a codebase.

web standards and web components themselves wont fundamentally change as often as a framework or a library, and when standards change they are usually backwards compatible or deprecation and migration is usually well documented at MDN

#### How?
Going frameworkless looks attractive to me for many reasons, but mostly because it is eminently doable. The Modern Browser is now capable of doing so much more since the addition of the following to basic browser ecosystems.

* Fetch API
* ES6 Features

with vast improvements under the hood of the browsers addressing:

* DOM manipulation works
* front-end application state management with different patterns

Documentation fo web standards has been dramatically improved by the multi corporate collaboration to keep the MDN sites updated.

### [Web components](#web-components)
#### Why?
web components represent a leap forward in basing development on standards. A web component is an application built inside of a custom HTML tag.

```<my-custom-element myProperty='someValue'></my-custom-element>```

A web component has the capacity to be like a stand alone application with its own built in DOM and facilities, and can be 100% agnostic of your application look and feel (Styles), or the opposite, it can 100% conform to your application style depending on how you build them.
#### How?
I have gone through the experience of learning how to build web components from pure HTML, CSS and Javascript, and the first thing I learned is, Its hard, and takes time and would be easier if there was something that was not a bloated framework to get it done. Hello litElement.

[litElement](#lit-element)
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




### Service Oriented Architecture
#### Why?

SOA, or service-oriented architecture, defines a way to make software components reusable via service interfaces. These interfaces utilize common communication standards in such a way that they can be rapidly incorporated into new applications without having to perform deep integration each time.

#### How?

By developing specific micro-services with dedicated APIs on the back end, we are facilitating the use of abstracted micro-front ends that communicate via standardized APIs

## Progressive Web Apps

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
- After installation of PWAs, access it via a desktop(desktop/laptop/tablet) or homescreen(mobile) icon.
- Some browsers offer call-to-action-like teasers that prompt users to download these apps
eg using
``` beforeinstallprompt ``` on Chrome & Edge.
This is built into those browsers, and for those that cannot do it, you can easily access the PWA via a URL, which means high shareability.


4. Better Performance
- PWAs cache and serve content in a specific, efficient manner,
- Act like websites but perform ultra fast like native apps.
- Research at corporations show that PWAs provide more positive user experience than mobile apps by improving retention and customer loyalty.

5. Platform- and Device-Agnosticism
- Normal applications are very demanding on OS and the devices,
- PWAs work everywhere. A single PWA can deliver uniform user experience on different endpoints.
- PWAs enable cross-support to users that switch between their devices by providing them with a continuous experience.
- Users can access a PWA that has the same settings and data as that on another device.
- significantly contributes to business automation
- PWAs are highly responsive to various form factors, as they adapt properly to various screen sizes.

6. No Updating Issues
- PWAs can update automagically, without notifying users or asking permission.
- PWAs are update every time you go online, eliminating the need to download batch changes and install them.
- PWAs provide a renewed look with no human participation.
- PWAs can be configured to send push notifications,informing end users of a new update.


7. Seamless Offline Operation
- PWAs operate offline or in compromised networks.
- Built-in service workers cache important features and information automatically
- PWAs can provide offline services that do not feel offline.

8. No Dependence on App Distribution Services
- No need for expensive or inconvenient app distribution services, such as the App Store, Google Play or Microsoft Store.
- Meeting app distribution service requirements becomes an expensive,time- and effort-consuming process.
- Some services remove applications from databases without notice if it fails to meet some of the requirements.
- PWAs allow Devs to avoid complex reconciliation procedures as they do not need to be stored in similar services.

9. Push Notification Functionality
- PWAs have access to device-specific functionality, such as push notifications.
- PWA push notifications are especially efficient.
- almost 60% of users allow their PWAs to send them notifications

10. Enhanced Security
- PWAs rely on HTTPS to provide data safety and minimize the risk of security issues
- PWAs leverage Web Bluetooth technology that includes certain security capabilities.

[summarized from: https://www.sam-solutions.com/blog/
the-benefits-of-progressive-web-apps-pwa-for-business/] [1]

#### How?

Building, Implementing and maintaining PWAs can be streamlined with the following tools/products (See explanations elsewhere in this document):

- open web components
- litElement
- nodeJS


### Mobile First
#### Why?

Every piece of software I have ever developed has had the client come to me and say, can we make it into an app now?

Making an app or a website mobile ready after the fact is silly and wasteful and usually compromises the original design to make it more mobile friendly, by taking a mobile first approach, it will never be an afterthought with respect to mobility.

#### How?

- Leverage W3.CSS (mobile first)
- Leverage PWAs



## Typescript

- [ ] Should we or shouldn't we.

This might be a moot point, I think we should, I just don't know typescript yet.

## Frameworks/Libraries I am avoiding (most popular first)

### React
#### Why?
- size
- complexity
- learning curve
- my deadlines

### Vue.js
#### Why?
- size
- complexity
- learning curve
- my deadlines

### Svelte
#### Why?
- size
- complexity
- learning curve
- my deadlines

### Angular
#### Why?
- size
- complexity
- learning curve
- my deadlines
- very old (relative)

### Jquery & Jquery UI
#### Why?
- size
- complexity
- learning curve
- my deadlines
- most functionality can be achieved by using ES6 standard.
- UBER old (relative)

## Libraries/technologies I am leaning towards.


### W3.CSS
#### Why?
- [W3.CSS](https://www.w3schools.com/w3css/default.asp) is a great standards based, pure CSS framework providing a vast array of complex web features by simply adding well defined and named classes
- Junior and beginner web developers find themselves learning coding from w3schools, the developers of W3.CSS. Because of this, W3.CSS is thoroughly documented with examples and online sandboxes to experiment outside your app with some of your own code. Additionally, W3.CSS is easy to use and to understand for beginners, but ridiculously simple and a no-brainer for pros. so people who find themselves in code loire this have little trouble understanding how to change ot or what it is doing. eg:
```
<div class="w3-container w3-teal"> <!-- Give it container abilities, color it teal ->
  <h1>Summer Holiday</h1>
</div>

<div class="w3-row-padding w3-margin-top"> <!-- pad the rows, put a margin at the top ->

  <div class="w3-third"> <!-- this div will take up 1/3 of the screen width. ->
    <div class="w3-card"> <!-- style it as a card object ->
      <img src="img_5terre.jpg" style="width:100%">
          ...
```

### NodeJS & NPM
#### Why?
NodeJS and NPM offer several benefits:
- NodeJS and NPM can be used to pre-build web components and while required during development, they do not add dependance to the final application, neither NodeJS nor NPM are required by the end user.
- This combo has been very successful for rapid development of pure pure (HTML/JS vs React/Vue) web components.

### litElement (and LitHTML)
#### Why?
The advantages are obvious, [but see details else where in this document](#lit-element)
### Pure Web Components (HTML/JS vs React/Vue)
#### Why?
see: [Web Components Elsewhere in this document](#web-components)
### OpenAPI 3.0 aka Swagger
#### Why?
__Code Generation__
By defining the API Requirements in a very specific format (YAML or JSON), the definitions is then used by code generation tools to produce a backend API server (Written in Node JS) and a front end client library (Written in Pure Javascript) to include in your app/component to ensure perfect communication between front end and back end.

__Documentation__
Further, OpenAPI 3 also provides immediate robust and accessible API documentation with built in teaching and demo tools to help a user understand exactly how to use the API and to implement it in your favorite language.

__Demos and Sample Request and Response Structures__
Finally, the resultant documentation provides not only great information on how to use the API but also examples of what the API input need to look like, but also what the returned results look like in either JSON or XML (and even more formats)


### Open Web Components
#### Why?
__Code Generation__
with a simple line of code and 4 easy to answer questions, the OWC code generator can scaffold out a basic standards-based web component in seconds. and the code is perfect.




[1]: [above summarized from: https://www.sam-solutions.com/blog/the-benefits-of-progressive-web-apps-pwa-for-business/](https://www.sam-solutions.com/blog/the-benefits-of-progressive-web-apps-pwa-for-business/)