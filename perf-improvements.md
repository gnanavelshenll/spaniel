## Host interface
  * rAF
  * Way to wrap work queue (ember-spaniel can use this instead of clobering the default engine) (we dont need to wrap read)
  * Allow hook for host to specify when objects can be resized

## Reduce clientBoundingRect calls
  * Only update window bounds on scroll or resize event. Only if we have passive listeners to detect any user interaction.
  * Passive listeners are only needed where the callback can preventDefault()
  * Cache the window bounds, not the entire boudingRect object
  * Heuristics to avoid polling when we believe the system to be stable

## Support scrolling divs
  * Allow manual declaration of root element

## Chrome Tracing!!!

Then release V3