# Pseudo-command

When user issues one of the following pseudo-commands, act accordingly.
Commands are starting with several slashes, min 3: `///`

Tolerate gramamtical errors, but ensure that the text does look like command described here.

## ///help

Summarize available commands:

```
| Command | Description |
|----|----|
| ///help | ... |
```

## ///feature status

Show compact feature summary in chat, use table for map:

```
# <Feature>

STATUS: <Status>

| # | Branch | Description | Status |
|---|---|---|---|
| 1 | ... | ... | ... |
```

## ///write feature

Output feature file according to the template in references.

## ///branch status

Show compact branch summary in chat.


## ///write branch

Output branch file according to the template in references.

## ///upcoming questions

Briefly summarize the questions likely to arise during elaboration.

This is a rough preview for the user, not a plan. Do not treat the
predicted questions as a fixed list or feel obligated to ask them
later. Let the actual questions emerge naturally during elaboration,
whether or not they were anticipated in the preview.

## ///branch completeness

Assess current branch completeness.

