# AgileGuide
My take on how to run an Agile team

The purpose of the doc is to provided a step by step outline how to mange the SDLC via Salesforce. 

To utilize the table of contents, click the hamburger next to the line count


# Intro

# 1. What is Waterfall? 
Waterfall is exactly as it says, a linear and constant flow. When developing with Waterfall, things tend to be more stringent. Testers do not see the end product until it is 100% done. Waterfall leads to bureaucracy hold ups, flow bug fixes, and tends to stick to the initial design, no matter what.  

The core principal of waterfall is following the steps outlined at the begining of the development process. [This diagram illustrates the flow](https://lucid.app/lucidchart/0075636a-267f-4d14-93f5-4e4f53dba908/edit?page=0_0&invitationId=inv_a86c91a3-9f9b-47e8-b54c-99868ea6e6e7#)

The main attraction to waterfall is the clear answer for legacy systems and processes. Waterfall makes its name when things are easily predicatble and constant. Every step of the way is followed to a tee. The key to success in waterfall is properly outlining the requirements in advance. Because everything is locked into place once a step begins, errors occur when there is no SME for the system. 

Waterfall has traditionally been used by Governments and Financial Institutions because of the clear cut requirements and consistent tech stack. Utilizing the same systems, with the same constraints, for the same clients, allows for waterfall to flow. 

# 2. Where does Waterfall need some help?
What makes waterfall fall short is when things are not as clear. 

For example, if we are developing a new solution with a new product from Salesforce. This product has some documentation and examples from Salesforce, but the team is completely new to creating a solution with the product. 

If this new product does not work EXACTLY as we expect, waterfall begins to fail. Since the project was scoped out 6 months prior based on this product, we cannot create changes as the entire flow is dependent. If the product has idiosyncrasies we did not account for, the development process can be immediately thrown out of whack. 

The burden then falls on the development team to respond quickly to find a solution. This usually means late nights and weekends in order to stay on the timeline proposed to the customer. 

If there is any level of ambiguity in the development work, Waterfall is almost guaranteed to cause greater issues than it solves


# 3. What is Agile?
Agile is a method developed to overcome the pitfalls of waterfall's immutable nature. Agile focuses on the people and how they interact, rather than sticking to a stringent design document. 

1. The core pillars of Agile are:
Our highest priority is to satisfy the customer
through early and continuous delivery
of valuable software.

2. Welcome changing requirements, even late in
development. Agile processes harness change for
the customer's competitive advantage.

3. Deliver working software frequently, from a
couple of weeks to a couple of months, with a
preference to the shorter timescale.

4. Business people and developers must work
together daily throughout the project.

5. Build projects around motivated individuals.
Give them the environment and support they need,
and trust them to get the job done.

6. The most efficient and effective method of
conveying information to and within a development
team is face-to-face conversation.

7. Working software is the primary measure of progress.

8. Agile processes promote sustainable development.
The sponsors, developers, and users should be able
to maintain a constant pace indefinitely.

9. Continuous attention to technical excellence
and good design enhances agility.

10. Simplicity--the art of maximizing the amount
of work not done--is essential.

11. The best architectures, requirements, and designs
emerge from self-organizing teams.

12. At regular intervals, the team reflects on how
to become more effective, then tunes and adjusts
its behavior accordingly.

Agile sees its biggest boost in regards to more forward thinking solutions. Agile can be broken down as granular as day by day. Although this can lead to tedium, if properly scoped, it allows for the developer teams to respond to new issues in a way that is conducive.

Using the same example from above: we are developing a new solution with a brand new Salesforce product. 

As we go through development, we realize that a business requirement is missing from the current solution. In agile, as things change, our delivery date and process also may change. If we need an extra day to add the missing requirements, agile allows for this. In waterfall, we may not even notice the missing requirement until testing has begun. 

Agile is all about communication. The entire team needs to communicate during the end-to-end process. If the conversation remains open, the business can call out things to be quickly changed and the product owners are aware of every step we take. Waterfall often silos these processes so that the product owner may not see anything until testing or review, long after the changes could have been made. 


# 4. Where does Agile fall short? 
Agile fails from a few different reasons. Two common issues are 1. a lack of strong technical leadership and 2. a lack of communication with the business. 

Without a strong sense of guidance and leadership from the technical team, solutions do not properly get scoped. Agile's "Just in time" mentality can lead to a infinite loop of development. We need to deliver products without wasting time, but we also need to scope them out. We may not have a hard due date, but we constantly need one more day. 

Example:

Scenario: Our project runs on 3 week sprints. We do a daily checkin with the product owners and developers to track the progress of our solutions. During these calls, we review code and the previous days progress. Recently, the client has been mentioning that we are missing every single deadline, development days are running long, and they are unhappy. During the calls, the technical lead asks the developers for updates, and they consistently say things are "almost done" or "done" even if they are not. The team has been using Agile since its inception, but recently has been failing to deliver conistent products. 

Explanation: 

The above scenario is something that occurs when there is no clear leader. The team needs direction and architecture provided to build on. When the projects are not scoped ahead of time, the discovery process can be never ending. 

To overcome these issues, it is essential for the architect of the team to create proof of concepts and conceptual designs at least **ONE SPRINT AHEAD**. If the architect is always one sprint ahead, they can get in front of technical limitations.

It comes down to communication. If the team is not able to freely and openly communicate, things get missed. The product owners need to be comfortable in a technical environment and communicating around technical topics. They do not need to write code, but should at least understand what an API is and how it works. 

# Agile vs Waterfall Examples


A team is developing a chatbot using Salesforce. The team knows that the bots can be natively integrated to websites, but they do not know how to pass data from SAP back to Salesforce using the built in funtionalty. The documentation calls out the ability to do this, but is not clear how to go about implementation. 

**Agile:**
In the sprint before starting the bot coding, the architect creates a dummy third party site and a local server to host the website on. He then hard codes site variables and moves through accessing them via nodeJS. After this, he tests the various methods he knows to provide SF the data. After further deliberation, he realizes what needs to be done and is able to pass the values. Had this not been possible in the sprint, the team could either adjust the business requirements, adjust the ask, or continue working towards a solution. Development was not impacted as we found this issue before it occured for the developers. If we needed, we could bring in other tasks to fill in the missing work. 

**Waterfall:**
Prior this year, we met with the business and decided projects we will take on this year. During that time, we decided that a chatbot would be part of the roadmap, to be delivered on a given date of the year. We quickly create a basic design that says the data will flow from our site to the chatbot, and the response from the agent will also be returned. We know what data we _probably_ need. We at least kind of guess how it should look based on experience. Since we never did a proof of concept, we are unaware of any issues that may occur from passing the data. We are guessing this will be two days worth of work, completely able to be handled in one sprint.  

As we go to develop, we run into the issues the first team found during discovery. Because we did not account for these issues arising, we are already behind in delivery. The developers work 60+ hour weeks to overcome this which leads to burnout and coding errors which we dont find until testing. 

Once the chatbot "works", we test it. During testing, we run into new bugs that were not considered. These new bugs are now piled on top of the next set of development, but because we are static, and the cycle repeats. 


