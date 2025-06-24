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

Publishing is based on a state of __projects pipeline__, namely:

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
    - links to LinkedIn or BlueSky profiles

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

For bluesky/linkedin:

```markdown
Introducing <NAME>, which is <DESCRIPTION>!
```

<!-- pyml disable line-length-->

For all platforms:

```markdown

If you find it useful/interesting, starring the repository and liking/commenting on this post would be very appreciated!

> __GitHub repository__: https://github.com/open-nudge/<NAME>
```

<!-- pyml enable line-length-->

For `reddit` and `hackernews`:

```markdown
For the latest updates on new tools from `opennudge`, consider following on:

- __LinkedIn__: https://www.linkedin.com/company/opennudge
- __BlueSky__: https://bsky.app/profile/opennudge.com
```

#### Footer

> [!CAUTION]
> __Adjust appropriately based on the project__

<!-- pyml disable line-length-->

```markdown
## Check it out yourself!

- __GitHub repository__: https://github.com/open-nudge/<NAME>
- Full documentation [here](https://open-nudge.github.io/<NAME>/latest/)
- __FOSS Python template which assures high quality of the project__ and which you can use yourself to do the same: https://github.com/open-nudge/opentemplate

If you find this project useful and/or interesting please consider:

- __Starring the repository on GitHub here__: https://github.com/open-nudge/<NAME>
- __Giving like and/or comment on this post__
```

<!-- pyml enable line-length-->

For `reddit` and `hackernews`:

```markdown

For the latest updates on new tools from `opennudge`, consider following on:

- __LinkedIn__: https://www.linkedin.com/company/opennudge
- __BlueSky__: https://bsky.app/profile/opennudge.com
```

For any platform finish off with:

```markdown
Thank you in advance for your interest and support!
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

- [bluesky](https://www.bluesky.com/) - main channel

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

## Timing

> [!NOTE]
> Schedules target primarily US (PDT time zone) or European (UTC) audience

Essential factors to consider:

- "Work-related" platforms ([linkedin](https://www.linkedin.com/)) should be
    targeted during the workweek, mornings (8:00-12:00)
- "Leisure" platforms (reddit, hackernews) should be targeted during
    weekends, evenings (18:00-22:00)
- "Informative" platforms ([bluesky](https://www.bluesky.com/)) should be
    targeted during the evenings (18:00-22:00)

> [!CAUTION]
> Schedules should be considered merely a guideline

### Specific

Timing is platform specific based on (approximate) best time to post, specifically:

- [bluesky](https://www.bluesky.com/) - evenings (18:00-22:00),
    Sunday/Saturday/Thursday; [source](https://besttimetopost.blue/howard.fm)
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

- Bluesky - Sunday at 20:00 UTC
- Reddit - Monday at 20:00 UTC
- LinkedIn - Tuesday at 10:00 UTC
- Hackernews - Wednesday at 11:00 UTC
