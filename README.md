Design iteration loop:                                                                                                                                                            
Figma  →  Claude Code implements changes in HTML  →  git push  →  colleague git pull
                                                                                                                                                                                    
Sending screens back to Figma:                            
Edit HTML locally  →  capture to Figma  →  git push

One thing to note — Figma and the HTML don't sync automatically in either direction. Each handoff is a deliberate step:

- Figma → Code: You share the Figma URL with me, I read the design and make changes to the HTML files
- Code → Figma: You ask me to send screens, I run the capture workflow (Python server + browser tabs)

So the full picture looks like this:

You (design)          Figma ←──── capture screens ────┐
                         │                              │
                         │ share URL / describe changes │
                         ↓                              │
You (code)       Claude Code edits HTML ───────────────┘
                         │
                      git push
                         │
                         ↓
Colleague          git pull → makes their own edits → git push

Both you and your colleague are always working from the same source of truth (GitHub), and Figma stays updated when you deliberately push screens to it.
