# Quantum Computing, Gently

**A free, open textbook on quantum computing for people who have never studied physics or computer science.**

## Upcoming Research

This paper is part of an ongoing independent research initiative focused on DeepTech, quantum computing, and emerging technologies.

Further research papers exploring new concepts, theoretical approaches, and potential applications are coming soon.

Follow this repository to stay updated on future publications and research developments.

by Kaiser · written in January 2026 · Version 1.0

[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)

📘 **[Download the PDF](Quantum-Computing-Gently.pdf)** (227 pages)

---

## What this book is

Most introductions to quantum computing are written for third- or fourth-year physics or mathematics students. This one starts from zero. If you can work out a 15% tip on a restaurant bill, you have enough mathematics to begin. Everything else, from arrows and probabilities to complex numbers and matrices, is built up step by step, with pictures first and formulas second.

By the end you should be able to explain in your own words:

- what a qubit is, and why superposition is neither "both at once" nor "one or the other, we just don't know"
- what happens when you measure a quantum system
- what entanglement does, what it cannot do, and why Bell's theorem matters
- how Shor's algorithm could break today's internet encryption, and how far we are from that
- why Grover's search is faster, but only by a square root
- why quantum computers are so hard to build, and how error correction rescues them
- how to read a news headline about a "quantum breakthrough" critically

## What's inside

| | |
|---|---|
| **Part I: Foundations** | 1 Why build a quantum computer? · 2 How an ordinary computer thinks · 3 A small mathematical toolkit · 4 Light, waves and a puzzle · 5 The qubit · 6 Looking at a qubit |
| **Part II: Computing with qubits** | 7 A qubit as a point on a globe · 8 Quantum gates · 9 Many qubits · 10 Entanglement · 11 Two-qubit gates and circuits · 12 What the quantum world forbids |
| **Part III: Quantum algorithms** | 13 Interference as a way of computing · 14 Teleportation and superdense coding · 15 The quantum Fourier transform · 16 Shor's algorithm · 17 Grover's algorithm · 18 Simulating nature |
| **Part IV: Information, noise and machines** | 19 Quantum cryptography · 20 Noise · 21 Protecting quantum information · 22 Building a quantum computer · 23 Measuring information · 24 What quantum computers can and cannot do · 25 Where we stand and where we might go |
| **Back matter** | Glossary · Hints and answers · Further reading · References |

Along the way:

- more than 60 figures, including the Bloch sphere, interferometers, amplitude diagrams and quantum circuit diagrams
- worked examples that follow every amplitude through teleportation, Deutsch–Jozsa, Shor (for N = 15) and Grover (for N = 8)
- exercises at the end of every chapter, with hints and answers at the back
- optional "a little more maths" boxes for readers who want to go further
- a references section of about 90 original papers, from Feynman (1982) and Shor (1994) to the latest error-correction experiments

## Who it's for

- curious readers with no technical background
- school and university students who want intuition before the formal course
- programmers who want to understand what the quantum SDKs are actually doing
- journalists, policy makers and investors who need to judge quantum claims
- teachers looking for free material to use in class

After this book, the natural next steps are a course in linear algebra and a standard textbook such as Nielsen & Chuang. The *Further reading* chapter lists free resources for both.

## Building the PDF yourself

The book is written in Markdown and built into a PDF with a small Node.js script.

Requirements: [Node.js](https://nodejs.org) 18 or newer, and Microsoft Edge or Google Chrome installed.

```bash
npm install
node build.js
```

The script writes `Quantum-Computing-Gently.pdf` in the project folder.

### Project layout

```
kapitel/      chapters as Markdown, read in file-name order
titel.html    title page and imprint
stil.css      page layout and typography
circuit.js    turns text descriptions of quantum circuits into SVG
build.js      Markdown → HTML → PDF
```

### Writing conventions

Quantum circuits are written as small text blocks and drawn automatically:

```circuit
in: |0⟩; |0⟩
H 0
CNOT 0 1
M 0; M 1
```

Each line is one time step; gates in the same step are separated by `;`. Supported gates include single-qubit boxes (`H 0`, `R_z(θ) 1`), `CNOT c t` (several controls as `CNOT 0,1 2`), `CZ`, `SWAP`, controlled boxes (`C U 0 1`), classically controlled gates (`CC X 1 2`), multi-qubit boxes (`BOX "U_f" 0-2`), measurements (`M 0`) and `BARRIER`. See the comment at the top of `circuit.js` for the full syntax.

Matrices use the shorthand `[[a, b; c, d]]` (rows separated by `;`). Other figures are inline SVG.

## Contributing

Found a mistake, an unclear explanation or a broken figure? Contributions are very welcome.

- **Errors and typos:** open an issue with the page or section number, or send a pull request that edits the chapter file in `kapitel/`.
- **Better explanations:** if a passage confused you, please say so; that is exactly the feedback this book needs.
- **Translations:** the licence allows them, and they are encouraged. Please keep the same licence and credit the original.

Please run `node build.js` before submitting a pull request, to check that the PDF still builds.

## License

Text and figures are licensed under [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/).

You may copy, share, print, translate and adapt the book, including for commercial use, as long as you credit the author and release any adapted version under the same licence.

## Citation

```
Kaiser, Quantum Computing, Gently: An introduction for people who have never
studied physics or computer science. Version 1.0, January 2026.
Licensed under CC BY-SA 4.0.
```
