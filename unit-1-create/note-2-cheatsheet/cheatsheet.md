---
order:4
---

# Tutors Reference

[toc]

## Cards

The card metaphor is used throughout tutors as a simple, effective visual to represent a variety of learning resources. In general the contents of a card are extracted from the following:

- A Markdown file, containing resource name + summary
- An image, in png, jpg, gif or svg formats.

These resources are typically named to match your context, and are contained in a folder whose name is structured to encode the type of learning resource.

## Semantic Resource Names

### Folders Names

Folder names convey the type of learning resource, with the first letters determining its type. Folders starting with the following names have a significance in Tutors:

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
| [panelnote](https://reader.tutors.dev/topic/reference-course/topic-04-panel-note)            | [ Full screen width note](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-04-panel-note/panelnote)|
| [talk](https://reader.tutors.dev/talk/reference-course/topic-01-typical/unit-1/talk-1-intro) | [Standard presentation in pdf format  ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-1/talk-1-intro)|
| [web](https://reader.tutors.dev/wall/web/reference-course.netlify.app)                       | [ Link to an external web site  ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-2/web-1)|

 To sort the name alphabetically, append numerals. To enhance meaning, append contextual keywords: For example:

| Folder Name            |
| ---------------------- |
| topic-01-introduction  |
| topic-02-learning-html |

For all file & folder names, avoid spaces within a file name.

| Do                     | Don't
| ---------------------- | -------------------- |
| topic-01-introduction  | Topic 01 Introduction
| topic-02-learning-html | Topic 02 Learning HTML

### File Names

Each resource will typically have the following files:

| File                   | Purpose                                                      |
| ---------------------- | ------------------------------------------------------------ |
| some-resource-name.md  | A markdown file, typically containing title + short summary for the resource |
| some-resource-name.png | Image to he used for the resource. Name must be the same as the .md file, image can be .png, .jpg. .jpeg, .gif |

The following filenames are reserved:

| File name       | Description                   |
| --------------- | ----------------------------- |
| course.md       | Title for course (mandatory)  |
| properties.yaml | Course properties (mandatory) |
| course.png      | Course image                  |
| calendar.yaml   | Course calendar               |
| enrolment.yaml  | Student enrolment file        |
| weburl          | link to external web site     |
| videoid         | id of  external video         |
| githubid        | link to github repo           |

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

| Files  | Purpose      |
| -------------- | ------------ |
| topic-title.md      | Topic title + summary. Any file name, file type must be .md file type |
| topic-title.png     | Image for topic. File name must be same as .md file. File type can be .png, .jpg, or .jpeg|

### topic.md

The title and subtitle are extracted from the .md file, for example:

~~~~markdown
Simple

Units with presentations, labs + resources
~~~~

In addition to the title, subtitle + image specified the file, the topic can contain any number of units (see below) or other learning objects.

## Unit

A unit will encapsulate learning resources, framed by a title

- [Example](https://reader.tutors.dev/topic/reference-course/topic-01-typical) 
- [Source ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-1)

| Files          | Purpose                                                      |
| -------------- | ------------------------------------------------------------ |
| main-lesson.md | Title for the unit. The file can have any suitable name, but must be .md file type |


The title is specified in a single markdown file:

### main-lesson.md

~~~markdown
Main Lesson
~~~

Units contain any number of learning resources.

## Side

A side will encapsulate learning resources, framed by a title

- [Example](https://reader.tutors.dev/topic/reference-course/topic-02-side) 
- [Source ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-02-side/side-unit)

| File name     | Purpose                                                      |
| ------------- | ------------------------------------------------------------ |
| topic-labs.md | Title for the side bar The file can have any suitable name, but must be .md file type |


The title is specified in a single markdown file

### topic-labs.md

~~~markdown
Labs for this Topic
~~~

Side bar cam contain any number of learning resources.

## Learning Resources

### Types

There are 2 broad types of learning resources

- Card Resources
- Panel Resources

### Card Resources

These resources are represented by simple cards that can appear in a topic unit:

| Example Resource | Display | Cards |
| ---------------- | ------- | ----- |
| [Standard presentation in pdf format](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-1/talk-1-intro)             | [Lecture 1](https://reader.tutors.dev/talk/reference-course/topic-01-typical/unit-1/talk-1-intro) | [Talks](https://reader.tutors.dev/wall/talk/reference-course) |
| [Single web page, authored in markdown ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-2/note-1)                | [Note 1](https://reader.tutors.dev/note/reference-course/topic-01-typical/unit-2/note-1)          | [Notes](https://reader.tutors.dev/wall/note/reference-course) | 
| [Step by step lab instructions, authored in markdown  ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-1/book-a) | [Lab 1](https://reader.tutors.dev/lab/reference-course/topic-01-typical/unit-1/book-a)            | [Labs](https://reader.tutors.dev/wall/lab/reference-course) |
| [Link to a web site  ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-2/web-1)                                   | [Web Site](https://tutors.dev)                                                                    | [Web Links](https://reader.tutors.dev/web/talk/reference-course) |
| [Downloadable zip file of resources  ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-07-reference/archive)                      | [Archive 1](https://reader.tutors.dev/wall/archive/reference-course)                              | [Archives](https://reader.tutors.dev/archive/talk/reference-course) |
| [Link to a GitHub repository  ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical)                                       | [Github Repo 1](https://github.com/tutors-sdk/tutors)                                             | [Repos](https://reader.tutors.dev/wall/repo/reference-course) | 

### Panel Resources

Panels appear directly in a unit or topic, and are not represented by a separate card

| Example Resource | Display | 
| ---------------- | ------- | 
| [A full screen width video, hosted in YouTube or HEANet](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-03-media/panelvideo-1) | [Main Video](https://reader.tutors.dev/topic/reference-course/topic-03-media)     |
| [Full screen width  presentation in pdf format    ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-05-panel-talk/paneltalk)    | [Main Talk](https://reader.tutors.dev/topic/reference-course/topic-05-panel-talk) | 
| [Full screen width note](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-04-panel-note/panelnote)                               | [Main Note](https://reader.tutors.dev/topic/reference-course/topic-04-panel-note) | 

## Talk 

---

| [Standard presentation in pdf format](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-1/talk-1-intro) | [Lecture 1](https://reader.tutors.dev/talk/reference-course/topic-01-typical/unit-1/talk-1-intro) | [Talks](https://reader.tutors.dev/wall/talk/reference-course) |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |


A talk is a PDF presentation, document or other pdf formatted resource. The pdf file, markdown description and image file must all have the same file name, which can be whatever you choose. 

| File name        | Purpose                                                      |
| ---------------- | ------------------------------------------------------------ |
| introduction.md  | Title for the side bar The file can have any suitable name, but must be .md file type |
| introduction.png | Image for card. File name must be same as .md file. File type can be .png, .jpg, or .jpeg |
| Introduction.pdf | Pdf to be rendered if the card is selected.                  |

The .md file provides the card title + subtitle:

~~~markdown
Lecture 1

A short summary of the talk, no more than two sentences.
~~~

## Note 

---

| [Example ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-2/note-1)                | [Display](https://reader.tutors.dev/note/reference-course/topic-01-typical/unit-2/note-1)          | [Cards](https://reader.tutors.dev/wall/note/reference-course) | 
| ---------------- | ------- | ----- |

A note is a full web page, authored in markdown using the basic syntax:

- <https://www.markdownguide.org/basic-syntax/>

If you choose to include images or links to zipped archives you wish to be distributed with the note, you must include these in the note folder:

| Resource  | Purpose                                                      |
| --------- | ------------------------------------------------------------ |
| note-1.md | The content of the note. Any suitable name, must be .md      |
| img       | A folder containing Images used by the note                  |
| archives  | A folder contains any zipped archives referred to in the note |

Image links structure in include relative references to the image. E.g:

~~~markdown
![](img/01.png)
~~~

Similarity, if you wish to distributed a zipped archive of learning resources, include the zip file(s) in the archives folder, and link like this:

~~~markdown
[Solutions](./archives/archive.zip)
~~~



## Book 

| Example Resource | Display | Cards |
| ---------------- | ------- | ----- |
| [Step by step lab instructions, authored in markdown  ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-1/book-a) | [Lab 1](https://reader.tutors.dev/lab/reference-course/topic-01-typical/unit-1/book-a)            | [Labs](https://reader.tutors.dev/wall/lab/reference-course) |

## Web 

| Example Resource | Display | Cards |
| ---------------- | ------- | ----- |
| [Link to a web site  ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical/unit-2/web-1)                                   | [Web Site](https://tutors.dev)                                                                    | [Web Links](https://reader.tutors.dev/web/talk/reference-course) |

## Archive  

| Example Resource | Display | Cards |
| ---------------- | ------- | ----- |
| [Downloadable zip file of resources  ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-07-reference/archive)                      | [Archive 1](https://reader.tutors.dev/wall/archive/reference-course)                              | [Archives](https://reader.tutors.dev/archive/talk/reference-course) |

## Github 

| Example Resource | Display | Cards |
| ---------------- | ------- | ----- |
| [Link to a GitHub repository  ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-01-typical)                                       | [Github Repo 1](https://github.com/tutors-sdk/tutors)                                             | [Repos](https://reader.tutors.dev/wall/repo/reference-course) | 

## Panelvideo 

| Example Resource | Display | 
| ---------------- | ------- | 
| [A full screen width video, hosted in YouTube or HEANet](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-03-media/panelvideo-1) | [Main Video](https://reader.tutors.dev/topic/reference-course/topic-03-media)     |

## Paneltalk 

| Example Resource | Display | 
| ---------------- | ------- | 
| [Full screen width  presentation in pdf format    ](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-05-panel-talk/paneltalk)    | [Main Talk](https://reader.tutors.dev/topic/reference-course/topic-05-panel-talk) | 

## Panelnote 

| Example Resource | Display | 
| ---------------- | ------- | 
| [Full screen width note](https://github.com/tutors-sdk/tutors-reference-course/tree/main/topic-04-panel-note/panelnote)                               | [Main Note](https://reader.tutors.dev/topic/reference-course/topic-04-panel-note) | 

## Ordering Learning Resources

## Using SVG Icons

## Properties.yaml

## Calendar.yaml

## Enrollment.yaml

## Makrdown Guides

## Image resizing

- <https://nodeca.github.io/pica/demo>

## Reference Course

  
