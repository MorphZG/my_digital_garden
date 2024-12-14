---
{"dg-publish":true,"permalink":"/000-workflow/","title":"My Obsidian Workflow","tags":["index","obsidian"]}
---


# My Obsidian Workflow

Even the longest journey starts with a single step. I was searching for a way to organise knowledge and remember it, and there are many very good systems that can help. The best option might be to find a system you like and then customise and reorganise it to fit your needs.

## Directories

>[!Note] Underscores and Private Directories
>Inspired by the programming concept of private variables, these directories are used by the system to store things that the general public (or readers) need not bother with. Examples include:
> - `_assets`: Storage of images or other files used in notes
> - `_templates`: Storage of note templates
> - `_calendar`: Storage of daily notes
> - `_dataview_database`: Dataview queries
> - And so on...

- **00_Fleeting_inbox**
	- Fleeting notes or inbox directory is a place where fresh notes start. This is a starting point for notes that still need to be refined, quick thoughts, and work in progress. Conduct a weekly review; completed notes should move forward into one of the following categories.

- **01_Reference**
	- This directory is for practical knowledge. From tools and software to life and philosophy, reference notes are here to quickly scan through if needing a reminder.

- **02_Ideas_and_projects**
	- These are my own ideas and personal thoughts. A place to start and manage personal projects, akin to a cooking pot with different ingredients, almost ready to be served. Unlike references, these are my own views on particular subjects which can but don't have to be right.

- **03_Literature_notes**
	- Literature doesn't have to be a physical book, it can be a digital article or a blog post. While `01_Reference` directory have very practical notes, literature notes are wider range of ideas and personal thoughts about different concepts. When taking literature notes be mindful of a structure but also take note of important metadata.
	- Read more about [[00_Fleeting_inbox/literature notes structure\|effective literature notes]]

- **04_Expressions**
	- After collecting enough knowledge and different ideas, when there is enough to encapsulate written words into my own expressions, I will share them online. This is the directory where everything comes together.

- **05_Archive**
	- **Never delete notes, archive them**
	- Place for all notes that you wish to remove from the current structure. Never delete them; keep them in the Archive so you can search them, read them, and maybe even revive them in the future.

## Important properties

There are two types of properties i will use, essential and optional. Essential properties must be included since those will help indexing and finding the relevant notes. Some plugins like `Dataview` requires metadata to be included so you can query relevant information. In future i will probably use some static site generators or frameworks to publish my notes as an [[online digital garden\|online digital garden]]. Such frameworks require properties like `title` and `description` to improve search engine optimisation, or `published` being set to `true` or `false` which enables you to store the written note as an draft while you still work on it.

Create the [[_dataview_database/index\|Dataview index]] to query the list of available frontmatter properties. It is important to review the index file with key-value pairs that are used often and don't create new key-value pairs if it is not necessary. If i already have `source: web` there is no need to create additional `source: article` and `source: blog`. If i already have `URL` property there is no need to create additional `link` property. Not going to wide will help later when you need to search for information.

>[!tip]- Essential properties
>- **tags**: List datatype. With not more than 3 tags. It is crucial to minimise number of tags to make them more specific.
>- **type**: String datatype, double quoted. Indicates the type of a note with only one input value set from the currently available values listed under [[000_Workflow#Type property\|#Type property]]

>[!tip]- Optional properties
>- **date**: Date datatype.
>- **source**. String datatype, source for reference notes
>- **author**: String datatype, author of source
>- **title**: String datatype, title of source
>- **URL**: String datatype, link to source

## Type property

>Utilising YAML frontmatter, **type**  is essential property that must be set for every file and with only one value written as a double quoted string.

It would be a mess going to wide with different types of notes. It will for sure loose the purpose. When i see a need to expand the list of available values i will for sure add more.

### Current type values

>TODO: List all available values with short explanation for each

## Plugins

- **Dataview**
	- Treat your Obsidian Vault as a database which you can query. Create dynamic views of your notes. For instance, you can create a table of all notes tagged with `#project` or a list of all `#reference` notes with a specific tag. It provides a JavaScript API and pipeline-based query language for filtering, sorting, and extracting data from Markdown pages. More info can be found at [GitHub](https://github.com/blacksmithgu/obsidian-dataview).

- **Templater**
	- Templater is a template language that lets you insert variables and function results into your notes. It also lets you execute JavaScript code manipulating those variables and functions. With Templater, you can create powerful templates to automate manual tasks. Documentation is available at [silentvoid13.com](https://silentvoid13.github.io/Templater/).

- **Excalidraw**
	- The Obsidian-Excalidraw plugin integrates Excalidraw, a feature-rich sketching tool, into Obsidian. You can store and edit Excalidraw files in your vault, embed drawings into your documents, and link to documents and other drawings. For a showcase of Excalidraw features, browse the [GitHub repository](https://github.com/excalidraw/excalidraw).

## Linking Notes

I'm still looking for a well-structured way to link notes. Options include:
- Footnotes
- Tags and front matter
- Inline styled wiki links

Each method has pros and cons. Currently, the most organised approach seems to be a combination of front matter tags and linking everything at the bottom as a footnote or reference section.

## References

[[04_Expressions/productivity/my note on notetaking\|my note on notetaking]] - personal note
[[_dataview_database/index\|index page]] - personal note
[[01_Reference/productivity/Building a second brain\|Building a second brain]] - book reference
[[01_Reference/productivity/How to take smart notes\|How to take smart notes]] - book reference
