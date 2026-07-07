**UX DETECTIVE: SQUAD MODE**

*A 30-Minute Group Game — Screen-by-Screen Design Document*

Grade 8–9  •  Groups of 3  •  Sequel to the solo UX Crimes investigation game

# **1\. Game Overview**

**Concept.**  Having each investigated UX crimes solo, students now form a design studio of 3\. In one 30-minute session they pick a real school problem, build a working UI mock in a drag-and-drop \+ prompt builder, and prove their design avoids all 8 UX Crimes.

**Shift in thinking.**  The solo game trained students to SPOT crimes. This game trains them to PREVENT crimes while creating — the harder, real designer skill.

**Build tool.**  A no-backend, template-based builder embedded in the same HTML window. Students pick components from a tray, drag them onto a phone frame, and type short prompts (e.g. 'add a green success message') that the builder maps to pre-made component templates. No internet, no login, no API — fully offline on your server.

**Win condition.**  Not the prettiest UI. The group wins by shipping a UI that (a) solves the chosen problem and (b) survives the Critic's 8-crime audit with the fewest violations.

# **2\. The Three Roles**

Each student picks ONE role and keeps it for the whole game. Roles are designed so nobody is idle and the crime-checking discussion is forced.

| Role | One-line job | What they do |
| :---- | :---- | :---- |
| **Product Lead** | Runs the clock & drives decisions | Keeps the group on time using the on-screen timer. Reads the 3 problem statements aloud, forces the group to pick ONE within the time limit, and makes the final call if the group is split. During building, keeps asking: 'Does this actually solve the user's problem?' |
| **Designer** | Types prompts & builds the UI | The only one who touches the keyboard/mouse in the builder. Turns the group's decisions into prompts and drag-drop components. Must build what the group agrees on, not personal preference. Explains each design choice out loud before placing it. |
| **Critic / User Tester** | Hunts for UX crimes | Holds the 8 UX Crimes card. After every screen the Designer builds, the Critic checks it against all 8 crimes and calls out any committed. Also role-plays a confused first-time user trying to complete the task, narrating confusion aloud. |

**Rotation rule (optional).**  If you run the game twice, students must swap roles so everyone experiences building and critiquing.

# **3\. The 8 UX Crimes (Reference Card)**

This card is on screen throughout and physically held by the Critic. Every built screen is audited against all 8\.

| Crime | What it means | School example |
| :---- | :---- | :---- |
| **Lost\!** | No indication of where you are or what just happened after an action | *Clicking Submit shows a blank white screen with no confirmation* |
| **Alien Speak** | Buttons or labels use jargon that doesn't match what they do | *A button labelled Initiate Session that starts a video call* |
| **No Escape** | Can't go back, undo, or cancel without losing your work | *Filling a 10-field form and hitting back deletes all entries* |
| **Identical Twins** | Things that look the same do different things, or vice versa | *Two green buttons side by side — one saves, one submits permanently* |
| **Error, So What?** | An error appears but doesn't tell you what to do next | *Error 403 with no explanation or recovery path* |
| **Marathon Click** | A simple task takes far more steps than it should | *Downloading your timetable takes 7 taps across 4 screens* |
| **Visual Chaos** | So much on screen that you don't know where to look first | *A dashboard with 14 badges, 3 banners and 6 menus at once* |
| **Silent Action** | No confirmation that anything happened after an action | *Tapping Save with no visual change, sound or message* |

# **4\. 30-Minute Timeline**

| Time | Phase | Screen(s) |
| :---- | :---- | :---- |
| **0–3 min** | Assemble the squad | Screen 1–2: roles chosen, rules shown |
| **3–8 min** | Pick the case | Screen 3: read 3 problems, debate, lock one |
| **8–12 min** | Crime briefing | Screen 4: group predicts which crimes threaten their problem |
| **12–24 min** | Build in the studio | Screen 5: drag-drop \+ prompt builder |
| **24–28 min** | Crime audit | Screen 6: Critic runs the 8-crime checklist live |
| **28–30 min** | Verdict & skills | Screen 7–8: score, skill ratings, debrief |

# **5\. Screen-by-Screen Design**

*Each screen below lists: purpose, what's on screen, the group interaction / role-play, and the build note for Claude Code.*

## **SCREEN 1  Welcome — Enter the Studio**

**Purpose.**  Set the frame: you are now a design studio, not solo detectives.

**On screen:**

* Title 'UX Detective: Squad Mode' with a short line: 'You've caught the criminals. Now build something that commits zero crimes.'

* A single \[Enter the Studio →\] button. (Deliberately ONE clear action — models good UX from the first second.)

**Build note.**  Static hero screen. Store nothing yet.

## **SCREEN 2  Assign Roles**

**Purpose.**  Lock the three roles before any work starts.

**On screen:**

* Three role cards (Product Lead, Designer, Critic/User Tester) with the one-line job \+ icon.

* Each card has a text field: 'Who is this? → \[name\]'. All three must be filled to continue.

* Note under Designer card: 'Only this person drives the keyboard for the rest of the game.'

**Role-play prompt (shown on screen):**

* *"Read your role card aloud to your group in your own words. Product Lead goes first."*

**Build note.**  Save the 3 names in memory/state; reuse them in later screens and the final scorecard.

## **SCREEN 3  Pick Your Case**

**Purpose.**  Group debates and commits to ONE of three problem statements.

**On screen — three case cards:**

* **The Vanishing Homework.**  Students submit homework on an app but never know if it actually went through — half re-submit 'just in case'.  *Your mission: Design a homework submission screen where the student always knows their status.*  (Likely crimes: Lost\!, Silent Action, Error So What?)

* **The Canteen Queue.**  The school canteen pre-order app takes 8 taps to order one snack, so nobody uses it and queues stay long.  *Your mission: Design a 'quick order' flow that gets a student from open-app to order-placed in as few steps as possible.*  (Likely crimes: Marathon Click, Alien Speak, Visual Chaos)

* **The Field-Trip Form.**  Parents fill a long permission form; one wrong tap on 'Back' wipes everything and there's no confirmation at the end.  *Your mission: Design a multi-step form that protects the user's work and confirms success clearly.*  (Likely crimes: No Escape, Identical Twins, Lost\!)

**Role-play (structured 4-min debate):**

* **Product Lead**: 'Which problem is most real for OUR school?' — reads all three aloud.

* **Critic**: argues which problem has the WORST current UX (most crime potential).

* **Designer**: argues which is most buildable in 12 minutes.

* *Product Lead makes the final call and taps \[Take this case\].*

**Build note.**  Selecting a card locks it (others grey out) and carries that problem \+ its 'likely crimes' into Screens 4–6. Include a \[Change case\] escape — modelling 'No Escape' prevention.

## **SCREEN 4  Crime Briefing — Predict the Threats**

**Purpose.**  Before building, the group discusses all 8 crimes against their chosen problem. This is the core discussion screen you asked for.

**On screen:**

* The 8-crime card displayed as 8 tiles.

* For each crime, a toggle: 'Could this crime appear in OUR UI? — High / Medium / Low risk'.

* A free-text 'how we'll prevent it' box under any crime marked High.

**Role-play (round-robin through all 8):**

* *Critic reads a crime aloud → group discusses 'where could this bite us?' → Product Lead sets the risk level → Designer notes one prevention idea. Repeat for all 8\.*

**Why all 8, every time.**  Even 'Low risk' crimes must be spoken about — this guarantees the full framework is rehearsed, not just the obvious ones.

**Build note.**  Carry the High-risk crimes forward so the Screen 6 audit can highlight them first. This screen's output \= the group's 'design contract'.

## **SCREEN 5  The Studio — Build Your UI**

**Purpose.**  The group builds a working mock. 12 minutes, one keyboard (Designer).

**Layout — three zones:**

* **Left: Component Tray.**  Drag-and-drop blocks — Button, Text label, Input field, Success message, Error message, Back button, Progress bar, Icon, Card, Menu, Confirmation popup, Image placeholder.

* **Centre: Phone Frame.**  Drop zone showing a phone screen; components stack in order and can be reordered / deleted.

* **Right: Prompt Box \+ Crime Card.**  A text box: 'Describe what you want and we'll add it.' Typed prompts map to templates — e.g. 'add a green tick saying Submitted' inserts a Success-message component. The 8-crime card stays pinned here.

**How the no-backend prompt builder works (for Claude Code):**

* Maintain a keyword→template map (e.g. 'success/done/tick' → success component; 'error/wrong' → error component; 'back/cancel' → back button; 'step/progress' → progress bar).

* Parse the typed prompt for keywords, insert the matching pre-styled component into the frame. No AI/API needed — pure JS string matching \+ a template library.

* If no keyword matches, show a friendly hint listing example prompts (this itself models good 'Error, So What?' handling).

**Role-play during build:**

* *Designer builds and narrates each choice. Product Lead watches the timer and the problem statement. Critic watches for crimes being committed live and may shout 'Crime\!' — but Designer decides whether to fix now or note for audit.*

**Build note.**  Keep the component set small and pre-styled so any combination looks clean. Store the built layout so Screen 6 can inspect it.

## **SCREEN 6  The Crime Audit**

**Purpose.**  The Critic runs the full 8-crime checklist against the finished UI. This is where learning is proven.

**On screen:**

* The built UI on the left, the 8-crime checklist on the right.

* For each crime: \[Committed\] or \[Avoided\] \+ a one-line 'evidence' field ('We avoided Silent Action because we added a green Submitted message').

* A live counter: 'Crimes avoided: X / 8'.

**Role-play:**

* *Critic leads, reading each crime and inspecting the UI. Designer defends the design. Product Lead settles disputes and taps the verdict. The group must give evidence, not opinion.*

**Build note.**  Cross-reference the High-risk crimes from Screen 4 — flag any the group predicted but still committed. That gap is the richest teaching moment.

## **SCREEN 7  Verdict & Skill Ratings**

**Purpose.**  Give the group a clear result plus a rating across the real skills the game exercises.

**On screen — Studio Report Card:**

* Big result: 'Crimes avoided: X / 8' with a badge tier — 8 \= Master Studio, 6–7 \= Pro Studio, 4–5 \= Junior Studio, below 4 \= Back to the Drawing Board.

**Group skill ratings (1–5 stars each), auto-suggested from gameplay \+ adjustable by facilitator:**

| Skill | How it's judged |
| :---- | :---- |
| **Empathy** | Did the design solve the actual user's problem from the case? |
| **Communication** | Quality of the role-play debate — did all 3 voices contribute? |
| **Problem-Solving** | Crimes avoided score (X / 8). |
| **Collaboration** | Did they stick to roles and reach decisions without one person dominating? |
| **Design Thinking** | Did they predict crimes in Screen 4 and prevent them in Screen 5? |

**Build note.**  Auto-fill Problem-Solving from the audit score; leave the others as tappable star inputs the facilitator/group set together. Show the 3 player names on the card.

## **SCREEN 8  Debrief — What We Learned**

**Purpose.**  Lock in the learning with a short, explicit takeaway.

**On screen:**

* One headline: 'Spotting crimes is easy. Preventing them while you build is the real skill.'

* Three prompts, one per role, answered aloud: Designer — 'One crime I nearly committed…'; Critic — 'The sneakiest crime to catch was…'; Product Lead — 'If we had 5 more minutes we'd fix…'.

* A \[Play again — swap roles\] button and a \[Download our report card\] option.

**Build note.**  Report card can be a printable HTML view or a simple canvas image. No backend required.

