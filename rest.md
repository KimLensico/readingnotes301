# REST

## Roy Fielding
- helped write the first web servers 
- did a ton of research explaining why the web works the way it does
- His name is on the specification for the protocol that is used to get pages from servers to your browser

- HTTP is one of the most important breakthroughs in the history of computing.
  -  it is capable of describing the location of something anywhere in the world from anywhere in the world
  - the foundation of the web

- The whole world wide web is built on an architectural style called “REST”
  - REST provides a definition of a “resource”, which is what those things point to

- **Web Page** - is a “representation” of a resource. 
  - Resources are just concepts. 
  - URLs tell the browser that there's a concept somewhere 
  - A browser can then go ask for a specific representation of the concept
    - the browser asks for the web page representation of the concept
  - [in most cases] a resource has only a single representation
    - for now, there are new formulas popping up so there could be more in the future 

## APIs 
> “Web Services” or "APIs" (concept)
> - means a lot of different things to a lot of different people
> - the basic concept is that machines could use the web just like people do.

- computers can use those same protocols to send messages back and forth to each other 
- people have been doing that for a long time 
  - none of the techniques used today work well when attempting to talk to all of the machines in the entire world
   - [<!-- --> APIs <!-- -->] weren't designed to be used like that. 
   
- When Fielding and his buddies started building the web, being able to talk to any machine anywhere in the world was a primary concern 
  - Most of the techniques we use at work to get computers to talk to each other didn't have those requirements.
    - [<!----> PAST] just needed to talk to a small group of machines.
    - [<!----> PRESENT] We need to be able to talk to all machines about all the stuff that's on all the other machines
      - We need some way of having one machine tell another machine about a resource that might be on yet another machine.
- Machines tell each other where things are through the URL
  - If everything that machines need to talk about has a corresponding URL 
  - Machines don't have a universal noun ~~-that's why they suck.~~ 
    - Every programming language, database, or other kind of system has a different way of talking about nouns. 
      - Why the URL is so important: It lets all of these systems tell each other about each other's nouns.

**“polymorphism”** - a ~~geeky~~ way of saying that different nouns can have the same verb applied to them

HTTP is all about applying ***verbs*** to **nouns**. 
 - For instance, when you go to a web page, the browser does an HTTP GET on the URL you type in and back comes a web page.
  - images on web pages are separate resources. 
    - The web page just specifies the URLs to the images  
    - the browser goes and does more GETs using the HTTP protocol on them until all the resources are obtained and the web page is displayed 
    - But the important thing here is that **very different kinds of nouns can be treated the same.** 
      - whether the noun is an image, text, video, an mp3, a slideshow, whatever. We can GET all of those things the same way given a URL.
  - Browsers pretty much just GET stuff
    - They don't do a lot of other types of interaction with resources.
      - This is a problem because it has led many people to assume that HTTP is just for GETing. 
      - But HTTP is actually a general purpose protocol for applying verbs to nouns

A machine can't understand a normal web page
 - web pages are designed to be understood by people
 - a machine doesn't care about layout and styling 
    - machines basically just need the data 
    - [<!----> Ideally] every URL would have a human readable and a machine readable representation. 
      - When a machine GETs the resource, it will ask for the machine readable one. 
      - When a browser GETs a resource for a human, it will ask for the human readable one.