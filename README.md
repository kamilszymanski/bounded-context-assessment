# The Bounded Context Assessment

***This tool is currently Experimental. All feedback, ideas, and testing are welcome and may be included in the official release with attribution.***

The Bounded Context Assessment is a toolkit for assessing the design quality of an individual and an entire domain portfolio of bounded contexts. The purpose of this toolkit is to:

- Compare multiple design alternatives and choose the best
- Identify how the design quality of a single bounded context affects the wider architecture

Currently, the Bounded Context Assessment contains 2 tools:

- Bounded Context Design Assessment (for assessing a single context)

![Bounded Context Design Assessment](/resources/bounded-context-assessment-example-basic.jpg)

- Bounded Context Portfolio Assessment (for visualizing the design scores of an entire portfolio and their relations.)

![Bounded Context Portfolio Assessment](/resources/bounded-context-portfolio-assessment-example.jpg)

## Bounded Context Design Assessment

The Bounded Context Design Assessment is used to create a assign a score from 0 - 5 for each major aspect of a design: Business, Domain, Social, Technical, User Experience (UX). The higher the score the better the design. Scores are for the design of a single bounded context, although a single diagram could be used to compare the scores of multiple design options.

The strategic classification of the bounded context (core, supporting, generic) will determine the criteria used to assign a score in each category.

### Business

How well does the design of this bounded context allow the business to build and sustain a competitive advantage?

- is high business differentiation decoupled from low differentiation?
- are supporting contexts no wider in scope than they need to be so that more effort can be applied to the core?
- are generic contexts outsourced where they can be and where there is no benefit to building in-house?

### Domain

How well does the design of this bounded context manage the complexity of the domain?

- Does this context align 1:1 with the ideal subdomain boundary?
- Would a business or domain expert understand the name and purpose of this context?
- What is the level of local complexity introduced by this context (how big and how complex are the domain rules and policies)?
- What is the level of global complexity introduced by this context (how many external dependencies and interactions)?

### Social

How well does the design of this bounded context enable teams to focus on learning the domain and solving business problems?

- Can this context be owned by a single team working normal working hours and not having to reduce the quality of their work?
- What is the level of cognitive load required to maintain this context?
- How much purpose, autonomy, and mastery will teams have working on this context?

### Technical

How well does the design of this bounded context minimise the amount of techical complexity needed to build and maintain the context?

- How much specialist or non-paved road technology is required to implement this context?
- How much technical complexity is required to integrate this context with other contexts?

### User Experience

How well does the design of this bounded context minimise negative impacts on the user experience or even improve the user experience?

- How much eventual consistency will the user face as a result of the design of this context?
- How much inconsistency into the UX will be introduced due to the design of this context?

## Bounded Context Portfolio Assessment

Designing bounded contexts is a trade-off. Simplifying one bounded context (local complexity) may add complexity in another bounded context or add extra complexity in the integration of bounded contexts (global complexity). The goal of designing a system is to provide the optimal design -- the design that leads to the most positive business outcomes.

The purpose of the Bounded Context Portfolio Assessment is to put the design trade-offs of each context into perspective to ensure that the system is optimised for producing maximum value in the core business domains.

### Insights

Here are a small example of the insights that can be gleaned from the portfolio assessment (feel free to submit a PR with any others you have discovered):

- When a core context has a bad design 
- When a core context depends on other contexts which have bad design (and thus may impact the core)
- When a high leverage context (a context with many clients) has a poor design, and thus it has the potentially to amplify it's negative effects by impacting a large number of contexts

> *Note*: The portfolio view may indicate a problem but it is usually necessary to dive in deeper and explore which part of the design is causing a problem. Equally, the portfolio view will not surface all problems. It may be necessary to create alternative views comparing more granular aspects of the design

## Contributions and Feedback

The Bounded Context Assessment is freely available for you to use. In addition, your feedback and ideas are welcome to improve the canvas or to create new versions. 

Feel free to also send us a pull request with your examples.

[![CC BY 4.0][cc-by-shield]][cc-by]

This work is licensed under a [Creative Commons Attribution 4.0 International
License][cc-by].

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg