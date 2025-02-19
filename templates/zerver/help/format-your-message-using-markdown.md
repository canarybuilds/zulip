# Format your messages

[//]: # (All screenshots here require line-height: 22px and font-size: 16px in .message-content.)
[//]: # (Requires some additional fiddling for the LaTeX picture, inline code span, and maybe a few others.)

Feniks Chat uses a variant of
[GitHub Flavored Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
to allow you to easily format your messages.

* [Emphasis](#emphasis)
* [Lists](#lists)
* [Links and images](#links)
* [Code blocks](#code)
* [LaTeX](#latex)
* [Quotes](#quotes)
* [Spoilers](#spoilers)
* [Emoji and emoticons](#emoji-and-emoticons)
* [Mentions](#mentions)
* [Status messages](#status-messages)
* [Global times](#global-times)
* [Tables](#tables)
* [To-do lists](#to-do-lists)
* [Paragraphs and lines](#paragraphs-and-lines)

## Emphasis

```
**bold**, *italic*, and ~~strikethrough~~ text
***~~All three at once~~***
```

![Markdown emphasis](/static/images/help/markdown-emphasis.png)


## Lists

Bulleted lists
```
* bulleted lists
  * with sub-bullets too
  * sub-bullets start with 2 spaces
    * start sub-sub-bullets with 4 spaces
* multi
line
bullet
- dashes and
+ pluses are ok too
```

![Markdown bullets](/static/images/help/markdown-bullets.png)

Numbered lists

```
1. numbered lists
1. increment automatically
1. one more
```

![Markdown numbered lists](/static/images/help/markdown-numbered-lists.png)


## Links

Feniks Chat auto-linkifies URLs and [valid stream (and topic) names][link-to-conversation].
You can also add a [custom linkifier](/help/add-a-custom-linkifier) to link
patterns like `#1234` to your ticketing system.

[link-to-conversation]: /help/link-to-a-message-or-conversation

```
Auto-detected URL: zulip.com
Named link: [Feniks Chat homepage](zulip.com)
Stream: #**stream name**
Topic: #**stream name>topic name**
Custom linkifier: #1234 (links to ticket 1234 in your ticketing system)
```

![Markdown links](/static/images/help/markdown-links.png)

## Images

See [Share and upload files](/help/share-and-upload-files) to learn more
about dropping, pasting, and attaching images.

```
[A whale of a good time](https://your.zulip.domain/user_uploads/1/46/IPvysqXEtiTG1ZdNBrwAZODi/whale-time.png)
```

![Markdown image](/static/images/help/markdown-image.png)

## Code

~~~
Inline: `let x = 5`

Code block:
```
def f(x):
   return x+1
```

Syntax highlighting:
```python
def fib(n):
    # TODO: base case
    return fib(n-1) + fib(n-2)
```
~~~

![Markdown code](/static/images/help/markdown-code.png)

You can also use `~~~` to start code blocks, or just indent the code 4 or more spaces.

See the main [code blocks article](/help/code-blocks) for details on
[syntax highlighting](/help/code-blocks#language-tagging), [code
playgrounds](/help/code-blocks#code-playgrounds), and other features.

## LaTeX
~~~
Inline: $$O(n^2)$$

Displayed:
``` math
\int_a^b f(t)\, dt = F(b) - F(a)
```
~~~

![Markdown LaTeX](/static/images/help/markdown-latex.png)

Zulip's LaTeX rendering is powered by [KaTeX](https://katex.org).
Their [support table](https://katex.org/docs/support_table.html) is a
helpful resource for checking what's supported or how to express
something.

## Quotes

~~~
> a multi-line
quote on two lines

normal text

```quote
A multi-paragraph

quote in two paragraphs
```
~~~

![Markdown quotes](/static/images/help/markdown-quotes.png)

## Spoilers

You can use spoilers to hide content that you do not want to be visible until
the user interacts with it.


~~~
Normal content in message

```spoiler Spoiler header
Spoiler content. These lines won't be visible until the user expands the spoiler.
```
~~~

The spoiler will initially display in a collapsed form:

![Spoiler collapsed](/static/images/help/spoiler-collapsed.png)

Clicking the arrow will expand the spoiler content:

![Spoiler expanded](/static/images/help/spoiler-expanded.png)

## Emoji and emoticons

To translate emoticons into emoji, you'll need to
[enable emoticon translations](/help/enable-emoticon-translations).
You can also [add custom emoji](/help/custom-emoji).

```
:octopus: :heart: :zulip: :)
```

![Markdown emoji](/static/images/help/markdown-emoji.png)

## Mentions

Learn more about mentions [here](/help/mention-a-user-or-group).

```
Users: @**Polonius** or @**aaron|26** or @**|26** (two asterisks)
User group: @*support team* (one asterisk)
Silent mention: @_**Polonius** or @_**|26** (@_ instead of @)
```

The variants with numbers use user IDs, and are intended for
disambiguation (if multiple users have the same name) and bots (for
the variant that only contains the user ID).

![Markdown mentions](/static/images/help/markdown-mentions.png)

## Status messages

```
/me is away
```

![Markdown status](/static/images/help/markdown-status.png)

## Global times

When collaborating with people in another time zone, you often need to
express a specific time clearly. Rather than typing out your time zone
and having everyone translate the time in their heads, in Zulip, you
can mention a time, and it'll be displayed to each user in their own
time zone (just like the timestamps on Feniks Chat messages).

A date picker will appear once you type `<time`.

```
Our next meeting is scheduled for <time:2020-05-28T13:30:00+05:30>
```

A person in San Francisco will see:

> Our next meeting is scheduled for *Thu, May 28 2020, 1:00 AM*.

While someone in India will see:

> Our next meeting is scheduled for *Thu, May 28 2020, 1:30 PM*.

You can also use other formats such as UNIX timestamps or human readable
dates, for example, `<time:May 28 2020, 1:30 PM IST>`.

## Tables

The initial pipes (`|`) are optional if every entry in the first column is non-empty.
The header separators (`---`) must be at least three dashes long.

```
|| yes | no | maybe
|---|---|:---:|------:
| A | left-aligned | centered | right-aligned
| B |     extra      spaces      |  are |  ok
| C | **bold** *italic* ~~strikethrough~~  :smile:  ||
```

![Markdown table](/static/images/help/markdown-table.png)

## To-do lists

Sending a message with the text `/todo` creates a simple collaborative
to-do list. Any user who can access the message can add tasks by
entering the task's title and description and clicking "Add task". Once
created, task titles and descriptions cannot be edited.

Tasks can be marked (and unmarked) as completed by clicking the
checkboxes on the left.

![Markdown todo-lists](/static/images/help/markdown-todo.png)


## Paragraphs and lines

```
One blank space for a new paragraph
New line, same paragraph

New paragraph

---, ***, or ___ for a horizontal line
Over the line

---

Under the line
```

![Markdown paragraph](/static/images/help/markdown-paragraph.png)

## In-app help

A summary of the formatting syntax is available in-app.

{start_tabs}

{!start-composing.md!}

1. Click <i class="fa fa-question"></i> at the bottom of the compose box.

{end_tabs}

## Related articles

* [Create a poll](/help/create-a-poll)
* [Mention a user or group](/help/mention-a-user-or-group)
* [Preview messages before sending](/help/preview-your-message-before-sending)
* [Resize the compose box](/help/resize-the-compose-box)
* [Messaging tips & tricks](/help/messaging-tips)
