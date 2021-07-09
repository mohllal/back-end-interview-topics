# Back-End Interview Topics

This repository contains a list of Back-End interview topics that I had to review, or want to deepen.

Feel free to contribute, it would be highly appreciated!

## Table of Contents

- [Programming Languages](#programming-languages)
  - [JavaScript](#javascript)
- [Frameworks](#frameworks)
  - [Node.js](#nodejs)
- [Object Oriented Programming](#object-oriented-programming)
- [Architectures](#architectures)
  - [Microservices](#microservices)
- [Design Patterns](#design-patterns)
- [Security](#security)
- [Databases](#databases)
  - [MySQL](#mysql)
  - [MongoDB](#mongodb)
  - [Redis](#redis)
  - [Kafka](#kafka)
- [Networking](#networking)
- [Infrastructure](#infrastructure)
  - [Docker](#docker)
  - [Nginx](#nginx)
  - [Kubernetes](#kubernetes)
- [Deployment](#deployment)
- [Git](#git)
- [Testing](#testing)
- [Data Structures and Algorithms](#data-structures-and-algorithms)
- [Agile](#agile)

### Programming Languages

#### JavaScript

- What are the *programming paradigms* supported by JavaScript?

- What is the difference between **classical inheritance** and **prototypal inheritance**?
  - [What’s the Difference Between Class & Prototypal Inheritance?](https://medium.com/javascript-scene/master-the-javascript-interview-what-s-the-difference-between-class-prototypal-inheritance-e4cd0a7562e9)

- What is **asynchronous programming**, and why is it important in JavaScript?

- What is **callback hell** and how can it be avoided? What is the point of Promises?
  - [What is a Promise?](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-promise-27fc71e77261)

- What is the difference between between **global scope**, and **local scope** (function scope, and block scope)?
  - [Scope: Local, Global and Lexical](https://medium.com/altcampus/scope-local-global-and-lexical-e164f53450b3)
  - [Scopes in JavaScript](https://towardsdatascience.com/still-confused-in-js-scopes-f7dae62c16ee)

- What is **hoisting**, and **IIFE**?
  - [Understanding Hoisting in JavaScript](https://scotch.io/tutorials/understanding-hoisting-in-javascript)
  - [JavaScript Execution Context and Hoisting](https://towardsdatascience.com/javascript-execution-context-and-hoisting-c2cc4993e37d?)

- What is **closures**? How to emulate **encapsulating** using it?
  - [What is a Closure?](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-closure-b2f0d2152b36)

- What are the different *patterns of function invocation* in JavaScript? And what is the value of `this` in each one them?
  - [JavaScript: Function Invocation Patterns](http://doctrina.org/Javascript-Function-Invocation-Patterns.html)

- What is the different between `.__proto__` and `.prototype`?
  - [JavaScript inheritance behind the scene](https://hackernoon.com/understand-nodejs-javascript-object-inheritance-proto-prototype-class-9bd951700b29)
  - [What is the difference between `prototype` and `__proto__` in JavaScript?](https://medium.com/javascript-in-plain-english/proto-vs-prototype-in-js-140b9b9c8cd5)

- How to change the context of functions using `.call()`, `.apply()`, or `.bind()`?
  - [How-to: `call()` , `apply()` and `bind()` in JavaScript](https://www.codementor.io/@niladrisekhardutta/how-to-call-apply-and-bind-in-javascript-8i1jca6jp)

- What do `Object.assign()` and `Object.create()` do?
  - [Object.create() and Object.assign()?](https://stackoverflow.com/questions/34838294/what-is-difference-between-creating-object-using-object-create-and-object-assi)

- What do `Promise.race()` and `Promise.all()` do?
  - [The Difference Between Promise.all and Promise.race in JavaScript](https://alligator.io/js/promise-all-promise-race/)

- What happens when we call a function with the `new` keyword?
  - [`new` operator](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/new)

- What is the output of this code:

  ```javascript
  for (var i = 0; i < 3; i++) {
      setTimeout(function() { console.log(i); }, 1000 + i);
  }
  ```

  What will be printed on the console if we change `var i` with `let i`?

- Consider the following code:

  ```javascript
  (function() {
      var a = b = 5;
  })();
  console.log(b);
  ```

  What will be printed on the console? If the *strict mode* was enabled by using the `'use strict';`, what will be the output?

- Define a `repeatify` function on the String object. The function accepts an integer that specifies how many times the string has to be repeated. The function returns the string repeated the number of times specified. For example:

  ```javascript
  console.log('hello'.repeatify(3));
  ```

  It should print `hellohellohello`.

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

Resources

- [5 Typical JavaScript Interview Exercises](https://www.sitepoint.com/5-typical-javascript-interview-exercises/)
- [JavaScript: Object Prototypes](http://doctrina.org/Javascript-Objects-Prototypes.html)
- [Tricky JavaScript Interview Questions](https://dmitripavlutin.com/simple-but-tricky-javascript-interview-questions/)
- [Floating Point Math](https://0.30000000000000004.com/)

**[[⬆]](#table-of-contents) return to TOC**

### Frameworks

#### Node.js

- Is everything that’s asynchronous in Node.js handled by the `libuv`'s Worker Pool?
  - [Don't Block the Event Loop (or the Worker Pool)](https://nodejs.org/en/docs/guides/dont-block-the-event-loop/)

- What are the **phases of the Event Loop**?
  - [Node.js event loop architecture](https://medium.com/preezma/node-js-event-loop-architecture-go-deeper-node-core-c96b4cec7aa4)

- What do you know about **Worker Threads** module in Node.js?
  - [Worker Threads](https://nodejs.org/api/worker_threads.html)

- What is the difference between `process.nextTick()`, `setTimeout()`, `setInterval()`, and `setImmediate()`?
  - [The Node.js Event Loop, Timers, and `process.nextTick()`](https://nodejs.org/en/docs/guides/event-loop-timers-and-nexttick/)

- What are the **Timers** functions of Node.js?
  - [Timers in Node.js](https://nodejs.org/en/docs/guides/timers-in-node/)

- What can be done if a **Timeout** or **Immediate** object needs to be *cancelled*?

- What will printed by running the following code:

  ```javascript
  const fs = require('fs');

  fs.readFile(__filename, () => {
    setTimeout(() => {
        console.log('timeout');
    }, 0);
    setImmediate(() => {
        console.log('immediate');
    });
    process.nextTick(() => {
        console.log('nextTick');
    });
  });
  ```

- Explain what is **Reactor Pattern** in Node.js?

- Rewrite the code sample without **try/catch** block:
  
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

- What is **Globals** in Node.js? (explain *global*, *process*, and *buffer*)
  - [Global Objects](https://nodejs.org/api/globals.html)

- What is the use of **Underscore (`_`)** in Node.js?
  - [Use of Underscore (_) in Node.js](https://www.codingdefined.com/2014/06/use-of-underscore-in-nodejs.html)

- What are **Error First Callbacks** in Node.js?

- How to **gracefully shutdown/kill** Node.js process? (explain `process.kill()`)

- What is the difference between `readFile()` vs `createReadStream()`?

- What is the `EventEmitter` in Node.js?
  - [Node.js event emitter explained](https://medium.com/technoetics/node-js-event-emitter-explained-d4f7fd141a1a)

- How many types of **Streams** are present in Node.js?

- How to solve **Process out of Memory Exception** in Node.js?
  
- What is the use of **DNS** module in Node.js?

- What's wrong with the following code snippet? *(explain [timing attacks](https://en.wikipedia.org/wiki/Timing_attack))*

  ```javascript
  function checkApiKey (apiKeyFromDb, apiKeyReceived) {
    if (apiKeyFromDb === apiKeyReceived) {
        return true
    }
    return false
  }
  ```

- How does Node.js support *multi-processor* platforms, and does it fully utilize all processor resources? (explain **Cluster** module)

- Consider the following code snippet:
  
  ```javascript
  {
    console.time("loop");
    for (var i = 0; i < 1000000; i += 1){
        // Do nothing
    }
    console.timeEnd("loop");
  }
  ```

Resources

- [7 Hardest Node.js Interview Questions](https://dev.to/fullstackcafe/7-hardest-nodejs-interview-questions--answers-3lje)
- [Top 20 Interview Questions on Node.js](https://www.codingdefined.com/2017/04/top-20-interview-questions-on-nodejs.html)
- [Frequently asked: Node JS Interview Questions and Answers](https://medium.com/@vigowebs/frequently-asked-node-js-interview-questions-and-answers-b74fa1f20678)
- [8 Essential Node.js Interview Questions](https://www.toptal.com/nodejs/interview-questions)
- [Node.js Interview Questions and Answers](https://blog.risingstack.com/node-js-interview-questions-and-answers-2017/)
- [Express and Node JS Interview Questions](https://www.onlineinterviewquestions.com/node-js-interview-questions/)

**[[⬆]](#table-of-contents) return to TOC**

### Object Oriented Programming

- What are the pros and cons of **functional programming** vs **object-oriented programming**?
- What are the four **pillars of OOP**? *(A brief description for each one)*
- What is dynamic or **run time polymorphism**?
- What is **static/early binding** and **dynamic/late binding**?
- When is **classical inheritance** an appropriate choice?
- When is **prototypal inheritance** an appropriate choice?
- What does **“favor object composition over class inheritance”** mean? When should we choose inheritance over composition?
- When it is more appropriate to use a *structure* (struct) instead of a *class*?
- What are **abstract classes**? What are the distinct characteristics of an abstract class?
- How is **method overriding** different from **method overloading**?
- What is the difference between **cohesion** and **coupling**?
- Why should we strive for **"high cohesion, and low coupling"** in designing a system?
- Explain the concept of **destructor/deinitializer**?
- What is LSP (**Liskov Substitution Principle**) and what are some examples of its use?
- What is the difference between **association**, **aggregation** and **composition**?

**[[⬆]](#table-of-contents) return to TOC**

### Architectures

#### Microservices
  
- What is the **Microservices** architecture? And what are its pros and cons?
- What are the differences between **Monolithic**, **SOA** and **Microservices**?
- What is the **API Gateway** pattern?
- What are the **decomposition patterns** used in Microservices? (briefly describe decomposition by **business capability**, decomposition by **subdomain**, and **self-contained** services)
- What are the **deployment strategies** used in Microservices?
- What are the *challenges* faced while working with Microservices?
- What is **Domain Driven Design (DDD)**?
- What is **Ubiquitous Language (UL)** and what is its uses in DDD?
- What is the **Distributed Transaction** pattern?
- What is the **Bounded Context** pattern?
- What do you understand by **Contract Testing**?
- What is **End to End Testing** in Microservices?
- What are **Reactive Extensions** in Microservices?

**[[⬆]](#table-of-contents) return to TOC**

### Design Patterns

**[[⬆]](#table-of-contents) return to TOC**

### Security

- What is **JSON** Web Token? And when to use it?
- What is the JSON Web Token *structure*? And How does it work?
- What is **OAuth 2.0**? What are its roles?
- What are the five grants for acquiring an access token in **OAuth 2.0**?

**[[⬆]](#table-of-contents) return to TOC**

### Databases

#### MySQL

- Suppose we have two tables `tbl1` and `tbl2`; Each of these tables contains one column on which join condition has been defined. The table `tbl1` contains the column `col1` and the table `tbl2` contains the column `col2`.
  
  - What will the outcome of the following **inner** join query?
  
  ```SQL
  SELECT a.col1, b.col2
  FROM tbl1 a INNER JOIN tbl2 b
  ON a.col1 = b.col2
  ```
  
  - What will the outcome of the following **left outer** join query?
  
  ```SQL
  SELECT a.col1, b.col2
  FROM tbl1 a LEFT OUTER JOIN tbl2 b
  ON a.col1 = b.col2
  ```
  
  - What will the outcome of the following **right outer** join query?
  
  ```SQL
  SELECT a.col1, b.col2
  FROM tbl1 a RIGHT OUTER JOIN tbl2 b
  ON a.col1 = b.col2
  ```
  
  - What will the outcome of the following **full outer** join query?
  
  ```SQL
  SELECT a.col1, b.col2
  FROM tbl1 a FULL OUTER JOIN tbl2 b
  ON a.col1 = b.col2
  ```

    In case of:
        - Join columns having **unique** values.
        - Join columns having **duplicate** values.
        - *One* Join table contains **Null** value.
        - *Both* tables containing **Null** values.

- Consider the following `staffs` table:
  
  | id  | first_name | last_name | manager_id |
  | --- | ---------- | --------- | ---------- |
  | 1   | Genna      | Jakson    | NULL       |
  | 2   | Adam       | Ahmed     | 1          |
  | 3   | Kali       | Boyer     | 2          |
  | 4   | Layla      | David     | 2          |
  | 5   | Ali        | Mohamed   | 3          |
  
  The `staffs` table stores the staff information such as `id`, `first_name`, and `last_name`. It also has a column named `manager_id` that specifies the direct manager.
  
  Use **self join** and **recursive common table expression (CTE)** to get who reports to whom?

- Describe and give an example of the **cross join**?

**[[⬆]](#table-of-contents) return to TOC**

#### MongoDB

**[[⬆]](#table-of-contents) return to TOC**

#### Redis

**[[⬆]](#table-of-contents) return to TOC**

#### Kafka

**[[⬆]](#table-of-contents) return to TOC**

### Networking

- What does the term **network topology** refer to? What are the different types of network topology? What are the pros and cons of each one?
  - Star Topology
  - Bus Topology
  - Ring Topology
  - Tree Topology
  - Mesh Topology
  - Hybrid Topology
- What are the layers of the **OSI model**? *(A brief description for each layer)*
  1. Physical Layer
  2. Data Link Layer
  3. Network Layer
  4. Transport Layer
  5. Session Layer
  6. Presentation Layer
  7. Application Layer
- What are the layers of the **TCP/IP model**? *(A brief description for each layer)*
  1. Physical Layer
  2. Data Link Layer
  3. Internet Layer
  4. Transport Layer
  5. Application Layer
- What are the differences between **IPv4** and **IPv6**?
- What are the differences between **TCP** and **UDP**?
- What are **DNS**, **DHCP**, and **NAT**?
- What is the difference between **DNAT (Destination Network Address Translation)** and **SNAT (Source Network Address Translation)** ?
- How does **tracert** or **traceroute** tool work?
- How do **content delivery networks (CDNs)** work?
- What are the differences between **reverse proxies** and **forward proxies**?
- What does the term **AAA** mean in network security?
- What is **DoS/DDoS** attack? How can protect servers from it?
- The age-old question: **What happens when you type google.com into your browser and press enter?**

Resources

- [What Is Network Topology?](https://www.dnsstuff.com/what-is-network-topology)
- [TCP/IP vs OSI Model: What's the Difference?](https://www.guru99.com/difference-tcp-ip-vs-osi-model.html)
- [IPv4 vs IPv6: What’s the Difference?](https://www.guru99.com/difference-ipv4-vs-ipv6.html)
- [TCP vs UDP: What's the Difference?](https://www.guru99.com/tcp-vs-udp-understanding-the-difference.html)
- [SNAT vs DNAT](https://ipwithease.com/snat-vs-dnat/)
- [How content delivery networks (CDNs) work](https://humanwhocodes.com/blog/2011/11/29/how-content-delivery-networks-cdns-work/)
- [What is Reverse Proxy Server](https://www.imperva.com/learn/performance/reverse-proxy/)
- [AAA](https://en.wikipedia.org/wiki/AAA_(computer_security))
- [What is a DDoS Attack?](https://www.cloudflare.com/learning/ddos/what-is-a-ddos-attack/)
- [What happens when you type google.com into your browser and press enter?](https://github.com/alex/what-happens-when)

**[[⬆]](#table-of-contents) return to TOC**

### Infrastructure

#### Docker

- What is **Docker**? What is the difference between **Docker** and **VM** (Virtual Machine)?
- What is the advantage of **Docker** over **Hypervisors**? (briefly describe What is the main difference between the approaches of *Docker* and *standard hypervisor* virtualization?)
- What is Docker **Image** and **Container**?
- How do Docker containers make use of kernel cgroups and namespaces?
- What is the default Docker **network driver**, and how can we change it when running a Docker image?
- What are the *four* different **restart policies** in Docker?
- What is **Docker Compose**? What can it be used for?
- What is **Docker Hub** and what is the other type of **Docker Image Registry**?
- What are the possible ways of using *insecure* Docker image registries?
- What is **Docker Swarm**? What can it be used for?
- What is **Dockerfile**? What can it be used for?
- Is there any *data loss* when the Docker *container exits*?
- Why `docker-compose down` may take `10` seconds to recreate or stop? (briefly describe `SIGTERM` and `SIGKILL`)
- What is the difference between `docker-compose up`, `docker-compose run`, and `docker-compose start`?
- What is the difference between `COPY` and `ADD` in a Dockerfile?
- What is the difference between Docker `ADD` command and `VOLUME` flag?
- What is the difference between the `docker run` and the `docker create`?
- What are the *various states* that a Docker container can be in at any given point in time?
- What is the preferred way of removing containers - `docker rm -f` or `docker stop` then followed by a `docker rm`?
- What does the volume parameter `-v` do in a `docker run` command?
- What is the use of the `docker save` and `docker load` commands?
- Is there any problem with just using the `latest` tag in a container orchestration environment? What is considered best practice for **image tagging**?

Resources

- [What is Docker?](https://docs.docker.com/get-started/overview/)
- [How is Docker different from a virtual machine?](https://stackoverflow.com/questions/16047306/how-is-docker-different-from-a-virtual-machine)
- [What is Container?](https://www.docker.com/resources/what-container)
- [Network containers](https://docs.docker.com/engine/tutorials/networkingcontainers/)
- [Use bridge networks](https://docs.docker.com/network/bridge/)
- [Use overlay networks](https://docs.docker.com/network/overlay/)
- [What is the difference between bridge network and overlay network?](https://stackoverflow.com/questions/40974299/what-is-the-difference-between-bridge-network-and-overlay-network)
- [Start containers automatically](https://docs.docker.com/config/containers/start-containers-automatically/)
- [Overview of Docker Compose](https://docs.docker.com/compose/)
- [Swarm mode overview](https://docs.docker.com/engine/swarm/)
- [Swarm mode key concepts](https://docs.docker.com/engine/swarm/key-concepts/)
- [Best practices for writing Dockerfiles](https://docs.docker.com/develop/develop-images/dockerfile_best-practices/)
- [Do I lose my data when the container exits?](https://docs.docker.com/engine/faq/#do-i-lose-my-data-when-the-container-exits)
- [Why do docker compose services take 10 seconds to recreate or stop?](https://docs.docker.com/compose/faq/#why-do-my-services-take-10-seconds-to-recreate-or-stop)
- [Trapping signals in Docker containers](https://medium.com/@gchudnov/trapping-signals-in-docker-containers-7a57fdda7d86)
- [Docker ADD vs VOLUME](https://stackoverflow.com/questions/27735706/docker-add-vs-volume)
- [What are the possible states for a docker container?](https://stackoverflow.com/questions/32427684/what-are-the-possible-states-for-a-docker-container)
- [Lifecycle of Docker Container](https://medium.com/@BeNitinAgarwal/lifecycle-of-docker-container-d2da9f85959)
- [Recommendations for tagging and versioning container images](https://docs.microsoft.com/en-us/azure/container-registry/container-registry-image-tag-version)
- [Understanding the Docker Internals](https://medium.com/@BeNitinAgarwal/understanding-the-docker-internals-7ccb052ce9fe)
- [Cgroups, namespaces, and beyond: what are containers made from?](https://www.youtube.com/watch?v=sK5i-N34im8&ab_channel=Docker)
- [PaaS under the hood, episode 1: kernel namespaces](https://web.archive.org/web/20150326185901/http://blog.dotcloud.com/under-the-hood-linux-kernels-on-dotcloud-part)

**[[⬆]](#table-of-contents) return to TOC**

#### Nginx

- What is nginx?
- What is C10K problem?
- Explain how Nginx can handle multiple connections within a single process?
- Does Nginx support compress the request to the upstream?

Resources

- [What is NGINX?](https://www.nginx.com/resources/glossary/nginx/)
- [C10k problem](https://en.wikipedia.org/wiki/C10k_problem)
- [Inside NGINX: How We Designed for Performance & Scale](https://www.nginx.com/blog/inside-nginx-how-we-designed-for-performance-scale/)
- [Tuning NGINX for Performance](https://www.nginx.com/blog/tuning-nginx/)
- [The Architecture of Open Source Applications: nginx](https://aosabook.org/en/nginx.html)
- [ngx_http_gunzip_module](https://nginx.org/en/docs/http/ngx_http_gunzip_module.html)
- [Nginx Interview Questions](https://www.courseya.com/nginx-interview-questions/)

**[[⬆]](#table-of-contents) return to TOC**

#### Kubernetes

**[[⬆]](#table-of-contents) return to TOC**

### Deployment

- What are the differences between continuous integration, continuous delivery, and continuous deployment?
- What is the difference between a Blue/Green deployment and a rolling deployment?
- What is the Canary deployment strategy?
- Explain how DevSecOps impacts on the CD pipeline?
- What is pipeline as code?

Resources

- [Continuous integration vs. continuous delivery vs. continuous deployment](https://www.atlassian.com/continuous-delivery/principles/continuous-integration-vs-delivery-vs-deployment)
- [Deployment Strategies Defined](http://blog.itaysk.com/2017/11/20/deployment-strategies-defined)
- [DevSecOps: Injecting Security into CD Pipelines](https://www.atlassian.com/continuous-delivery/principles/devsecops)
- [What is pipeline as code?](https://about.gitlab.com/topics/ci-cd/pipeline-as-code/)

**[[⬆]](#table-of-contents) return to TOC**

### Git

- What are the pros and cons of distributed version control systems like **Git** over centralized ones like **SVN**?
  - [Why is Git better than Subversion?](https://stackoverflow.com/questions/871/why-is-git-better-than-subversion)
  - [Should I use SVN or Git?](https://stackoverflow.com/questions/161541/should-i-use-svn-or-git/161572)

- What is Git fork? What is difference between **fork**, **branch** and **clone**?
  - [What are the differences between git branch, fork, fetch, merge, rebase and clone?](https://stackoverflow.com/questions/3329943/what-are-the-differences-between-git-branch-fork-fetch-merge-rebase-and-clon)

- What is the difference between `git pull` and `git fetch`?

- How to *revert previous commit* in git?
  - [Undo the most recent local commits in Git?](https://stackoverflow.com/questions/927358/how-do-i-undo-the-most-recent-local-commits-in-git)

- What is `git cherry-pick`?
  - [Git Cherry Pick](https://www.atlassian.com/git/tutorials/cherry-pick)

- What is the difference between **HEAD**, **working tree** and **index**, in Git?

- Explain the **Gitflow** workflow?
  - [Gitflow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)

- What is `git stash`? And when to use it?

- How to remove a file from git without removing it from the file system?

- How do you *find a list of files* that has changed in a particular commit?

- What is `git bisect`? How can you use it to determine the source of a (regression) bug?
  - [`git bisect`](https://git-scm.com/docs/git-bisect)

- When to use `git rebase` instead of `git merge`? What does the **interactive rebasing** do?
  - [When do you use `git rebase` instead of `git merge`?](https://stackoverflow.com/questions/804115/when-do-you-use-git-rebase-instead-of-git-merge)
  - [Merging vs. Rebasing](https://www.atlassian.com/git/tutorials/merging-vs-rebasing)

- What are the different ways we can use to refer to a commit?

Resources

- [11 Painful Git Interview Questions](https://www.codementor.io/@alexershov/11-painful-git-interview-questions-and-answers-you-will-cry-on-lybbrqhvs)
- [Essential Git Interview Questions](https://www.toptal.com/git/interview-questions)
- [Advanced Git Tutorials](https://www.atlassian.com/git/tutorials/advanced-overview)

**[[⬆]](#table-of-contents) return to TOC**

### Testing

- What is **Test Driven Development** (TDD)? And what is its process?

- What is **Data-Driven Development** (DDD)? And what is its process?

- What is **Keyword Driven Development** (KDD)? And what is its process?

- What is **Behavior Driven Development** (BDD)? And what is its process?

- What is the difference between **Fake**, **Mock**, and **Stub**?
  - [Mocks Aren't Stubs](https://www.martinfowler.com/articles/mocksArentStubs.html)
  - [The difference between faking, mocking, and stubbing?](https://stackoverflow.com/questions/346372/whats-the-difference-between-faking-mocking-and-stubbing)

- What are the various *types of Unit Testing*?
  - [State vs Interaction Based Testing](http://www.natpryce.com/articles/000342.html)

- What do you know about **Mike Cohn’s Test Pyramid**?
  
- What is **Code Coverage**? And what are its various techniques?
  - [What is code coverage?](https://stackoverflow.com/questions/195008/what-is-code-coverage-and-how-do-you-measure-it)
  - [Pitfalls of code coverage](https://stackoverflow.com/questions/695811/pitfalls-of-code-coverage/695888)

- How is *Unit Testing* different from *Integration Testing*?
  - [Difference between Unit Testing and Integration Testing?](https://www.softwaretestingclass.com/what-is-difference-between-unit-testing-and-integration-testing/)

Resources

- [Unit Testing Interview Questions and Answers](https://www.janbasktraining.com/blog/unit-testing-interview-questions/)
- [The 100% Code Coverage Myth](https://hackernoon.com/the-100-code-coverage-myth-900b83d20d3d)
- [Code Coverage: The Metric That Makes Your Tests Worse](https://medium.com/@AikoPath/code-coverage-the-metric-that-makes-your-tests-worse-c1dddcc0831)
- [5 Questions Every Unit Test Must Answer](https://medium.com/javascript-scene/what-every-unit-test-needs-f6cd34d9836d)
- [Behavior-Driven Development and Test-Driven Development](https://medium.com/swlh/behavior-driven-development-and-test-driven-development-ef9f406db542)
- [The Value at the Intersection of TDD, DDD, and BDD](https://medium.datadriveninvestor.com/the-value-at-the-intersection-of-tdd-ddd-and-bdd-da58ea1f3ac8)

**[[⬆]](#table-of-contents) return to TOC**

### Data Structures and Algorithms

- What is the difference between **static array** and **dynamic array**?
- Compare the *time complexity* and *space complexity* of *searching*, *insertion*, and *deletion* for the following data structures:
  - **Dynamic Array**
  - **Linked List**
  - **Hash Table (Hash Map)**
  - **Binary Search Tree (BST)**
  - **Heap (Max Heap/Min Heap)**
  - **Red-Black Tree**
  - **AVL Tree**
- Compare the time complexity and *space complexity* for the following sorting algorithms:
  - **Bubble Sort**
  - **Insertion Sort**
  - **Selection Sort**
  - **Merge Sort**
  - **Heap Sort**
  - **Quick Sort**
  - **Counting Sort**
- What is the difference between **inorder**, **preorder**, and **postorder** tree traversal algorithms?
- What is the difference between **breadth-first-search (BFS)** and **depth-first-search (DFS)**?

**[[⬆]](#table-of-contents) return to TOC**

### Agile

- What is the *Agile Software Development* standing for? And why we should use it!
- What is the difference between the **Agile** and **Waterfall** software development models?
- What is the *four main principles* of the Agile Software Development? (**Agile Manifesto**)
- How does *Agile* work?
- List some Agile software development (or system development) **methodologies**?
- What is the difference between **Kanban** and **Scrum** *Agile* frameworks?
- What is the duration of a *Scrum sprint*?
- What is the **Scrum of Scrums**?
- What is the term **increment** standing for, in Scrum context?
- Explain the **scrum poker**/**planning poker** technique?
- What is the **Release candidate**?
- What is a **story point** in the Scrum?
- What are the *main roles* in the Scrum?
- What are the **Sprint Planning** meeting, **Stand-up** meeting, **Definition of Done (DoD)** meeting, and **Sprint Retrospective** meeting?

**[[⬆]](#table-of-contents) return to TOC**
