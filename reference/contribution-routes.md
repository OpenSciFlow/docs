# Contribution routes

OpenSciFlow is early. The best contributions are small corrections, focused reviews, and concrete workflow examples.

## If you maintain an upstream project

Use this route if OpenSciFlow lists your project or drafts a manifest for it.

Best places:

- Landscape corrections: https://github.com/OpenSciFlow/awesome-ai4s-workflows/issues
- Manifest corrections: https://github.com/OpenSciFlow/plugin-manifest/issues
- Outreach/process concerns: https://github.com/OpenSciFlow/community/issues

Helpful corrections:

- project classification;
- canonical repository or documentation URL;
- required citation;
- license and model-weight terms;
- inputs and outputs;
- installation or execution requirements;
- warnings, misuse risks, and scientific limitations.

No integration work is expected from upstream maintainers.

## If you want to review a plugin manifest

Start here:

- https://github.com/OpenSciFlow/plugin-manifest

Review checklist:

- Does the command template match upstream usage?
- Are required inputs and outputs explicit?
- Are model weights, data, and environment requirements represented correctly?
- Is a dry run or smoke test possible?
- Are license and citation fields clear?
- Are scientific limitations stated before execution?

## If you want to propose a workflow template

Start here:

- https://github.com/OpenSciFlow/workflow-templates

A good v0.1 workflow template should include:

- task scope;
- required and optional tools;
- ordered steps;
- expected artifacts;
- validation level;
- estimated runtime;
- limitations;
- citation and license propagation.

Avoid broad "autonomous scientist" workflows. Start with a narrow, repeatable task.

## If you want to test the reference prototype

Start here:

- https://github.com/OpenSciFlow/biopilot-prototype

The first target is:

```text
Protein MD Stability Report Lite
```

Useful feedback:

- whether the MVP acceptance criteria are realistic;
- whether the run-record fields are sufficient;
- whether the sample-data policy is too strict or too loose;
- whether report limitations are clear.

## If you want to contribute to the white paper

Start here:

- https://github.com/OpenSciFlow/whitepaper
- https://github.com/OpenSciFlow/whitepaper/blob/main/policies/authorship.md

White paper authorship requires substantial intellectual contribution to framing, standard design, architecture, analysis, or writing. Smaller corrections should be acknowledged.

## If you found a risky or misleading claim

Open an issue in the most relevant repository and mark the concern clearly:

- false partnership implication;
- unsupported scientific claim;
- unsafe execution assumption;
- unclear license or citation;
- clinical or drug-development overclaim.

OpenSciFlow should revise or remove misleading material quickly.
