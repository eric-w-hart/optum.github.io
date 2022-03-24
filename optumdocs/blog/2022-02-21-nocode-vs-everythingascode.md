---
title: Low-code / No-code vs Everything as Code
author: Russ Rogers
author_title: Senior Principal Software Engineer
author_url: https://www.linkedin.com/in/russ-rogers-b0393b3
author_image_url: https://github.optum.com/avatars/u/16114?s=460&u=1774dbe0a390875fce76767e8c1856df3f69064f
tags: [Engineering, Low-code, no-code, engineering culture]
hide_table_of_contents: false
---

Low-code / No code systems are touted as faster ways to do development but it's important to understand what they do well and to avoid the shortcuts that bypass good engineering practices.

Let's clarify what "no code" is. These systems allow coding in a declarative "configuration" rather than a traditional programming language. These configurations may take the form of JSON, YAML, XML, properties files, or proprietary formats. They work to simplify the coding tasks by eliminating some of the complications of syntax, module structure, constructs like functions, flow control, and variables. I include Domain Specific Languages in here as well. Nevertheless, when these configurations are interpreted at runtime, the result is a "program". Programming languages, whether compiled or interpreted, are themselves simplifications on top of lower-level machine instructions. It's a matter of how much abstraction vs. control provided to the user.

Conversely, "everything as code" emphasizes the idea that most aspects of a system benefit from the same treatment as traditional "source code". This includes the deployment of the infrastructure, application configurations, automated code deployment, and testing / validation. There are also some process elements like version control, release management, and code reviews that should be considered as part of an "everything as code" philosophy too.

These are not incompatible paradigms. Terraform configurations are a form of "low code" for infrastructure specification.

### Expanding the pool of "developers"

By enabling SMEs in particular subject areas to provide input directly as "executable", they can eliminate a step in the translation of the specification into the instantiation of a solution. It may also enable use of lower-cost resources, providing a way of scaling out development work.

### Don't skip good engineering practices

With the inclusion of non-engineering members into the development process, it's important NOT to also throw out engineer practice when using a low-code/no-code solution. When "no code" is touted for its "speed", there can be pressure to loosen process controls at the same time, especially if they are not part of the team's development culture.

#### Version Control

Because the configurations are often text-based, they work well in version control systems, allow for differencing, versioning, and structured collaboration. Release planning, branching, and change management, etc are still valuable regardless of the programming environment. It can serve as a central knowledge store for process control audits.

#### Code reviews

In good engineering practice, a code developer makes a change and submits a request (PR) for the change to be accepted. The change is reviewed and may require "approval" by someone other than the original developer, to catch unintended issues and enforce coding standards. This is true whether the change is C++ code or a no-code configuration file.

#### Unit and Integration Testing

The ability to build tests to verify that the code works as expect is an important tenant of agile development. It may not be applicable in all cases, especially where the systems to not support reuse but it should not be discarded out of hand.

#### Deployment

Automated, hands-off deployments, especially to production environments, is a good way to ensure rigorous progress has been followed and avoid unintended changes making their way into production. Again, this can be important for audits.

### Take-aways

Don't skip good engineering practices when employing a low-code/no-code solution. Think about the "no code" configuration as another piece of the "everything as code" ecosystem and be sure the "non-coders" on your team understand the benefits of good engineering. If you're already using Terraform, you have a no-code / low-code component in your stack and you'd never consider not using the good practices above for that piece of your application.
