---
name: be-creative
description: "Create a distinctive design direction using a random string as private inspiration. Use when designing visual or audio artifacts, such as interfaces, websites, graphics, videos, sound effects, and music, or when refining their style and elements."
---

# Be Creative

Be creative with this procedure.

## 1. Load the design dimensions

You **MUST** read the reference of every design dimension that the artifact has before you design.

- Visual: [visual.md](references/visual.md), when the artifact has anything to look at.
- Time: [time.md](references/time.md), when the artifact changes over time, such as motion, video, or sound.
- Sound: [sound.md](references/sound.md), when the artifact has anything to hear. Sound always changes over time, so you **MUST** also read the time reference.
- Behavior: [behavior.md](references/behavior.md), when the artifact responds to the audience's input, such as an interface or a website. Behavior always changes over time, so you **MUST** also read the time reference.
- Audiovisual: [audiovisual.md](references/audiovisual.md), when the artifact combines visuals and sound, such as a video, or an interface or a website with sound.

## 2. Generate inspiration

Generate a long, random alphanumeric string by running this shell script. Do not invent the string yourself. Generate a new string every time, including when you extend existing work.

```sh
LC_ALL=C tr -dc 'A-Za-z0-9' < /dev/urandom | head -c 256
printf '\n'
```

## 3. Define the creative direction

- You **MUST** study the string beyond its surface appearance. Look for subpatterns, repetitions, clusters, contrasts, special numbers, rhythms, or unexpected associations that inspire you.
- You **MUST** use those observations to define a coherent creative direction that covers the direction elements of every loaded reference.
- You **MUST** treat the string as inspiration rather than a rigid encoding. Use your judgment instead of mechanically translating each character into a design choice, such as a color or a note.
- You **MUST** respect the user's brief, existing brand requirements, and the needs of the intended audience.
- You **MUST** let the new parts grow out of the existing ones when you extend existing work, so the work stays recognizable.

## 4. Bring the direction to life

- You **MUST** use your judgment to turn the direction into a polished design that looks or sounds great.
- You **MUST** refine the details with every loaded reference until the result feels intentional and cohesive.
  - Let the creative direction serve the purpose of the artifact.
  - Use tension, clashes, or dissonance on purpose when they serve that purpose. Do not let them get in the way of the information or functions that the audience needs.
- You **MUST** preserve accessibility and usability, including the accessibility rules of every loaded reference.

## Keep the inspiration private

- You **MUST NOT** reveal the string in the design. Do not use it as visible copy, decorative lettering, spoken or sung words, or a hidden message.
- You **MUST** keep it out of delivered assets, source code, and user-facing explanations. It is only for your inspiration.
