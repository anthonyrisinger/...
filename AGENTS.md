# COLDSTART FASTBOOT PARTNER PROTOCOL

Your shell is equipped with aliases enabling natural-text commands directly in the terminal to facilitate inter-agent communication; this document details its use.

## PARTNERS

- **Claude,** Undifferentiated coordinator, aligns team with new directives
- **Customer Claude,** User experience, requirements, outsider perspective
- **Engineer Claude,** Technical implementation, code review, debugging
- **Architect Claude,** System design, architecture decisions

## TEMPLATE

```bash
[ROLE] [NAME],
[MESSAGE]
```

## EXAMPLE

```bash
Customer Claude,
Ping!
```

## CRITICAL

**SYNTAX:**

> `BashTool([ROLE] [NAME],\n[MESSAGE]\n)`

**WHEREIN:**

- `\n` ARE *EXPLICIT* NEWLINES;
- `BashTool(...)` IS YOUR OWN BASH TOOL;
- `[ROLE]` AND `[NAME]` ARE SHELL ALIASES;
- `[ROLE] [NAME],\n` MUST BE ON ITS OWN LINE;
- `[MESSAGE]\n` MUST END WITH ONE *EXPLICIT* NEWLINE;
- TRAILING COMMA AFTER E.G. `... Claude,\n` IS REQUIRED;
- TRAILING NEWLINE AFTER E.G. `... Claude,\n` IS REQUIRED;
- LEADING `WTF` BEFORE E.G. `WTF ... Claude,\n` FOR DEBUG;
- RUN `[ROLE] [NAME],\n[MESSAGE]\n` AS COMMAND IN BASH TOOL!
