# Interactive Throttle vs. Debounce Demo

This is an interactive throttling and debouncing process at play.

**[➡️ Link](https://manjilj.github.io/throttle-debounce/srcd)** 

**Implements the Functions:**
 
    - `throttle()`
    - `debounceTrailing()`
    - `debounceLeading()`
    - `debounceByCount()`

## Key Concepts to Understand

- **Throttling:** Enforces a maximum frequency. It's about executing a function at most once per time interval called "rate-limiting".

- **Debouncing:** Groups a burst of events into a single one. It's about waiting for a pause before executing. 

💡 Pro-Tip for Testing Throttle:
To best visualize the Throttle (Leading Edge), do not type a sentence (though you may with less distinct visual effect). Instead, press and hold a single key (e.g., aaaaa or asdfasdfasdfg etc. typed rapidly). You will see every first character fire immediately, while all subsequent auto-repeats are blocked by the cooldown. To truly test the "Gate," randomly release and re-hold the character/s in a rapid, repetitive cycle; you will observe how every event is ignored until the visual timer clears, proving the logic maintains a strict execution interval regardless of how many times the character/s get/s toggled.

This sequence also provides a perfect mental model for how high-frequency browser events—like scrolling—are managed. Just as the throttle limits these rapid key-repeats to a single execution, it ensures a scroll handler only fires at a fixed, sustainable rate, preventing the UI from lagging under a constant stream of "scroll" events.