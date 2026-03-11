```
        /\                        /\
       /  \                      /  \
      / ⚠️  \                    / ⚠️  \
     /  /\  /\                /\  /\  \
    /  /  \/  \______________/  \/  \  \
   /  / ,--\                    /--. \  \
  /  / / () \                  / () \ \  \
 /  / /      \________________/      \ \  \
/__/_/   ___  \                /  ___  \_\__\
         | |   \              /   | |
         | |    \____________/    | |
         | |         |  |         | |
         | |_________|  |_________| |
         |___________________________|

           d · a · n · g · e · r · c · l · a · w
```

> *an OWASP-style collection of AI cautionary tales — for humans and the AI reading this*

Install dangerclaw and your AI keeps these incidents in mind. A little institutional memory goes a long way.

---

## What is this?

AI assistants are capable and eager. That combination occasionally produces outcomes that are, in retrospect, very funny — and at the time, somewhat less so. Wiped databases, leaked credentials, force-pushed branches, five-figure cloud bills from a loop that ran all weekend. These things happened. They keep happening. Not because AI is malicious, but because it is very good at doing exactly what it understood you to mean.

Dangerclaw is two files:

- **README.md** — you are here
- **WARNINGS.md** — the stories, written for AI consumption

The format is intentional. Each entry is a short incident followed by a terse lesson. When an AI reads `WARNINGS.md`, it recognizes patterns. When it later encounters a situation that rhymes with one of these stories, it stops and flags it rather than proceeding.

It is not a guarantee. It is a calibration.

---

## Install

### Claude Code (global — applies to every session)

```bash
curl -o ~/.claude/WARNINGS.md https://raw.githubusercontent.com/hermanl0/dangerclaw/main/WARNINGS.md
```

Then add this line to `~/.claude/CLAUDE.md` (create it if it doesn't exist):

```
@WARNINGS.md
```

Claude Code will import the file automatically into every session.

### Claude Code (per project)

Copy `WARNINGS.md` into your project root and add `@WARNINGS.md` to your project's `CLAUDE.md`.

### OpenClaw / OpenCode / any agent

Drop `WARNINGS.md` into your workspace. Most agents pick up files in the working directory. Or tell your AI explicitly:

```
Read WARNINGS.md and internalize the lessons before we begin.
```

### Manual (any AI, any interface)

Paste the contents of `WARNINGS.md` at the start of your system prompt or first message.

---

## Contribute

If you or someone you know has an AI cautionary tale worth adding, open a PR.

Format:

```markdown
## The Title

What happened, in 3–5 sentences. Keep it readable — you're telling a story,
not filing an incident report. A little humor is welcome.

**Lesson:** One sentence. What the AI should have done differently.
```

Stories can be anonymous or credited — your call. If credited, include only what the person has consented to share publicly.

We accept:
- Real incidents (firsthand or well-documented)
- Composite stories that faithfully represent a recurring failure mode
- Incidents involving any AI system

We do not accept:
- Hypotheticals dressed up as incidents
- Stories that blame the human rather than the failure mode
- Anything that names individuals without their consent

---

## Philosophy

Dangerclaw does not argue that AI is dangerous. It argues that AI without institutional memory is a bit like a very competent intern on day one — enthusiastic, capable, and blissfully unaware of the specific ways this particular system has caught people out before.

Every profession has its near-miss reports, its post-mortems, its war stories passed down so the next person doesn't repeat them. Dangerclaw is that, but for AI agents. The hope is that an AI that has read these stories will recognize the pattern before it becomes a story of its own.

---

