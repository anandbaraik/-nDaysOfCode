# Eevent Propagation

Event propagation is a way to describe the “stack” of events that are fired in a web browser. Event Propagation determines in which order the elements receive the event. There are two ways to handle this event propagation order of HTML DOM is `Event Bubbling and Event Capturing/Trickling`.

# Event Bubbling

The movement of events from the bottom to top is called bubbling. can be avoid bubbling by using `e.stopPropagation()` on event.

## Difference between stopimmediatepropagation & stopPropagation

you can read about it more ![here](https://www.carlrippon.com/stoppropagation-v-stopimmediatepropagation/#:~:text=stopPropagation%20allows%20other%20event%20handlers,bubbling%20phases%20from%20being%20executed.)

## Which events do not bubble?

There are few events which don't bubble like

- HTML frame/object
  - load
  - unload
  - scroll
- HTML form
  - focus
  - blur
- Mutation
  - DOMNodeRemovedFromDocument
  - DOMNodeInsertedIntoDocument
    Progress
  - loadstart
  - progress
  - error
  - abort
  - load
  - loadend

# Event Capturing/Trickling

The movement of events from the top to bottom is called Capturing/Trickling.
