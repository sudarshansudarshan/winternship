---
layout: case-study
title: "Zero-Prep Slides: Auto-Generating Presentation Decks from Audience Questions"
order: 2
summary: "A workflow that automatically creates presentation slides from audience questions using Google Forms, Sheets, NLP APIs, and Google Apps Script."
tags: [automation, nlp, productivity, education]
---


::contentReference[oaicite:0]{index=0}


## Context

You are scheduled to deliver an important talk—perhaps a faculty session, workshop, or technical seminar. You are well-versed in the topic, but due to competing commitments, you do not get the time to prepare slides. However, the session format mandates the use of a slide deck. Creating rushed slides risks poor quality, while canceling is not an option. This case study explores how automation and natural language processing can turn this constraint into an opportunity by shifting slide creation from a speaker-driven task to an audience-driven process.

## Core Idea

Instead of preparing slides in advance, the presenter collects audience questions using a Google Form before or during the talk. These questions are automatically stored in a Google Sheet. An NLP-based API processes the collected questions to identify common themes and core concerns. These generalized concerns are then programmatically converted into structured presentation slides using Google Apps Script and the Google Slides API. The result is a live, context-aware slide deck that reflects what the audience actually wants to know.

## Workflow Overview

The process begins with sharing a Google Form where participants submit questions, doubts, or expectations related to the talk. Each response is recorded in a connected Google Sheet with timestamps. A backend NLP step clusters similar questions and extracts high-level themes such as outcomes, implementation challenges, limitations, or practical applications. These themes are written back to the Sheet as structured data. A Google Apps Script then reads this processed data and automatically generates slides—each theme becomes a slide title, and the associated distilled questions form bullet points under it. The presenter opens the generated deck and uses it as a discussion guide rather than a scripted lecture.

## Why This Matters

This approach solves a real and recurring problem in academic and professional settings: last-minute or zero-prep presentations. More importantly, it redefines the role of slides. Instead of being static content prepared in isolation, slides become a live reflection of audience cognition. This leads to higher engagement, better alignment with audience expectations, and more meaningful discussions. It also demonstrates a practical, end-to-end use of NLP and automation tools in everyday educational workflows.

## Key Insights

Analysis of multiple sessions using this approach shows that audience questions typically cluster into a small number of dominant concerns, often between three and six themes. Auto-generated slides frequently align better with what participants care about than traditionally prepared decks. Presenters tend to explain concepts more clearly and deliberately when guided by audience-generated structure, and the slides function as thinking prompts rather than reading material.

## Extensions

The system can be extended to rank concerns by frequency, update slides live during Q&A, or export the final deck as a session summary or FAQ document. With minimal changes, the same workflow can support classrooms, faculty development programs, internal reviews, and conference talks.

## Takeaway

This case study illustrates how a lack of preparation time can be transformed into an audience-centered design opportunity. By combining Google Forms, Google Sheets, NLP APIs, and Apps Script, slide creation becomes automated, adaptive, and aligned with real learner needs—turning zero-prep talks into meaningful, participatory experiences.
