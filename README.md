# commanded-guidelines

- Add `version` field to all events.
- Add `at` timestamp field to all events.
- Add `by` field to all events.
- Avoid nested maps inside of events because Commanded decodes all keys as atoms.
- Be wary of maps inside of Process Manager state, because Commanded decodes all of the keys as atoms.  This can be problematic if the keys are related to user input in any way, leading to a potential memory leak.
- Add sleep retries to all projectors.
- Try to have a "Create" or "New" command that initializes an aggregate.  Trying to make an aggregate command-order-agnostic is tricky.
- All commands in the router should have a prefix to make debugging easier to avoid collisions.
- If two different aggregates have the same identity, they probably should be the same aggregate.
- Have separate test modules for the `CommandFactory` and the `EventFactory`.  
