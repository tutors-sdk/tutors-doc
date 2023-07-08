---
order:4
---
Tutors CheatSheet v2.0

Tutors quick reference

[toc]

## Course Folders

Folders starting with the following names have a significance in Tutors:

| Folder Name | Description                                            | Example | Source
| ----------- | ------------------------------------------------------ | ------  |------  |
| topic       | Top level course topic                                 | [link](https://reader.tutors.dev/topic/reference-course/topic-01-typical)| [link](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical)|
| unit        | Group of learning objects within a topic               | [link](https://reader.tutors.dev/topic/reference-course/topic-01-typical)| [link](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-1)|
| side        | Group of learning objects framed in a sidebar          | [link](https://reader.tutors.dev/topic/reference-course/topic-02-side)                  | [link](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-02-side/side-unit)|
| archive     | Downloadable zip file of resources                     | [link](https://reader.tutors.dev/wall/archive/reference-course)| [link](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-07-reference/archive)|
| book        | Step by step lab instructions, authored in markdown    | [link](https://reader.tutors.dev/lab/reference-course/topic-01-typical/unit-1/book-a)| [link](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-1/book-a)|
| github      | Link to a GitHub repository                            | [link](https://reader.tutors.dev/wall/github/reference-course)| [link](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical)|
| note        | Single web page, authored in markdown                  | [link](https://reader.tutors.dev/note/reference-course/topic-01-typical/unit-2/note-1)| [link](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-2/note-1)|
| panelvideo  | A full screen width video, hosted in YouTube or HEANet | [link](https://reader.tutors.dev/topic/reference-course/topic-03-media)| [link](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-03-media/panelvideo-1)|
| paneltalk   | Full screen width  presentation in pdf format          | [link](https://reader.tutors.dev/topic/reference-course/topic-05-panel-talk)| [link](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-05-panel-talk/paneltalk)|
| panelnote   | Full screen width note                                 | [link](https://reader.tutors.dev/topic/reference-course/topic-04-panel-note)| [link](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-04-panel-note/panelnote)|
| talk        | Standard presentation in pdf format                    | [link](https://reader.tutors.dev/talk/reference-course/topic-01-typical/unit-1/talk-1-intro)| [link](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-1/talk-1-intro)|
| web         | Link to an external web site                           | [link](https://reader.tutors.dev/wall/web/reference-course.netlify.app)| [link](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-2/web-1)|

The following filenames are significant:

| File name | Description |
| ----------- | ----------- |
| topic.md    |  title + subtitle for a topic or a unit  |
| topic.png   |  image for a topic  |
| weburl      |  link to external web site  |
| videoid     |  id of  external video  |
| githubid    |  link to github repo  |


For all file & folder names, avoid spaces within a file name. So instead of:

- Topic Introduction

...use:

- topic-introduction


## Course Structure

The minimum requirements for a course are a folder containing these three files:

| File name | 
| ----------- | 
| course.md      |  
| course.png     | 
| properies.yaml   |  

### course.md

A markdown file, structured as follows:

~~~markdown
Course Title

Course information - a course outline, description or any other information. Can be any length. Will appear as slide over if the user presser the Info button on the top left.
~~~

### course.png

An image that will be used in the course title bar

### properties.yaml

Course metadata in yaml format. At a minimum, this must contain the following:

~~~yaml
credits: The course author(s) or organisation
~~~

The credits property will appear as a subtitle in the course title bar.

There are a range of other optional properties. See the end of this document for a complete list.

### Folder Structure

A course typically consists of a series of topic folders, named to sort alphabetically: 

| Folder Name            |
| ---------------------- |
| topic-01-introduction  |
| topic-02-learning-html |
| topic-03-learning-css  |

## Topic

A topic folder may be laid out like this:

![](img/topic-folder.png)

The title and subtitle are extracted from the topic.md file, for example:

### topic.md

~~~~markdown
# Simple

Units with presentations, labs + resources
~~~~

The image is contained in topic.png

## Unit

A unit will encapsulate learning resources, framed by a title:

![](img/unit.png)

The above unit is laid out as follows:

![](img/unit-folder.png)

Three learning objects (discussed below) + another topic.md file, which contains the unit title:

### topic.md

~~~markdown
Main Lesson
~~~

## Learning Resources

### Types

Tutors supports nine types learning resources: 

| Type | Description  | 
| ----------- | ------------------------------------------------------ |
| talk        | Standard presentation in pdf format                    |
| web         | Link to an external web site                           |
| note        | Single web page, authored in markdown                  |
| book        | Step by step lab instructions, authored in markdown    |
| panelvideo  | A full screen width video, hosted in YouTube or HEANet |
| paneltalk   | Full screen width  presentation in pdf format          |
| panelnote   | Full screen width note                                 |
| github      | Link to a GitHub repository                            |
| archive     | Downloadable zip file of resources                     |

Each learning resource is contained within a folder, whose name starts with the name above, and may continue with additional sorting & semantic information. Eg:

- talk-1-intro
- talk-2-explore

The numerals imply alphabetic sorting of these 2 learning resources.

### File Structure

Each resource much have the following files:

- some-resource-name.md
- some-resource-name.png

The name chosen for the markdown file must be also used for the .png. These provide essential information to populate a tutors card. For example this card:

![](img/card-1.png)

would require these two files:

#### introduction.md

~~~markdown
Lecture 1

A short summary of the talk, no more than two sentences.
~~~

#### introduction.png

![](img/introduction.png)


## Talk 

A talk is a PDF presentation, document or other pdf formatted resource. The pdf file, markdown description and image file must all have the same file name, which can be whatever you choose. For example:

![](img/talk.png)

The .md file provides the card title + subtitle:

#### introduction.md

~~~markdown
Lecture 1

A short summary of the talk, no more than two sentences.
~~~

These will populate the card:

![](img/card-1.png)

... which will include the .png image provide

Selecting the card will open the pdf in a reader, with an accompanying context panel on the right - called the Topic Navigator:

![](img/talk-pdf.png)

Slide next/prev + rotate, download and full screen buttons are included in the title bar.

- [Talk Example](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-1/talk-1-intro)

## Web 



## Note 

## Book 

## Panelvideo 

## Paneltalk 

## Panelnote 

## Github 

## Archive  

## Ordering Learning Resources

## Using SVG Icons

## Properties.yaml

## Calendar.yaml

## Enrollment.yaml

## Makrdown Guides

## Image resizing

- <https://nodeca.github.io/pica/demo>

## Reference Course

  
