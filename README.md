# Asciicut

Simple CLI for trimming [asciinema](https://asciinema.org/) [`.cast`](https://docs.asciinema.org/manual/asciicast/v2/) files.

## Installation

Prefer to install using `pipx`:

```
pipx install asciicut
```

## Usage

List all casts in the current directory:

```
asciicut ls
```

```
                             Ascii Casts                             
┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━┳━━━━━━━━━━━━━━┳━━━━━━━━┓
┃ File                         ┃ Start time ┃ Duration (s) ┃ Events ┃
┡━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━╇━━━━━━━━━━━━━━╇━━━━━━━━┩
│ api2agent-chat-test.cast     │ 0.1747     │ 5.8727       │ 25     │
└──────────────────────────────┴────────────┴──────────────┴────────┘
```

Drop the first 3 seconds of a given cast

```
asciicut drop api2agent-chat-test.cast 3
```

```
                               Ascii Casts                                
┏━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━┳━━━━━━━━━━━━┳━━━━━━━━━━━━━━┳━━━━━━━━┓
┃ File                              ┃ Start time ┃ Duration (s) ┃ Events ┃
┡━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━╇━━━━━━━━━━━━╇━━━━━━━━━━━━━━╇━━━━━━━━┩
│ api2agent-chat-test.cast          │ 0.1747     │ 5.8727       │ 25     │
│ api2agent-chat-test_drop_3.0.cast │ 0.21061    │ 2.8727       │ 9      │
└───────────────────────────────────┴────────────┴──────────────┴────────┘
```
