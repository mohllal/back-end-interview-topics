# Back-End Interview Topics

This repository contains a list of Back-End interview topics that I had to review, or want to deepen.

Feel free to contribute, it would be highly appreciated!

## <a name="toc">Table of Contents</a>

- [Programming Languages](#languages)
  - [JavaScript](#javascript)
- [Node.js](#nodejs)
- [Object Oriented Programming (OOP)](#oop)
- [Networking](#networking)
- [Architectures and Design Patterns](#architecture):
  - [Microservices](#microservices)
- [SQL](#sql)
- [Security](#security)
- [Git](#git)
- [Testing](#testing)
- [Data Structures and Algorithms](#dataStructure-algorithm)
- [Scrum](#scrum)

### <a name="languages">Programming Languages</a>

- <a name="javascript">JavaScript</a>:
  
  - What are the *programming paradigms* supported by JavaScript?
  
  - What is the difference between ***classical inheritance*** and ***prototypal inheritance***?
  
  - What is ***asynchronous programming***, and why is it important in JavaScript?
  
  - What is the difference between between ***global scope***, and ***local scope*** (function scope, and block scope)?
  
  - What is ***hoisting***, and ***IIFE***?
  
  - What is ***closures***? How to emulate ***encapsulating*** using it?
  
  - What are the different *patterns of function invocation* in JavaScript? And what is the value of `this` in each one them?
  
  - What is the different between `.__proto__` and `.prototype`?
  
  - How to change the context of functions using `.call()`, `.apply()`, or `.bind()`?
  
  - What happens when we call a function with the `new` keyword?
  
  - Consider the following code:

    ```javascript
    (function() {
        var a = b = 5;
    })();
    console.log(b);
    ```

    What will be printed on the console? If the *strict mode* was enabled using `'use strict';`, what will be the output?
  
  - Define a `repeatify` function on the String object. The function accepts an integer that specifies how many times the string has to be repeated. The function returns the string repeated the number of times specified. For example:

    ```javascript
    console.log('hello'.repeatify(3));
    ```

    It should print hellohellohello.
  
  - What is the result of the following code snippets?

    ```javascript
    var fullname = 'John Doe';
    var obj = {
        fullname: 'Colin Ihrig',
        prop: {
            fullname: 'Aurelio De Rosa',
            getFullname: function() {
                return this.fullname;
            }
        }
    };
    console.log(obj.prop.getFullname());

    var test = obj.prop.getFullname;
    console.log(test());
    ```

    ```javascript
    const obj1 = {
        value: 'hi',
        print: function() {
            console.log(this);
        },
    };

    const obj2 = { value: 17 };

    obj1.print.call(obj2);
    new obj1.print();
    ```

**[[⬆]](#toc) return to Table of Contents**

### <a name="nodejs">Node.js</a>

- Is everything that’s asynchronous in Node.js handled by the `libuv`'s Thread Pool?

- What are the ***phases of the Event Loop***?

- What is ***callback hell*** and how can it be avoided?

- What are the ***Timers*** functions of Node.js?

- Explain what is ***Reactor Pattern*** in Node.js?

- What is the difference between `process.nextTick()` `setTimeout()`, and `setImmediate()`?

- Rewrite the code sample without ***try/catch*** block:
  
  ```javascript
  async function check(req, res) {
    try {
        const a = await someOtherFunction();
        const b = await somethingElseFunction();
        res.send("result")
    } catch (error) {
        res.send(error.stack);
    }
  }
  ```

- What is ***Globals*** in Node.js? (explain *global*, *process*, and *buffer*)
- What is the use of ***Underscore (`_`)*** in Node.js?
- What are ***Error First Callbacks*** in Node.js?
- How to ***gracefully shutdown/kill*** Node.js process? (explain `process.kill()`)
- What is the difference between `readFile()` vs `createReadStream()`?
- What is the `EventEmitter` in Node.js?
- How many types of ***Streams*** are present in Node.js?
- How to solve ***Process out of Memory Exception*** in Node.js ?

**[[⬆]](#toc) return to Table of Contents**

### <a name="languages">Object Oriented Programming (OOP)</a>

- What are the pros and cons of ***functional programming*** vs ***object-oriented programming***?
- What are the four ***pillars of OOP***? *(A brief description for each one)*
- What is dynamic or ***run time polymorphism***?
- What is ***static/early binding*** and ***dynamic/late binding***?
- When is ***classical inheritance*** an appropriate choice?
- When is ***prototypal inheritance*** an appropriate choice?
- What does ***“favor object composition over class inheritance”*** mean? When should we choose inheritance over composition?
- When it is more appropriate to use a *structure* (struct) instead of a *class*?
- What are ***abstract classes***? What are the distinct characteristics of an abstract class?
- How is ***method overriding*** different from ***method overloading***?
- What is the difference between ***cohesion*** and ***coupling***?
- Why should we strive for ***"high cohesion, and low coupling"*** in designing a system?
- Explain the concept of ***destructor/deinitializer***?
- What is LSP (***Liskov Substitution Principle***) and what are some examples of its use?
- What is the difference between ***association***, ***aggregation*** and ***composition***?

**[[⬆]](#toc) return to Table of Contents**

### <a name="networking">Networking</a>

- What does the term ***network topology*** refer to? Describe the star topology and its cons?
- What are the layers of the ***OSI*** reference model? *(A brief description for each layer)*
- What are the layers of the ***TCP/IP model***? *(A brief description for each layer)*
- What are the differences between ***IPv4*** and ***IPv6***?
- What are the differences between ***TCP*** and ***UDP***?
- What are ***DNS***, ***DHCP***, and ***NAT***?
- What does the ***tracert*** tool (Windows) or the ***traceroute*** tool (Linux) do?
- What are ***CDNs***? What are its pros and cons?
- What are the differences between ***reverse proxies*** and ***forward proxies***?
- What does the term ***AAA*** mean in network security?
- What is ***DoS/DDoS***? How can protect servers from it?

**[[⬆]](#toc) return to Table of Contents**

### <a name="architecture">Architectures and Design Patterns</a>

- <a name="microservices">Microservices Architecture</a>:
  
  - What is the ***Microservices*** architecture? And what are its pros and cons?
  - What are the differences between ***Monolithic***, ***SOA*** and ***Microservices***?
  - What is the ***API Gateway*** pattern?
  - What are the ***decomposition patterns*** used in Microservices? (briefly describe decomposition by ***business capability***, decomposition by ***subdomain***, and ***self-contained*** services)
  - What are the ***deployment strategies*** used in Microservices?
  - What are the *challenges* faced while working with Microservices?
  - What is ***Domain Driven Design (DDD)***?
  - What is ***Ubiquitous Language (UL)*** and what is its uses in DDD?
  - What is the ***Distributed Transaction*** pattern?
  - What is the ***Bounded Context*** pattern?
  - What do you understand by ***Contract Testing***?
  - What is ***End to End Testing*** in Microservices?
  - What are ***Reactive Extensions*** in Microservices?

**[[⬆]](#toc) return to Table of Contents**

### <a name="sql">SQL</a>

- Suppose we have two tables `tbl1` and `tbl2`; Each of these tables contains one column on which join condition has been defined. The table `tbl1` contains the column `col1` and the table `tbl2` contains the column `col2`.
  
  - What will the outcome of the following ***inner*** join query?
  
  ```SQL
  SELECT a.col1, b.col2
  FROM tbl1 a INNER JOIN tbl2 b
  ON a.col1 = b.col2
  ```
  
  - What will the outcome of the following ***left outer*** join query?
  
  ```SQL
  SELECT a.col1, b.col2
  FROM tbl1 a LEFT OUTER JOIN tbl2 b
  ON a.col1 = b.col2
  ```
  
  - What will the outcome of the following ***right outer*** join query?
  
  ```SQL
  SELECT a.col1, b.col2
  FROM tbl1 a RIGHT OUTER JOIN tbl2 b
  ON a.col1 = b.col2
  ```
  
  - What will the outcome of the following ***full outer*** join query?
  
  ```SQL
  SELECT a.col1, b.col2
  FROM tbl1 a FULL OUTER JOIN tbl2 b
  ON a.col1 = b.col2
  ```

    In case of:
        - Join columns having ***unique*** values.
        - Join columns having ***duplicate*** values.
        - *One* Join table contains ***Null*** value.
        - *Both* tables containing ***Null*** values.

- Consider the following `staffs` table:
  
  | id  | first_name | last_name | manager_id |
  | --- | ---------- | --------- | ---------- |
  | 1   | Genna      | Jakson    | NULL       |
  | 2   | Adam       | Ahmed     | 1          |
  | 3   | Kali       | Boyer     | 2          |
  | 4   | Layla      | David     | 2          |
  | 5   | Ali        | Mohamed   | 3          |
  
  The `staffs` table stores the staff information such as `id`, `first_name`, and `last_name`. It also has a column named `manager_id` that specifies the direct manager.
  
  Use ***self join*** and ***recursive common table expression (CTE)*** to get who reports to whom?

- Describe and give an example of the ***cross join***?

**[[⬆]](#toc) return to Table of Contents**

### <a name="security">Security</a>

- What is ***JSON*** Web Token? And when to use it?
- What is the JSON Web Token *structure*? And How does it work?
- What is ***OAuth 2.0***? What are its roles?
- What are the five grants for acquiring an access token in ***OAuth 2.0***?

**[[⬆]](#toc) return to Table of Contents**

### <a name="git">Git</a>

- What is Git? And what it is used for?
- What are the pros and cons of distributed version control systems like ***Git*** over centralized ones like ***SVN***?
- What is Git fork? What is difference between ***fork***, ***branch*** and ***clone***?
- What is the difference between ***"git pull"*** and ***"git fetch"***?
- How to *revert previous commit* in git?
- What is ***"git cherry-pick"***?
- What is the difference between ***HEAD***, ***working tree*** and ***index***, in Git?
- Explain the ***Gitflow*** workflow?
- What is ***"git stash"***? And when to use it?
- How to remove a file from git without removing it from the file system?
- When to use ***"git rebase"*** instead of ***"git merge"***?

**[[⬆]](#toc) return to Table of Contents**

### <a name="testing">Testing</a>

- What is ***Test Driven Development*** (TDD)? And what is its process?
- What is ***Data-Driven Development*** (DDD)? And what is its process?
- What is ***Keyword Driven Development*** (KDD)? And what is its process?
- What is ***Behavior Driven Development*** (BDD)? And what is its process?
- What is the difference between ***Mock*** or ***Stub***?
- What do you know about ***Mike Cohn’s Test Pyramid***?

**[[⬆]](#toc) return to Table of Contents**

### <a name="dataStructure-algorithm">Data Structures and Algorithms</a>

- What is the difference between ***static array*** and ***dynamic array***?
- Compare the *time complexity* and *space complexity* of *searching*, *insertion*, and *deletion* for the following data structures:
  - ***Dynamic Array***
  - ***Linked List***
  - ***Hash Table (Hash Map)***
  - ***Binary Search Tree (BST)***
  - ***Heap (Max Heap/Min Heap)***
  - ***Red-Black Tree***
  - ***AVL Tree***
- Compare the time complexity and *space complexity* for the following sorting algorithms:
  - ***Bubble Sort***
  - ***Insertion Sort***
  - ***Selection Sort***
  - ***Merge Sort***
  - ***Heap Sort***
  - ***Quick Sort***
  - ***Counting Sort***
- What is the difference between ***inorder***, ***preorder***, and ***postorder*** tree traversal algorithms?
- What is the difference between ***breadth-first-search (BFS)*** and ***depth-first-search (DFS)***?

**[[⬆]](#toc) return to Table of Contents**

### <a name="scrum">Scrum</a>

- What is the *Agile Software Development* standing for? And why we should use it!
- What is the difference between the ***Agile*** and ***Waterfall*** software development models?
- What is the *four main principles* of the Agile Software Development? (***Agile Manifesto***)
- How does *Agile* work?
- List some Agile software development (or system development) ***methodologies***?
- What is the difference between ***Kanban*** and ***Scrum*** *Agile* frameworks?
- What is the duration of a *Scrum sprint*?
- What is the ***Scrum of Scrums***?
- What is the term ***increment*** standing for, in Scrum context?
- Explain the ***scrum poker***/***planning poker*** technique?
- What is the ***Release candidate***?
- What is a ***story point*** in the Scrum?
- What are the *main roles* in the Scrum?
- What are the ***Sprint Planning*** meeting, ***Stand-up*** meeting, ***Definition of Done (DoD)*** meeting, and ***Sprint Retrospective*** meeting?

**[[⬆]](#toc) return to Table of Contents**
