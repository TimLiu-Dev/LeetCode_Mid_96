# NOTES & Architectural Decisions

## 1. File Naming Standard: Dual Indexing
All 96 lessons follow the format:
`./lessons/{0001-0096}-lc{LeetCode#}-{slug}.html`
- **Example 1:** `0001-lc217-contains-duplicate.html`
- **Example 2:** `0002-lc1-two-sum.html`
- **Example 3:** `0067-custom-in-memory-kv-store-ttl.html` (for custom system drill)
- **Benefit:** Guarantees chronological folder sorting (0001 to 0096) while enabling instant `Cmd+P` search by official LeetCode problem ID (e.g. searching "217" or "lc217").

## 2. The Comprehensive Sections per Lesson
0. **Official Problem Statement & Comprehension Enhancers**:
   - Verbatim LeetCode description + direct link.
   - **Plain-English Translation Callout**: Strips away academic jargon into a 1-sentence real-world summary.
   - Official Examples (Input, Output, Explanation).
   - Official Constraints card.
   - **Canonical Input Shapes (Mental Boundary Checks)**: 3 visual mini-cards (Minimum base case, Best-case early exit, Worst-case full scan).
0.5. **Interactive Vector Whiteboard & Interview Sketchpad**:
   - High-DPI canvas supporting mouse, trackpad, touch, and Apple Pencil / stylus.
   - 6-color palette (Emerald, Cyan, Amber, Purple, White, Red).
   - Pen vs Eraser toggle + 3 stroke sizes (2px, 4px, 8px).
   - Vector path engine supporting instant **Undo** and **Clear**.
   - Collapsible toggle to minimize or expand anytime.
1. **The Mental Model & "Explain Like I'm 12"**: Real-world analogy + "A-Ha!" switch + pattern recognition trigger (+ 2 sister problems).
2. **The Naive Trap (Red) vs. Optimal Breakthrough (Green)**: Pinpoint wasted CPU cycles + space-time bargain table.
3. **The Concrete Variable Trace Table**: Clean state table row-by-row on a concrete test case.
4. **The Interactive Matt Pocock Visual Stepper**: Vanilla JS simulation with Reset/Prev/Next/Play, pointer arrows, live memory inspector, dynamic narration, synced pseudocode line highlight.
5. **Multi-Approach Solution Evolution & Interactive Sandbox (Kotlin → Python → Java)**:
   - **Approach Progression (Option A)**:
     - `1. Brute Force (O(N²))`: The naive baseline to state verbally in the first 45 seconds of an interview.
     - `2. Better: Sorting / Space-Time Tradeoff`: The go-to memory-constrained answer when asked *"What if extra heap allocation is forbidden?"*.
     - `★ 3. Optimal (O(N))`: The production gold standard (active by default for coding muscle memory).
   - **Tri-Language Tabs**: In every approach, languages are strictly ordered **Kotlin (Default)** $\rightarrow$ **Python** $\rightarrow$ **Java** with copy buttons and deep runtime/memory breakdowns.
   - **Interactive Code Scratchpad**: In-browser code editor with Tab indentation support, live syntax/delimiter validator, and automated test runner against official LeetCode examples.
6. **Live Interview Spoken Script & Gotchas**: 4-phase word-for-word interview script + edge cases checklist + real-world scalability follow-up.
7. **The Pocock Micro-Quiz & Practice Protocol**: 2 interactive MCQs + 48-Hour Cold Practice protocol with localStorage recall countdown timer.

## 3. Technology & Portability Rules
- **Pure Vanilla JS + Tailwind CDN**: No npm dependencies, no local dev server required. Double-clicking any HTML file opens seamlessly in any browser.
- **Interlocking Navigation**: Top breadcrumb bar + bottom footer with `← Prev Problem` and `Next Problem →` links across all 96 files.
