# Screen Chrome Review Checklist

- Status and navigation bars: confirm content, app bars, and gestures do not collide with occupied system-bar space.
- Keyboard occlusion: confirm focused fields, submit actions, and validation messages remain visible when the IME shows.
- Scroll reachability: confirm the screen can still scroll or reposition to the focused field instead of trapping it below the keyboard.
- Edge-to-edge assumptions: confirm each screen intentionally owns or rejects edge-to-edge treatment rather than inheriting it blindly.
- Overlays and sheets: confirm transient surfaces handle system bars, keyboard overlap, and dismissal affordances independently of the base screen.
- Form shells: confirm long forms, sticky actions, and mixed static-plus-scroll layouts still work when the keyboard appears.
