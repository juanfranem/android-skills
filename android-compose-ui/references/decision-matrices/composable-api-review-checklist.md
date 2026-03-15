# Composable API Review Checklist

- Required parameters first, `modifier` as the first optional parameter, optional tuning after that, and the main content lambda last.
- Defaults keep the common call site short and named arguments still read clearly.
- Slot and lambda order make structural customization obvious without forcing a DSL.
- State ownership is explicit: stateless values and callbacks first, hoisted state only when it clarifies the contract.
- Broad mutable parameters, unstable public types, or hidden locals do not smuggle complexity into the surface area.
