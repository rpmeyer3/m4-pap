# Milestone 4 Report

**Dr. Jayalath | CSCI 4800 | Spring 2026 | University of Georgia**
**Prepared By: Group 11: Beer Buddies**
Ryan Meyer, Kristian Pitshugin, Matt Harpur, Daniel Fairchild
April 13th, 2026

---

## 1. Introduction

### Mission Statement

FreshKeep exists to eliminate invisible food waste — the groceries that are purchased with good intentions but silently expire in the backs of refrigerators and pantries. Our mission is to bridge the gap between purchasing and consuming by transforming passive food storage into active, intelligent inventory awareness with near-zero effort from the user.

### Problem/Solution Overview

Our needfinding across seven interviews and a 35-person survey revealed that 83% of respondents actively think about food waste, 80% are bothered by it, and yet 71% still throw away expired food sometimes or often. The core issue is not careless purchasing — it is that once groceries are stored, they enter a "forgotten state" where items become invisible until it is too late. Users described this as "an inevitable consequence of a busy lifestyle," and 97% said they would adopt a solution only if it required minimal effort.

FreshKeep addresses this by using computer vision and ML to tokenize items from scanned receipts, automatically building a digital pantry inventory. Each item is matched against a food database to generate personalized expiration estimates. The app then surfaces timely reminders, suggests recipes using soon-to-expire ingredients, and tracks waste metrics over time — all without requiring users to manually catalog a single item.

### Solution Choice and Reasoning

From our three finalist solutions in Milestone 3, we selected the **ML Receipt to Inventory Manager** (FreshKeep) over the Rotating Fridge Tray and the Second Look Visual Analysis Tool. The Rotating Fridge Tray, while creative, addresses only refrigerator visibility and requires physical hardware adoption — a significant barrier. The Second Look tool relies on users actively photographing each item, which directly conflicts with our finding that 97% of users demand a low-effort solution. FreshKeep, by contrast, requires only a single action (scanning one receipt) to log an entire shopping trip, making it the solution most aligned with user needs.

### Task Descriptions

**Task 1 — Simple: Check an item's expiration status.**
The user opens the app, navigates to Inventory, and taps on an item (e.g., Greek Yogurt) to view its expiration date, storage location, and AI freshness assessment. Expected completion: under 30 seconds, 3 taps or fewer.

**Task 2 — Moderate: Scan a receipt and review imported items.**
The user taps "Scan Receipt" from the Home screen, positions a grocery receipt within the camera frame, and reviews the list of automatically detected items. The user confirms correct items and corrects or removes any misidentified entries. Expected completion: 1–2 minutes.

**Task 3 — Complex: Connect a grocery store account and configure notifications.**
The user navigates to Settings, selects a grocery store (e.g., Kroger), authorizes account linkage for automatic receipt import, reviews the first batch of synced items, and then configures notification preferences for expiration reminders. Expected completion: 3–5 minutes.

---

## 2. Sketches

We brainstormed five distinct design alternatives, each using a fundamentally different interaction paradigm, and produced 3–5 rough sketches per alternative (20 total).

### Alternative A: Tab-Based Dashboard
A conventional mobile app layout with a persistent bottom navigation bar (Home, Inventory, Stats, Settings). Users interact by tapping tabs and scrolling content feeds. Receipt scanning is accessed via a prominent camera button on the Home screen. This is the most familiar pattern for mobile users and minimizes the learning curve.

### Alternative B: Conversational Chat Interface
An AI chatbot-driven interface where users interact entirely through natural language input — typing or speaking commands like "What's expiring this week?" or "Add my Kroger receipt." The interface is minimal, consisting primarily of a chat thread and a text input field. While innovative, this design risks slower task completion for simple lookups.

### Alternative C: Widget-First Home Screen
The app's primary value is delivered through phone home screen widgets rather than an in-app experience. Widgets display expiring items, daily meal suggestions, and waste summaries. Users only open the full app for setup and receipt scanning. This maximizes passive awareness but limits discoverability of deeper features.

### Alternative D: Card-Swipe Interface
A swipe-based interaction model inspired by dating apps. Each day, the app presents a "deck" of food items needing attention. Users swipe right to confirm they still have the item, swipe left to mark it as used or discarded. While engaging, this interaction model is less efficient for users managing large inventories.

### Alternative E: Calendar/Timeline View
A calendar-centered layout that maps food items to their estimated expiration dates. Users scroll through a weekly or monthly view to see which items expire on which days, enabling meal planning around upcoming expirations. This approach emphasizes planning but may feel cluttered for users with many items.

---

## 3. Selected Interface Design

### Top Two Alternatives

**Alternative A (Tab-Based Dashboard)** and **Alternative D (Card-Swipe Interface)** were selected as the top two based on team evaluation and alignment with user preferences for simplicity.

Alternative A provides the most intuitive, universally recognizable navigation pattern. Users understand tab bars instinctively, and the design supports both quick glances (checking one item) and deep exploration (browsing full inventory, viewing stats). Wireflows showed smooth task completion for all three defined tasks.

Alternative D offers a novel, engaging interaction that could improve daily check-in habits. However, wireflow analysis revealed friction for the complex task (store account connection), as the swipe metaphor does not naturally extend to settings and configuration flows.

### Best Alternative: Tab-Based Dashboard (Alternative A)

We selected Alternative A as our final design. It scored highest on:
- **Learnability:** Familiar navigation pattern across iOS and Android.
- **Efficiency:** Direct access to all key features within 1–2 taps from any screen.
- **Scalability:** Cleanly supports additional features (recipes, household sharing, AI food check) without UI overhaul.
- **User alignment:** 97% of our participants demanded minimal effort — a tab-based layout reduces cognitive overhead to near zero.

### Wireflows for Each Task

**Task 1 wireflow (Simple):** Home → tap "Inventory" tab → scroll/search for item → tap item card → view Expiration Date, Storage Location, and AI Assessment.

**Task 2 wireflow (Moderate):** Home → tap "Scan Receipt" button → camera activates → position receipt in frame → auto-detect items → review detected items list → confirm/edit items → items added to Inventory.

**Task 3 wireflow (Complex):** Home → tap "Settings" tab → tap "Connected Stores" → tap "Connect" on desired store → authorize account → auto-import receipt history → review imported items → navigate to Notification Settings → configure reminder timing → save preferences.

---

## 4. Prototype

Our low-fidelity prototype was built as an interactive HTML/CSS wireframe simulating the FreshKeep mobile app. The prototype includes all screens necessary to complete the three defined tasks and uses a grayscale wireframe aesthetic consistent with low-fi prototyping conventions.

The prototype consists of the following screens:
1. **Home Screen** — Displays quick-action buttons (Scan Receipt, Quick Sync) and a summary of expiring items.
2. **Scan Receipt Screen** — Simulates camera-based receipt scanning with a detected items review list.
3. **Inventory Screen** — Filterable list of all tracked food items by storage location (All, Fridge, Freezer, Pantry).
4. **Item Detail Screen** — Individual item view showing expiration date, storage info, and AI freshness assessment.
5. **Stats/Impact Screen** — Monthly waste and savings tracker with category breakdown.
6. **Settings Screen** — Store account connections and notification configuration.

The prototype supports click-through navigation between all screens via the bottom tab bar and interactive elements within each screen.

---

## 5. Testing Methodology

### Participants
We recruited three participants who are not friends, family, or classmates:

| # | Name | Age | Occupation | Relevance |
|---|------|-----|------------|-----------|
| 1 | [PARTICIPANT 1 NAME] | [AGE] | [OCCUPATION] | [Why relevant to problem area] |
| 2 | [PARTICIPANT 2 NAME] | [AGE] | [OCCUPATION] | [Why relevant to problem area] |
| 3 | [PARTICIPANT 3 NAME] | [AGE] | [OCCUPATION] | [Why relevant to problem area] |

### Roles
- **Facilitator:** Guides the participant through tasks, reads scripts, and asks follow-up questions.
- **Note-taker/Observer:** Documents participant actions, hesitations, errors, verbal comments, and timestamps.
- **Computer (Wizard of Oz):** Operates the prototype, advancing screens in response to participant interactions to simulate app behavior.

### Demo Script
"Thank you for participating in our usability study. We are testing a prototype of a mobile app called FreshKeep that helps people track their grocery inventory and reduce food waste. We are testing the design, not you — there are no wrong answers. Please think aloud as you work through each task, telling us what you are looking at, what you expect to happen, and any confusion you experience. You may stop at any time."

### Task Directions Given to Participants

**Task 1:** "Imagine you just got home and want to check whether your Greek Yogurt is still good. Using the app, find the yogurt and determine its expiration status."

**Task 2:** "You just returned from Kroger with a paper receipt. Use the app to scan your receipt and review the items the app detected. Confirm the items are correct."

**Task 3:** "You want to set up your Kroger account so the app automatically imports your receipts in the future. Connect your store account and then configure your notification preferences for expiration reminders."

### Usability Goals and Measurements

**Goal 1: Efficiency** — Users should complete the simple task (check item expiration) quickly and with minimal navigation effort.
- *Measurement 1:* Time on task (target: ≤ 30 seconds)
- *Measurement 2:* Number of taps/screen transitions (target: ≤ 3)

**Goal 2: Learnability** — First-time users should complete the moderate task (scan receipt and review items) without external help.
- *Measurement 1:* Task completion rate (target: 100% success)
- *Measurement 2:* Number of errors or wrong-path navigations before completion (target: ≤ 1)

---

## 6. Results

> **[FILL IN AFTER CONDUCTING USABILITY TESTS]**

### Quantitative Results

| Participant | Task 1 Time | Task 1 Taps | Task 2 Success | Task 2 Errors | Task 3 Success | Task 3 Time |
|-------------|------------|-------------|----------------|---------------|----------------|-------------|
| P1 | [__s] | [__] | [Y/N] | [__] | [Y/N] | [__s] |
| P2 | [__s] | [__] | [Y/N] | [__] | [Y/N] | [__s] |
| P3 | [__s] | [__] | [Y/N] | [__] | [Y/N] | [__s] |

### Critical Incidents

| # | Participant | Task | Description | Severity (0–4) |
|---|-------------|------|-------------|-----------------|
| 1 | [P#] | [#] | [Describe what happened — e.g., "User tapped Reminders instead of Inventory to find item"] | [0–4] |
| 2 | [P#] | [#] | [Describe incident] | [0–4] |
| 3 | [P#] | [#] | [Describe incident] | [0–4] |

**Severity Scale:**
- 0 = Not a usability problem
- 1 = Cosmetic problem only
- 2 = Minor usability problem
- 3 = Major usability problem (causes significant delay or failure)
- 4 = Usability catastrophe (prevents task completion)

### Goal 1 (Efficiency) Assessment
[Summarize whether the 30-second / 3-tap targets were met or missed. Note any patterns across participants.]

### Goal 2 (Learnability) Assessment
[Summarize task completion rates and error counts for Task 2. Note whether participants needed hints.]

---

## 7. Discussion

> **[FILL IN AFTER CONDUCTING USABILITY TESTS — guidance below]**

### What Worked Well
[Describe aspects of the design that participants navigated smoothly. For example: "All three participants immediately identified the Inventory tab as the correct starting point for Task 1, completing it well under the 30-second target."]

### What Needs Improvement
[Describe pain points uncovered. For example: "Two participants expected the Scan Receipt button to be on the Inventory screen rather than the Home screen, causing initial confusion in Task 2." Or: "The Settings → Connected Stores path was not intuitive; P2 looked under the Home screen first."]

### Design Recommendations
[List 2–4 concrete changes for the next iteration. For example:
1. Add a "Scan" shortcut button to the Inventory screen in addition to Home.
2. Rename "Connected Stores" to "Link My Grocery Accounts" for clearer labeling.
3. Add an onboarding tooltip the first time a user opens the app pointing to the Scan Receipt feature.
4. Increase the visual prominence of the notification settings within the Settings screen.]

### Limitations
[Note limitations: small sample size (3 participants), Wizard of Oz prototype rather than functional software, participants may not represent full target demographic. Note any tasks that could not be fully tested due to prototype fidelity.]

---

## 8. Appendices

### Appendix A: All 20 Design Sketches
[Insert photos/scans of the 3–5 rough sketches per each of the 5 design alternatives]

### Appendix B: Wireflows for Top 2 Alternatives
[Insert detailed wireflow diagrams for Alternative A (Tab-Based Dashboard) and Alternative D (Card-Swipe Interface)]

### Appendix C: Detailed Wireflows for Final Design (Alternative A)
[Insert the detailed wireflow for each of the 3 tasks — can reference the HTML prototype screenshots]

### Appendix D: Participant Consent Documentation
[Include signed consent forms or verbal consent confirmations]

### Appendix E: Raw Testing Notes
[Include the note-taker's raw observation notes from each participant session]

### Appendix F: Contribution Table

| Team Member | Contributions |
|------------|--------------|
| Ryan Meyer | [List specific contributions] |
| Kristian Pitshugin | [List specific contributions] |
| Matt Harpur | [List specific contributions] |
| Daniel Fairchild | [List specific contributions] |

---

*Word count (excluding tables, headings, appendices): ~1,950 words*
