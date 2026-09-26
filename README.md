# Masrad | مسرد

AI-Powered Accessible Reading of Arabic Visual Novels for Visually Impaired Readers

Graduation project (CSC 496/497), Computer Science Department, College of Computer and Information Sciences, King Saud University, 2026/2027.

About

Visual novels communicate stories through dialogue, artwork and panel layout, which creates accessibility barriers for visually impaired readers. Masrad is an AI-powered web application that transforms Arabic visual novel chapters into screen-reader-compatible text, combining dialogue, speaker information and concise descriptions of essential visual events in reading order.

How it works

Masrad accepts a visual novel chapter and processes its pages in sequence through five stages:

Visual novel structure analysis: MagiV3 detects panels, text regions and characters, establishes reading order and associates dialogue with speakers.
Arabic visual-novel text recognition: an Arabic OCR model (candidate: QARI-OCR) fine-tuned on synthetic lettering and annotated visual novel text.
Essential visual-detail selection: a vision-language model proposes descriptions of actions, expressions and other visual details, and a trained ranking model prioritizes them within a defined description length.
Arabic text generation: combines dialogue and selected visual details into coherent Arabic text, using only the current and preceding panels to reduce premature disclosure of later events.
Accessible delivery: a screen-reader-compatible web interface, so readers can use their existing screen readers.

Only the OCR component and the detail selector are trained specifically for this project.

Proposed tech stack
Layer	Tools
Frontend	React, TypeScript
Backend	FastAPI, PostgreSQL
Models	Python, PyTorch, Transformers, PEFT, MagiV3, QARI-OCR (candidate), a vision-language model
Annotation	Label Studio

These choices will be finalized during system design.

Roadmap

Semester 1 (CSC 496): Analysis and design

Literature review and requirements
Dataset and evaluation design
System and interface design
Semester 1 report and poster

Semester 2 (CSC 497): Implementation and evaluation

Data preparation and baseline testing
OCR and detail-selector training
Text generation and system integration
Evaluation and refinement
Final release and documentation

Data

Visual novel pages, datasets and model weights are not stored in this repository. Instructions for getting the data will be added here.

Team

See AUTHORS.md.
