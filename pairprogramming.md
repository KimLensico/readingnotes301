# Pair Programming

## JQuery:
> a javascript file that you include in your web pages. It lets you find elements using CSS-style selectors and then do something with the elements using JQuery methods

- ```jQuery()``` lets you find one or more elements on the page
  - creates an object called **jQuery** 
    - holds references to those elements
    ```$()``` is often used as a shorthand
- jQuery selectors perform a similar task to traditional DOM queries
  - syntax is simpler
- jQuery objects can be stored in a variable [like DOM nodes]
- you can use jQuery methods and properties to manipulate the DOM nodes that you select
  - the methods represent tasks that you commonly need to perform with elements

  ### KEY DIFFERENCES FROM DOM
  - cross-browser, no need to write fallback code
  - selecting elements is simpler
    - uses css style syntax (more accurate)
  - event handling is simpler
    - uses one method that works in all major browsers
  - methods affect all the selected elements without the need to loop through each one
  - additional methods are provided for popular required tasks. ex: animations
  - one you made a selection, you can apply MULTIPLE methods to it

### Adding jQuery to a Page
  1. in order to use jQuery, the jQuery scrip has to be included in the html page
    - before the ```</body>``` tag
  2. add a second javascript file that uses jQuery selectors and methods to update the content of the HTML page

- websites that use jQuery files with the extension .min.js means unnecessary spaces and carriage returns have been stopped from the file
  - ex: ```jquery-1.11.0.js``` becomes
```jquery-1.11.0.min.js.``` 
-  **minification** - converting to a much smaller file
  - makes it faster to download it 
  - harder to read 
- jQuery's motto: *"Write less, do more"*

---

## Pair Programming
>pair programming commonly involves two roles: the Driver and the Navigator. 
 - **Driver** - the programmer who is typing and the only one whose hands are on the keyboard
 - **Navigator** - uses their words to guide the Driver but does not provide any direct input to the computer.
  - thinks about the big picture, what comes next, how an algorithm might be converted in to code, while scanning for typos or bugs.
  - might also utilize their computer as a second screen to look up solutions and documentation, but *should not be writing any code*. 

  ### Fundamentals to Learn a New Language
1. **Listening**: hearing and interpreting the vocabulary 
2. **Speaking**: using the correct words to communicate an idea 
3. **Reading**: understanding what written language intends to convey 
4. **Writing**: producing from scratch a meaningful

  ### 4 Skills Pair Programming Covers:
  1. **explain** out loud what the code should do
  2. **listen** to others’ guidance
  3. **read** code that others have written
  4. **write** code themselves.

  ### Outcome of Pair Programming
  1. **Greater Efficiency**
    - when two people focus on the same code base, it is easier to catch mistakes in the making. 
    - research indicates that pair programing takes slightly longer, but produces higher-quality code that doesn’t require later effort in troubleshooting and debugging 
      - [in the long-run] it’s more efficient than two people working on separate features. 
      - when coming up with ideas and discussing solutions out loud, two programmers may come to a solution faster than one programmer on their own. 
      - when the pair is stuck, both programmers can research the problem and reach a solution faster
      - pairing enhances technical skills and team communication
        - also helped with the **enjoyability** of coding in the workplace.

2. **Engaged Collaboration**
  - When two programmers focus on the same code, the experience is more engaging
    - both programmers are more focused than if they were working alone. 
    - harder to procrastinate or get off track when someone else is relying on you to complete the work
  - Another important aspect of learning to program is **knowing when to ask for help**. 
    - *spend no more than fifteen minutes stuck on a problem* before asking a teaching assistant or instructor for help. 
      -pairs rely more on each other and can often find a solution together without needing to ask for additional help 
      - ultimately boosts overall confidence.

3. **Learning from Fellow Students**
  - Everyone has a different approach to problem solving 
    - working with a teammate can expose developers to techniques they otherwise would not have thought of
      - if one developer has a unique approach to a specific problem, pair programming exposes the other developer to a new solution.
  - Often times, developers in a pairing have different skill sets
    - If one programmer is more experienced in a certain skill, they can teach a student who is less familiar with that area. 
      - less experienced developer benefits from the experienced developer’s knowledge and guidance
      - the more experienced developer benefits from explaining the topic in their own words, further solidifying their own understanding

4. **Social Skills**
  - Pair programming is great for improving social skills. 
  - When working with someone who has a different coding style, communication is key. 
    - can become more difficult when two programmers have different personalities 
  - Pair programming can also help programmers develop their interpersonal skills
  - Has long-term career impacts. 
    - **As much as employers want strong programmers, they know it’s essential to hire people who can work well with others.**

5. **Job Interview Readiness**
  - A common step in many interview processes involves pair programming between a current employee and an applicant, either in person or through a shared screen. 
    - Carry out exercises together, such as code challenges, building a project or feature, or debugging an existing code base. 
  - By doing so, companies can get a better feel for how an applicant will fit into the team and their collaboration style.
  - For most roles, the ability to work with and learn from others and stellar communication skills are as (or more) important to a company than specific technical skills

6. **Work Environment Readiness**
  - Many companies that utilize pair programing expect to train fresh hires from CS-degree programs on how they operate to actually deliver a product
  - Code Fellows graduates who are already familiar with how pairing works can hit the ground running at a new job

