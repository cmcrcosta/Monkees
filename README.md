# MONKEES WEBSITE

## 1. BRIEF

The objective is to Build a static (front-end only) website for a 1960’s rock band that has around 50 years experience of performing live at numerous events around the world. 

I have choosen to use the assets provided to achieve the client's following requirements:

* Target audiences - their fans and potential fans.
* Allow target audiences to see and hear clips from their back catalog, and any new material as it becomes available.
* Showcase their music and publicise their availability to perform at events such as weddings and Christmas parties.
* Showcase:
    * Photos of the band members
    * A video clip
    * Audio clips
* Add links to their Facebook, Twitter and YouTube pages.


## 2. PLANNING

Firstly I decided the site structure and objectives - 5 Sections:

* Index
    * Navigation Menu pointing to the other 4 sections
    
* Our Music 
    * Promote new material as it becomes available 
    * Allow seeing and hearing clips from their back catalog

* Events 
    * Promote new events 
    * Publicise their availability to perform at events
    
* News and Media
    * Show relevant news
    * Showcase Previous Events
 
* Hire Us
* Contact Us form

I chose to add a fixed navigation bar on the header across all sections (except index).

## 3. DEVELOPMENT

## 3.1. Main Structure

The main structure contains 5 sections each showing at the full size of the screen.

**HTML**

    <!DOCTYPE html>
        <html lang="en">
        <head>
            <meta charset="utf8">
            <meta name="viewport" content="width=device-width, initial-scale=1.0">
            <link rel="stylesheet" href="assets/css/style.css" type="text/css"/>
            <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css">
            <link rel="stylesheet" href=https://cdnjs.cloudflare.com/ajax/libs/hover.css/2.1.1/css/hover-min.css>
            <link href="https://fonts.googleapis.com/css?family=Coiny" rel="stylesheet">
        </head>
        
        <body>
            <header></header>
            <main>
            <section id="index"></section>
            <section id="music"></section>
            <section id="events"></section>
            <section id="news"></section>
            <section id="hire"></section>
            </main>
            <footer></footer>
        </body>
    </html>
    
**CSS**

    html, 
    body,
    main {
        height:100%;
        width:100%;
        margin: 0;
        padding:0;
    }
    
    section {
        display:block;
        height:100%;
        width:100%;
        padding: 0;
        margin: 0;
    }
    
    a {
    text-decoration: none;
    color: inherit;
    }
    
### 3.1.1 Navigation Bar

    The same navigation bar is used across all devices 
    with minor changes added with media query:

**HTML**

    <header>
        <nav>
            <ul>
                <li class="li-index"><a href="#index">HOME</a></li>
                    <li class="li-music"><a href="#music">MUSIC</a></li>
                    <li class="li-events"><a href="#events">EVENTS</a></li>
                    <li class="li-news"><a href="#news">NEWS &amp; MEDIA</a></li>
                    <li class="li-hire"><a href="#hire">HIRE US</a></li>
                </ul>
            </nav>
    </header>
    
**CSS:**

    nav {
        position: fixed; 
        z-index:7;
        display: table;
        margin:0 auto;
        padding:0;
        font-size: 0;
        width: 100%;
        height:10%;
        background-color: rgb(38,37,37);
    }
    
    nav ul {
        display: table;
        margin:0 auto;
        padding:0;
        width:100%;
        height:100%;
    }
    
    nav ul li { 
        display: table-cell;
        width:20%;
        height:100%;
        font-family: 'Coiny', cursive;
        font-weight: 700;
        font-size: 1.75vw;
        text-align: center;
        vertical-align: middle;
        line-height:200%;
    }
    
    nav ul li a { 
        display: block;
    }
    
    .li-index {
        color: rgba(173,43,173,0.9);
    }
    
    .li-index:hover {
        color: rgb(255,255,255);
        -webkit-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        -moz-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        -o-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        background-color: rgba(173,43,173,0.5);
    }
    
    .li-music {
        color: rgba(243,208,18,0.9);
    }
    
    .li-music:hover {
        color: rgb(255,255,255);
        -webkit-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        -moz-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        -o-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        background-color: rgba(243,208,18,0.5);
    }
    
    .li-events {
        color: rgba(205,228,49,0.9);
    }
    
    .li-events:hover {
        color: rgb(255,255,255);
        -webkit-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        -moz-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        -o-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        background-color: rgba(205,228,49,0.5);
    }
    
    .li-news {
        color: rgba(135,218,224,0.9);
    }
    
    .li-news:hover {
        color: rgb(255,255,255);
        -webkit-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        -moz-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        -o-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        background-color: rgba(135,218,224,0.5);
    }
    
    .li-hire {
        color: rgba(252,78,154,0.9);
    }
    
    .li-hire:hover {
        color: rgb(255,255,255);
        -webkit-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        -moz-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        -o-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        background-color: rgba(252,78,154,0.5);
    }
    
    @media only screen and (max-device-width: 767px){
    nav ul li { 
        font-size: 2.5vw;
    }
    }

## 3.2. Section Index
    
The Index section only contains 4 buttons, each one linking to a different section.
    
To achieve this I created 2 div colums and 4 buttons. And I also added 1 span per button 
on the media query to center the text on the buttons for small/medium screens.
The configuration is also different depeding on the devices.

**HTML:**

    <section id="index">
            <div class="column-menu">
                <div class="button-menu music">
                    <span class="span-menu"><a href="#music">OUR MUSIC</a></span>
                </div>
                <div class="button-menu events">
                    <span class="span-menu"><a href="#events">EVENTS</a></span>
                </div>
            </div>
            
            <div class="column-menu">
                <div class="button-menu news">
                    <span class="span-menu"><a href="#news">NEWS &amp; MEDIA</a></span>
                </div>
                <div class="button-menu hire">
                    <span class="span-menu"><a href="#hire">HIRE US</a></span>
                </div>
            </div>
    </section>
    
**CSS:**

    Section - Index:
    
    .column-menu {
        display: table;
        width: 100%;
        height: 50%;
        margin: 0;
        padding:0;
    }
    
    .button-menu {
        display: table-cell;
        font-family: 'Coiny', cursive;
        font-weight: 700;
        font-size: 5vw;
        text-align: center;
        vertical-align: middle;
        width: 50%;
        height: 50%;
    }
    
    .button-menu.music {
        color: rgba(243,208,18,0.9);
    }
    
    .button-menu.music:hover {
        color: rgb(5,48,69);
        -webkit-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        -moz-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        -o-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        background-color: rgba(243,208,18,0.5);
    }
    
    .button-menu.events {
        color: rgba(205,228,49,0.9);
    }
    
    .button-menu.events:hover {
        color: rgb(5,48,69);
        -webkit-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        -moz-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        -o-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        background-color: rgba(205,228,49,0.5);
    }
    
    .button-menu.news {
        color: rgba(135,218,224,0.9);
    }
    
    .button-menu.news:hover {
        color: rgb(5,48,69);
        -webkit-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        -moz-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        -o-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        background-color: rgba(135,218,224,0.5);
    }
    
    .button-menu.hire {
        color: rgba(252,78,154,0.9);
    }
    
    .button-menu.hire:hover {
        color: rgb(5,48,69);
        -webkit-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        -moz-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        -o-transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        transition: background-color 0.5s ease-in-out, color 0.5s ease-in-out;
        background-color: rgba(252,78,154,0.5);
    }
    
    Section - Index - Small Devices:

    @media only screen and (max-device-width: 767px){
        .column-menu {
            display: table;
            width: 100%;
            height: 50%;
            margin: 0;
            padding:0;
        }
    
        .button-menu {
            display: table;
            font-family: 'Coiny', cursive;
            font-weight: 700;
            font-size: 10vw;
            width: 100%;
            height: 50%;
        }
        
        .span-menu {
            display:table-cell;
            text-align: center;
            vertical-align: middle;
        }
    
        .button-menu.music {
            color: rgb(5,48,69);
            background-color: rgba(243,208,18,0.5);
        }
    
        .button-menu.events {
            color: rgb(5,48,69);
            background-color: rgba(205,228,49,0.5);
        }
        
        .button-menu.news {
            color: rgb(5,48,69);
            background-color: rgba(135,218,224,0.5);
        }
        
        .button-menu.hire {
            color: rgb(5,48,69);
            background-color: rgba(252,78,154,0.5);
        }
    }
    
    @media only screen and (orientation: landscape) {
            .button-menu {
            font-size: 5vw;
            }
    }