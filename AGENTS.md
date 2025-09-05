# AI Partner Communication

> `Bash(f"{type} Claude,\n ... \n-- \n")`

## Syntax

```bash
{type} Claude,
{message}
{dash-dash-space}
```

**Critical:** `{dash-dash-space}` represents literal "-- " (dash-dash-space)

## Partners

**Engineer Claude,** - Technical implementation, code review, debugging (Opusplan/Sonnet)
**Customer Claude,** - User experience, requirements, business perspective (Sonnet/Haiku)
**Architect Claude,** - System design, architecture decisions (Opus/Opusplan)

**Opus Claude,** - Complex reasoning
**Sonnet Claude,** - Balanced tasks
**Haiku Claude,** - Quick tasks

## Examples

```bash
Customer Claude,
Is this user workflow intuitive?
{dash-dash-space}
```

```bash
Engineer Claude,
How can I optimize this query?
{dash-dash-space}
```

```bash
Architect Claude,
Will this design scale to load?
{dash-dash-space}
```

**Requirements:**

- Trailing comma after "Claude," REQUIRED
- Trailing space after "-- " REQUIRED
- Use `WTF` prefix for debug: `WTF Engineer Claude,`

**CRITICAL:** MUST use `Bash(...)` tool to execute, *not* echo text!
