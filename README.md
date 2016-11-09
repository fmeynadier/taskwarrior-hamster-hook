# taskwarrior-hamster-hook
A minimal hook for TaskWarrior to help tracking time with hamster-cli

## Prerequisites

- Taskwarrior (>= 2.4)
- <code>hamster-cli</code> (>= 2.91.3) (<code>hamster</code> in fedora)
- python (>= 3.3)

## Installation

- Copy or link on-modify.hamster into $HOME/.task/hooks/
- Make sure it is executable

## Usage

Start and stop tasks using the usual commands in Taskwarrior.

If a "start" is detected, hook will call "hamster-cli start [Task description]@[project], #[TAG1],#[TAG2] "

If a "stop" is detected, hook will call "hamster-cli stop" (effectively stopping any task currently active in hamster).

The '#' and '@' characters within any field (description, project, tags) are replaced by '\_' in order to avoid incorrect parsing.

