Trello
-----------

This section will define how we should be using Trello in our projects.

###Naming of Cards (US, Tasks)

The name of the card should contain a user story that somebody will have to do. This task can be obtained from the user stories or by a requirement that the client needs.

The name of the card should be short but it needs to explain what is needed to be done, if there is some extra information that is needed to fully understand the task it should be written in the description of the card. The same way if there is document that is related to the task it should be attached to the card so the person responsible of making the task can easy access to it.

###Use of Trello in Weekly Meetings

Trello is the main way in which we can communicate with the client about what we are currently doing, what we did and what we are going to do in the future. This means that that we need to keep it up to date and inform the client that he can keep an eye on the project at any moment just by looking at the cards on Trello.

Before every meeting we need to look at what is in Trello and what is the status of every card so we can give a correct information about the project to the client. Use trello to write the agenda of the meeting, in this way everybody can see what have happen in the previous meetings in an easy way. Also write in the agenda thing that come out in the meeting as thing that need to be done that aren't necessary a task.

During the meeting you need to inform the client about the status of Trello which should also be the status of the project. Let the client ask questions about the cards and answer any doubts that come up. After the meeting you need to update Trello to reflect what is going to be done in the next iteration and estimate the corresponding cards.

###Lists and meaning of lists

#### 1. **Backlog:**
Every task that defines the project should be here. If a task is not in the backlog (or any other list) it doesn't exist. Any idea, any "nice to have" feature, everything that should be included in the product at any point in the development should be there so everybody can track what the things that are left to complete the project are. The bugs that are found in the project should also be created in this list and must be marked with a **BUG** label.

#### 2. **ToDo:**
In this list should be the tasks that are going to be done in the current iteration. Those tasks should have been estimated in order to be sure that the iteration can be completed on time.

#### 3. **Doing:**
As soon as you begin to work on a task you should move it from "ToDo" to "Doing" as
this helps the team and the client, know what the current status of the iteration
is as well what things the team is working on.

As development on the card advances, you need to tag the title of the card by adding
the number of story points of effort dedicated to the card, wrapped in brackets
( **[  ]**, i.e. **[8]**). For example, if two days of work have been devoted to a
card estimated to take 8 story points and named "***(8) As a user I want to
login***", you should update it to "***(8) As a user I want to login [4]***". This
should be done at the end of each week for all cards for which development has
started or ended during that week.

This process is vital and should never be skipped since it provides important data
about how effectively the team is estimating cards and it allows the splitting of
cards over the span of several weeks.

#### 4. **Pending Review (optional, to be reviewed by other dev):**
The general idea behind this list is to add a step in the quality of the software that we are building. There are some things that the client can't or don't want to test, this things should be tested by someone different of the developer of the task. This is optional, it depends if the team is bigger than one developer and if there is time planned in the iteration to do this tests.

#### 5. **To be tested (to be reviewed and approved by client):**
This tests are known as "Acceptance Tests", the client is the only one who knows what he really wants so it depends of him if the feature that we build satisfies his needs. Sometimes the client doesn't want to do the tests in the test server, but is really necessary to make him understands that this is the only way that we can be sure that we are building the right product.

#### 6. **Approved (Ready for Deploy):**
The client let the team knows that the card is approved by moving it from "To be tested" to "Approved". Only the client can move the cards to this list (Unless there is a previous agreement that another person can do it). The cards on this list can be deployed into production when the client needed to.

    a- Code is implemented and working.

    b- Tests are written and passes.

    c- Code is live in the development (or staging) server.

#### 7. **Done:**
Here should be the cards that are approved by the client and that are already in the production server. After the client approves the card, the person responsible of making the deploy into production should put the card in this list as soon as he finish the deploy (The features should be ["*smoke tested*"](https://en.wikipedia.org/wiki/Smoke_testing_(software)) to be sure that everything is OK).

    a- Task was in Approved (ready for deploy).

    b- Acceptance test have been carried out by the client.

    c- Code is in production environment.

#### 8. **Agenda:**
In this list every card represents a meeting, in those cards is the information about the points that were discussed in the meeting. The name of the card is the date in which the meeting occurs.
Use a *todo list* to show the points to be discussed. Use the description to annotate any information relevant about the points of the meetings.
You can attach documents or make comments about the meeting using the corresponding feature in Trello.

### Tips
Remember that a tool is only useful if everyone uses it. Due to the fact that we are not in the same place we strongly depend on these kind of tools to be able to do our job in the best possible way. Do not hesitate to bring in new insights about how we can improve the way we use Trello or if there is another tool that can replace this and make our life easier.
