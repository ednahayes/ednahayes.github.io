---
layout: post
title:  "Bloc Chat Case Study"
url: /_layouts/newpost.html
published: false

---

## Summary

Bloc Chat is a real-time chat application which was built using Firebase JavaScript, AngularFire, CSS, GIT, HTML and Atom Editor.

## Explanation
Bloc Chat is for the simple user in mind with no strings-attached and ad-free.
Every user, my self included, we look for a convenient way to chat,
user-friendly, with not to many distractions, and bloc chat is just that.
Although it is still a work in process, I feel that bloc chat needs to be
just “simple” but inviting.

## Problem
As we started with Bloc Chat there were different needs that needed to be met:

-A user wants to be able to create a new chat room

-A user would like to add messages in a chat room

-The user name needs to be saved

-New messages are associated with no chat rooms other than the active chat room

## Solution
First, we created the basic test rooms in Firebase, then we created a Room Factory
in Angular which defined all the room related API queries extracting all
the rooms previously created in Firebase. AngularFire was used to coding Bloc Chat,
which is somewhat simpler than others.

![Bloc Chat Code](/images/BlocChatCodeReady.png)

As a user enters the application he/she has the ability to create a room as well as
to visit each chat room before deciding if is the correct chat they want to spend time at. Once a user browses thru the bloc chat application and decides they want to start chatting
(adding messages) then the user will be required to enter a user name.


One of the problems that I encountered was that after the user entered his user name,
that user name needed to be saved in order that when he changed rooms the same user name
will remain in each chat room he enters, this was solved by saving the user name
to the appropriate cookie, therefore, completing the first part of Bloc Chat.

![Bloc Chat screenshot](/images/BlocChatReady.png)
