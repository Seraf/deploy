# Contributing Guidelines

#Table of Contents
  * [Agile Project Management](#an-agile-project-management-workflow-just-using-github-issues)
    * [Agile Components](#agile-components)
      * [Stories](#user-stories)
      * [Sprints](#sprints)
      * [Sprint Backlog](#sprint-backlog)
      * [Global Backlog](#global-backlog)
    * [Stories Issues](#stories-issues)
    * [Sprints Milestones](#sprints-milestones)
    * [Sprint Backlog (Ready)](#sprint-backlog-ready)
    * [Global Backlog](#global-backlog)
  * [A Basic Agile Workflow](#a-basic-agile-workflow)
    * [The Global Backlog](#the-global-backlog)
    * [The Sprint Backlog](#the-sprint-backlog)
    * [In Progress](#in-progress)
    * [In Review](#in-review)
    * [Closed](#closed)
  * [Party](#party)
Stories Issues

##An Agile Project Management Workflow Just Using GitHub Issues

Although GitHub Issues doesn't have many of the features that you'd normally want in a project management system, you can still use Issues to create a lightweight Agile workflow. All it takes is a bit of finesse and some self imposed structure.
To achieve this, we use Waffle : https://waffle.io/cycloidio/youdeploy/

###Agile Components

These are the core components of an agile system that you can implement using GitHub issues (you might want to skip ahead if you're already an agile ninja).

####User Stories

Stories are the smallest unit of work to be done for a project. The goal of a story is to deliver a unit of value to the customer. In Agile-land, common syntax for writing stories is:

*As a `<type of user>`, I want `<some goal>` so that `<some reason>`.*

####Sprints

Sprints are fixed-length iteration cycles, usually lasting one, 2 or 4 weeks. The goal is for the team to deliver a working piece of software by the end of the sprint (a potentially shippable increment).

####Sprint Backlog

The sprint backlog is the collection of work that is scheduled to be tackled during a sprint. At the beginning of the sprint, the team decides what work they should do during the sprint and moves those stories from the global backlog to the sprint backlog. Stories in the sprint backlog should be organized by priority so the team can pick off the top tasks as they work through the sprint.

####Global Backlog

The global backlog is a prioritized list of work (stories) that has not been scheduled to be completed. As new work comes in, it gets added to the global backlog and prioritized. In an Agile workflow, the development team pulls from the backlog as opposed to a manager pushing work onto the developers. The goal is to keep the backlog as small and as organized as possible.

Mapping the Agile Components to GitHub Issues

Now that we've laid out the Agile components, here's how you can implement them in GitHub Issues.

| Agile          | Github         |
| -------------- | -------------- |
| Stories        | Issues         |
| Sprint         | Milestone      |
| Global Backlog | Column Backlog |
| Sprint Backlog | Column Ready   |


###Stories Issues

If you make an issue the same way as you would make a story then you've got this one in the bag.

The problem with a user story is that's too long for a github issue title. Give a good summary of the issue in the title and format your issue like this:

**User Story**:
As a `<type of user>`, I want `<some goal>` so that `<some reason>`.

**Description**:
`<...>`

###Sprints Milestones

Milestones are a great surrogate for sprints because they have due dates and allow you to group issues together. As a bonus, GitHub displays the current number of completed issues for any milestone.

###Sprint Backlog (Ready)

GitHub doesn't have a place to store your issues in a way that resembles a proper sprint backlog, so for this need, use the label **ready**. This label will be set automatically by moving an issue from the backlog to the column Ready on Waffle.

For the priority there's a label available, but the most urgent issue is alway at the top of the column on Waffle.

###Global Backlog

The concept is the same as the sprint backlog. You can use the GitHub issues search to find only those issues that are open, unassigned, and not on any milestone. This is your global backlog. Once again, use priority labels to indicate precedence.


##A Basic Agile Workflow

Our Agile workflow will have five stages: global backlog, sprint backlog, in progress, in review, closed. Cool? Let's go!

###The Global Backlog

All new issues should go to the global backlog which means they should be unassigned and unmilestoned. Everyday, the team lead should look over the new backlogged issues and assign them a priority. Remember, in order to find your global backlog issues, use the GitHub issue search to display open issues with no milestone and no one assigned.

###The Sprint Backlog

Next, it's time to decide what to work on so you should create a new milestone on GitHub. If due dates are your cup of tea, give the milestone a due date. As we have some ops work, sprints will have a duration of one month.

As a team, work through the issues in the global backlog and add the appropriate issues to the sprint backlog. You move issues from the global backlog to the sprint backlog by milestoning the issues and moving them into **Ready** column. It's pretty easy to just do on the fly when you come across an issue that you want to work on this sprint cycle. Remember to leave the issue unassigned, or you'll inadvertently skip the sprint backlog, which is not cool in Agile land.

As you build up your sprint backlog, update the priority labels on the issues to reflect their priority relative to the other issues in the sprint backlog. This indicates what tasks the team should be working on first. Also, if you want to add story points to the issue, now's the time to do it! Create another class of labels for your points and use those to weight your issues.

###In Progress

When an open issue is assigned to someone, that means the issue is in progress.

Once your sprint begins, your team starts by pulling tasks off the sprint backlog, starting with the issues with the highest priority (and the lowest point values if you want to hyper-optimize your flow efficiency). When someone grabs a task, they assign it to themselves to indicate the work is in progress. It's best if your team members only have things assigned to them if they are actually working on them. This way the team knows what everyone is working on and what issues are still available for them to bang out.

###In Review

Moving issues to the review stage starts by opening a pull request. Give the PR a descriptive title and reference all the relevant issues. Something like, “Adds widget to new feature - closes #1, closes #2" is awesome because when the pull request is merged, those referenced issues will be closed as well. Make sure the milestone of the pull request is the milestone you are using for your current sprint, and remember to assign the PR to the reviewer.

###Closed

Once a pull request has been merged, you move all the resolved issues to closed. If you referenced your issues correctly in your pull request, your cards will automatically be marked as closed when the pull request is merged. Leave the milestone and assignee set on the issue as a record for later reference.

##Party!

Ideally, the team should have code that's ready to ship by the end of your sprint. Any open pull requests for the sprint should either be merged, closed or moved to the next milestone. Any open issues from the sprint should either be moved to the next milestone (if it's in progress) or back to the global backlog by unmilestoning and unassigning the issue.

You finish your sprint by closing the milestone. Set the milestone state to closed and leave any notes about the sprint in the description section of the milestone. Some good things to record here are number of issues that had to be pushed to the next sprint (and point values), what was accomplished and what was not, and any problems that came up. Then, party!
