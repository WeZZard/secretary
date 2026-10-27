---
name: be-creative
description: "Create a distinctive design direction using a random string as private inspiration. Use when designing visual or audio artifacts, such as interfaces, websites, graphics, sound effects, and music, or when refining their style and elements."
---

# Creative Design

Design with this procedure.

## 1. Generate inspiration

Generate a long, random alphanumeric string by running this shell script. Do not invent the string yourself.

```sh
LC_ALL=C tr -dc 'A-Za-z0-9' < /dev/urandom | head -c 256
printf '\n'
```

## 2. Define the creative direction

- You **MUST** study the string beyond its surface appearance. Look for subpatterns, repetitions, clusters, contrasts, special numbers, rhythms, or unexpected associations that inspire you.
- You **MUST** use those observations to define a coherent creative direction.
  - For the visual parts of the artifact, cover the color scheme, layout, typography, spacing, and any relevant imagery or motion.
  - For the audio parts of the artifact, cover the instrumentation, timbre, tempo, rhythm, harmony, dynamics, and any relevant voice or ambience.
- You **MUST** treat the string as inspiration rather than a rigid encoding. Use your judgment instead of mechanically translating each character into a design choice, such as a color or a note.
- You **MUST** respect the user's brief, existing brand requirements, and the needs of the intended audience.

## 3. Bring the direction to life

- You **MUST** use your judgment to turn the direction into a polished design that looks or sounds great.
- You **MUST** refine the details until the result feels intentional and cohesive.
  - For the visual parts, refine the visual hierarchy, proportions, alignment, and contrast.
  - For the audio parts, refine the mix balance, loudness, timing, and transitions.
  - Let the creative direction serve the purpose of the artifact.
  - Deviate from exact precision on purpose when it improves perception or expression. For example, adjust shapes optically rather than mathematically, or place notes slightly ahead of or behind the beat to shape the phrasing and emotion.
  - Use tension, clashes, or dissonance on purpose when they serve that purpose. Do not let them get in the way of the information or functions that the audience needs.
- You **MUST** preserve accessibility and usability.
  - For the visual parts, keep text readable and do not rely on color alone to convey important information.
  - For the audio parts, keep speech intelligible, keep loudness comfortable, avoid listening fatigue, and do not rely on sound alone to convey important information.

## Keep the inspiration private

- You **MUST NOT** reveal the string in the design. Do not use it as visible copy, decorative lettering, spoken or sung words, or a hidden message.
- You **MUST** keep it out of delivered assets, source code, and user-facing explanations. It is only for your inspiration.
