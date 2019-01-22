---
title: "ServiceNow Scoped Applications"
date: 2019-01-13T00:00:00-04:00
draft: true
tags: ['servicenow, development']
category: ['servicenow']
author: Brian Richards
---

#ServiceNow application development notes#

I am hesitant to characterize this as a 'best practices' post or a 'developer's guide' of any kind, because what I have come to believe after making use of application scope in ServiceNow for the last couple of years is that it is ultimately just another feature of the product. And as such there are many 'right' ways of taking advantage of application scopes for a project.

* Let's start with the first point I want to make: application scopes are not the same thing as applications. Nor are they the same thing as projects. If you're going to build something on the platform 'project' is the term you use for the way you management your development effort, and 'application' is the term you use for the thing a user uses in order to do work. 'Scope' is different from both of these, and really just applies to a meta-information-linked set of objects that you have some tools to manipulate on the platform differently than things that are not in a 'scope.'

* So what can you do with a scoped application? Here's what I have found to be useful.

1. You can publish a scoped application as a container-ish thing from one instance to another easily as a one click action. Conversely you can easily uninstall that application in a similar easy manner. This is pretty nice.

2. You view all your scoped objects in a nice development interface called the Studio that helps to keep things organized. It does not really do much for your development process of, say, a business rule that cannot already do in the platform, but the organization thing is nice.

3. You use Git to back up your scoped application stuff to a third party environment (I've done this with both Github and Gitlab) so that you can, for example, transfer a project to a personal development instance to hack away. Don't get too excited about this relationship with Git things, however. While it is possible to work with branches and stanches when you use a repository, there are a few important things you cannot do. Such as merge branches. It's also valuable to know that switching branches causes the instance to uninstall and then reinstall the application. Which may or may not be a traumatic experience for you.

