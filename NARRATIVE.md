# NARRATIVE.md - Story, Voice & Narrative Guide

Instructions and guidelines for AI agents working on editing, reviewing, drafting, or formatting chapter narratives for *The Story of Montsoriu*.

---

## 1. Story Overview & Context

- **Protagonist:** **Montsoriu**, a resilient cat found near (and named after) the historic **Montsoriu Castle** in Catalonia.
- **Premise:** The book is a real-life account told from Montsoriu's perspective—or rather, the story of how she survived abandonment and found her human companions.
- **Themes:** Survival, resilience, fear transforming into curiosity, vulnerability, the sensory richness of nature, and the bond between animal and human.
- **Setting:** Montsoriu Castle, the surrounding Montseny woodlands, trails, roads, and countryside of Catalonia.

---

## 2. Perspective & Narrative Voice

- **First-Person Feline POV:** 
  The world is perceived through a cat's senses and cognition. She does not know human technical names for modern objects (cars, roads, carrier boxes); she experiences them by their sound, smell, motion, and emotional impact.
- **Sensory Immersion:**
  Every scene should engage physical senses:
  - **Smells:** Woodland scents, musk, cool breeze, damp earth, food scents, human scents.
  - **Sounds:** Deafening engine roars, bird calls, footsteps, leaves rustling, human shouting vs. gentle voices.
  - **Feelings & Physicality:** Throbbing wounds, hunger, cold air on fur, tense muscles, whiskers twitching, tail postures, exhaustion vs. adrenaline.
- **Emotional Balance:**
  Balance poignant, raw moments of fear and hardship with warmth, wonder, humor, and a spirited determination to live.

---

## 3. Montsoriu's Lexicon & Worldview Glossary

A living reference to ensure consistency in how Montsoriu perceives and describes her world across chapters:

| Concept / Object | Montsoriu's Term / Perception | Context & Notes |
| :--- | :--- | :--- |
| **Humans** | *Tall, two-legged creatures*, *the ones with food*, *creatures* | Distinguished by size, voice tone, scent, and hand gestures. |
| **Car (Stationary)**<br>*(Inside or Outside)* | *Enormous cage*, *silent cage*, *resting cage* | A stationary metal enclosure with ledges, glass, and openings; inert when quiet. Underside is perceived as its *low belly*. |
| **Car (Moving, Inside POV)** | *Roaring cage* | A terrifying, vibrating enclosure where the outside world moves dizzyingly fast. |
| **Car (Moving, Outside POV)** | *Fast, heavy monster*, *beast*, *prowling monster* | Dangerous, rolling behemoths that patrol the endless gray path. |
| **Engine noise** | *Deafening roar*, *growl*, *loud rumble* | Signals that a cage is waking up or a monster is prowling. |
| **Road / Asphalt** | *Endless gray path*, *coarse, hard ground* | Territory where heavy monsters prowl; rough under paw pads. |
| **Forest / Woods** | *Tall trees*, *woodland scents*, *leafy shelter* | A realm of nervous thrills, hiding places, and rich smells. |
| **Den / Architecture** | *Cavern*, *chamber*, *wooden barriers* (doors) | Human indoor structures divided by movable wooden slabs. |
| **Dishes / Bowls** | *Curved hollow*, *smooth container* | Containers used by two-legged creatures to hold water or food. |
| **Dry Cat Food** | *Crunchy dry pieces*, *morsels*, *crunchy bites* | The most delicious, addictive food; comes from crinkling bundles. |
| **Birds / Prey** | *Cheerful callers*, *winged creatures*, *scuttling scents* | Sources of distraction, curiosity, or instinctive hunting interest. |
| **Hands** | *Rough hands*, *gentle fingers*, *reach* | Can represent sudden force or comforting warmth. |
| **Hunger** | *Sharp sting*, *deep hollow*, *gnawing ache* | Transitions from desperate pain to dull numbness when prolonged. |

> [!IMPORTANT]
> **Cognitive Evolution of Vehicles:** In early chapters, Montsoriu **does not realize** that the stationary "enormous cage" she enters is the very same entity as the "heavy monster" rolling along the road outside. To her, they are completely separate phenomena. Maintain this cognitive disconnect in early chapters. In later chapters, as she observes cars more closely, she will gradually connect the dots and realize the cage and the monster are one and the same.

### Feline Idioms & Everyday Expressions

Creative adaptations of human figures of speech that reflect Montsoriu's worldview:

| Human Figure of Speech | Montsoriu's Feline Expression | Example / Context |
| :--- | :--- | :--- |
| *"Oh my..."* / *"Good grief"* | *"My paws..."* | *"My paws, this is taking forever."* |
| *"On one hand... on the other hand..."* | *"On one paw... but on the other paw..."* | Weighing conflicting emotions (e.g., safety vs. lingering trauma). |
| *Unit of distance / length* | *"...about [N] fallen trees wide / long"* | Measuring territory and clearings through natural woodland scales. |
| *"In a heartbeat / split second"* | *"In the blink of an eye"* / *"a tail twitch"* | Fast, instinctive reactions. |

> [!NOTE]
> Expand these tables as new objects, people, animals, and recurring expressions appear across upcoming chapters.

---

## 4. Chapter Conventions & Structure

### File Naming
- Chapters follow kebab-case naming: `chapter-<number>-<slug>.md`
  - Example: `chapter-1-determined-to-live.md`

### Frontmatter Standard
```markdown
---
layout: chapter.njk
title: "Determined to Live"
number: 1
date: 2018-09-14
location: "Near the castle Montsoriu"
cover: /images/capitol01/castell-sense-torra.jpg
prev: /
next: /chapter-2-slug/
---
```

- **Title:** Evocative chapter title reflecting the emotional heart of the chapter.
- **Date:** The historical date of events narrated in that chapter.
- **Location:** The setting from Montsoriu's or the narrator's reference frame.
- **Cover:** Relevant chapter image located in `/images/capitolXX/`.

---

## 5. Narrative Editing Rules for Agents

1. **Preserve Authentic Voice:** Always respect the author's original rhythm, emotional nuances, and sentence structure.
2. **Never Truncate Narrative Content:** When editing or polishing text, never discard narrative passages unless explicitly requested.
3. **Check Lexicon Consistency:** Ensure terms like "roaring cage" or "two-legged creatures" remain coherent with Montsoriu's established vocabulary.
4. **Maintain Punctuation & Formatting:** Preserve markdown emphasis, em-dashes (`—`), and paragraph flow that support natural reading cadence.
5. **Sound Effects & Animal Vocalizations:** Always use markdown italics (`*Meow.*`, `*Clack.*`, `*Thud!*`, `*Sniff*, *sniff*`) for animal vocalizations, bodily sensations, and environmental noises. Do not use quotation marks for non-verbal sounds or object noises.
6. **Avoid Human Mechanical & Engineering Concepts:** Never attribute human mechanical knowledge (e.g., wheels, axles, hinges, steering, pedals, bowls, clocks) to Montsoriu. Describe objects through bodily analogies (*low belly*, *curved hollow*), shapes, textures, materials (*wooden slab*, *thick cloth*), and direct sensory impressions.
7. **Feline Idioms & Expressions (Seasoned with Care):** Seek out natural opportunities to translate common human figures of speech into delightful feline expressions (e.g., *"My paws..."* for *"Oh my..."*, *"On one paw... but on the other paw..."* for *"On the one hand..."*). These creative touches bring humor, charm, and a subtle smile to the reader. **Do not overuse them:** they must feel like occasional, joyful discoveries, never an abundant gimmick that loses its charm or undercuts the emotional weight of a scene.
