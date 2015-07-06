Trello
-----------

This section will define how we should be using Trello in our
projects.

### Naming of Cards (US, Tasks)

The name of the card should contain a user story that somebody will,
eventually, have to do. This should be obtained from the requirements
that the client has specified previously.

The name of the card should be short but it needs to explain what
needs to be done. If there is some extra information that is needed
to fully understand the task it should be written down in the description
of the card. In the same spirit, If a document exists that is related to 
the task, it should be attached to the card so the person responsible 
of working on the task can easily access it.

In order to track the work being done on a user story, checklists
should be used inside the card to keep track of the actual tasks that
need to be done. When a particular task is completed, it should be
marked as such in the task checklist, so Trello can display the
percentage of completion for the whole card.

Ideally, work on a card shouldn't be split over the span of multiple
weeks. As such, the "actual effort" that has been poured into a user
story should be tracked in the task. More information about this below
on the **Doing** list. The general motivation for this is calculating
the differential between what we have previously estimated and the
actual effort that we do. At the end of the week, this differential is
the number of story points that get carried over the next week, in
the case of a card that wasn't completed.

Those tasks that are not part of a user story, like sysadmin stuff,
should also be tracked using a card. We suggest using a label so they
can be easily identified. The color suggested to identify this kind of
cards is blue.

### Use of Trello in Weekly Meetings

Trello is the main way in which we communicate to the client
what we are currently doing, what we did and what we are going to do
in the future. This means that we need to keep it up to date and
inform the client that he can keep an eye on the project at any moment
just by looking at the cards on Trello.

Before every meeting we need to look at what is in Trello and what is
the status of every card so we can give a correct information about
the project to the client. Use Trello to write the agenda of the
meeting, in this way everybody can see what has happened in the
previous meetings in an easy way. Also write in the agenda those
aspects that come out during the meeting, as well as those aspects
that need to be done that aren't necessary a task.

During the meeting you need to inform the client about the status of
Trello, which should also be the current status of the project. Let
the client ask questions about the cards, and answer any doubts that
come up. After the meeting you need to update Trello to reflect what
is going to be done in the next iteration and estimate the
corresponding cards.

### Lists and meaning of lists

#### 1. **Backlog:**

Every task that regarding the project should be here. **If a task is
not in the backlog (or any other list) it doesn't exist**. Any idea,
any "nice to have" feature, everything that should be included in the
product at any point in the development, should be there, so everybody
can track what things are left to be completed on the project. The
eventual bugs that are found in the project should also be created in
this list and must be marked with a **BUG** label. We additionally
suggest using the red label to identify bug cards, so they can be
easily triaged.

#### 2. **ToDo:**

This list should have the tasks that are going to be worked on the
current iteration. Those tasks should have been estimated in order to
be certain that the iteration can be completed on time.

#### 3. **Doing:**

As soon as you begin working on a task you should move it from "ToDo" to
"Doing" as this helps the team and the client to know what the current
status of the iteration is, as well as what things the team is
currently working on.

As development on the card advances, you need to tag the title of the
card by adding the number of story points of effort dedicated to the
card, wrapped in brackets ( **[ ]**, i.e. **[8]**). For example, if
two days of work have been devoted to a card estimated to take 8 story
points and named "***(8) As a user I want to login***", you should
update it to "***(8) As a user I want to login [4]***". This should be
done at the end of each week for all cards for which development has
started or ended during that week.

This process is vital and should never be skipped since it provides
important data about how effectively the team is estimating cards and
it allows the splitting of cards over the span of several weeks.

#### 4. **Pending Review (optional, to be reviewed by another dev):**

The general idea behind this list is to add a step of quality
assurance of the software that we are building. There are some things
that the client can't or doesn't want to test. These things should be
tested by a developer different from the one responsible for the
task. This is optional, as it depends of various factors, for example,
if the team is bigger than one developer and if there is time planned
in the iteration to do these tests.

#### 5. **To be tested (to be reviewed and approved by the client):**

These tests are known as "Acceptance Tests". The client is the only
one who knows what he really wants, so it's up to him to decide if the
feature that we build satisfies his needs. Sometimes the client
doesn't want to do the tests in the staging server, but it is really
important to make him understand that this is the only way that we can
be sure that we are on track and building the right product.

#### 6. **Approved (Ready to Deploy):**

Once the client performs the tests related to a card, he lets the team
know that the card is approved by moving it from the "To be tested"
list to the "Approved" list. **Only the client can move the cards to
this list (unless, of course, there is a previous agreement that
another person can do it)**. The cards on this list can be deployed
into production when needed.

- Code is implemented and working.

- Tests are written and passes.

- Code is live in the development (or staging) server.

#### 7. **Done:**

This list should have the cards that are approved by the client and
are already in the production server. After the client approves the
card, the person responsible of making the production deploy should
put the card in this list as soon as he finishes the deploy (The
features should be
["*smoke tested*"](https://en.wikipedia.org/wiki/Smoke_testing_(software))
to be sure that everything is OK).

- Task was in Approved (ready for deploy).

- Acceptance test have been carried out by the client.

- Code is in production environment.

#### 8. **Agenda:**

In this list every card represents a meeting. Those cards contain the
information about the points that were discussed in the meeting. The
name of the card is the date in which the meeting occurs.  Use a
checklist to show the points to be discussed. Use the description to
annotate any information relevant about the points of the meetings.
You can attach documents or make comments about the meeting using the
corresponding feature in Trello.  These cards should be created before
the meeting with the client, preferably during the team's pre-meeting.

### Tips

Remember that a tool is only useful if everyone uses it. Due to the
fact that we are not in the same place, we strongly depend on these
kind of tools to be able to do our job in the best possible way. Do
not hesitate to bring in new insights about how we can improve the way
we use Trello or if there is another tool that can replace this and
make our life easier.
