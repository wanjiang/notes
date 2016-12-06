#Java and Flash decline
##Java
- the language's complex nature
- slow evolution and lack of integration
- not enough to provide the tools to create the applications demanded by an 
  increasing number of users. 
##Flash
- share the same basic characteristics with its competitor

##Javascript (Web 2.0)
- browers were improving their Javascript engines
- more pwer brought more opportunities, and this scripting language was 
  ready to embrace them.

#html5 content markup
HTML5 is the development of that combination, the glue that holds
everything together. HTML5 proposes standards for every aspect of the Web as
well as a clear purpose for each technology involved. 

##HTML5 three basic features
- structure
- style
- functionality

###HTML5
- HTML5 is considered a product of the combination of HTML, CSS and Javascript.
  - HTML (markup language) is in charge of the structure, provides the structural elements
    - Form API
    - Fullscreen API
    - Canvas API
    - Cross-Origin using CORS (Cross-Origin Resource Sharing)
      - is an application that is allocated in one domain and accessing 
        resources from another. 
    - WebGL and Three.js
      - WebGL is an exteremely low-level API that works with the <canvas>
        element to create 3D graphics for the web. It utilizes the GPU of
        the video card to perform some perations and relieves the CPU
        of the hard work.
    - Drag and Drop
    - Web Storage API
      - Cookies (store small pieces of information on the client side)
      - Web Storage API store data in the user's hard drive and use it later
        as a desktop applicaiton would
        - sessionStorage
          - will keep data available only for the duration of a page session.
        - localStorage
          - works similarly to a storage system for a desktop application.
    - IndexedDB API
      - the web storage API is useful for small amounts of data,
        indexedDB API is for large  amounts of structured data.
    - File API
      - File Storage
    - Geolocation API
      - provide a standard detection mechanism for browsers to let
        developer determine the user's geographic location.
    - Page Visibility API
    - Ajax Level 2
      - XMLHttpRequest, provides a way to access the server and retrieve
        information from javascript without reloading the HTML document
    - Web Messaging API
      - communicating with an iFrame
    - WebSockets
      - provides connection support for faster and more effective bi-directional        communication between browsers and servers.
    - WebRTC
      - web real-time communication.
      - create an effective peer-to-peer connection.
    - Web Workers 
      - multithreading language
      - Types of workers
        - dedicated worker (only responds to the main code from which it 
          was created)
        - shared worker (responds to multiple documents, share the same worker
          from different windows, tabs ..)


  - CSS (sheet of style) presents that structure and its content on the screen,
    manages the structure to make it attractive and useful
    - selector
    - properties are the core of CSS
    - Styles
      - Inline Styles
      - Embedded Styles
      - External Files
        - References by Keyword
        - References by the Id Attribute
        - References by the Class Attribute
        - References by the Any Attribute
        - References by the Pseudo-Class

  - Javascript (scripting language, prototype-based scripting language) 
    has the necessary power to provide functionality and build full 
    web applications.
    - Ajax is the name of group of techniques developed in Javascript
      that allow applications to get information form the server without
      refreshing the web page or loading a new document.
    - Types
      - Inline 
      - Embedded <script>
      - External File
    - Things
      - Refernece elements
      - register events
      - Interacting with the document
    - InnerHTML outerHTML and InsertAdjacentHTML
    - API
      - Native APIs (are included natively by HTML5)
      - External APIs (Google Maps, jQuery)

###Introduction to HTML
- The HyperText Markup Language is a programming language.
- It is not composed by commands or instruction but rather
  a set of tags that organize and declare a purpose for the 
  content of the document.
- The concept behind the creation of this language was the idea of
  sharing through the Internet not only the text included in the
  documents but also its format.

####HTML Tags
- meta
  - defines the character encoding of the document.
  - important for search engines and devices that need to preview 
    or get aa summary of the relevant data.
- title
- link
  - used to incorporate style, script, images or icons from external files
- head vs header
  - header is intended to provide introductory information,
    only to be used for the body or for sections within the body.
  - head providing information about the entire document
- nav
- section
- aside

####HTML Attributes
- Data-* 
- Reversed
- Ping and Download

#Browser engine
- WebKit (Chrome)
- (Firefox)


###CSS Model
####Box Models
Browsers consider every HTML element as a box,
A webpage is actually a group of boxes put together following certain rules
- Traditional Box Model
  - The boxes were created by expanding cells and combining rows of cells,
    columns of cells and entire tables.
  - It needs the boxes to be wrapped together to procide horizontal order.
- Grid
- Flexible Box Model
  - The main purpose of a box model is to provide a mechanism for dividing
    the window's space into several boxes and creating the rows and columns
    that are part if a regular web design.
  - However, the Traditional Box Model fails in this regard.
  - The Flexible Box Model solves the Traditional Box Model's problems
    in an elegant manner.
  - In this model, the boxes finally represent those virtual rows and
    columns that are, in fact, what designers and users really see and
    care about.
  - the need to distribute the space in the window among the elements
    of the dicument. the elements had to be reduced or increased in size
    according to the space available.
    - flex containers
      - is an element that allows its content to be flexible.
      - declares two axes
        - the main axis
        - the cross axis
    - Justify-Content
      - the capacity to lay out free space
    - flex-wrap

####CSS3
- filter
  - add effect to an image
- transform
  - scale
  - rotate
  - skew
  - move or translate
- 3D transform
- transition
- animation


###Javascript
- is an interpreted language used for multiple purpose
- turn script into machine code in order to reach execution speeds similar to
  desktop app.
- perform numerous tasks
- capacity to store and process information

####Event Attributes
- HTML provides attribute to insert Javascript code.

####cross-browser technique




#Webworkers (threading)

#Websockets

#Geolocation (gps)

#orientation (accelerometer)

#audio/visual (play and record)

#webstorage (files, indexdb)

#canvas (2D and 3D)

#webgl (opengl for web)

#svg (inline graphics)

#drag and drop

#metatags

#selectors

#offline cache and use of "apps"

#fullscreen API

#pointer-lock API

#Server-Sent Events / Notifications

#RTC (Real-time Communications e.g. teleconference)

#improvements in forms

#improvements in iframe

#Layout

##css3

##Flexbox

##GridLayout
