# Introduction

## Scope

This course is made for you. It is part of d-fine's introductory curriculum for
new hires and is provided to CorrelAid. Its aim is to **impart basic IT knowledge**, so that you can hit the
road running when staffed on your first IT project.

The course covers version control with `git`.

## Intent

As prerequisites differ, the training is offered in the form of _supported
self-study_. This means that instead of following a presentation of a week's
worth of topics, you can follow the plan of the course _at your own pace_.
As everyone brings different prerequisites, the course is designed in such
a way that even participants with previous knowledge will be busy for a few
hours.
During the meetings, instructors will be available to _help you_ with
any questions that you cannot figure out for yourself (see also
[Where to get help](#where-to-get-help)).

Almost every chapter consists of both a theoretical and a practical part. You
are encouraged to follow the practical exercises and hand them in once you are
done. Your instructor will review your submissions and give an overall feedback
in the following meeting such that everyone can benefit from it.

_The aim of this exercise is not to assess you, but to enable you to deliver
value in your future work._ Functional IT knowledge is at the core of our work
on many projects. Therefore, although we are well aware that one could easily
create and distribute solutions for the practical exercises, we would like to
appeal to your common sense in discouraging you from engaging in such a
practice: In most cases, reading someone's solution to a problem without having
yourself attempted to solve it does _not_ have the effect of conveying the
desired proficiency. **We ask you to refrain from copying solutions, for your
own good, and for the good of others.**

Note also that this course is not intended to make you an expert programmer.
Its aim is to hand you a toolbox with just enough inside to get you started.
Feel free to deepen your knowledge in any of the individual areas, and to
broaden it to any of the many others that are out there.

_We hope you will enjoy this training course. We are dedicated to the continual
improvement of our course materials. Therefore, if you have **questions,
comments, or any other feedback, please feel free to reach out to your course
instructors**._ Even better, fork the `basis-it-training` repository, make a
merge request against the master branch with your improvements, and assign it to
your instructor. (You are going to learn how to do this during the training.)

## Schedule

The general idea of the course is that you should follow it at your own pace.
However, we have an idea of what we would like you to learn and
make the following recommendation:

| Course section | When to complete |
| --- | --- | --- |
| Version control with `git` | Complete the `Bash Basics` section till the second meeting |
| Version control with `git` | Complete the `Git advanced` section till the third meeting |
| Version control with `git` | Complete the `Git expert` section till the final meeting |

To guide you through the course, we have marked the sections of the course as
core and/or elective. In addition, every section contains some guidance
on until when you should complete it to stay on track.

## Where to get help

As noted above, an engagement with the course materials and a brief
online research is part of the expected scope of the course.
If you need help or have questions, follow the steps below:

- Look closely at the course material (~5 min).
- Try to answer your question via online search (~5 min).
- Pose your question to another course participant.
- Send an email to the trainers so that they can answer it at the next meeting.

## Submitting solutions to exercises

In the course of this training, we will ask you to submit the solutions to every
exercise at the end of each chapter. Please submit the solution to every
exercise as soon as you are done with it. In the next meeting, a possible
solution and some possible mistakes will be discussed so that everyone
can benefit from it.

### Review process on git

For the git chapters in the training you will need to write
bash scripts and send those to the supervisors of this training.
In order to do so:

- Send your bash scripts which executes all commands necessary to complete the
  exercise by e-mail.\
  _Hint:_ Your bash saves the last 500 commands you executed in a hidden file
  called `.bash_history` which you can find in your home directory. You can use
  this history file to collect the commands you would like to add to your bash
  script in case you forgot to write them down right away. Just navigate to your
  home directory and display the file:

  ```lang-bash
  cd ~
  less .bash_history
  ```

  Copy only the necessary commands and paste them to a text file. (NB: As per
  convention, shell scripts are saved with the file extension `.sh`.) Remove
  errors or repetitions and send the saved file to your trainers.

  Be aware that the content of the `.bash_history` file is not being updated
  dynamically but only after the respective session of your bash has been closed.

Start now with [Git / Bash Installation](git/GitBashInstallation).

## Navigation

- [Continue with "Git / Bash Installation"](git/GitBashInstallation)
- [Return to top level](home)
