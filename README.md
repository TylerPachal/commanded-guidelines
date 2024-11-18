# commanded-guidelines

- Add `version` field to all events.
- Add `at` timestamp field to all events.
- Add `by` field to all events.
- Avoid nested maps inside of events because Commanded decodes the keys as atoms.
- Add sleep retries to all projectors.
- Try to have a "Create" or "New" command that initializes an aggregate.  Trying to make an aggregate command-order-agnostic is tricky.
