Solid is a language that syntactically looks very similar to React but has a major architectural difference: signals.

# Signals
Signals implement what Solid calls Fine-Grained Reactivity. Instead of enforcing a strict parent-child tree of dependencies, components have a graph like dependency where components are monitoring only the dependecies they directly rely on.
