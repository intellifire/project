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
#### How?

## Progresive Web Apps
#### Why?
#### How?

### Mobile First - #### Why?
#### How?

## Typescript

- [ ] Should we or shouldnt we.

## Frameworks/Libraries I am avoiding

### React

### Vue.js

### Jquery & Jquery UI

## Librarys/technologies I am leaning towards.

## litEleent (and LitHTML)

## Web Components (HTML/JS vs React/Vue)

