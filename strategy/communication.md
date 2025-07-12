<!--
SPDX-FileCopyrightText: © 2025 open-nudge <https://github.com/open-nudge>
SPDX-FileContributor: szymonmaszke <github@maszke.co>

SPDX-License-Identifier: Apache-2.0
-->

# Communication

## Table Of Contents

- [Definitions](#definitions)
- [Rules](#rules)
- [Schedule](#schedule)
- [Platforms](#platforms)
    - [Platform manager](#platform-manager)
- [Timing](#timing)
    - [Specific](#specific)
    - [Exemplary](#exemplary)
- [Schedule](#schedule)

## Definitions

- __Unit__ - new project or a new release of the existing project
- __Ready project__ - project which is `~90%+` ready for publishing
    (or at most one week of work left)

## Rules

- Communication is mostly one-way, from the project to the audience,
    except for:

    - technical discussions, mostly on GitHub or similar platforms
    - commercial client-related discussions, performed
        on a case-by-case basis and according to client needs
    - __main__ channel (usually with limited interaction, e.g. answering
        tech-related questions, etc.)

- All published posts are related to __Units__, no other posting activity
    allowed (with an eventual exceptions for __main__ channel)

- Comments have to be unit-related, no off-topic discussions allowed;
    possible exceptions __only__ on the main channel

## Schedule

Schedule is done based on the project readiness and Buffer
scheduling tool.

- If `5` or more units are ready, release them every week
- If `3-5` units are ready, release them every two weeks
- If `2` units are ready, release them every month
- If `1` unit is ready, release every quarter

Exact publishing schedule is subject to change based on:

- Workload and bug fixing on current projects maintenance
- Contributors availability

## Content

Content should be related to the unit and posses the following traits:

- comprehensive description

- many links to related resources

- __all links should be markdown hidden__ EXCEPT:

    - links to the project repository (e.g. GitHub)
    - links to starring the project on GitHub
    - links to LinkedIn or Twitter profiles

- contain "boilerplate" like links to social media

### Boilerplate

These boilerplate information should be included especially in promotional
posts on Reddit or HackerNews.

#### Header

> [!CAUTION]
> __Adjust appropriately based on the project__

For reddit/hackernews:

```markdown
## Introducing <NAME>!

Hey, I have created <NAME> which <DESCRIPTION>.
```

For twitter/linkedin:

```markdown
Introducing <NAME>, which is <DESCRIPTION>!
```

<!-- pyml disable line-length-->

For all platforms:

```markdown

Starring the repo and liking/sharing this post is greatly appreciated!

> __GitHub repository__: https://github.com/open-nudge/<NAME>
```

<!-- pyml enable line-length-->

For `reddit` and `hackernews`:

```markdown
Stay up to date with new tools from opennudge:

- __LinkedIn__: https://www.linkedin.com/company/opennudge
- __Twitter/X__: https://x.com/opennudge
```

#### Footer

> [!CAUTION]
> __Adjust appropriately based on the project
> and only use it on `reddit`/`hackernews` platforms__

<!-- pyml disable line-length-->

```markdown
## Check it out yourself!

- __GitHub repository__: https://github.com/open-nudge/<NAME>
- Full documentation [here](https://open-nudge.github.io/<NAME>/latest/)
- __FOSS Python template ensuring high project quality — and ready for your own use__: https://github.com/open-nudge/opentemplate

If you find this project useful or interesting please consider:

- __Starring the repository on GitHub here__: https://github.com/open-nudge/<NAME>
- __Liking or commenting on this post__
```

<!-- pyml enable line-length-->

For `reddit` and `hackernews`:

```markdown

Stay up to date with new tools from opennudge:

- __LinkedIn__: https://www.linkedin.com/company/opennudge
- __Twitter/X__: https://x.com/opennudge
```

For any platform finish off with:

```markdown
Thanks so much for your interest and support — it truly means a lot!
```

## Platforms

Publishing platforms are separated into three categories:

- __targeted__ - used to publish units targeting specific audience
    and to answer unit-related questions
- __official__ - everything targeted includes, plus official
    announcements, job postings and other general information
- __main__ - one platform (subject to change), includes
    everything in official and targeted channels, plus
    a limited option to interact with the current events

The following platforms were identified:

- [twitter](https://www.x.com/) - main channel

- [threads](https://www.threads.com/) - secondary channel

- [linkedin](https://www.linkedin.com/) - official channel

- [reddit](https://www.reddit.com/) - targeted channel,
    with the following subreddits (chosen based on the project's topic,
    listed in the order of audience size):

    - [r/MachineLearning](https://www.reddit.com/r/MachineLearning/)
    - [r/python](https://www.reddit.com/r/python/)
    - [r/cybersecurity](https://www.reddit.com/r/cybersecurity/)
    - [r/devops](https://www.reddit.com/r/devops/)

- [hackernews](https://hackernews.com)/ - targeted channel

### Platform manager

[Buffer](https://buffer.com/) is used to manage platforms which
are available as a direct integration.

> [!NOTE]
> Buffer automatically manages the posting schedule, but some manual
> adjustments might be necessary

## Timing

> [!CAUTION]
> Buffer scheduling tool is used to manage the timing of the posts,
> consider information below as a guideline

> [!NOTE]
> Schedules target primarily US (PDT time zone) or European (UTC) audience

Essential factors to consider:

- "Work-related" platforms ([linkedin](https://www.linkedin.com/)) should be
    targeted during the workweek, mornings (8:00-12:00)
- "Leisure" platforms (reddit, hackernews) should be targeted during
    weekends, evenings (18:00-22:00)
- "Informative" platforms ([twitter](https://www.x.com/)) should be
    targeted during the evenings (18:00-22:00)

> [!CAUTION]
> Schedules should be considered merely a guideline

### Specific

Timing is platform specific based on (approximate) best time to post, specifically:

- [twitter](https://www.x.com/) - evenings (18:00-22:00),
    Sunday/Saturday/Thursday; [source](https://besttimetopost.blue/howard.fm)
- [threads](https://www.threads.com/) - evenings (18:00-22:00),
    Thursday 8:00 ([source](https://www.hopperhq.com/blog/best-time-to-post-on-threads/))
- [linkedin](https://www.linkedin.com/) - mornings (8:00-12:00),
    Tuesdays/Thursdays/Wednesdays
- [reddit](https://www.reddit.com/) - evenings (18:00-22:00),
    Monday/Saturday/Sunday (you can use
    [this tool](https://dashboard.laterforreddit.com/analysis)
    to target specific subreddits);
    [source](https://dashboard.laterforreddit.com/analysis/?subreddit=r%2FMachineLearning&threshold=100&period=year)
- [hackernews](https://hackernews.com)/ - Sunday/Saturday/Wednesday
    (mornings, 11:00-12:00)

> [!CAUTION]
> This is an initial schedule, subject to change based on audience engagement
> and further analysis

### Exemplary

- Twitter - Sunday at 20:00 UTC
- Threads - Sunday at 20:00 UTC
- Reddit - Monday at 20:00 UTC
- LinkedIn - Tuesday at 10:00 UTC
- Hackernews - Wednesday at 11:00 UTC
