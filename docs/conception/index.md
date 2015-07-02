## The Conception Phase

The conception phase begins at the moment a new project walks through
the door. The main focus in this stage is understanding the
requirements of the project, and the results of this whole process is
a set of mockups and estimations that fulfills those requirements.

During this stage, the team that will be involved in a project is
built, taking into consideration what is known initially. The idea is
that each team member strengths can be used to successfully take the
project from zero to production in reasonable time.

At talPor, this process is known as the **discovery**. During a
discovery, fast paced meetings between the client and the team take
place with the goal of defining the requirements and defining what
will be part of the **MVP (Minimum Viable Product)**. These meetings
should be happening as fast as schedule permits.

Generally, clients will want to build every conceivable feature that
is remotely related to their idea. As such, generally there is a lot
of noise when you try to figure out what is the real problem the
client is trying to solve. At this stage you want to understand and
isolate what is the big problem at hand, and provide the tools to
solve it.

Also remember, at the end of the day, we are also developing the
client idea. We are interested in the client to be successful, so we
want to be able, at the end of the development process and into the
production stage, to (in)validate the path that has been chosen.

Always keep in mind:

- Listen to what the client says and want. **Take notes**.

- Be polite with your client but very assertive.

- Explain when something is not possible (or extremely hard).

- Involve everybody, including the client, in the process. Don't take
  ideas for granted, don't make assumptions, speak up when necessary.

### The Feedback Loop

The feedback loop is the shape the discovery process takes as meetings
with the client take place. When the first meeting with the client
happens, it is expected that the client will talk and explain the
project to the team, while the team takes notes and asks questions. In
this meeting, most of the talk will be done by the client.

After the first meeting, the team will start shaping up the
requirements the client talked about. Possibly, the team will come up
with wireframes or mockups, or some other way to visualize it. As the
next meeting with the client comes around (which should be as soon as
possible), roles in the meeting slightly shift.

During the second meeting, the team will present their mockups to the
client. It is expected that the client will have comments, questions
or simply have more to add to what was already said. Again, the team
takes notes and gets the opportunity to ask more questions which help
solidify the vision of a project.

The internal work is repeated again, coming up with new visualizations
of the requirements. As the next meeting comes around, the roles in
the meeting shift even more, with the team explaining the vision of
the requirements they have, and the client, ideally, aligning even
further with that vision. More comments and questions can be posed by
the client, but ideally as every meeting with further developments
happen, the client will have less and less to say.

This loop continues, until a united vision between the team and the
client is agreed upon.

Always keep in mind:

- **Prepare before your client meeting and summarize what happens after
  it.** Take the time to do a short *pre-meeting* with your teammates to
  have a common understanding and goals in the meeting, and a short
  *post-meeting* once the meeting is over.

- **Try to validate your team hypothesis.** For example, try to propose
  stuff that is known to work instead of reinventing the wheel.

- **Use what is available to you.** If this is not a new project, ask to
  see Google Analytics data, or any data that the project has
  available. Make better hypothesis using this.

- **Assume as little as possible.** If you can't validate, it's just a
  hunch.

- Sometimes, the client doesn't want to let go of a feature they deem
  really important. Try to compromise, try to explain why is it not
  possible. Explain that if that feature makes it into the final
  vision for the MVP, other features will have to be dropped for now.

- The whole point of the discovery is to converge on a concrete but
  not final vision for the project. Sometimes, your client will always
  have something more to say, if possible listen, if not, remind them
  that this is a MVP and more time to build other features will always
  be there afterwards.

- Remind your client there is space for more development after the MVP
  is done. The point of bounding the reach of the MVP is to be able to
  **validate as soon as possible** rather than when multiple months of
  development have been poured into the wrong hypothesis.

### Mockups

Mockups are one of the deliverables of the discovery process. It
should represent a very basic view of the direction the team is taking
with the project. During the discovery process, mockups should be used
to aid the delivery of the vision by the team.

Always keep in mind:

- While simple, mockups should be sufficient to represent the vision
  the project will take. Don't overlook details, but be pragmatic
  about them.

- Currently, we use [Balsamiq Mockups](https://balsamiq.com/) to build
  mockups.

### Estimations

Estimations are one of the deliverables of the discovery process. At
talPor, we use a system of **user stories and story points** to
estimate tasks to be done in a project. A user story is a sentence of
the form "As a [actor], I want to [action]". For example, one possible
user story is "As a user, I want to log in".

Every single feature that is proposed during the discovery process
should be turned into one or several user stories. Consider using
*themes* to classify user stories. For example, the previous user
story could be part of the *accounts* theme. **Every user story should
be estimated using story points.**

At talPor we use a Fibonacci schemed story point system. We can assign
to every task the following story points: 0.5, 1, 2 (a day worth of
work), 3, 5, 8, 13, and 20+. We estimate every engineer can perform 10
story points a week, as such, assigning 8 to a task is saying it is
expected to take less than a week, and 13 more than one week.

Assigning story points to a task should be done by the engineering
team physically at the same place (or via a video conference if not
possible). Ideally, each team member should have a set of cards or 
pieces of paper with the possible story point values (0.5, 1, 2, 3, ...) 
written on them.

You should start by agreeing upon a user story that you all
estimate to be a 2, and another user story that you all estimate to be a 5.
The need for this is to set a baseline for comparison when estimating the
remaining cards. Once these have been agreed upon, for each user story
every team member shows the card with the story points they believe the
story will take. If every member estimated the same, then the value is
recorded as the user story estimation. In case there was a disagreement,
a **consensus needs to be reached** before an estimation can be recorded
for the user story.

Once every user story is estimated, some calculations should be done
to figure out the expected standard deviation for the user
stories. There are internal spreadsheets available to do this. Using
those calculations, an expected delivery time for all the user stories
can be estimated.

Projects generally have a time frame. If the expected delivery time
exceeds the project time frame, then further negotiation is needed
between the team and client, even if a common vision was agreed upon
by both parties. Common ways to do this include removing user stories
or changing their scopes or reach.

Always keep in mind:

- **Your estimation will probably be wrong.** Humans are exceptionally
  bad at estimating time, especially under-estimating. Do your best to
  keep the estimation as honest and real as possible.

- **Account for testing, deployment, bugfixing and other changes.**
  You will not always be building new features in the project. Account
  for time building tests for the codebase, time spent making sure
  deployment works, bugfixing or design changes.

- If you find yourself using big story points for a user story, or
  needing higher story points, consider splitting your user stories
  into smaller more manageable user stories.

- Keep your estimations up-to-date in the project's [Trello](https://trello.com)
  board.
