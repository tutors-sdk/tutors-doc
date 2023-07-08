---
order:4
---

# Tutors Reference

[toc]

## Course Folders

Folders starting with the following names have a significance in Tutors:

|  Example                                                                                     | Source | 
| -------------------------------------------------------------------------------------------- | ------------------------------------------  |
| [topic](https://reader.tutors.dev/topic/reference-course/topic-01-typical)                   | [Top level course topic ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical)|
| [unit](https://reader.tutors.dev/topic/reference-course/topic-01-typical)                    | [Group of learning objects within a topic  ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-1)|
| [side](https://reader.tutors.dev/topic/reference-course/topic-02-side)                       | [Group of learning objects framed in a sidebar  ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-02-side/side-unit)|
| [archive](https://reader.tutors.dev/wall/archive/reference-course)                           | [Downloadable zip file of resources  ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-07-reference/archive)|
| [book](https://reader.tutors.dev/lab/reference-course/topic-01-typical/unit-1/book-a)        | [Step by step lab instructions, authored in markdown  ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-1/book-a)|
| [github](https://reader.tutors.dev/wall/github/reference-course)                             | [Link to a GitHub repository  ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical)|
| [note](https://reader.tutors.dev/note/reference-course/topic-01-typical/unit-2/note-1)       | [Single web page, authored in markdown ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-2/note-1)|
| [panelvideo](https://reader.tutors.dev/topic/reference-course/topic-03-media)                | [A full screen width video, hosted in YouTube or HEANet](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-03-media/panelvideo-1)|
| [paneltalk](https://reader.tutors.dev/topic/reference-course/topic-05-panel-talk)            | [Full screen width  presentation in pdf format    ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-05-panel-talk/paneltalk)|
| [pnelnote](https://reader.tutors.dev/topic/reference-course/topic-04-panel-note)             | [ Full screen width note](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-04-panel-note/panelnote)|
| [talk](https://reader.tutors.dev/talk/reference-course/topic-01-typical/unit-1/talk-1-intro) | [Standard presentation in pdf format  ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-1/talk-1-intro)|
| [web](https://reader.tutors.dev/wall/web/reference-course.netlify.app)                       | [ Link to an external web site  ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-2/web-1)|

The above table links to examples + the tutors course resource used to generate the example (the source).

The following filenames are reserved:

| File name       | Description |
| --------------- | ----------- |
| course.md       |  Title for course (mandatory)  |
| properties.yaml |  Course properties (mandatory) |
| course.png      |  Course image |
| calendar.yaml   |  Course calendar |
| enrolment.yaml  |  Student enrolment file|
| weburl          |  link to external web site  |
| videoid         |  id of  external video  |
| githubid        |  link to github repo  |

#### Folder Names

Folder names convey the type of learning resourcee, with the first letters determining its type.  To sort the name alphabetically, append numberals. To enhance meaning, append contextual keywords: For example:

| Folder Name            |
| ---------------------- |
| topic-01-introduction  |
| topic-02-learning-html |

For all file & folder names, avoid spaces within a file name.

| Do                     | Don't
| ---------------------- | -------------------- |
| topic-01-introduction  | Topic 01 Introduction
| topic-02-learning-html | Topic 02 Learning HTML


## Course Structure

The minimum requirements for a course are a folder containing these three files:

| File name      | Purpose      |  
| -------------- | ------------ | 
| course.md      | Course title + general course information
| course.png     | Course image
| properies.yaml | Course properties

### course.md

A markdown file, structured as follows:

~~~markdown
Course Title

Course information - a course outline, description or any other information. Can be any length. Will appear as slide over if the user presser the Info button on the top left.
~~~

### properties.yaml

Course metadata in yaml format. At a minimum, this must contain the following:

~~~yaml
credits: The course author(s) or organisation
~~~

The credits property will appear as a subtitle in the course title bar.

There are a range of other optional properties. See later in this document for a complete list.


## Topic

Top level learning object for a course. Typically encapsulating a session or week of learning material.

- [Example](https://reader.tutors.dev/topic/reference-course/topic-01-typical) 
- [Source ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical)

| File name      | Purpose      |  
| -------------- | ------------ | 
| topic-title.md      | Topic title + summary. Any file name, file type must be .md
| topic-title.png     | Image for topic. File name must be same as .md file. File type can be .png, .jpg, or .jpeg


### topic.md
The title and subtitle are extracted from the topic.md file, for example:

~~~~markdown
Simple

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

  
