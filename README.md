# FPSU FeatureMap

A feature inventory connected to the shared primitives and components an application actually uses.

FPSU FeatureMap brings four things together:

- **Art direction.** The intended visual style and references.
- **Primitives.** Shared variables for colors, sizes, spacing, corners and typography.
- **Components.** Reusable code built from those primitives.
- **Features.** The complete inventory of what the software does, organized by domain, feature and sub-feature, with exact code names for the primitives and components it uses.

Features without an interface belong in the inventory too. Visual details apply only where an interface exists.

## Why keep them together?

A feature description should point to the real components, not describe a second, disconnected version of the interface. Components should use shared definitions rather than copied values or code.

Changing a shared definition changes its consumers. The map makes those definitions and their uses easier to find before adding or changing a feature.

## The standard

Read [FPSU-FEATUREMAP.md](FPSU-FEATUREMAP.md) for the complete standard, in its original French wording.

It covers the intent, definition of a feature, folder organization, working instructions, maintenance triggers and map format. This repository publishes the method, not a map of FPSU's private products.

## Use it in a project

1. Give your coding agent the [standard](FPSU-FEATUREMAP.md) as part of its project instructions.
2. Keep a `FeatureMap` folder at the project root. It contains the Markdown map and the shared primitive and component code used by the application.
3. Describe art direction, primitives, components and features in the map. Reference code by its actual names and locations.
4. Consult the map before adding a feature. Reuse existing visual elements by default.
5. Update the map when its content or code references change, including immediately after a referenced variable or component is renamed. Remove stale or contradictory information.

The shared code is the implementation. The Markdown describes and links to it; it does not replace it.

## Relationship to DOX

The approach was developed with [Agent Zero's DOX](https://github.com/agent0ai/dox) as a reference for concise agent instructions and documentation maintenance.

DOX describes project documentation contracts and their hierarchy. FPSU FeatureMap describes features and their relationship to shared visual code. The two can be used together without replacing the project's documentation hierarchy.

## What this is not

FPSU FeatureMap is a written standard, not a package, generator or automated synchronization tool. Applying it requires updating the project documentation and connecting the application to the shared code.

Created by FPSU.
