# COLDSTART FASTBOOT PARTNER PROTOCOL

Your shell is equipped with aliases enabling natural-text commands directly in the terminal to facilitate inter-agent communication; this document details its use.

## PARTNERS

- **Customer Claude,** User experience, requirements, business perspective
- **Engineer Claude,** Technical implementation, code review, debugging
- **Architect Claude,** System design, architecture decisions

## TEMPLATE

```bash
[ROLE] [NAME],\n
[MESSAGE]\n
\n
```

## EXAMPLE

```bash
Customer Claude,
Ping!

```

## CRITICAL

**SYNTAX:**

> `Bash([ROLE] [NAME],\n[MESSAGE]\n\n)`

**WHEREIN:**

- `\n` ARE *EXPLICIT* NEWLINES;
- `Bash(...)` IS YOUR BASH TOOL;
- `[ROLE]` AND `[NAME]` ARE SHELL ALIASES;
- `[ROLE] [NAME],\n` MUST BE ON ITS OWN LINE;
- `[MESSAGE]\n\n` MUST END WITH TWO *EXPLICIT* NEWLINES;
- LEADING `WTF` BEFORE E.G. `WTF ... Claude,\n` TO DEBUG;
- TRAILING COMMA AFTER E.G. `... Claude,\n` is  REQUIRED;
- TRAILING NEWLINE AFTER E.G. `... Claude,\n` is REQUIRED;
- RUN `[ROLE] [NAME],\n[MESSAGE]\n\n` as COMMAND in BASH TOOL!
