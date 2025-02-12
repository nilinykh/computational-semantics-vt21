# Group Work Guidelines

## Pre-requisites

1. **For every student**: make sure you have a GitHub account.
Follow the steps below if you don't have one:
* If you don't have `git`, install it on your system (https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).
* Sign up for GitHub (https://github.com/).
* Go to https://education.github.com/ and sign up for the Student Developer Pack to get unlimited private repositories and the ability to add several collaborators. You are a "student" and you want an "individual account".
* Setup your terminal acceess with ssh-key from your local computer to your Github account. (https://github.com/settings/keys)

2. **For every student**: make sure you have installed Jupyter.
You can use either Jupyter Lab or Jupyter Notebook - the former is a new version of the latter, using either of them is not really affecting the submission infrastructure.
To install Jupyter, please have a look [here](https://jupyter.org/install).

3. **For every group**: Fork this repository and create personal folders.
Read detailed instruction on how to fork repository [here](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo).
*There should be one fork of the original repository per group.*
Within your groups, assign a person who is going to fork this repository.
The resulting fork can be locally cloned by any of the group members and, from this point, every change/commit from the group members should be done to this fork.

Create personal folders of group members within the forked repository.
Within the root, it should look as follows:

```bash
├── {group-name}
│   ├── assignment-01
│   │   ├── adam
│   │   ├── simon
│   │   └── nikolai
│   ├── assignment-02
│   │   ├── ...
```

{group-name} stands for any name you are giving to your group.
For each assignment, there should be a folder for each of the group members.
Your personal folders are used as placeholders for you individual work on the assignment.
In other words, you can put there your own proposals (and work in progress) on how you solved the assignment / how you think it should be solved.
Then, these solutions can be used when discussing assignment within the group.

## Changing a group

Since you are free to change your group or create a brand new group with other students, there is a couple of things for you to take into account.
If you are changing the group, simply create folder with your name in the new group.
If the group if completely new, they should create a brand new fork for them to work on the assignment.

Example situation when changing the group:
3 members of the Group A have submitted their results for 2 assignments.
Their fork now has the following structure in the ```{group-name}``` folder:

```bash
├── {A}
│   ├── assignment-01
│   │   ├── student1
│   │   ├── student2
│   │   └── student3
│   ├── assignment-02
│   │   ├── student1
│   │   ├── student2
│   │   └── student3
```

Then, student1 decides to leave this group and join Group B for the 3rd assignment.
The fork of Group B then would look as follows:

```bash
├── {B}
│   ├── assignment-01
│   │   ├── student4
│   │   ├── student5
│   │   └── student6
│   ├── assignment-02
│   │   ├── student4
│   │   ├── student5
│   │   └── student6
│   ├── assignment-03
│   │   ├── student4
│   │   ├── student5
│   │   ├── student1
│   │   └── student6
```

Example situation when creating a brand new group:

Similarly, we start from this point:

```bash
├── {A}
│   ├── assignment-01
│   │   ├── student1
│   │   ├── student2
│   │   └── student3
│   ├── assignment-02
│   │   ├── student1
│   │   ├── student2
│   │   └── student3
```

Let's say, student1 has decided to make a brand new group with student2 from Group A and student4 from Group B.
To do this, they create a new fork of the original repository and structure their individual work as follows:

```bash
├── {C}
│   ├── assignment-03
│   │   ├── student1
│   │   ├── student2
│   │   └── student4
│   ├── assignment-04
```

Note that the assignment id start with 03 since all of the students have already worked on previous assignments in their older groups.

## Submit Assignments

Once you are done with all the steps above, the repository should look something like this:

```bash
├── 01-logic-and-lambda-calculus
│   ├── assignment
│   │   ├── logic-and-lambda-calculus.ipynb
│   │   ├── simple-sem.fcfg
│   │   └── utils.py
│   └── examples
│       ├── first-order-logic.ipynb
│       ├── lambda-calculus.ipynb
│       ├── propositional-logic.ipynb
│       └── simple-sem.fcfg
└── README.md
├── notes
│   └── work-in-groups.md
├── {group-name}
│   ├── assignment-01
│   │   ├── adam
│   │   ├── simon
│   │   └── nikolai
│   ├── assignment-02
│   │   ├── ...
```

We have:
* individual work as .ipynb file (./{group-name}/assignment-01/adam/logic-and-lambda-calculus.ipynb, etc.)
* group solution as .ipynb file (./01-logic-and-lambda-calculus/assignment/logic-and-lambda-calculus.ipynb)

Each **group** needs to propose solutions in the group solution .ipynb file, which is also the file with the actual task.
**Individual** work .ipynb files are for you to discuss between group members and for us to observe your progress.

For final submission, you need to make a pull request with the changes in your group solution file (./01-logic-and-lambda-calculus/assignment/logic-and-lambda-calculus.ipynb) and, if there are any, in your individual work (./{group-name}/assignment-01/adam/logic-and-lambda-calculus.ipynb).
Through pull requests we will be able to see full history of your commits and changes, both for the group file and for your individual work.
This will give us more information about your progress and better insights into what we can help with.

Read detailed instructions on how to do a pull requests [here](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request)

Before making a pull request with your assignment, make sure your fork is up-to-date.
Things to do once - connect fork with the original repository:
```
git remote add upstream git://github.com/sdobnik/computational-semantics-vt21.git
git fetch upstream
```
Things to do before every assignment submission - update your fork with any changes from the original repository:
```
git pull upstream main
```

When making a pull request write the following title:
```assignment-{assignment-number}-{group-name}```
For example, ```assignment-03-groupA```
Please write names of the group members in the comment field as well.


## How do we expect our students to work in the group?

The general idea is that members in each group would communicate as follows:

- First, try to solve the questions individually by writing out your own solutions in your individual .ipynb files for the corresponding assignment.
- Then, meet online in Zoom as a group with some points for discussion prepared based on your individual work.
- Let also others try to solve the question first on their own.
- If you don't understand a question, or you if you encounter an error, discuss it with other members.
- If you need clarification from the teachers, write your questions to the general Canvas discussion topic for Lab N rather than sending us individual emails. This is to ensure that if we provide additional information about the assignments, the information will be available for everyone.
- There might be more than one solution for each question.
- After everyone found and ran an answer for each question, start working on the final group submission in a separate notebook, e.g. ./01-logic-and-lambda-calculus/assignment/logic-and-lambda-calculus.ipynb for the first assignment
- Make a pull request and add all necessary information.
