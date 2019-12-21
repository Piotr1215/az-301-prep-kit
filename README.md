# AZ-301 exam preparation kit

<img src="https://docs.microsoft.com/en-us/media/learn/certification/badges/microsoft-certified-expert-badge.svg" alt="Exam badge" width="200"/>

This repo is part of preparation for **Microsoft Certified: Azure Solutions Architect Expert**, you can find second part, preparation for AZ-300 [here](https://github.com/Piotr1215/az-300-prep-kit).

You can clone this repo and mark your progress. If you want use this repo as a starter for your learning process you will need to reset the state of checkboxes. Currently most are marked as done, but you can easily do search and replace in your editor of choice (search for \[x] and replace with [ ], notice there is space between empty brackets).

Feel free to fork or submit PR, but please stick to the format.

I took a slightly different approach compared to creating learning notes for AZ-300. On top of adding just links, I also started adding my own notes and observations, so the repo will continue to evolve as I learn more about Azure and add my experience and hopefully you dear reader might add yours too.

## Content & Learning Progress

Exam curriculum is based on material update from __December 4, 2019.__. There is also a file in [resources folder](/resources/README.md) that contains unorganized useful information gathered during learning process that needs to be **memorized** or is known to be needed to answer questions.

See below announcement from exam page:

> Exam AZ-301: Microsoft Azure Architect Design
> The content of this exam was updated on __December 4, 2019.__ Please download the Skills measured document below to see what changed.

* [x] [Determine workload requirements (10-15%)](/1-workload-requirements/README.md)

* [x] [Design for identity and security (20-25%)](/2-identity-&-security/README.md)

* [x] [Design a data platform solution (15-20%)](/3-data-platform/README.md)

* [x] [Design a business continuity strategy (15-20%)](/4-business-continiuty/README.md)

* [x] [Design for deployment, migration, and integration (10-15%)](/5-deploy-migrate-integrate/README.md)

* [x] [Design an infrastructure strategy (15-20%)](/6-infrastructure/README.md)

## Resources

This exam is different than AZ-300, it has no labs and questions are geared towards design and architecture best practices in Azure rather than concrete implementaitons. Still, it's important to  practice yourself in the portal, but not as essencial as for AZ-300.

Resources also contain recommendations how to make best use of each one. At least this was how I was using each resource and it yielded good results.

### _Resources are ordered from used **least** often to used **most** often (please note that this is purely subjective on my part and something else might work better for you)_

1. [Video from MS Ignite with tips on taking the exam](https://myignite.techcommunity.microsoft.com/sessions/78629?source=sessions)

    **How to use:** watch one time to understand exam requirements and learn about varioius tips and tricks.

2. [Cloud Design Patterns](https://docs.microsoft.com/en-us/azure/architecture/patterns/)

    **How to use:** use as support resource if you want to know more about any given topic.

3. [Azure Architecture Center](https://docs.microsoft.com/en-gb/azure/architecture/)

    **How to use:** if you are interested in learning more about given topic, look it up on the architecture center and study.

4. [Self paced Azure labs](https://www.microsoft.com/HandsOnLabs/SelfPacedLabs)

    **How to use:** perform labs and/or read the documentation: Links are scattered across README files.

5. [Azure Tips and Tricks Youtube playlist curated by Microsoft](https://www.youtube.com/playlist?list=PLLasX02E8BPCNCK8Thcxu-Y-XcBUbhFWC)

    **How to use:** choose videos you are interested in and watch, most of the videos are very short and have enought info to help you understand the topic.

6. [Plularsight Courses](https://app.pluralsight.com/paths/certificate/microsoft-azure-architect-design-az-301)

    **How to use:** View while learning certain topic: Links to videos from Plularsight are scattered across README files or watch on demand.

7. [LinkedIn Learning](https://www.linkedin.com/learning/me)

    **How to use:**

    * There are plenty of detailed short videos describing many topics needed to pass the exam in detail.

    * You will need to start free month with LinkedIn, but you can cancell afterwards

    * Search topic you are interested in (copy/paste from exam topics) and watch videos

    * Content is detailed and almost always has a lot of Azure Portal print screens

8. [Udemy "AZ-301 Azure Architect Design Exam Prep" by Scott Duffy](https://www.udemy.com/course/az301-azure/)

    **How to use:** Watch relevant section and try to follow along on Azure Portal.

9. [Azure Landing Page](https://azure.microsoft.com/en-ca/)

    **How to use:**

    * This is main resource I was working with most of the time

    * Select "Products" and what you want to learn about. From there you will have access to full documentation and other areas. I highly recommend checking out the "Pricing" section as well as "FAQ", they both contain information useful during the exam.

        ![Products](https://raw.githubusercontent.com/Piotr1215/azure-architect-exams-resources/master/use-azure-portal.png)

    * Another very useful resource are Solutions -> Solution Architectures. This gives you a good overview how reference architectures are setup on Azure and helps a lot with the exam. Some of them have even source code and ARM templates on GitHub as well as Visio and other diagrams to help better understand the solution. For example, it's much easier to learn about Web Apps with a [reference architecture to play with](https://docs.microsoft.com/en-gb/azure/architecture/reference-architectures/app-service-web-app/basic-web-app).

        ![Solutions](https://github.com/Piotr1215/azure-architect-exams-resources/blob/master/azure-reference-architectures.png?raw=true)

10. This repo of course :). Use GitHub search functionality to find quickly what you need or simply navigate through README files.

## Exam preparation tips

### #1: Understand exam structure

Az-300 is focusing on practical usecases of Azure technologies. Exam has following characteristics:

1. Questions: 40-60 questions

   * Some questions are worth 1 point

   * Some questions cannot be skipped

   * There are different types of questions: multiple-choice, build list, hot area, drag and drop, reorder etc

   * There are also Performance based questions (labs) to be done in Azure portal

   * Questions are often in context of Case Studies where you need to gather and understand information across multiple sources

2. Duration: 3,5 hours

   * Schedule 30 minutes for reading and understangin instructions and rest for actal exam.

   * Take your time with the questions, it is important to read carefully with understanding. I have finished the exam more than 1 hour before end time, so there is plenty of time.

### #2: Learn how to manipulate resources on Azure using command line tools and Azure ARM templates

I had maybe 2-3 questions with some powershell commands and none with azure CLI, but of course each exam is different, so it's best to stay safe and learn this as well.

* Use `az interactive` to enable CLI auto completion and helpful tips

* Use `powershell`, get help on commands and understand the order of command-lets (first create resource group, etc)

### #3: Preview features are NOT included in the exam curriculum

Preview features are not included, but you should keep an eye on the exam page and check for updates. For example, while I was preparing for the exam it has been updated and some preview features are now GA.

### #4: Always answer all the questions. There is no penalty for wrong answers

### #5: Before you schedule the exam, check for offers

* [Exam with retake](https://eu1.mindhub.com/microsoft-exam-replay-mcp-exam-plus-retake/p/Microsoft-Exam-Replay?utm_source=msftmarketing&utm_medium=msft_offers&utm_campaign=ExamReplayFY20&utm_term=ERFY20&utm_content=weblink3)

* [Exam with retake and practice test](https://eu1.mindhub.com/microsoft-exam-replay-with-practice-test-mcp-exam/p/Microsoft-Exam-Replay-PT?utm_source=msftmarketing&utm_medium=msft_offers&utm_campaign=ExamReplayFY20&utm_term=ERFY20&utm_content=weblink)

### #6: Practice key components using Azure Portal, there will be practice tests

You need to be very familiar with Azure Portal, know how to search for resources and create them quickly. Make use of tooltips (usually under small "?" icon), they often explain details you will need to finish the lab in case you don't remember details for a service or resource.

* [Create free account on Azure and practice!](https://azure.microsoft.com/en-us/free/)

### #7: Schedule exam and create and follow preparation plan

When I was confident I have enought preparation and understand the material, it was time to **schedule the exam**. Scheduling exam was important to set a date in calendar and make sure I stay focus and plan my time well.

**10 days** from exam I scheduled final preparation plan focusing on each section as below. Each time I would use the links, refresh core info, do a lab and most importantly go to Azure Portal and try to perform given task myself. I also used mindmaps and OneNote to keep the learning material organized.

* Day 1: Determine workload requirements (10-15%)

* Days 2-3: Design for identity and security (20-25%)

* Day 4: Design a data platform solution (15-20%)

* Day 5: Design a business continuity strategy (15-20%)

* Day 6: Design for deployment, migration, and integration (10-15%)

* Day 7: Design an infrastructure strategy (15-20%)

* Day 8-9: Practice exams and mock questions, final review. Please **don't** use so called braindumps. I used [AZ-301: The complete practice test, Azure Architect Design](https://www.udemy.com/course/exam-az-301-microsoft-azure-architect-design-test/) (bought cheap on Udemy during Cyber Week)

* Day 10: EXAM! Make sure to get plenty of sleep and schedule the exam in the time when you are most active (for me it is late morning)

### Good luck :)
