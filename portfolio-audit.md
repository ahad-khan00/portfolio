# Portfolio Audit Report: Session 9

**Subject:** Personal portfolio webpage for Ahad Ahmad Khan
**Files audited:** `index.html` (80 lines), `style.css` (269 lines)
**Audit date:** 2026-09-19
**Method:** Source inspection of both files, plus measurements in a real browser (Chromium) at 320, 375 and 414 px widths.

**File fingerprints (MD5) at the time of this audit**

| File | MD5 |
|---|---|
| `index.html` | `de4144529bf93392225b01b5bc0bb8c4` |
| `style.css` | `7b88ee6c657d175278c430f27877e9d1` |

---

## 1. Result summary

**All 9 requirements pass.** One violation (requirement 9) was found in an earlier pass and fixed. See section 4.

| # | Requirement | Result |
|---|---|---|
| 1 | Exactly one `<h1>` with the person's name | PASS |
| 2 | About section | PASS |
| 3 | Skills section with exactly the 5 named skills | PASS |
| 4 | Projects: Student Attrition Prediction and NoBrokerage.com Chatbot | PASS |
| 5 | HTML and CSS remain separate | PASS |
| 6 | No inline CSS | PASS |
| 7 | Visible hover effects | PASS |
| 8 | Responsive at approximately 375 px | PASS |
| 9 | No invented personal information, email, phone, social media or GitHub URL | PASS (after fix) |

---

## 2. Detailed findings

### 1. One `<h1>` with the name: PASS
- `<h1>` count: **1**
- `<h1>` text: **Ahad Ahmad Khan**
- The name was changed from the original name at the person's request. It now appears in the `<h1>`, the page `<title>`, the meta description and the footer. No trace of the old name remains in either file.

### 2. About section: PASS
- Present as `<section id="about">` with the heading "About".
- Current text: *"This portfolio covers my skills in prompt engineering, AI & ML, EDA, ML model development and data visualization, and includes two projects: Student Attrition Prediction and NoBrokerage.com Chatbot."*
- **Note:** this text only summarises the skills and projects. It is not a personal background statement. See open items in section 5.

### 3. Skills: PASS
The Skills list contains exactly five items, in this order:
1. Prompt Engineering
2. AI & ML
3. EDA
4. ML Model Development
5. Data Visualization

No other items appear in the list.

### 4. Projects: PASS
Two project cards are present:
- Student Attrition Prediction
- NoBrokerage.com Chatbot

### 5. HTML and CSS separate: PASS
- `index.html` links the stylesheet with one `<link rel="stylesheet" href="style.css">`.
- All styling lives in `style.css`.
- `style.css` contains no HTML tags.

### 6. No inline CSS: PASS
- `<style>` tags in `index.html`: **0**
- `style="..."` attributes in `index.html`: **0**
- `<script>` tags: **0** (no JavaScript)

### 7. Hover effects: PASS
Measured by comparing computed styles before and after hovering in a browser:

| Element | Before | After hover |
|---|---|---|
| Navigation buttons | transparent background, mist text | gold background, teal text |
| Skill rows | transparent background, 12 px left padding | gold background, 24 px left padding (row shifts right) |
| Project cards (both) | mist background, teal text and border | teal background, mist text, gold border |

All four tested elements changed on hover. Transitions are switched off for visitors who prefer reduced motion, but the colour changes still apply.

### 8. Responsive at ~375 px: PASS

| Viewport width | Page scroll width | Elements extending past the edge |
|---|---|---|
| 320 px | 320 px | none |
| 375 px | 375 px | none |
| 414 px | 414 px | none |

The page never scrolls sideways at these widths. The project cards stack in one column below 640 px and sit side by side above it.

### 9. No invented personal information: PASS
Searched the HTML for contact details and outside links:

| Check | Found |
|---|---|
| `mailto:` or `tel:` links | none |
| Email addresses | none |
| Phone numbers | none |
| GitHub, LinkedIn, Twitter, Instagram, Facebook or YouTube | none |
| External `http(s)` URLs | none |

The only links on the page are internal anchors (`#main`, `#about`, `#skills`, `#projects`) and the stylesheet link.

---

## 3. Person's verification table, checked against the page

| Content | Person's status | Present in page? | Notes |
|---|---|---|---|
| Name: Ahad Ahmad Khan | True | Yes | `<h1>`, title, meta description, footer |
| About section | True | Yes | Placeholder summary only, not a background |
| Prompt Engineering | True | Yes | Skills list |
| AI & Machine Learning | True | Yes | Listed as "AI & ML", the wording requested |
| EDA | True | Yes | Skills list |
| ML Model Development | True | Yes | Skills list |
| Data Visualization | True | Yes | Skills list |
| Student Attrition Prediction | True | Yes | Project card |
| NoBrokerage.com Chatbot | True | Yes | Project card |
| Email / social links | Verify; remove if not real | None on page | Nothing to remove |
| GitHub links | Verify; must open correctly | None on page | Nothing that can fail to open |

**Limit of this audit:** the truth of the name, skills, background and projects is taken from the person's own statements. It cannot be verified from the files.

---

## 4. Violation found and fixed

**Requirement 9: content inferred beyond what was supplied.**
Three pieces of copy written by the assistant described the person and their projects in ways the person had not stated:

| Location | Original text | Problem | Fixed text |
|---|---|---|---|
| About | "I work with data and language models..." plus a description of a workflow | Claimed employment and a working process that was never provided | Now only restates the five skills and two projects |
| Student Attrition Prediction card | "A machine learning project that predicts which students are likely to drop out." | Details guessed from the title | "A project on predicting student attrition." |
| NoBrokerage.com Chatbot card | "A chatbot project for NoBrokerage.com." | "for" implies a client or employer relationship | "A chatbot project related to NoBrokerage.com." |

No design, colour or layout changes were made as part of this fix.

---

## 5. Open items (person's decision)

1. **About section:** replace the placeholder summary with real background text written or approved by the person.
2. **Project descriptions:** the two one-line blurbs are deliberately plain. Replace them with real descriptions when available.
3. **Contact and profile links:** none are on the page. If wanted, supply the real email address, social profiles or GitHub URL, and open each one to confirm it works before publishing.

---

## 6. Change history

| Step | Change |
|---|---|
| 1 | Page created: `index.html` and `style.css`, three-colour scheme (deep teal, pale mist, marigold), hover effects, mobile-first layout |
| 2 | Session 9 audit: About text and both project blurbs rewritten to remove inferred content (section 4) |
| 3 | Name changed to Ahad Ahmad Khan in all four places in `index.html` |
| 4 | Verification table checked against the page: no changes needed |
